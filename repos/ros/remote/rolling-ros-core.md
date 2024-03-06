## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:570426983cdb163f2d153a2ef30c1baa3146836d177827d935f76d664d5b2646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c0a01b8e7d9f303a7e8e6117d682da239c06b1fd929417a9eeb7041e8640c66e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159683718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe64f3a27e0086cf28d100c5cdb3a54ffda116c006bf09dd047eb6da0d8d3b1`
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
# Wed, 06 Mar 2024 04:53:52 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:54:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:54:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:54:41 GMT
CMD ["bash"]
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
	-	`sha256:89d93a44684bbcbc78e29bcab36972dab63fec251f48a63ecfb1ae10ba3a9f52`  
		Last Modified: Wed, 06 Mar 2024 05:05:50 GMT  
		Size: 124.2 MB (124186646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c637203e66d84fab8aecbd4017a80ec1df09a80ac25baabf93d3f3efc6e0de`  
		Last Modified: Wed, 06 Mar 2024 05:05:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5d4d17f39682d3bfd32d842801e2909be503388975252d5bb46ef68a3166724a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155043033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea638ed33f92eaf96d9e2509eca402a6fed2eab43244bddac1719f86ba1a51`
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
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
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
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
