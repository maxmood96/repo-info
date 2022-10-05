## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:671ab05ffcef6bec1b17f2d72ceaf8691d1ec540853afc7d4c2ddd3d4a6a76bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:31e95499a197997474216a4cb9ece22ea610e5b8432d33b081f8a56cdf09b51d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234948199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34842cadd0ae6b77ece4f5f2d3460b0be17b6dd7fae9bada523c9f441d84ecb9`
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
# Wed, 05 Oct 2022 10:27:33 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 10:28:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:28:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 10:28:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 10:28:18 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 10:28:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 10:28:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 10:28:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 10:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:20f09aca0821084fd31221ce78f055e457cb666af60a41c8c19af97408974840`  
		Last Modified: Wed, 05 Oct 2022 10:56:47 GMT  
		Size: 104.0 MB (103964019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962252ee5d05117da8058bde3a9410684e471a0d7e8bbe43d008a1be9c3a8590`  
		Last Modified: Wed, 05 Oct 2022 10:56:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2325e55da12fa5a2fe5cc77f5f4c49fd8c54a8b75b1371f5a3ad006d8da4cd99`  
		Last Modified: Wed, 05 Oct 2022 10:57:07 GMT  
		Size: 73.3 MB (73278776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7c9f33f63d472a14808c264f99830797a829ade91081d5538b5f038d545818`  
		Last Modified: Wed, 05 Oct 2022 10:56:57 GMT  
		Size: 277.8 KB (277810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0f0a76d4c60c66ee530a65c3a89f82c1474b1d942484e6254626fb32b7a38c`  
		Last Modified: Wed, 05 Oct 2022 10:56:56 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be9160af9b9ec898e502540ef556ed949674959b38ee20cf5532793f4150c91`  
		Last Modified: Wed, 05 Oct 2022 10:57:00 GMT  
		Size: 22.1 MB (22137635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9823d71d84a6facb9ad6ab94361c78eaafb082eedee10eb50d0fcf03e3196e40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223197069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a96e112da177db105e7ab8a4629e2f05d7ebf4a0f23fba4094e15b8f76174cb`
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
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:53:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a956f99c4721f7dc25bfe3b1c9c90ce2a2d8b0474b19e342030574fa077dbc98`  
		Last Modified: Wed, 05 Oct 2022 14:15:59 GMT  
		Size: 67.4 MB (67402819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231122a3faa9e29e7dcfbc07429b9a375bde70cf77017ed38de61d4a42bb924`  
		Last Modified: Wed, 05 Oct 2022 14:15:50 GMT  
		Size: 277.8 KB (277756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5317376816f40e243dc89e1427d6106c53bd777b2ad592afdce65fa1301cdce8`  
		Last Modified: Wed, 05 Oct 2022 14:15:49 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a90f00672da01678118f187b2830f6621555d9e05eddf1d8c10a2d25f967f2`  
		Last Modified: Wed, 05 Oct 2022 14:15:53 GMT  
		Size: 21.5 MB (21458239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
