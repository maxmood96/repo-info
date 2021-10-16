## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:99f1c176a39d64a79a3cb84cb375b0bc012286f2d345bd479e43758e5bb9c15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:d6a691738fa31cf6f356ae929c63fa9c3cee10fa2a11b85aaeddea89cdc6bf21
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 MB (345574883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03ee3a802313ea6d94c4ea06dcf0a4ea7d519713184674747a57bd5e0705497`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:53:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:26:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:37:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 16 Oct 2021 03:37:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 03:37:51 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 03:37:51 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 Oct 2021 03:37:51 GMT
ENV ROS_DISTRO=foxy
# Sat, 16 Oct 2021 03:38:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:38:52 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 16 Oct 2021 03:38:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 03:38:52 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:39:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:39:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 03:39:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 16 Oct 2021 03:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:40:04 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 03:40:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 03:40:10 GMT
ENV ROS1_DISTRO=noetic
# Sat, 16 Oct 2021 03:40:10 GMT
ENV ROS2_DISTRO=foxy
# Sat, 16 Oct 2021 03:40:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.13-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:40:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:40:54 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3c993d4c25d2ec8adbe5b497acc2226d8b6b602f68679037b8993f53617e2b`  
		Last Modified: Sat, 16 Oct 2021 03:02:27 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e9dfa7092d8b77085dc1f7f400d3a0618187cefd4af7037e9dec2f88eadec7`  
		Last Modified: Sat, 16 Oct 2021 03:46:47 GMT  
		Size: 5.5 MB (5547495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc9a74c1dba9c88845d88e89e5987b2c38fa8df2fceefed614e3f8cf7d835b5`  
		Last Modified: Sat, 16 Oct 2021 03:49:29 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8299091b3ca45435fb28fad59303294248fb9b00ddcdf278f067eb472a8c86ef`  
		Last Modified: Sat, 16 Oct 2021 03:49:29 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1ceb427087b3041b32a2be8c73788330f9675008ba201372eac0b4efc2cc18`  
		Last Modified: Sat, 16 Oct 2021 03:49:49 GMT  
		Size: 120.0 MB (119985810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7b97e74c6f685d0d0a9362a5cf4a8769e1696bbf995293763867daaba3d19`  
		Last Modified: Sat, 16 Oct 2021 03:49:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7748c6e4eab99c248c57227d0705c45d1b5c16a2a61bc6e2b4390c76f5346b70`  
		Last Modified: Sat, 16 Oct 2021 03:50:09 GMT  
		Size: 70.8 MB (70844958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204e3cb07dc82bf75a08f0e4498123299d9e74ab8013405bfcf2d7c06b149b00`  
		Last Modified: Sat, 16 Oct 2021 03:49:59 GMT  
		Size: 244.9 KB (244893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbf530a707a11219db69d544ff5edbf747a4541147f82d4c0a9072da290fe8f`  
		Last Modified: Sat, 16 Oct 2021 03:49:59 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d0f031d5ee8d2a1754ef8291702f1ddc0a60f24fe9e0f529f7d6bbefa59828`  
		Last Modified: Sat, 16 Oct 2021 03:50:01 GMT  
		Size: 10.3 MB (10288974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3266ccdb42b1bec97ebd06d1c3eaa4d779d288eb37ae26849976749b79c80ae3`  
		Last Modified: Sat, 16 Oct 2021 03:50:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bef8c1f330d77992b360d005a576e48ec3d99fd46b1987a0ea1b1040582c021`  
		Last Modified: Sat, 16 Oct 2021 03:50:25 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb3ee012879069e106e17763a6e2d3e49c73191dd093ef747c5b2e3169bc98e`  
		Last Modified: Sat, 16 Oct 2021 03:50:40 GMT  
		Size: 76.1 MB (76133715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f37efb0fea05d9d8bcc998f6107f9c748ff4392c0b21867cf7932632b57f3`  
		Last Modified: Sat, 16 Oct 2021 03:50:32 GMT  
		Size: 32.8 MB (32770666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99793e32227b0d56e1de7b3a51a55c90f798adef85c7e29bf5612a90f185ecbb`  
		Last Modified: Sat, 16 Oct 2021 03:50:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ee4e073ea4611160dbbfc6de7e157c317c5e33164af06dc142b4d41c884682e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313238986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3d34c3c3c4bc62fbf29383cca6753f61c1310a64555bbd09b26b322e39c6c2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:19:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:19:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:30:39 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 16 Oct 2021 02:30:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 02:30:41 GMT
ENV LANG=C.UTF-8
# Sat, 16 Oct 2021 02:30:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 16 Oct 2021 02:30:43 GMT
ENV ROS_DISTRO=foxy
# Sat, 16 Oct 2021 02:31:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:31:37 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 16 Oct 2021 02:31:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 02:31:38 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:32:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:32:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 02:32:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 16 Oct 2021 02:32:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:32:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 02:32:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 02:32:47 GMT
ENV ROS1_DISTRO=noetic
# Sat, 16 Oct 2021 02:32:48 GMT
ENV ROS2_DISTRO=foxy
# Sat, 16 Oct 2021 02:33:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.13-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:33:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:33:46 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44426e3a0ed188569ceb995612f61d01b012f19e6849dacdcdef24f70e9e820b`  
		Last Modified: Sat, 16 Oct 2021 02:44:04 GMT  
		Size: 1.2 MB (1186725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74557b92a76c488a6e2f31c091f03671baadbd5b593c4af9dbde2baea1616333`  
		Last Modified: Sat, 16 Oct 2021 02:44:02 GMT  
		Size: 5.3 MB (5322455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799e8bd4d8f9479b13bd0d148a873ef866dc81e123396022ca5230b690127bc`  
		Last Modified: Sat, 16 Oct 2021 02:49:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac91bb16ec2aa9ad80cd7ef5c44472bd9691216081f8f16049fb6a2b377b9cf`  
		Last Modified: Sat, 16 Oct 2021 02:49:08 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149fc655748fb600fd752cb6805c8a4ca22cb195276c6222f500719d598fb59c`  
		Last Modified: Sat, 16 Oct 2021 02:49:26 GMT  
		Size: 104.2 MB (104159054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa569375e41dce495d90956baf65112208fd3655215fd4563bd0dd5a665da217`  
		Last Modified: Sat, 16 Oct 2021 02:49:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b885237a11c3c3a5e31b49a568d28e2f32c00c1cde49be15ef946313a54218c`  
		Last Modified: Sat, 16 Oct 2021 02:49:47 GMT  
		Size: 65.0 MB (64966810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c0695bf566d5652b3dd582cbc3fabac21343dc6476601a5fae98304412675a`  
		Last Modified: Sat, 16 Oct 2021 02:49:38 GMT  
		Size: 244.8 KB (244842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8067ff73af3c358526193f7ea6d83e770f689e4b23865209c2b5f56b3d9d56`  
		Last Modified: Sat, 16 Oct 2021 02:49:38 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85d6588bac0c377f420f223ef5eff321027f991a1cbf69f707bf743e3248758`  
		Last Modified: Sat, 16 Oct 2021 02:49:39 GMT  
		Size: 9.1 MB (9085686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b3f8b242de8613b5d45b654f5bf5568fd17f9a92cbd928b34797b63391423`  
		Last Modified: Sat, 16 Oct 2021 02:50:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a8a5380e7abb39261fa5400a00576025d4eb11caeeb986aaaf2c8568bf5f8d`  
		Last Modified: Sat, 16 Oct 2021 02:50:20 GMT  
		Size: 76.0 MB (75965631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed331b81210890b615cf836e0ee15a88c272727bd3297ae76a759d75a13e876`  
		Last Modified: Sat, 16 Oct 2021 02:50:09 GMT  
		Size: 25.1 MB (25132062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93afdda0273b3dcaa4f74bf774af1ab186012afe83faac4c6fb6a1b09af2e2`  
		Last Modified: Sat, 16 Oct 2021 02:50:05 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
