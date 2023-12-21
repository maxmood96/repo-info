## `ros:iron`

```console
$ docker pull ros@sha256:dc6ab7d4482386f71c72508cdfa4b12b8f39c07f6289e30c304e40d9a4208105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:03ed47cb2baa96e686a948ed232fda7493b2fedd23e749e3382063c33d70fb3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268916218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a3dc6a1cff914dc74998b050d0625b7960656d2b798bc5f8a54162679081a4`
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
# Thu, 21 Dec 2023 00:48:52 GMT
ENV ROS_DISTRO=iron
# Thu, 21 Dec 2023 00:49:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:49:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 21 Dec 2023 00:49:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:49:41 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:50:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:50:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:50:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Dec 2023 00:50:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:5a8745ea836877ef0a40501d0288afaf8502abdfcce31117769fd61392ac6da0`  
		Last Modified: Thu, 21 Dec 2023 01:01:51 GMT  
		Size: 124.2 MB (124212054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5b41d1cf62b5969275519356e129d0c890ff5582411e46f73a38ea724b730d`  
		Last Modified: Thu, 21 Dec 2023 01:01:31 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d126862873345c66dfbbecaaa9863adcae4a0acfd1ca870d90403a8364d1a6e`  
		Last Modified: Thu, 21 Dec 2023 01:02:11 GMT  
		Size: 85.2 MB (85168662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037929c4c4cf9cddf273225cb5d79a57053c38fcc7675dd3b2957d860a4c579a`  
		Last Modified: Thu, 21 Dec 2023 01:02:01 GMT  
		Size: 309.1 KB (309060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e02561515334e63d40d440deaa2b8d1fcc9896d4fd34e70647523b93d04c27b`  
		Last Modified: Thu, 21 Dec 2023 01:02:01 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5f6c27af14f0d2effb9324014c3c17228bf303553e408da495fcc91806ebe9`  
		Last Modified: Thu, 21 Dec 2023 01:02:05 GMT  
		Size: 23.7 MB (23732847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:04024a247f7eaaf0bcca50a8308a89160e3355ea437f6e9e6d0125cf8eaf5965
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261371417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8470b7a8e4524cb111763ba69d5328984860ec089a07a4ec23f543bdecec5b`
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
# Thu, 21 Dec 2023 00:34:11 GMT
ENV ROS_DISTRO=iron
# Thu, 21 Dec 2023 00:34:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:34:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 21 Dec 2023 00:34:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:34:59 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:35:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:35:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Dec 2023 00:35:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7c5371c2637a1c572a602937b6fd11207c0d71ce7493d75ba1db95381489fda8`  
		Last Modified: Thu, 21 Dec 2023 00:46:44 GMT  
		Size: 121.7 MB (121674168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1520cfe0033f3f60a2bd627934bd9b360b48158af49252dff2f72d3be3315327`  
		Last Modified: Thu, 21 Dec 2023 00:46:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2167a0342ec520aea0ca93579b2dddd5613f88462395d7a692630cb7c463b6`  
		Last Modified: Thu, 21 Dec 2023 00:47:02 GMT  
		Size: 82.8 MB (82845496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf7be70767715a7c5283a6896f7f42cdbaee2a947e429bef3b6461fefecf657`  
		Last Modified: Thu, 21 Dec 2023 00:46:53 GMT  
		Size: 309.1 KB (309054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86021cb404bc74550ce79d7cbe14543d7fbfe61351b22422fbf930c8310edf45`  
		Last Modified: Thu, 21 Dec 2023 00:46:54 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34380bc14289029bd9419c722f3697b2a25757381a5731aed82b9cab5436bd42`  
		Last Modified: Thu, 21 Dec 2023 00:46:57 GMT  
		Size: 23.1 MB (23120744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
