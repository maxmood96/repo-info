## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:23ccc9dbba22bb04efb39700e30838e421e3078a4c8020fd6a8c3a3258755585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:47bbdada6ec4dbc2f19ed702bcbd8916a26f8964a2c25790dd65668cfb939d27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155701113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7ee85a49e46466a088fa050f4373b9accb131b1b137c3650e9919ecd67d036`
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

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:52ee321733098fccaaf6a0618e45b7dc52f08ce058fb8349984592e05de6bf38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138308211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9bc639ef7ce7d698d0dce478a9a4828085c53c24246570ed03bd3b8871dc0b`
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
