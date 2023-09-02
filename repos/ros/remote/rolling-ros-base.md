## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:7b41d593bdafc3c49a2a06ef745d00c9e28f76ab2ba6f5c29f37661cd32ede92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1eb37637706038cfb3e3a6baf7e050c44875a75a15dd8c806ea6bd8371620f1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268809712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9260100409aea587864f3f4b9cbb2478201645c4d09cd3593d93b567cb51fdc7`
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
# Thu, 17 Aug 2023 07:45:51 GMT
ENV ROS_DISTRO=rolling
# Thu, 17 Aug 2023 07:46:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:46:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 17 Aug 2023 07:46:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:46:34 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:46:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:46:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:47:02 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 17 Aug 2023 07:47:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4a0d826ae8a425a531099a2cdf38a8a676d2b5fed44696baae9f3fb4f616c0a1`  
		Last Modified: Thu, 17 Aug 2023 07:56:58 GMT  
		Size: 124.2 MB (124169199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d8d470a26bf7cf8ff69901448f40e22982e72e083f6467d4d84602b2e172c6`  
		Last Modified: Thu, 17 Aug 2023 07:56:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deace5f39fdb0a253a37240d9f8043cdd448a0eaebac0d89cc3a7128fd8ac095`  
		Last Modified: Thu, 17 Aug 2023 07:57:17 GMT  
		Size: 85.2 MB (85155692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c6f4de5010f71d02db424bfe54429d44e0a17804c731e49664dad582ec2e32`  
		Last Modified: Thu, 17 Aug 2023 07:57:07 GMT  
		Size: 293.9 KB (293863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64ba642bde73cfe3a6ed7a25367f07e6a21db84621553450c6a047d95933344`  
		Last Modified: Thu, 17 Aug 2023 07:57:07 GMT  
		Size: 2.4 KB (2409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7739dea0f29e15d1bc9d1d3914d5a905adf6ac5efe47d1bf33bcfcef52abb4`  
		Last Modified: Thu, 17 Aug 2023 07:57:10 GMT  
		Size: 23.7 MB (23706340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:40cfdd3d89ecf88a0f9228fcffeca26d2c45a1f7670a4e18504c2307c5b4989f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261280765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0594f5593323d6af3a45c4ef0368843cd518e0818d6937647217e985488d53`
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
# Sat, 02 Sep 2023 00:39:16 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Sep 2023 00:39:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:40:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Sep 2023 00:40:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Sep 2023 00:40:01 GMT
CMD ["bash"]
# Sat, 02 Sep 2023 00:40:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:40:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Sep 2023 00:40:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Sep 2023 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:fac57ba3d69f161b5cbcaaf5bcb4371f6b36256c810306cfcc4f2c779904f27e`  
		Last Modified: Sat, 02 Sep 2023 00:47:51 GMT  
		Size: 121.6 MB (121622867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f819035049306e4fd5b131a0971c2daff48f95c0c0cc378aec37ab0e1cb291`  
		Last Modified: Sat, 02 Sep 2023 00:47:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d6143eb2220e8d9afb221d0fa655a5077c5f98b5f6a64c4b7bc581df94207d`  
		Last Modified: Sat, 02 Sep 2023 00:48:07 GMT  
		Size: 82.8 MB (82840195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99426183657f085286925e298ba13fe7c3ffdeb4fdaae65eff9e7fa08d3d537`  
		Last Modified: Sat, 02 Sep 2023 00:47:59 GMT  
		Size: 296.4 KB (296418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed58b9cae2a1ecd194bbd9e221feb51eab6abd8e334f13d9aeaeab299b9378b`  
		Last Modified: Sat, 02 Sep 2023 00:47:59 GMT  
		Size: 2.4 KB (2397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1320cc5b95f582bfb8ee5c8d92da3bc220dac1fbdc8a1de8c5fec4a3243db88e`  
		Last Modified: Sat, 02 Sep 2023 00:48:02 GMT  
		Size: 23.1 MB (23105075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
