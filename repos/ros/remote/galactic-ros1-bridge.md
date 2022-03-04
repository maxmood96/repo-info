## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:e8423998a53717145f0fdd7f6490fcc32803ae304e9968ad6b333a66a504fc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:27a670666d8ccff4e83882b79f9867abd92d98910475a9f2f62cfad1ebf45b5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327118570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aafcbea07b171b4f69586b3745f9b45c50da133bcf370ad143a186e6f27ac6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:11:02 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:11:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:11:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:11:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:12:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 23:13:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:13:12 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 23:13:12 GMT
ENV ROS2_DISTRO=galactic
# Thu, 03 Mar 2022 23:13:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:13:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:13:45 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b248cd64c64d8e30c5cb2f7ea8dbecb02fab8491c449e0048783e3c1205d124d`  
		Last Modified: Thu, 03 Mar 2022 23:27:34 GMT  
		Size: 103.7 MB (103667338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e15bc9621edeab205d7571ce463791887cabdc21b9e8e1ac5935a76ebb995`  
		Last Modified: Thu, 03 Mar 2022 23:27:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732c3e362fa680af3dd9651f9aec63ef06df9c94b1a1dd431f145c87d748f54`  
		Last Modified: Thu, 03 Mar 2022 23:27:56 GMT  
		Size: 70.8 MB (70810157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701903a724365f87cb60a32b5451bd9fd1cb50c2e4dee6654808a8feb0f2e8f`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 259.1 KB (259109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752acc754cec460fa8bcbdba673e5550046741728000255b0703d7452f6536fe`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 2.2 KB (2197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3863acee3e82cec893523789175d85445eb3c8b9cb65be831fda3921510ed3`  
		Last Modified: Thu, 03 Mar 2022 23:27:49 GMT  
		Size: 22.1 MB (22112701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e7b46e5b5f113985bacb845856e85d14963d36d088ceaa252db41356811896`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8138ddd0a976f036fb80071ba323cba6da065e2558abc4db3df504995762de6`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cca671b57fb188baee96041b23f929cba69e33bf3a2ea94411119dec659f6e2`  
		Last Modified: Thu, 03 Mar 2022 23:28:29 GMT  
		Size: 78.6 MB (78598774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaab2677aec32303bba20adc1ec9701c5032f47334ac1e5ea197dddf17f1aa31`  
		Last Modified: Thu, 03 Mar 2022 23:28:14 GMT  
		Size: 16.4 MB (16370626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c08b09b5b4a5ca6937134a3af1433aae5df635fc9254b400c7c2c8fb7ac715`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:410823f474c93353c212c190f415e4a0e1301610fc7a1272cb74cb4047035703
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314348568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a5389ec8da4846fd1dae53e6425e1dd4244a2a37365e008f1c8d99a9f9e86a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:30:49 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 21:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:31:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:31:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:31:43 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:32:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:32:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:52 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:33:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:33:23 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 21:33:25 GMT
ENV ROS2_DISTRO=galactic
# Thu, 03 Mar 2022 21:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:16 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74ba87af23be8f4aafd5c8302b2c467c2e6e67b9794d06802e60b060e39bfd`  
		Last Modified: Thu, 03 Mar 2022 21:45:48 GMT  
		Size: 100.0 MB (100046542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c4b0afbfb88a5779d6abf06adb29ca9d54b62d91ea159930e32462307ceea4`  
		Last Modified: Thu, 03 Mar 2022 21:45:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345c2a2a8a38fcc2d0b77b5163370614cc12f1b4ea4d4ad4788daf63b495e62d`  
		Last Modified: Thu, 03 Mar 2022 21:46:09 GMT  
		Size: 64.9 MB (64933636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aceb2a5ab9c6f59cd0a5078300dc2090bc5bca6d071cd804997dce357ee33d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 259.1 KB (259066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fcb9bad2c4037cdb5644f47bcf33538409d201e1138610e734d9f92899033d`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c97bb6461d23f7baa16c6659051576ee711edb2c04d350122e94eec49fa15af`  
		Last Modified: Thu, 03 Mar 2022 21:46:03 GMT  
		Size: 21.4 MB (21435107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fab5e336e5e39a97b55eb611e6a9a384dfd59d4b0a3b6233a8cd8b28d8cc0d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6830c0744c85b7f4dedaf77d774a3e56a947aff0a8038943ef82f3ee3151d7`  
		Last Modified: Thu, 03 Mar 2022 21:46:39 GMT  
		Size: 78.3 MB (78323318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d6996295c1690911f8f20370aab626e914d0617128bcfd8ea7f61318620e3`  
		Last Modified: Thu, 03 Mar 2022 21:46:27 GMT  
		Size: 15.7 MB (15670064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e92b1df749ade68a89f261301805003060e300745185b6f9a12e2cf32f3d52`  
		Last Modified: Thu, 03 Mar 2022 21:46:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
