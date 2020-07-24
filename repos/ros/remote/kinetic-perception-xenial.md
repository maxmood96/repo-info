## `ros:kinetic-perception-xenial`

```console
$ docker pull ros@sha256:0cfd946b61bf708555c619305d06faa826c528cef159138f0cc9403192925724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-perception-xenial` - linux; amd64

```console
$ docker pull ros@sha256:1f685b3c3d98419dbe6de31db1668e5f408172fc53005f310b2c811aa201302e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.3 MB (687280001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399ed45d41c52cd9a2801512356e45f96a8a78dd580cb9a9c7b7b23b73b8d6c4`
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
# Tue, 07 Jul 2020 00:33:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:33:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jul 2020 00:34:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:38:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7cdee4b700a36a8d86df4110ecc0f257303aadacc2a9e9da7711ff8a702a3170`  
		Last Modified: Tue, 07 Jul 2020 01:16:40 GMT  
		Size: 57.2 MB (57243272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7c4e728abb2e9fca68e95cf1daf03828cd905dca2708ab243cf884cd9b4837`  
		Last Modified: Tue, 07 Jul 2020 01:16:26 GMT  
		Size: 260.4 KB (260396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29914de82b70e0992158f3b0df7f217bbb798b7264239204d06b45f43a4153ff`  
		Last Modified: Tue, 07 Jul 2020 01:16:58 GMT  
		Size: 63.6 MB (63573248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d5c611e2355e554cf9c89f7e906cfa378d5a2642b427d4741f5a7b14fd0ad0`  
		Last Modified: Tue, 07 Jul 2020 01:18:20 GMT  
		Size: 324.4 MB (324434512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-perception-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:c84b354122506a489f64e4a0a43b979cffd05ee822286e92e75de9a2164c7975
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.5 MB (576494829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c33436f5f455e0fcc285c7979efc434b53b8f4902bf61f7806526abe5035016`
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
# Fri, 24 Jul 2020 16:32:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:32:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 16:35:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:44:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a384e82031356697089c00f899e83ddb238c3fbac71c705ae2d22594475a56c2`  
		Last Modified: Fri, 24 Jul 2020 17:32:24 GMT  
		Size: 42.9 MB (42892739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef6d4c2cad78f9c307a56b3bf01cdda2a3805d14395177772bef9d69f701c5f`  
		Last Modified: Fri, 24 Jul 2020 17:32:09 GMT  
		Size: 261.5 KB (261547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1c8804339dd85cac8deacdf91a94f05fe7576406d4de7060780235517e2236`  
		Last Modified: Fri, 24 Jul 2020 17:32:27 GMT  
		Size: 55.5 MB (55501374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3602abe63c1ec78df19858671d337f3902d673a31076beda4b128016f4ec14`  
		Last Modified: Fri, 24 Jul 2020 17:34:32 GMT  
		Size: 266.2 MB (266184004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-perception-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:277e82f4189506ee0a03c5ac7879af2f5ea0f73050859499a5e51e21dbdbbc05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600142912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edce86c3560da2f6812f3154eb930b805ac5e4f14a626facd1294cb5d17b43e7`
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
# Fri, 24 Jul 2020 16:37:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:38:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 16:40:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:45:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7882cb49935fa348f0e3b473d812599196078588f2ce8478a4a3959bd6c4ec04`  
		Last Modified: Fri, 24 Jul 2020 17:40:56 GMT  
		Size: 46.0 MB (45953072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd7eff6b60a1b27641649ad49d8a67a7db88cbd74871b4e32b1c8280d7f561d`  
		Last Modified: Fri, 24 Jul 2020 17:40:32 GMT  
		Size: 261.6 KB (261629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e031cb5a1d31714b1b1f232b00b326ef1cf62133cea749e67154d808097533f`  
		Last Modified: Fri, 24 Jul 2020 17:41:04 GMT  
		Size: 57.3 MB (57286641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f728b1a8a3b623f496cc939ba1bfbf75160e446b0ca9ae822b08b054fa84ef3`  
		Last Modified: Fri, 24 Jul 2020 17:43:37 GMT  
		Size: 275.8 MB (275771871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
