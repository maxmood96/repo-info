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
$ docker pull ros@sha256:ffcf6bbd1d13815d20c60c7afa4f76d1ca71d66602934fc93ecce3cedf6bc3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:7c2f84cfe223cc6f4f94346ce62f760d030e36354723e821e1f22545cc1112c4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263323429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a9b05df63f7c45dd46ccdddab1bfb025bbd870bc4edbca63217fc58d99c95a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 06:13:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:13:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:13:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:13:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:14:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:14:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:14:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6ad111ea9e627c5ddd919cccc3f44a8ffe7ba3b24068fae2b35143321f834`  
		Last Modified: Tue, 02 Jul 2024 06:27:23 GMT  
		Size: 106.5 MB (106534706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1089c45a27fa6775af871e4c2a4fe847d10f55db1aeddfc745406207518119`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc28a3d8ba8d4113899198db9fd697dcd7c545f49b1063b676a5198b5fcf9f3`  
		Last Modified: Tue, 02 Jul 2024 06:27:43 GMT  
		Size: 98.1 MB (98145979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe07c304cdbbeac013841c1866ea8f65b3cc60b250758c177aa7225cda40021a`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 329.5 KB (329506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e75bb1bfb3eb97b0e2abdaa51660f203f2fc4bd967f467f977b4bf5ad86e5e6`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2055f9c9cc67e0e78e21d16d3cf2c9ba4a63fbc9dcf4427fc942f8f189df4`  
		Last Modified: Tue, 02 Jul 2024 06:27:34 GMT  
		Size: 22.8 MB (22824049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3f69e9df8d99de535ea34dab96ad2127643e1dedcc72213fd90a3d8c0445a7c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255963688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04c14e5337fa54b4cb81c4401cefd471a1f1bb26c45505685ea7c8641f98af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:40:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:40:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a0fb56b7f1e4b815ae336e390970c0f24f893dd71218daf35b302a34dd4a9`  
		Last Modified: Tue, 02 Jul 2024 04:55:41 GMT  
		Size: 95.7 MB (95715416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bed3eca41259a671dec69d55ff9184d01d25d1655ec828ec45204579b6df29`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 329.5 KB (329499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3ca19b14268fc7aed9d9edab3b959ea7a2551523997a1250b2b297528dd662`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ca8ad62e3384aca8bf996f68146f47006029f9094904a72f297d5021c9a7b`  
		Last Modified: Tue, 02 Jul 2024 04:55:32 GMT  
		Size: 22.2 MB (22236600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:3aacd66a9c7b1789495997f92ec9d8da8334e6e8bca25732e86fbc07c67d930e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:191aaa65c6f079e29c1b009402cd53ec4151134bf1be5b8d00be9ea8af8f0e00
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.9 MB (954893842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb3d9147c655081d54ba105d7321de64c7ff681bbfee1d0a49dbf86347bb2f9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 06:13:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:13:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:13:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:13:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:14:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:14:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:14:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:21:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6ad111ea9e627c5ddd919cccc3f44a8ffe7ba3b24068fae2b35143321f834`  
		Last Modified: Tue, 02 Jul 2024 06:27:23 GMT  
		Size: 106.5 MB (106534706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1089c45a27fa6775af871e4c2a4fe847d10f55db1aeddfc745406207518119`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc28a3d8ba8d4113899198db9fd697dcd7c545f49b1063b676a5198b5fcf9f3`  
		Last Modified: Tue, 02 Jul 2024 06:27:43 GMT  
		Size: 98.1 MB (98145979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe07c304cdbbeac013841c1866ea8f65b3cc60b250758c177aa7225cda40021a`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 329.5 KB (329506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e75bb1bfb3eb97b0e2abdaa51660f203f2fc4bd967f467f977b4bf5ad86e5e6`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2055f9c9cc67e0e78e21d16d3cf2c9ba4a63fbc9dcf4427fc942f8f189df4`  
		Last Modified: Tue, 02 Jul 2024 06:27:34 GMT  
		Size: 22.8 MB (22824049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e2d84f2e1bd771c94e90f8efccd97606d4d11741b815cc758a8b2b88452575`  
		Last Modified: Tue, 02 Jul 2024 06:29:20 GMT  
		Size: 691.6 MB (691570413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ee40053af58c37010977f74761ffda66d2cf680293a48656aff8e49c2fe66bf2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.4 MB (915449931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4effc3cabe26473746f30726a09937b3506fd116ee347f4494221776a65377`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:40:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:40:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:50:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a0fb56b7f1e4b815ae336e390970c0f24f893dd71218daf35b302a34dd4a9`  
		Last Modified: Tue, 02 Jul 2024 04:55:41 GMT  
		Size: 95.7 MB (95715416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bed3eca41259a671dec69d55ff9184d01d25d1655ec828ec45204579b6df29`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 329.5 KB (329499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3ca19b14268fc7aed9d9edab3b959ea7a2551523997a1250b2b297528dd662`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ca8ad62e3384aca8bf996f68146f47006029f9094904a72f297d5021c9a7b`  
		Last Modified: Tue, 02 Jul 2024 04:55:32 GMT  
		Size: 22.2 MB (22236600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55de3ffa3a7b727436f175ee25b99e280bffa6b8e2e07484f4f0f83837f60b57`  
		Last Modified: Tue, 02 Jul 2024 04:56:53 GMT  
		Size: 659.5 MB (659486243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:3aacd66a9c7b1789495997f92ec9d8da8334e6e8bca25732e86fbc07c67d930e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:191aaa65c6f079e29c1b009402cd53ec4151134bf1be5b8d00be9ea8af8f0e00
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.9 MB (954893842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb3d9147c655081d54ba105d7321de64c7ff681bbfee1d0a49dbf86347bb2f9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 06:13:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:13:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:13:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:13:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:14:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:14:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:14:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:21:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6ad111ea9e627c5ddd919cccc3f44a8ffe7ba3b24068fae2b35143321f834`  
		Last Modified: Tue, 02 Jul 2024 06:27:23 GMT  
		Size: 106.5 MB (106534706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1089c45a27fa6775af871e4c2a4fe847d10f55db1aeddfc745406207518119`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc28a3d8ba8d4113899198db9fd697dcd7c545f49b1063b676a5198b5fcf9f3`  
		Last Modified: Tue, 02 Jul 2024 06:27:43 GMT  
		Size: 98.1 MB (98145979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe07c304cdbbeac013841c1866ea8f65b3cc60b250758c177aa7225cda40021a`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 329.5 KB (329506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e75bb1bfb3eb97b0e2abdaa51660f203f2fc4bd967f467f977b4bf5ad86e5e6`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2055f9c9cc67e0e78e21d16d3cf2c9ba4a63fbc9dcf4427fc942f8f189df4`  
		Last Modified: Tue, 02 Jul 2024 06:27:34 GMT  
		Size: 22.8 MB (22824049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e2d84f2e1bd771c94e90f8efccd97606d4d11741b815cc758a8b2b88452575`  
		Last Modified: Tue, 02 Jul 2024 06:29:20 GMT  
		Size: 691.6 MB (691570413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ee40053af58c37010977f74761ffda66d2cf680293a48656aff8e49c2fe66bf2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.4 MB (915449931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4effc3cabe26473746f30726a09937b3506fd116ee347f4494221776a65377`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:40:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:40:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:50:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a0fb56b7f1e4b815ae336e390970c0f24f893dd71218daf35b302a34dd4a9`  
		Last Modified: Tue, 02 Jul 2024 04:55:41 GMT  
		Size: 95.7 MB (95715416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bed3eca41259a671dec69d55ff9184d01d25d1655ec828ec45204579b6df29`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 329.5 KB (329499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3ca19b14268fc7aed9d9edab3b959ea7a2551523997a1250b2b297528dd662`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ca8ad62e3384aca8bf996f68146f47006029f9094904a72f297d5021c9a7b`  
		Last Modified: Tue, 02 Jul 2024 04:55:32 GMT  
		Size: 22.2 MB (22236600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55de3ffa3a7b727436f175ee25b99e280bffa6b8e2e07484f4f0f83837f60b57`  
		Last Modified: Tue, 02 Jul 2024 04:56:53 GMT  
		Size: 659.5 MB (659486243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:ffcf6bbd1d13815d20c60c7afa4f76d1ca71d66602934fc93ecce3cedf6bc3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:7c2f84cfe223cc6f4f94346ce62f760d030e36354723e821e1f22545cc1112c4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263323429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a9b05df63f7c45dd46ccdddab1bfb025bbd870bc4edbca63217fc58d99c95a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 06:13:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:13:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:13:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:13:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:14:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:14:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:14:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6ad111ea9e627c5ddd919cccc3f44a8ffe7ba3b24068fae2b35143321f834`  
		Last Modified: Tue, 02 Jul 2024 06:27:23 GMT  
		Size: 106.5 MB (106534706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1089c45a27fa6775af871e4c2a4fe847d10f55db1aeddfc745406207518119`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc28a3d8ba8d4113899198db9fd697dcd7c545f49b1063b676a5198b5fcf9f3`  
		Last Modified: Tue, 02 Jul 2024 06:27:43 GMT  
		Size: 98.1 MB (98145979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe07c304cdbbeac013841c1866ea8f65b3cc60b250758c177aa7225cda40021a`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 329.5 KB (329506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e75bb1bfb3eb97b0e2abdaa51660f203f2fc4bd967f467f977b4bf5ad86e5e6`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2055f9c9cc67e0e78e21d16d3cf2c9ba4a63fbc9dcf4427fc942f8f189df4`  
		Last Modified: Tue, 02 Jul 2024 06:27:34 GMT  
		Size: 22.8 MB (22824049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3f69e9df8d99de535ea34dab96ad2127643e1dedcc72213fd90a3d8c0445a7c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255963688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04c14e5337fa54b4cb81c4401cefd471a1f1bb26c45505685ea7c8641f98af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:40:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:40:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a0fb56b7f1e4b815ae336e390970c0f24f893dd71218daf35b302a34dd4a9`  
		Last Modified: Tue, 02 Jul 2024 04:55:41 GMT  
		Size: 95.7 MB (95715416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bed3eca41259a671dec69d55ff9184d01d25d1655ec828ec45204579b6df29`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 329.5 KB (329499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3ca19b14268fc7aed9d9edab3b959ea7a2551523997a1250b2b297528dd662`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ca8ad62e3384aca8bf996f68146f47006029f9094904a72f297d5021c9a7b`  
		Last Modified: Tue, 02 Jul 2024 04:55:32 GMT  
		Size: 22.2 MB (22236600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:ffcf6bbd1d13815d20c60c7afa4f76d1ca71d66602934fc93ecce3cedf6bc3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:7c2f84cfe223cc6f4f94346ce62f760d030e36354723e821e1f22545cc1112c4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263323429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a9b05df63f7c45dd46ccdddab1bfb025bbd870bc4edbca63217fc58d99c95a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 06:13:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:13:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:13:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:13:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:14:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:14:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:14:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6ad111ea9e627c5ddd919cccc3f44a8ffe7ba3b24068fae2b35143321f834`  
		Last Modified: Tue, 02 Jul 2024 06:27:23 GMT  
		Size: 106.5 MB (106534706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1089c45a27fa6775af871e4c2a4fe847d10f55db1aeddfc745406207518119`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc28a3d8ba8d4113899198db9fd697dcd7c545f49b1063b676a5198b5fcf9f3`  
		Last Modified: Tue, 02 Jul 2024 06:27:43 GMT  
		Size: 98.1 MB (98145979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe07c304cdbbeac013841c1866ea8f65b3cc60b250758c177aa7225cda40021a`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 329.5 KB (329506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e75bb1bfb3eb97b0e2abdaa51660f203f2fc4bd967f467f977b4bf5ad86e5e6`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2055f9c9cc67e0e78e21d16d3cf2c9ba4a63fbc9dcf4427fc942f8f189df4`  
		Last Modified: Tue, 02 Jul 2024 06:27:34 GMT  
		Size: 22.8 MB (22824049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3f69e9df8d99de535ea34dab96ad2127643e1dedcc72213fd90a3d8c0445a7c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255963688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04c14e5337fa54b4cb81c4401cefd471a1f1bb26c45505685ea7c8641f98af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:40:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:40:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a0fb56b7f1e4b815ae336e390970c0f24f893dd71218daf35b302a34dd4a9`  
		Last Modified: Tue, 02 Jul 2024 04:55:41 GMT  
		Size: 95.7 MB (95715416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bed3eca41259a671dec69d55ff9184d01d25d1655ec828ec45204579b6df29`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 329.5 KB (329499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3ca19b14268fc7aed9d9edab3b959ea7a2551523997a1250b2b297528dd662`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ca8ad62e3384aca8bf996f68146f47006029f9094904a72f297d5021c9a7b`  
		Last Modified: Tue, 02 Jul 2024 04:55:32 GMT  
		Size: 22.2 MB (22236600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:3193cbfbea1206ee3ff9de0db05d5966ad7bc06678bfdd81920b8c9fb9b4de14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:eb1e1df640e98ef44dae24f9f7ef51489efcc548e776bbf48d0bee1e1edd5465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140908480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af43d69053fc59b45358d995c484701e274ae2d96372c405bbbfb9559a6b9eb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1edf04025a122811e708ccc8040d53a46e573f84b68d5247d9588ac36b74b7`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 1.2 MB (1214732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3a9afb6d76657fc94397c228fd19083463ec0fe70881d152e5ba5b040054d4`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 3.6 MB (3624561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85780c0ead4f3a7f56e455d70f23d79210a63e1ba6103e67128cb281318b83`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34432dd821bdfd3e40b782714a265caf961044dbff025c9fc02e176f4bd90f`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab814f3f3a32d87ca5c6bde7c77d2578379a6cc59be2c305126c1aae06b0591`  
		Last Modified: Fri, 05 Jul 2024 19:57:18 GMT  
		Size: 106.5 MB (106532664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88c71908435c810f2f816f9b482653ca9899fb8aa44f1478df5aba224ab6e27`  
		Last Modified: Fri, 05 Jul 2024 19:57:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ac921bd22cff2f99946d1ad629b0ace7d46332b073f2f96b4926500e795ce088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16883717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b77d9ed4c477cdada4622088996561c8a7f4660324e3032caa8aca06a919eb`

```dockerfile
```

-	Layers:
	-	`sha256:395e09817bbcc0a45d7d548ae7d77a609a3c9cee3289b99ee7306ba44692db1f`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 16.9 MB (16867580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b470888f8b64d739e558349d01218eb2a5ba489570fff6c07d7ed338f4438b`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:83aa819731f39b0abb83eb438ae4464df909892bc8ee99355d1acc2f9fdb01c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137679738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2732ba8618deb2ce3ae0837f2ad92b9f0b2ab1d60e4cd0c7c0dcf61d7b0c6752`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:3193cbfbea1206ee3ff9de0db05d5966ad7bc06678bfdd81920b8c9fb9b4de14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:eb1e1df640e98ef44dae24f9f7ef51489efcc548e776bbf48d0bee1e1edd5465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140908480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af43d69053fc59b45358d995c484701e274ae2d96372c405bbbfb9559a6b9eb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1edf04025a122811e708ccc8040d53a46e573f84b68d5247d9588ac36b74b7`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 1.2 MB (1214732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3a9afb6d76657fc94397c228fd19083463ec0fe70881d152e5ba5b040054d4`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 3.6 MB (3624561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85780c0ead4f3a7f56e455d70f23d79210a63e1ba6103e67128cb281318b83`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34432dd821bdfd3e40b782714a265caf961044dbff025c9fc02e176f4bd90f`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab814f3f3a32d87ca5c6bde7c77d2578379a6cc59be2c305126c1aae06b0591`  
		Last Modified: Fri, 05 Jul 2024 19:57:18 GMT  
		Size: 106.5 MB (106532664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88c71908435c810f2f816f9b482653ca9899fb8aa44f1478df5aba224ab6e27`  
		Last Modified: Fri, 05 Jul 2024 19:57:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:ac921bd22cff2f99946d1ad629b0ace7d46332b073f2f96b4926500e795ce088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16883717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b77d9ed4c477cdada4622088996561c8a7f4660324e3032caa8aca06a919eb`

```dockerfile
```

-	Layers:
	-	`sha256:395e09817bbcc0a45d7d548ae7d77a609a3c9cee3289b99ee7306ba44692db1f`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 16.9 MB (16867580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b470888f8b64d739e558349d01218eb2a5ba489570fff6c07d7ed338f4438b`  
		Last Modified: Fri, 05 Jul 2024 19:57:16 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:83aa819731f39b0abb83eb438ae4464df909892bc8ee99355d1acc2f9fdb01c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137679738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2732ba8618deb2ce3ae0837f2ad92b9f0b2ab1d60e4cd0c7c0dcf61d7b0c6752`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:9d1eaeb3445b6895eca1cf02e122e979a44bb9376f6fae1b7ce9df98a0d9ffb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:4c19d95dac345f57f945cc4322e328f1d0369316e4442c55fbe0b5f1053cee3c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269041898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd874b4161f2dad2ed935ab7d27d7d0849f5330a89b1dc28f99c853fc03d44b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:22:21 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 06:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:23:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:23:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:23:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:24:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6035e0c20aa9a6a0e72cf291215a36408ff518e0b9da966329c30f8c9580a36`  
		Last Modified: Tue, 02 Jul 2024 06:29:47 GMT  
		Size: 124.3 MB (124331033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c982681289ab5fec9bc8ad601404cf9b8cf253486448949dd554ae96b169dc53`  
		Last Modified: Tue, 02 Jul 2024 06:29:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3dd9ed9a2217783c07c06264630b1d38f0f53924faa3d7be94edee1f46a5d2`  
		Last Modified: Tue, 02 Jul 2024 06:30:05 GMT  
		Size: 85.2 MB (85177019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6602c7f18082b5d3dad3c904b267f744d9b5549b8f4d1b0e6a4ef7711953cd`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 309.1 KB (309061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03594b9a6a50634d9d79b7783fc18c923e0da60100953a1d7c9e7b430e7f86f4`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4948e4b0173081d9719e580a03997444c2a559883e955f0fbb92d2d3c5c5f5cc`  
		Last Modified: Tue, 02 Jul 2024 06:29:58 GMT  
		Size: 23.7 MB (23735580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:16d2b3738a331abe3e244afd17bdedc6d56784b15fda5c2c9a2c1f01c2542a3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261510145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6b324397fa8b290c69e2c123d187c85bacf69fb08e232e4d8aa51831882617`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:50:55 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 04:51:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:51:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:51:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:51:42 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:52:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:52:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:52:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:52:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30cdc1a9ff2f9ebf8213a700af558357b58ae913c7e61edcb1d27a280e6ad96`  
		Last Modified: Tue, 02 Jul 2024 04:57:16 GMT  
		Size: 121.8 MB (121787632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08fbb2991af2e722c40559a15cb594a3c45661508bc2b7949ea31be77da61b5`  
		Last Modified: Tue, 02 Jul 2024 04:57:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318e763e20b58a15dcf9b1149f8fd8e451417b06f70ea72ed5efd37d9c81bb5`  
		Last Modified: Tue, 02 Jul 2024 04:57:31 GMT  
		Size: 82.9 MB (82864796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2b526fed218337f0520e3445d0429a8fa8bfe0ac52b6a4b3f33185b01d52a7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 309.1 KB (309054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c90e04e32de4d9cc1872a0e6b6145c9249699644d747bff9a66798f07053ec7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293d50e1335efefa8a6cdb594118dd02584b001e0ce1e50c126cadd5d805544`  
		Last Modified: Tue, 02 Jul 2024 04:57:26 GMT  
		Size: 23.1 MB (23125986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:57d5330559ed0df42fb0b093fc1901b60282f77a3caaffd9a197e3ab83f086c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:47df8429d108a81cb9156e4cfe4076c71b3e5824948654ed104d59c0a8727191
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.4 MB (961381346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719c5ab476d3208dd75305ef2361f4071967a6156d7bf4e08deb610da88ba6a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:22:21 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 06:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:23:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:23:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:23:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:24:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:26:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6035e0c20aa9a6a0e72cf291215a36408ff518e0b9da966329c30f8c9580a36`  
		Last Modified: Tue, 02 Jul 2024 06:29:47 GMT  
		Size: 124.3 MB (124331033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c982681289ab5fec9bc8ad601404cf9b8cf253486448949dd554ae96b169dc53`  
		Last Modified: Tue, 02 Jul 2024 06:29:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3dd9ed9a2217783c07c06264630b1d38f0f53924faa3d7be94edee1f46a5d2`  
		Last Modified: Tue, 02 Jul 2024 06:30:05 GMT  
		Size: 85.2 MB (85177019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6602c7f18082b5d3dad3c904b267f744d9b5549b8f4d1b0e6a4ef7711953cd`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 309.1 KB (309061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03594b9a6a50634d9d79b7783fc18c923e0da60100953a1d7c9e7b430e7f86f4`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4948e4b0173081d9719e580a03997444c2a559883e955f0fbb92d2d3c5c5f5cc`  
		Last Modified: Tue, 02 Jul 2024 06:29:58 GMT  
		Size: 23.7 MB (23735580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af257a623f983e2e8d42742126bbf11bc7bbf9f8dcde0becc5e67315d8c78f09`  
		Last Modified: Tue, 02 Jul 2024 06:31:43 GMT  
		Size: 692.3 MB (692339448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7164a41db893aecc6fc0bba88604f7a07666bad9a15b29d417277fc3bad39e79
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.7 MB (921691478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e44a58f57c90284a6043f5c00d27b64a9e0cbdb65dfc653f39648ac6d10bbbe`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:50:55 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 04:51:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:51:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:51:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:51:42 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:52:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:52:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:52:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:52:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:54:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30cdc1a9ff2f9ebf8213a700af558357b58ae913c7e61edcb1d27a280e6ad96`  
		Last Modified: Tue, 02 Jul 2024 04:57:16 GMT  
		Size: 121.8 MB (121787632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08fbb2991af2e722c40559a15cb594a3c45661508bc2b7949ea31be77da61b5`  
		Last Modified: Tue, 02 Jul 2024 04:57:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318e763e20b58a15dcf9b1149f8fd8e451417b06f70ea72ed5efd37d9c81bb5`  
		Last Modified: Tue, 02 Jul 2024 04:57:31 GMT  
		Size: 82.9 MB (82864796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2b526fed218337f0520e3445d0429a8fa8bfe0ac52b6a4b3f33185b01d52a7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 309.1 KB (309054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c90e04e32de4d9cc1872a0e6b6145c9249699644d747bff9a66798f07053ec7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293d50e1335efefa8a6cdb594118dd02584b001e0ce1e50c126cadd5d805544`  
		Last Modified: Tue, 02 Jul 2024 04:57:26 GMT  
		Size: 23.1 MB (23125986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ae3db0abb1c48789d6032454829c6b30955dce1bab1fb652d74a4395dbf6df`  
		Last Modified: Tue, 02 Jul 2024 04:58:43 GMT  
		Size: 660.2 MB (660181333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:57d5330559ed0df42fb0b093fc1901b60282f77a3caaffd9a197e3ab83f086c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:47df8429d108a81cb9156e4cfe4076c71b3e5824948654ed104d59c0a8727191
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.4 MB (961381346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719c5ab476d3208dd75305ef2361f4071967a6156d7bf4e08deb610da88ba6a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:22:21 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 06:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:23:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:23:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:23:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:24:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:26:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6035e0c20aa9a6a0e72cf291215a36408ff518e0b9da966329c30f8c9580a36`  
		Last Modified: Tue, 02 Jul 2024 06:29:47 GMT  
		Size: 124.3 MB (124331033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c982681289ab5fec9bc8ad601404cf9b8cf253486448949dd554ae96b169dc53`  
		Last Modified: Tue, 02 Jul 2024 06:29:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3dd9ed9a2217783c07c06264630b1d38f0f53924faa3d7be94edee1f46a5d2`  
		Last Modified: Tue, 02 Jul 2024 06:30:05 GMT  
		Size: 85.2 MB (85177019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6602c7f18082b5d3dad3c904b267f744d9b5549b8f4d1b0e6a4ef7711953cd`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 309.1 KB (309061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03594b9a6a50634d9d79b7783fc18c923e0da60100953a1d7c9e7b430e7f86f4`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4948e4b0173081d9719e580a03997444c2a559883e955f0fbb92d2d3c5c5f5cc`  
		Last Modified: Tue, 02 Jul 2024 06:29:58 GMT  
		Size: 23.7 MB (23735580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af257a623f983e2e8d42742126bbf11bc7bbf9f8dcde0becc5e67315d8c78f09`  
		Last Modified: Tue, 02 Jul 2024 06:31:43 GMT  
		Size: 692.3 MB (692339448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7164a41db893aecc6fc0bba88604f7a07666bad9a15b29d417277fc3bad39e79
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.7 MB (921691478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e44a58f57c90284a6043f5c00d27b64a9e0cbdb65dfc653f39648ac6d10bbbe`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:50:55 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 04:51:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:51:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:51:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:51:42 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:52:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:52:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:52:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:52:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:54:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30cdc1a9ff2f9ebf8213a700af558357b58ae913c7e61edcb1d27a280e6ad96`  
		Last Modified: Tue, 02 Jul 2024 04:57:16 GMT  
		Size: 121.8 MB (121787632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08fbb2991af2e722c40559a15cb594a3c45661508bc2b7949ea31be77da61b5`  
		Last Modified: Tue, 02 Jul 2024 04:57:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318e763e20b58a15dcf9b1149f8fd8e451417b06f70ea72ed5efd37d9c81bb5`  
		Last Modified: Tue, 02 Jul 2024 04:57:31 GMT  
		Size: 82.9 MB (82864796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2b526fed218337f0520e3445d0429a8fa8bfe0ac52b6a4b3f33185b01d52a7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 309.1 KB (309054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c90e04e32de4d9cc1872a0e6b6145c9249699644d747bff9a66798f07053ec7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293d50e1335efefa8a6cdb594118dd02584b001e0ce1e50c126cadd5d805544`  
		Last Modified: Tue, 02 Jul 2024 04:57:26 GMT  
		Size: 23.1 MB (23125986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ae3db0abb1c48789d6032454829c6b30955dce1bab1fb652d74a4395dbf6df`  
		Last Modified: Tue, 02 Jul 2024 04:58:43 GMT  
		Size: 660.2 MB (660181333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:9d1eaeb3445b6895eca1cf02e122e979a44bb9376f6fae1b7ce9df98a0d9ffb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:4c19d95dac345f57f945cc4322e328f1d0369316e4442c55fbe0b5f1053cee3c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269041898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd874b4161f2dad2ed935ab7d27d7d0849f5330a89b1dc28f99c853fc03d44b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:22:21 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 06:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:23:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:23:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:23:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:24:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6035e0c20aa9a6a0e72cf291215a36408ff518e0b9da966329c30f8c9580a36`  
		Last Modified: Tue, 02 Jul 2024 06:29:47 GMT  
		Size: 124.3 MB (124331033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c982681289ab5fec9bc8ad601404cf9b8cf253486448949dd554ae96b169dc53`  
		Last Modified: Tue, 02 Jul 2024 06:29:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3dd9ed9a2217783c07c06264630b1d38f0f53924faa3d7be94edee1f46a5d2`  
		Last Modified: Tue, 02 Jul 2024 06:30:05 GMT  
		Size: 85.2 MB (85177019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6602c7f18082b5d3dad3c904b267f744d9b5549b8f4d1b0e6a4ef7711953cd`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 309.1 KB (309061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03594b9a6a50634d9d79b7783fc18c923e0da60100953a1d7c9e7b430e7f86f4`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4948e4b0173081d9719e580a03997444c2a559883e955f0fbb92d2d3c5c5f5cc`  
		Last Modified: Tue, 02 Jul 2024 06:29:58 GMT  
		Size: 23.7 MB (23735580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:16d2b3738a331abe3e244afd17bdedc6d56784b15fda5c2c9a2c1f01c2542a3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261510145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6b324397fa8b290c69e2c123d187c85bacf69fb08e232e4d8aa51831882617`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:50:55 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 04:51:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:51:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:51:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:51:42 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:52:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:52:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:52:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:52:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30cdc1a9ff2f9ebf8213a700af558357b58ae913c7e61edcb1d27a280e6ad96`  
		Last Modified: Tue, 02 Jul 2024 04:57:16 GMT  
		Size: 121.8 MB (121787632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08fbb2991af2e722c40559a15cb594a3c45661508bc2b7949ea31be77da61b5`  
		Last Modified: Tue, 02 Jul 2024 04:57:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318e763e20b58a15dcf9b1149f8fd8e451417b06f70ea72ed5efd37d9c81bb5`  
		Last Modified: Tue, 02 Jul 2024 04:57:31 GMT  
		Size: 82.9 MB (82864796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2b526fed218337f0520e3445d0429a8fa8bfe0ac52b6a4b3f33185b01d52a7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 309.1 KB (309054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c90e04e32de4d9cc1872a0e6b6145c9249699644d747bff9a66798f07053ec7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293d50e1335efefa8a6cdb594118dd02584b001e0ce1e50c126cadd5d805544`  
		Last Modified: Tue, 02 Jul 2024 04:57:26 GMT  
		Size: 23.1 MB (23125986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:9d1eaeb3445b6895eca1cf02e122e979a44bb9376f6fae1b7ce9df98a0d9ffb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:4c19d95dac345f57f945cc4322e328f1d0369316e4442c55fbe0b5f1053cee3c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269041898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd874b4161f2dad2ed935ab7d27d7d0849f5330a89b1dc28f99c853fc03d44b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:22:21 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 06:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:23:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:23:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:23:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:24:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6035e0c20aa9a6a0e72cf291215a36408ff518e0b9da966329c30f8c9580a36`  
		Last Modified: Tue, 02 Jul 2024 06:29:47 GMT  
		Size: 124.3 MB (124331033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c982681289ab5fec9bc8ad601404cf9b8cf253486448949dd554ae96b169dc53`  
		Last Modified: Tue, 02 Jul 2024 06:29:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3dd9ed9a2217783c07c06264630b1d38f0f53924faa3d7be94edee1f46a5d2`  
		Last Modified: Tue, 02 Jul 2024 06:30:05 GMT  
		Size: 85.2 MB (85177019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6602c7f18082b5d3dad3c904b267f744d9b5549b8f4d1b0e6a4ef7711953cd`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 309.1 KB (309061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03594b9a6a50634d9d79b7783fc18c923e0da60100953a1d7c9e7b430e7f86f4`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4948e4b0173081d9719e580a03997444c2a559883e955f0fbb92d2d3c5c5f5cc`  
		Last Modified: Tue, 02 Jul 2024 06:29:58 GMT  
		Size: 23.7 MB (23735580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:16d2b3738a331abe3e244afd17bdedc6d56784b15fda5c2c9a2c1f01c2542a3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261510145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6b324397fa8b290c69e2c123d187c85bacf69fb08e232e4d8aa51831882617`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:50:55 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 04:51:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:51:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:51:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:51:42 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:52:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:52:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:52:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:52:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30cdc1a9ff2f9ebf8213a700af558357b58ae913c7e61edcb1d27a280e6ad96`  
		Last Modified: Tue, 02 Jul 2024 04:57:16 GMT  
		Size: 121.8 MB (121787632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08fbb2991af2e722c40559a15cb594a3c45661508bc2b7949ea31be77da61b5`  
		Last Modified: Tue, 02 Jul 2024 04:57:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318e763e20b58a15dcf9b1149f8fd8e451417b06f70ea72ed5efd37d9c81bb5`  
		Last Modified: Tue, 02 Jul 2024 04:57:31 GMT  
		Size: 82.9 MB (82864796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2b526fed218337f0520e3445d0429a8fa8bfe0ac52b6a4b3f33185b01d52a7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 309.1 KB (309054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c90e04e32de4d9cc1872a0e6b6145c9249699644d747bff9a66798f07053ec7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293d50e1335efefa8a6cdb594118dd02584b001e0ce1e50c126cadd5d805544`  
		Last Modified: Tue, 02 Jul 2024 04:57:26 GMT  
		Size: 23.1 MB (23125986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:04d3d2c707d25a6d16ab3ff0a98536c02888c0e2c91c7da6966d912f1dcb1d9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:4e506641bcf906c29ec1346c96052849612619dab8a1a15a19faf1892f2feb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158705142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a288fe803cdfa4235ef8dd8cd2a7c7b9334a027feb1db9881038cec65ff7b77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f7236f93b78a4c5838ad92c9a6bd7e07011f128ca1f1a8c982b8de30a776a`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 1.2 MB (1214729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bebe6781c366f7c1fdc19b776fb1d789e4bcadbc43d40671685831fd3b23bf`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 3.6 MB (3624541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b74d1b6c5ce02dddf579d8b0e5b7af7f7a8e586f96f6e4403ce1b253c4a30`  
		Last Modified: Fri, 05 Jul 2024 19:57:26 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177212e66b063c476b2f24bae2438585fdb791a9d5ca4f4ffb967a56dfcdeef9`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a51e4e3fc35489d611b105db96d3fa487d2174d8d96917d3832b883a1194ab6`  
		Last Modified: Fri, 05 Jul 2024 19:57:29 GMT  
		Size: 124.3 MB (124329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047335e2d0fda3eb0e56df44fb15d63cfbee7c96c69d558d1e0b3c133737df32`  
		Last Modified: Fri, 05 Jul 2024 19:57:28 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f1f00e0d131404a9033643ed2d717dc1f525c9e57fcb672b60392d5a38ac5325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19117202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc93e5bc011dd30ec3b72e9ca33047666b25bd8f417d95c18d37d087b20523`

```dockerfile
```

-	Layers:
	-	`sha256:2a713eae60df8a95226dad4c460e4a4be6ac2b9a61fdedbbc3219515736f6040`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 19.1 MB (19101091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1db33be56a1734802498c927303472a1cabb3ae97dd6a734d566d86d3c03782`  
		Last Modified: Fri, 05 Jul 2024 19:57:26 GMT  
		Size: 16.1 KB (16111 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0aa49e1e3d9a8b41e0ccbd37a2e7b456fdea6fc86b498bbf18a7d914d3e157cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155207877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3ead61c5a6d83b4898b61bcfde734853af26f40352246084e8e861be74cb07`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:50:55 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 04:51:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:51:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:51:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:51:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30cdc1a9ff2f9ebf8213a700af558357b58ae913c7e61edcb1d27a280e6ad96`  
		Last Modified: Tue, 02 Jul 2024 04:57:16 GMT  
		Size: 121.8 MB (121787632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08fbb2991af2e722c40559a15cb594a3c45661508bc2b7949ea31be77da61b5`  
		Last Modified: Tue, 02 Jul 2024 04:57:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:04d3d2c707d25a6d16ab3ff0a98536c02888c0e2c91c7da6966d912f1dcb1d9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:4e506641bcf906c29ec1346c96052849612619dab8a1a15a19faf1892f2feb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158705142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a288fe803cdfa4235ef8dd8cd2a7c7b9334a027feb1db9881038cec65ff7b77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f7236f93b78a4c5838ad92c9a6bd7e07011f128ca1f1a8c982b8de30a776a`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 1.2 MB (1214729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bebe6781c366f7c1fdc19b776fb1d789e4bcadbc43d40671685831fd3b23bf`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 3.6 MB (3624541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b74d1b6c5ce02dddf579d8b0e5b7af7f7a8e586f96f6e4403ce1b253c4a30`  
		Last Modified: Fri, 05 Jul 2024 19:57:26 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177212e66b063c476b2f24bae2438585fdb791a9d5ca4f4ffb967a56dfcdeef9`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a51e4e3fc35489d611b105db96d3fa487d2174d8d96917d3832b883a1194ab6`  
		Last Modified: Fri, 05 Jul 2024 19:57:29 GMT  
		Size: 124.3 MB (124329348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047335e2d0fda3eb0e56df44fb15d63cfbee7c96c69d558d1e0b3c133737df32`  
		Last Modified: Fri, 05 Jul 2024 19:57:28 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:f1f00e0d131404a9033643ed2d717dc1f525c9e57fcb672b60392d5a38ac5325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19117202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cc93e5bc011dd30ec3b72e9ca33047666b25bd8f417d95c18d37d087b20523`

```dockerfile
```

-	Layers:
	-	`sha256:2a713eae60df8a95226dad4c460e4a4be6ac2b9a61fdedbbc3219515736f6040`  
		Last Modified: Fri, 05 Jul 2024 19:57:27 GMT  
		Size: 19.1 MB (19101091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1db33be56a1734802498c927303472a1cabb3ae97dd6a734d566d86d3c03782`  
		Last Modified: Fri, 05 Jul 2024 19:57:26 GMT  
		Size: 16.1 KB (16111 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0aa49e1e3d9a8b41e0ccbd37a2e7b456fdea6fc86b498bbf18a7d914d3e157cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155207877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3ead61c5a6d83b4898b61bcfde734853af26f40352246084e8e861be74cb07`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:50:55 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 04:51:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:51:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:51:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:51:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30cdc1a9ff2f9ebf8213a700af558357b58ae913c7e61edcb1d27a280e6ad96`  
		Last Modified: Tue, 02 Jul 2024 04:57:16 GMT  
		Size: 121.8 MB (121787632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08fbb2991af2e722c40559a15cb594a3c45661508bc2b7949ea31be77da61b5`  
		Last Modified: Tue, 02 Jul 2024 04:57:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy`

```console
$ docker pull ros@sha256:e0f9ca2c294fdc7f90a85b5fabda258814ebb1e30420a90e3831e3f387b32487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:7a86535d35141d9c670e3ac22d61820941f668df69c11e74c43108c8ae4d1b7d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299753250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2978d0177f10c303c210a050f03e7067a92a2ea2c7ec247934be9296398871fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 22:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:53:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:53:04 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 22:53:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 22:53:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 22:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb560ba80e4159bbd7ecd0b2b087742543cda4c6a38d6e11962899cf93f2a99`  
		Last Modified: Mon, 17 Jun 2024 23:03:06 GMT  
		Size: 122.4 MB (122449281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f73baf8579b4bee759b3d8255736d35aaea708c7807937e9fa93672b74912`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fffed5895f069623e78dd312f447401d9427c7955cbf44a7a5d6e9d1f793b`  
		Last Modified: Mon, 17 Jun 2024 23:03:30 GMT  
		Size: 114.3 MB (114314047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff86107534e43b482d4ed6f953a16a76dea0fd2355e45153fc52cd185d78ce7`  
		Last Modified: Mon, 17 Jun 2024 23:03:16 GMT  
		Size: 314.5 KB (314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c28d23077d3ae521447fc0ce44530ee13e13395ef0de730f3ee6263b7df0be`  
		Last Modified: Mon, 17 Jun 2024 23:03:15 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e7b1ff4609540214de8a236a1a608ef17ca2d2913bb57f6ee161c6355f305`  
		Last Modified: Mon, 17 Jun 2024 23:03:20 GMT  
		Size: 27.7 MB (27666753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d6a6cc25a0d45532e0089e43a09d431c24b55fec5e972e475f42daf847779143
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289902927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa85df97749ff635c71460155fa1120b6f37900ebe4039cee1fb4ddde9915a3e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:46:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:46:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:46:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c227546804467a35149673a9940ef7ba3bec2ca50b237ac3a8dbfbe65a346f93`  
		Last Modified: Mon, 17 Jun 2024 23:57:07 GMT  
		Size: 111.2 MB (111158516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a75a7a4fb720def18c709bff7759e8ec90103efc11974be93b35b4d8bb60e09`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 314.5 KB (314458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb39b65c9c71daa91633b54cbad6d09c4e4e2a88323868569c0ccd15ceacc3`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f222721a53e6bd52638b546ab83ac3dfe065f3d27213fa0b81c0dcc98ad81`  
		Last Modified: Mon, 17 Jun 2024 23:56:58 GMT  
		Size: 26.8 MB (26813598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:bd8204a95f1d46b9ee7c78f77ba5d34d6921b50c02bae31f374468d74f097f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:f6721cc9d725c0e77ce6bcbed204c83f50febe75c524a926e83b4582fd6b74b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623670793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522872f7ab271415a58b3cc68eb554b3f58b0a58b619883bf4d5675fe1c6777c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 22:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:53:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:53:04 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 22:53:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 22:53:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 22:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:58:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb560ba80e4159bbd7ecd0b2b087742543cda4c6a38d6e11962899cf93f2a99`  
		Last Modified: Mon, 17 Jun 2024 23:03:06 GMT  
		Size: 122.4 MB (122449281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f73baf8579b4bee759b3d8255736d35aaea708c7807937e9fa93672b74912`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fffed5895f069623e78dd312f447401d9427c7955cbf44a7a5d6e9d1f793b`  
		Last Modified: Mon, 17 Jun 2024 23:03:30 GMT  
		Size: 114.3 MB (114314047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff86107534e43b482d4ed6f953a16a76dea0fd2355e45153fc52cd185d78ce7`  
		Last Modified: Mon, 17 Jun 2024 23:03:16 GMT  
		Size: 314.5 KB (314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c28d23077d3ae521447fc0ce44530ee13e13395ef0de730f3ee6263b7df0be`  
		Last Modified: Mon, 17 Jun 2024 23:03:15 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e7b1ff4609540214de8a236a1a608ef17ca2d2913bb57f6ee161c6355f305`  
		Last Modified: Mon, 17 Jun 2024 23:03:20 GMT  
		Size: 27.7 MB (27666753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf7e67c8b7c76d5cad0865b1d9b6f8c530dbaf74aebba9d2663f114a691c579`  
		Last Modified: Mon, 17 Jun 2024 23:04:26 GMT  
		Size: 323.9 MB (323917543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e8c78bc53cc58bb80ff9524a2c18a1724020b7c63852fa3a916c1630865c3b6a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.0 MB (566971316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf7db3d282f096ee145c24ad99ccc3b4a681782e3b8f94b025abaafabfb3533`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:46:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:46:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:46:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c227546804467a35149673a9940ef7ba3bec2ca50b237ac3a8dbfbe65a346f93`  
		Last Modified: Mon, 17 Jun 2024 23:57:07 GMT  
		Size: 111.2 MB (111158516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a75a7a4fb720def18c709bff7759e8ec90103efc11974be93b35b4d8bb60e09`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 314.5 KB (314458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb39b65c9c71daa91633b54cbad6d09c4e4e2a88323868569c0ccd15ceacc3`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f222721a53e6bd52638b546ab83ac3dfe065f3d27213fa0b81c0dcc98ad81`  
		Last Modified: Mon, 17 Jun 2024 23:56:58 GMT  
		Size: 26.8 MB (26813598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff20b0ef4daf156e82f37126f5a0d485f125ea3d17d4a0201496e97d8132224b`  
		Last Modified: Mon, 17 Jun 2024 23:57:48 GMT  
		Size: 277.1 MB (277068389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:bd8204a95f1d46b9ee7c78f77ba5d34d6921b50c02bae31f374468d74f097f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:f6721cc9d725c0e77ce6bcbed204c83f50febe75c524a926e83b4582fd6b74b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623670793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522872f7ab271415a58b3cc68eb554b3f58b0a58b619883bf4d5675fe1c6777c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 22:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:53:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:53:04 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 22:53:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 22:53:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 22:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:58:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb560ba80e4159bbd7ecd0b2b087742543cda4c6a38d6e11962899cf93f2a99`  
		Last Modified: Mon, 17 Jun 2024 23:03:06 GMT  
		Size: 122.4 MB (122449281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f73baf8579b4bee759b3d8255736d35aaea708c7807937e9fa93672b74912`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fffed5895f069623e78dd312f447401d9427c7955cbf44a7a5d6e9d1f793b`  
		Last Modified: Mon, 17 Jun 2024 23:03:30 GMT  
		Size: 114.3 MB (114314047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff86107534e43b482d4ed6f953a16a76dea0fd2355e45153fc52cd185d78ce7`  
		Last Modified: Mon, 17 Jun 2024 23:03:16 GMT  
		Size: 314.5 KB (314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c28d23077d3ae521447fc0ce44530ee13e13395ef0de730f3ee6263b7df0be`  
		Last Modified: Mon, 17 Jun 2024 23:03:15 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e7b1ff4609540214de8a236a1a608ef17ca2d2913bb57f6ee161c6355f305`  
		Last Modified: Mon, 17 Jun 2024 23:03:20 GMT  
		Size: 27.7 MB (27666753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf7e67c8b7c76d5cad0865b1d9b6f8c530dbaf74aebba9d2663f114a691c579`  
		Last Modified: Mon, 17 Jun 2024 23:04:26 GMT  
		Size: 323.9 MB (323917543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e8c78bc53cc58bb80ff9524a2c18a1724020b7c63852fa3a916c1630865c3b6a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.0 MB (566971316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf7db3d282f096ee145c24ad99ccc3b4a681782e3b8f94b025abaafabfb3533`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:46:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:46:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:46:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c227546804467a35149673a9940ef7ba3bec2ca50b237ac3a8dbfbe65a346f93`  
		Last Modified: Mon, 17 Jun 2024 23:57:07 GMT  
		Size: 111.2 MB (111158516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a75a7a4fb720def18c709bff7759e8ec90103efc11974be93b35b4d8bb60e09`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 314.5 KB (314458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb39b65c9c71daa91633b54cbad6d09c4e4e2a88323868569c0ccd15ceacc3`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f222721a53e6bd52638b546ab83ac3dfe065f3d27213fa0b81c0dcc98ad81`  
		Last Modified: Mon, 17 Jun 2024 23:56:58 GMT  
		Size: 26.8 MB (26813598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff20b0ef4daf156e82f37126f5a0d485f125ea3d17d4a0201496e97d8132224b`  
		Last Modified: Mon, 17 Jun 2024 23:57:48 GMT  
		Size: 277.1 MB (277068389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:e0f9ca2c294fdc7f90a85b5fabda258814ebb1e30420a90e3831e3f387b32487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:7a86535d35141d9c670e3ac22d61820941f668df69c11e74c43108c8ae4d1b7d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299753250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2978d0177f10c303c210a050f03e7067a92a2ea2c7ec247934be9296398871fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 22:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:53:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:53:04 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 22:53:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 22:53:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 22:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb560ba80e4159bbd7ecd0b2b087742543cda4c6a38d6e11962899cf93f2a99`  
		Last Modified: Mon, 17 Jun 2024 23:03:06 GMT  
		Size: 122.4 MB (122449281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f73baf8579b4bee759b3d8255736d35aaea708c7807937e9fa93672b74912`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fffed5895f069623e78dd312f447401d9427c7955cbf44a7a5d6e9d1f793b`  
		Last Modified: Mon, 17 Jun 2024 23:03:30 GMT  
		Size: 114.3 MB (114314047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff86107534e43b482d4ed6f953a16a76dea0fd2355e45153fc52cd185d78ce7`  
		Last Modified: Mon, 17 Jun 2024 23:03:16 GMT  
		Size: 314.5 KB (314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c28d23077d3ae521447fc0ce44530ee13e13395ef0de730f3ee6263b7df0be`  
		Last Modified: Mon, 17 Jun 2024 23:03:15 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e7b1ff4609540214de8a236a1a608ef17ca2d2913bb57f6ee161c6355f305`  
		Last Modified: Mon, 17 Jun 2024 23:03:20 GMT  
		Size: 27.7 MB (27666753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d6a6cc25a0d45532e0089e43a09d431c24b55fec5e972e475f42daf847779143
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289902927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa85df97749ff635c71460155fa1120b6f37900ebe4039cee1fb4ddde9915a3e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:46:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:46:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:46:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c227546804467a35149673a9940ef7ba3bec2ca50b237ac3a8dbfbe65a346f93`  
		Last Modified: Mon, 17 Jun 2024 23:57:07 GMT  
		Size: 111.2 MB (111158516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a75a7a4fb720def18c709bff7759e8ec90103efc11974be93b35b4d8bb60e09`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 314.5 KB (314458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb39b65c9c71daa91633b54cbad6d09c4e4e2a88323868569c0ccd15ceacc3`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f222721a53e6bd52638b546ab83ac3dfe065f3d27213fa0b81c0dcc98ad81`  
		Last Modified: Mon, 17 Jun 2024 23:56:58 GMT  
		Size: 26.8 MB (26813598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:e0f9ca2c294fdc7f90a85b5fabda258814ebb1e30420a90e3831e3f387b32487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:7a86535d35141d9c670e3ac22d61820941f668df69c11e74c43108c8ae4d1b7d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299753250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2978d0177f10c303c210a050f03e7067a92a2ea2c7ec247934be9296398871fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 22:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:53:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:53:04 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 22:53:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 22:53:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 22:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb560ba80e4159bbd7ecd0b2b087742543cda4c6a38d6e11962899cf93f2a99`  
		Last Modified: Mon, 17 Jun 2024 23:03:06 GMT  
		Size: 122.4 MB (122449281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f73baf8579b4bee759b3d8255736d35aaea708c7807937e9fa93672b74912`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fffed5895f069623e78dd312f447401d9427c7955cbf44a7a5d6e9d1f793b`  
		Last Modified: Mon, 17 Jun 2024 23:03:30 GMT  
		Size: 114.3 MB (114314047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff86107534e43b482d4ed6f953a16a76dea0fd2355e45153fc52cd185d78ce7`  
		Last Modified: Mon, 17 Jun 2024 23:03:16 GMT  
		Size: 314.5 KB (314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c28d23077d3ae521447fc0ce44530ee13e13395ef0de730f3ee6263b7df0be`  
		Last Modified: Mon, 17 Jun 2024 23:03:15 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e7b1ff4609540214de8a236a1a608ef17ca2d2913bb57f6ee161c6355f305`  
		Last Modified: Mon, 17 Jun 2024 23:03:20 GMT  
		Size: 27.7 MB (27666753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d6a6cc25a0d45532e0089e43a09d431c24b55fec5e972e475f42daf847779143
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289902927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa85df97749ff635c71460155fa1120b6f37900ebe4039cee1fb4ddde9915a3e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:46:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:46:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:46:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c227546804467a35149673a9940ef7ba3bec2ca50b237ac3a8dbfbe65a346f93`  
		Last Modified: Mon, 17 Jun 2024 23:57:07 GMT  
		Size: 111.2 MB (111158516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a75a7a4fb720def18c709bff7759e8ec90103efc11974be93b35b4d8bb60e09`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 314.5 KB (314458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb39b65c9c71daa91633b54cbad6d09c4e4e2a88323868569c0ccd15ceacc3`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f222721a53e6bd52638b546ab83ac3dfe065f3d27213fa0b81c0dcc98ad81`  
		Last Modified: Mon, 17 Jun 2024 23:56:58 GMT  
		Size: 26.8 MB (26813598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:fb6f39dd0a9dee031e7a41dab6c7e2acc72cce622d1270d931ff772fc9bf8943
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e2210a4a3331cf5ca965ba303ee6013ebd21dffed65d94d3d5850a1c6715ef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156406651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a20bffe6e20a2386465358485d7190ebbe0dd6c2bfd6239182da0249b396f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08803d401c081fc3d12416d99b187a634698db36a10df80f4cef29170ef83e5b`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 681.8 KB (681844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f68a5436d21a97e82cf7e242efe03dde4f5b729ed2dbaf097fa8087d993f1c`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 3.6 MB (3558040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36adc7815cbb0b60279e15f0898d1f5d3880e45c336e2d37b6e55f3c19a7d41`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd0181ad8621c2a9206894fa0ac8823b0e7b0c1e07f8700418d53b93a2fa76`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b76af7af5fdf91bcc77e8167917c7c9febf10158f328daafe713d29813881e`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 122.5 MB (122459142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ae2ca4e9abcb78cdac5210d4cbcc57bb261e4fd8cca1695e8606c8e4193be`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:9c8fd8442f082ce2292b4081373891e19bf177069044539319c52955b8c80b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17709145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478bc18e7fb696948cffd284c5a971c603debc121132e3845f43ac7aaa1ad6fc`

```dockerfile
```

-	Layers:
	-	`sha256:57de735ba8354022e87468ff71de5bed30883a305227c776817e4d0dda0885ac`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 17.7 MB (17693028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5cb0a359f2ece50fa7fca665005192834964183e863a8a9506ffe63fe40e2f`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 16.1 KB (16117 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c3168eacba547192d800351b9edc64604d881376b386bed03d0c134b099379a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345f08d42b19afe6542ccf950058268a4a8e3d1908ff5dd01d0bb2cbb4af86b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:fb6f39dd0a9dee031e7a41dab6c7e2acc72cce622d1270d931ff772fc9bf8943
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:e2210a4a3331cf5ca965ba303ee6013ebd21dffed65d94d3d5850a1c6715ef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156406651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a20bffe6e20a2386465358485d7190ebbe0dd6c2bfd6239182da0249b396f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08803d401c081fc3d12416d99b187a634698db36a10df80f4cef29170ef83e5b`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 681.8 KB (681844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f68a5436d21a97e82cf7e242efe03dde4f5b729ed2dbaf097fa8087d993f1c`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 3.6 MB (3558040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36adc7815cbb0b60279e15f0898d1f5d3880e45c336e2d37b6e55f3c19a7d41`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd0181ad8621c2a9206894fa0ac8823b0e7b0c1e07f8700418d53b93a2fa76`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b76af7af5fdf91bcc77e8167917c7c9febf10158f328daafe713d29813881e`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 122.5 MB (122459142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ae2ca4e9abcb78cdac5210d4cbcc57bb261e4fd8cca1695e8606c8e4193be`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9c8fd8442f082ce2292b4081373891e19bf177069044539319c52955b8c80b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17709145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478bc18e7fb696948cffd284c5a971c603debc121132e3845f43ac7aaa1ad6fc`

```dockerfile
```

-	Layers:
	-	`sha256:57de735ba8354022e87468ff71de5bed30883a305227c776817e4d0dda0885ac`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 17.7 MB (17693028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5cb0a359f2ece50fa7fca665005192834964183e863a8a9506ffe63fe40e2f`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 16.1 KB (16117 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c3168eacba547192d800351b9edc64604d881376b386bed03d0c134b099379a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345f08d42b19afe6542ccf950058268a4a8e3d1908ff5dd01d0bb2cbb4af86b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:e0f9ca2c294fdc7f90a85b5fabda258814ebb1e30420a90e3831e3f387b32487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:7a86535d35141d9c670e3ac22d61820941f668df69c11e74c43108c8ae4d1b7d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299753250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2978d0177f10c303c210a050f03e7067a92a2ea2c7ec247934be9296398871fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 22:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:53:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:53:04 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 22:53:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 22:53:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 22:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb560ba80e4159bbd7ecd0b2b087742543cda4c6a38d6e11962899cf93f2a99`  
		Last Modified: Mon, 17 Jun 2024 23:03:06 GMT  
		Size: 122.4 MB (122449281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f73baf8579b4bee759b3d8255736d35aaea708c7807937e9fa93672b74912`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fffed5895f069623e78dd312f447401d9427c7955cbf44a7a5d6e9d1f793b`  
		Last Modified: Mon, 17 Jun 2024 23:03:30 GMT  
		Size: 114.3 MB (114314047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff86107534e43b482d4ed6f953a16a76dea0fd2355e45153fc52cd185d78ce7`  
		Last Modified: Mon, 17 Jun 2024 23:03:16 GMT  
		Size: 314.5 KB (314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c28d23077d3ae521447fc0ce44530ee13e13395ef0de730f3ee6263b7df0be`  
		Last Modified: Mon, 17 Jun 2024 23:03:15 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e7b1ff4609540214de8a236a1a608ef17ca2d2913bb57f6ee161c6355f305`  
		Last Modified: Mon, 17 Jun 2024 23:03:20 GMT  
		Size: 27.7 MB (27666753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d6a6cc25a0d45532e0089e43a09d431c24b55fec5e972e475f42daf847779143
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289902927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa85df97749ff635c71460155fa1120b6f37900ebe4039cee1fb4ddde9915a3e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:46:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:46:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:46:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c227546804467a35149673a9940ef7ba3bec2ca50b237ac3a8dbfbe65a346f93`  
		Last Modified: Mon, 17 Jun 2024 23:57:07 GMT  
		Size: 111.2 MB (111158516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a75a7a4fb720def18c709bff7759e8ec90103efc11974be93b35b4d8bb60e09`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 314.5 KB (314458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb39b65c9c71daa91633b54cbad6d09c4e4e2a88323868569c0ccd15ceacc3`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f222721a53e6bd52638b546ab83ac3dfe065f3d27213fa0b81c0dcc98ad81`  
		Last Modified: Mon, 17 Jun 2024 23:56:58 GMT  
		Size: 26.8 MB (26813598 bytes)  
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
$ docker pull ros@sha256:156756671f825f68c7936c2241f26278029474ca7989f774decb7cffc4656586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:406f995fef5ec8de51bcf83c34d29b92c15d5a35328b79a6cc72cda2886bc57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211071590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a0d9cd739b1b152a9ecc305fc6a17285a6dacf67686ea1b0bb4a32dd59bdde`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541596f8b358e9f0225f58281f3a5f29192357a2d9eba92a600eb4e7486da20`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 1.2 MB (1198610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904313c44f3c8af3a115d7f73029cf8628f3992e20054ad796c7781e3417adbf`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 5.4 MB (5361726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a0710e8ce116746283a133d532bfc0552b821c541c640314b033605b7efc16`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab8426a021e540c85fbeac7e60cc406e2b6038505811aa7a132de889ee284fb`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb19495c8176c1c1ca74fa7251646aa38ade801d766bc5893d14708c768d452`  
		Last Modified: Fri, 05 Jul 2024 19:58:08 GMT  
		Size: 177.0 MB (176997016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df37cf2580810a1de28e2d3533ee7cee4d9439b281ae37a403f9ed021d1c2c8`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:04a1097c2ea1976b74b26ee1f2bd07b294cf0a04fd7a9bff7e9b9cd7f5318862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26044713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ffe64fc0ed9d0692579308d151cab7195f45ef4f98ac8985104789fce1b2eb`

```dockerfile
```

-	Layers:
	-	`sha256:70cf225b82ce7d40955cdd3a5000a8fb1984f381ed8c610288c77d857d73cd00`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 26.0 MB (26028590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5c21fd839a6e3b6581b8a1a7267ab00554b5bda7f79ec68fd5e20d4217c441`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:7ea2944f49233aa49136153185db5959e6acfd209795adfaf67403b19f479605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186785602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5e76a8a76bd29286c14026097ccc28aa65061dab2502c573a2d21b7410a10f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f30cf37c3fd58825124b0f1bf686ac079d10bcea99ba8b2f6d1b21eacaa54d2`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 1.2 MB (1200145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d046f7fdbe893bfdae348a80dd5560e508012ed4d254d0b451554a52492062`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 4.5 MB (4488723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8c7896dff426ab4df0a37bc9f58570f0376c96a6b25482adba107154dcfca`  
		Last Modified: Fri, 05 Jul 2024 20:02:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68053c27827f8faf9453f43780db0948212bbb2fd5f1cd4bade0f6841a0283c2`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf01d6db61aed61d096a4784518c9f045efa6cc61f20ff23c985ed4b92e77d`  
		Last Modified: Fri, 05 Jul 2024 20:02:18 GMT  
		Size: 157.5 MB (157470886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67194fb46b1c786ab9722506fa148b7c7df2462d50ab143fb103e9e328580345`  
		Last Modified: Fri, 05 Jul 2024 20:02:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:c1132cde1a4e65edac3fbf8d6cbfd9c2814405c2ae229ab62eca34b0dd0843f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25959346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18d0055e1600e729af1ca06899733278fb9363beca4c5ad869d9153fcc8feca`

```dockerfile
```

-	Layers:
	-	`sha256:7a1f5b23e89a758c6f6053ab3bf429e6b1ebf29557a3d68dbff1e98cd8c08f42`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 25.9 MB (25943119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc195ed05ddc13c616d5bafcb17f7a57f8e0fec3fe4a9de875bb559d18f5eb93`  
		Last Modified: Fri, 05 Jul 2024 20:02:13 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull ros@sha256:156756671f825f68c7936c2241f26278029474ca7989f774decb7cffc4656586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:406f995fef5ec8de51bcf83c34d29b92c15d5a35328b79a6cc72cda2886bc57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211071590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a0d9cd739b1b152a9ecc305fc6a17285a6dacf67686ea1b0bb4a32dd59bdde`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541596f8b358e9f0225f58281f3a5f29192357a2d9eba92a600eb4e7486da20`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 1.2 MB (1198610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904313c44f3c8af3a115d7f73029cf8628f3992e20054ad796c7781e3417adbf`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 5.4 MB (5361726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a0710e8ce116746283a133d532bfc0552b821c541c640314b033605b7efc16`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab8426a021e540c85fbeac7e60cc406e2b6038505811aa7a132de889ee284fb`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb19495c8176c1c1ca74fa7251646aa38ade801d766bc5893d14708c768d452`  
		Last Modified: Fri, 05 Jul 2024 19:58:08 GMT  
		Size: 177.0 MB (176997016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df37cf2580810a1de28e2d3533ee7cee4d9439b281ae37a403f9ed021d1c2c8`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:04a1097c2ea1976b74b26ee1f2bd07b294cf0a04fd7a9bff7e9b9cd7f5318862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26044713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ffe64fc0ed9d0692579308d151cab7195f45ef4f98ac8985104789fce1b2eb`

```dockerfile
```

-	Layers:
	-	`sha256:70cf225b82ce7d40955cdd3a5000a8fb1984f381ed8c610288c77d857d73cd00`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 26.0 MB (26028590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5c21fd839a6e3b6581b8a1a7267ab00554b5bda7f79ec68fd5e20d4217c441`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:7ea2944f49233aa49136153185db5959e6acfd209795adfaf67403b19f479605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186785602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5e76a8a76bd29286c14026097ccc28aa65061dab2502c573a2d21b7410a10f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f30cf37c3fd58825124b0f1bf686ac079d10bcea99ba8b2f6d1b21eacaa54d2`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 1.2 MB (1200145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d046f7fdbe893bfdae348a80dd5560e508012ed4d254d0b451554a52492062`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 4.5 MB (4488723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8c7896dff426ab4df0a37bc9f58570f0376c96a6b25482adba107154dcfca`  
		Last Modified: Fri, 05 Jul 2024 20:02:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68053c27827f8faf9453f43780db0948212bbb2fd5f1cd4bade0f6841a0283c2`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf01d6db61aed61d096a4784518c9f045efa6cc61f20ff23c985ed4b92e77d`  
		Last Modified: Fri, 05 Jul 2024 20:02:18 GMT  
		Size: 157.5 MB (157470886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67194fb46b1c786ab9722506fa148b7c7df2462d50ab143fb103e9e328580345`  
		Last Modified: Fri, 05 Jul 2024 20:02:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:c1132cde1a4e65edac3fbf8d6cbfd9c2814405c2ae229ab62eca34b0dd0843f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25959346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18d0055e1600e729af1ca06899733278fb9363beca4c5ad869d9153fcc8feca`

```dockerfile
```

-	Layers:
	-	`sha256:7a1f5b23e89a758c6f6053ab3bf429e6b1ebf29557a3d68dbff1e98cd8c08f42`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 25.9 MB (25943119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc195ed05ddc13c616d5bafcb17f7a57f8e0fec3fe4a9de875bb559d18f5eb93`  
		Last Modified: Fri, 05 Jul 2024 20:02:13 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull ros@sha256:ad848c081f616b70f3916cbe5164bfd2e4e466a4e265ff405a3642ef5b652cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:1569a90380536a8a55416203fc87501a40cc5686123ae1be1c7b9f66791d5983
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299750562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc58e01c5bb3f94e5a3c6565881b0e2f7d83691e89defb0484cfd8afd346a68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:59:04 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 22:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:59:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:59:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:59:49 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:00:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:00:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:00:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:00:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bf4a81719799814110e9f58b3944ea90c1033a2274eab4e6624992c9f09a`  
		Last Modified: Mon, 17 Jun 2024 23:04:52 GMT  
		Size: 122.4 MB (122447596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cc489dc7cb1f7d20b13283e4b7586c6fe6955dcd75de71f41fb9d4e839d2ef`  
		Last Modified: Mon, 17 Jun 2024 23:04:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126a1d525e956c943a665be6a1bdf2bd1c748cb8a6959056e416b5b858b4f2dc`  
		Last Modified: Mon, 17 Jun 2024 23:05:16 GMT  
		Size: 114.3 MB (114314070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dae707d6964653e32e5684b13a14702cfd58eb44815e4409bee401b4e94f77`  
		Last Modified: Mon, 17 Jun 2024 23:05:01 GMT  
		Size: 313.8 KB (313847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b5327b73417c56e1fd5f8a00a275431abffe89465447f184ec4399a924c693`  
		Last Modified: Mon, 17 Jun 2024 23:05:00 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe718ce59110b6c800a1a2ca943b53eaf075e1e58706b121dff1445fd9d00ef`  
		Last Modified: Mon, 17 Jun 2024 23:05:04 GMT  
		Size: 27.7 MB (27666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b7890dc1eb4f340307aad568e0223085ed2369d7b19b345575f24a192105a16c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289899219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e375df26376d28b4c17bc3c2dbcaf0d36a1b3f6b48c8244d0e1f3089c125dff`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:53:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 23:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:54:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:54:06 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:54:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:54:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2283aa8cd9a67e68a92a1c6ef2ba08fa913e8a9ecd115b9624f2c79b2baf8`  
		Last Modified: Mon, 17 Jun 2024 23:58:10 GMT  
		Size: 117.3 MB (117264050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7a3a2659c109b159fdd90652b146d33ec87f5c8499db391ee301917cff9fd`  
		Last Modified: Mon, 17 Jun 2024 23:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522c26a1107802862fb3c5b0c7868208a077488d3d0977dfb803db3d598e1142`  
		Last Modified: Mon, 17 Jun 2024 23:58:29 GMT  
		Size: 111.2 MB (111158453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ab82cfb68dcf0114114543a7659da00feb606f498aae6ce2aad99b2e9a48`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 313.8 KB (313848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a2bbcf1f89f35dd755ead0f7aeaef3785ca51299465a477cb4c35ba2b4e138`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d582da3204ba7dd4dbfd74b023cfe074bf7196ff83bcf9369ff4e29be61a`  
		Last Modified: Mon, 17 Jun 2024 23:58:21 GMT  
		Size: 26.8 MB (26812207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:80792af51a6a8a84f293f6c577f3496e2a16ff35bae7bfbedc8a38cff40e2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:13fed4a74f9796cbcd0b8a110cb5e9cd5cdee601dc799893f26fecaebabfe43a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.8 MB (623800191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f5176119c845ec92b0097c148a6ca132c3aa93e911322d340a0acdc487894b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:59:04 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 22:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:59:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:59:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:59:49 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:00:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:00:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:00:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:00:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:01:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bf4a81719799814110e9f58b3944ea90c1033a2274eab4e6624992c9f09a`  
		Last Modified: Mon, 17 Jun 2024 23:04:52 GMT  
		Size: 122.4 MB (122447596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cc489dc7cb1f7d20b13283e4b7586c6fe6955dcd75de71f41fb9d4e839d2ef`  
		Last Modified: Mon, 17 Jun 2024 23:04:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126a1d525e956c943a665be6a1bdf2bd1c748cb8a6959056e416b5b858b4f2dc`  
		Last Modified: Mon, 17 Jun 2024 23:05:16 GMT  
		Size: 114.3 MB (114314070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dae707d6964653e32e5684b13a14702cfd58eb44815e4409bee401b4e94f77`  
		Last Modified: Mon, 17 Jun 2024 23:05:01 GMT  
		Size: 313.8 KB (313847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b5327b73417c56e1fd5f8a00a275431abffe89465447f184ec4399a924c693`  
		Last Modified: Mon, 17 Jun 2024 23:05:00 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe718ce59110b6c800a1a2ca943b53eaf075e1e58706b121dff1445fd9d00ef`  
		Last Modified: Mon, 17 Jun 2024 23:05:04 GMT  
		Size: 27.7 MB (27666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9471c1116581f96eb086f4b1ed900d890e8c0c9d4d70d307046c88e00e4b52ca`  
		Last Modified: Mon, 17 Jun 2024 23:06:10 GMT  
		Size: 324.0 MB (324049629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89ff7d5cb7337bcced25c7ef0885a392bd762c0c159b58cdf13a96d97fe29e0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.1 MB (567075776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcc2b73c565144e7741190c70c1e97eea7ba74866d7d512562305d431eb72f8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:53:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 23:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:54:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:54:06 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:54:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:54:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:55:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2283aa8cd9a67e68a92a1c6ef2ba08fa913e8a9ecd115b9624f2c79b2baf8`  
		Last Modified: Mon, 17 Jun 2024 23:58:10 GMT  
		Size: 117.3 MB (117264050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7a3a2659c109b159fdd90652b146d33ec87f5c8499db391ee301917cff9fd`  
		Last Modified: Mon, 17 Jun 2024 23:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522c26a1107802862fb3c5b0c7868208a077488d3d0977dfb803db3d598e1142`  
		Last Modified: Mon, 17 Jun 2024 23:58:29 GMT  
		Size: 111.2 MB (111158453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ab82cfb68dcf0114114543a7659da00feb606f498aae6ce2aad99b2e9a48`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 313.8 KB (313848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a2bbcf1f89f35dd755ead0f7aeaef3785ca51299465a477cb4c35ba2b4e138`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d582da3204ba7dd4dbfd74b023cfe074bf7196ff83bcf9369ff4e29be61a`  
		Last Modified: Mon, 17 Jun 2024 23:58:21 GMT  
		Size: 26.8 MB (26812207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10e15a8c12dbe14c888d8ed39d89b2d869bab71c7d6375cb89fd6d9a5cdf3b3`  
		Last Modified: Mon, 17 Jun 2024 23:59:07 GMT  
		Size: 277.2 MB (277176557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:80792af51a6a8a84f293f6c577f3496e2a16ff35bae7bfbedc8a38cff40e2271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:13fed4a74f9796cbcd0b8a110cb5e9cd5cdee601dc799893f26fecaebabfe43a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.8 MB (623800191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f5176119c845ec92b0097c148a6ca132c3aa93e911322d340a0acdc487894b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:59:04 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 22:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:59:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:59:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:59:49 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:00:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:00:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:00:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:00:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:01:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bf4a81719799814110e9f58b3944ea90c1033a2274eab4e6624992c9f09a`  
		Last Modified: Mon, 17 Jun 2024 23:04:52 GMT  
		Size: 122.4 MB (122447596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cc489dc7cb1f7d20b13283e4b7586c6fe6955dcd75de71f41fb9d4e839d2ef`  
		Last Modified: Mon, 17 Jun 2024 23:04:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126a1d525e956c943a665be6a1bdf2bd1c748cb8a6959056e416b5b858b4f2dc`  
		Last Modified: Mon, 17 Jun 2024 23:05:16 GMT  
		Size: 114.3 MB (114314070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dae707d6964653e32e5684b13a14702cfd58eb44815e4409bee401b4e94f77`  
		Last Modified: Mon, 17 Jun 2024 23:05:01 GMT  
		Size: 313.8 KB (313847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b5327b73417c56e1fd5f8a00a275431abffe89465447f184ec4399a924c693`  
		Last Modified: Mon, 17 Jun 2024 23:05:00 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe718ce59110b6c800a1a2ca943b53eaf075e1e58706b121dff1445fd9d00ef`  
		Last Modified: Mon, 17 Jun 2024 23:05:04 GMT  
		Size: 27.7 MB (27666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9471c1116581f96eb086f4b1ed900d890e8c0c9d4d70d307046c88e00e4b52ca`  
		Last Modified: Mon, 17 Jun 2024 23:06:10 GMT  
		Size: 324.0 MB (324049629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89ff7d5cb7337bcced25c7ef0885a392bd762c0c159b58cdf13a96d97fe29e0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.1 MB (567075776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcc2b73c565144e7741190c70c1e97eea7ba74866d7d512562305d431eb72f8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:53:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 23:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:54:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:54:06 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:54:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:54:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:55:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2283aa8cd9a67e68a92a1c6ef2ba08fa913e8a9ecd115b9624f2c79b2baf8`  
		Last Modified: Mon, 17 Jun 2024 23:58:10 GMT  
		Size: 117.3 MB (117264050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7a3a2659c109b159fdd90652b146d33ec87f5c8499db391ee301917cff9fd`  
		Last Modified: Mon, 17 Jun 2024 23:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522c26a1107802862fb3c5b0c7868208a077488d3d0977dfb803db3d598e1142`  
		Last Modified: Mon, 17 Jun 2024 23:58:29 GMT  
		Size: 111.2 MB (111158453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ab82cfb68dcf0114114543a7659da00feb606f498aae6ce2aad99b2e9a48`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 313.8 KB (313848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a2bbcf1f89f35dd755ead0f7aeaef3785ca51299465a477cb4c35ba2b4e138`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d582da3204ba7dd4dbfd74b023cfe074bf7196ff83bcf9369ff4e29be61a`  
		Last Modified: Mon, 17 Jun 2024 23:58:21 GMT  
		Size: 26.8 MB (26812207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10e15a8c12dbe14c888d8ed39d89b2d869bab71c7d6375cb89fd6d9a5cdf3b3`  
		Last Modified: Mon, 17 Jun 2024 23:59:07 GMT  
		Size: 277.2 MB (277176557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:ad848c081f616b70f3916cbe5164bfd2e4e466a4e265ff405a3642ef5b652cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1569a90380536a8a55416203fc87501a40cc5686123ae1be1c7b9f66791d5983
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299750562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc58e01c5bb3f94e5a3c6565881b0e2f7d83691e89defb0484cfd8afd346a68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:59:04 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 22:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:59:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:59:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:59:49 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:00:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:00:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:00:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:00:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bf4a81719799814110e9f58b3944ea90c1033a2274eab4e6624992c9f09a`  
		Last Modified: Mon, 17 Jun 2024 23:04:52 GMT  
		Size: 122.4 MB (122447596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cc489dc7cb1f7d20b13283e4b7586c6fe6955dcd75de71f41fb9d4e839d2ef`  
		Last Modified: Mon, 17 Jun 2024 23:04:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126a1d525e956c943a665be6a1bdf2bd1c748cb8a6959056e416b5b858b4f2dc`  
		Last Modified: Mon, 17 Jun 2024 23:05:16 GMT  
		Size: 114.3 MB (114314070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dae707d6964653e32e5684b13a14702cfd58eb44815e4409bee401b4e94f77`  
		Last Modified: Mon, 17 Jun 2024 23:05:01 GMT  
		Size: 313.8 KB (313847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b5327b73417c56e1fd5f8a00a275431abffe89465447f184ec4399a924c693`  
		Last Modified: Mon, 17 Jun 2024 23:05:00 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe718ce59110b6c800a1a2ca943b53eaf075e1e58706b121dff1445fd9d00ef`  
		Last Modified: Mon, 17 Jun 2024 23:05:04 GMT  
		Size: 27.7 MB (27666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b7890dc1eb4f340307aad568e0223085ed2369d7b19b345575f24a192105a16c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289899219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e375df26376d28b4c17bc3c2dbcaf0d36a1b3f6b48c8244d0e1f3089c125dff`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:53:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 23:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:54:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:54:06 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:54:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:54:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2283aa8cd9a67e68a92a1c6ef2ba08fa913e8a9ecd115b9624f2c79b2baf8`  
		Last Modified: Mon, 17 Jun 2024 23:58:10 GMT  
		Size: 117.3 MB (117264050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7a3a2659c109b159fdd90652b146d33ec87f5c8499db391ee301917cff9fd`  
		Last Modified: Mon, 17 Jun 2024 23:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522c26a1107802862fb3c5b0c7868208a077488d3d0977dfb803db3d598e1142`  
		Last Modified: Mon, 17 Jun 2024 23:58:29 GMT  
		Size: 111.2 MB (111158453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ab82cfb68dcf0114114543a7659da00feb606f498aae6ce2aad99b2e9a48`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 313.8 KB (313848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a2bbcf1f89f35dd755ead0f7aeaef3785ca51299465a477cb4c35ba2b4e138`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d582da3204ba7dd4dbfd74b023cfe074bf7196ff83bcf9369ff4e29be61a`  
		Last Modified: Mon, 17 Jun 2024 23:58:21 GMT  
		Size: 26.8 MB (26812207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:ad848c081f616b70f3916cbe5164bfd2e4e466a4e265ff405a3642ef5b652cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:1569a90380536a8a55416203fc87501a40cc5686123ae1be1c7b9f66791d5983
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299750562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc58e01c5bb3f94e5a3c6565881b0e2f7d83691e89defb0484cfd8afd346a68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:59:04 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 22:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:59:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:59:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:59:49 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:00:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:00:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:00:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:00:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bf4a81719799814110e9f58b3944ea90c1033a2274eab4e6624992c9f09a`  
		Last Modified: Mon, 17 Jun 2024 23:04:52 GMT  
		Size: 122.4 MB (122447596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cc489dc7cb1f7d20b13283e4b7586c6fe6955dcd75de71f41fb9d4e839d2ef`  
		Last Modified: Mon, 17 Jun 2024 23:04:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126a1d525e956c943a665be6a1bdf2bd1c748cb8a6959056e416b5b858b4f2dc`  
		Last Modified: Mon, 17 Jun 2024 23:05:16 GMT  
		Size: 114.3 MB (114314070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dae707d6964653e32e5684b13a14702cfd58eb44815e4409bee401b4e94f77`  
		Last Modified: Mon, 17 Jun 2024 23:05:01 GMT  
		Size: 313.8 KB (313847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b5327b73417c56e1fd5f8a00a275431abffe89465447f184ec4399a924c693`  
		Last Modified: Mon, 17 Jun 2024 23:05:00 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe718ce59110b6c800a1a2ca943b53eaf075e1e58706b121dff1445fd9d00ef`  
		Last Modified: Mon, 17 Jun 2024 23:05:04 GMT  
		Size: 27.7 MB (27666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b7890dc1eb4f340307aad568e0223085ed2369d7b19b345575f24a192105a16c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289899219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e375df26376d28b4c17bc3c2dbcaf0d36a1b3f6b48c8244d0e1f3089c125dff`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:53:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 23:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:54:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:54:06 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:54:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:54:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2283aa8cd9a67e68a92a1c6ef2ba08fa913e8a9ecd115b9624f2c79b2baf8`  
		Last Modified: Mon, 17 Jun 2024 23:58:10 GMT  
		Size: 117.3 MB (117264050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7a3a2659c109b159fdd90652b146d33ec87f5c8499db391ee301917cff9fd`  
		Last Modified: Mon, 17 Jun 2024 23:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522c26a1107802862fb3c5b0c7868208a077488d3d0977dfb803db3d598e1142`  
		Last Modified: Mon, 17 Jun 2024 23:58:29 GMT  
		Size: 111.2 MB (111158453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ab82cfb68dcf0114114543a7659da00feb606f498aae6ce2aad99b2e9a48`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 313.8 KB (313848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a2bbcf1f89f35dd755ead0f7aeaef3785ca51299465a477cb4c35ba2b4e138`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d582da3204ba7dd4dbfd74b023cfe074bf7196ff83bcf9369ff4e29be61a`  
		Last Modified: Mon, 17 Jun 2024 23:58:21 GMT  
		Size: 26.8 MB (26812207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:abb734d823719f8499f2f0eaad556d821fb20e84908c0eb2dd9bef85586e998d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:379046c5702f3accda804b0d544ef0bb45a0b18f382985103a541cdb3c670010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156388422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38b9805957947f07cbd0fb47f806d2e6679e2a731db31f83d8e391d6f4af597`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f265dd1822d4bbda2f1664e89c70840207a1cb0f581e84bcae46c1c171fcf05f`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 681.8 KB (681846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928cb5f378100586d71a3f255bfe5fa4132b083e7865faab44a222e87b804bdf`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 3.6 MB (3558081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c330d2857efd338c3ffa191ca727dcc48f9935769f3a656679f59aa808305d`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e8991caeb96415de4fc0f3a65a35f66a7ccf9a27ed08f39a93c8037d290f41`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15aa456906e686b25d81fe30c2b8713c36e49eacd1b7b8d9e80feb7f38d6d2cf`  
		Last Modified: Fri, 05 Jul 2024 19:57:34 GMT  
		Size: 122.4 MB (122440869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d92833e9bcf5d58c3df73aed11c11222570327151eb3b8c271b060b0e22f43`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:706fdfb1c550bb51b567fa300d8c916d4e9b3804ec08939ba96a28bcffc25137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2ee02b289d2a74b69a531f25688203570cb7c6da2563478e9434a44f510098`

```dockerfile
```

-	Layers:
	-	`sha256:ba675725fe91db4754caf60665474d8bb72af096b69df72abc3918666d13e348`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 17.7 MB (17718808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec61e55fbebbfe85fb646aa245b2da0c03d3933884abf3ebf7d4760cb3ced422`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f818b7410c6ec21e720286b2e74c52fad5d9d8fc5b43460976c3596f7671a029
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151612280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922a3075647b4183c0d9896800c2e833198af3d98a4f9ce7a071d25834f5ac94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:53:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 23:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:54:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:54:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2283aa8cd9a67e68a92a1c6ef2ba08fa913e8a9ecd115b9624f2c79b2baf8`  
		Last Modified: Mon, 17 Jun 2024 23:58:10 GMT  
		Size: 117.3 MB (117264050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7a3a2659c109b159fdd90652b146d33ec87f5c8499db391ee301917cff9fd`  
		Last Modified: Mon, 17 Jun 2024 23:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:abb734d823719f8499f2f0eaad556d821fb20e84908c0eb2dd9bef85586e998d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:379046c5702f3accda804b0d544ef0bb45a0b18f382985103a541cdb3c670010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156388422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38b9805957947f07cbd0fb47f806d2e6679e2a731db31f83d8e391d6f4af597`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f265dd1822d4bbda2f1664e89c70840207a1cb0f581e84bcae46c1c171fcf05f`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 681.8 KB (681846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928cb5f378100586d71a3f255bfe5fa4132b083e7865faab44a222e87b804bdf`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 3.6 MB (3558081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c330d2857efd338c3ffa191ca727dcc48f9935769f3a656679f59aa808305d`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e8991caeb96415de4fc0f3a65a35f66a7ccf9a27ed08f39a93c8037d290f41`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15aa456906e686b25d81fe30c2b8713c36e49eacd1b7b8d9e80feb7f38d6d2cf`  
		Last Modified: Fri, 05 Jul 2024 19:57:34 GMT  
		Size: 122.4 MB (122440869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d92833e9bcf5d58c3df73aed11c11222570327151eb3b8c271b060b0e22f43`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:706fdfb1c550bb51b567fa300d8c916d4e9b3804ec08939ba96a28bcffc25137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17734948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2ee02b289d2a74b69a531f25688203570cb7c6da2563478e9434a44f510098`

```dockerfile
```

-	Layers:
	-	`sha256:ba675725fe91db4754caf60665474d8bb72af096b69df72abc3918666d13e348`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 17.7 MB (17718808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec61e55fbebbfe85fb646aa245b2da0c03d3933884abf3ebf7d4760cb3ced422`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f818b7410c6ec21e720286b2e74c52fad5d9d8fc5b43460976c3596f7671a029
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151612280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922a3075647b4183c0d9896800c2e833198af3d98a4f9ce7a071d25834f5ac94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:53:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 23:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:54:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:54:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2283aa8cd9a67e68a92a1c6ef2ba08fa913e8a9ecd115b9624f2c79b2baf8`  
		Last Modified: Mon, 17 Jun 2024 23:58:10 GMT  
		Size: 117.3 MB (117264050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7a3a2659c109b159fdd90652b146d33ec87f5c8499db391ee301917cff9fd`  
		Last Modified: Mon, 17 Jun 2024 23:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
