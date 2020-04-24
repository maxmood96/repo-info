## `ros:kinetic-ros-core-xenial`

```console
$ docker pull ros@sha256:9c18a26d06592c332ad93f46f9fb90db42ca557596b085767f00d17489aa5ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core-xenial` - linux; amd64

```console
$ docker pull ros@sha256:d1650303967a3ec3289039f7c66237adbe50bee8fe19cc794377923bb157830d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299803553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d665cc6b0a82859d377f77d0d57d2e5e1f18d8f1825059f890945ea0e372944`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 01:08:29 GMT
ADD file:4fe14d9555e739e4d006eecb273a2f4a53e6dbe93bd0db26d5f999168b5d4114 in / 
# Fri, 24 Apr 2020 01:08:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 01:08:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:08:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:08:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 20:46:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:46:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Apr 2020 20:46:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Apr 2020 20:47:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:47:18 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 20:47:18 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Apr 2020 20:47:18 GMT
ENV ROS_DISTRO=kinetic
# Fri, 24 Apr 2020 20:47:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Apr 2020 20:49:09 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 20:49:10 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Apr 2020 20:49:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Apr 2020 20:49:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e92ed755c008afc1863a616a5ba743b670c09c1698f7328f05591932452a425f`  
		Last Modified: Fri, 27 Mar 2020 14:20:10 GMT  
		Size: 44.2 MB (44247132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fd7cb1ff8f489cf082781b0e1fe0c13b840e20147e8fc8204b4592da7c2f70`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee690f2d57a128744cf4c5b52646ad0ba7a5af113d9d7e0e02b62c06d35fd14c`  
		Last Modified: Fri, 24 Apr 2020 01:09:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3366ec435596bed2563cc882ba47ec25df6be2b1027e3243e83589c667c1e`  
		Last Modified: Fri, 24 Apr 2020 01:09:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bc5fb3503cef1f5ff32b818035c1219faef0f8537b7ae31801418cc2c2f2a2`  
		Last Modified: Fri, 24 Apr 2020 21:10:22 GMT  
		Size: 6.9 MB (6936473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610e21ec5cdfbae18990f30735b7b9828a18edcb8c830fd254e12adcda8f33b9`  
		Last Modified: Fri, 24 Apr 2020 21:10:21 GMT  
		Size: 13.1 KB (13106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d26f628f675b503ffd3214c6f7f6bc9998ea6e58dcf5a6383668fb42ca3d12`  
		Last Modified: Fri, 24 Apr 2020 21:10:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7737f190310e82ece9e301a28dd3e5a41b4621d663a4b96ea3ace7b964e7656`  
		Last Modified: Fri, 24 Apr 2020 21:10:34 GMT  
		Size: 54.8 MB (54790036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec575ad79465df1013d0dbac2313c5ed95a9ee139ecf0aab9ff390e9fca20d4`  
		Last Modified: Fri, 24 Apr 2020 21:10:20 GMT  
		Size: 253.6 KB (253595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da84296616d772863d7fd73fd41703bd301e0c4ce55cb2b9a6fe3368d61bd582`  
		Last Modified: Fri, 24 Apr 2020 21:11:04 GMT  
		Size: 193.6 MB (193561245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e41803963b06568632321145bf5de5acf1b2ae55a102201855d136b24cc623d`  
		Last Modified: Fri, 24 Apr 2020 21:10:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:50db698e56119f91d42e86ef14182c4565199cf84d04c33fe55397e2c95275b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260200830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d004bd27a3c1c8c78412e8193fee25297354f13b2966da79affe30e1ff05d17`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 22:07:55 GMT
ADD file:baa32b9dff77005bab52997f1dcb9df3558abb0e2ef834cc2d09fd2f9b199f75 in / 
# Thu, 23 Apr 2020 22:07:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 22:08:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 22:08:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 22:08:03 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:30:05 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:30:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Apr 2020 11:30:10 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Apr 2020 11:31:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:31:21 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 11:31:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Apr 2020 11:31:23 GMT
ENV ROS_DISTRO=kinetic
# Fri, 24 Apr 2020 11:31:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Apr 2020 11:33:48 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:33:52 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Apr 2020 11:33:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Apr 2020 11:33:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:471714e6acf6feae8152818c3e754b9ca6a0bb98630e01ccc7f3a11b3c167d67`  
		Last Modified: Mon, 30 Mar 2020 15:50:01 GMT  
		Size: 38.9 MB (38921731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452137b54c197f3f182da5f3c8f8464b32e21e6023206fc84f1973bd7b5d6d0e`  
		Last Modified: Thu, 23 Apr 2020 22:08:50 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba3c36f61e095df847ba29ce216ff56b6cef111df85728fe0dee190fc49193d`  
		Last Modified: Thu, 23 Apr 2020 22:08:50 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414dfa5050bda9cc1932154a5ad6031f727ff248a9098137827aa48f60e11ceb`  
		Last Modified: Thu, 23 Apr 2020 22:08:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6b68f3d41b9f69a317613dc09fbb7bbd90e74a633d3d4cd82883740dc61f9`  
		Last Modified: Fri, 24 Apr 2020 11:58:34 GMT  
		Size: 5.7 MB (5700698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1b2a2b38a66d74db9685123dbd74d305072081e3be996b1bbc27dab42efc53`  
		Last Modified: Fri, 24 Apr 2020 11:58:33 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5984390cba2b35cadbc00adb04a91fc17112a1743ff6c761502f564457931e81`  
		Last Modified: Fri, 24 Apr 2020 11:58:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1480cbc19af5716cdd5cfb5933c0eedecae676e73c66da7a017cb9c911b93425`  
		Last Modified: Fri, 24 Apr 2020 11:58:49 GMT  
		Size: 50.4 MB (50352264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb115936c3a9df41806d09e9d15c9a2ba0ad819ad677ea1a99a79c617721e472`  
		Last Modified: Fri, 24 Apr 2020 11:58:31 GMT  
		Size: 253.6 KB (253596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3712e7c8e4bd80b089ebd8bf85b34aae8d3ee7701eeab9d09dc9afb172a46053`  
		Last Modified: Fri, 24 Apr 2020 11:59:21 GMT  
		Size: 165.0 MB (164957478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f481d9aac9ef6966403b693b4a07e5803633042543e7c49be213fe5ed7be7af`  
		Last Modified: Fri, 24 Apr 2020 11:58:31 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e5b950967d66770feb66eb4d67c083756551f0b457218dac5abf6934de2eab78
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272527911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0505c253b7a0bf0220b5c35ef4a88d5f04b8525ebc36f3bfac0cd89e24ca9fea`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 15:07:24 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:07:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Apr 2020 15:07:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Apr 2020 15:08:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:08:35 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 15:08:36 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Apr 2020 15:08:36 GMT
ENV ROS_DISTRO=kinetic
# Fri, 24 Apr 2020 15:08:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Apr 2020 15:10:46 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 15:10:50 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Apr 2020 15:10:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Apr 2020 15:10:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7c90921649b9f3cbb166f1e7855183c9279e66255ecccdacd8d50ab227b51d`  
		Last Modified: Fri, 24 Apr 2020 15:38:58 GMT  
		Size: 6.0 MB (5958923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746fe22f751624a02dac2053e33f6f9ff3c7d7b8b49c425e95ca0c7070f5bb7e`  
		Last Modified: Fri, 24 Apr 2020 15:38:57 GMT  
		Size: 13.1 KB (13103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c987dca6dd6b9fe0c80f563b4875bff8dcc141b5f34cfb4e1eb8c01a0b6d0d`  
		Last Modified: Fri, 24 Apr 2020 15:38:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a18bb8b026ed4b9b7a7353ad77f25040546e8fef3518489ad6e6142c506086c`  
		Last Modified: Fri, 24 Apr 2020 15:39:13 GMT  
		Size: 52.1 MB (52080831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaa0f6e5606c1bba121e6d0dbe69a81288185397dc350cda105e68362d1ec5e`  
		Last Modified: Fri, 24 Apr 2020 15:38:55 GMT  
		Size: 253.6 KB (253640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9d24e768d1998989be9ded331fa29a8c50e23d0fabff7bc8c69452f42bc1a`  
		Last Modified: Fri, 24 Apr 2020 15:39:48 GMT  
		Size: 174.3 MB (174250705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79fc9d55b1c4856d7d6f7313254ada25174fc64b5d913da70b72cfd07d550e0`  
		Last Modified: Fri, 24 Apr 2020 15:38:55 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
