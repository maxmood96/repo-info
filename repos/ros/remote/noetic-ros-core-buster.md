## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:171b71608b58b7b14e3e89d131b3a44bf6db64785b65e7475a211d7a39bbe498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:c2293e8255cb39b9e84464f1758c5edcccfd10a7a81b6721a07919e053b56469
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300388600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8598f2cd238f3788ea1441cfb1618471c50dddd28eff1745497832df35cc82e5`
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

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0684d6a87e895094574883528a51ad31c58a2453bfef73981f32b487db50d859
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244347695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42db978a3ff3a7a18a119b3b59d7ad9a553dd993a7e9d9a36d856549935cc4`
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
