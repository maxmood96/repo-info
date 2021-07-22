## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:ed99e701d67fed21249aeeab42f1793511203c2b3dc724183a2544c56607280c
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
$ docker pull ros@sha256:4185918e89325b55017522d348e538aa76fab90f83beb6ff7b58f029cbba5335
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423985866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c7bc6a80756eb0ec2452a29c1063dcd54e4b0845cc169539962bb988bbfcf9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:59 GMT
ADD file:3e8e075f08a6b727602af05c539f43648a48663cbb3a88eeba310cfc32c01d78 in / 
# Thu, 22 Jul 2021 00:40:00 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:23:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:23:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 22 Jul 2021 12:23:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 22 Jul 2021 12:23:13 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 12:23:13 GMT
ENV LC_ALL=C.UTF-8
# Thu, 22 Jul 2021 12:23:13 GMT
ENV ROS_DISTRO=noetic
# Thu, 22 Jul 2021 12:24:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:24:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 22 Jul 2021 12:24:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 22 Jul 2021 12:24:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:24:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:24:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 22 Jul 2021 12:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:25:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d272b0d8f7c4fd0caf0ef022ce544cfe3800e349a73b585f82837e6526a4247e`  
		Last Modified: Thu, 22 Jul 2021 00:45:18 GMT  
		Size: 49.2 MB (49222109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be023b22932cf47a4eb2115be15d3539f42a9ba7f9e98e522ed582fea89d40ee`  
		Last Modified: Thu, 22 Jul 2021 12:30:33 GMT  
		Size: 10.9 MB (10883239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb89b3f136886dea2466ea37659c55816ee15ebbf27efcfa566bbfc6a0384ab2`  
		Last Modified: Thu, 22 Jul 2021 12:30:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524675b4de3d1ee20d4a04933115962a10c720490abede3b8f36e10eaca5459`  
		Last Modified: Thu, 22 Jul 2021 12:30:31 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fbd2e0d882c66b95029d4dfcf0c4e74d13cda2c7384b2a05c68ede1a772f1a`  
		Last Modified: Thu, 22 Jul 2021 12:31:04 GMT  
		Size: 184.2 MB (184228886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5d957f3309d21e8071f4420302d491f5888cc1cda7dc47be23381343b24229`  
		Last Modified: Thu, 22 Jul 2021 12:30:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1abb177db0c6957e16f2623b80172d001eda36151c5c11fb362295292e0770`  
		Last Modified: Thu, 22 Jul 2021 12:31:24 GMT  
		Size: 84.4 MB (84358083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f870b59a8cbee52a2156009d6000e43da6e47aa64620f552a819fe668656e4`  
		Last Modified: Thu, 22 Jul 2021 12:31:13 GMT  
		Size: 307.5 KB (307547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1425c523ebd4c20244bcc2aa541c97cde933812583ffa085a0eb7f47503c35`  
		Last Modified: Thu, 22 Jul 2021 12:31:23 GMT  
		Size: 74.1 MB (74087996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765f3948e8f3422392178187ba9aff2c14a86239f065129ed760e293e7a11335`  
		Last Modified: Thu, 22 Jul 2021 12:31:38 GMT  
		Size: 20.9 MB (20895591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
