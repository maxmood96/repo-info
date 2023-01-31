## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:95949afb6a3b9acbea4125d0c93cd6aab1cac26b5fd00d0807be77ea6c81a424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:5d9b84d1a80e0ca534ecca1c4dc021d36b2e58751bd46170f680bc439e1971e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835163354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7880d8ce1763209068646879aaee1b4db773a15f27eff4d6664d0e158c436baa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:19:55 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:19:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:19:57 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Thu, 26 Jan 2023 13:19:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:29:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:30:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:30:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Jan 2023 19:30:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Jan 2023 19:30:03 GMT
ENV LANG=C.UTF-8
# Tue, 31 Jan 2023 19:30:03 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Jan 2023 19:30:03 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Jan 2023 19:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 31 Jan 2023 19:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Jan 2023 19:32:46 GMT
CMD ["bash"]
# Tue, 31 Jan 2023 19:33:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:33:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Jan 2023 19:35:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:42:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c07949706a41bd26517c40195af4c4877c4a94497526c106a6293763dc1765b`  
		Last Modified: Tue, 31 Jan 2023 20:08:43 GMT  
		Size: 1.2 MB (1154542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2670e9e05f7f793dd7dbe48fba615b13142ad5665135c312378240da79579b`  
		Last Modified: Tue, 31 Jan 2023 20:08:41 GMT  
		Size: 5.6 MB (5553673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804981d9bf482904db4b4d104296f3927c0fec21315768200c549e60779cfc1b`  
		Last Modified: Tue, 31 Jan 2023 20:08:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b32c4d8969e5d55023be486caf122cd9d5087fe207766e38640e00eef95b89`  
		Last Modified: Tue, 31 Jan 2023 20:08:41 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8112d9bcc28c8015cc517eaa9d8fa13b7f81c56a16cc1ad99377486ea883d1cc`  
		Last Modified: Tue, 31 Jan 2023 20:09:10 GMT  
		Size: 177.0 MB (177012436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69af09dbb1547496b02120dafb830cdca8c96bb6f57f6c825d29cabbe61bcc9`  
		Last Modified: Tue, 31 Jan 2023 20:08:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f6d27d12c31896425b068abf5aa177ae41dfa12615cf7d2ab85f7a9d4e409c`  
		Last Modified: Tue, 31 Jan 2023 20:09:27 GMT  
		Size: 50.9 MB (50939989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d0675f14db1e48e7d2d1368064952427c6f9db0a5f0a4041fe0529c67da8d`  
		Last Modified: Tue, 31 Jan 2023 20:09:18 GMT  
		Size: 342.5 KB (342485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c42e45b24027e16138a0b07603a15c2800a3a4961df245293946b7ae01dd37`  
		Last Modified: Tue, 31 Jan 2023 20:09:31 GMT  
		Size: 79.6 MB (79606644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260fd7b5f44fab914eb69836104a2061145dba37429bac6110dda9950d899f4f`  
		Last Modified: Tue, 31 Jan 2023 20:11:05 GMT  
		Size: 492.0 MB (491973287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:3d24bba67de87b80e78f3e44edb38826d8315ff381344479d757e0cc59678463
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726201459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108d3ea7464c5f15453d8efcff98b4cb5f8381715bd3a7104c95ccd3d58417e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:35:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:35:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:35:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:35:44 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:35:48 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Thu, 26 Jan 2023 13:35:49 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:33:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:33:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:33:40 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Jan 2023 18:33:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Jan 2023 18:33:41 GMT
ENV LANG=C.UTF-8
# Tue, 31 Jan 2023 18:33:42 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Jan 2023 18:33:42 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Jan 2023 18:36:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:36:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 31 Jan 2023 18:36:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Jan 2023 18:36:43 GMT
CMD ["bash"]
# Tue, 31 Jan 2023 18:37:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:37:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Jan 2023 18:39:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:47:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:316383d79e03258e1fee780854f6da78da364194ded4ace8bff50687070e1c8f`  
		Last Modified: Sat, 28 Jan 2023 04:40:09 GMT  
		Size: 24.6 MB (24586318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73209ac50fce6ee1d3368473e2be1e02425e2cb8fc8ad762895cfb842bee6b08`  
		Last Modified: Tue, 31 Jan 2023 18:51:03 GMT  
		Size: 1.2 MB (1154606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90698334bb1ff08b647a303bd7210b788d1e200280de6e177b452a74bb0818b`  
		Last Modified: Tue, 31 Jan 2023 18:51:01 GMT  
		Size: 4.7 MB (4679059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eab8854e1f5c3635b92c6eb81804fcf72bee4e038f88d66ef405144d7e15c04`  
		Last Modified: Tue, 31 Jan 2023 18:51:01 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c9907fd41c91b73f0149cd68d3dc973c62540b5820090868a78203c0fe6700`  
		Last Modified: Tue, 31 Jan 2023 18:51:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90346d16afe0cbfb1e4a3bf20b71a6d8df7ce2d4c39a9b9d06688e6c7623510`  
		Last Modified: Tue, 31 Jan 2023 18:51:35 GMT  
		Size: 157.5 MB (157513696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0faea215e84eb74a5b274dead0fa5f78341b9258f1a4ef16002d9361ae00046`  
		Last Modified: Tue, 31 Jan 2023 18:51:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce081281d244ace2049f072739dea8f8f6a69c0918ea4a1603f074ee5d2504a`  
		Last Modified: Tue, 31 Jan 2023 18:51:52 GMT  
		Size: 40.5 MB (40502535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078fb972a455f801f8e25fc3a86e886ba908b00aa489021fe2582d639300044e`  
		Last Modified: Tue, 31 Jan 2023 18:51:46 GMT  
		Size: 342.4 KB (342407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4d8ffbfbc59a98c291f4579945a85eade7b60d679f760a4688665d509e9a6f`  
		Last Modified: Tue, 31 Jan 2023 18:51:56 GMT  
		Size: 60.5 MB (60496374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7a33cd68e1a6d4296fe3563c7fe94782695c677984390c977efb26a92781af`  
		Last Modified: Tue, 31 Jan 2023 18:53:46 GMT  
		Size: 436.9 MB (436924048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6bfb3ee3047ec58492603dcd96117685b4f13e06f3efbda52e99a93eb3d78c67
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.4 MB (785410887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba9e06f2b759003d7ca5ae8ffc9203eca2ea6a4ce2dfe454fb30096a6216ed7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:21:57 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:22:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:22:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Jan 2023 19:22:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Jan 2023 19:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 31 Jan 2023 19:22:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Jan 2023 19:22:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Jan 2023 19:24:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:24:57 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 31 Jan 2023 19:24:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Jan 2023 19:24:58 GMT
CMD ["bash"]
# Tue, 31 Jan 2023 19:25:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:25:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Jan 2023 19:27:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:35:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e6380b087085d9b7d1b6b0f477cb1118d8dc3c23beed89295043bc3b4c7b7d`  
		Last Modified: Tue, 31 Jan 2023 19:59:21 GMT  
		Size: 1.2 MB (1154598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cd0e27783c2fceeab20da4ff5fb069eeabebd04b81c662745ccaf81f8bd59e`  
		Last Modified: Tue, 31 Jan 2023 19:59:19 GMT  
		Size: 5.5 MB (5532024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f24679f7f25530861f56fbea52c1295e54ba36bed4d2ebfb0b5b1f90440ab3a`  
		Last Modified: Tue, 31 Jan 2023 19:59:18 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa0bae2649d44ac8b018f5323d3cf124900d32e858787fda15656be5668af33`  
		Last Modified: Tue, 31 Jan 2023 19:59:18 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5a0651ced15d02764547f999abe26c2de60d8affaea46847e78895d82132ab`  
		Last Modified: Tue, 31 Jan 2023 19:59:47 GMT  
		Size: 171.4 MB (171445704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7db3eda367bc7e8524047a533c757ef5afdcbe5afea5b4391418ff9027a24af`  
		Last Modified: Tue, 31 Jan 2023 19:59:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b437ee9e255a2a300ee07d1c69ecf872541734607845309d7193dc660c846d12`  
		Last Modified: Tue, 31 Jan 2023 20:00:01 GMT  
		Size: 45.2 MB (45202843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5ce6608c08a4ba6cc7f5e46690be422b36b83fa275396826c5ae89a9008f3`  
		Last Modified: Tue, 31 Jan 2023 19:59:55 GMT  
		Size: 342.5 KB (342489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632d86abc0d27267c3f6fdc5f8d397ddea31e79d7b9175664874a22a07cb6cd7`  
		Last Modified: Tue, 31 Jan 2023 20:00:06 GMT  
		Size: 72.0 MB (71973502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998d1e8a784d7ce121878c6ceabacebf31c0fb9984e469012663bd6b94df7ee8`  
		Last Modified: Tue, 31 Jan 2023 20:01:26 GMT  
		Size: 462.6 MB (462563581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
