## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:84693dbdf2847f740b584229ebd3bfbebf411ea7e450a61f5272ca468b260a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:670d0f8f29324f5d15fe53c99f4cb268133580585924b92428ead3dc0dfb429e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300524569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a45164c156c820452f2bc1aa5c01e542e53f15a8349fa258fd4ee1197c5e1b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:22:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:22:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:22:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:22:52 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:23:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:23:57 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:23:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:23:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5785ad494f16fd45414b77fd2e2429ebc6d521448ef6d033e1585a5ed6bcbcd1`  
		Last Modified: Tue, 02 Aug 2022 13:58:24 GMT  
		Size: 10.9 MB (10893408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a04cce4da471da7339c364869465ed016774874978f22acce2cc39bb9ead437`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65bdc45a558ffba287816e17e1126b9285c238098635aa3c00f6579301a3b2`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c550336ebd94e7da67ecab9e9641d1125ae9892a6e53beb15510cdaeb177d7`  
		Last Modified: Tue, 02 Aug 2022 13:59:01 GMT  
		Size: 239.2 MB (239187767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d7f1bdf1bd7fd0f7d737e9250e43650de8b5e815bd77d8403f6834729f133c`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c8162efc3fd26d1b5852c27967ec46955932f12ef40b64f120342a1183162644
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244292956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4dc8001330440dfc00997bb6dad496313c61b61d3c1a7f3f098b5165e8ed28`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:14:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:14:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:14:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:14:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:14:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:14:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:15:34 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:15:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:15:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e88751172e93002d9fab715ef025cd9a58382c4888b4934c054c6173397dad`  
		Last Modified: Tue, 02 Aug 2022 15:44:04 GMT  
		Size: 10.7 MB (10689284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f0efe68ed19a3b673e70c93625803a8fb308bf11f8888841e81b8d0d6a9744`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4855fcd49a7c12011d55ed482968d218c494e066da8b0e9df0a3ead99e7002ce`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfd4e3998e04572199a3d7bb537f309bc7477561fe26c3ddfed63b62abf3e7`  
		Last Modified: Tue, 02 Aug 2022 15:44:33 GMT  
		Size: 184.4 MB (184372250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f36ec89e9e1541930fa7fcaa7a8f92fcb400ee8fb5a4abcade58343bed9c44`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
