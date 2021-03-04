## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:12b3070bc74fec76b4a52a344d98068687e18573fc336ac62cf000af2e1e05ee
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
$ docker pull ros@sha256:88649811e3d517ff4f53df7fed2f523417e06d8df7a14433cc88cb6b122d5e94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309617312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cb0c074f24b9b3c061bf44a285a97aa77b09611f972db4cafd73a7f6df00e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:52 GMT
ADD file:1dfda258a4ebfa53687877ae153107d2e472e0b039363ec35aafe9f5733cae22 in / 
# Thu, 04 Mar 2021 02:52:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:53:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:53:01 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 03:22:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:22:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:22:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 03:47:10 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 04 Mar 2021 03:47:12 GMT
ENV LANG=C.UTF-8
# Thu, 04 Mar 2021 03:47:13 GMT
ENV LC_ALL=C.UTF-8
# Thu, 04 Mar 2021 03:47:14 GMT
ENV ROS_DISTRO=foxy
# Thu, 04 Mar 2021 03:49:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:49:10 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 04 Mar 2021 03:49:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 04 Mar 2021 03:49:13 GMT
CMD ["bash"]
# Thu, 04 Mar 2021 03:50:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:50:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 04 Mar 2021 03:50:30 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 04 Mar 2021 03:50:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:51:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 03:51:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 04 Mar 2021 03:51:09 GMT
ENV ROS1_DISTRO=noetic
# Thu, 04 Mar 2021 03:51:10 GMT
ENV ROS2_DISTRO=foxy
# Thu, 04 Mar 2021 03:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:52:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:53:02 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:32d7611b468cbc07986302f1a8e74d92e30a1f11cdfa8bc2900aedda2758d050`  
		Last Modified: Wed, 17 Feb 2021 08:25:24 GMT  
		Size: 27.2 MB (27175799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5be16fdc30614524222cdec466297e7ed49c7695e868c5dd2700a1778d88b23`  
		Last Modified: Thu, 04 Mar 2021 02:54:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a361e87bde5e27ceda037ab2116d88d9570b6d53c34102a2a214ef2944270138`  
		Last Modified: Thu, 04 Mar 2021 02:54:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1317e878738b2e361ab2bc6c5e9dad3effcdd7f83f6a2e3687fc82bc9c1ada3`  
		Last Modified: Thu, 04 Mar 2021 04:04:00 GMT  
		Size: 1.2 MB (1182875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba5f746c529c10d1d08e23f12a45a07e2921c194edd5618c4b72f862233e909`  
		Last Modified: Thu, 04 Mar 2021 04:03:59 GMT  
		Size: 5.5 MB (5512834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea8b4c459768d7eb6fc2a16d12531aface693a3d22b366e35336593ee89d6ad`  
		Last Modified: Thu, 04 Mar 2021 04:03:58 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d21be1269617b9a86a32152d26029110477c2c276439a32dadbb93c5fa52754`  
		Last Modified: Thu, 04 Mar 2021 04:11:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d73feefadb76d43056d52a05b0eb003c4bd10c406e5cf924754a23922d663b6`  
		Last Modified: Thu, 04 Mar 2021 04:12:15 GMT  
		Size: 104.1 MB (104106276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6732d7db72f219eaa7fe5f1c6ff2937694a7b9af6bcffef65ab92812d78cccc4`  
		Last Modified: Thu, 04 Mar 2021 04:11:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352270052b6bd522955000a0d8b627b3f38b47ee1beb5d5b89669d099c5bc0fe`  
		Last Modified: Thu, 04 Mar 2021 04:12:39 GMT  
		Size: 61.0 MB (60959975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4306a174c5fc18925fbe21b82861f938c08d6b06acd983680b446723726ee5ef`  
		Last Modified: Thu, 04 Mar 2021 04:12:25 GMT  
		Size: 214.0 KB (213990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dfb484a78e8562d9f13704ab9c05cfa3401829964fd71e2aeb81a2892a20c7`  
		Last Modified: Thu, 04 Mar 2021 04:12:25 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f604b6078a90357d2344badb2376bdd420424d010881bf1d0c59c5320aa05ca1`  
		Last Modified: Thu, 04 Mar 2021 04:12:28 GMT  
		Size: 9.3 MB (9298560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ab179d5e73e3df6207a06d2854f0251d075aea464a4ffffeb9ce85b9646c2f`  
		Last Modified: Thu, 04 Mar 2021 04:12:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8053c49f2e7be94c3af9b546971d0503c7bd4c79bddcefc72f4d98a9f7999ccf`  
		Last Modified: Thu, 04 Mar 2021 04:12:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239ea0fd2d0e09c4bfbd8eaa042f7c9e2dbfd32ec15c501843c1a40086e361ca`  
		Last Modified: Thu, 04 Mar 2021 04:13:14 GMT  
		Size: 76.2 MB (76156665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd6437411a1546129739b8f2d6fbbea741b28261e467797d5752fc362bbadbe`  
		Last Modified: Thu, 04 Mar 2021 04:12:56 GMT  
		Size: 25.0 MB (25004774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e53da697a8bf1d67c42258be96bf3fd59e33764e03ef1c2d281f62a60bde59`  
		Last Modified: Thu, 04 Mar 2021 04:12:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
