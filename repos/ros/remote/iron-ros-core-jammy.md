## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:e0ee41066afc44253511c135fc3d05ef22680fe9bf9f85327ddad6f516c22bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:18f05ac562c1ebb43ffa4ab507a15e9789fe492b198cd8541a78e01b61602223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159582399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5e6419d00ad0e5309de29c100ca93f7d87acfa6cdb966031b35b86181d721b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:48:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:48:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:48:30 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 04 Jul 2023 19:48:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:48:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:48:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b96b181e03e7c00f9ff313a35cb309648ea7a63a12165e78d4298df8d842ef7`  
		Last Modified: Tue, 04 Jul 2023 20:09:20 GMT  
		Size: 1.2 MB (1213029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981b99f5f99f37d026fe791185912ef266fd67d841915968d7f58e1e21aa67dd`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 3.8 MB (3828864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457911032da59063f35f0ed9962d1f7235ab9b54c6a1b2434538945c43049d6d`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca97964148324558ddeb21e9e1395cff5cbcb0443e2d4b59209fa6930ea226d`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8abb53d261569686b18feafb805eb0d6bc1ef7f3d484bb36b41731c64cd75859
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155028486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce607efc4cbe9f78af921a43648895fda5b6b43eea249692b090a343fc7110b4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:16:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:40 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 16 Aug 2023 15:16:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:16:41 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:16:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb23ce0adf8021e5f112c4ebb6b7985390219367991abf52dc7c9e4a59d4e5`  
		Last Modified: Wed, 16 Aug 2023 15:38:58 GMT  
		Size: 1.2 MB (1214567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9e5d7e79405f9ead5346e83d4f49c73608d784a30ccea5e9f0a1cb44319e56`  
		Last Modified: Wed, 16 Aug 2023 15:38:56 GMT  
		Size: 3.8 MB (3801963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61556f61e2363012e91a6b26a6d4854861844ae4d453b2e94e69a8cedb8bd75c`  
		Last Modified: Wed, 16 Aug 2023 15:38:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341a3b77ddbf45ba0b2711355c528b654f522ef0e6f08211fb17a01e1d8cc114`  
		Last Modified: Wed, 16 Aug 2023 15:38:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
