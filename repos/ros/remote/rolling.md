## `ros:rolling`

```console
$ docker pull ros@sha256:6eebba1d7d8127f90cd790964c23521597aba363fa60ec1a387895b1274c8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:da1a2d2e9e41bd9c29cb3c99a8cb4b45f8d8c87fbab20c8f3399819bebb74de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262719439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436e82c5b0bca3bd441eaded5e62eefc4c3b7bfa6903d1a814e70b9192e560ee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:28:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:28:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:28:35 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 01:28:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 01:28:36 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 01:28:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 01:40:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Jun 2022 01:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:41:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 01:41:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 01:41:09 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:41:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:41:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 01:41:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 01:42:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d1d4bf62a3722d7122bc1b8ee8ad3051fcaf598ca72ad725fea76cb53f6b3c`  
		Last Modified: Tue, 07 Jun 2022 01:52:41 GMT  
		Size: 1.2 MB (1191642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5c906965a7cb2488a6e23da68abe175ee9acffbe27e61b1152cfff4fbf840b`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 3.8 MB (3827182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1af53ce2d5965bf4c8489cf5459894d2e6c3f6b00538c076d38e41668d6cf`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8d3945eb76a1a2076630ee2752a89342d614a9298134e198075975ec08400d`  
		Last Modified: Tue, 07 Jun 2022 01:52:38 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9c71936f086360e13475372b678edf9e90dda0249fc0cb007070b136f0b431`  
		Last Modified: Tue, 07 Jun 2022 01:55:42 GMT  
		Size: 106.1 MB (106131399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba72d83ed0d2e6bbd2f45b43761d9699bdc1bdeecc565de30d7c4c75696f0b5`  
		Last Modified: Tue, 07 Jun 2022 01:55:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e141275ac844961d5e6aae4adaff24bbc71e569676a50e4ceb83aac78b808c03`  
		Last Modified: Tue, 07 Jun 2022 01:56:14 GMT  
		Size: 97.8 MB (97838742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecab1f16ec251a3dfbd7c86db15d68f7937ac612f6b6342c89b6f7272eeb318`  
		Last Modified: Tue, 07 Jun 2022 01:56:00 GMT  
		Size: 273.2 KB (273161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e01aa968f971f9b30c74f1b45be67addb7b3ac071b1d2879a5f99184f6bd40c`  
		Last Modified: Tue, 07 Jun 2022 01:56:00 GMT  
		Size: 2.3 KB (2272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cf2ef0c2f0d6cdbddea8135625ff2a75b8f0358d46a81e65d0e8622c5bf671`  
		Last Modified: Tue, 07 Jun 2022 01:56:04 GMT  
		Size: 23.0 MB (23028911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:41b8bc478d097ea077e2d01bf81624f9836ad30ba3ae9a2bef03c148369a1038
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254977578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8807bdd5c76dea927a5e6a26a7ad603b8cc5fac7625f14815dfda17213ce482b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:32 GMT
ADD file:20805b983efd5443e34ebdfb7795010e5684eb1ca1ffea30a3e61e0089c0eee8 in / 
# Tue, 07 Jun 2022 01:25:32 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:04:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:04:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:04:56 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jun 2022 06:04:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 06:04:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 06:05:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 06:09:33 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Jun 2022 06:10:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:10:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jun 2022 06:10:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 06:10:22 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 06:10:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 06:11:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 06:11:05 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jun 2022 06:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ed02c6ade914c2962413c1ad2ccc86ed8d1512098f2c87fe7bafa8e1b5293185`  
		Last Modified: Thu, 02 Jun 2022 08:38:25 GMT  
		Size: 28.4 MB (28378212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b38f97e6001c6a08e3dc9944afe7213ac786bed47db29ee11755c6040f4eb0`  
		Last Modified: Tue, 07 Jun 2022 06:23:22 GMT  
		Size: 1.2 MB (1193148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e937b319a974108dac2f8e36b8f73cd96710ce7663bdf1f72284fccd43df6abe`  
		Last Modified: Tue, 07 Jun 2022 06:23:20 GMT  
		Size: 3.6 MB (3595011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1effce9a47b0ec30acadccc8c075e64e320b43af40a3600dbac215a9d94b87`  
		Last Modified: Tue, 07 Jun 2022 06:23:19 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3da9dba47edebe9f3610145826c05ead7b35e702981de104853623ccc5208fd`  
		Last Modified: Tue, 07 Jun 2022 06:23:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afae557291fb262be019f4a220aeb20ea7c6b1474c968d4bb9d8ba63e5295e39`  
		Last Modified: Tue, 07 Jun 2022 06:26:21 GMT  
		Size: 103.9 MB (103865174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aab77c96357ad802c699db548bd10726e6a4ac599df8ef215e6ddfe925444b`  
		Last Modified: Tue, 07 Jun 2022 06:26:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9904a4fe7a75f1eed88c54411c41df21cea85b5e1eee36bfc1426a6c355b152`  
		Last Modified: Tue, 07 Jun 2022 06:26:45 GMT  
		Size: 95.2 MB (95223816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d35cdddc2acfbc5c458c06a2df30fb69d28a1fe576252273c8f5d734335eb83`  
		Last Modified: Tue, 07 Jun 2022 06:26:32 GMT  
		Size: 273.1 KB (273097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6c7be9982d5ae74dffb3e90ca2f2b866364281b12e84fd5373efc8e07565cd`  
		Last Modified: Tue, 07 Jun 2022 06:26:31 GMT  
		Size: 2.2 KB (2191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d873c09a237a9c1df0a3031bef8211427e58da4c8fb2f6a0a5b06b8d9f27353`  
		Last Modified: Tue, 07 Jun 2022 06:26:35 GMT  
		Size: 22.4 MB (22444556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
