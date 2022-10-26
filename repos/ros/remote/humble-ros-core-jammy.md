## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:a77dcc38d9454e8a3d10971146eeb7a13bc36a0e97e8c97cade9ac090d9959aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:8bacb2ad63d34e815a7983fd8001a3f4183c28384feb5538e6dce2ec715eb7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a32cd2767cb289a14d77fd1f6dd451fa60a7f107555bf2bc9a71dfe8dc5ac8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bd98c1e23890289ecd4c1c3dcabb9871dd202d4e596196345862d17810dea087
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137337380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b6bffeab8857cd2edb8dd6c91809c31e3962be3f8132941040595a48cf1c1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
