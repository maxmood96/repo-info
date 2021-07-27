## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:c2629dc0135caf62e003870fff2727ebaa3dfd5f2ff23189345f0c9dd131111e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:f9ab26ad9caf7c6025ff2669c4a4413746b68ea9ed05b3641829ccb515771e8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437364658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07711f635f57ed1907b716dba3ea6e751395f9e0e6d27350c4bb37860fac936`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:39:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:39:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75838d174816c0a4cd1517ea28102b2d7fdff541aa8d4229b56f30f29817ca86`  
		Last Modified: Tue, 27 Jul 2021 01:12:14 GMT  
		Size: 70.2 MB (70229942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dde022f386e96e5a68cbc925d59be0ae93c493ce8f4915b24e88d8f8300035`  
		Last Modified: Tue, 27 Jul 2021 01:12:03 GMT  
		Size: 270.4 KB (270435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640152ffa6b1628c31822b6fed053f5978e7d41168ccdc646fca24e4869f1870`  
		Last Modified: Tue, 27 Jul 2021 01:12:18 GMT  
		Size: 75.0 MB (74994434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:6339006da8aa9f01c5f140ff102a1281d7211f285c2079dd99bf3f9b115548f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385879574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9813875c3478474e0d8357aaaf54b39d326da4491c5e3329cc4ea7ef5bf40e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:59:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:00:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:01:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4f135bc94ed38c27e20719c75a5e0a7159c305d1169046923b45458d5240`  
		Last Modified: Tue, 27 Jul 2021 02:21:29 GMT  
		Size: 54.7 MB (54695577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0296cffbb764eaba4174d14eb10d04dfaf32b3a2ee78b34e89246accb24e714`  
		Last Modified: Tue, 27 Jul 2021 02:21:00 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4c0cb893c1e65e83d2d1e4b4a23b5987c6936c3effd137151aa55f3bdb5a6`  
		Last Modified: Tue, 27 Jul 2021 02:21:49 GMT  
		Size: 64.7 MB (64745753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:13a0303bb0f2769556ab356ebe7bfe219b853c231dd99630a6683fecf8fa804b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411949654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7c5f138f899b76a5d1a336165a47ed55398b821cbd84a95197f7995603c6e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:58:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:58:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:58:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 26 Jul 2021 22:58:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 26 Jul 2021 22:58:38 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 22:58:38 GMT
ENV LC_ALL=C.UTF-8
# Mon, 26 Jul 2021 22:58:38 GMT
ENV ROS_DISTRO=melodic
# Mon, 26 Jul 2021 22:59:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:59:55 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Mon, 26 Jul 2021 22:59:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 26 Jul 2021 22:59:55 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:00:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:00:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 26 Jul 2021 23:01:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec48fab32c57250a0a316617993b1f19f17f7e3eb1f5b4b632c9e249bb8be37`  
		Last Modified: Mon, 26 Jul 2021 23:17:30 GMT  
		Size: 841.3 KB (841297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda3a4d02e2669921c5de51d652aabfb73f4df2b82620e22cee0613358f560c`  
		Last Modified: Mon, 26 Jul 2021 23:17:28 GMT  
		Size: 4.5 MB (4453714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cc312c19bce6f60c0e01ada675f9b439a2c4e6e65fdc361f6d9dfa88a88968`  
		Last Modified: Mon, 26 Jul 2021 23:17:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f078b2e134b3bbc567abf387a039e07d7e9b62a44937b65e4486b11a93d0fa`  
		Last Modified: Mon, 26 Jul 2021 23:17:27 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bb5e0dcebd403b1631077c2bf6f918a579e8261929dd592e97c3599825d707`  
		Last Modified: Mon, 26 Jul 2021 23:18:13 GMT  
		Size: 252.4 MB (252370080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262db146cf4cceac59a83a88e61705c701c9d85f669bade5fb3551c8f1cee8e3`  
		Last Modified: Mon, 26 Jul 2021 23:17:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab725edf1b9f4a135356a05ee3965e94a8d870362463cfa1fdd8b121ae62082`  
		Last Modified: Mon, 26 Jul 2021 23:18:36 GMT  
		Size: 63.1 MB (63058039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7c0963f89fcec01a24152c167c502a6ea1d71b33c04b6c7446ca5c665813a4`  
		Last Modified: Mon, 26 Jul 2021 23:18:25 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44737e66a0fd9299314b82210b7ef1b09c9ec7087b11e374538c570a10ef4e62`  
		Last Modified: Mon, 26 Jul 2021 23:18:39 GMT  
		Size: 67.2 MB (67222081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
