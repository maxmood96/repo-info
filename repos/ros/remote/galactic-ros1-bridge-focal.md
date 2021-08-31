## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:e823c602de06494ad06a3b642b3599685bad58c8e45d71c1256fbbac95aa7aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:3cfba0166cb37b1a2e2b252102343ed7bd265bae34092826d2b39e0664275208
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326842374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb19318f478c5ad3deebb1767360a541c56af0014dd542003565bd5e3e24bf1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:05:32 GMT
ENV ROS_DISTRO=galactic
# Tue, 27 Jul 2021 01:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:06:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:06:17 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:06:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:06:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:07:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:07:15 GMT
ENV ROS1_DISTRO=noetic
# Tue, 27 Jul 2021 01:07:16 GMT
ENV ROS2_DISTRO=galactic
# Tue, 27 Jul 2021 01:07:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:49 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698085f1b967a89a6f46a3ab27fbf0926f76b483b0843140c750e906cdbce36e`  
		Last Modified: Tue, 27 Jul 2021 01:18:43 GMT  
		Size: 103.6 MB (103633085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66de36d29cf49a4bbc2b20c3f5795f7d9c972b6c03fbfef58203d93014aab22`  
		Last Modified: Tue, 27 Jul 2021 01:18:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71385bc5f93112c08888184a0254508d98eb9c547e40f70af98924d3c7f7b735`  
		Last Modified: Tue, 27 Jul 2021 01:19:05 GMT  
		Size: 70.8 MB (70797407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6f08ba387a09b78071f694d7eb0fb4774c732d8bbeba44462bd43acc75d78f`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 241.2 KB (241230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7990cf09456775859f728e71494b2adcec01b46fdbcda5a418970af90f5e5056`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23344c0439abccd2d4aff93d7e57f3697c56daad83902005a615a0e70e52a77c`  
		Last Modified: Tue, 27 Jul 2021 01:18:59 GMT  
		Size: 22.1 MB (22095808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14520e7f4d5e7abaa150d713df486bd446780cf35343d659c964a116fb83314d`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be30453f2f44b3a020e5ec2bfe5b2c6da662ed820f295c10522d1fd3d163da`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83f5e8e2ce60a31e2b6723160edad367d80a1dd8677d7e650af6cd43d84cb6a`  
		Last Modified: Tue, 27 Jul 2021 01:19:35 GMT  
		Size: 78.4 MB (78409624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901678866177d90b4b62b1fe5d39bc27b9c4485b64c290167252b5f8d99f76f9`  
		Last Modified: Tue, 27 Jul 2021 01:19:24 GMT  
		Size: 16.4 MB (16362675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b1b98982ff37b0d26a053f62a31f785d695504cc4b5e359ba3018868504af`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ee3aaa53b5dd9b2f6c0676fdb499beb43d3aa6eb5e7def7a7594da50b85f135c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314996851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9498f260b5eed9c2e2bdae18ec2ac543e03c00e6e934a013f8e6b3f148abe78`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:42:53 GMT
ENV ROS_DISTRO=galactic
# Tue, 31 Aug 2021 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:43:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:43:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:43:33 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:44:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:44:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:44:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:44:46 GMT
ENV ROS1_DISTRO=noetic
# Tue, 31 Aug 2021 02:44:46 GMT
ENV ROS2_DISTRO=galactic
# Tue, 31 Aug 2021 02:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:21 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77fc4622ebe94f4dbfef84290640d2b0a8cb645e806937cae119da66e0a32c`  
		Last Modified: Tue, 31 Aug 2021 02:57:26 GMT  
		Size: 100.0 MB (100037845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1ce4ccd8df8c236b714872e85748b5011a9c784f1308d3e8b7cde6d55cdcf`  
		Last Modified: Tue, 31 Aug 2021 02:57:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f71bfc8c301186b7c6a5b38b04e91f5b5a52d664b2f8270051b08e762181c`  
		Last Modified: Tue, 31 Aug 2021 02:57:48 GMT  
		Size: 65.1 MB (65138271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44554f0d6a1dfdf9fb1da0b542b9e1bcbbecca7421118b2a705e78f5b956b609`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 245.0 KB (245012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217cf8322ac9a1b82365a9710371636864d32637d22bd1d637b2bb97c4ddd306`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120720b5aa2190a67c0c60941709cb411d04a7bc7e208f954115857ef0529410`  
		Last Modified: Tue, 31 Aug 2021 02:57:41 GMT  
		Size: 21.4 MB (21435306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000b79fc3753c17e268692b74af07168e20ef832f41c2b6d51aa4ebdc9b0b584`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcfa3302fc9ef900d7b52b011d213d5500e493f37186bf49394b21ab8667ad9`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267cbfb8468f5b8c83aa8a80301a114a9cfbf2fa9ceecbfbc4199761e9d3a022`  
		Last Modified: Tue, 31 Aug 2021 02:58:21 GMT  
		Size: 78.4 MB (78375726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60cd931079f2558a9451c7b49abf36df676a1d533d65e6a646fe8b96549293`  
		Last Modified: Tue, 31 Aug 2021 02:58:07 GMT  
		Size: 15.9 MB (15890170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9e59276ccde1a327278f910f28b22a92d0e79cfa1b7b11a53e064f99baab37`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
