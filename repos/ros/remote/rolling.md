## `ros:rolling`

```console
$ docker pull ros@sha256:0dd9697a07835941b4f6ba401cfa904ab8c4ee487887288ce9a467096301d106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:4f692bd459b8c069c95b1161b70c7012b6bd6d3f03d8da71d8fa0f36731ac630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299699712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4feba4c47c41fdc1d74bf02589c7f5c8ad628bab02a9f507c9047c481a94a1e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Apr 2024 00:02:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:02:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:02:43 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 26 Apr 2024 00:02:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Apr 2024 00:02:44 GMT
ENV ROS_DISTRO=rolling
# Fri, 26 Apr 2024 00:04:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:04:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 26 Apr 2024 00:04:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Apr 2024 00:04:33 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 00:05:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:05:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Apr 2024 00:05:55 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f5159575f7bbbce11277d1532c12d73076587ebb492562917370449a8c5e7fa`  
		Last Modified: Wed, 24 Apr 2024 17:16:59 GMT  
		Size: 29.7 MB (29702068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d685d4b1835697d792719b9d32a49e6f2ff490bf4864a1e921e19bdcf9b574`  
		Last Modified: Fri, 26 Apr 2024 00:16:06 GMT  
		Size: 680.6 KB (680624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4876135551aef0e8eb1671e4e34d581297f7255ba571e4bd11321bc6ebbb4ca0`  
		Last Modified: Fri, 26 Apr 2024 00:16:05 GMT  
		Size: 4.6 MB (4615573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d1f96a582d77e142a9372c219837cfe0f63629329a255baa7d24c420180aa8`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5d59efebd94c99ec9df4d45496b0da2a6cf7b2c0cdf5d25b454fcb2e658edb`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58520ddab8eb418ed7f39a6254a49b4bcfd80de215fa34ce34a9225fda76cfa1`  
		Last Modified: Fri, 26 Apr 2024 00:16:23 GMT  
		Size: 122.4 MB (122419667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d901e24f0b5da18df9a9856ebd15b74d91636de5681425f96f796b0b33eee6fa`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0f6d3a4fe977861e43b66af02f2cb05ddf4dc2f1077710ce94e3e725465777`  
		Last Modified: Fri, 26 Apr 2024 00:16:48 GMT  
		Size: 114.3 MB (114304236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edda434a4d5818268d4c619a9bc04730867294dd2019473d6caddd71e839979`  
		Last Modified: Fri, 26 Apr 2024 00:16:32 GMT  
		Size: 308.4 KB (308383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74118983417a907cbd593804ea5005eac2b24de69f5a15beba9c617db19c4308`  
		Last Modified: Fri, 26 Apr 2024 00:16:32 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a05c6e33bf42de738f5c7251416ca858af547a21401340c42c8b7f81140638e`  
		Last Modified: Fri, 26 Apr 2024 00:16:36 GMT  
		Size: 27.7 MB (27664162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28918bebd9a511129af137e7ff3d6c14c68c720e24289a08789fd1e3a7dc7980
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289846314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05834fd869cba3632b8eb6eb73a152e5c15da85b0993832bb70fc64c443db503`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Thu, 02 May 2024 02:23:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:23:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:23:49 GMT
CMD ["bash"]
# Thu, 02 May 2024 02:24:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:24:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:24:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:24:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9c27e6b07ed6f6642218c3b8a1eeec6661cffc8a02391bed51154498ab163d`  
		Last Modified: Thu, 02 May 2024 02:35:13 GMT  
		Size: 117.2 MB (117225103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6e9fc856033a2d60a00f8b9c0f2d6cf1af09f0eff1aaaf65b33a4e142a52b`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeee49f272384ea98c1409e784ee434d221d14fc91b442c7ce9a63bf9fe09af`  
		Last Modified: Thu, 02 May 2024 02:35:35 GMT  
		Size: 111.2 MB (111162003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae90260d02fe631fea4319a71d06ce90edb8fb039c93bc235b988ecbb4e6ee1`  
		Last Modified: Thu, 02 May 2024 02:35:22 GMT  
		Size: 308.7 KB (308742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884c3f02d72ee39446f6d04fdebc2167c27296b6b140301f990f00d27f22f20b`  
		Last Modified: Thu, 02 May 2024 02:35:21 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b339374ab1ff5470fd91de8a2ca0ea42e7bb7fffea3c5156c63022eebbaad60d`  
		Last Modified: Thu, 02 May 2024 02:35:26 GMT  
		Size: 26.8 MB (26811230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
