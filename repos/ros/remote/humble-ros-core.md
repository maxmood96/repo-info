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
