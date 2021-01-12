## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:64d95e1473aeddc53016c96f63a2761adb2830054fe9a9e60cb003e99d783722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:60808a56ee9c96024369a639c990934188e69d37f879f4c06fbd884a7a1f5969
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.8 MB (462815251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb39e55d6f51ea2ed380c5f3840e4ff647d523aa3c56c28d1a75272f75c5d13`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:05 GMT
ADD file:166cd044a29ad501c753917f07d638932f2ce960a8570b12d9155e8c38d1e917 in / 
# Tue, 12 Jan 2021 00:35:06 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:02:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:02:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 12 Jan 2021 01:02:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 12 Jan 2021 01:02:50 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 01:02:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 12 Jan 2021 01:02:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 12 Jan 2021 01:04:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:04:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 12 Jan 2021 01:04:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 12 Jan 2021 01:04:25 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:05:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:05:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 12 Jan 2021 01:05:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:06:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2587235a7635c6991dfee9791c7977ab29694cf73bc64c3c5a79097ca99364d1`  
		Last Modified: Tue, 12 Jan 2021 00:43:05 GMT  
		Size: 45.4 MB (45380014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc107b7888825e0d5853ecf389db5b2515fe6326c73985cf48a2ce01aad26f5`  
		Last Modified: Tue, 12 Jan 2021 01:19:52 GMT  
		Size: 6.9 MB (6867770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf6fe34e55ea6e017ffb666a3989f281d46efd2f8515fcc9731d7c7bc9a5584`  
		Last Modified: Tue, 12 Jan 2021 01:19:52 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2572de55c9fd89fcf7d45082824b8a3847f1b721aa9cf9be7ed74f9dce36c0ff`  
		Last Modified: Tue, 12 Jan 2021 01:19:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75953d4f06b47b6e647839b21436c9ec886e57d4a9c6b2a49ca984ead018cccc`  
		Last Modified: Tue, 12 Jan 2021 01:21:07 GMT  
		Size: 270.0 MB (269996440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534164b2c2d43871e0b1a96ffe3f39b0af254e4d847fb1557cabcca5440b71b5`  
		Last Modified: Tue, 12 Jan 2021 01:19:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf6ad1cd65e8c47f1241487b6bcc2688fa67e744aaf3095c17e742ff36ea462`  
		Last Modified: Tue, 12 Jan 2021 01:21:43 GMT  
		Size: 70.2 MB (70152137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd5acb068dd42d818d372fd435d3f186e11db38dbc8430c80ee177a3bf3e6fc`  
		Last Modified: Tue, 12 Jan 2021 01:21:14 GMT  
		Size: 243.8 KB (243822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6369f3ff951a6a2e89d0fe30f2622871bd14906af898577a8555f3bea22f111a`  
		Last Modified: Tue, 12 Jan 2021 01:21:40 GMT  
		Size: 55.1 MB (55053482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6682bd58f34d51f668b7e726b02ddd33bf91a56b7a4d33a87c9d29c8d19fc5a`  
		Last Modified: Tue, 12 Jan 2021 01:21:56 GMT  
		Size: 15.1 MB (15119768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d9e7242ebafd7757ec25d4e69b253e26318ee3191009da8a681ffb8924cc0aff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407718544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daae786157207966b368bf3936cc1bb29df89cfb39c8f49e4b6207daef0e02c4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:18 GMT
ADD file:bc4af94773a01defa7a79adb22199dde2229843dae224d13d3385c522cb71652 in / 
# Tue, 12 Jan 2021 00:45:22 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 16:52:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 16:52:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 12 Jan 2021 16:52:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 12 Jan 2021 16:52:58 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 16:52:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 12 Jan 2021 16:52:59 GMT
ENV ROS_DISTRO=melodic
# Tue, 12 Jan 2021 16:55:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 16:55:42 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 12 Jan 2021 16:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 12 Jan 2021 16:55:44 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 16:56:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 16:56:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 12 Jan 2021 16:57:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 16:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec4f0a0f30ab1b4fc2e412a926b8608502de98203ca1994c7916de2017136729`  
		Last Modified: Tue, 12 Jan 2021 00:54:45 GMT  
		Size: 43.2 MB (43177964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e8239a7d8ab4bee604fb1cbe80d3b4626bc8acc2aac57b72c796f1df90dcfc`  
		Last Modified: Tue, 12 Jan 2021 17:19:42 GMT  
		Size: 6.4 MB (6442128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba0c86565e756ed3e4b30d4defdb5a05c4fa9003af196a2339f78ee34d7327a`  
		Last Modified: Tue, 12 Jan 2021 17:19:41 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1b375834829a4e5e0a592407ed74f1602a3d9b06b46e344684c89d9cb32f29`  
		Last Modified: Tue, 12 Jan 2021 17:19:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41b4520c9fa74d7df36a1d382749cb9a1cc38894d750c425a64ba26e1ab86f3`  
		Last Modified: Tue, 12 Jan 2021 17:20:40 GMT  
		Size: 225.1 MB (225095855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7f1a09c11b17890907dd9234634ee66ce853062cc262bc85d6fa2eff682c80`  
		Last Modified: Tue, 12 Jan 2021 17:19:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e007e9fd419b94a9e3973bea456a0488bc87d4896cc50f48d151eb90c501db2`  
		Last Modified: Tue, 12 Jan 2021 17:21:10 GMT  
		Size: 64.8 MB (64841363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5996f090d2e43890c4b004ee289bcf1368c596deaeaa867d237956c1fed69943`  
		Last Modified: Tue, 12 Jan 2021 17:20:49 GMT  
		Size: 243.9 KB (243873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebac23cb600e01b4ad85eb361f8a14d22b24401d3db4cb7b416134632a67eafb`  
		Last Modified: Tue, 12 Jan 2021 17:21:03 GMT  
		Size: 53.2 MB (53242822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32ffc9f464b01e8b02e4f1c0975973d4df55fba17633d734231dac06dc85256`  
		Last Modified: Tue, 12 Jan 2021 17:21:27 GMT  
		Size: 14.7 MB (14672721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
