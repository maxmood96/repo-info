## `ros:iron`

```console
$ docker pull ros@sha256:31fc87b52b7eb766520a117fa69c9df3629525e81fae6e04e40051e04bab22c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:607ee8119333c9efcfd1867133359185a17b8cbc4b979dbea7c408f1f9f0fb30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268834339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628c188ccfe1fc5e02bd3f2202e95db70a72ec1a51b4a7de8f98d4f168ccf22`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 07:31:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:31:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:31:36 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 17 Aug 2023 07:31:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:31:37 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:31:37 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:42:34 GMT
ENV ROS_DISTRO=iron
# Thu, 17 Aug 2023 07:43:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:43:20 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 17 Aug 2023 07:43:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:43:20 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:43:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:43:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:43:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 17 Aug 2023 07:44:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600b47cfe73537fcd64a009d5dacdcf7d702797d171ab8db562b76b0eae3a99f`  
		Last Modified: Thu, 17 Aug 2023 07:51:54 GMT  
		Size: 1.2 MB (1212944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f425b271337eb04909cb8bf9e639e501a7ed053df9f2e3ba7cc4f8f5d36e1e`  
		Last Modified: Thu, 17 Aug 2023 07:51:52 GMT  
		Size: 3.8 MB (3828890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0344b496bb0e17c4da2c4bcb2f517df43eb98024c48e14a1ffb3d6d8d84dff20`  
		Last Modified: Thu, 17 Aug 2023 07:51:51 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e06b3b3a15b8db0305dcb972029d07a91201f5e9b63f029914575556fd4ac57`  
		Last Modified: Thu, 17 Aug 2023 07:51:51 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881b222f849bf63f5701c0c6b3ec3e4caa00564dc15f8e0e07c59fb0889b2492`  
		Last Modified: Thu, 17 Aug 2023 07:54:36 GMT  
		Size: 124.2 MB (124168096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cab8740f7a2572e1314cb6a9658b354a54c760904fe7f761f1fb08c3f6db9c7`  
		Last Modified: Thu, 17 Aug 2023 07:54:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785d659073790018ac331d7d48e698b788cda24c1110012e78885af72a4aba03`  
		Last Modified: Thu, 17 Aug 2023 07:54:55 GMT  
		Size: 85.2 MB (85155472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225db91c69f1fdc24aafe3f0f1b4c80a63e4d8c350e3f8a5e6d25e9751b996ce`  
		Last Modified: Thu, 17 Aug 2023 07:54:45 GMT  
		Size: 299.8 KB (299846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2739eabab267a52d5893d16b9c3e3db87d7be205d190f77c9e35a0c6807ca8ab`  
		Last Modified: Thu, 17 Aug 2023 07:54:44 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc314b73ffce739a82bcb63f04e653a43b3a26ae47df7f35305b0d54dd706654`  
		Last Modified: Thu, 17 Aug 2023 07:54:48 GMT  
		Size: 23.7 MB (23726301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:31a5be63ab3b2fe0edd2aa2a6cc114a8d681c7b43bace413d0d67dd215dc958a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261313267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb5b932dd24d525cfc727ed1de564380748feed2f728000e8a3c38b41087348`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:23:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:23:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:23:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Sep 2023 00:23:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Sep 2023 00:23:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Sep 2023 00:23:43 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Sep 2023 00:35:55 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Sep 2023 00:36:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:36:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Sep 2023 00:36:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Sep 2023 00:36:41 GMT
CMD ["bash"]
# Sat, 02 Sep 2023 00:36:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:37:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Sep 2023 00:37:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Sep 2023 00:37:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459959187d1cd1ed01b1de7494f5bb59b926b9976aed48c10c5e308b617f3a64`  
		Last Modified: Sat, 02 Sep 2023 00:43:02 GMT  
		Size: 1.2 MB (1215524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440f0140b644ef647ab4b336f96b8f557b1b5b55664bc032127b6dd99046456b`  
		Last Modified: Sat, 02 Sep 2023 00:43:00 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee378876d0254603b8b7793ae409c0503de6acfa52cc70d5e7855dafbdd1d783`  
		Last Modified: Sat, 02 Sep 2023 00:43:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb175d09d5d9ec6033b5d0507062ba5aeb144487d0679a1f01cb2f5b08e768f4`  
		Last Modified: Sat, 02 Sep 2023 00:43:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48558794d076ebc8d1292a959ac39a17e7683b2b9a85b38a6553e7667413408`  
		Last Modified: Sat, 02 Sep 2023 00:45:43 GMT  
		Size: 121.6 MB (121639017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4068f1ecb356b50671aad74bab133f4c7173d2c5544374a926bb511c509d0a6`  
		Last Modified: Sat, 02 Sep 2023 00:45:23 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcb57bc4c7d7e86f5a699347526dd36d6d6a796ca281a1c43190a17b675f70d`  
		Last Modified: Sat, 02 Sep 2023 00:46:00 GMT  
		Size: 82.8 MB (82840292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f472afd96ac321a5e6cadf1a1f9d0468065b38db7177e38ee01ef8f5caa1a426`  
		Last Modified: Sat, 02 Sep 2023 00:45:52 GMT  
		Size: 301.8 KB (301784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792c71e1cd7464d234a82b207e6d65c1d368e11b7d519a91a05eed7c028cb33d`  
		Last Modified: Sat, 02 Sep 2023 00:45:52 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3335d0568506900d516401d3bb154f04e931bb4304218a71377ef3c4a8286c`  
		Last Modified: Sat, 02 Sep 2023 00:45:56 GMT  
		Size: 23.1 MB (23115925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
