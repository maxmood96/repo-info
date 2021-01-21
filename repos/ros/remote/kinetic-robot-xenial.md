## `ros:kinetic-robot-xenial`

```console
$ docker pull ros@sha256:17d72afb0b28733e0be014d34db4e4c41bc5d12037ea170e713a369b88ae949f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot-xenial` - linux; amd64

```console
$ docker pull ros@sha256:8f6bf59c0a77d23f3da4dc6228fc13f2ee13914154e7ab4e45244a1dc3b4deed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381100413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d86be5915db2ec919b76d43870a9fba5e4148eb2bb4de78d58c08733ac6a7b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 10:54:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 10:54:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 10:54:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 10:54:32 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 10:54:32 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 10:54:33 GMT
ENV ROS_DISTRO=kinetic
# Thu, 21 Jan 2021 10:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 10:56:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 10:56:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 10:56:45 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 10:57:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 10:57:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 10:58:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 10:58:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0d4796d30e0f43e182db9920acc4250ade5b495763f9240bccefb7009b9b13`  
		Last Modified: Thu, 21 Jan 2021 11:42:03 GMT  
		Size: 5.4 MB (5363051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19715d04d91ee89929e4d148b1d8195184afa401cfdd80f4a99c525413f0481`  
		Last Modified: Thu, 21 Jan 2021 11:42:01 GMT  
		Size: 14.7 KB (14743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00130b4546e0f845662e6de8c7d312bfdac7e3a5c3623a110d31cd056084c920`  
		Last Modified: Thu, 21 Jan 2021 11:42:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980049987743cb32239796a293a5292039ab7ad9c963dab35279b738c449bfba`  
		Last Modified: Thu, 21 Jan 2021 11:42:45 GMT  
		Size: 187.2 MB (187158602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fe00c9b3f64d5a8a70fc298a78ac8bf408931047b0bd20d91162e6ecb2620e`  
		Last Modified: Thu, 21 Jan 2021 11:42:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3675a9dc8f29a43751160d63bd135c8083f21b15a290b9ceb8790af28a3d634`  
		Last Modified: Thu, 21 Jan 2021 11:43:04 GMT  
		Size: 57.2 MB (57241407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f10d32bd1ce757e1327ea8b8f46d80362e49f8c35e0966488bf1bffd21a7fda`  
		Last Modified: Thu, 21 Jan 2021 11:42:53 GMT  
		Size: 274.6 KB (274608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2357ee3932199000cf549c533d658c589364695cf2a8f41ae4ceb0d586b1df6`  
		Last Modified: Thu, 21 Jan 2021 11:43:05 GMT  
		Size: 63.6 MB (63577378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73907565a0ae5d8e7e5e35a566f85776ead14daf0e8ef1e2bbb9ad95f8730f23`  
		Last Modified: Thu, 21 Jan 2021 11:43:17 GMT  
		Size: 21.5 MB (21506303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:14949fd8f62d7e38cec6771ae33a97bcb6855d8365ded5e8b4cd0e51449e908d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.6 MB (331584660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e886882e46df8496ce8a0da81f0a6968108ec3e3221e507ea0a52f0b23aa559a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:17:15 GMT
ADD file:c77c1a2ea3c8b1d59252626e6c8be57cca539dfce0a16a0ed2ff0311c0f5a265 in / 
# Thu, 21 Jan 2021 03:17:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:17:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:17:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:17:26 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:21:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 04:21:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 04:21:14 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 04:21:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 04:21:15 GMT
ENV ROS_DISTRO=kinetic
# Thu, 21 Jan 2021 04:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:24:02 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 04:24:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 04:24:04 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 04:24:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:24:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 04:26:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:26:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2af2a813aac2db23328a29ab84155e95fbb6681e872751a4f11f688c005e84c5`  
		Last Modified: Mon, 18 Jan 2021 19:38:27 GMT  
		Size: 40.0 MB (39972659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ef2a276bd8b4a122330892d4a9b9383249f945d22fc34e7b2b0688fbf6af8`  
		Last Modified: Thu, 21 Jan 2021 03:19:28 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01c8ce931ce58b3726d3fa387bcf38f02ca4a4d9fa6db2a764bb8aae4f69079`  
		Last Modified: Thu, 21 Jan 2021 03:19:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ba02aed017c06ce4541aa061d63a8068bd1651fc0f00b9c0995ec1b22bea3`  
		Last Modified: Thu, 21 Jan 2021 03:19:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453d6bcd4fcc109ea638feb11f4efb3cc42368c709239e97d0c80b058d7bac48`  
		Last Modified: Thu, 21 Jan 2021 05:08:43 GMT  
		Size: 4.6 MB (4615362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dada356e54fac0aeb0fc744ccbca68ed154ef97d589d1a9b2e810dab83264c6`  
		Last Modified: Thu, 21 Jan 2021 05:08:41 GMT  
		Size: 14.7 KB (14744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b25c03a830017441e51bb0ee2af49968aa6de63b2d1c8dc15c295e3a71c60`  
		Last Modified: Thu, 21 Jan 2021 05:08:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dfd6725ae662c908d1df455362722a807ff5ce1dd3f66e0356c7fc3cba8f9a`  
		Last Modified: Thu, 21 Jan 2021 05:09:44 GMT  
		Size: 168.1 MB (168052304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe4dcfe4ec1442358eef15e27bdb52616942a46251eeb5e16c05e6e01fc7abe`  
		Last Modified: Thu, 21 Jan 2021 05:08:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f640b399302a8c35ab8373896f86ac688da8f6eb2c5eb6c9e7977057471058`  
		Last Modified: Thu, 21 Jan 2021 05:10:10 GMT  
		Size: 42.9 MB (42891135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3149006c9bfc8193e1b28706b09ddb0d0840baec42688597fbe1e214396cc2a8`  
		Last Modified: Thu, 21 Jan 2021 05:09:57 GMT  
		Size: 274.6 KB (274554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3daa3c23566e4ffe5aa17951beca2e7c692f9394657b16e8180d1595780c02`  
		Last Modified: Thu, 21 Jan 2021 05:10:15 GMT  
		Size: 55.5 MB (55503412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deef93f281643639f5bc5a55a35938116b6f0b24937f99b3f296c36f482a10c8`  
		Last Modified: Thu, 21 Jan 2021 05:10:35 GMT  
		Size: 20.3 MB (20258540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2e492f4346570c95295da7fe9ea8509a8983c8b206d7e18c4ff69eb4f0474bcd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345788517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05c66e81008f3b2b523cee6dbde5e8c698ea4c963ff52e5132dbf3e1ba05ae9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:27:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:27:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 06:27:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 06:27:09 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 06:27:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 06:27:11 GMT
ENV ROS_DISTRO=kinetic
# Thu, 21 Jan 2021 06:29:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:29:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 06:29:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 06:29:22 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 06:30:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:30:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 06:31:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:32:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0596a8732aadbc8704f74fca2d9a1a5a769d11c968c46103f313b03d4d5cd68`  
		Last Modified: Thu, 21 Jan 2021 07:22:49 GMT  
		Size: 4.8 MB (4820293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbda91611b700613684e2b08b7cb4c1ce1b58c152f34838d51f2b320ceef983`  
		Last Modified: Thu, 21 Jan 2021 07:22:48 GMT  
		Size: 14.7 KB (14744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2b1318bd99b208ca1a2d36788e661df11ae80e5a774b26095bd70e517a8873`  
		Last Modified: Thu, 21 Jan 2021 07:22:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a247eee41c59c7799a7f9b83a86a04c4be4fb946d8b463b5f1f12b52b36fb`  
		Last Modified: Thu, 21 Jan 2021 07:23:36 GMT  
		Size: 176.0 MB (176022535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff9c81e12c5a66cd90daa8379fbca97b6a27b3005b29c5a698d1b6ef8ce185a`  
		Last Modified: Thu, 21 Jan 2021 07:22:48 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90772b1d03ef4da83d907f82d13c25d9fe179700a20e33eca675151614e93ed`  
		Last Modified: Thu, 21 Jan 2021 07:23:59 GMT  
		Size: 46.0 MB (45952777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c2f93aee64d6c527b1b8dc673cf673c919d853ab95ed477c8c6474b328d66`  
		Last Modified: Thu, 21 Jan 2021 07:23:46 GMT  
		Size: 274.7 KB (274656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e43589f2444624dc3dc7629a4e77bf104aace7fd4d90cd183cf2fa6591cc9`  
		Last Modified: Thu, 21 Jan 2021 07:24:02 GMT  
		Size: 57.3 MB (57298136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302148fb6beb83a18076f49ecb9781f8043db1b7a15af6c4d63361af80395222`  
		Last Modified: Thu, 21 Jan 2021 07:24:20 GMT  
		Size: 20.5 MB (20518249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
