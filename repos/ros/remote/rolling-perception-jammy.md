## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:8ffd2eec34c1595e747f73919b7b2eb4f7c536d383cbbd19ff2cd33672e2e969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:5b6c57eef6e1d7715608064ff21c0dda63c00346cf7aff24cb7d14e7cc1cfa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1088048490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a22bed2655671151456cb87328451adae485aa8e08b1dbf61ce345483c70dce`
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
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:48:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57143ed7f731779085a0e57d22932271e243520fd47318ed7ccf08cd50211152`  
		Last Modified: Tue, 25 Oct 2022 08:07:51 GMT  
		Size: 824.8 MB (824826828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f43bef87315efebf16422ccfebe6b8366a1bf1d431d8789128fc8d289b10ceaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1038301133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2208bc0701c962aa607e1c384fe787bd5ccf177a7dfd210023c80bdfadafab`
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
# Tue, 25 Oct 2022 21:55:07 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 21:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:55:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:55:43 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:56:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:56:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:56:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:56:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:5ed727913da2df4c85f543bb622ca8250788089578111439f22bb714798459b3`  
		Last Modified: Tue, 25 Oct 2022 22:11:22 GMT  
		Size: 104.1 MB (104123415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583f3a54ad44a88d2f8f3cef0123a92cfd2d0812bc3b17ae46dee50616c62cc`  
		Last Modified: Tue, 25 Oct 2022 22:11:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2894b1d29796d37211f1faac9997114b1d9ac24cb16aa7b37a55e7e053dfe5c4`  
		Last Modified: Tue, 25 Oct 2022 22:11:44 GMT  
		Size: 95.5 MB (95469739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb51cac7761444f42be6933140a6f38701364f808935260001a5e6de62b856a`  
		Last Modified: Tue, 25 Oct 2022 22:11:33 GMT  
		Size: 289.2 KB (289217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0a1dcd2273219e84ecf67eca79433d30c31344c46ac2fd9599a574a40114f3`  
		Last Modified: Tue, 25 Oct 2022 22:11:32 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebfdea86c967860b279ac03d6a5c556c40da6dc586face59732850ca052e284`  
		Last Modified: Tue, 25 Oct 2022 22:11:36 GMT  
		Size: 22.6 MB (22649690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ebe977e9b8257a2674fee21fd63af1c08eac5e57e2ada34b1822c9c0cdb80e`  
		Last Modified: Tue, 25 Oct 2022 22:13:20 GMT  
		Size: 782.4 MB (782405367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
