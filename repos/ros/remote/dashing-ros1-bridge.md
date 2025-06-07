## `ros:dashing-ros1-bridge`

```console
$ docker pull ros@sha256:e7a390ef72e0ff452e365dc96d5380424dec9e1bd32cdaab1671431728893c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:dashing-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:b73373f3511aefb837a5c12b2453955235761d1fdf04ac3ba9936a04e5d111f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.4 MB (417404972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d78881b09c95eb6fd429e13eeb7b581e44a3bbfc77cb5464fcaa22171c1781`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/dashing/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=dashing
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS1_DISTRO=melodic
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS2_DISTRO=dashing
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.13-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.9-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Fri, 13 Dec 2024 13:10:33 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd8ed8441cd37839342498b388249635a383eaf297f5499589ce8979f046f6`  
		Last Modified: Fri, 06 Jun 2025 22:49:21 GMT  
		Size: 818.8 KB (818769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa79e0ec580b251d0807a84ec30251d139b8bf726a52d81333afefa4ebed9a9`  
		Last Modified: Fri, 06 Jun 2025 22:49:21 GMT  
		Size: 4.7 MB (4688750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4a1914be82607906bca469c2a3498ad11c47c0a992e8b7b1356d0547b91ce8`  
		Last Modified: Fri, 06 Jun 2025 22:49:21 GMT  
		Size: 2.4 KB (2366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d9cfdc1998122f3c5a4201d80848edd2156c95b8d00afd778a8cc57241e02`  
		Last Modified: Fri, 06 Jun 2025 22:49:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0218ca39ff7a1fed492f7642c12e7571566f4d8dd62da790e77d207c98081309`  
		Last Modified: Fri, 06 Jun 2025 23:07:46 GMT  
		Size: 179.6 MB (179618642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef0a1c07f2aa35a613d990a378483fc39698ed4ec70214f61088c71c59b47d8`  
		Last Modified: Fri, 06 Jun 2025 22:49:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436203b5ed1c3299da3aca7029d044bd99e8abe4228cd5d2193598287824c1fc`  
		Last Modified: Fri, 06 Jun 2025 23:09:32 GMT  
		Size: 64.4 MB (64386571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5536d23635a3f10d572e4eca4960650964bf66c00b9ec5df0853a818e24f9f4`  
		Last Modified: Fri, 06 Jun 2025 23:09:34 GMT  
		Size: 271.7 KB (271657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd124da1ebd9f9e635460a93390b5deadbcdd845a6b3d733cdc01f8b53035fd`  
		Last Modified: Fri, 06 Jun 2025 23:09:35 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113fe3be73dd568fa57d295e65212829fc252f3749b4c7b57c5eb39805e4c8d7`  
		Last Modified: Fri, 06 Jun 2025 23:09:38 GMT  
		Size: 4.1 MB (4098813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b018883210015e67b91e2bf3b49c2dea3b0ac4f9d86d0edc4f1098b34928cc`  
		Last Modified: Sat, 07 Jun 2025 00:10:19 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa72a958330cb8545010845352cae8ee9a6dc5ca8613f531ed267569c8b9188`  
		Last Modified: Sat, 07 Jun 2025 00:10:26 GMT  
		Size: 117.8 MB (117753974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017fe4b565954710483d3fed286180edd305f8d43e539ecd09a40215bc3660b`  
		Last Modified: Sat, 07 Jun 2025 00:10:20 GMT  
		Size: 19.6 MB (19643039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5194cb0fc892ff83f734426e0615ced1f25917bcc87b897bd8918bb80bfe05`  
		Last Modified: Sat, 07 Jun 2025 00:10:21 GMT  
		Size: 427.7 KB (427669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bba2dbaaa80ecb900b604b41416c0bb92892259fef0ddf2f8601a3653ad6ae`  
		Last Modified: Sat, 07 Jun 2025 00:10:21 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:dashing-ros1-bridge` - unknown; unknown

```console
$ docker pull ros@sha256:45b2abe500e2564750cf7834b01c37a77f7402589a7c51d38c144364bff81ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38539695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0928e02a9d1c24d36acb1e831b52032bbb5496857d4e229f2a15d646b1d865f7`

```dockerfile
```

-	Layers:
	-	`sha256:b9bc8330390a2909a4ac38f0f15fab30733a6846ecc61ad4169f97718724c382`  
		Last Modified: Sat, 07 Jun 2025 01:18:42 GMT  
		Size: 38.5 MB (38512795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fdaab8239fd38c2404e0e58f58e59e311e32885fa039d72a63195cde1314eed`  
		Last Modified: Sat, 07 Jun 2025 01:18:44 GMT  
		Size: 26.9 KB (26900 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:dashing-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:68955c66c38ff41ef6740803b3917bde29d99c4005697339168b9832e676a055
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.0 MB (354982206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bec64ac749ddc56a1f2a071b28061f5511a2b168a1961e1512a8bc6a2372fe`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 May 2021 17:00:25 GMT
ADD file:c990710d70105be91eebcea7dfdf28e2212d37ea9279eb2dfd0071e9ed2fd4f1 in / 
# Wed, 26 May 2021 17:00:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 17:00:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 17:00:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 17:00:27 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 23:58:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 23:59:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Jun 2021 19:52:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 02 Jun 2021 19:52:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Jun 2021 19:52:27 GMT
ENV LANG=C.UTF-8
# Wed, 02 Jun 2021 19:52:27 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Jun 2021 19:52:28 GMT
ENV ROS_DISTRO=dashing
# Wed, 02 Jun 2021 19:53:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Jun 2021 19:53:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 02 Jun 2021 19:53:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Jun 2021 19:53:24 GMT
CMD ["bash"]
# Wed, 02 Jun 2021 19:54:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Jun 2021 19:54:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Jun 2021 19:54:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 02 Jun 2021 19:54:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Jun 2021 19:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Jun 2021 19:54:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Jun 2021 19:54:36 GMT
ENV ROS1_DISTRO=melodic
# Wed, 02 Jun 2021 19:54:36 GMT
ENV ROS2_DISTRO=dashing
# Wed, 02 Jun 2021 19:55:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.11-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Jun 2021 19:55:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.8-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Jun 2021 19:55:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Jun 2021 19:55:48 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:c61ae1d5a3957b8a0838e053004a2ddf56e395d58ee3b63baa7b1c865a6383b9`  
		Last Modified: Mon, 17 Feb 2025 09:56:51 GMT  
		Size: 22.3 MB (22292007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efaa8fe9a238b7a58ef37a164ef3a580b7e27445d98012b50395eedd92bad76e`  
		Last Modified: Mon, 17 Feb 2025 09:56:50 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07c60aae22667580605aaf11e146d4ccd94df1bb94c42d91954727cd3515f9a`  
		Last Modified: Thu, 19 Dec 2024 12:05:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d935c6c5648a195e1f983ccaccfaf15bc4a8a7d76fbc25ca9d74a088cf1eca58`  
		Last Modified: Fri, 09 May 2025 07:56:50 GMT  
		Size: 841.2 KB (841165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced11f60bd4cd445ffd162c5741258552033e478ee07a70c27a6bcbe9617084`  
		Last Modified: Thu, 05 Jun 2025 08:25:57 GMT  
		Size: 4.1 MB (4085572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308525c4bd3588947e48a27beef1637e3ab5e638c6b44e8982e5ad7e3943d4fe`  
		Last Modified: Fri, 09 May 2025 07:56:50 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342619be33a81f08f2565508ff5f1b725ea6265bd56c12c8637f4c9434cf0b16`  
		Last Modified: Fri, 09 May 2025 07:56:50 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44be94c3c3454be01b9676a6a11be82df6885b2e68530d74fe47b5caea09c20`  
		Last Modified: Wed, 02 Jun 2021 20:09:26 GMT  
		Size: 153.6 MB (153586272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79775ecfa941b1960cf016f711dabbef63c4e6fa108e8bceecfc11f08bd5729`  
		Last Modified: Fri, 09 May 2025 07:56:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c4a32587c01245eaa5505c89ef0c58bd886983a180ffea9a72a8eec496c7cf`  
		Last Modified: Thu, 05 Jun 2025 08:26:14 GMT  
		Size: 48.5 MB (48548709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e18e3ae33bf71c2c3f6b39e3e43efee4cfc0dae38e61b8d8d40632fc0abe9e`  
		Last Modified: Thu, 05 Jun 2025 08:26:01 GMT  
		Size: 220.9 KB (220875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255e43bfd3e4071b149283084c286c04105b8b52a0b3ff7b1410659752b25f5`  
		Last Modified: Thu, 05 Jun 2025 08:26:03 GMT  
		Size: 2.0 KB (2039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979f81fe6b9535fb2b6dc97a8eac48831e4cbfe42a24c53adb1d91513b8f750b`  
		Last Modified: Thu, 05 Jun 2025 08:26:06 GMT  
		Size: 3.2 MB (3249519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543e1f3ae1ff56cbc032b311258a0ab5de797f613890d4b0949b4b6ae69fd3af`  
		Last Modified: Thu, 05 Jun 2025 08:26:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df045367f7d726407f0198bcfb789f84c0fe466abe7be396fc4dc8aca520cf`  
		Last Modified: Thu, 05 Jun 2025 08:26:53 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd67259368caad61b4d8888f895fa7011ebe87fe19d0b025f0b8cab8d92f8d72`  
		Last Modified: Thu, 05 Jun 2025 08:27:14 GMT  
		Size: 110.7 MB (110702722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facfc5809acff17547783514945bc1f773ba8e311e81a48ec2f59fbcf534ae59`  
		Last Modified: Thu, 05 Jun 2025 08:26:59 GMT  
		Size: 10.8 MB (10814340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf34bada9e270a6adbb558662e93c2be495f5be7315ae5ea967b4b122cb24fb`  
		Last Modified: Thu, 05 Jun 2025 08:26:55 GMT  
		Size: 634.9 KB (634916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c202383cd45183acd3b3c9353a6371a38acf6c65cc1aa34e7a06de1292ab8e30`  
		Last Modified: Thu, 05 Jun 2025 08:26:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2b10925c5f66df3abdcc5b1309b29ae28d6a5b3bb06f7de5698ed9696febc105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 MB (385797053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bb0fc814acbe5aa1bd34fef53293aa18dbf2c0c26e5c6dab45ae482062a621`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/dashing/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=dashing
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS1_DISTRO=melodic
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS2_DISTRO=dashing
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.13-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.9-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Fri, 13 Dec 2024 14:46:44 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6559b6c0a95271b577d553166080f5d9965d9e2d2b1732c96a566175205af31f`  
		Last Modified: Fri, 06 Jun 2025 22:59:17 GMT  
		Size: 818.8 KB (818832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99d6787c1aa8369d0f0e3a1051c56c004c0b42816139b09e85d5fed6e44a27`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 4.3 MB (4270397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5c6de79efb0ec1e3e319f9a58fd5e398fcb65ffb3eff75ff9ff1cff87f158`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de66311d99fe34c7b7bc06e2833185403e088158b4326bbbd2022eabe9a378a`  
		Last Modified: Fri, 06 Jun 2025 23:07:20 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199be9d95ced96059857f7c4db21a0bc6625497f5d13118bca846cb28a919ff3`  
		Last Modified: Sat, 07 Jun 2025 11:46:52 GMT  
		Size: 165.3 MB (165270927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615a4d69dc93931e292692b409e35758072fd07749599cf55495669e5cfee61b`  
		Last Modified: Fri, 06 Jun 2025 23:07:20 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c914c54309fb70eb49b742330277718567eb12e0ebf14c7e8bdb31080ee5cc51`  
		Last Modified: Sat, 07 Jun 2025 11:47:15 GMT  
		Size: 57.1 MB (57082129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9931fc588f4429cff4befdcc8ce81ee800e02c67ac1df621afee0c4d5851211d`  
		Last Modified: Sat, 07 Jun 2025 00:59:12 GMT  
		Size: 271.7 KB (271660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82095c11725fa657ad435b923721974e36264b897daddcccf3ac0748e08a9042`  
		Last Modified: Sat, 07 Jun 2025 00:59:18 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d619f4a1bc076bce16c0ddd0463fcd1913dc19a930f554beed43a52ec4cf60`  
		Last Modified: Sat, 07 Jun 2025 00:59:24 GMT  
		Size: 3.4 MB (3448369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1188d9918375ff4fcad7d410a3497b50e391ad56de21abeac4b62b1563a1b32e`  
		Last Modified: Sat, 07 Jun 2025 01:10:49 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775d4ed89323e5b08f6a53cac49d984a5d465a2430185f329fa897ebf47ad843`  
		Last Modified: Sat, 07 Jun 2025 01:10:54 GMT  
		Size: 116.7 MB (116687731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7da46059d323c74154a387d88715a17e9261b74f7c0f3ec02fe11bf945475`  
		Last Modified: Sat, 07 Jun 2025 01:10:51 GMT  
		Size: 14.8 MB (14803911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d982fcf5dfca8e88179e1c1c8293d74070525a125ae7ec58e03f2ba8ae08575d`  
		Last Modified: Sat, 07 Jun 2025 01:10:51 GMT  
		Size: 423.8 KB (423803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88d33ac9653178683dc785faf4c8d3c2e864d072bb3023cdd373e729064277d`  
		Last Modified: Sat, 07 Jun 2025 01:10:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:dashing-ros1-bridge` - unknown; unknown

```console
$ docker pull ros@sha256:dcb85e544ca73ac6d044441f028accf3f0dd506ae7c1cc392a5651137c332ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37173573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08727de6eaf82c1426714be2ee6112f32487ab4c001724307f3fa9a663cc68b`

```dockerfile
```

-	Layers:
	-	`sha256:748f576bb95f57926fadad97529aada126326d7a3830904106bb39c0f7b2495d`  
		Last Modified: Sat, 07 Jun 2025 04:18:02 GMT  
		Size: 37.1 MB (37146533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff2ca6ad5a626f112f2612821c6814d277af065260806e4adf976b5ea375eb6`  
		Last Modified: Sat, 07 Jun 2025 04:18:03 GMT  
		Size: 27.0 KB (27040 bytes)  
		MIME: application/vnd.in-toto+json
