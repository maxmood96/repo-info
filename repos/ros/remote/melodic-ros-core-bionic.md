## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:9b03709d6c54ab97d50a1b99d3d00878071189aa2e7bf7faf3daac1c055bedc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:75a3bb07c9b6265827bf559fcc633d660776bb8f408b6dc4c3901f8d48a7fc3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291869847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947363507d39ea6611167fc1c338d12ef5b49ba0a2a5cc6274d9860949f1d3a8`
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

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:bbd128c88179834dd78f67e2f697f122e407e77a4a2f0e86dc2873ff0deca7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266167808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71b21d55415e370ea0f2efce7f099343d10317d448c608d9927230700632df0`
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

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bd615357015446c6a4266c213417b07280476af2f6870933de92121f921a3f37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281399098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8a9970b020adee0ec5936a93a2db6069dc9e5f2db3a889e6ecda9ac45dd189`
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
