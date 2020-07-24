## `ros:eloquent-ros-base-bionic`

```console
$ docker pull ros@sha256:8bb8d9bbcd8d0c094b045339d482af498c9e6fac5006aae15e7245f8f486271e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:49b76a9e3c4b06cf85054d705c41a42b84dd922cb4a6ad72cdbda5f7f76c486f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289031537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b1a82f9dbc878cadad38d4f95157086c545992a2e26e1e089753128b7b1e3a`
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

### `ros:eloquent-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:4df4e6884391dd1bed51eea9d5d17c278b8921724f6972f35ed0cb91a79ac77b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235377951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6eadad4c3f9fda41c3a03f1d52daa68283ebfe3c0cfdc39da6ba1d2ad85554`
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

### `ros:eloquent-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fd6d98b4cd95c068e446e1f6ea8befb0dce8270741983340dd7fe1a8c6c2e3ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257723969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6edae6ff7eda2a1cb395edb37b5b57a34587a4d4cbef3027ccac74cb7f7a4b5`
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
