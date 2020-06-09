## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:ea01b9c1c4b7108a78b1a6db997caedc31271d79bbda4499830ebf63b528ba24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:3fa039b9d5ea7876c0a7e680c1c9d9ca2d3dbbe0ccc53e62521f97ffb1fe857c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.8 MB (462815498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511434b33513128afeb503acb8ba498d824581c3b79c19031b44518fa7417e48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:39 GMT
ADD file:1ab357efe422cfed5e37af2dc60d07ccfd4bdee4d4a0c00838b5d68f19ff20c7 in / 
# Tue, 09 Jun 2020 01:20:39 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 20:30:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 09 Jun 2020 20:30:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 09 Jun 2020 20:30:32 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 20:30:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 09 Jun 2020 20:30:32 GMT
ENV ROS_DISTRO=noetic
# Tue, 09 Jun 2020 20:31:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 20:31:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 09 Jun 2020 20:31:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 09 Jun 2020 20:31:53 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 20:32:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 20:32:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 09 Jun 2020 20:33:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e9afc4f90ab09248d75c8081b6dfba749a7f7efdac704ced7e0ceb506e02fa4a`  
		Last Modified: Tue, 09 Jun 2020 01:25:37 GMT  
		Size: 50.4 MB (50389504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2bc4e7737d5a2d3f5e9c833d870438ac7e50548abf7def874bc8ea95386dd0`  
		Last Modified: Tue, 09 Jun 2020 20:41:26 GMT  
		Size: 10.9 MB (10889380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4ff2824e647ea24bbff6408793f4f55d062652f3335695a415c55bd25912be`  
		Last Modified: Tue, 09 Jun 2020 20:41:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f982c829c7a71db4d03162f1624b3cbe81db4a2b15a6564fb9ec7c3aee69111`  
		Last Modified: Tue, 09 Jun 2020 20:41:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e21da98db453fa2714971f1395653edd6f2f4444e816ff2e1f1eb64fb8ced0b`  
		Last Modified: Tue, 09 Jun 2020 20:42:25 GMT  
		Size: 238.8 MB (238811177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1492e22c666d6f79fb430015c6a1ecd5cf0e03a036b3a2c1c95f1a66eaf7b80`  
		Last Modified: Tue, 09 Jun 2020 20:41:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910c19ba0ac7edcdff9c367e31c8832fa2773ccb40bab4b4a48e5385fd10def1`  
		Last Modified: Tue, 09 Jun 2020 20:42:52 GMT  
		Size: 86.6 MB (86563054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd25eb6ecc8af9898c262cb6fb7cc612dda5aaad982c5c1a4fdd493be975b75d`  
		Last Modified: Tue, 09 Jun 2020 20:42:29 GMT  
		Size: 194.1 KB (194107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14987723430ac78287b8cfd1e846a06fbe77ce5846b4bb0ae0cacd84fe41ee13`  
		Last Modified: Tue, 09 Jun 2020 20:42:50 GMT  
		Size: 76.0 MB (75966441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:87114ffff6d587b8a22f7f7fda25641fd8ff3f04789c47c8972c3a56dd008601
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402736933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ff08d040c8c468fa786bab45fe64037e5694a296342c070e9ff1fd5189dab6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:51:33 GMT
ADD file:73f1cc6ac15b24788e78ae41cd6c89cb5211d64baf491accbd95b6fe9718f17f in / 
# Tue, 09 Jun 2020 01:51:36 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 13:05:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:05:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 09 Jun 2020 13:05:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 09 Jun 2020 13:05:33 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 13:05:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 09 Jun 2020 13:05:35 GMT
ENV ROS_DISTRO=noetic
# Tue, 09 Jun 2020 13:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:08:05 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 09 Jun 2020 13:08:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 09 Jun 2020 13:08:07 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 13:08:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 13:09:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 09 Jun 2020 13:10:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1db90d3d3b6598d485690f804e96153fb632e7434251d334e9a0c49b773855c9`  
		Last Modified: Tue, 09 Jun 2020 01:57:52 GMT  
		Size: 49.2 MB (49167914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754a42675c9c6fb259aa9d305f565b45c35444de6deaee3143fb56477372bb67`  
		Last Modified: Tue, 09 Jun 2020 13:23:16 GMT  
		Size: 10.9 MB (10881984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24dae9041ffde16867846c8dc990ca42ed1e294c72b3060c495946be316ecf0`  
		Last Modified: Tue, 09 Jun 2020 13:23:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efc0e56bd18d48d8ccc89e984449e10ded921e728cef559dba731616be82bb1`  
		Last Modified: Tue, 09 Jun 2020 13:23:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafb1ab885364f60259d270c2d3791ed51aaf39b5a03364b73600d7dd72f2c4f`  
		Last Modified: Tue, 09 Jun 2020 13:24:18 GMT  
		Size: 184.0 MB (184047168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea9cc53a321a61c0dcc7accf7d1a059153fdd405bd5b16e1dc6fc6c2c902221`  
		Last Modified: Tue, 09 Jun 2020 13:23:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e858d951b016c6b27902affe779566632a4274e26898d0e128bbbc5e9cd856`  
		Last Modified: Tue, 09 Jun 2020 13:24:43 GMT  
		Size: 84.4 MB (84354203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e88070e535eb6222848c6c5e21b81314ea1f15bfc66938d789bae88a1b0eca`  
		Last Modified: Tue, 09 Jun 2020 13:24:23 GMT  
		Size: 193.6 KB (193575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8d803494aafc6c9af2032fd359f9decf7edcf48564b7c282149a840034d22b`  
		Last Modified: Tue, 09 Jun 2020 13:24:45 GMT  
		Size: 74.1 MB (74090252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
