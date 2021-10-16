## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:2460c7566039843af23a4225886759e22c4baed07b7614868be17609eab3edef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:c6dd40e51f57c2ec7e1b8738e8c26a6c475a648dd84e0a4deb9a28ce4ef28fd7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326882035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f301a02130abaf6bbb58b78735b412ab18b95ba7732b267e56c41d0042546e`
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
# Sat, 16 Oct 2021 03:41:01 GMT
ENV ROS_DISTRO=galactic
# Sat, 16 Oct 2021 03:41:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:41:44 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 16 Oct 2021 03:41:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 03:41:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:42:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:42:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 03:42:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 16 Oct 2021 03:42:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:42:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 03:42:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 03:42:43 GMT
ENV ROS1_DISTRO=noetic
# Sat, 16 Oct 2021 03:42:43 GMT
ENV ROS2_DISTRO=galactic
# Sat, 16 Oct 2021 03:43:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.13-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:43:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 03:43:21 GMT
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
	-	`sha256:4667bbaa58b18042bba7f627e73f63afc769ef1ba6dd8d02db26a97639896068`  
		Last Modified: Sat, 16 Oct 2021 03:51:07 GMT  
		Size: 103.6 MB (103626785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a680ad47ebc112dc93a40e8bd9e894aaf9519f94d0682ddd3fd48b7397cf56`  
		Last Modified: Sat, 16 Oct 2021 03:50:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99485d848bd2d8d3e44bc608ce7b5ded397a3875cd31a870b9204f6cf034156`  
		Last Modified: Sat, 16 Oct 2021 03:51:28 GMT  
		Size: 70.8 MB (70797181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0eba6427f6ee57b80c5edcf96532a72d18d44acf2723fcb86619039bbcfd4e`  
		Last Modified: Sat, 16 Oct 2021 03:51:18 GMT  
		Size: 250.9 KB (250902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec01b9342ad47c2d894dd5445179b44b59795f39844beddfe6e4ff69fcd8f8`  
		Last Modified: Sat, 16 Oct 2021 03:51:18 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60aa73989292d31559372cc09b8599aba98531656e025666399df977d646028b`  
		Last Modified: Sat, 16 Oct 2021 03:51:21 GMT  
		Size: 22.1 MB (22109577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6ab392dd7f78d2056a4c25f10f651ca439c1864d9cd6a1fbb27fc2935cb775`  
		Last Modified: Sat, 16 Oct 2021 03:51:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94ca8cbc799d108c3749d14472e55fd288c0e598eaa1b9edc53f0cf025cbac3`  
		Last Modified: Sat, 16 Oct 2021 03:51:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3af756f97cfe386dea5b1db3e1b5fe1f35ea544431b7291a007b670e582f862`  
		Last Modified: Sat, 16 Oct 2021 03:51:55 GMT  
		Size: 78.4 MB (78428180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe76e0e0d2ca464b408860b8e23a18a43452e301954cfe7bbc93d2c0a2278d1`  
		Last Modified: Sat, 16 Oct 2021 03:51:44 GMT  
		Size: 16.4 MB (16363582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb2b71889a46b806951a881fb9dd19ab87702574bab162ec2564946c94b4248`  
		Last Modified: Sat, 16 Oct 2021 03:51:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:611804205cea57f17c89440b48101650ce1d61515b496d43a3f28b9e4b5b4523
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314114501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7738fa2f2e57d4f0ea940e4301ac4ddc546c31a474be7d02185684e9919a4eb5`
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
# Sat, 16 Oct 2021 02:33:55 GMT
ENV ROS_DISTRO=galactic
# Sat, 16 Oct 2021 02:34:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:34:40 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 16 Oct 2021 02:34:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 16 Oct 2021 02:34:41 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:35:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:35:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 16 Oct 2021 02:35:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 16 Oct 2021 02:35:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 16 Oct 2021 02:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 16 Oct 2021 02:35:52 GMT
ENV ROS1_DISTRO=noetic
# Sat, 16 Oct 2021 02:35:54 GMT
ENV ROS2_DISTRO=galactic
# Sat, 16 Oct 2021 02:36:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.13-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:36:50 GMT
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
	-	`sha256:cc3549f1d260e60d8924c9b7e02611c65b2136c4991bbccee64e068f45993511`  
		Last Modified: Sat, 16 Oct 2021 02:50:49 GMT  
		Size: 100.0 MB (100010821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c03abd5daa700ddf866335aef47153c602aab661fc4e8a8cd6b920a3b78c6d9`  
		Last Modified: Sat, 16 Oct 2021 02:50:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bee7cb9969d594ee7bc764af007e4c0e9dbdd159efb7f78cd99599fe5d24227`  
		Last Modified: Sat, 16 Oct 2021 02:51:09 GMT  
		Size: 64.9 MB (64922456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d5fa4cfb7df399ade2516372c36c4997dd6b036fcf0fed2519961a0cc9cfca`  
		Last Modified: Sat, 16 Oct 2021 02:51:00 GMT  
		Size: 250.8 KB (250842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290e07cbc601974d308056bc5dd837d1e5cf3f31275052df2573bbe28b172562`  
		Last Modified: Sat, 16 Oct 2021 02:50:59 GMT  
		Size: 2.0 KB (1961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0000799c6000c28c01d2cfe4f94f943eea059b940290cb2bbeda007a003af9e`  
		Last Modified: Sat, 16 Oct 2021 02:51:02 GMT  
		Size: 21.4 MB (21426708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2851f2a6e5262082b1f79d371bd1027a38174d9acfc54c904de4322dd8a3a9`  
		Last Modified: Sat, 16 Oct 2021 02:51:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d940b7e8be291f71cd4fccbd8a9d1a3605e2afc316fe0b0a585842ddb079e93`  
		Last Modified: Sat, 16 Oct 2021 02:51:38 GMT  
		Size: 78.2 MB (78154188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fd20dbaace6c0249bf97438631a252e94c1375061c252235c665d890e6684c`  
		Last Modified: Sat, 16 Oct 2021 02:51:26 GMT  
		Size: 15.7 MB (15664601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5459c33b271053f26001f47c2a62cea83cea63737804c92278fb38390dbc233b`  
		Last Modified: Sat, 16 Oct 2021 02:51:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
