## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:13860edc1a2159de6b0b7e67fec088e7493d7c310826251048d584ee8a5852d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:ef2edf8853df759f9b68b04805e2fe2e619d8d7b9c8f821f03b08438048804f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **968.0 MB (968022934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dbfdedf7f890ba0fb2acbcd595bbae921c7afdbf93518ea5e8cc86f064a4d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:32 GMT
ADD file:948d0998410ef6681d723219eb1dfb4a7d804228e03d84bb296f0d3c8826dd92 in / 
# Fri, 03 Sep 2021 01:21:32 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 13:39:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 13:39:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 03 Sep 2021 13:39:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 03 Sep 2021 13:39:05 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 13:39:05 GMT
ENV LC_ALL=C.UTF-8
# Fri, 03 Sep 2021 13:39:05 GMT
ENV ROS_DISTRO=noetic
# Fri, 03 Sep 2021 13:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 13:40:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 03 Sep 2021 13:40:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 03 Sep 2021 13:40:54 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 13:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 13:41:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 03 Sep 2021 13:42:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 13:45:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f04e8168e3873638397ca4beb7d8484b150eca0d10fe1b033a125202ba57692`  
		Last Modified: Fri, 03 Sep 2021 01:27:52 GMT  
		Size: 50.4 MB (50435893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f8731e6891953c99de9e4d8a8d2160b1ddb1cf38881f80f6dbd850c445add7`  
		Last Modified: Fri, 03 Sep 2021 13:47:30 GMT  
		Size: 10.9 MB (10891857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bc2d7188917ba116440a3ef55113a49a25f13264f1883b7afed97e6d531b0`  
		Last Modified: Fri, 03 Sep 2021 13:47:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a30664a92baf3a743d7e281e54e280ce4d8b292ca00c6bc4de7e8776d11e712`  
		Last Modified: Fri, 03 Sep 2021 13:47:28 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cd5e0f8fdd631f86a464eccfec4a35b566db8010b85e70701448b160b169f7`  
		Last Modified: Fri, 03 Sep 2021 13:48:07 GMT  
		Size: 239.1 MB (239058438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3ba467a0503d72a944ff6201cf973f0b369ee9b9b56cf99006f56c66af2691`  
		Last Modified: Fri, 03 Sep 2021 13:47:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a97b810648c6bfcec77cf569fec556dd7ebe75daa515006e655db8a3d5c4ae`  
		Last Modified: Fri, 03 Sep 2021 13:48:29 GMT  
		Size: 86.6 MB (86566413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1791f17950632ab38ddd9645475ed1f3108478391b699c89313410d4dfa81946`  
		Last Modified: Fri, 03 Sep 2021 13:48:15 GMT  
		Size: 313.3 KB (313346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c042e5859c1cdcb8f90b44f7eb6d48790aedeb75372a48dc65069342c542be`  
		Last Modified: Fri, 03 Sep 2021 13:48:26 GMT  
		Size: 76.0 MB (75975297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e522bf6d94f03bead5b61983dac57623997e5695b39f5f37520b7b25fa351021`  
		Last Modified: Fri, 03 Sep 2021 13:50:29 GMT  
		Size: 504.8 MB (504779278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7ca031717582542aaa39f11604722d89d177f746e48eaaad369a7600361d03e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.8 MB (884800192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd3c1343c557e7442d399fb0380f6b87362fb20379e162f2f24ee5eb737e8c9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:56 GMT
ADD file:51975e5f400da759b2cd8f7eba13ad61dd4edbbee0d0fac09b697bfa039d1515 in / 
# Tue, 28 Sep 2021 01:40:57 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 12:17:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:17:58 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 28 Sep 2021 12:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 28 Sep 2021 12:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 12:18:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 28 Sep 2021 12:18:09 GMT
ENV ROS_DISTRO=noetic
# Tue, 28 Sep 2021 12:19:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:19:16 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 28 Sep 2021 12:19:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 28 Sep 2021 12:19:16 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 12:19:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:20:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 28 Sep 2021 12:20:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70fe10514d0290bd1e8986c0fd63a67204813d37fc5863cf9bf8bf61b2031537`  
		Last Modified: Tue, 28 Sep 2021 01:48:53 GMT  
		Size: 49.2 MB (49222381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b719e84e5c17a05db4cb91b65b25f4cecd9fda5ca86f7c93b9e8918c83ad07`  
		Last Modified: Tue, 28 Sep 2021 12:26:12 GMT  
		Size: 10.9 MB (10883372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b180205050ab5009747a1fa863a1467a5e672c5116542801e3f3890b57cc64`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0309f751216573b01fdef820a8e7c97a9ef1170563c0136c2e3faa29e4e99ed`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290538ca4b138960141fb0cf9d84a1ada042c2286a8714c2afa426ef9ea5baf9`  
		Last Modified: Tue, 28 Sep 2021 12:26:44 GMT  
		Size: 184.2 MB (184242688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8fe4a6c015780d0a432c652d6ac68724f7b7305a66625f3dde29654973d374`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570cd6760219c636efbd15651c975651d6776ef161e5daf5e95ca0d02cf74440`  
		Last Modified: Tue, 28 Sep 2021 12:27:04 GMT  
		Size: 84.4 MB (84358024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225d1354fc88caaadf4d1c8428bc28ea51f87d230c8889449d028a90955656a4`  
		Last Modified: Tue, 28 Sep 2021 12:26:52 GMT  
		Size: 315.2 KB (315237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b400ed504130934571dad558eea43e0360a76dce52a046e08a6ad9ca01b97e`  
		Last Modified: Tue, 28 Sep 2021 12:27:02 GMT  
		Size: 74.1 MB (74088130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab0fcd02a4c23ce4ead674fc0400593f9796826f4accf07f8121249de06589f`  
		Last Modified: Tue, 28 Sep 2021 12:28:37 GMT  
		Size: 481.7 MB (481687945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
