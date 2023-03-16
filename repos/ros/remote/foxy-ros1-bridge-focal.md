## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:85e6616e9a877d362a59861821b66f37c19a20389506955a71060f8c9915a45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:9da2e17fdcbde4b6c85e683288c16318aeb1abd725f4b8e338b79aa5913e4e8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349048873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5754690238d8794729825bfa477f6b5705e179fbd80c81f41180bb945d7646`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:03:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:09:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:20:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 16 Mar 2023 04:20:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 04:20:27 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 04:20:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 04:20:27 GMT
ENV ROS_DISTRO=foxy
# Thu, 16 Mar 2023 04:21:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:21:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 16 Mar 2023 04:21:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 04:21:25 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 04:21:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:22:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 04:22:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 16 Mar 2023 04:22:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:22:34 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Mar 2023 04:22:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 04:22:35 GMT
ENV ROS1_DISTRO=noetic
# Thu, 16 Mar 2023 04:22:36 GMT
ENV ROS2_DISTRO=foxy
# Thu, 16 Mar 2023 04:23:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:23:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:23:14 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03a3bf9c2e8661d0de58d4a85390b5a17d80f3abf64250efc0769650aa9ab69`  
		Last Modified: Thu, 16 Mar 2023 03:13:05 GMT  
		Size: 1.2 MB (1154522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd341efe0542b6414a62580c02a19287b22de0f35bfdd76fb24d84ae342511e`  
		Last Modified: Thu, 16 Mar 2023 04:43:26 GMT  
		Size: 5.6 MB (5553614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b6c60e4af795544c6d1c364ed29a2ed8c498f2e5da5a57dea651d7c7a523b5`  
		Last Modified: Thu, 16 Mar 2023 04:46:01 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eed6591731f4cd0e89ff07e515fd42f1466e54d5fc27307ce4f3b8ae3afb141`  
		Last Modified: Thu, 16 Mar 2023 04:46:01 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0523ba22e09bf736f80bd994abe837c7b137f287b8eea0f5e7bdbd00da85176c`  
		Last Modified: Thu, 16 Mar 2023 04:46:21 GMT  
		Size: 120.4 MB (120370671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d32eb5055c7800fac72e3cac723ba624a400884ebf5f5a9500ee754097b1e3`  
		Last Modified: Thu, 16 Mar 2023 04:46:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f9d766c59781e81fe431a83896cad4f0713dbabebe97aed5147ad1b93882ff`  
		Last Modified: Thu, 16 Mar 2023 04:46:40 GMT  
		Size: 73.3 MB (73340719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3213fb9cdb02761d0f1588aafdd6d1aea86527d98ac336b4990038700eafd6`  
		Last Modified: Thu, 16 Mar 2023 04:46:30 GMT  
		Size: 279.9 KB (279912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e850f044353a9cd5a3393fdcb430d07b7ed8b8ebdf18fc92426f230eff57e4f9`  
		Last Modified: Thu, 16 Mar 2023 04:46:30 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aabf876615ac9c2be0dd9f801770504d13fde42076b0b2f95e4f68dd0c57216`  
		Last Modified: Thu, 16 Mar 2023 04:46:33 GMT  
		Size: 21.7 MB (21662435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c55c6a35c527c80ba41ab57cfc0aeecbcaf03a8e21d52d510181da679bfac6`  
		Last Modified: Thu, 16 Mar 2023 04:46:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20b731e283d25346685de83f1440763ca136e6cc0a35cbe21422d043b972dd`  
		Last Modified: Thu, 16 Mar 2023 04:46:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20660b50a185f3eeb1a43d67bdaeb11a64c73fe6f4e32197642c8408848c6b18`  
		Last Modified: Thu, 16 Mar 2023 04:47:05 GMT  
		Size: 76.4 MB (76429157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad40a10a98c57a7eb642b09195ade82c9548952e17c9fcf1240770d671c7103`  
		Last Modified: Thu, 16 Mar 2023 04:46:56 GMT  
		Size: 21.7 MB (21674281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13756eb5e96bd40ce7f9ad35d1c2b643de10c62455af3309904258c67215e74`  
		Last Modified: Thu, 16 Mar 2023 04:46:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ae4f7591eae21b9f0abb07cf02221b942789d6336423f1f0b891f77a40ed9e89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317630108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5d55ffb232c17b5db88aa6e0b5cd1d38dd1c0c8c450ffe7bc57137086dd187`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:10:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:10:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:23:12 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 16 Mar 2023 03:23:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 03:23:13 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 03:23:13 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 03:23:13 GMT
ENV ROS_DISTRO=foxy
# Thu, 16 Mar 2023 03:24:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:24:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 16 Mar 2023 03:24:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 03:24:06 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 03:24:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:24:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 03:24:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 16 Mar 2023 03:24:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:24:58 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Mar 2023 03:24:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 03:24:59 GMT
ENV ROS1_DISTRO=noetic
# Thu, 16 Mar 2023 03:24:59 GMT
ENV ROS2_DISTRO=foxy
# Thu, 16 Mar 2023 03:25:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:25:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:25:30 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c235c7a3c272479c47e3fdeef457877dd1bce12f4b4d8726aeb2b8e16d6acae4`  
		Last Modified: Thu, 16 Mar 2023 03:46:17 GMT  
		Size: 1.2 MB (1155462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e62e51f71a010b6fdbdb16725b3bbfca6a13fca1e447d14e311d361db90f4`  
		Last Modified: Thu, 16 Mar 2023 03:46:15 GMT  
		Size: 5.5 MB (5532807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42860775fce781d98f8f21abfafa48660e634182b69b05266851498055971a82`  
		Last Modified: Thu, 16 Mar 2023 03:48:28 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7191287fc71fa37ace07c3fb721fe8b0df2516866da1e7b98f48aa71b8bdb94e`  
		Last Modified: Thu, 16 Mar 2023 03:48:28 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e24d2145f0cc2cf9a85047ab49b1f2f4b457e7b81b534c1bfc25642cd3a10fd`  
		Last Modified: Thu, 16 Mar 2023 03:48:43 GMT  
		Size: 104.6 MB (104568150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27f4054f4fcc5c1a7c641b6a19891c7fe042a2d4ba353b8eb7d094b1ccde304`  
		Last Modified: Thu, 16 Mar 2023 03:48:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b61acdd97d95df9976326ba8a1dc79a739c367e9d0232e2ae3560909a891af4`  
		Last Modified: Thu, 16 Mar 2023 03:48:59 GMT  
		Size: 67.7 MB (67684730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef11b685a5e9052a6bd9772d42b4900972bc1037ca8648eae13801e200578820`  
		Last Modified: Thu, 16 Mar 2023 03:48:52 GMT  
		Size: 279.9 KB (279917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8d4285dfe20611b685fe67cf842b70a9e8b6409de0e9d12bcc27174be70897`  
		Last Modified: Thu, 16 Mar 2023 03:48:51 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab10b5ea657202d97bef2d89bc8b1d0d91f7b99e5f04ee9ef87100edfc1dccd`  
		Last Modified: Thu, 16 Mar 2023 03:48:54 GMT  
		Size: 20.4 MB (20385758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9da9850fbdebec3cf3685151e664e038e2628dd8c09bca753e13b538675fcd`  
		Last Modified: Thu, 16 Mar 2023 03:49:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a82cab40cfa91b60ba64a899790a39b77200d232069659d5aaeaf10ee1dbf92`  
		Last Modified: Thu, 16 Mar 2023 03:49:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf248e08c595e13904d0d40d28e22b9f0f5e586c0f55ceba204e34c55b2d334`  
		Last Modified: Thu, 16 Mar 2023 03:49:23 GMT  
		Size: 76.5 MB (76495934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7713413d61c87cbf93543d08a3a476192cbdf1db9eb33cc0dee39d37f60de8f2`  
		Last Modified: Thu, 16 Mar 2023 03:49:12 GMT  
		Size: 14.3 MB (14325733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ee2466e3b53232367b496f7990dd5a5594945dfa09301dd087beee9b2ce3e8`  
		Last Modified: Thu, 16 Mar 2023 03:49:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
