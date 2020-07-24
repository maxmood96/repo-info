## `ros:rolling-ros1-bridge-focal`

```console
$ docker pull ros@sha256:61d29a190e124ce5afc4784101d2d0207904d1fad1cbbe77e754d316ae97ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:ffb2666b71790f8d849dce1c69c486419a632a4fa2a51628b9f5cd33bb097433
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.1 MB (411074791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905a05448080ec0f6057dbe379afbf06decbbfef6ec76d6fbd47a9c977567605`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:51:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:49:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 01:08:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jul 2020 01:08:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jul 2020 01:08:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jul 2020 01:12:04 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Jul 2020 01:12:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:12:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jul 2020 01:12:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jul 2020 01:12:56 GMT
CMD ["bash"]
# Tue, 07 Jul 2020 01:13:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:13:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jul 2020 01:13:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jul 2020 01:13:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:13:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 01:13:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jul 2020 01:13:57 GMT
ENV ROS1_DISTRO=noetic
# Tue, 07 Jul 2020 01:13:57 GMT
ENV ROS2_DISTRO=rolling
# Tue, 07 Jul 2020 01:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.7-1*     ros-noetic-roscpp-tutorials=0.10.1-1*     ros-noetic-rospy-tutorials=0.10.1-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:15:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.9.2-2*     ros-rolling-demo-nodes-cpp=0.10.0-1*     ros-rolling-demo-nodes-py=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 01:15:00 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbd34696aad22f9a861bdae9aed1bc14aed3426d245147e55a759747acc2357`  
		Last Modified: Tue, 07 Jul 2020 00:03:20 GMT  
		Size: 1.2 MB (1175806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d44cae379b4797d812ed05b65c080aba6074d55e8d8b0b0c612b3923d9f5a`  
		Last Modified: Tue, 07 Jul 2020 01:21:06 GMT  
		Size: 5.5 MB (5549483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220c1b9e59cfca503e7910992752f72112d96b996c272d25c279bcbe31fb9210`  
		Last Modified: Tue, 07 Jul 2020 01:21:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b543ebbbdc63c94db2b759d1ed8cd54ae18f43a4819e01c5fadec51f9e2c393e`  
		Last Modified: Tue, 07 Jul 2020 01:27:20 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d11c3c352bbba6334b226dcafdc89fef67ee469024cf9078851f51b763589`  
		Last Modified: Tue, 07 Jul 2020 01:29:44 GMT  
		Size: 119.3 MB (119270006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0d256bd0e6e404fe94f7d14e3828f40f20cf34e17d96e21269d7bc3d31185`  
		Last Modified: Tue, 07 Jul 2020 01:29:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecd071be9eb3fa6fe6ecd661421eb46c692c8290624848a020c6f2a08ad557`  
		Last Modified: Tue, 07 Jul 2020 01:30:02 GMT  
		Size: 66.6 MB (66574259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb746b11ed4dcd4e8a8a5fba1b2dc91174b725f399cdb3afe14346ddcc924db`  
		Last Modified: Tue, 07 Jul 2020 01:29:49 GMT  
		Size: 182.6 KB (182613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646dbb40c22396713fdd5064a773475e336cb49b09a6f2a0fa5c56a20393e54`  
		Last Modified: Tue, 07 Jul 2020 01:29:49 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffa2fdc8d1a068c8cc80d980511e2dffe7f00eaa854982af583047807b757de`  
		Last Modified: Tue, 07 Jul 2020 01:29:52 GMT  
		Size: 10.3 MB (10282380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfa0d69498dc79c389e5b81d25a9404d6fdc2d17c87acbfbf272f711414feba`  
		Last Modified: Tue, 07 Jul 2020 01:30:09 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4791895222aefe27f49b6296de7eee04aeab0598b33f08e20bcab0b005c8929f`  
		Last Modified: Tue, 07 Jul 2020 01:30:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e9754b7b572c6fa53b82a81cedd16c0c962f3ee62d8342b2072b9679ae050f`  
		Last Modified: Tue, 07 Jul 2020 01:30:34 GMT  
		Size: 76.1 MB (76069441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c47dc772b8b3840281a96bb76adba9eeabee8a33043aed2b867b6d65dfc2b2`  
		Last Modified: Tue, 07 Jul 2020 01:30:31 GMT  
		Size: 103.4 MB (103376252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86bc975d013b6e83159a5d4cdc3447108f1c183f990e7812df7c0533cd82343`  
		Last Modified: Tue, 07 Jul 2020 01:30:09 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1cf5e7cddc77a8e53d6eb3d77c8b4f892817dba8057495d2140eeab4d87b6cc1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.7 MB (376650010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21991753e1e53d9792bb891bbe3ed7b3386987045815cf7ca3f6281a603ef628`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:24:06 GMT
ADD file:26bd57f1dbcfd1a91715cc84cf0f221783655f16bbb7a912aaf20507cc252535 in / 
# Fri, 24 Jul 2020 16:24:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:24:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:24:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:24:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:57:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:57:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:57:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 17:24:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 24 Jul 2020 17:24:08 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 17:24:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 17:30:58 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 Jul 2020 17:32:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:32:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 24 Jul 2020 17:32:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 17:32:57 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 17:33:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:34:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 17:34:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 Jul 2020 17:34:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:34:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 17:34:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 17:34:55 GMT
ENV ROS1_DISTRO=noetic
# Fri, 24 Jul 2020 17:34:56 GMT
ENV ROS2_DISTRO=rolling
# Fri, 24 Jul 2020 17:35:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.7-1*     ros-noetic-roscpp-tutorials=0.10.1-1*     ros-noetic-rospy-tutorials=0.10.1-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:37:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.9.2-2*     ros-rolling-demo-nodes-cpp=0.10.0-1*     ros-rolling-demo-nodes-py=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:37:20 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:3583fd5e2faf2976fb6333a3a15414f2708dc284c018a672e37112326bc7b7a1`  
		Last Modified: Mon, 20 Jul 2020 15:50:10 GMT  
		Size: 27.2 MB (27159444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2d9e0aed378588f59f8f4276e70ea379b773d7d6507046cd7a044601499785`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 32.3 KB (32333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4a6dca9e536449681a937b8f49022cb56b230e352da8aed9b616fadb14dc30`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d9e98650a6106452fc9e640abe8929399fa4f7a0d3ef58a593e8d68cdf3a6`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b877914f23fdc8a3fd15f9b3daa4a5a017f378e476b524967a0ab3874b518fe5`  
		Last Modified: Fri, 24 Jul 2020 17:48:49 GMT  
		Size: 1.2 MB (1175990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd422d18fc87ff73ecb113f2cf765e9b4e16079bb0f4c697b78fc61dfbbbb2f`  
		Last Modified: Fri, 24 Jul 2020 17:48:49 GMT  
		Size: 5.5 MB (5511790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281dec9f244ed77fbf977c9357ced59b8843bba14d99bbbaf00a19cb797f655a`  
		Last Modified: Fri, 24 Jul 2020 17:48:43 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8222dc272a4ea67fceee9f2cd1d6fa321f28a2ca48e4187dbef9fc609c03fde7`  
		Last Modified: Fri, 24 Jul 2020 18:02:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e42434d879d59a987c2c6aae212c34d2c3581854d0bcf3dcd95bb5c77ccc38a`  
		Last Modified: Fri, 24 Jul 2020 18:06:37 GMT  
		Size: 103.5 MB (103496824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d66d3005f38065aca76a79dd178e370c20bb4c958bc23a5085471b0a7d8fc13`  
		Last Modified: Fri, 24 Jul 2020 18:05:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbe4ce6b34429b9cf3c595068b425eb279fa003b6ffcd755af09b4de39a38f6`  
		Last Modified: Fri, 24 Jul 2020 18:07:28 GMT  
		Size: 60.9 MB (60932117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ff26300fad41529f36f1b1bdb0e6bce4af3b005161d294e875982b855466c7`  
		Last Modified: Fri, 24 Jul 2020 18:06:48 GMT  
		Size: 183.8 KB (183788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4497e482a6bcda17c5af840af74f4f4439f74d4eefb6dd7a378ef2313c0e3b82`  
		Last Modified: Fri, 24 Jul 2020 18:06:48 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831e9e3f59f3ec1ff626d44ed6a5f7463529aa8839125c2c10190441ea9d347`  
		Last Modified: Fri, 24 Jul 2020 18:06:55 GMT  
		Size: 9.3 MB (9302620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4dbcd98641e93dc690dc032eb1f907ed22c3f81e13b27dd50443cc37b977a8`  
		Last Modified: Fri, 24 Jul 2020 18:07:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adce0bb834206f67e28ffdbb6d2b18cc261d86186910184bb295f0190ea2ca8c`  
		Last Modified: Fri, 24 Jul 2020 18:07:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959f552e40d9ec5f430a3dc25c09cbfb98835f8ac2b08bb409542c0f8e17a75a`  
		Last Modified: Fri, 24 Jul 2020 18:08:53 GMT  
		Size: 76.1 MB (76107416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2fa40db443c5f00a90c62635ed4493ce82b3fbe3da915e27ca3ab9a6008533`  
		Last Modified: Fri, 24 Jul 2020 18:08:44 GMT  
		Size: 92.7 MB (92742164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16284451912c59e9269b67e40952c8f05fb08f3a37990a3b59dfd2b5655d1514`  
		Last Modified: Fri, 24 Jul 2020 18:07:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
