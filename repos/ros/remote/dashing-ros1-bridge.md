## `ros:dashing-ros1-bridge`

```console
$ docker pull ros@sha256:954c789ac2bb5c1282635a1c1adbb0ef66b6772dad10ffb7c4e30fb8dc4dd15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:ceda000f2dc8ef7fa3145156c0ba06b7d833f14af2b04e0618ab4dc5b7f57476
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.5 MB (419467116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3c23c0d116f69db0e60c650f4b21c1e50d47f253d782c47c3424514fdff35a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:55:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:55:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:55:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:46:40 GMT
RUN echo "deb http://snapshots.ros.org/dashing/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:46:40 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:46:40 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:46:40 GMT
ENV ROS_DISTRO=dashing
# Sat, 09 Dec 2023 03:47:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:47:46 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:47:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:47:46 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:48:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:48:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:48:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:48:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 06:45:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 06:45:57 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 06:45:57 GMT
ENV ROS1_DISTRO=melodic
# Sat, 09 Dec 2023 06:45:57 GMT
ENV ROS2_DISTRO=dashing
# Sat, 09 Dec 2023 06:48:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.13-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 06:48:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.9-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 06:48:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 06:48:39 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384ee9769243a721793f2bfc136371fa17319fb6c6b6477a2e03a17d545616c`  
		Last Modified: Sat, 09 Dec 2023 04:36:31 GMT  
		Size: 818.9 KB (818932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc85c6d8f29e7702b5251b205f55245dc5eb2973909564ad084046a1f6c9324a`  
		Last Modified: Sat, 09 Dec 2023 04:36:29 GMT  
		Size: 4.9 MB (4878334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9964396126f3f0fdee6bb57ba39280b6966c6879a933be850490cea1c00bc65f`  
		Last Modified: Sat, 09 Dec 2023 04:36:28 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788b95565c8f61259b95dd1b2561b4ef4f089b2ae04279e10ce20451703552bb`  
		Last Modified: Sat, 09 Dec 2023 04:47:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bcc35ac8493e8f94f98dbb1b7f9b1bf1f9fbf2b79ed48cde33b9296a53bd07`  
		Last Modified: Sat, 09 Dec 2023 04:47:36 GMT  
		Size: 179.6 MB (179629066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc587f4dedd9f2b690c35896398079acda7605bcd099008e985fed10106620a`  
		Last Modified: Sat, 09 Dec 2023 04:47:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:face2e9daa6a265038ebb05abbdf83953f2661b888387babb624133f7138748d`  
		Last Modified: Sat, 09 Dec 2023 04:47:55 GMT  
		Size: 64.4 MB (64392291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fc6a765840e7992e5efaa89334015d1c29fc0ccea97db5e96d964db766a7e5`  
		Last Modified: Sat, 09 Dec 2023 04:47:46 GMT  
		Size: 241.5 KB (241494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a8d6b556f5350189b615539df8dedc35fecc8cb598120f73d6caa78396a740`  
		Last Modified: Sat, 09 Dec 2023 04:47:46 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a818116c7d27bf162b6e6b5b714efbbe1ae281cef3daa0802d4d71809f1917a`  
		Last Modified: Sat, 09 Dec 2023 04:47:47 GMT  
		Size: 4.3 MB (4314576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a08afab6f888d68cb78b5f00700719a51d99a136a9ff2a6d2ade0579d2e76e`  
		Last Modified: Sat, 09 Dec 2023 06:50:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1ac27716b1e062cccbb5e3b0d2a45c86ad98e1dd731906e45a74029a2c6f8`  
		Last Modified: Sat, 09 Dec 2023 06:50:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6d2c44f329f85e9c8b95002760589900a00753ce63dfc980d88979cf07e72e`  
		Last Modified: Sat, 09 Dec 2023 06:51:08 GMT  
		Size: 118.0 MB (117969931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72d39143062b775d1d05fe0136b91a5a40bd21712b24492fec7c3e29206224c`  
		Last Modified: Sat, 09 Dec 2023 06:50:55 GMT  
		Size: 19.9 MB (19858357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc44035d7bc9fbf9f0f24275c3fde80b238a94913be3e65fbf0bf8965676a76c`  
		Last Modified: Sat, 09 Dec 2023 06:50:51 GMT  
		Size: 640.8 KB (640836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69e40bf88fcd008e67b637a5bc11ed3fc3d7657e6210e510f510f96ec7cbbf4`  
		Last Modified: Sat, 09 Dec 2023 06:50:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
		Last Modified: Wed, 19 May 2021 20:23:59 GMT  
		Size: 22.3 MB (22292007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efaa8fe9a238b7a58ef37a164ef3a580b7e27445d98012b50395eedd92bad76e`  
		Last Modified: Wed, 26 May 2021 17:03:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07c60aae22667580605aaf11e146d4ccd94df1bb94c42d91954727cd3515f9a`  
		Last Modified: Wed, 26 May 2021 17:03:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d935c6c5648a195e1f983ccaccfaf15bc4a8a7d76fbc25ca9d74a088cf1eca58`  
		Last Modified: Thu, 27 May 2021 00:25:19 GMT  
		Size: 841.2 KB (841165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced11f60bd4cd445ffd162c5741258552033e478ee07a70c27a6bcbe9617084`  
		Last Modified: Thu, 27 May 2021 00:25:18 GMT  
		Size: 4.1 MB (4085572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308525c4bd3588947e48a27beef1637e3ab5e638c6b44e8982e5ad7e3943d4fe`  
		Last Modified: Wed, 02 Jun 2021 20:08:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342619be33a81f08f2565508ff5f1b725ea6265bd56c12c8637f4c9434cf0b16`  
		Last Modified: Wed, 02 Jun 2021 20:08:56 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44be94c3c3454be01b9676a6a11be82df6885b2e68530d74fe47b5caea09c20`  
		Last Modified: Wed, 02 Jun 2021 20:09:26 GMT  
		Size: 153.6 MB (153586272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79775ecfa941b1960cf016f711dabbef63c4e6fa108e8bceecfc11f08bd5729`  
		Last Modified: Wed, 02 Jun 2021 20:08:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c4a32587c01245eaa5505c89ef0c58bd886983a180ffea9a72a8eec496c7cf`  
		Last Modified: Wed, 02 Jun 2021 20:09:48 GMT  
		Size: 48.5 MB (48548709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e18e3ae33bf71c2c3f6b39e3e43efee4cfc0dae38e61b8d8d40632fc0abe9e`  
		Last Modified: Wed, 02 Jun 2021 20:09:40 GMT  
		Size: 220.9 KB (220875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8255e43bfd3e4071b149283084c286c04105b8b52a0b3ff7b1410659752b25f5`  
		Last Modified: Wed, 02 Jun 2021 20:09:40 GMT  
		Size: 2.0 KB (2039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979f81fe6b9535fb2b6dc97a8eac48831e4cbfe42a24c53adb1d91513b8f750b`  
		Last Modified: Wed, 02 Jun 2021 20:09:41 GMT  
		Size: 3.2 MB (3249519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543e1f3ae1ff56cbc032b311258a0ab5de797f613890d4b0949b4b6ae69fd3af`  
		Last Modified: Wed, 02 Jun 2021 20:10:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df045367f7d726407f0198bcfb789f84c0fe466abe7be396fc4dc8aca520cf`  
		Last Modified: Wed, 02 Jun 2021 20:10:07 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd67259368caad61b4d8888f895fa7011ebe87fe19d0b025f0b8cab8d92f8d72`  
		Last Modified: Wed, 02 Jun 2021 20:10:32 GMT  
		Size: 110.7 MB (110702722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facfc5809acff17547783514945bc1f773ba8e311e81a48ec2f59fbcf534ae59`  
		Last Modified: Wed, 02 Jun 2021 20:10:10 GMT  
		Size: 10.8 MB (10814340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf34bada9e270a6adbb558662e93c2be495f5be7315ae5ea967b4b122cb24fb`  
		Last Modified: Wed, 02 Jun 2021 20:10:07 GMT  
		Size: 634.9 KB (634916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c202383cd45183acd3b3c9353a6371a38acf6c65cc1aa34e7a06de1292ab8e30`  
		Last Modified: Wed, 02 Jun 2021 20:10:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9283508b12c4e41f94d5a4694de358eb97ef76ff310ad84069edaf79c6b17f9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387869426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9692444dba3ae952d2df73c88cc149a86d5387ca7bc0e41f16cb9ddd73c4b58f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:23:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:24:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:24:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:11:34 GMT
RUN echo "deb http://snapshots.ros.org/dashing/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:11:35 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:11:35 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:11:35 GMT
ENV ROS_DISTRO=dashing
# Sat, 09 Dec 2023 03:12:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:12:29 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:12:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:12:29 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:12:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:13:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:13:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:13:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:13:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:13:22 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 03:13:22 GMT
ENV ROS1_DISTRO=melodic
# Sat, 09 Dec 2023 03:13:22 GMT
ENV ROS2_DISTRO=dashing
# Sat, 09 Dec 2023 03:15:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.13-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:16:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.9-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:16:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:16:12 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92311637e9983a187857b246a6417188e5a1de48e9d03e831eb2cb63a811cf67`  
		Last Modified: Sat, 09 Dec 2023 03:53:39 GMT  
		Size: 819.0 KB (818985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4394df3604b47aaa3d36d1ad63c563ac4d8b172081757c048ee6bf10cdd08`  
		Last Modified: Sat, 09 Dec 2023 03:53:38 GMT  
		Size: 4.5 MB (4461631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1d3a8f1076e5ddb09c78ae7493c813f46853e1e63d7cfe42ba1c50cf6bcf28`  
		Last Modified: Sat, 09 Dec 2023 03:53:37 GMT  
		Size: 2.4 KB (2409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2545580ec0a4ba0c7aa8bffbe603c06fffedd642b5468d14c13339ee16e244eb`  
		Last Modified: Sat, 09 Dec 2023 04:02:44 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383e747daf631ce9bbf197315add6b3faaa7bac26c19426e47b8d50aa50cf8c7`  
		Last Modified: Sat, 09 Dec 2023 04:03:11 GMT  
		Size: 165.3 MB (165280758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ff6dc59f0cc5618aba6bccea80f63550c7289f596c55212df9fe01188964ab`  
		Last Modified: Sat, 09 Dec 2023 04:02:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6671a60e9a363fd0c4d8c6711a6569cc101e737b15685cb1d34fa02ea6d63270`  
		Last Modified: Sat, 09 Dec 2023 04:03:27 GMT  
		Size: 57.1 MB (57089322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4123d745d5582f1227b572e6541752caaef0584d7724bfd86060365f7ad63ffe`  
		Last Modified: Sat, 09 Dec 2023 04:03:20 GMT  
		Size: 241.5 KB (241510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b29509f39e6dbe80f5b7218f1396b6dd3e93534eed2d534c32d6b18d114e2f`  
		Last Modified: Sat, 09 Dec 2023 04:03:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdcfb3fd6f26e1b58df2c03de3f56380d45ab73be74d080b9ce6eef13da042f`  
		Last Modified: Sat, 09 Dec 2023 04:03:21 GMT  
		Size: 3.7 MB (3664865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee240425de65434441438c819fdc45a0f352ca1a3184587cb0700a4befa615a2`  
		Last Modified: Sat, 09 Dec 2023 04:03:41 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c020a7a7c516611369eb1a136280098379cc58926a3e5077745971a6044124e`  
		Last Modified: Sat, 09 Dec 2023 04:03:39 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986d219be57b681cab52620bbc7f2bc561d9bf7422a8868261e82cb4ce8ed711`  
		Last Modified: Sat, 09 Dec 2023 04:04:02 GMT  
		Size: 116.9 MB (116908010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c86c7cdf8b4a8492af6b4238ee4fb3b9bdf2dc36a88c0ea5d624719d1e913c`  
		Last Modified: Sat, 09 Dec 2023 04:03:42 GMT  
		Size: 15.0 MB (15020708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ab6302c1d3c15022ea23644afb4a17cbfa51fb8cca93d847ab3a60e00b6555`  
		Last Modified: Sat, 09 Dec 2023 04:03:39 GMT  
		Size: 636.8 KB (636813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6820582c38053e5df22aedc7a14f45761e2a0866e754a9351f2796c6e016fb4a`  
		Last Modified: Sat, 09 Dec 2023 04:03:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
