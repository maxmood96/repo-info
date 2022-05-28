## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:629260c4521b3247df0e7a2289c38ec954f8b40bab68d4ed3b4c627b7f43ea9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:50e58478e847d121a86d4816556a11684ecae176b1a9d03d3f92ad96737f2a78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484808290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936acaef930b0cc0e1f46c0e67a00fd133e4deaf2184fcd0dd9ee0f910e10c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:32 GMT
ADD file:5c5cde050dbdbd5c7c0d9c723f436d37ab4a8b1a498647a719771eccce99d9cb in / 
# Sat, 28 May 2022 01:20:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 15:31:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 15:31:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 May 2022 15:31:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 May 2022 15:31:04 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 15:31:04 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 May 2022 15:31:04 GMT
ENV ROS_DISTRO=noetic
# Sat, 28 May 2022 15:32:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 15:32:08 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 May 2022 15:32:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 May 2022 15:32:08 GMT
CMD ["bash"]
# Sat, 28 May 2022 15:32:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 15:32:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 28 May 2022 15:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 15:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:982cba7e471c6d3ce96014cf58b2e4e115a525e60da2e1e08716818f2c057a6b`  
		Last Modified: Sat, 28 May 2022 01:25:39 GMT  
		Size: 50.4 MB (50440422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5daa03f5fdf981e5e003e8bcdd00a064f8dec5b68d41a8637fa6e6614fb6daa`  
		Last Modified: Sat, 28 May 2022 15:37:19 GMT  
		Size: 10.9 MB (10892084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f843ce8d3b561918a03456323ce94ad1312c2635f4f04d88a0cccf0359be63`  
		Last Modified: Sat, 28 May 2022 15:37:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e16ee1496f8cf91f13a0be11f546bcc8a1019871d1ae4a593080f404b5cecdc`  
		Last Modified: Sat, 28 May 2022 15:37:18 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e5bca9474dcc4d1c2cb55eb48a9d537e3a19b1977360f0103e67ed68327b2e`  
		Last Modified: Sat, 28 May 2022 15:37:51 GMT  
		Size: 239.2 MB (239165226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e7664792e8911a123880c178f4d96e7735082492c404ecedd78d4ebfee2ede`  
		Last Modified: Sat, 28 May 2022 15:37:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f466cb7b956c2d5d24b517e11f67106e99b1aadea96679c2c2aa0f36b5948e`  
		Last Modified: Sat, 28 May 2022 15:38:10 GMT  
		Size: 86.6 MB (86570564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b328f6c28b3c6930c70d90984ccc80767ee81d5d23ba5124e76bd4e8b7b261a3`  
		Last Modified: Sat, 28 May 2022 15:37:58 GMT  
		Size: 312.9 KB (312930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20422cafa91bad3014676282ceb99ebc8b675eda565d3274d05c57ddc9818011`  
		Last Modified: Sat, 28 May 2022 15:38:08 GMT  
		Size: 76.0 MB (75976311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436b651b7982ed73c7a14ccad8204d4be266c53f8caca9a730fdf73481e171c5`  
		Last Modified: Sat, 28 May 2022 15:38:20 GMT  
		Size: 21.4 MB (21448342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4379cffebfd82e9556a65fd6c18e7d3520c3c5da70f942ff407c970d9627e4ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423938507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8239cccc0facfea3f86fa5ae266ff1caa023bc216529a34a3ce81063ebfa0f1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:49 GMT
ADD file:af879be34a7eccc177a3000eb8c45d5207bfbec108caf9be9d11c1a6620c376c in / 
# Sat, 28 May 2022 00:40:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 09:31:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:31:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 May 2022 09:31:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 May 2022 09:31:49 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 09:31:50 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 May 2022 09:31:51 GMT
ENV ROS_DISTRO=noetic
# Sat, 28 May 2022 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:33:11 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 May 2022 09:33:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 May 2022 09:33:14 GMT
CMD ["bash"]
# Sat, 28 May 2022 09:33:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:33:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 28 May 2022 09:34:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:34:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fadbed17b01e84815ca3018d3dc42670c3add65c67e7cc74d6bc477ae8425934`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 49.2 MB (49229054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3038e2c6f4de92209486b85dbcdfb0c3794568ec22f4fd2438f984045c9ab600`  
		Last Modified: Sat, 28 May 2022 09:40:41 GMT  
		Size: 10.7 MB (10688315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3e60f35c740bab355e4948391f92c4a13422a4e4c8b87db723eadc9c13293d`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986db8ad07690449985043b0f62b086ffb7575f69651d238a6c7914d8964a16a`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5687faf58ed162f39e6695b07560ab17b035ad665611906636878c34709ce634`  
		Last Modified: Sat, 28 May 2022 09:41:11 GMT  
		Size: 184.4 MB (184374214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a862c7e717410bf0c285d49d4b7c55f6aa21daeaf531c763e01ba890bd544d`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074ba53d7f27638353dab267e782918a7ed0010556584e804cb93de4701ef79b`  
		Last Modified: Sat, 28 May 2022 09:41:29 GMT  
		Size: 84.4 MB (84359217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94008c1f225dc6382751509d1eeffd4225fb329e811d11ff8880fc02717ac95c`  
		Last Modified: Sat, 28 May 2022 09:41:18 GMT  
		Size: 312.9 KB (312868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c12a69a2b5ce14bdc763302315975583e743718ebb8b05509b19227329d001e`  
		Last Modified: Sat, 28 May 2022 09:41:28 GMT  
		Size: 73.9 MB (73865730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec076d605ab54bd35291bb3ee6fea64c2896123a8210550888042fb3e0b81c84`  
		Last Modified: Sat, 28 May 2022 09:41:40 GMT  
		Size: 21.1 MB (21106740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
