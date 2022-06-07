## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:dfcdbfc5622005e48a57a28c840bd8256695f9c52aad78e6906d3049044fd292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:845fc60bb1307a03bf649f02283e0cfe1304fbf4823b8541fb1a0060c543b43f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348478447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665532b112476db2c919c9d6ea566b426ee92be833f5eb901fff3e427584f343`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:10:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:11:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:22:52 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 01:22:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:22:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 01:22:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 01:22:53 GMT
ENV ROS_DISTRO=foxy
# Tue, 07 Jun 2022 01:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:23:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 01:23:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 01:23:54 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:24:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:24:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 01:24:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 01:24:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:24:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 01:25:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:25:00 GMT
ENV ROS1_DISTRO=noetic
# Tue, 07 Jun 2022 01:25:00 GMT
ENV ROS2_DISTRO=foxy
# Tue, 07 Jun 2022 01:25:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:25:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:25:38 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1e38681d9b6d153af3be7e0550217dc0dfb994512346ebc7d9a7a602651e74`  
		Last Modified: Tue, 07 Jun 2022 01:47:20 GMT  
		Size: 1.2 MB (1181179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a44b59555aadd115e37e45f079fef0ca694c5888fcd16350e10a693138a6db4`  
		Last Modified: Tue, 07 Jun 2022 01:47:19 GMT  
		Size: 5.5 MB (5547097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f29772f338ee6a1336a8cfeab6d4550be032d0e9cea76c782ba25f708e14a6`  
		Last Modified: Tue, 07 Jun 2022 01:50:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b699c33a19954e95275906408065472c7989f2a8bc685a5c9ffc5f7a70446e7`  
		Last Modified: Tue, 07 Jun 2022 01:50:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb42810f84e69169e13f4ba7e14a1a7fa6d81dba996d2b091493577783be695e`  
		Last Modified: Tue, 07 Jun 2022 01:50:21 GMT  
		Size: 120.1 MB (120077388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f92457a493c04a77f0ac61cd065d158768a70191e86bf92fc446076123f8e7`  
		Last Modified: Tue, 07 Jun 2022 01:50:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476e616a90701bee44fbc310458b18ce75a4bdfe5680a22b27dba9a84bf0ef1c`  
		Last Modified: Tue, 07 Jun 2022 01:50:41 GMT  
		Size: 73.3 MB (73321142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa71ae8a0c62c2ef33328de080cdabeefda3946cc96f59ccad1ecba1796a9209`  
		Last Modified: Tue, 07 Jun 2022 01:50:31 GMT  
		Size: 257.1 KB (257124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9ad82940247dc7731be3759d12e58bd52af7b3b53b4731f2d88990db31c281`  
		Last Modified: Tue, 07 Jun 2022 01:50:31 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0def727ac7744929624ad45072377c38e2b427e4acda1e1c0b108c45e6cae0f`  
		Last Modified: Tue, 07 Jun 2022 01:50:35 GMT  
		Size: 21.7 MB (21663791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3d2bc7757d3d9d4bb3b8f6a36ae62da3d95745ee4f11a56e38fdf554486938`  
		Last Modified: Tue, 07 Jun 2022 01:50:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ebc1131df0b50eabcf4d4c6f3247f87ddbbffc13edbfa443427e13add36ad4`  
		Last Modified: Tue, 07 Jun 2022 01:50:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12074399c950505a578a1947414ca27201fa77d5d64a7acd791e9a54957a4f68`  
		Last Modified: Tue, 07 Jun 2022 01:51:10 GMT  
		Size: 76.3 MB (76316167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed4199ae2cdec8ea37d6ec3ae7cdeab825069a3f7d924bb5cbea0c4a5dc8f65`  
		Last Modified: Tue, 07 Jun 2022 01:51:00 GMT  
		Size: 21.5 MB (21536602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4fe45deb83c6b2ef4410607491f98ec61e82e32dde9b31b45a8868a4fc9248`  
		Last Modified: Tue, 07 Jun 2022 01:50:55 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9fa283c8598fc76684226b6f65b836c00b9d130696533bf623845110a5b71027
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316167892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baa20aae39af9039e05f17398914fe7dfa6e7c6d4496da5a250957c69e6c245`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 05:53:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:53:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:58:09 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 05:58:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 05:58:12 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 05:58:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 05:58:14 GMT
ENV ROS_DISTRO=foxy
# Tue, 07 Jun 2022 05:59:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:59:11 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 05:59:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 05:59:13 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 05:59:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:59:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 05:59:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 06:00:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:00:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 06:00:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 06:00:28 GMT
ENV ROS1_DISTRO=noetic
# Tue, 07 Jun 2022 06:00:30 GMT
ENV ROS2_DISTRO=foxy
# Tue, 07 Jun 2022 06:01:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:01:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:01:14 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260269f7c7c500761ab4d24037f4187c4da07bfe2287a50d134b0421fad862ac`  
		Last Modified: Tue, 07 Jun 2022 06:18:02 GMT  
		Size: 1.2 MB (1182691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3124e11618c0a455d11e98a3c2abad2b0dfa785eb7e7e709b4e9880836df1802`  
		Last Modified: Tue, 07 Jun 2022 06:18:00 GMT  
		Size: 5.3 MB (5322854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ba1af7accc591a88c8a5f7fcf1bf476eff87854e2eac51402705fb2a99e6d`  
		Last Modified: Tue, 07 Jun 2022 06:20:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de599d7de9bc16e737c7d0bfa8e04fbc3af9a6e8c01427667056cf9b535382b`  
		Last Modified: Tue, 07 Jun 2022 06:20:40 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98cdbf24e724491ae84bce273d36577ddf420bcbb4080a8280e8fa98fdede28b`  
		Last Modified: Tue, 07 Jun 2022 06:20:58 GMT  
		Size: 104.3 MB (104273904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c3959e0f6ed1971e7ada61486d677ef1ae06a0844bb1f91bc5cace3e398a9a`  
		Last Modified: Tue, 07 Jun 2022 06:20:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da51ac80ef0bd3a07b16018b52a649d62ec03591a4ca2deb530380c0330f0a44`  
		Last Modified: Tue, 07 Jun 2022 06:21:19 GMT  
		Size: 67.5 MB (67454614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039855e65a5d9a35f11df9edc8607488801249ef521c9a8cb8e9e3be8e492e25`  
		Last Modified: Tue, 07 Jun 2022 06:21:10 GMT  
		Size: 257.1 KB (257142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaf578d4ad8db14ff5e85735f040f6db5169e03eae2d6898571946a73e1078a`  
		Last Modified: Tue, 07 Jun 2022 06:21:09 GMT  
		Size: 2.2 KB (2200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce23c0b6803030685f8d276f2f65beef17c9e37a95ce4f0304ca579a92f8901`  
		Last Modified: Tue, 07 Jun 2022 06:21:12 GMT  
		Size: 20.4 MB (20366539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3217c1f4b754041ab2f4260ac2ddf77be53a7318d99d8539e26d73b86a872f`  
		Last Modified: Tue, 07 Jun 2022 06:21:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774b3b3a7dd0b783eab2421ff96b00d4bf25eb41057a27a39f1f4a90174f1fbc`  
		Last Modified: Tue, 07 Jun 2022 06:21:49 GMT  
		Size: 76.2 MB (76156799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b38386e8040edbd93e865cbc03188975712bce21f1fb727cc3ecd02f255bf3`  
		Last Modified: Tue, 07 Jun 2022 06:21:37 GMT  
		Size: 14.0 MB (13957100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d63e2111fa8780ea446d84d204450a96516d1d076b93e8a4b0a48684463fe1a`  
		Last Modified: Tue, 07 Jun 2022 06:21:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
