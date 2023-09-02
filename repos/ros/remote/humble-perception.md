## `ros:humble-perception`

```console
$ docker pull ros@sha256:ab9f144784da3c3968bc720c4c7ec1a7d3aa966203e592b0a62c3c4491ba83d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:dfabb1a593195fc15ea602b8c4c900b366b94d370db22dabf21fbdd6cbd65299
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.6 MB (953615780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e94c09f4b5978468488dced7ba48854a6c6e673c2d839d0d32d70ce6d0a35c`
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
# Thu, 17 Aug 2023 07:31:37 GMT
ENV ROS_DISTRO=humble
# Thu, 17 Aug 2023 07:33:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 17 Aug 2023 07:33:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:33:12 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:34:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:34:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:34:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 17 Aug 2023 07:34:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:42:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9eb70872c7bc069482cc1fecdc64dfdbe4e98b4b52b2f0961c0af76751f63bc3`  
		Last Modified: Thu, 17 Aug 2023 07:52:07 GMT  
		Size: 106.4 MB (106416908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaca63120feaf1722b2a93a621c439d3a643fd0fe9beed50bdac14ad16ce5d2`  
		Last Modified: Thu, 17 Aug 2023 07:51:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024278867e7eb85a13798e71fa98a3d4187d0d4888614d0b0cccbe42fcc6f7e7`  
		Last Modified: Thu, 17 Aug 2023 07:52:28 GMT  
		Size: 98.1 MB (98120033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dac9f5526003e7c8ac018dd6cc7aade32c5fb8cb9ff8f596ff781616a3358e`  
		Last Modified: Thu, 17 Aug 2023 07:52:16 GMT  
		Size: 312.4 KB (312355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6689ce17b641b850e589f3b40c2a01260c55e0db08451320aa4b1c22bc04fd86`  
		Last Modified: Thu, 17 Aug 2023 07:52:16 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62756e04638f7a4baa40728ef77214913ad88f874930378d247b3261d560782f`  
		Last Modified: Thu, 17 Aug 2023 07:52:19 GMT  
		Size: 23.1 MB (23090160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1ed7ce572a63c8bec3156aa887f6e833bd0066abca8f70d1b6644b7c07db4b`  
		Last Modified: Thu, 17 Aug 2023 07:54:08 GMT  
		Size: 690.2 MB (690191668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a1012f29357f78f9bb00ce55bfc95072973d6ae73627674b5ef4837114001aa7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914088422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2193a560c90e7968ca85465a319d367d990e8026e8a668ee951ee34c2da0fc9`
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
# Sat, 02 Sep 2023 00:23:43 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Sep 2023 00:25:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:25:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Sep 2023 00:25:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Sep 2023 00:25:07 GMT
CMD ["bash"]
# Sat, 02 Sep 2023 00:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Sep 2023 00:25:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Sep 2023 00:26:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2a295b8a66bcb3a64684c4c57388e4c53eb16e08c6388d1c528220854c1473c9`  
		Last Modified: Sat, 02 Sep 2023 00:43:20 GMT  
		Size: 104.1 MB (104123742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843c4bd601a8295db4d64a4af68d90f98ebf28ee9bc4831d0d8ef6900fc2e27b`  
		Last Modified: Sat, 02 Sep 2023 00:43:00 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450003932f122cef453b721c74a349ef5e6dee2503cfafdc5584691209809c19`  
		Last Modified: Sat, 02 Sep 2023 00:43:40 GMT  
		Size: 95.7 MB (95680017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123ca121d14fe945dfc4c8138cbdfd144695d6634e53ecd9739b0a38280a10bb`  
		Last Modified: Sat, 02 Sep 2023 00:43:29 GMT  
		Size: 314.3 KB (314295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dba5301f57280a3b5523918a7706a4f75580c5c0d0f18fc694c055af5135216`  
		Last Modified: Sat, 02 Sep 2023 00:43:29 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c9442090566b229f0b496eb3db50f6b3464c97769f46550dc5f4bc098e7a7f`  
		Last Modified: Sat, 02 Sep 2023 00:43:33 GMT  
		Size: 22.5 MB (22515200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8590d691e0846807c4802d8a4a74d60b6d0600c0a2d1cc6da88d0e6899e06d8`  
		Last Modified: Sat, 02 Sep 2023 00:45:14 GMT  
		Size: 658.0 MB (658038945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
