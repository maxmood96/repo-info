## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:81d557f305cd24ff0c2a26069902e6d67f31258cdf47fac1d05d37b54a619e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:2c8d7d955404a70aabfcf460eef0130642b2f38b0b539f45440284d37472ce8a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340219634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cee1c8e26173f90e964d6076f4099193051e2a0f93d55f32ca9a1ed58beb67`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:34 GMT
ADD file:9f937f4889e7bf6467d34e7ac4f093054993a93399443dc7469d53750a62234f in / 
# Wed, 19 Aug 2020 21:14:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:39 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:56:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:10:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:10:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 20 Aug 2020 00:30:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 20 Aug 2020 00:30:24 GMT
ENV LANG=C.UTF-8
# Thu, 20 Aug 2020 00:30:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 20 Aug 2020 00:30:24 GMT
ENV ROS_DISTRO=foxy
# Thu, 20 Aug 2020 00:31:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:31:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 20 Aug 2020 00:31:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 20 Aug 2020 00:31:20 GMT
CMD ["bash"]
# Thu, 20 Aug 2020 00:31:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:31:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 20 Aug 2020 00:32:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 20 Aug 2020 00:32:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:32:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 20 Aug 2020 00:32:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 20 Aug 2020 00:32:16 GMT
ENV ROS1_DISTRO=noetic
# Thu, 20 Aug 2020 00:32:16 GMT
ENV ROS2_DISTRO=foxy
# Tue, 01 Sep 2020 23:56:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.8-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 23:05:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.3-7*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Sep 2020 23:05:45 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:54ee1f796a1e650627269605cb8e6a596b77b324e6f0a1e4443dc41def0e58a6`  
		Last Modified: Wed, 29 Jul 2020 15:19:55 GMT  
		Size: 28.6 MB (28558017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bfea53ad120b47cea5488f0b8331e737a97b33003517b0bd05e83925b578f0`  
		Last Modified: Wed, 19 Aug 2020 21:16:56 GMT  
		Size: 32.3 KB (32336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d371e02073acecf750a166495a63358517af793de739a51b680c973fae8fb9`  
		Last Modified: Wed, 19 Aug 2020 21:16:55 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66c17bbf772fa072c280b10fe87bc999420042b5fce5b111db38b4fe7c40b49`  
		Last Modified: Wed, 19 Aug 2020 21:16:56 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa557cc6371ecdf29da34fb9617bb250fff91a99f8d09bd3b5f4ba454d5c4d8b`  
		Last Modified: Wed, 19 Aug 2020 23:11:16 GMT  
		Size: 1.2 MB (1175798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d14d67fb1371eab29e8b3ebd3cc38806d01da3fe7d7dacf2ee8fe215c2f74b`  
		Last Modified: Thu, 20 Aug 2020 00:42:13 GMT  
		Size: 5.5 MB (5546328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0f0cb43f8f135cf525d89b3ea013f7c5b7c19e56d68b80ca9c9473ad7f98f2`  
		Last Modified: Thu, 20 Aug 2020 00:42:11 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bef4bdda2da36783e1bf00a1c99b386fc7130a92dff0242646a81c8879e60f3`  
		Last Modified: Thu, 20 Aug 2020 00:48:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a194702420ea560879a75664cf83b50f5e1a80c30255f164e3c4d42f6c0bd5b4`  
		Last Modified: Thu, 20 Aug 2020 00:48:50 GMT  
		Size: 119.3 MB (119325706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd87ad3bb30fdce533ab5c821d5b574e321a8badc8f3ba557547c4b4ac80c1d`  
		Last Modified: Thu, 20 Aug 2020 00:48:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf01c9494f348cdc30a318c91f4af127ecf106148f44c7e53dc6c903d43fcf5`  
		Last Modified: Thu, 20 Aug 2020 00:49:08 GMT  
		Size: 66.6 MB (66578193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564e0662a79ca83816c38b8eed1750a75349c62328faab5b3b7cdc67ab1efccd`  
		Last Modified: Thu, 20 Aug 2020 00:48:55 GMT  
		Size: 191.2 KB (191189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d21aeee94d4d2159f98a39d6ef4104c2c0e96f7f37234e4824319a59a32c58b`  
		Last Modified: Thu, 20 Aug 2020 00:48:54 GMT  
		Size: 2.0 KB (2008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540b3328bf471d3974e574e59d0bd60cf133a94644471ffb2ef88c5d0af31205`  
		Last Modified: Thu, 20 Aug 2020 00:48:58 GMT  
		Size: 10.3 MB (10278123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae3dc358cbd8b97ceabbeaa8d72660dbcc25374a2174d7b4e81190c9eea48f6`  
		Last Modified: Thu, 20 Aug 2020 00:49:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951d604a7521e8261e253308d15f92147aacbef32ff17722d578158e276de950`  
		Last Modified: Thu, 20 Aug 2020 00:49:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173d4c3ca3f37769f4de65a7bf043acfbec125fefbb2073909c8c7ae84d93e3c`  
		Last Modified: Tue, 01 Sep 2020 23:59:45 GMT  
		Size: 76.1 MB (76091425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01955843cfe58a7ff1c2919c7d9289a004b6c8ec0f5a656bcda55a46cfea2aaa`  
		Last Modified: Fri, 11 Sep 2020 23:07:09 GMT  
		Size: 32.4 MB (32437043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07deba9e1b5006a6ceb3f6d220c4f12e41c6a2446675c0815de52a1044b5eee7`  
		Last Modified: Fri, 11 Sep 2020 23:07:00 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:87a4ccbca6a0c476af77c15e3dfbec28bc2d3d00eb5e0da63f484894bfe12399
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (308963428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3682a11c4dbc86fb9f00b2cd49b1a8e9965f3968c60d2836095241f389da406`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:16:56 GMT
ADD file:063d9d9577619d2eeb19bbc784fecf567039a314d8f741500841f6b4f3c847b3 in / 
# Wed, 16 Sep 2020 23:17:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:17:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:17:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:17:04 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 01:44:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:44:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:45:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 02:13:08 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 17 Sep 2020 02:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 02:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 02:13:10 GMT
ENV ROS_DISTRO=foxy
# Thu, 17 Sep 2020 02:14:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:15:08 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 17 Sep 2020 02:15:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 02:15:18 GMT
CMD ["bash"]
# Thu, 17 Sep 2020 02:16:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:16:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Sep 2020 02:16:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 17 Sep 2020 02:16:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:16:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 02:17:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Sep 2020 02:17:01 GMT
ENV ROS1_DISTRO=noetic
# Thu, 17 Sep 2020 02:17:01 GMT
ENV ROS2_DISTRO=foxy
# Thu, 17 Sep 2020 02:17:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.8-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 22 Sep 2020 16:44:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.4-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 22 Sep 2020 16:44:43 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:33c9bf8777b52e6bc989f3a77a8a680861b9a7f7385e2d5ee02fdede89acf606`  
		Last Modified: Wed, 16 Sep 2020 08:25:33 GMT  
		Size: 27.2 MB (27158462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1900e162114f589f3e78ba5b26957f2b6ec38c8aaa6efdd8afbfaf5d9e8841`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53c8a81c25472b52dd428e136c84a1f407ce933911cab5910676d1a7b7a4df3`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ddde6856911f795c55f1e3e7d0658aa1d457594dbf63fd18f6cbc10fd0658`  
		Last Modified: Thu, 17 Sep 2020 02:36:11 GMT  
		Size: 1.2 MB (1177642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3c413801c3e32051187650ead158523b1424776c96e4f3d3410b393309dc4`  
		Last Modified: Thu, 17 Sep 2020 02:36:03 GMT  
		Size: 5.5 MB (5513389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe76cc3db355f14c9557f875c35c68fbbd7d00a458bbc2ab91a3dd10ae61464b`  
		Last Modified: Thu, 17 Sep 2020 02:36:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd035db57351467e95400554c075d902030a7049744862ceb593f9fe9f3d4eed`  
		Last Modified: Thu, 17 Sep 2020 02:49:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6486f66e843c2d0fa9f8b67886198175a38db9b12b600c24419d605194ceaec4`  
		Last Modified: Thu, 17 Sep 2020 02:50:31 GMT  
		Size: 103.6 MB (103594229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d38132067b4812cb0aeae56852e8f528befce4d1a0303b9c6557e85c4559df`  
		Last Modified: Thu, 17 Sep 2020 02:49:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae327fa62e8643a3be1ea4b079aad5f44ee7da97a71ce449164802e3de57d87`  
		Last Modified: Thu, 17 Sep 2020 02:51:06 GMT  
		Size: 60.9 MB (60935351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44ffbeddc38b313a58d4574d3d473d989aa83ce65ae18cc4ffcf8ed79af5a33`  
		Last Modified: Thu, 17 Sep 2020 02:50:41 GMT  
		Size: 194.0 KB (194003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a792002dd65736fdd1ec6c142dc6220b768b9b0cce37fbc02d0667de757c7bf2`  
		Last Modified: Thu, 17 Sep 2020 02:50:40 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afd760246da7e723c31746019ce3d8774971fbb22c7d13b1adbfa4ef99d99ec`  
		Last Modified: Thu, 17 Sep 2020 02:50:50 GMT  
		Size: 9.3 MB (9299667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e166ebf8ce7d781f6fb282ec60de9bc6c61c42d17fba300bebf5fcfe489264`  
		Last Modified: Tue, 22 Sep 2020 16:46:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb038e9184a7cf177d1d2cda7e3ca48b09cd0e20980732f3eca081a0d8cb49`  
		Last Modified: Tue, 22 Sep 2020 16:46:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e470d007d076d3414973e5cd7569b66aa896d1c41e1e91c0b2b529cc4b7ea42`  
		Last Modified: Tue, 22 Sep 2020 16:47:05 GMT  
		Size: 76.1 MB (76132653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d279110313bb4929ad2e333bf7ddce11209a59de438ce162dd0ad53a59089dc`  
		Last Modified: Tue, 22 Sep 2020 16:46:10 GMT  
		Size: 25.0 MB (24952475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710f083bfce2134e97b4af86252e12826c832d63f12c3cb3ea5bdd6a7289b8d0`  
		Last Modified: Tue, 22 Sep 2020 16:46:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
