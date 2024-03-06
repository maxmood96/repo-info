## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:962fa2ff74ce609a2cd1d9fb866502ab3b4bbe3b81af52194325eb9135b80cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:6dd9fb81134cfe4696e09d9c9541e6d41b7853cda69080633391d763e1fca0b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268925574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22184b5715a73536fbcb27573f171783290bd710be1691a893de06c129898bad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:50:10 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:50:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:50:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:50:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:51:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:51:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:51:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:51:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e3ea014906f3a7c3e83d63e916e71430408df8cc6ca0b1b428cb5a7f7456`  
		Last Modified: Wed, 06 Mar 2024 05:03:20 GMT  
		Size: 124.2 MB (124224432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7cc6de96d628a75624552fc6df79665be5f96ede7dd447f5eecddd16adcf7`  
		Last Modified: Wed, 06 Mar 2024 05:03:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3167aa37ba92964ce15c83d9bb0f226b86fc57041d959a84f2bd786e535449aa`  
		Last Modified: Wed, 06 Mar 2024 05:03:39 GMT  
		Size: 85.2 MB (85170647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdfa9a57e3781d78cdc781adb91610b842cf34ccc7992e17a29fe285e982bda`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 297.8 KB (297817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0094ff430353f6440554ec0e0d7480ebec80674101740bba21cfe36d577343`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d2239bae29d1d76b8e33286d5c267501ed50825666af9b379391a898eec3f`  
		Last Modified: Wed, 06 Mar 2024 05:03:32 GMT  
		Size: 23.7 MB (23733119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8fa53945e1f892ec8132dc28885848ebf49d62de9c209a7a3c698d7d5eb714ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261399957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9511ef962573abab8adb8f5c2535e7c0b6226cd663392be971e30512d9290d0d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:36:56 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:37:43 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:38:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:38:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94163e2e56dff6bcf8394dcf0c51e0c1e05f7d35905bf61f7868375517678a69`  
		Last Modified: Wed, 06 Mar 2024 04:49:30 GMT  
		Size: 121.7 MB (121715975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a09d4269a9877c1e165e1c2c52b60e6d81faf469d4acea17a4e625b2e046b`  
		Last Modified: Wed, 06 Mar 2024 04:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21979e52cf569da9d1ca16c13ba7cadf068e3d0af36e6864cb518352191009e0`  
		Last Modified: Wed, 06 Mar 2024 04:49:48 GMT  
		Size: 82.8 MB (82844860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc557ba7379579a08b2dabcc6bb9a358d34de5a1d4ab4a6dbcd905a4ccf7a93`  
		Last Modified: Wed, 06 Mar 2024 04:49:40 GMT  
		Size: 297.8 KB (297812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167f55e60982941a94e2c52ee255fbcc15677fea931cc30658f05bf3410dbbdb`  
		Last Modified: Wed, 06 Mar 2024 04:49:39 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e377e2a2bd9912a433ca23ee48613e4122b8d7a2035c06f344264f4fb431e`  
		Last Modified: Wed, 06 Mar 2024 04:49:44 GMT  
		Size: 23.1 MB (23120349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
