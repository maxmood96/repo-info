## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:8266cc5f19c8960f7c8b02a42272cd83034aa351a319051a5435c71b7c86ac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:00c01c2ee59af1b7cd0667332f1cc7c8ba5c9dda46a2812412544d086b51f1e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141820076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf8329c1fd5ff5cd43d44cfaa0fe95aa812fe452d280fdec75b035ffb8c7ba5`
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
# Tue, 04 Jul 2023 19:48:31 GMT
ENV ROS_DISTRO=humble
# Tue, 04 Jul 2023 19:50:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:50:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 19:50:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:50:04 GMT
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
	-	`sha256:fd524cf7754594d911fa06358015cf1327cb43355eb465f630a366e97dedef5b`  
		Last Modified: Tue, 04 Jul 2023 20:09:34 GMT  
		Size: 106.3 MB (106344539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a0ac1a73dab9eca6d1d3cb5656032709291067b9f54a573c4a4730296d262b`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5f6465b6c7ec7432ea043f6810f89f5d09acdc6e6665287f4183e4a12b7b82bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137544930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b415d51f1ac13111c78516191c20ceefc8fa19e287ac46c91af846f482439a6`
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
# Wed, 16 Aug 2023 15:16:41 GMT
ENV ROS_DISTRO=humble
# Wed, 16 Aug 2023 15:18:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:18:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:18:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:18:11 GMT
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
	-	`sha256:6f8d16cf4626b88f51269b779ec210c233b939c6fd312ef437d166e1d21de979`  
		Last Modified: Wed, 16 Aug 2023 15:39:08 GMT  
		Size: 104.1 MB (104134081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10891661248957cb4be16727c1a8f8182ff1cc1b5b3cc48fe93960c67ba2c66a`  
		Last Modified: Wed, 16 Aug 2023 15:38:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
