## `ros:kinetic-ros-core-xenial`

```console
$ docker pull ros@sha256:fe6a9eced54b86bd2ced5cf5f45b917c89e950100525689b6810136bee332bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core-xenial` - linux; amd64

```console
$ docker pull ros@sha256:53fc2cdb0c5848239c4c3594968cb20571ca85c8419ae8dfc4effe149dd8f1a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241768573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b71052693d2d073eb72ecf99f2a390fe92ebea21bf577c1c30ebf10daddf7e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:30:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:30:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 00:30:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jul 2020 00:30:14 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jul 2020 00:30:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jul 2020 00:30:15 GMT
ENV ROS_DISTRO=kinetic
# Tue, 07 Jul 2020 00:32:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:32:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 07 Jul 2020 00:32:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jul 2020 00:32:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d6d7e7d876fdb59a936541ed124278c05f29167c9a0db737090efe8bfe53f8`  
		Last Modified: Tue, 07 Jul 2020 01:15:33 GMT  
		Size: 5.4 MB (5362055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83575d76825cf907d9fe86af9ff273d68d1c7d8e7028f7da59535488085ffe08`  
		Last Modified: Tue, 07 Jul 2020 01:15:32 GMT  
		Size: 14.7 KB (14745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33a894c36017b7e6661e1ce032ac236903bfd74dfa9efd9e5b854bf086ab30c`  
		Last Modified: Tue, 07 Jul 2020 01:15:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb5d4a90f6a0f0a26e7e991647798243e14d4c1b6f1c845c5d34881a72d0640`  
		Last Modified: Tue, 07 Jul 2020 01:16:18 GMT  
		Size: 192.0 MB (192015657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac20add01075f2102b672082d0c7bf56a68fa1d0fc5515cab555bd404bb7a3`  
		Last Modified: Tue, 07 Jul 2020 01:15:32 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:9a38f4a4a8542b91a902a59784a275ac3c1d4b3f32587399951ae380b9a7b420
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.7 MB (211655165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9786706289028e1037ce76a0c58e836b50569c46678ef60f03bef7c1250fcbb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:09:57 GMT
ADD file:c7836321aa9dc9832d8e14c042281f4a3525083619649e000d08159b6da79460 in / 
# Fri, 24 Jul 2020 16:10:21 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:11:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:11:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:11:59 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:25:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:25:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 16:25:34 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 16:25:44 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 16:25:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 16:25:51 GMT
ENV ROS_DISTRO=kinetic
# Fri, 24 Jul 2020 16:30:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:30:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Jul 2020 16:30:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 16:30:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:111f37a6818f459bbc8076c0f741a76111210d34c5738743f43dc1488cf91458`  
		Last Modified: Mon, 13 Jul 2020 15:55:00 GMT  
		Size: 39.0 MB (39022996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fa2e8f0d9a725920aa624702144baeaae474875e43f4515d9e69c2bddec4bf`  
		Last Modified: Fri, 24 Jul 2020 16:20:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c110f6a5721b4e19fdabed9edeb5446f52132952947cd7b409ac4d4e50b7dc02`  
		Last Modified: Fri, 24 Jul 2020 16:20:13 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07bd4b31471725e34aa841d95fec2e7425ac418ee0a0f69b6d5ca73c6a17c9e`  
		Last Modified: Fri, 24 Jul 2020 16:20:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c8cb740b420db49d2b9df4cc36d3a7547d77acc2cbeacf15151cb9b940c125`  
		Last Modified: Fri, 24 Jul 2020 17:30:30 GMT  
		Size: 4.6 MB (4615060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a0003531b818fd1c35748797bb0869f814fc0b99b51c56daf1b18098d835ac`  
		Last Modified: Fri, 24 Jul 2020 17:30:28 GMT  
		Size: 14.7 KB (14743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ed872f7d0b6ec64dc1d274b933a10aa128065ea067bdd9c3103e948db94b6d`  
		Last Modified: Fri, 24 Jul 2020 17:30:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db036ce8a45a21f6b3f6df19023dd48216e291a202f9073046646585139ebf`  
		Last Modified: Fri, 24 Jul 2020 17:31:58 GMT  
		Size: 168.0 MB (168000414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e3518cf7245e334ae0fbe802330fd68f7146b08830e2de8e2863667a77d8db`  
		Last Modified: Fri, 24 Jul 2020 17:30:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:49e75e63983f2000c326a2fd232503d21b617420db51e5643cab1ad83cbf4833
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220869699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a105d06660cd00920a5bdac53a5537a2a9a187d77241acbcae05c2be86a679`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:25:59 GMT
ADD file:d816988decfebf469e2b28b4858ce7d4a991a101957a43051324255fbe64c86e in / 
# Fri, 24 Jul 2020 16:26:14 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:26:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:26:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:26:27 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:31:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:31:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 16:31:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 16:31:10 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 16:31:11 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 16:31:12 GMT
ENV ROS_DISTRO=kinetic
# Fri, 24 Jul 2020 16:36:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:36:47 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Jul 2020 16:36:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 16:36:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f783735449ae0b09fb9e5ee128904f2f3131f6ba46fcf1350fb6a10f872866be`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 40.1 MB (40050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35a03aa6fbe0d9147b23501e6fa41d33cd4489470455008ddcbe201063d7b98`  
		Last Modified: Fri, 24 Jul 2020 16:27:47 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55e221892467d43fdd76b2b592c2fe46e1c69b08e0e9b94f2b383f38e681f65`  
		Last Modified: Fri, 24 Jul 2020 16:27:47 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a9069021914a77a3d51ffbff02ea5b8a200180601b2be52e9f98d31b6f1389`  
		Last Modified: Fri, 24 Jul 2020 16:27:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ac69f173003c8bf0c008eaef291209c10ae7cd840633b6dfa0c3351a3c19a`  
		Last Modified: Fri, 24 Jul 2020 17:38:25 GMT  
		Size: 4.8 MB (4820044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658dddd254b3a9732e5e0eff70e9f0c4ca573b2ffb9d7031fa9a89c1b99c518`  
		Last Modified: Fri, 24 Jul 2020 17:38:21 GMT  
		Size: 14.7 KB (14745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e008049660c6d8aae525a64b5fba4a4b918e212cc2548f8b1e35eb7a1cc35e41`  
		Last Modified: Fri, 24 Jul 2020 17:38:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b3f6f90a52db94535a8a10507e8b9981b17dddce080db1b8f558a66fdb497a`  
		Last Modified: Fri, 24 Jul 2020 17:40:19 GMT  
		Size: 176.0 MB (175982202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4782a0457e8a49bdd7b6d2f7935bf248fa8eb8dc68b418fdab6e7edccf157cb7`  
		Last Modified: Fri, 24 Jul 2020 17:38:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
