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
	-	`sha256:ab9cfdb297cb2e56f5144d6a03d94e416f7101347779b1dac8d072ddb965d0b5`  
		Last Modified: Sat, 09 Dec 2023 04:49:40 GMT  
		Size: 3.6 KB (3622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ae93d7330b04913f411e004ee6e95c6f115a405deced6159ed0ae4c9987099`  
		Last Modified: Sat, 09 Dec 2023 04:51:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadbc41c419150c402c40f1d1eed2da57691737b48cfabb2a85a677c999bdb79`  
		Last Modified: Sat, 09 Dec 2023 04:51:27 GMT  
		Size: 109.2 MB (109169623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f16c937df28690cec98c60ae445a5ad2e4d5c2868816a30a5d8859297cd824c`  
		Last Modified: Sat, 09 Dec 2023 04:51:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491e9e6abb4a9e20e09b6c4e4a30c80e408608a98793f29587a4d6f27eced1e3`  
		Last Modified: Sat, 09 Dec 2023 04:51:47 GMT  
		Size: 73.5 MB (73462168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b21021fd9b9e6faa1b78a6061fb9d053fe7c15d2241f597844b39fd421ecca`  
		Last Modified: Sat, 09 Dec 2023 04:51:36 GMT  
		Size: 279.0 KB (278988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b4e77c324c9b353c1655c675dc3e15d5690491f12eb6cc3f7983b7541e3ee`  
		Last Modified: Sat, 09 Dec 2023 04:51:35 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8d940467045531264741a07da79cb54953c596a4a949f3a20bb49f0e647f93`  
		Last Modified: Sat, 09 Dec 2023 04:51:40 GMT  
		Size: 22.1 MB (22140300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4ad6250fdd606f65fe888d9aeeae5cb468c07f8b0a609f4bb0f7e3e036953`  
		Last Modified: Sat, 09 Dec 2023 04:51:58 GMT  
		Size: 5.4 KB (5405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa839d68c2779d2c21b487d0e59c1c818f020b889e6019c78caa3626e48458d8`  
		Last Modified: Sat, 09 Dec 2023 04:51:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f7f6251bccfdf666858e6a457027bff3aee9e402b196a7e93519b6a230a7d`  
		Last Modified: Sat, 09 Dec 2023 04:52:17 GMT  
		Size: 78.8 MB (78845967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf377c92f3fc74e02dc633002b07ec3f6b1fbda80d373c592630677be0a45f4`  
		Last Modified: Sat, 09 Dec 2023 04:52:02 GMT  
		Size: 16.5 MB (16493310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff95dbe602ee48c3060f917022573dfd5abc52c081264a6eaa8b7c2904654a0`  
		Last Modified: Sat, 09 Dec 2023 04:51:58 GMT  
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
	-	`sha256:2293949a62535f558d267574d694fe0b0e9498fce13b94a8a2e83b00a4d86669`  
		Last Modified: Sat, 09 Dec 2023 04:05:04 GMT  
		Size: 3.6 KB (3625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e6106ec9b9e87d61a209dae736d5a55521179a1e971b3e19fbf6e6cf862b0`  
		Last Modified: Sat, 09 Dec 2023 04:06:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd4c4d79e02de926140a561865bc9b24c63a07e419305ab0a1deae10efadf8`  
		Last Modified: Sat, 09 Dec 2023 04:06:44 GMT  
		Size: 104.7 MB (104684595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b236153245646eabf2f747172467aceaec88d3f377325803397c5ea67e5fd6e4`  
		Last Modified: Sat, 09 Dec 2023 04:06:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25521cd7c38d4702acc35bf86286dd8ec0b25b29688062df02aa6a6e40b0aeb7`  
		Last Modified: Sat, 09 Dec 2023 04:07:01 GMT  
		Size: 67.8 MB (67820715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd225e47b2314091e4a77693b5adde09531a56c382944dcdf26fca1a9945ea9`  
		Last Modified: Sat, 09 Dec 2023 04:06:53 GMT  
		Size: 279.0 KB (278989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5facdfbd066e270842cecd5e7b2804fff0a51adcc271885cb5b96a58a90a8b2f`  
		Last Modified: Sat, 09 Dec 2023 04:06:53 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9da6baa7ccdaef0b14c4f0599c9e580f7a4e2ec3439bbe0d5f1512901e72e`  
		Last Modified: Sat, 09 Dec 2023 04:06:57 GMT  
		Size: 21.5 MB (21481488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3f2d3f902424fa2e5e82a830345f1bf72ad3c82a63f8ca46697e7edc7db75`  
		Last Modified: Sat, 09 Dec 2023 04:07:12 GMT  
		Size: 5.4 KB (5399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7eccd88a94f9e4bf8fbc013fc95ef5ee569265cfa57eb403d08eee628154e6f`  
		Last Modified: Sat, 09 Dec 2023 04:07:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad198325fabb7033faed92791501d458083ad53178e95679c991883331768c2c`  
		Last Modified: Sat, 09 Dec 2023 04:07:31 GMT  
		Size: 78.7 MB (78745423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bcee0cd0a03a0d245a95f48999570b936cf0370ff10f5f7ccb61adaf15b0b3`  
		Last Modified: Sat, 09 Dec 2023 04:07:16 GMT  
		Size: 16.0 MB (16013019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1020862ac6a704344c0c4453c4b2f2d2afda6aee0b57898df747ddd1e6b43c04`  
		Last Modified: Sat, 09 Dec 2023 04:07:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
