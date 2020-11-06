## `ros:kinetic-ros-core`

```console
$ docker pull ros@sha256:34a79032d4d019da17862e3f1a56e5678e93c9a0214e674afb25acb6ba467673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:74a52a63d935c56715c33cf3f6731997cc3f1370192a53e9e7fdcd5d7963cf0e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238336979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72703e0ea45bd608252f1a4b19137e945a220a6a74ab8b1ce6014429c7418073`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Oct 2020 17:33:08 GMT
ADD file:c1f3147c7b6710af5affd417ff822ee28df872d716003858d3d2e23d2277c981 in / 
# Fri, 23 Oct 2020 17:33:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:33:09 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 17:33:10 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:33:10 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 19:31:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 19:31:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 23 Oct 2020 19:31:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 23 Oct 2020 19:31:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 Oct 2020 19:31:13 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 Oct 2020 19:31:14 GMT
ENV ROS_DISTRO=kinetic
# Fri, 23 Oct 2020 19:33:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 19:33:16 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 23 Oct 2020 19:33:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 Oct 2020 19:33:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2c11b7cecaa5d3e2a57e290921ababbfb8572b549015168d4cbd91c340d2c566`  
		Last Modified: Wed, 14 Oct 2020 13:20:30 GMT  
		Size: 45.8 MB (45825714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04637fa562525a9366f00e8f4b08d04a347bded1ee513738451ef9d42b4dfc4e`  
		Last Modified: Fri, 23 Oct 2020 17:33:48 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6af23a0f38c4a6511147d2a9dc06a07a7afa0669000cb62720c7eafe031ae`  
		Last Modified: Fri, 23 Oct 2020 17:33:49 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a424de92ad71639c5cabadcdab0493e4067eb2f9cf109ffef40db178349238`  
		Last Modified: Fri, 23 Oct 2020 17:33:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6506cb466c9caaf79d9099a213fd08adcba6f018cd8360f20c05919d8a12fae1`  
		Last Modified: Fri, 23 Oct 2020 19:54:17 GMT  
		Size: 5.4 MB (5362322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb38ec3e7afd32045ced91202a93a356861f16a3e976adfdd92f79b3a5675c`  
		Last Modified: Fri, 23 Oct 2020 19:54:14 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67b35dcd31ec1c224bcbae1f0b564049e4cc416771f17352a0ce2a19c1c2feb`  
		Last Modified: Fri, 23 Oct 2020 19:54:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210b782ec4e83a272258b58e4cc1dca9d9da861b0f15f0bf000821cb56972000`  
		Last Modified: Fri, 23 Oct 2020 19:55:01 GMT  
		Size: 187.1 MB (187132234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff55477f12b851aca47ff841b7b4b4d03002c8e5a4eefdc02a54f0bc97dc682c`  
		Last Modified: Fri, 23 Oct 2020 19:54:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:631382e4269308de7282ec0a7d4c596e08659072e6409f3c252a86271ddc8463
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212547342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa63fe9fbc1927b9f0f68c0a651875d8c78fa2963bfab40b0d203d6ca7b5028`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Oct 2020 18:17:14 GMT
ADD file:5c0d6a48e839c912491edae36f7465b9efe445d4a5ee58861fee1ccd424890ec in / 
# Fri, 23 Oct 2020 18:17:18 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:17:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:17:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:17:22 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 18:54:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:54:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 23 Oct 2020 18:54:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 23 Oct 2020 18:54:28 GMT
ENV LANG=C.UTF-8
# Fri, 23 Oct 2020 18:54:29 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 Oct 2020 18:54:29 GMT
ENV ROS_DISTRO=kinetic
# Fri, 23 Oct 2020 18:56:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:56:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 23 Oct 2020 18:56:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 Oct 2020 18:56:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:183a558dd6745131430d26859b5c0b308384044df34cc35f69c406432c022d3a`  
		Last Modified: Mon, 19 Oct 2020 17:04:41 GMT  
		Size: 39.9 MB (39897338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c9cb164a2e061f22d5b157a0e96dcd278984851436ba61b9eeafd17cd0a8e4`  
		Last Modified: Fri, 23 Oct 2020 18:18:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae3963d7d3f6c0b3ca836f488586277a576d3477f7976e185bbbc4b79fea203`  
		Last Modified: Fri, 23 Oct 2020 18:18:14 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da982e99c6f88739b993432f872f7b916b7f2c3d185cadf69c4ebbf511964e2`  
		Last Modified: Fri, 23 Oct 2020 18:18:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadf93f7cf1c717a7e93b88e644ef1c651835d4214ad288e5a4b8e409355e9a6`  
		Last Modified: Fri, 23 Oct 2020 19:15:27 GMT  
		Size: 4.6 MB (4614846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9133d92cbd0a86346bbabc16b7efeef8edcf85420898da7ebbab948e3a312fda`  
		Last Modified: Fri, 23 Oct 2020 19:15:26 GMT  
		Size: 14.7 KB (14744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed55684850ac54be387a7869f7aa3ec3f663d7db8097700ef42817c7524c1a2b`  
		Last Modified: Fri, 23 Oct 2020 19:15:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65972f4a630f6d2690c798e849ad315dc4f536ee2718212a6fa6da3d054ce465`  
		Last Modified: Fri, 23 Oct 2020 19:16:28 GMT  
		Size: 168.0 MB (168018463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce33d191d74030c32fcfceb9ce1b0fe70b43d34510fafd9ee77220686d35c94`  
		Last Modified: Fri, 23 Oct 2020 19:15:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6e367aa422b2309a1f303c9740ab1b973d234023293a0f2c30083a6722dc492d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223328998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc990d8f04b642f7f19f33b7d456808ec8019a1e0d586f17285a02fe56de1041`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Oct 2020 18:20:23 GMT
ADD file:5611ef5e4a339aa780380c12e06ca701cb7f2392b12aa8a481278806abc2a17c in / 
# Fri, 23 Oct 2020 18:20:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 18:20:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:20:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 18:20:31 GMT
CMD ["/bin/bash"]
# Fri, 06 Nov 2020 03:07:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 03:07:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 06 Nov 2020 03:07:52 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 06 Nov 2020 03:07:53 GMT
ENV LANG=C.UTF-8
# Fri, 06 Nov 2020 03:07:53 GMT
ENV LC_ALL=C.UTF-8
# Fri, 06 Nov 2020 03:07:54 GMT
ENV ROS_DISTRO=kinetic
# Fri, 06 Nov 2020 03:10:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 03:10:31 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 06 Nov 2020 03:10:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 06 Nov 2020 03:10:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d2a73c0bcd690b0c96f2917b855b4499d5b9f1c49f92a39f32b6840fa49fe74e`  
		Last Modified: Wed, 14 Oct 2020 15:58:06 GMT  
		Size: 40.8 MB (40818920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ee81a9e6847a65206218a3b456bc136f8e38689ebb56cc9877d597a41bb371`  
		Last Modified: Fri, 23 Oct 2020 18:21:28 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f489a564b05761b210f9a87ff4b2b1e232cdd89eaaffd5e27bf658d0956b1d57`  
		Last Modified: Fri, 23 Oct 2020 18:21:26 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c25910825cfb7d71977bb81419f287002fb712d755ec89fb9fb9f120e30936`  
		Last Modified: Fri, 23 Oct 2020 18:21:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfc1090d496f6d9e58885af23345826a7aed6c1a1dc56fa111acb409ef673be`  
		Last Modified: Fri, 06 Nov 2020 03:19:56 GMT  
		Size: 4.8 MB (4819918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094d324d33448a883f9d8a3bb4967841e7fdaf021284fe462221d78b8310507c`  
		Last Modified: Fri, 06 Nov 2020 03:19:55 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1bf9f0c81f295adcf4feb522a86d41beaeb62ebe24014cb86b38d8158c32257`  
		Last Modified: Fri, 06 Nov 2020 03:19:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7f2fefe258569eee0005cc03c2fa1af65e4a1d6276375ca1d45f43e7a9eb3`  
		Last Modified: Fri, 06 Nov 2020 03:20:48 GMT  
		Size: 177.7 MB (177673504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f37a4e5c2cacf2cebcea210108485a903a3eda0a1484dc4f73e943be5998d8`  
		Last Modified: Fri, 06 Nov 2020 03:19:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
