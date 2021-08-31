## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:e3f5b74ecccd504f8d69c9fa31a6fc9c2a8a1cadcb3809d07ff3995b46846e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:343d66d45a2db6917dcf8f2e9e0ecbb0dff0ebe4a10500330d92bd0199c6a8bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232538721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31047f12e16b5886c3a18ae5a9c86ecb487730e1f4d402d208ec8ba461027409`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:07:55 GMT
ENV ROS_DISTRO=rolling
# Tue, 27 Jul 2021 01:08:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:08:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:08:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:08:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:09:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:09:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:09:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:09:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928ebb6fc76f821cd15ef57553baa7177425b57b45dca1dc55d1fa7ac567a99`  
		Last Modified: Tue, 27 Jul 2021 01:20:05 GMT  
		Size: 104.0 MB (104037402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87230aa31aac601bd98ed495d1da57881931ef6ba2fd088208ff7edcc11a6645`  
		Last Modified: Tue, 27 Jul 2021 01:19:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ecfae6e660eea869e3a4f0b50e02e1f4d59061ecd4f0183ae66f147a79b142`  
		Last Modified: Tue, 27 Jul 2021 01:20:31 GMT  
		Size: 70.8 MB (70796958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dc0d5adb890f7b8a3773d5280d5a49fc76acb26a178acc8625286d67ffb48`  
		Last Modified: Tue, 27 Jul 2021 01:20:21 GMT  
		Size: 239.9 KB (239910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72269352c197138327479f8993a3f63c4d1e1f551153f8892c4b0e0655b7cda`  
		Last Modified: Tue, 27 Jul 2021 01:20:20 GMT  
		Size: 2.0 KB (2029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164c9e6f758bbce1c98b1b54d6df1e86f651ececc09089ad70ff299c3251599b`  
		Last Modified: Tue, 27 Jul 2021 01:20:24 GMT  
		Size: 22.2 MB (22162528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:068d654eb81e37f10f8b7d2652a176acb72aa68be74703ba8aafd790601b4af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221316964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02d60688898aa225f7ab6565faaf26af8515852e06e50b584ae6ba7a2a6283c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:45:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 31 Aug 2021 02:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:46:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:46:09 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:46:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5c1e17fbe503ccf8bebc08da06f5478b90f03326ea7cc016d9e73507f10ce`  
		Last Modified: Tue, 31 Aug 2021 02:58:52 GMT  
		Size: 100.5 MB (100535790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45400d8e0bf75fe9e077d037d3f7b0e895432f5540ae74445ce40f4b797111a7`  
		Last Modified: Tue, 31 Aug 2021 02:58:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1497a728946ec991c8b236b4101cde77517a464c2b22ebc0c2853c613f8edc`  
		Last Modified: Tue, 31 Aug 2021 02:59:15 GMT  
		Size: 65.1 MB (65137816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb14f8cc4408bc999a0012920c6670355132f9cd04cfa6f3632da05868c24b`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 243.4 KB (243377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f33083ce43a2fe6e2a6de6c0ef97f01bfded87f9bb0c50615c85cb4e312`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b7dcdd13b2c3e4ae37d2c849c4d4f5288ac23426c57d481e802f7cc6d6d96`  
		Last Modified: Tue, 31 Aug 2021 02:59:07 GMT  
		Size: 21.5 MB (21526088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
