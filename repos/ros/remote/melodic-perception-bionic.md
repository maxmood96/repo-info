## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:a617c3a947fb71a67b4e20d4ed09e1c97f479bde213aa8c301de665c6afde5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:46f10d430df6b2948638a77f4509c53b2db38d7488467f33e7bcfb9beb0c9e1c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **787.1 MB (787070531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d727ef1a06afb7a5273f3cfe378096e1c8aa14a86da35cc7bd372d51d65274`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:17:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:18:00 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:18:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 20 Mar 2020 20:18:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 20 Mar 2020 20:18:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:18:40 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2020 20:18:40 GMT
ENV LC_ALL=C.UTF-8
# Fri, 20 Mar 2020 20:18:40 GMT
ENV ROS_DISTRO=melodic
# Fri, 20 Mar 2020 20:18:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 20 Mar 2020 20:21:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:21:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 20 Mar 2020 20:21:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 20 Mar 2020 20:21:24 GMT
CMD ["bash"]
# Fri, 20 Mar 2020 20:22:28 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 20:28:40 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97510123400e649cc5a98136827c7d21af815d5d349e28a7ab4aa81822936de7`  
		Last Modified: Fri, 20 Mar 2020 20:33:10 GMT  
		Size: 838.2 KB (838197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c7a500c430cd0ee6521049692da24c28361089e2a38a5d667d05bd89f2f37`  
		Last Modified: Fri, 20 Mar 2020 20:33:11 GMT  
		Size: 6.8 MB (6780648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125f6604a24ccf37e970782122cd9555537f23610aabbdf6af720a702f49ba9a`  
		Last Modified: Fri, 20 Mar 2020 20:33:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0c8c12af7d1e4fb4f872bc3101021978d381a410df03445b8e523c1a26d479`  
		Last Modified: Fri, 20 Mar 2020 20:33:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3aff419fe252900a06808d6e28988f189072b2faef1436540af08b5630d9ab`  
		Last Modified: Fri, 20 Mar 2020 20:33:21 GMT  
		Size: 55.1 MB (55076910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b76fd88f837aa07fe3b6dfee50e685dd3d8ef1a41cb1a55f148d72e0e9f6a90`  
		Last Modified: Fri, 20 Mar 2020 20:33:08 GMT  
		Size: 437.1 KB (437144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d1d2ac404c52c3621e8e3b4cbeb234494497a3fa90e44e0dd802015652bb6d`  
		Last Modified: Fri, 20 Mar 2020 20:33:52 GMT  
		Size: 274.1 MB (274075154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f813601d535c9783da555b4808e71f7a411e1ef4578bfde672c9fe598f3f63`  
		Last Modified: Fri, 20 Mar 2020 20:33:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873da7bcc558a66c3691fd349a02284ac8d9667878d0a34c2fae9cfe5fdc4940`  
		Last Modified: Fri, 20 Mar 2020 20:34:10 GMT  
		Size: 72.9 MB (72923972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8c7790ed1653a12fc56b42d3a5a94fddc6a88a01070f713ab8455691a01cc7`  
		Last Modified: Fri, 20 Mar 2020 20:35:32 GMT  
		Size: 350.2 MB (350209700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:beaab77e3c0f705d75c67f1fe46e55b59731b9415ea1e2baa193de75ed745a33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.7 MB (685668096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfcd813377d0a1f36481591e0f64a03f91592b78c19ed33a7a6a414aac9ea8d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:58:33 GMT
ADD file:9a073d6996d363ef5ffe4f4e7d334e834af1d84a1bb0b1e02145cce2931bc8c9 in / 
# Fri, 20 Mar 2020 18:58:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:58:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:58:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:58:39 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:32:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:51 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 20 Mar 2020 19:32:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 20 Mar 2020 19:33:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:34:00 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2020 19:34:00 GMT
ENV LC_ALL=C.UTF-8
# Fri, 20 Mar 2020 19:34:01 GMT
ENV ROS_DISTRO=melodic
# Fri, 20 Mar 2020 19:34:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 20 Mar 2020 19:37:11 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:37:17 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 20 Mar 2020 19:37:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 20 Mar 2020 19:37:20 GMT
CMD ["bash"]
# Fri, 20 Mar 2020 19:38:33 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:44:05 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ca414fffae684c882959a9839b54c358a452fd0f39ec47c521f2ba19a8247f4`  
		Last Modified: Mon, 16 Mar 2020 15:39:00 GMT  
		Size: 22.3 MB (22275458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4494bf6d26aa26ddb62f91d669167b4129fe8cf25d2673b5c31af555e5cf9`  
		Last Modified: Fri, 20 Mar 2020 19:00:15 GMT  
		Size: 35.5 KB (35470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7001ff2516d9cbe17e7f01a2dada38b32eb61827dd53372bf3d015ea56a994c8`  
		Last Modified: Fri, 20 Mar 2020 19:00:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b800647044909d03feb20339a3053ce366d2170f399d907fb678d89746512a9a`  
		Last Modified: Fri, 20 Mar 2020 19:00:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619c0fe278b09907dee8f50ff003820a3521a92e20706876a158cf6fb3082c21`  
		Last Modified: Fri, 20 Mar 2020 19:52:58 GMT  
		Size: 838.0 KB (838031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bee2f26fbf5051222a87e609c9e665175919d7195998962763ddad54ece5e3`  
		Last Modified: Fri, 20 Mar 2020 19:52:59 GMT  
		Size: 5.6 MB (5630984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322df2c534ef56d80462b9c55c5d142b76c76222058745db367d921947a66125`  
		Last Modified: Fri, 20 Mar 2020 19:52:57 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52e697d8b3d43bb1c2fc98e68f573e27afbb9bbceaac1b2c6d78c981b7751f1`  
		Last Modified: Fri, 20 Mar 2020 19:52:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26e967de1f3647dc80bf1ce51a24ed0e33f9f9c6ea2bc06afbb5cbdef1aeba4`  
		Last Modified: Fri, 20 Mar 2020 19:53:14 GMT  
		Size: 50.1 MB (50113323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df6019cf01cbbe1d180f65b9ce63c7358859568a637b1e1e255111772615df4`  
		Last Modified: Fri, 20 Mar 2020 19:52:55 GMT  
		Size: 437.1 KB (437061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3492993f5cc48a187c5995cc9cdd0e1c40f3808cc92668cf41e81eac90c7120`  
		Last Modified: Fri, 20 Mar 2020 19:54:03 GMT  
		Size: 243.3 MB (243293257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee1a2c9e211604e4cae90b1aaad109ff56096287360a4471ed42ff3badd1168`  
		Last Modified: Fri, 20 Mar 2020 19:52:55 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5c6809b12b8b77e7f83dbf7b8c022834619c571ed87896114d67584295442c`  
		Last Modified: Fri, 20 Mar 2020 19:54:32 GMT  
		Size: 62.9 MB (62881320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cfde474e8a1bf6a02d93eb0fd1ee521f5e5ffbadf56e8caffde06f2cfdb280`  
		Last Modified: Fri, 20 Mar 2020 19:56:31 GMT  
		Size: 300.2 MB (300160315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9f52e623a8e05d010bbbfcaa8100422b6f893c1136e23b125cf2820dd76c6050
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.8 MB (744767781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca637f90f1810023eb208f9b4afb9d5ae56b1dff3ce94682f5e0069731c0b22b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 20 Mar 2020 18:43:33 GMT
ADD file:e4214b65d372c2f971e6544f69c465e8b1ba82290276558036047179a02ba9e3 in / 
# Fri, 20 Mar 2020 18:43:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:43:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:43:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:43:39 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:36:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:36:51 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:36:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 20 Mar 2020 19:36:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 20 Mar 2020 19:38:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2020 19:38:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 20 Mar 2020 19:38:08 GMT
ENV ROS_DISTRO=melodic
# Fri, 20 Mar 2020 19:38:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 20 Mar 2020 19:41:14 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:41:22 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 20 Mar 2020 19:41:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 20 Mar 2020 19:41:24 GMT
CMD ["bash"]
# Fri, 20 Mar 2020 19:42:48 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:48:07 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2f61026a351316126bfad6f6cac3971b3b3e928b126ac53026bb4263459d2ff`  
		Last Modified: Mon, 16 Mar 2020 15:39:01 GMT  
		Size: 23.7 MB (23720219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538fb30c42c023ad64c0e31ce3cb02e3c4150f9ac944a46d3386b8212b80043`  
		Last Modified: Fri, 20 Mar 2020 18:45:00 GMT  
		Size: 35.2 KB (35206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b05810781a3c493e08dc6e2c9b9553244f8f86248f7d709a50becbac344234`  
		Last Modified: Fri, 20 Mar 2020 18:45:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0180a33352d6b41ad6ca5fac27544fb3c8c7cb69e67dc30bf9584b49cd3b3938`  
		Last Modified: Fri, 20 Mar 2020 18:45:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20dccc73d95622df55ec7a2fc56f5f8b18792bc5d60888e80ad8222d43bb83b`  
		Last Modified: Fri, 20 Mar 2020 19:57:02 GMT  
		Size: 837.8 KB (837781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d0aefc0ebc82e46a6b97bf8e5bcb60b4dfed1d8017ca94c1b961593e22af1`  
		Last Modified: Fri, 20 Mar 2020 19:57:03 GMT  
		Size: 6.1 MB (6097090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63df2f9941ec660b42531ae3d9964fcd212917446056aefc986ade73972cde1`  
		Last Modified: Fri, 20 Mar 2020 19:57:01 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1311879655db08a0f21f490fdaa81b2845d95b6a8b83946dae2426122812a4e`  
		Last Modified: Fri, 20 Mar 2020 19:56:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f0bbe00a4e5cf78a8e7434ca7bfd4f4670ea860bfa67d8de8823354020be21`  
		Last Modified: Fri, 20 Mar 2020 19:57:17 GMT  
		Size: 52.9 MB (52924504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e88a3c258c9cf62ae6d061f23045603152696570ba38933dba4158fa028128`  
		Last Modified: Fri, 20 Mar 2020 19:57:00 GMT  
		Size: 437.2 KB (437203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e71c25c0b0c107d0d09b96b6944fce8970bae844a470118168f670fe71e1854`  
		Last Modified: Fri, 20 Mar 2020 19:58:11 GMT  
		Size: 262.3 MB (262297391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f7c1caf46c87497d081f899e20016ecd344dce1a466dc8ef7cbb67a116ad94`  
		Last Modified: Fri, 20 Mar 2020 19:56:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e1a89ac73ae3cc5e7ba02ad2771de149900a08ab359b13478c4aae0bde22c4`  
		Last Modified: Fri, 20 Mar 2020 19:58:37 GMT  
		Size: 65.6 MB (65558366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c46bd5bad8c72f0c526439835784693c32881a09e5b53c64ffd0ad1f2546dd0`  
		Last Modified: Fri, 20 Mar 2020 20:00:37 GMT  
		Size: 332.9 MB (332857138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
