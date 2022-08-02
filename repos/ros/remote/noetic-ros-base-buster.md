## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:3079c4ae9bcc96785297b478364d1819f4406ca648f6b2e6e115fd25cf1c38fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:32e776592bc2676b559eca78d2cf447adbcf153aba7909c290e078933a9560f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463388107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6305a3b060b8ef21af857817efc0baa81168a01e75c72530e57380b0f89605e3`
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
# Tue, 02 Aug 2022 13:24:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:24:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:24:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:cf730b591358262d29294f063a2a095bb438b736d09b9867750da9a660388827`  
		Last Modified: Tue, 02 Aug 2022 13:59:22 GMT  
		Size: 86.6 MB (86568972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bafa8402824e8fc2746fac433d95ca63c18c25e7157347c220bb275e701214a`  
		Last Modified: Tue, 02 Aug 2022 13:59:09 GMT  
		Size: 317.8 KB (317845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c53a4a6a59b2d6fb99c5aa1d32fd18b873d7c25500236c513a2330680a399a`  
		Last Modified: Tue, 02 Aug 2022 13:59:20 GMT  
		Size: 76.0 MB (75976721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a38107b726611e43727c1b2e7229b39feaf72241daca46d4a4c47ac8d41f18d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402846650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd65edd326af89df0190f60b846bb6d458749f8e84780a72e3c54c4c832bec8`
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
# Tue, 02 Aug 2022 15:16:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:16:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:39030940ae9a93159cb08570c346fd2752db24ffb712e6f3dadb2e60725810de`  
		Last Modified: Tue, 02 Aug 2022 15:44:53 GMT  
		Size: 84.4 MB (84370573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d057e3372b0e330210969889e51a3c9995917b106b06b89795293f5b414ae645`  
		Last Modified: Tue, 02 Aug 2022 15:44:42 GMT  
		Size: 317.8 KB (317803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffbef9b0e37dd10c397077421ef3b79575b972c2dd339ac10d4d57ac18a7d06`  
		Last Modified: Tue, 02 Aug 2022 15:44:51 GMT  
		Size: 73.9 MB (73865318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
