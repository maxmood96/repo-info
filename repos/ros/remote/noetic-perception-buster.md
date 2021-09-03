## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:4224490e2742c5aec9e525b346e68871124c290a1c1df9a2e6730332de7aa241
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
$ docker pull ros@sha256:b125f0aa8c4f4c983c9a2d4f86fa924bb3213ce72f437e7c9cd51e3ed6231c0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.8 MB (884790908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0df7b3716b359e1fef891e626df838827f22961f2d578af5470027d5395e506`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:44 GMT
ADD file:1d6e5f5349752ab5c5888d38637821d2943472188c06bd14ea2bdf7a676ea19b in / 
# Fri, 03 Sep 2021 00:40:44 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 11:27:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 11:27:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 03 Sep 2021 11:27:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 03 Sep 2021 11:27:50 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 11:27:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 03 Sep 2021 11:27:51 GMT
ENV ROS_DISTRO=noetic
# Fri, 03 Sep 2021 11:28:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 11:28:49 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 03 Sep 2021 11:28:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 03 Sep 2021 11:28:50 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 11:29:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 11:29:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 03 Sep 2021 11:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 11:32:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e3c1991bf0816d8624d8191a43732b869478319ed39c5f218e5878ed1ee05d58`  
		Last Modified: Fri, 03 Sep 2021 00:49:16 GMT  
		Size: 49.2 MB (49222144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1462dbe8ebf1cb3c2f5806cb19d8c66f38c095230d7abce37bddb2ba968ca5bd`  
		Last Modified: Fri, 03 Sep 2021 11:35:40 GMT  
		Size: 10.9 MB (10883319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2664a95765076375c283614578526207643956bf3842410bcc7bf4d68dee1862`  
		Last Modified: Fri, 03 Sep 2021 11:35:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02b32b930665db018324ae169bf319ec4667a22080016cfe417f1c301a301bb`  
		Last Modified: Fri, 03 Sep 2021 11:35:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b848e0f07ce6baab097af02bd4e576eb86c8e1b06351507016049cb42b6631d`  
		Last Modified: Fri, 03 Sep 2021 11:36:12 GMT  
		Size: 184.2 MB (184239824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b0fa9131028a94f4fffe644b96939f628590f4295592695f28746a9e10984b`  
		Last Modified: Fri, 03 Sep 2021 11:35:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b96c7e42a14a58819a5bb3314a6f83b3626344879f544d27813fb33a8ed36e2`  
		Last Modified: Fri, 03 Sep 2021 11:36:33 GMT  
		Size: 84.4 MB (84358204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae83f3620e550f184b0f2548271c264a849e7c8f8925a1ec8d6cf06b06e12f4`  
		Last Modified: Fri, 03 Sep 2021 11:36:21 GMT  
		Size: 313.3 KB (313339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35aad3176387dcdd01db7601abcb3321fc3ba932666dd79a8b225e297b96d426`  
		Last Modified: Fri, 03 Sep 2021 11:36:31 GMT  
		Size: 74.1 MB (74087922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8507d540be8d1bdac423987942a18de5eec31fdd7232e8d79b4c8a30f30480`  
		Last Modified: Fri, 03 Sep 2021 11:38:08 GMT  
		Size: 481.7 MB (481683748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
