## `ros:kinetic-robot`

```console
$ docker pull ros@sha256:4fee248b2e54e8f4d64bdc95ed01e1f7c2ee7eb4ec00a450a8dd9079958d37ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:82d48aad891af810d59a8f4af6379bd470560a13777eb7dcdde6890b59d3b719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386563619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d0ebd6f1ec59bcef29d0f48875f2096119090eff72f267cad26d75684d9fd3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:39:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:39:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 May 2021 21:39:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 May 2021 21:39:28 GMT
ENV LANG=C.UTF-8
# Wed, 19 May 2021 21:39:28 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 May 2021 21:39:28 GMT
ENV ROS_DISTRO=kinetic
# Wed, 19 May 2021 21:42:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:42:17 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 19 May 2021 21:42:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 May 2021 21:42:17 GMT
CMD ["bash"]
# Wed, 19 May 2021 21:42:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:42:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 19 May 2021 21:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:44:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14684ba412c39757a989fb7fe7e1858ffaecf276e3190ccd4765dabe7a1e8b11`  
		Last Modified: Wed, 19 May 2021 22:09:00 GMT  
		Size: 5.4 MB (5364316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d57d18c871aa3698dca1c280246f6e78f80e39a8c306763750d9fdce93efff`  
		Last Modified: Wed, 19 May 2021 22:09:00 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea861d8af8441bf794d8e6e8770d22b11cec75699560edff78932dce34e29a83`  
		Last Modified: Wed, 19 May 2021 22:08:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39413ca8ec49abf567b8c4497755073cb268ea3568fbe548b86f454849e3566d`  
		Last Modified: Wed, 19 May 2021 22:09:30 GMT  
		Size: 192.1 MB (192075126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3d8fde9915f7333a8aa902f390231c5576b7f801aff8f872367f5531572170`  
		Last Modified: Wed, 19 May 2021 22:08:59 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da38743f7f0589daee248db97589a070b938c027b9759bcc15c4106da225b0c1`  
		Last Modified: Wed, 19 May 2021 22:09:50 GMT  
		Size: 57.3 MB (57252738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e211bc1889df4ae714743757913cf5a0224dcbf36913330f42e26e09a904a`  
		Last Modified: Wed, 19 May 2021 22:09:41 GMT  
		Size: 291.4 KB (291407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cb1b82e308266626f8151c9d9590de87e82cfc2e423fade7cab95840290d76`  
		Last Modified: Wed, 19 May 2021 22:09:52 GMT  
		Size: 63.6 MB (63577704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda506da9f33e3aec35a7062b4b0864f9707bb54b6b167f06a3781a5cf9759f3`  
		Last Modified: Wed, 19 May 2021 22:10:10 GMT  
		Size: 21.5 MB (21523838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:aedcbd45359d10123fb6ecb5c17454e22f2d9ec0761932fda582d322f89b67fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335874311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bb6ff28337f192660fed573711ed0d51f13df2cc7011a14d6e47cebfd4a4fe`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 May 2021 17:01:40 GMT
ADD file:7e5c1f0262200ed290a61913d7f2c3b2b064c9b02aa1a55a818e38ab1316bbda in / 
# Wed, 26 May 2021 17:01:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 17:01:41 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 17:01:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 17:01:42 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 23:52:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 23:52:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 26 May 2021 23:52:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 26 May 2021 23:52:36 GMT
ENV LANG=C.UTF-8
# Wed, 26 May 2021 23:52:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 26 May 2021 23:52:37 GMT
ENV ROS_DISTRO=kinetic
# Wed, 26 May 2021 23:54:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 23:54:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 26 May 2021 23:54:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 26 May 2021 23:54:21 GMT
CMD ["bash"]
# Wed, 26 May 2021 23:54:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 23:55:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 26 May 2021 23:55:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 23:56:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae1370da0037e05eb3f24cd486c49ee3a450840763c7d31deef8274cb9abfd86`  
		Last Modified: Wed, 19 May 2021 20:24:51 GMT  
		Size: 40.3 MB (40292258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f08183c6e31c7e342a25706e54f9869aaf760990cb4a4ccbd4ed8aa917076c`  
		Last Modified: Wed, 26 May 2021 17:05:29 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5e978cf38433440cb631931ba431ef9da5d6e3ee162ca67891562db1df11af`  
		Last Modified: Wed, 26 May 2021 17:05:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4087b5e6a0394da1cbb5e8e721ff4d4cb511d79e6a83e7e1d84ed9352de6aac0`  
		Last Modified: Wed, 26 May 2021 17:05:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faccb4c2f61c169e577fcfdc727151dd9b03ec93da6e0fca01674d95cc322f`  
		Last Modified: Thu, 27 May 2021 00:21:41 GMT  
		Size: 4.6 MB (4615749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f6e9c01108a0f8f16fd0ce8d6c5a20f0852da78cb8365cd092def0bb6852f8`  
		Last Modified: Thu, 27 May 2021 00:21:39 GMT  
		Size: 14.7 KB (14745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a02f61386a0196c1c99f7458202856ace3934e6b5d5cb394e079db5363f345a`  
		Last Modified: Thu, 27 May 2021 00:21:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb01c41b95a6205f484a9dc3c089458d5e38b1707af7b3f01135f72bc7b93ab`  
		Last Modified: Thu, 27 May 2021 00:22:38 GMT  
		Size: 172.0 MB (171977161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca5fd0bb4c103d17b24eb900b0d32c3e9fcc35ca9976e420e5e5f648b68f569`  
		Last Modified: Thu, 27 May 2021 00:21:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b931b76ac16783f6be28c0e73dbae05bf557cbd1acdd1b3824d93ff331d8da`  
		Last Modified: Thu, 27 May 2021 00:23:10 GMT  
		Size: 42.9 MB (42897531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a0c12af0fba17c81bc294ea59a50b841fbb2b2ebc15cce1855fbeca4f281b0`  
		Last Modified: Thu, 27 May 2021 00:22:53 GMT  
		Size: 292.4 KB (292351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb3bf8d0b01a641a227a194ab47bf62aac3b549bd1cdac0608b9c9933f0f72d`  
		Last Modified: Thu, 27 May 2021 00:23:13 GMT  
		Size: 55.5 MB (55503489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7784c809a7e7a5c02c06e8d572c7ed09ffd6ba9c3dbeb16859a51db96f9d487b`  
		Last Modified: Thu, 27 May 2021 00:23:43 GMT  
		Size: 20.3 MB (20279075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2e75416d05414cbac158a1b43f815dae02dc2a9af97d4e04d1daf6acaf718444
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345942899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5453577db089496612fb35e139957c89dddc5557b88ca20ecdff4ddf681d0de`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:13:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:13:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 24 Apr 2021 00:13:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 24 Apr 2021 00:13:29 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 00:13:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 24 Apr 2021 00:13:31 GMT
ENV ROS_DISTRO=kinetic
# Sat, 24 Apr 2021 00:16:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:16:17 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 24 Apr 2021 00:16:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 24 Apr 2021 00:16:20 GMT
CMD ["bash"]
# Sat, 24 Apr 2021 00:17:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 24 Apr 2021 00:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:19:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef091df1ad3b49c777e51fcbdbef24b7a792d400584b31ffd16e771e1c09d7c9`  
		Last Modified: Sat, 24 Apr 2021 01:17:48 GMT  
		Size: 4.8 MB (4820634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dce1815ff82daa6b03af2100a095b9a5c3e2dfbd30442adfbe66a06ee9df5e5`  
		Last Modified: Sat, 24 Apr 2021 01:17:45 GMT  
		Size: 14.7 KB (14749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442c97bda99730a3a0034634612cfb5a799e8ccb1666e3f834a87699b974ec6c`  
		Last Modified: Sat, 24 Apr 2021 01:17:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf5408c0eb281fed7aa611c1331b0f4151887b838d7c45baa1657da2029aaaa`  
		Last Modified: Sat, 24 Apr 2021 01:19:33 GMT  
		Size: 176.0 MB (176021723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88cff5bdb08e16f518885da7949f063f4bdeb59f313bcb790922e7a60899df6`  
		Last Modified: Sat, 24 Apr 2021 01:17:45 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227e3d5739d14ea70647c8f71a41062e3538d6353b8f0a2efc88df369bdcc49b`  
		Last Modified: Sat, 24 Apr 2021 01:20:02 GMT  
		Size: 46.0 MB (45953079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be931fbac577bd32681c67f33ac30f6f43f8e773306787d5ad5195af28017d2`  
		Last Modified: Sat, 24 Apr 2021 01:19:43 GMT  
		Size: 280.2 KB (280211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e0f2ef7eabb94ba855a03a7217873d5eff015bd51b5297c05c4c3e1fc82cbb`  
		Last Modified: Sat, 24 Apr 2021 01:20:09 GMT  
		Size: 57.3 MB (57297623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f90af7701137c7100d35bcdc4da1dccf43bfb85d39e416f535ac7473a43b511`  
		Last Modified: Sat, 24 Apr 2021 01:20:33 GMT  
		Size: 20.5 MB (20526212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
