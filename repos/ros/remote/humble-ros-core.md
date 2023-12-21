## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:6dfb9be809f27b8c7c5c8704616c0e257f811eb06399dbf66e4aaca4e59eb550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:096ae9de1ab8238cb118dabc1a788e9c5fc4e99bf09fd0e597b389cdcfe9dfae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141916874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856f6ce9227fbfd31905903a9725e553b4af1cc814bd133e913810f63af7ab9e`
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

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6e24415917aca0d17581293cc0004d7ad1a33dac0aeb4931fbab63813f72b199
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137565386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d71f01b27c965c659ce83fd672d83a5b254637448df1e7990201a1c604b0d`
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
