## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:a05313485b1699704638abd3d0b2210d130497564c927c75d8b02f63a8990896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:d5288bf07359d1a92f6ae3333f2fec4eddc429dd253619d5db7394448df1fe42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212169620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08514670a8a0e2d7393eb92d8355d2323bc3aa9a8a38570af6d3fc4ed2e19386`
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
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
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
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:69847763c27a17f9baed0ed3ba6503ff5ef275178ba870d4f4d8ce703b7db288
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187346253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7910025a10d5ed351671eef8398c4a03db22b18de6da5bd55b2b0b4a1b22c306`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:31 GMT
ADD file:984d3d8b31abd025bb9be52f42d60245a76b1ee991f286db819ae204da45390c in / 
# Thu, 03 Mar 2022 21:21:32 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 04:12:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:12:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:12:47 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 04 Mar 2022 04:13:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 04 Mar 2022 04:13:07 GMT
ENV LANG=C.UTF-8
# Fri, 04 Mar 2022 04:13:08 GMT
ENV LC_ALL=C.UTF-8
# Fri, 04 Mar 2022 04:13:08 GMT
ENV ROS_DISTRO=noetic
# Fri, 04 Mar 2022 04:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:15:35 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 04 Mar 2022 04:15:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 04 Mar 2022 04:15:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12a77aaceb8aa1438ebb61cb4904d74fc225cfa20464a060980580674a0a31e9`  
		Last Modified: Thu, 03 Mar 2022 21:25:09 GMT  
		Size: 24.1 MB (24073718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72622fcdf9dbbac555183c0a8524b5edd07dac35372a781fa331a84527019694`  
		Last Modified: Fri, 04 Mar 2022 04:31:50 GMT  
		Size: 1.2 MB (1183587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860aa28c84db54c9fed426839b7f3b84f1213a88c19079c6ee927607f3081038`  
		Last Modified: Fri, 04 Mar 2022 04:31:49 GMT  
		Size: 4.7 MB (4676687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b433cdb5f8666ed847229d536c6d0bf523324e8d6688f0b88e54119c4972e9e4`  
		Last Modified: Fri, 04 Mar 2022 04:31:47 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71446b82e1e8030f55d18180ae6a7c3eba3522690e38a24f07cd56b740f3ddab`  
		Last Modified: Fri, 04 Mar 2022 04:31:47 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a247fdd14cef732cf37eb2920b79152d4cf310e2e392c9d7b4ce744b6e6dacb7`  
		Last Modified: Fri, 04 Mar 2022 04:33:56 GMT  
		Size: 157.4 MB (157409847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf7ed080ab29e67b92dcff3c9aa29669318c436b7a2e75101d2e37255694861`  
		Last Modified: Fri, 04 Mar 2022 04:31:47 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:57e2eb6cb1a93699329efea25f0a8b55981572cc9b85a300248889e76715b509
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204991485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1923e44a0b1aea950d94e881520c3dcb56fd51938170dc107aabc210269f61d5`
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
# Fri, 18 Mar 2022 00:50:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Mar 2022 00:50:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Mar 2022 00:50:44 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 00:50:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Mar 2022 00:50:46 GMT
ENV ROS_DISTRO=noetic
# Fri, 18 Mar 2022 00:54:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:54:10 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Mar 2022 00:54:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Mar 2022 00:54:12 GMT
CMD ["bash"]
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
	-	`sha256:5c5b5aa37b1e8b16ca5b233578bd893ae2b152504bacf5e3b1d6635bcb7c6a9b`  
		Last Modified: Fri, 18 Mar 2022 01:21:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646fde79bbfd73df6e787bcd777ee24ee614779f1f71387d905fdfbfbc57c6fa`  
		Last Modified: Fri, 18 Mar 2022 01:21:28 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7755b1ea906b03f6abea33ec915fc50b397e81d51623b2fb53c5eca32a07f1cc`  
		Last Modified: Fri, 18 Mar 2022 01:21:57 GMT  
		Size: 171.3 MB (171312849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24432d16f00c088adad0694c3e1947c1d04571b5017b0efccf0e474a309a4cc`  
		Last Modified: Fri, 18 Mar 2022 01:21:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
