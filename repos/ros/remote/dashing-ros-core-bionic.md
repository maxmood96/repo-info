## `ros:dashing-ros-core-bionic`

```console
$ docker pull ros@sha256:ce8885a8a65e0879446c1409ddf56373754deda317e2798f31e75fa7aba63fd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:dashing-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:10f02108f8909997eb3781e7b250cd616499461d570c140691a9a5690a12b606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210820230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a04a7d9b80268944a266cb897717e63b399658845af7e16afe0f148ed45de27`
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
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/dashing/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=dashing
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
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

### `ros:dashing-ros-core-bionic` - unknown; unknown

```console
$ docker pull ros@sha256:32a28876fff94b0781be628c863f25ff3dfe25cce4757105fa926d046b67b9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18203607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736a94d0ac322ccf81b7f7fc06988c94fb371a0d62db233fdf66f89b091df5a2`

```dockerfile
```

-	Layers:
	-	`sha256:4f22a0bc2479633387d60b2f2ea8c793e78c8742a997dabb11575d78cacba642`  
		Last Modified: Sat, 07 Jun 2025 01:18:36 GMT  
		Size: 18.2 MB (18188441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fe8caa2e0bd7168591ed9c2dd8fe99f212c89585bae502ab4518b2dc7b15fa7`  
		Last Modified: Sat, 07 Jun 2025 01:18:38 GMT  
		Size: 15.2 KB (15166 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:dashing-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:6308182fd8540b53a53fa93a0bf4e151e82d33e8f395fcb5111761643283a38e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180808465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608b9589e436179502c3481483065844435a81ec6b361c5b62ded3cfcaff6f9f`
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

### `ros:dashing-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:278754957523b1b86f31b8a4f482a9954edaacd43452ee2e1740a9d77cd7201f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193076466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d57075118e6c6bf89d896e42e1a5b7c00a17897862b9311de3836eba49aefd`
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
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/dashing/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=dashing
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
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

### `ros:dashing-ros-core-bionic` - unknown; unknown

```console
$ docker pull ros@sha256:125b9430133a84ec65f39750a094230ad2715dc0a3248278e750de0429c20b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17235639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0818725df120cd803bc760fcdf10435ccf87fedb018d10e0412c9d21e52d01b0`

```dockerfile
```

-	Layers:
	-	`sha256:69eb7a122ffa29f53574acb02d6a2337f22abdfabef1a192834ab57a9fd5079d`  
		Last Modified: Sat, 07 Jun 2025 01:18:53 GMT  
		Size: 17.2 MB (17220339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f76a9d55ffbfc6d2c12cbf0f3ab40727b045d3c1d8e4b1ca09e8b8e4ada65d`  
		Last Modified: Sat, 07 Jun 2025 01:18:53 GMT  
		Size: 15.3 KB (15300 bytes)  
		MIME: application/vnd.in-toto+json
