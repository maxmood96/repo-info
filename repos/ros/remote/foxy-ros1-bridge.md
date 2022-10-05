## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:563cc611256b5618ed965af84b42b95da28ea8de2c7105ee1f418161dc1313b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:916ccdc4fb015c163586431e403398e9bbfc9f2826111e325cd004ada298fcb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349058814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c142f83d4bb74d1974a95aed03499ef4f432ebe1986c774237a7dd27127d3483`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:02:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:02:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:22:08 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 10:22:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 10:22:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 10:22:10 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 10:22:10 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 10:24:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:24:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 10:24:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 10:24:05 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:24:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:25:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 10:25:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 10:25:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:25:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 10:25:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 10:25:56 GMT
ENV ROS1_DISTRO=noetic
# Wed, 05 Oct 2022 10:25:56 GMT
ENV ROS2_DISTRO=foxy
# Wed, 05 Oct 2022 10:27:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:27:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:27:18 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db398de1191a2231a78b6d5d54baa0f980aa763df67adb3394a7269111109671`  
		Last Modified: Wed, 05 Oct 2022 10:50:03 GMT  
		Size: 1.2 MB (1163849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d2c75c8d50e5aa3470df0fc55d0148e41867398126d721472b626f05229661`  
		Last Modified: Wed, 05 Oct 2022 10:50:01 GMT  
		Size: 5.5 MB (5546788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62dae53f0e9e7911f61e2af662dfc6c10a32cd5717c41369e1316e320c64345`  
		Last Modified: Wed, 05 Oct 2022 10:55:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01c1f05f8d44c933ce4daf7979f608925683f5ab3dd0b86b37b69af0df974d2`  
		Last Modified: Wed, 05 Oct 2022 10:55:12 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f51876d6577a35c5e59f0be2aaf21be35ae0ccc2ae98272ff4fdc2a4710942e`  
		Last Modified: Wed, 05 Oct 2022 10:55:32 GMT  
		Size: 120.4 MB (120413613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f290f8a7da3fe7da67791a679b225fdfbea4a063f69014d0cc798b572a00606`  
		Last Modified: Wed, 05 Oct 2022 10:55:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bed5d7de950633b22457faefa5a82b47b766d96c02665e4faf86d9b7ebe9703`  
		Last Modified: Wed, 05 Oct 2022 10:55:53 GMT  
		Size: 73.3 MB (73322093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e37e53cfffae15445cfdce1b4b7ef7cea4b3e153ea7abf8cd18ebf02b77e34`  
		Last Modified: Wed, 05 Oct 2022 10:55:42 GMT  
		Size: 267.4 KB (267375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677b37769ea581ebd1d2e907d8c68c8a2c4f7920ce4e81e0099e4165a54aca77`  
		Last Modified: Wed, 05 Oct 2022 10:55:42 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216bc94919c7136aa052456840629454991399309eea61f5b2f7b34471de467c`  
		Last Modified: Wed, 05 Oct 2022 10:55:45 GMT  
		Size: 21.7 MB (21663849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d94baadca69524a33d3ca807ea019bbad1438b2b7217b4e86ba0e93367003`  
		Last Modified: Wed, 05 Oct 2022 10:56:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccc523540c72f37ce74bb0e501bd649759b2c7dfcb655447fac8913c1517dee`  
		Last Modified: Wed, 05 Oct 2022 10:56:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30e1cb5bcf08c41cd9a4d2e6fe7eaf091057e629ff6f04e3d14c40db29b0048`  
		Last Modified: Wed, 05 Oct 2022 10:56:20 GMT  
		Size: 76.4 MB (76429483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb854b70cf802670e97b4d6ccb7d054bba536f3eb14a57315543c577468c56e`  
		Last Modified: Wed, 05 Oct 2022 10:56:10 GMT  
		Size: 21.7 MB (21671851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dda7b30665fed39bcf488e91c73c1165eea1cd815014048c13330d18959877`  
		Last Modified: Wed, 05 Oct 2022 10:56:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9ff7fc96b5af30a5599b70993ddb7041334f53323b4ca7640b57ff9e1e68c4a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.8 MB (316765174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbacdad4c164be3b4c8a143c155c989069e4828ffb5b6bde2b18b7349c7c079b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:48:55 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 13:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:49:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:49:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:50:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:50:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:50:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:50:57 GMT
ENV ROS1_DISTRO=noetic
# Wed, 05 Oct 2022 13:50:59 GMT
ENV ROS2_DISTRO=foxy
# Wed, 05 Oct 2022 13:51:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:51:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:51:45 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c65c3947a6f0c271454a1a4196e78bc089909ef0635e4fb722f0d26058386`  
		Last Modified: Wed, 05 Oct 2022 14:14:18 GMT  
		Size: 104.6 MB (104627758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d57dc14ffab1724d55720e415410361be4700ed6ecc13df5afc8d58b22afd`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b933fcbe46312ae813f092369a156c253b1e52cb3a43298b9a4fdbee1eb6fa6b`  
		Last Modified: Wed, 05 Oct 2022 14:14:40 GMT  
		Size: 67.4 MB (67449275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d7c2e640d21fee0497f12b54a0f888d39799eb93389888e1da33e797737919`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 267.3 KB (267323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2d4224582edb4e076612a46599ad24ba3ccfc164b2d512b2006c21094a621`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d9c31822b3bf7270af1ce9bc509a7516e60401dcfc80333756e3f62d45364`  
		Last Modified: Wed, 05 Oct 2022 14:14:33 GMT  
		Size: 20.4 MB (20366915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f2c8f261aabc480326a91bee38a862a180cfdd89bb015b9d655b99993403e`  
		Last Modified: Wed, 05 Oct 2022 14:14:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3614d3bded093673281f432c55f0f746dbe555a0849f2c657164b0dd0a2725`  
		Last Modified: Wed, 05 Oct 2022 14:15:10 GMT  
		Size: 76.3 MB (76271820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301707bbed02236a81c065964e76a9676c5058644e3974e8e8970beeb8e4d4f0`  
		Last Modified: Wed, 05 Oct 2022 14:14:58 GMT  
		Size: 14.1 MB (14098760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769ba38f03d3d37fa954731a02f330fbfd4cf12cbd6179196026f9909fe85cc`  
		Last Modified: Wed, 05 Oct 2022 14:14:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
