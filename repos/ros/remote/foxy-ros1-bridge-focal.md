## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:ae3a2586113103ab62f457d0b4f2b4fc37690dac72ce5fcbf112b932e14732e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:6a82ef6c322c9dcc744e97cb4d9963082d628b814f2c661b32acbbec17df4513
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346058199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9837fbe5b59081660925be593be0641db31c4d810097d704e6749878165e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:09:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:09:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 23:10:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:10:23 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 23:10:23 GMT
ENV ROS2_DISTRO=foxy
# Thu, 03 Mar 2022 23:10:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:57 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbad41d04cdd4ef0ac30989e309c7b3c6e2195487617f6de0de31531e94f0e0`  
		Last Modified: Thu, 03 Mar 2022 23:26:26 GMT  
		Size: 70.9 MB (70858279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2334a170618fa03d191f1cd8e76fc82332385dc22bf836010ede2a8d3f3a8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 251.4 KB (251411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19351c10f0dc4c8c58bf2b0c669363804f1d9b92749d5edb3877509307285bc8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5cea3cbaf19126de5c75f225a7b897c0dc23588d0f04f627c7f54b8b6ccd16`  
		Last Modified: Thu, 03 Mar 2022 23:26:19 GMT  
		Size: 21.7 MB (21668565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da4735eb0f83b7e7035ec5c2b795a45802eaa037f0396d7ce85bed3d974b46`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eac423a1ad520cfeaee1eb128a6c76cf8c96a5da4e2d639a1dae97441e8e5e4`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b15f5a81eed01b7221df719b0ae09c496f479919878cf653779190b846afce`  
		Last Modified: Thu, 03 Mar 2022 23:27:02 GMT  
		Size: 76.3 MB (76324495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d28e7e3b67e20f4905961c74a0a7bf08e737ccb31981aa0743a0ed3096473bd`  
		Last Modified: Thu, 03 Mar 2022 23:26:48 GMT  
		Size: 21.5 MB (21544127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec25e5b6d44635614eec05ea663ac517157327ef1e48387d7d8a7f67c18fc99b`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a1efd9981157111a468345b39dbdaa22229735fc859c71de45555cf595dfab59
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317366822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfe8df067c0062bb8e8927bc18896ce0afa9e9970f95e9fec3235f97b55d902`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:49:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:50:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:06:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 18 Mar 2022 01:07:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Mar 2022 01:07:22 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 01:07:23 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Mar 2022 01:07:24 GMT
ENV ROS_DISTRO=foxy
# Fri, 18 Mar 2022 01:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:08:14 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 18 Mar 2022 01:08:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Mar 2022 01:08:16 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 01:08:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:08:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Mar 2022 01:08:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 18 Mar 2022 01:09:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:09:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Mar 2022 01:09:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Mar 2022 01:09:27 GMT
ENV ROS1_DISTRO=noetic
# Fri, 18 Mar 2022 01:09:28 GMT
ENV ROS2_DISTRO=foxy
# Fri, 18 Mar 2022 01:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:10:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:10:35 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d953991afcd7221257c049654fd6b9a0badc205ef512295d0a14e5b32d79048a`  
		Last Modified: Fri, 18 Mar 2022 01:21:31 GMT  
		Size: 1.2 MB (1184246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7450625577b445654ef80809da992a35c912b1abbf9bbc4ae7cbdd5b1acba574`  
		Last Modified: Fri, 18 Mar 2022 01:21:29 GMT  
		Size: 5.3 MB (5322403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a226af793efce534c13da03becff4b9ca10c9a78e73068425350180b1f6dd357`  
		Last Modified: Fri, 18 Mar 2022 01:26:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca4830ffd26df3e3e23de6bb26197dded9d88809e2a88b370594102526587bb`  
		Last Modified: Fri, 18 Mar 2022 01:26:49 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a14b2daae663639c39577d0c7d4593bd5574bd84d8cc4eab597182dda98e14`  
		Last Modified: Fri, 18 Mar 2022 01:27:06 GMT  
		Size: 104.3 MB (104279184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dc8ed32f6736949944b94d4d4616553dd4b8a76e9a9660f4521a62ac4284d7`  
		Last Modified: Fri, 18 Mar 2022 01:26:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bb58734c528dbf439eb6fd5f41bad51b1219ef59cbbb4aa9249f1b7ee7b776`  
		Last Modified: Fri, 18 Mar 2022 01:27:30 GMT  
		Size: 68.7 MB (68660506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f928dc74080d0875487138c18b5be16c28fb8eebeaca7cd7ff43e5c053bcf30`  
		Last Modified: Fri, 18 Mar 2022 01:27:18 GMT  
		Size: 251.8 KB (251796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2de71e5cdcb594ee0949c5bd975f379ad91d9be834a96504a4506e12cdc8e6`  
		Last Modified: Fri, 18 Mar 2022 01:27:18 GMT  
		Size: 2.1 KB (2136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0525ce65e691fa28b8277972d7bacd7427660a270de514d249fd213d63d36a`  
		Last Modified: Fri, 18 Mar 2022 01:27:21 GMT  
		Size: 20.4 MB (20373802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad24ecbe9c7efb4897ead8256b5de51aaa70a6975457b5308234934d3eccbe6`  
		Last Modified: Fri, 18 Mar 2022 01:27:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ac548bf3515cbca7c930a68cb952494ac153c33c757588e9870a42bbeb2e03`  
		Last Modified: Fri, 18 Mar 2022 01:28:14 GMT  
		Size: 76.2 MB (76155220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce527927efa348d31fb039bc094edfddc20602790341fc2b0697eba09ce3ea6`  
		Last Modified: Fri, 18 Mar 2022 01:28:01 GMT  
		Size: 14.0 MB (13965074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b59f779d25f18d3f09e480bc05f31d9588066a82bc187dc74545a38266c985d`  
		Last Modified: Fri, 18 Mar 2022 01:27:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
