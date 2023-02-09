## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:db4ba7c38174bd6fca9fbd9c4c75b162c6f046e74075700ea72f5845becac57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:e794a5c364e8ce73954ce049a15d29d9d2da9350d19741d82cc343a8c54e08e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.2 MB (951247773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509b105dc2e421a7a83a6adb1b6bbab6bb4bf15bac1d33930d7ad6abc46d7e22`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:33 GMT
ADD file:dc52371b5f4608e5887e8c657ff951d1895e0047960f44b153c4a55ebf1726d5 in / 
# Thu, 09 Feb 2023 03:20:33 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 11:02:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:02:10 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 09 Feb 2023 11:02:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 09 Feb 2023 11:02:12 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 11:02:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 09 Feb 2023 11:02:12 GMT
ENV ROS_DISTRO=noetic
# Thu, 09 Feb 2023 11:03:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:03:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 09 Feb 2023 11:03:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 09 Feb 2023 11:03:36 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 11:04:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:04:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 09 Feb 2023 11:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2404786f3febb4866f85b0c8f52b0b0b94dfdb6543e94cd65f961c68f325ff7`  
		Last Modified: Thu, 09 Feb 2023 03:25:32 GMT  
		Size: 50.4 MB (50449613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb999b8f3a9c7e636ecfd923eab21dab4ad56a6e3e310ae695a43fd62c15d1e6`  
		Last Modified: Thu, 09 Feb 2023 11:09:45 GMT  
		Size: 10.9 MB (10897059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd0c17feddc0d5789db91293690ac182ed96538d0ded0ccd2d0f5f469cdee78`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffc213c160645ebd9d58dae23404a6674a1d8406053e9df8404ea590e0076a1`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c4103f7699bacf08762eca77b1ff9ec4d55eb718fe790240abc06fb3b16474`  
		Last Modified: Thu, 09 Feb 2023 11:10:16 GMT  
		Size: 239.2 MB (239207331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0d003a8d1db0ecd1033580e9d3bbba3e32d9bb734b95c13e106d204b27065d`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe84347070d668c166c22040d1df57e0c8cfe10caaecfa6436190b125f3dc9e`  
		Last Modified: Thu, 09 Feb 2023 11:10:36 GMT  
		Size: 86.6 MB (86620960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba92d1342fa78d83010e7582624db32acb6f9da4d30957b5438ca807c0bea4b3`  
		Last Modified: Thu, 09 Feb 2023 11:10:23 GMT  
		Size: 337.8 KB (337796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e70ef99469b77ef2ddec00093f5a670e81ea03172888773da63fdd67356935e`  
		Last Modified: Thu, 09 Feb 2023 11:10:33 GMT  
		Size: 76.0 MB (75978186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb0aac578297835008a69d3bc9c774e548e19fd737177a2e438f68195ecfffa`  
		Last Modified: Thu, 09 Feb 2023 11:12:03 GMT  
		Size: 487.8 MB (487754412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e895aaa0dd5d02478e2e5138e51367886ed842a855fb9c9d20f4adb961bdc30c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.0 MB (868043903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0460803f6e8c560b457eb4e66354c96a2166f53ac233d176720ae646e602de11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:26:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:26:04 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 04 Feb 2023 17:26:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 04 Feb 2023 17:26:06 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 17:26:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 04 Feb 2023 17:26:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 04 Feb 2023 17:27:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:27:25 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 04 Feb 2023 17:27:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 04 Feb 2023 17:27:26 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:27:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:28:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 04 Feb 2023 17:28:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:32:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b265718197183247c812f6e77250082b3ad9a6563b418ee7eb1d9aa48e81d2`  
		Last Modified: Sat, 04 Feb 2023 17:34:03 GMT  
		Size: 10.9 MB (10902637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c398dcb16c154524c0eb8b27ca3127a7af3ce52892f4f3e1fbb6769b147242`  
		Last Modified: Sat, 04 Feb 2023 17:34:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8806fb750e9db8cf1f79371eb9ad9aba0b0cf3a9efc612c4ca346319d1f847`  
		Last Modified: Sat, 04 Feb 2023 17:34:02 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2435ce7d72ccf71a222c2c1686bf6878a366f1c1a7951b450e40bfb17b285070`  
		Last Modified: Sat, 04 Feb 2023 17:34:26 GMT  
		Size: 184.4 MB (184402890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdbfb1ecc2f66b4bbde1c3d1610bf6704cd849a833fbb4d42f8db9a7705bb3d`  
		Last Modified: Sat, 04 Feb 2023 17:34:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46c4d3e1b6c6355329a5fd3d1b3ec96c3954acd510e496e300865d260b9f4a8`  
		Last Modified: Sat, 04 Feb 2023 17:34:41 GMT  
		Size: 84.4 MB (84397528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f153467df2e0635b70db210221437a533f094f9db97172b46e54f934538001`  
		Last Modified: Sat, 04 Feb 2023 17:34:32 GMT  
		Size: 337.3 KB (337312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d58e2a2f615bb1e77778923fa448498f501ddd1ee468ebe109e1c0f5e3ccd68`  
		Last Modified: Sat, 04 Feb 2023 17:34:40 GMT  
		Size: 74.1 MB (74090596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cc5089db4dce542c495555768ab1611c600026a0e8af92c5f28f4fe4225d6d`  
		Last Modified: Sat, 04 Feb 2023 17:35:48 GMT  
		Size: 464.7 MB (464671152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
