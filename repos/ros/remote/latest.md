## `ros:latest`

```console
$ docker pull ros@sha256:deb3ff82d3c8e9855c0df03fe6430527fcc535ea1bec6631b22dced979249426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:627e81b2b340d9effe4484166a9d9340b3139042742a756fdb1e7f19044f7197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263474766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d758cf62d560b4e2cf7b7803d4517f405ba7db9140164c9bc6bd0ce6c0493d96`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:47:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:47:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:37:12 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 21 Dec 2023 00:37:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Dec 2023 00:37:13 GMT
ENV LANG=C.UTF-8
# Thu, 21 Dec 2023 00:37:13 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Dec 2023 00:37:13 GMT
ENV ROS_DISTRO=humble
# Thu, 21 Dec 2023 00:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:39:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 21 Dec 2023 00:39:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:39:02 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:40:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:40:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:40:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Dec 2023 00:40:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e86ad086b67313d4c63edb54bf2739950b802e91ebad161233ae79cff83b4`  
		Last Modified: Sat, 16 Dec 2023 10:07:37 GMT  
		Size: 1.2 MB (1213112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f66abb2468094dfcd781577a433d6fc74be14642bfe0f0b63ac67cce0679d29`  
		Last Modified: Sat, 16 Dec 2023 10:07:35 GMT  
		Size: 3.8 MB (3828953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d02bb8b8ddc5230c53d73e08337222de1d40f5195882a3f250964564551b1d`  
		Last Modified: Thu, 21 Dec 2023 00:59:02 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f96db8146a87c98732d0394da04bb95176f8de8164a58333eac32e8be968c45`  
		Last Modified: Thu, 21 Dec 2023 00:59:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743804516e14cda80b2daf5be84511ffb98452a4c40ae22dbb6974fdaada6baa`  
		Last Modified: Thu, 21 Dec 2023 00:59:18 GMT  
		Size: 106.4 MB (106425740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859364f8b3ef4ac27b4ca997c9e1a41e676203d441c00276704527ad70b00f98`  
		Last Modified: Thu, 21 Dec 2023 00:59:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0bf823a95ae40b9fc6db6be680713548e0b4f8d3a35aafc354ff049052d303`  
		Last Modified: Thu, 21 Dec 2023 00:59:40 GMT  
		Size: 98.1 MB (98136723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2d8c09cf0a02e7e2a58f1d1bfc48f59cfad2580d54ce304074fedf2a897ee9`  
		Last Modified: Thu, 21 Dec 2023 00:59:27 GMT  
		Size: 323.7 KB (323662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb613503d0198be9a275178f7cd4727b635ea8cd37864b8dbca92c24897d2bf`  
		Last Modified: Thu, 21 Dec 2023 00:59:27 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d43614a420a9646ae37b5b1308e723ea84ee496c2b01d7f43a75fa89affda4e`  
		Last Modified: Thu, 21 Dec 2023 00:59:31 GMT  
		Size: 23.1 MB (23095040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f022500a0460f49e83d1b5705284052b169e2d3509eaea482ff148bcf4fba3bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256095309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b38887392a6862454bdcbb5e82a9dfd17eadcf0206ccfe3b940287a01de31b0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:17:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 11:17:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:20:19 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 21 Dec 2023 00:20:19 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Dec 2023 00:20:19 GMT
ENV LANG=C.UTF-8
# Thu, 21 Dec 2023 00:20:19 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Dec 2023 00:20:19 GMT
ENV ROS_DISTRO=humble
# Thu, 21 Dec 2023 00:22:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:22:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 21 Dec 2023 00:22:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:22:15 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:23:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:23:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:23:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Dec 2023 00:24:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1815cfe59f92746cc84bad64334c39e6762ccc361025df692b1ab623be95074e`  
		Last Modified: Sat, 16 Dec 2023 11:39:11 GMT  
		Size: 1.2 MB (1214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1a26b06ab0875840a858da280a123c026690c943f5011863a1ea39eb758c8`  
		Last Modified: Sat, 16 Dec 2023 11:39:09 GMT  
		Size: 3.8 MB (3802078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fad1b30929fca9b55dc79172ec41930dce1d48a91d348d4d46bee1e891dcb0`  
		Last Modified: Thu, 21 Dec 2023 00:43:48 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8e0aa06184a18be8a8dd1b017dbe3345c32fe3d131b98bc2f3bf140137509f`  
		Last Modified: Thu, 21 Dec 2023 00:43:48 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d903c08c37d0aab573e64a72288de26636dc02aa6adfe8cf61a61e1011952c39`  
		Last Modified: Thu, 21 Dec 2023 00:44:10 GMT  
		Size: 104.1 MB (104145910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9cc62ca65f9f9560f1762eabff0e8305dfe475e29038da5f7ab0026b47cfc7`  
		Last Modified: Thu, 21 Dec 2023 00:43:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9464706347fc26498ce1deb56a5e8fb1e674099e0b3a85f1851bc28cc7ecc50`  
		Last Modified: Thu, 21 Dec 2023 00:44:30 GMT  
		Size: 95.7 MB (95685455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855ac8371e9aaa956f7f373c0a43b70cd0e64f682eb364810b7dbb59855e4913`  
		Last Modified: Thu, 21 Dec 2023 00:44:18 GMT  
		Size: 323.7 KB (323656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf7173c5db781380d15cda0759ddf73e07783103c00328357715e221b096690`  
		Last Modified: Thu, 21 Dec 2023 00:44:18 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1b102262e97e824a4c7d21c9cad0797f159f1832971f893400d2443fc5ee45`  
		Last Modified: Thu, 21 Dec 2023 00:44:23 GMT  
		Size: 22.5 MB (22518359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
