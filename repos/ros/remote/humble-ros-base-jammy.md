## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:50bcdf7a659f810c5a353ed3da0b1ce32b6d9d8f07422de32034518aefea9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
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
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e6d1e6c4518e267f9642f3097c08f57026bb5b23a07518200df6e3aecab64c00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255538972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63521c990d674cda3c67249e6cfdcec14a99b82c74773fb5d1db4f07f726ab5c`
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
# Tue, 25 Oct 2022 21:44:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:44:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:44:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7c3b15e7b12a9239bb2946201d3c6989b08423aa83930600af3b36a69b572e5e`  
		Last Modified: Tue, 25 Oct 2022 22:09:16 GMT  
		Size: 95.5 MB (95469663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b453065d137014d9afd7b61bab790935a460401456f9bdcebf6dd134f5d37fc`  
		Last Modified: Tue, 25 Oct 2022 22:09:05 GMT  
		Size: 295.6 KB (295639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2316db5066b2f905bf3ef20d6f817416f350af05c67a3c8d3273d52234b41e4`  
		Last Modified: Tue, 25 Oct 2022 22:09:04 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c024b89761df7b88cd9ede63829964f10f26f025bc3e49c423b1ab95263630`  
		Last Modified: Tue, 25 Oct 2022 22:09:08 GMT  
		Size: 22.4 MB (22433878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
