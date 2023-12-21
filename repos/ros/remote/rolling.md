## `ros:rolling`

```console
$ docker pull ros@sha256:ef438205e582d19ef4c15166d17bf6287e32d45f54d383ce36966f508f17e2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:e1398dafb9e9c0cd36e8dc14b8d640aac9c5f3898ea9c8f4eeb4c7e40f6e2dc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269013550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e78d0563e6b88bb03e4556dc111bd79832edb3e082ba4382ad615c30ba74a7`
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
# Thu, 21 Dec 2023 00:52:34 GMT
ENV ROS_DISTRO=rolling
# Thu, 21 Dec 2023 00:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:53:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 21 Dec 2023 00:53:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:53:21 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:53:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:53:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:53:55 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Dec 2023 00:54:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:69757fbc65ff3f06a095e723e33230c57901a21bbdb6bc66e3e9410cd62ee84a`  
		Last Modified: Thu, 21 Dec 2023 01:04:20 GMT  
		Size: 124.3 MB (124267838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a76e1df0725d2f151cf684df301335a512b86340f371420d1f3e0d0dc6e56a5`  
		Last Modified: Thu, 21 Dec 2023 01:04:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f9c039cc852f3da90b717b14e8132cb7b1726eac5bcb0f320643415f905b5a`  
		Last Modified: Thu, 21 Dec 2023 01:04:39 GMT  
		Size: 85.2 MB (85171076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f635c6f7747d3bd4fc7aee1d86a26f78f150f2952784028536ea6ce8320c0a`  
		Last Modified: Thu, 21 Dec 2023 01:04:28 GMT  
		Size: 302.5 KB (302492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a1a6d7fac7e62aae48834a06cd9e99f9d32ea7f2825d70229663772894a112`  
		Last Modified: Thu, 21 Dec 2023 01:04:28 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140019aad602b30b5d89661f44e533e3856d90dde96f03424aacc111f518b880`  
		Last Modified: Thu, 21 Dec 2023 01:04:32 GMT  
		Size: 23.8 MB (23778570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:77c998d25342384093d735124331b9911912947466fb7c967e52124d979cbc1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261472272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99038d1dda822f7a84e16b87ea1154ec68080cdae4d9a42b611edce690a9849f`
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
# Thu, 21 Dec 2023 00:37:42 GMT
ENV ROS_DISTRO=rolling
# Thu, 21 Dec 2023 00:38:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:38:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 21 Dec 2023 00:38:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Dec 2023 00:38:27 GMT
CMD ["bash"]
# Thu, 21 Dec 2023 00:38:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Dec 2023 00:38:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Dec 2023 00:38:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Dec 2023 00:39:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c4d0bc030d72ecca85c50c66a53270a58b8a9aa81a5e5867c1fe39c9e013a223`  
		Last Modified: Thu, 21 Dec 2023 00:49:11 GMT  
		Size: 121.7 MB (121734387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33786e0274a16c26905bb42bcc07c27eb4be948a0f8ea6dc19b6fa740fe15165`  
		Last Modified: Thu, 21 Dec 2023 00:48:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e741e338410a9e11ade55d713eb82d61ea6bf9b32dbf4572f1a68ec6216444f`  
		Last Modified: Thu, 21 Dec 2023 00:49:28 GMT  
		Size: 82.8 MB (82848116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806adc1f1aa53812ff5efa08a5586062e39bb167479a3e7a8a6c3f6a942c4292`  
		Last Modified: Thu, 21 Dec 2023 00:49:19 GMT  
		Size: 302.5 KB (302487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58defdb49a6269fa7b9f133a8571b191507dc88c6c53cfbeba13c3b030ca6a63`  
		Last Modified: Thu, 21 Dec 2023 00:49:19 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ebbb5e05c5aece05e7866b9ac129d6fe8246b679145cba723f454c6e3fed3f`  
		Last Modified: Thu, 21 Dec 2023 00:49:24 GMT  
		Size: 23.2 MB (23165340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
