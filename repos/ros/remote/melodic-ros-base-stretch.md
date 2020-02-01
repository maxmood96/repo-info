## `ros:melodic-ros-base-stretch`

```console
$ docker pull ros@sha256:8371751d7085d88046cd417e7c83362d3ba2ca1f4c618553204e94ed0ca1bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-stretch` - linux; amd64

```console
$ docker pull ros@sha256:9056fca04123ab2ba33a44148b3a2c1270cae88b125e6d49d97d2458572bee3f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.9 MB (499917844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3853c13e59b2e126a99cda5e86d4f120371845e10d68f43eaf1e8f6c5167e858`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:41 GMT
ADD file:8a9218592e5d736a05a1821a6dd38b205cdd8197c26a5aa33f6fc22fbfaa1c4d in / 
# Sat, 01 Feb 2020 17:23:41 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:49:37 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:49:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 01 Feb 2020 18:49:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 01 Feb 2020 18:50:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:50:37 GMT
ENV LANG=C.UTF-8
# Sat, 01 Feb 2020 18:50:38 GMT
ENV LC_ALL=C.UTF-8
# Sat, 01 Feb 2020 18:50:54 GMT
RUN rosdep init     && rosdep update
# Sat, 01 Feb 2020 18:50:55 GMT
ENV ROS_DISTRO=melodic
# Sat, 01 Feb 2020 18:52:48 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:52:50 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 01 Feb 2020 18:52:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 01 Feb 2020 18:52:51 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:53:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3192219afd04f93d90f0af7f89cb527d1af2a16975ea391ea8517c602ad6ddb6`  
		Last Modified: Sat, 01 Feb 2020 17:28:49 GMT  
		Size: 45.4 MB (45380658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a905ca7a93e1f1f1e5a3c9d5dacdf39395a357b216f42962d54cb9f2f2779419`  
		Last Modified: Sat, 01 Feb 2020 18:59:03 GMT  
		Size: 10.5 MB (10476666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39d9067426f73e53072c040a66d4e587fa9badca3da3aed990b6ef8afe8385b`  
		Last Modified: Sat, 01 Feb 2020 18:59:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47253481cad39c6f079e90a602a37b6638204f66869e48320e2d414b8ec82be5`  
		Last Modified: Sat, 01 Feb 2020 18:59:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822fec1fbb983df499d36a4c4325090bc1538e03ea008262104c269ccf6d6dc4`  
		Last Modified: Sat, 01 Feb 2020 18:59:18 GMT  
		Size: 64.8 MB (64771303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa493f6b00dde329976001c9a67f03cb4dcd3052a4d21da4e652a24c37556835`  
		Last Modified: Sat, 01 Feb 2020 18:59:00 GMT  
		Size: 416.2 KB (416167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf08f403c96546a118d22bcb2c270059a7191a4f76e27b5cc75f7698e56c606`  
		Last Modified: Sat, 01 Feb 2020 19:00:04 GMT  
		Size: 270.4 MB (270396217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a46c3d9114d6ebdac21d5007ae9386278d464c9e0047cbb328922103e3d04f`  
		Last Modified: Sat, 01 Feb 2020 18:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b10e6c9cd44f10367aabcd3b0d59f7b642aa09deda5ec6d77d9a7cf0312b6b`  
		Last Modified: Sat, 01 Feb 2020 19:00:40 GMT  
		Size: 108.5 MB (108475015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bda4c8f3ddfb11e74a3e7a6e33f13b388b7b667c4832e20f0e3e0b11f486dbba
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.0 MB (443014746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95461410a52add4d5ba4d8315b9518d7ed40ff65a2044a57092a0b99fcbd92c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:34:23 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:34:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 18:34:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 18:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:35:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 18:35:41 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 18:36:03 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 18:36:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 18:38:50 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:39:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 18:39:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 18:39:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:40:15 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facfbd1fae886a379926b7add3095adbf575d32e87e67282e12488332f12f747`  
		Last Modified: Sat, 28 Dec 2019 18:48:28 GMT  
		Size: 9.8 MB (9774604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a6b709bed6b18e5ba839847d0f3e3a5a4e53a163b69ea7858c561fdc7f1e3a`  
		Last Modified: Sat, 28 Dec 2019 18:48:25 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af9a8179e95515f1f6e62a300ca75906566906d949c7403c9f61b8511afc033`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23b6ea616f3e8e138683f48ca757b84bc23de865b250839eba047a141cc6721`  
		Last Modified: Sat, 28 Dec 2019 18:48:46 GMT  
		Size: 62.1 MB (62085764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101b4656b4d26f6236d97a86a31ae20834b113b525d2830521853323cfb6369`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 451.5 KB (451514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e52b33734a366437f8b9e807980e3273684eeef72d2fd1822dc4ea7ae5638`  
		Last Modified: Sat, 28 Dec 2019 18:49:32 GMT  
		Size: 224.6 MB (224573326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de7b9c0321a0098bd333b1ceb564c2a4389249dc4f9e3f45da7c389198a1ba`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033d8666e6f7cc5f88f89356fb0b79d8bcb42f576c433b924571484da93bdc43`  
		Last Modified: Sat, 28 Dec 2019 18:50:04 GMT  
		Size: 103.0 MB (102961244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
