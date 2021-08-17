## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:ba2af5705274be54c5c7bc4c2af3dd55746cac3104d4806966a230f145b75eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:a8073a9adad5a48c446d33a95857af8de66a895fda2e750aef52aa6e99abbe42
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.4 MB (484449232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e571f51b7738b8d0d5a28b07de98b65d04a2ff5c1869304043ec23501e65c58`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 16:55:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:55:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 22 Jul 2021 16:55:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 22 Jul 2021 16:55:21 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 16:55:21 GMT
ENV LC_ALL=C.UTF-8
# Thu, 22 Jul 2021 16:55:22 GMT
ENV ROS_DISTRO=noetic
# Thu, 22 Jul 2021 16:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:57:08 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 22 Jul 2021 16:57:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 22 Jul 2021 16:57:09 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 16:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 22 Jul 2021 16:58:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:58:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a9e23cef13844415a9e0ba738d8dc842b835b642b50a5db44454ea7e17fb2c`  
		Last Modified: Thu, 22 Jul 2021 17:03:25 GMT  
		Size: 10.9 MB (10891942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f052a978ee78e2b721188ef00943552621db3d886d2e64c500b6cd546cb1f62`  
		Last Modified: Thu, 22 Jul 2021 17:03:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b972a8116085130ea1f7e2b694ca5364cc60dd8e15293c63337d7ea3d76028`  
		Last Modified: Thu, 22 Jul 2021 17:03:23 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e227b764282c7d358f86921d1dc30539fa889a1387502cdc44e4a05476557705`  
		Last Modified: Thu, 22 Jul 2021 17:04:08 GMT  
		Size: 239.1 MB (239050293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c25a4064f898eb049bc3943b87c6834f8ab8642db76c541df1c56006af45a`  
		Last Modified: Thu, 22 Jul 2021 17:03:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fcfacf13e0398090f4e417f9a1f53dd645ba6623f81e4b713439601bc96c4b`  
		Last Modified: Thu, 22 Jul 2021 17:04:38 GMT  
		Size: 86.6 MB (86566666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3fa5b953282ec24c6c60894c5106091e3b0db0680ccc9e618f701aad2b9f30`  
		Last Modified: Thu, 22 Jul 2021 17:04:17 GMT  
		Size: 307.6 KB (307555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300b0b07c0245b4e89bf87395093e158c06583aea73f0663de4afd50714228b3`  
		Last Modified: Thu, 22 Jul 2021 17:04:35 GMT  
		Size: 76.0 MB (75974971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8575a97d69e24bd7a153337b8d37f77a212194efa9169b334aa765d7211b7446`  
		Last Modified: Thu, 22 Jul 2021 17:04:50 GMT  
		Size: 21.2 MB (21219764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a71321e849437464740dadf3a7d92ba33aa9cd325313096b2092348fc5582503
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423996486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1339d6e7c2ba9eca967117d5d0a6a8b425002eb4c8f7803111013392eb2e9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:16 GMT
ADD file:9e7d801ba29c50f7388cf80395faef75e0b4db056e16d1117293539bda895467 in / 
# Tue, 17 Aug 2021 01:46:16 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:48:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 11:48:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 11:49:00 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 11:49:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:49:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 11:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 11:49:54 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:50:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 11:50:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b721438f56fc7c4bf10a9f9ac58d22b52d97c50353a44f531fb5b7a70314e642`  
		Last Modified: Tue, 17 Aug 2021 01:53:52 GMT  
		Size: 49.2 MB (49222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21602f601a18ce34c8a479ae1d7bac4442282478925664d6f67ad1d2b34e020`  
		Last Modified: Tue, 17 Aug 2021 11:56:11 GMT  
		Size: 10.9 MB (10883354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630d4e557cfdbdf3a855acc0ae4cb3c204ac63ae1dd071cd42e608dcb0645c2d`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f24119c6422825783e8ee727d9b12a12c7cb5605e9b6e883b5101a388b450a`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd82c4517707ac42892fd33d02b10b53c8eb41cf05683d381df617056c035fd`  
		Last Modified: Tue, 17 Aug 2021 11:56:42 GMT  
		Size: 184.2 MB (184236324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bbd42e097110d8576baa6d6d16c7a91e608fad20f3b7978c7e0e99f4ee7df`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf124f136abb277ab2e63f14af6802ccc288e34cc0c43a7d62f7c42717f23e3`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 84.4 MB (84358116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6515efab5054193f9a8defd851ec9536c17950ae722b38778b4bd6aef481e9`  
		Last Modified: Tue, 17 Aug 2021 11:56:51 GMT  
		Size: 310.1 KB (310090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa915bc3d0bc2ea62806da8704257a5df824c41fa8997831b5de9ac482cca14`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 74.1 MB (74087852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1b5f110e2990823b69a716c68ef7506a92319e4d3c59c1991db59244653d1`  
		Last Modified: Tue, 17 Aug 2021 11:57:14 GMT  
		Size: 20.9 MB (20895975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
