## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:da9aa266c57aefc1c905fffad776458642360041c3ed591cb152ce58583d2e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:a98de0a30433919a12ce2c9b51e59708ad82deb10efcb3a41c421a125c185650
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340562644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f34fcbf4cd3ae7147e85b2220b8b55e183b21736dde9f2c22823b0785e228a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:38:20 GMT
ADD file:2a90223d9f00d31e31eff6b207c57af4b7d27276195b94bec991457a6998180c in / 
# Thu, 21 Jan 2021 03:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:23 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:38:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:13:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:13:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 11:34:22 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 11:34:23 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 11:34:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 11:34:23 GMT
ENV ROS_DISTRO=foxy
# Thu, 21 Jan 2021 11:35:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:35:34 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 11:35:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 11:35:34 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 11:36:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:36:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 11:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Jan 2021 11:36:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:36:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 11:36:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 11:36:36 GMT
ENV ROS1_DISTRO=noetic
# Thu, 21 Jan 2021 11:36:36 GMT
ENV ROS2_DISTRO=foxy
# Thu, 21 Jan 2021 11:37:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:37:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:37:54 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:83ee3a23efb7c75849515a6d46551c608b255d8402a4d3753752b88e0dc188fa`  
		Last Modified: Thu, 21 Jan 2021 03:40:40 GMT  
		Size: 28.6 MB (28565893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98fc6f11f08950985a203e07755c3262c680d00084f601e7304b768c83b3b1`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f611acd52c6cad803b06b5ba932e4aabd0f2d0d5a4d050c81de2832fcb781274`  
		Last Modified: Thu, 21 Jan 2021 03:40:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b329de66e00a76df07e660eb83a5097f2bbaca25d0f8030ae04b2a9045d726e`  
		Last Modified: Thu, 21 Jan 2021 08:55:02 GMT  
		Size: 1.2 MB (1181953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ca6f3074dc19264c495086cc66977079fd2553a4803bff7061524587caeff8`  
		Last Modified: Thu, 21 Jan 2021 11:47:40 GMT  
		Size: 5.5 MB (5547368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b12fc1d4ab992cb14f16c7af9bd19f75b5fd82db79e4e925e38bcb4969667`  
		Last Modified: Thu, 21 Jan 2021 11:47:39 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b4b846f1510e05ec2e9f03bfbb1e0865f69dcb23742f4f04590bed5d988feb`  
		Last Modified: Thu, 21 Jan 2021 11:54:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b259f35f776936d1796eb51a1a47423174db720389088ac633f46483d543a`  
		Last Modified: Thu, 21 Jan 2021 11:54:41 GMT  
		Size: 119.6 MB (119557479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4229edc1d43a88c146e8d7fab4b1a5e259bfafedfa9c6cee45ba8714b3cd3e45`  
		Last Modified: Thu, 21 Jan 2021 11:54:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277b67b9622a56c53552f91d67a2d703edd5603bff90f60b963639d960bea5e9`  
		Last Modified: Thu, 21 Jan 2021 11:55:02 GMT  
		Size: 66.6 MB (66587799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8092a1e5a019a325196c165864fffcd5825976f4e4f73a19a9b71dadbc3e2`  
		Last Modified: Thu, 21 Jan 2021 11:54:50 GMT  
		Size: 211.3 KB (211258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878b6b31e0cb83e3415edba336817bf0e830a5d0fea4c06b0ca1af25cf91191d`  
		Last Modified: Thu, 21 Jan 2021 11:54:49 GMT  
		Size: 2.0 KB (1972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48020c84e0f0e92db373c8dff5c14935bbad322fe8df11bf39819243cabc769d`  
		Last Modified: Thu, 21 Jan 2021 11:54:53 GMT  
		Size: 10.3 MB (10290363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac5b16f6c8f731c4832e1bce44d120dea67296b79a590b4e7ce33987fd40eae`  
		Last Modified: Thu, 21 Jan 2021 11:55:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce73a2d73426a73b21e9fdde987fe6c1c7cd54619dfa3a03ec4d891e1594605d`  
		Last Modified: Thu, 21 Jan 2021 11:55:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e78bcd18e9cf956cbeafe157fe0f27b148c1140b6b1992f51e83c334efbab1`  
		Last Modified: Thu, 21 Jan 2021 11:55:39 GMT  
		Size: 76.1 MB (76083676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ed1ec0d84e49564cdd276bbcb2887a0d4a8ef5a6892adb0016eec0d79ab14a`  
		Last Modified: Thu, 21 Jan 2021 11:55:24 GMT  
		Size: 32.5 MB (32531417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a55840b4b7236efa0a350dffd8e3acfb29ff713e7a558c9acaa42fee1550645`  
		Last Modified: Thu, 21 Jan 2021 11:55:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e21f19d1c6436150cd9720d1a3b8a2d7937e20e9df3df014bb2f0937d31eef1f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309280824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611402ca59e7cc6f75f5e03c1e89655101b94ddeadc1494ba197ac3d28acb894`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:52 GMT
ADD file:545034ea3827af1e798fe258a2c4b8bb8fb5badc040b6003de9523eb395fa271 in / 
# Thu, 21 Jan 2021 03:49:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:59 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:00 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:45:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:45:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:45:37 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 07:09:09 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 07:09:09 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 07:09:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 07:09:11 GMT
ENV ROS_DISTRO=foxy
# Thu, 21 Jan 2021 07:10:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:10:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 07:10:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 07:10:57 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 07:11:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:12:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 07:12:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Jan 2021 07:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:12:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 07:12:48 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 07:12:49 GMT
ENV ROS1_DISTRO=noetic
# Thu, 21 Jan 2021 07:12:49 GMT
ENV ROS2_DISTRO=foxy
# Thu, 21 Jan 2021 07:13:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:14:29 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:19d658f3801a0fe0a5260f829f7f2d04d9153f1fc8556771ddbb5a672fa91aad`  
		Last Modified: Tue, 19 Jan 2021 08:25:38 GMT  
		Size: 27.2 MB (27172933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdea3dddb14aaf7dfe4ed67963d3c95d1325f4c5b8da5b9d6febaf9df6d875`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf194558d7d697893645e2928d8c12f602b77dd0aaf2f5344233277d7b160d1`  
		Last Modified: Thu, 21 Jan 2021 07:29:34 GMT  
		Size: 1.2 MB (1183038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f15cd3db3fa7d5351aa9b332d57ca02a4276fef9f7b3363ef98b2c4f9611d8`  
		Last Modified: Thu, 21 Jan 2021 07:29:31 GMT  
		Size: 5.5 MB (5514280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de67e6495e9d3639f76b9c4f19a8a602bcf7fe068fb7b7f08ee8cba855c1f301`  
		Last Modified: Thu, 21 Jan 2021 07:29:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dba3fea46fa21f2e435af76ebf72934a3b25fc18e9d03b07f583304b0335d7e`  
		Last Modified: Thu, 21 Jan 2021 07:36:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f91591140f1d30742b9bc74216ea65efb94af4c394cce84b7b2fe198767ae5e`  
		Last Modified: Thu, 21 Jan 2021 07:37:11 GMT  
		Size: 103.8 MB (103787544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b99cacb692debf9d4361dce6953ff14335b7d041eb854b15d5821e6856a5065`  
		Last Modified: Thu, 21 Jan 2021 07:36:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a208dbc4f03b742bef52fb1e5fce8691b1968159312ad723c181fcaeb88b0dd5`  
		Last Modified: Thu, 21 Jan 2021 07:37:37 GMT  
		Size: 61.0 MB (60960284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c5f3216884412ea3074277cc33323cd237873504b26931dd1a91442f07dc6d`  
		Last Modified: Thu, 21 Jan 2021 07:37:22 GMT  
		Size: 211.3 KB (211317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66752a00633f8d87929fc217ddf9325223ad15113d8b6b4c807c20a243960d4b`  
		Last Modified: Thu, 21 Jan 2021 07:37:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39324780393ceb2d62140c698f51132fcbcfca2bc48e3f4f652c9cf4215cf7de`  
		Last Modified: Thu, 21 Jan 2021 07:37:26 GMT  
		Size: 9.3 MB (9309437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9141363b3bbaca13476e46f05eb56577389f5c5f175dd9ae7e222753a1dae3`  
		Last Modified: Thu, 21 Jan 2021 07:37:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e566c9576c5996d73d9d99b0ba405ead78d1ecedd92bb8769fea25e936ae049b`  
		Last Modified: Thu, 21 Jan 2021 07:37:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5001c3a24669856860aee07650d2a052dc6404b2218029a471d401fdb5676a6`  
		Last Modified: Thu, 21 Jan 2021 07:38:15 GMT  
		Size: 76.1 MB (76142034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c884f87b2ed454477db6bdf42e71ba71878c5c2a093717cd1ce7c59108d930b`  
		Last Modified: Thu, 21 Jan 2021 07:37:57 GMT  
		Size: 25.0 MB (24994439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff9c0da17b48f6cb53e8689dc4bae10b9c650d59a147f4c9b46c522801d83e2`  
		Last Modified: Thu, 21 Jan 2021 07:37:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
