## `ros:eloquent-ros1-bridge-bionic`

```console
$ docker pull ros@sha256:05976dc1d58a201f1d4bc7eab95d090c96652b1850bbff2917c42ce9b4af7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros1-bridge-bionic` - linux; amd64

```console
$ docker pull ros@sha256:268b2f765a91aaba02ace6bbd0c253ce2be9bad9a0ebf885405a489e67deb2a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429289556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8300485aae7cc3e609d050dc1814f85da8bd627fe66e3e9a36484a5249d70ed9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:42:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:38:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:38:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 00:59:39 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jul 2020 00:59:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jul 2020 00:59:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jul 2020 01:05:15 GMT
ENV ROS_DISTRO=eloquent
# Tue, 07 Jul 2020 01:06:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:06:23 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jul 2020 01:06:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jul 2020 01:06:24 GMT
CMD ["bash"]
# Tue, 07 Jul 2020 01:06:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:07:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jul 2020 01:07:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jul 2020 01:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:07:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 01:07:20 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jul 2020 01:07:20 GMT
ENV ROS1_DISTRO=melodic
# Tue, 07 Jul 2020 01:07:20 GMT
ENV ROS2_DISTRO=eloquent
# Tue, 07 Jul 2020 01:08:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:08:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.2-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:08:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:08:34 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5a9a0d3edafb836db5fec8836034836fd3958d7f30865871a5e6bd21ea4f82`  
		Last Modified: Mon, 06 Jul 2020 23:59:55 GMT  
		Size: 837.6 KB (837576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ed212db9ead4a977f8bd6d2d39e7cd9419e44b909a063b5b687984ab277ff1`  
		Last Modified: Tue, 07 Jul 2020 01:18:26 GMT  
		Size: 4.9 MB (4867686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce51d2b74c6394890393140880b5297053345b1aa65996976782844361e29440`  
		Last Modified: Tue, 07 Jul 2020 01:18:25 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0339248bdb6a34fc05061e67c76e3eb5fed59a1df09268e704e59bdfb57208`  
		Last Modified: Tue, 07 Jul 2020 01:24:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb59529b620d343ab4db4c2b9ea14982a44f252752cac557eff8cac50b2ed6eb`  
		Last Modified: Tue, 07 Jul 2020 01:26:23 GMT  
		Size: 188.3 MB (188322042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc1fd2ceee6ee1a93471417f23c3cb9048a6cb882f5ef37a6ac067b062b21c4`  
		Last Modified: Tue, 07 Jul 2020 01:25:45 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645d143de9a1361505c35456bcc98ce5e4dc0dc879806d8f77c142580ef80c77`  
		Last Modified: Tue, 07 Jul 2020 01:26:40 GMT  
		Size: 63.5 MB (63504848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503e3a131385ebc66b1c4c96875188f16d6959a214f42e0b0e8b7f497942dd33`  
		Last Modified: Tue, 07 Jul 2020 01:26:29 GMT  
		Size: 182.9 KB (182853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a93dc6167c1a3a5304f68b12c971a6d825fc1360a07d68527e3a3be5642135`  
		Last Modified: Tue, 07 Jul 2020 01:26:29 GMT  
		Size: 2.0 KB (1972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18c4eeaf55e5574b7e247051497858df1c14aa49ebf13e505665f8d6a3c137`  
		Last Modified: Tue, 07 Jul 2020 01:26:30 GMT  
		Size: 4.6 MB (4580153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6432e9f57431ab905f0442fbab18a7311530321fc1132fc5e44dd98c9a93f5d`  
		Last Modified: Tue, 07 Jul 2020 01:26:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e251e4c9c1df3df77f5398235f5fb4ec8661a16990982a368d37ce5c90aeb`  
		Last Modified: Tue, 07 Jul 2020 01:26:45 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe2f9bd5afdfbc4f1c682b6283312f19a4ee08568bd5b4cf724d65ef6bf759`  
		Last Modified: Tue, 07 Jul 2020 01:27:13 GMT  
		Size: 117.7 MB (117669862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f59f5c1609a1e1a2426456e4be8df5c2c0d4d59be6cb3332c1af6f33c247fe3`  
		Last Modified: Tue, 07 Jul 2020 01:26:52 GMT  
		Size: 21.9 MB (21941584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d64103e170dcd15e3c9f7b77d02c9ced5aefc1acfc41d25053906d7e940bc67`  
		Last Modified: Tue, 07 Jul 2020 01:26:45 GMT  
		Size: 646.0 KB (645957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7f7a1b4aa7699f9ae8d964bf4bdd2e4c022dc3e505e8a6bc1fe85ee7efa889`  
		Last Modified: Tue, 07 Jul 2020 01:26:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:874f475cbbbe94fd7be2f76a53a061fe9d83da5b192082d8f879096e04464c45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359573562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca7570c6cbf482c7c9a9379a27d0cd3b0f3ebedce7655db71099f65bc19b1e2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:04:27 GMT
ADD file:934b4bc073556bbba45a5017b40df7ac076a57b031b6b7225919b1ea3c1d89ff in / 
# Fri, 24 Jul 2020 16:04:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:05:15 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:05:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:05:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:44:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:45:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:45:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 17:08:43 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 24 Jul 2020 17:08:44 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 17:08:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 17:17:35 GMT
ENV ROS_DISTRO=eloquent
# Fri, 24 Jul 2020 17:20:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:20:45 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 24 Jul 2020 17:20:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 17:20:56 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 17:22:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:23:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 17:23:30 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 Jul 2020 17:24:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:24:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 17:25:21 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 17:25:27 GMT
ENV ROS1_DISTRO=melodic
# Fri, 24 Jul 2020 17:25:32 GMT
ENV ROS2_DISTRO=eloquent
# Fri, 24 Jul 2020 17:28:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:28:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.2-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:29:43 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:de691405df56c17462a8052d9b88a283d955c448deda7a610d70096a5454ff13`  
		Last Modified: Mon, 13 Jul 2020 15:47:13 GMT  
		Size: 22.3 MB (22277635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a766b93ee2f7ed0525d6d90b71c5e860e5e54d4b5259de86c81e5c49ff120c`  
		Last Modified: Fri, 24 Jul 2020 16:13:28 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c97e104d7363348d21ddc11159cfa859c18d58712fcafc215fefb535baccbae`  
		Last Modified: Fri, 24 Jul 2020 16:13:28 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a97b3bf2bf845ce898abe48aed267cb2a554e220ee512500495c2791ea6ea8`  
		Last Modified: Fri, 24 Jul 2020 16:13:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40825ce490688cb6672f880a14c176e37993b3330e3da0bbbc85cdcfd2687dd1`  
		Last Modified: Fri, 24 Jul 2020 17:34:47 GMT  
		Size: 838.2 KB (838232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf54bc0901cce7c75270c8e95f9b1cdbb43e53d4276bb5af25d5c111e999ae07`  
		Last Modified: Fri, 24 Jul 2020 17:34:48 GMT  
		Size: 4.1 MB (4083613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cad6cc18429d2d3be719a3839da31b4664c588181a8bc873d7a2b095f710db`  
		Last Modified: Fri, 24 Jul 2020 17:34:45 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80c9de188c1e86fb75bac63f08f9fd6abf595c997d5ccea87a01a98d759336`  
		Last Modified: Fri, 24 Jul 2020 17:44:07 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9aa9476fb8bb66ddb506f4bfeb2d8475cde5fdc6f847bbd9ac9ab53f225075`  
		Last Modified: Fri, 24 Jul 2020 17:47:08 GMT  
		Size: 156.6 MB (156555936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c529ef5a697f8a24b31161a32ee0277b952a4b8c6af481c488f4eb39c5aa1061`  
		Last Modified: Fri, 24 Jul 2020 17:46:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53ee59574b00aa2a6b08b1ec76d154634664c26cc709ab42873e38089ca40d2`  
		Last Modified: Fri, 24 Jul 2020 17:47:36 GMT  
		Size: 47.9 MB (47906008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7433e640cec505de9adeabfec5c77a60dabb112be091ca20eb8e04be3042ca7f`  
		Last Modified: Fri, 24 Jul 2020 17:47:18 GMT  
		Size: 184.3 KB (184260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8bbc00fb5a703b481915da030ac0ac900a57e08c35bdf8262deae802a6335`  
		Last Modified: Fri, 24 Jul 2020 17:47:18 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6856f9e77a4a117a8fb90e58b6d703127ded5e3c642b797ffe6d97d3fb7ad50`  
		Last Modified: Fri, 24 Jul 2020 17:47:24 GMT  
		Size: 3.5 MB (3491882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffed07a191aed968cdb49b1bbdcfce78df43ba4ee4e5baf86978c2db87bb93b`  
		Last Modified: Fri, 24 Jul 2020 17:47:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09de9ca9b775468112056dc34e619d16a261fb2d3f3bd186c5e2418fbe6a32f`  
		Last Modified: Fri, 24 Jul 2020 17:47:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023af2a54a6bd1e4d6e02b445441a53d5f18079f814313f54bc499542df3e073`  
		Last Modified: Fri, 24 Jul 2020 17:48:26 GMT  
		Size: 110.5 MB (110519793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def1507b2e0c0950f8b89048a4dddaab37942ef08076998b2960241af5296352`  
		Last Modified: Fri, 24 Jul 2020 17:47:52 GMT  
		Size: 13.0 MB (13033052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c82f14f837602628ebcc3a0b76dc782fcc3d23866d06d50cfe26cd378de0ab0`  
		Last Modified: Fri, 24 Jul 2020 17:47:46 GMT  
		Size: 642.1 KB (642137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4466f208bb35ec450de35911be7834dbc2f46d09e94d6026e2302579c9456bd`  
		Last Modified: Fri, 24 Jul 2020 17:47:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:46ddfbe5a388c2a75ebd1b62270dbe8427e78224e9535a233b0bf89912359562
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391869101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7da4c275d5cc2361662011dff60778c813c7b44d206a165d9dcaba50aaaaad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:46:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:46:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:46:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 17:08:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 24 Jul 2020 17:08:26 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 17:08:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 17:16:00 GMT
ENV ROS_DISTRO=eloquent
# Fri, 24 Jul 2020 17:18:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:18:16 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 24 Jul 2020 17:18:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 17:18:18 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 17:19:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:19:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 17:19:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 Jul 2020 17:20:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:20:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 17:20:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 17:20:31 GMT
ENV ROS1_DISTRO=melodic
# Fri, 24 Jul 2020 17:20:33 GMT
ENV ROS2_DISTRO=eloquent
# Fri, 24 Jul 2020 17:22:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:23:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.2-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:23:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:23:44 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4768214edda94a7e9ba7ecb85272a0734e1ba302cbcacfc96cc61272ba1d0384`  
		Last Modified: Fri, 24 Jul 2020 17:43:50 GMT  
		Size: 838.1 KB (838078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d3d1819002b1349227a7ccd903ed09cc281fc5e00b1423e9743c364d72c92f`  
		Last Modified: Fri, 24 Jul 2020 17:43:50 GMT  
		Size: 4.5 MB (4451253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b983b780e9abf5b012f43ff113f18df26eb2f5cec23f65c85822562133ebfc5d`  
		Last Modified: Fri, 24 Jul 2020 17:43:45 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c828b5b5cc5a807aa32e5760404252e47b74bd5f0e5be84db84775507495964`  
		Last Modified: Fri, 24 Jul 2020 17:54:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8595cf4ab85d2b44fead192e00cbde44010891e66f36cc5a5b3b5b759c82073`  
		Last Modified: Fri, 24 Jul 2020 17:59:50 GMT  
		Size: 168.3 MB (168343639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510a538572a0d1ddde5ab11952be848e541053500f7d6133d6047d8fe17bbc1e`  
		Last Modified: Fri, 24 Jul 2020 17:58:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e04616e9d84cb877ab39fa2aab5240d8ad90218dbfbbf144623d3ba3efbf1af`  
		Last Modified: Fri, 24 Jul 2020 18:00:17 GMT  
		Size: 56.2 MB (56214278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15116d17cf9528904e125a2ec866c3ad8505df296f0c154ec55b91f0db0fa820`  
		Last Modified: Fri, 24 Jul 2020 18:00:00 GMT  
		Size: 184.3 KB (184256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d0efd7fbda58f0422ab0433e188f4d5bb8007ee8a029d31d5701324911189e`  
		Last Modified: Fri, 24 Jul 2020 18:00:00 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa568793eb2b5c31a7fb341f4a2eadb63a95ceb3ed7ecf70bd91de63343bcd3d`  
		Last Modified: Fri, 24 Jul 2020 18:00:04 GMT  
		Size: 3.9 MB (3931205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dfc2ca0056191adabdab2c582e4803ec569c32bb2bcf2151f63d94b1c1c9a0`  
		Last Modified: Fri, 24 Jul 2020 18:00:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee14173c9ae437bc6441b365ab5888b40da5d7a64310c834991e6b0e05925cda`  
		Last Modified: Fri, 24 Jul 2020 18:00:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93663aa06b2b9bf6f2db970797dc558bb2db899e6b93ff0a6f742ed10b4417b1`  
		Last Modified: Fri, 24 Jul 2020 18:01:56 GMT  
		Size: 116.6 MB (116610861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4511f6ddbaed441ce8d5db7e986f087d80bdd2543403d3c81831c6edd2e531`  
		Last Modified: Fri, 24 Jul 2020 18:00:38 GMT  
		Size: 16.9 MB (16889577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fd006a32e2247cfd0d00015ab712a9a6bb35925730a21e30791d34cc84fa0f`  
		Last Modified: Fri, 24 Jul 2020 18:00:26 GMT  
		Size: 644.1 KB (644067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b514a131a612b1ca9a9b55c28d2c1cc96a8d605abadb77c6db3a8b41bd7be7`  
		Last Modified: Fri, 24 Jul 2020 18:00:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
