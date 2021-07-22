## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:1d62c0d33379ba841465eb0b68848dcc3724b22757241659357b8c4ff8ea1e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:b884f292185ac0ae98aebb04cf31454443d602f12961865c6674cc528866ddc1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **968.0 MB (968008431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c7931a72bc6c06c98128ca55e05b1708bc1d87649b38e1c2fcd18dae9e4b95`
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
# Thu, 22 Jul 2021 17:01:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:aeebd989eb414b251471fe6071832683acde2a3d4e27ace5ec3f0f56be620acf`  
		Last Modified: Thu, 22 Jul 2021 17:06:28 GMT  
		Size: 504.8 MB (504778963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e4ccf144d6fa5685d3b764dbdd643e1644626f973fce66c71949569f2209f3a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.8 MB (884775941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa3e64aed6dd243473f2bb53890d4885fc9075284c2ce929bdf8eba77f23374`
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
# Thu, 22 Jul 2021 12:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:491805f2edd7a83e685a2114035aef7aff269ddcca8ec7371d67d6e51eb33164`  
		Last Modified: Thu, 22 Jul 2021 12:33:02 GMT  
		Size: 481.7 MB (481685666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
