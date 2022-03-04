## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:ef6398326083a99a10cfc1fd673822b90c94709f289a8a55d62870ae7703a9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:6a82ef6c322c9dcc744e97cb4d9963082d628b814f2c661b32acbbec17df4513
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346058199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9837fbe5b59081660925be593be0641db31c4d810097d704e6749878165e3`
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
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:09:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:09:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 23:10:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:10:23 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 23:10:23 GMT
ENV ROS2_DISTRO=foxy
# Thu, 03 Mar 2022 23:10:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:57 GMT
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
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbad41d04cdd4ef0ac30989e309c7b3c6e2195487617f6de0de31531e94f0e0`  
		Last Modified: Thu, 03 Mar 2022 23:26:26 GMT  
		Size: 70.9 MB (70858279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2334a170618fa03d191f1cd8e76fc82332385dc22bf836010ede2a8d3f3a8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 251.4 KB (251411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19351c10f0dc4c8c58bf2b0c669363804f1d9b92749d5edb3877509307285bc8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5cea3cbaf19126de5c75f225a7b897c0dc23588d0f04f627c7f54b8b6ccd16`  
		Last Modified: Thu, 03 Mar 2022 23:26:19 GMT  
		Size: 21.7 MB (21668565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da4735eb0f83b7e7035ec5c2b795a45802eaa037f0396d7ce85bed3d974b46`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eac423a1ad520cfeaee1eb128a6c76cf8c96a5da4e2d639a1dae97441e8e5e4`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b15f5a81eed01b7221df719b0ae09c496f479919878cf653779190b846afce`  
		Last Modified: Thu, 03 Mar 2022 23:27:02 GMT  
		Size: 76.3 MB (76324495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d28e7e3b67e20f4905961c74a0a7bf08e737ccb31981aa0743a0ed3096473bd`  
		Last Modified: Thu, 03 Mar 2022 23:26:48 GMT  
		Size: 21.5 MB (21544127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec25e5b6d44635614eec05ea663ac517157327ef1e48387d7d8a7f67c18fc99b`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75a13f909d02eb9b215c141c79353f7a4477b2f8e2656e61060cfa7ce2a178d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313685609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb658bf3078b2e64b9bbe724ec4d13a6a339e94d93efc8794e4f3ede1ee9455e`
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
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:28:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:28:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:29:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:29:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:29:32 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 21:29:33 GMT
ENV ROS2_DISTRO=foxy
# Thu, 03 Mar 2022 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:30:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:30:33 GMT
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
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa316f1e52a8742158d7e022dfed33680c4467154b94a6516bd8eff84dabce86`  
		Last Modified: Thu, 03 Mar 2022 21:44:45 GMT  
		Size: 65.0 MB (64978916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259c8d5169fc4cfec7b5c89bec35869a21563e7fd7a75dafe4bf7d62a2a0276b`  
		Last Modified: Thu, 03 Mar 2022 21:44:35 GMT  
		Size: 251.4 KB (251357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77fb0b75c8c330b2dfb7c0039de9cc5b918cd16d1fb5dfe5ffcfa2d946d6cd`  
		Last Modified: Thu, 03 Mar 2022 21:44:36 GMT  
		Size: 2.2 KB (2157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d067c6b6ac7d13b7c8d6074e843f1bc10d0b956e77e1088ce78fdd2a237b380`  
		Last Modified: Thu, 03 Mar 2022 21:44:38 GMT  
		Size: 20.4 MB (20373551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c049479168ee5d90c70a2c94ba07d775e84624893e0891e3512c8746d3962f`  
		Last Modified: Thu, 03 Mar 2022 21:45:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276caa0dbe0e51c985df9653b22670ddd523c804857e5be2b479b21cb1edfb97`  
		Last Modified: Thu, 03 Mar 2022 21:45:18 GMT  
		Size: 76.2 MB (76154541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de33646892d7a0d39f2850d920d648c8c345dd4bca7c96cceef7ce88a9a56e8`  
		Last Modified: Thu, 03 Mar 2022 21:45:06 GMT  
		Size: 14.0 MB (13964844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ace697c4b9d045e3b333b61bbf06cc7a5985b40576f92dfe88e2b91b225738`  
		Last Modified: Thu, 03 Mar 2022 21:45:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
