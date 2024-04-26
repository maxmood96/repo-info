## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:49da26992fa549a1c9c581154076dbd6618c3d5d5475e1a0f6e6841b16a5a08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:8cea41e8048594171cd9ab0cc251c2d833d12657f45a7805740fa040a7d413d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157420423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bb42ad1c8296633e0e30c976eb63cf011f02dee00b78954d7ba47ee6e5c948`
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

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:63f344d05e550961278e70af7c29c97ff452ea87660ed3c4cadb3870d8c3c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151552218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa575920bfdae9831d632e9c4e14a0a459f078417924d08a34395c7f665933e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:43 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:45 GMT
ADD file:61020b87bc980abd05e75207205df7ecca6ea7023b3a5e804aabded0eebbf2e7 in / 
# Tue, 23 Apr 2024 22:03:45 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:40:03 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:40:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:40:24 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:40:24 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV ROS_DISTRO=rolling
# Thu, 25 Apr 2024 23:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:42:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:42:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ec7cb58592b61e9a11cec56cc368247d061905f8eee62423f6dddd42173504b2`  
		Last Modified: Wed, 24 Apr 2024 17:24:38 GMT  
		Size: 29.0 MB (29037830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eeec93563e0c4bee2b919df0e289aa0a06346104ee647ecb90c42f12aea54e`  
		Last Modified: Thu, 25 Apr 2024 23:53:26 GMT  
		Size: 680.9 KB (680947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d8d27f77c20bc7eb1198a0fc5a3a3f5f22edf40094d000e31aaf9d3ca83c88`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 4.6 MB (4609997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67f27bf0eb8d01126489b229cc3de66eaf05114f0e8b097ec3cc1f82c7323d3`  
		Last Modified: Thu, 25 Apr 2024 23:53:23 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96db453f945716348ca0ce9b78ef87efa36506cc0eb304b6a721f8c3f7546e5b`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aaa8c881c7ea864f1ba79d24492f21979b6f4ef00bd8cb560a7c8d1cf24429`  
		Last Modified: Thu, 25 Apr 2024 23:53:47 GMT  
		Size: 117.2 MB (117220954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef1a74238ed8c5ca9164c6237a3de769a1ae331f532e3238a73422d516ed5d0`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
