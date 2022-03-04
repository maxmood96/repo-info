## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:f72486be3c09d539e3dd61144de6ac5b2e83a8942f53d2f382ad43d33f8125c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:db32264c05d9a644cb3d824c53f58925f6bc2a9a20cf906400136712fffc7e64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437400143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07b45da64ef12de4aa8a95490faff003d1b0e2fd1bb34b725a2a7736d4f0719`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:527edd5cb53dda632d40f47b024ef6c14c249e67293604c1034b8f621dafa4ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385890767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21394d3b4c786ff653a964f7dab4509dc78cbb489a7c17258bc1dac8ac6d1a1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aed820f4237dbd767f9d71944780cc89346127cdfe2c63ca5d2211f555866220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411547352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c8ad27d9dbc3d3329751a3c83aa314989729f01071e231f59ac9c938a12e4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:17:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:18:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908fc1da6687829639272ef87642b5189b703086a36418bd251644d6cf90a838`  
		Last Modified: Thu, 03 Mar 2022 21:39:54 GMT  
		Size: 63.1 MB (63067275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80f61cfdf9250e18c6dde75bca8870207161d0f38c1ef62f5505293cf93b3b`  
		Last Modified: Thu, 03 Mar 2022 21:39:46 GMT  
		Size: 277.3 KB (277339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e820e23ff014d59bcfd20cb2799ec78174c68fb17f14b25296ab734d5d103`  
		Last Modified: Thu, 03 Mar 2022 21:39:56 GMT  
		Size: 67.0 MB (67002031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
