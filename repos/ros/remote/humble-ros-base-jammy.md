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
