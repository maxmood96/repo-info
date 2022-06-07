## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:4d776d805039fa1a17b7ad2d3af4860bb4b861ad0f68b0e315267c36a40576f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e0e17b700196408888ab48ab7c914db7819ee82f326f2ba2cb6f8fe6d75f4919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262693307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014f0adf022ed5d398f0b7f1dbd93f0daf5c2c99f625fc0225a710c59afc1ed1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:28:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:28:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:28:35 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 01:28:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:28:36 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 01:28:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 01:28:36 GMT
ENV ROS_DISTRO=humble
# Tue, 07 Jun 2022 01:30:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:30:13 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 01:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 01:30:14 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:31:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:31:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 01:31:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 01:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d1d4bf62a3722d7122bc1b8ee8ad3051fcaf598ca72ad725fea76cb53f6b3c`  
		Last Modified: Tue, 07 Jun 2022 01:52:41 GMT  
		Size: 1.2 MB (1191642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5c906965a7cb2488a6e23da68abe175ee9acffbe27e61b1152cfff4fbf840b`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 3.8 MB (3827182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1af53ce2d5965bf4c8489cf5459894d2e6c3f6b00538c076d38e41668d6cf`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8d3945eb76a1a2076630ee2752a89342d614a9298134e198075975ec08400d`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc5978e994b6f023efb223710613e46034904f6dce39ece5e5b8bf07fe938e1`  
		Last Modified: Tue, 07 Jun 2022 01:52:55 GMT  
		Size: 106.1 MB (106124318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff090f1a8ef849bdfa42139c0684e11771a61f5bb61ffba6a2b7c1d2fda9239`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9c0d1c45afeb74327e597df16894662a900d8c355992eefeeb675d0769066`  
		Last Modified: Tue, 07 Jun 2022 01:53:18 GMT  
		Size: 97.8 MB (97838689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14416f74a08632618c2f5b301b40e1537c737981626b6d5a308c05ac0685cc69`  
		Last Modified: Tue, 07 Jun 2022 01:53:05 GMT  
		Size: 275.5 KB (275465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02f37a74d93c667b726c4a1db0b1e11226232ac78f437a285603c07d13d92ca`  
		Last Modified: Tue, 07 Jun 2022 01:53:05 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53e3e8d33911936f4e2551e3eae9526aa1994e89d0d66c3c0459900bd6d68ba`  
		Last Modified: Tue, 07 Jun 2022 01:53:08 GMT  
		Size: 23.0 MB (23007607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ccc3162be85ff1fa70519bfd257628a728e005b197bf1012a9f11ce2b98cff52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254957822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101c0763c9519ba7c8cae58c6684c706c6ef29b278b56091400ab961143e8f22`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:32 GMT
ADD file:20805b983efd5443e34ebdfb7795010e5684eb1ca1ffea30a3e61e0089c0eee8 in / 
# Tue, 07 Jun 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:04:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:04:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:04:56 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 06:04:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 06:04:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 06:05:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 06:05:01 GMT
ENV ROS_DISTRO=humble
# Tue, 07 Jun 2022 06:05:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:05:48 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 06:05:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 06:05:50 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:06:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:06:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 06:06:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 06:06:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ed02c6ade914c2962413c1ad2ccc86ed8d1512098f2c87fe7bafa8e1b5293185`  
		Last Modified: Thu, 02 Jun 2022 08:38:25 GMT  
		Size: 28.4 MB (28378212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b38f97e6001c6a08e3dc9944afe7213ac786bed47db29ee11755c6040f4eb0`  
		Last Modified: Tue, 07 Jun 2022 06:23:22 GMT  
		Size: 1.2 MB (1193148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e937b319a974108dac2f8e36b8f73cd96710ce7663bdf1f72284fccd43df6abe`  
		Last Modified: Tue, 07 Jun 2022 06:23:20 GMT  
		Size: 3.6 MB (3595011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1effce9a47b0ec30acadccc8c075e64e320b43af40a3600dbac215a9d94b87`  
		Last Modified: Tue, 07 Jun 2022 06:23:19 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3da9dba47edebe9f3610145826c05ead7b35e702981de104853623ccc5208fd`  
		Last Modified: Tue, 07 Jun 2022 06:23:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dfb35f5e4a5b9143c3d9046c7a959e8e235ba7491b4f03bb5647ece48cc7fd`  
		Last Modified: Tue, 07 Jun 2022 06:23:36 GMT  
		Size: 103.9 MB (103862447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b0c005a3d8c72a2326134dfb835545b11c09e1be826cb6796191a3df42673d`  
		Last Modified: Tue, 07 Jun 2022 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f3035c9ae316d5f3965a292003ea9a80fe4752179a91c4017aa9b0d68e07e6`  
		Last Modified: Tue, 07 Jun 2022 06:24:00 GMT  
		Size: 95.2 MB (95223955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e084c9022832d9836eeda7d8e74c887675c25779e5a393fa13d00d7346d01803`  
		Last Modified: Tue, 07 Jun 2022 06:23:46 GMT  
		Size: 275.4 KB (275402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58093b060a5da797812c0b09b2a2da2dbd1417c61297bc1c8d05a88397fb4bf2`  
		Last Modified: Tue, 07 Jun 2022 06:23:46 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1fdae332ebe53c9728d99ef659e2e4b56a11492df80326566359654277d7ff`  
		Last Modified: Tue, 07 Jun 2022 06:23:50 GMT  
		Size: 22.4 MB (22425056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
