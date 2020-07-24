## `ros:dashing-ros1-bridge`

```console
$ docker pull ros@sha256:6426587e8423a844d9007118d67539749e5710cc44cf7c5cee7cff17c3f2624b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:c73614bc42a1dfdb4ff09f37232d40a1c1e5bb6683a718374a151353aba55b36
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.1 MB (424061444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051e29129134dee1b904563049fda26a77b490c31c69f0100aea3774ca805ba0`
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
# Tue, 07 Jul 2020 00:59:40 GMT
ENV ROS_DISTRO=dashing
# Fri, 24 Jul 2020 14:25:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:25:07 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 24 Jul 2020 14:25:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 14:25:07 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 14:25:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:26:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 14:26:05 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 Jul 2020 14:26:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:26:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 14:26:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 14:26:19 GMT
ENV ROS1_DISTRO=melodic
# Fri, 24 Jul 2020 14:26:19 GMT
ENV ROS2_DISTRO=dashing
# Fri, 24 Jul 2020 14:28:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:28:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:28:28 GMT
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
	-	`sha256:673ab5e2a78a911067f6f2eda73924bffb21e61f08d5aaaeb77326f22680e3d2`  
		Last Modified: Fri, 24 Jul 2020 14:35:33 GMT  
		Size: 184.8 MB (184751205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2236cb12f17beb5fd7d677533a8235cc8ddef5b6582b60c732b3b9f223395e34`  
		Last Modified: Fri, 24 Jul 2020 14:34:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0163648c545996d85101d8841e9f24cf5944f3838387be2a3253db10fcfa6662`  
		Last Modified: Fri, 24 Jul 2020 14:35:48 GMT  
		Size: 64.1 MB (64123085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9769264e3792c16cc8957d890d3b9daea0e988df9170df9e6427517f7edb1528`  
		Last Modified: Fri, 24 Jul 2020 14:35:36 GMT  
		Size: 185.5 KB (185503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e913ba01baee0a734758fb9279c77ef1f9d5bf8e9fcdd5a725a5e04e5eadfdaa`  
		Last Modified: Fri, 24 Jul 2020 14:35:36 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf3c11b8f4b4d8317019346731baba08195bd1bd8db4caab117b76b34644f7b`  
		Last Modified: Fri, 24 Jul 2020 14:35:38 GMT  
		Size: 4.3 MB (4312193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0264ac6d5e79936a3e17ae9a551e4ae09b7c262e8133c44b3e494e3cfa7320c6`  
		Last Modified: Fri, 24 Jul 2020 14:35:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53516710b0b6d7b88f6e3c809d16ff50aa4b94692dab8bc8d2a39a245f72971b`  
		Last Modified: Fri, 24 Jul 2020 14:35:52 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088eb1d7bf85e9c6ac7c670c0156b098350ccb217745cae705cf6073f558c639`  
		Last Modified: Fri, 24 Jul 2020 14:36:20 GMT  
		Size: 117.8 MB (117832771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99326e079d8356e854ac855339d61ce4b147c3bdcb821bae0fee303fe4ce1af7`  
		Last Modified: Fri, 24 Jul 2020 14:35:58 GMT  
		Size: 19.8 MB (19776437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7463ed3a41cd22226c05039cf0f173cfd761f25f460589c01d4f4ad1ab25c63d`  
		Last Modified: Fri, 24 Jul 2020 14:35:52 GMT  
		Size: 638.0 KB (637972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ee91320db6590cbfb73a0f8d51713d1d0ccdfff5c8fff6cd752a98ce0798a4`  
		Last Modified: Fri, 24 Jul 2020 14:35:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:6685f29ca834c5bfb13bd5d736538e1598291fcdef1b675d50880bede5884f42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354656225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8443785751b18fe1991695ba9c3aad1222b20a3fecf1093de6100f5abadbbeb`
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
# Fri, 24 Jul 2020 17:08:46 GMT
ENV ROS_DISTRO=dashing
# Fri, 24 Jul 2020 17:11:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:11:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 24 Jul 2020 17:11:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 17:11:37 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 17:12:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:12:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 17:12:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 Jul 2020 17:13:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:13:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 17:13:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 17:13:23 GMT
ENV ROS1_DISTRO=melodic
# Fri, 24 Jul 2020 17:13:25 GMT
ENV ROS2_DISTRO=dashing
# Fri, 24 Jul 2020 17:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:16:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:17:05 GMT
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
	-	`sha256:489f0f02527df688ad2590f0b32ecd9575d084cb31f53e42c68ab093cbd77861`  
		Last Modified: Fri, 24 Jul 2020 17:44:55 GMT  
		Size: 153.5 MB (153516329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0470d9e01e4c2a5c1f8a74e60c141a49e27ef16960c91d1aa6777e37230a24cd`  
		Last Modified: Fri, 24 Jul 2020 17:44:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a163c3e77a6e149ca5850e98f64b153ba232f7fb32162e85e5eebf66a462e6a5`  
		Last Modified: Fri, 24 Jul 2020 17:45:16 GMT  
		Size: 48.5 MB (48527355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadbf07096d379bab8767464c071f3fa7c2f534352210c9e549c7cff494fe967`  
		Last Modified: Fri, 24 Jul 2020 17:45:02 GMT  
		Size: 185.6 KB (185556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4bb640b051ad458200851d3713b966767748559f0c3d7d9c4afe5bf522268b`  
		Last Modified: Fri, 24 Jul 2020 17:45:02 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801d697780e0ccf645910113fb1c8610ef8506a5d566b953570b8262a7c78ab7`  
		Last Modified: Fri, 24 Jul 2020 17:45:04 GMT  
		Size: 3.2 MB (3248444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9ef83b45616503d76db11bcf42cfb8649ccea3591c9a33608b5585e9afab0f`  
		Last Modified: Fri, 24 Jul 2020 17:45:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34c4ee2bf629387c656717c9a56484ec8096bc0c4c218968107d244b6ae85ed`  
		Last Modified: Fri, 24 Jul 2020 17:45:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920556c75ad038f38e05a5e61313b5d50819734fd05d2dd30052da1991f601c6`  
		Last Modified: Fri, 24 Jul 2020 17:46:11 GMT  
		Size: 110.5 MB (110514538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1807bb27a39c7f14a21f274ca3796fe566d48fd69344cd6a42ceec6f7caac352`  
		Last Modified: Fri, 24 Jul 2020 17:45:36 GMT  
		Size: 10.8 MB (10789265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f92639382e1ae4d533688643282588ef7db6c16f9fd5c09d9cd0465b287af`  
		Last Modified: Fri, 24 Jul 2020 17:45:26 GMT  
		Size: 634.3 KB (634271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5359c9ba9d5d337c1049150233e5896290456e23d18b648f6469e03fd5ec30`  
		Last Modified: Fri, 24 Jul 2020 17:45:26 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dc0e489e2b26114a91195e65242bb1aac29a5e00f47ea3860ae9c2d4e21af6b2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386975761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5196fec4c1cbe5e3ef022f61dad9579325bb7218b903a8f1a2446170f34d917`
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
# Fri, 24 Jul 2020 17:08:28 GMT
ENV ROS_DISTRO=dashing
# Fri, 24 Jul 2020 17:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:10:53 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 24 Jul 2020 17:10:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 17:10:58 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 17:12:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:12:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 17:12:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 Jul 2020 17:12:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:12:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 17:12:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 17:13:00 GMT
ENV ROS1_DISTRO=melodic
# Fri, 24 Jul 2020 17:13:01 GMT
ENV ROS2_DISTRO=dashing
# Fri, 24 Jul 2020 17:15:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.6-1*     ros-melodic-roscpp-tutorials=0.9.2-1*     ros-melodic-rospy-tutorials=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:15:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:15:52 GMT
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
	-	`sha256:a8b5c207f3b56e538ef0b3894f9b86fe395550e9037adc2baf14ce5f09158798`  
		Last Modified: Fri, 24 Jul 2020 17:56:26 GMT  
		Size: 165.1 MB (165070250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac410abdf584e0142e23a2bc43eb99d997dc56121671758a68feec6407ca5169`  
		Last Modified: Fri, 24 Jul 2020 17:54:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c3482443c74068090e1d39f2a356b5d4bf4251f88c0b33cbf38db7892f482c`  
		Last Modified: Fri, 24 Jul 2020 17:57:00 GMT  
		Size: 56.8 MB (56837275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e8feb97326cf75ebbcedfa9aaf6481c91f823f8f3921c353121937785aae1a`  
		Last Modified: Fri, 24 Jul 2020 17:56:36 GMT  
		Size: 185.6 KB (185566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece462ecb00f14573f266b76f2679147ed13a7186cfdc1907826d68050754c6e`  
		Last Modified: Fri, 24 Jul 2020 17:56:36 GMT  
		Size: 2.0 KB (2041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f130120108e818e4cfe842b1e58592a4f9c7d1c4ada9a95d228e6f02bca9cbe`  
		Last Modified: Fri, 24 Jul 2020 17:56:42 GMT  
		Size: 3.7 MB (3664153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760867f0748e57c25899fdbb18cda09ecc17efb82ce95dd69807541a95a02eef`  
		Last Modified: Fri, 24 Jul 2020 17:57:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3b5a6eac2012c33b24d619df9f061635fc5c0c4d7845cffd4a7db147ace224`  
		Last Modified: Fri, 24 Jul 2020 17:57:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a88d4b194a97c5b751f0ffc493d55324fd46d00397e3d45b99c51c084f9b72`  
		Last Modified: Fri, 24 Jul 2020 17:58:34 GMT  
		Size: 116.6 MB (116602117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf2ba71e5ff5606985ede38aa56b813f0f9c1f1adb0184226a6466efbacb8f6`  
		Last Modified: Fri, 24 Jul 2020 17:57:32 GMT  
		Size: 14.9 MB (14930220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827e49b2ec1b6c0d87bce66b550a61538cefe19d069d3f727f1c9c3ebd8026d8`  
		Last Modified: Fri, 24 Jul 2020 17:57:13 GMT  
		Size: 635.0 KB (634977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebffed09149cf7cf03430b42b7eb1b4a8bd54e2467caaae91817e3f61a36c7c3`  
		Last Modified: Fri, 24 Jul 2020 17:57:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
