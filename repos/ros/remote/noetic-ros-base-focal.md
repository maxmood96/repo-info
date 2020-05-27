## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:5403f4bd819d2aec891e67a32e46f17f86f04b180999db7da2513b718e3a6f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:3c94f741a61c954e77c970ddd4961d916258b7cd3fb5113d0218fe9fa30f2c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334503751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2b2d1db95c521302bcb7ef2dae3d78c6b39aa958f8aa84f5ad8e4fab7a9ac2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:46 GMT
ADD file:a58c8b447951f9e30c92e7262a2effbb8b403c2e795ebaf58456f096b5b2a720 in / 
# Fri, 24 Apr 2020 01:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:51 GMT
CMD ["/bin/bash"]
# Tue, 19 May 2020 18:42:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:21:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:21:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 01:21:44 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 01:21:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 01:21:44 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 01:21:45 GMT
ENV ROS_DISTRO=noetic
# Wed, 27 May 2020 01:23:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:23:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 01:23:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 01:23:55 GMT
CMD ["bash"]
# Wed, 27 May 2020 01:24:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 01:25:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d51af753c3d3a984351448ec0f85ddafc580680fd6dfce9f4b09fdb367ee1e3e`  
		Last Modified: Fri, 24 Apr 2020 01:09:34 GMT  
		Size: 28.6 MB (28556247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc878cd0a91c7bece56f668b2c79a19d94dd5471dae41fe5a7e14b4ae65251f6`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154df8ff9882934dc5bf265b8b85a3aeadba06387447ffa440f7af7f32b0e1d`  
		Last Modified: Fri, 24 Apr 2020 01:09:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5db0ff82f7aa5ace63497df4802bbadf8f2779ed3e1858605b791dc449425`  
		Last Modified: Fri, 24 Apr 2020 01:09:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3e5de01a1b5595882fcb3da54a47556f3d36ac6a4a952bc4d2432a0715a4ad`  
		Last Modified: Tue, 19 May 2020 19:01:20 GMT  
		Size: 1.2 MB (1174766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e1d894b26307c3fd316e1b286e7ea5840bca5139148f674e741f4762eae1bb`  
		Last Modified: Wed, 27 May 2020 01:38:49 GMT  
		Size: 5.5 MB (5548577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b657ccfc9d28c3e22960d6d4680437be8bf7b2192cc35c630e1ebc462215d97`  
		Last Modified: Wed, 27 May 2020 01:38:48 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdda584d4ef232bbfb98474f1b4d88e2bcf8ee3f749d628583330eefb30b8413`  
		Last Modified: Wed, 27 May 2020 01:38:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619ad093d22b60eef225154c3cf81fbc35bd61d5f88553451a0612b4b8e1a942`  
		Last Modified: Wed, 27 May 2020 01:39:32 GMT  
		Size: 173.0 MB (173033253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5682baf4b2f816eba7eb103d82831d17df31d82867aac6d1b4ab156822147c8d`  
		Last Modified: Wed, 27 May 2020 01:38:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1c23271149ddfb05dbee95b70d7d098d1030253dc014850a0e53e0af44c94c`  
		Last Modified: Wed, 27 May 2020 01:39:47 GMT  
		Size: 46.4 MB (46375833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a306d6bcd4649e112cf46feb0361a82920e5eb35b5684fc90188dad31ee2d1e0`  
		Last Modified: Wed, 27 May 2020 01:39:36 GMT  
		Size: 191.3 KB (191298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30517988b4271b1e1caeefdef5ac43b93f2be382f27f71ac3043f93a4e10b4cc`  
		Last Modified: Wed, 27 May 2020 01:39:54 GMT  
		Size: 79.6 MB (79588626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e747a628ee1504ffc17ffcbce8b0aecf3981d13d789d008f96b562fdd3eb5913
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314185964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d923b71186e4b72ea10a79b40bbc1e62fd4e5766130805478a11e4adc0e031`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Apr 2020 00:18:16 GMT
ADD file:e9947aff2dfa8f220d4b25dc0770aff8d9ffc08482e52f54833f39e1c3ec08bf in / 
# Fri, 24 Apr 2020 00:18:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:18:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:18:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:18:29 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2020 01:42:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:43:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:43:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 01:43:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 01:43:14 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 01:43:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 01:43:16 GMT
ENV ROS_DISTRO=noetic
# Wed, 27 May 2020 01:45:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:45:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 01:45:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 01:45:22 GMT
CMD ["bash"]
# Wed, 27 May 2020 01:45:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:46:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 27 May 2020 01:47:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6c2d76ba33f8d52087147ce28d8f03c08f69677591e3e10db810bf76a6e09427`  
		Last Modified: Fri, 24 Apr 2020 00:22:00 GMT  
		Size: 27.2 MB (27158644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92d4cfc71d3821474946021fdbf241a74992a84c6269c3e9a052ce7fc56cece`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 32.3 KB (32326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63063bfe137200b3c8d1ee8d819124352c20ee8c189a0388f461ec66bb759310`  
		Last Modified: Fri, 24 Apr 2020 00:21:53 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38385900086ffa7d7cb9c3bbeabaf2176d7d7958ebf0736d2a01773a830201ee`  
		Last Modified: Fri, 24 Apr 2020 00:21:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee47658e5a2b6951b5c8f1df079e5f94fa5babfcb132843f7e89a21a531555f5`  
		Last Modified: Wed, 27 May 2020 02:09:35 GMT  
		Size: 1.2 MB (1175483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9b7e5841799d26c7c96bfbade1ef6d8be3e67adbbc8402a26e6a6cf491a849`  
		Last Modified: Wed, 27 May 2020 02:09:35 GMT  
		Size: 5.5 MB (5515489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8079fbc9cd40b2782019694e3fdfea45d641b7cd63c3e41e193edc9581c050ee`  
		Last Modified: Wed, 27 May 2020 02:09:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466f2def65cbef8879615836953fdcf925a5f2939b8de31efd03f743b55b5a7e`  
		Last Modified: Wed, 27 May 2020 02:09:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c477f23a37aae87e79e2d039cc427c8174dd6513a2a0be7e2cf6cf9e0c02b6`  
		Last Modified: Wed, 27 May 2020 02:10:31 GMT  
		Size: 167.5 MB (167515200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402c98fd13dcd5aec2d2d17202a7b20a271f01fb363449fb52e239600b2c6e60`  
		Last Modified: Wed, 27 May 2020 02:09:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0b623443a32035b0a2ba25dd30f44dfec17d991256b6d4e3d524b3e89e0359`  
		Last Modified: Wed, 27 May 2020 02:10:48 GMT  
		Size: 40.6 MB (40626412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499487948ecf8c68d03a45de73d1b485af2b94f05a7009b59f9c20d828c9d0fd`  
		Last Modified: Wed, 27 May 2020 02:10:38 GMT  
		Size: 191.4 KB (191353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2550fc27e13f6970e02c8d4e08c471861113abbade943c750cae9816832c48d`  
		Last Modified: Wed, 27 May 2020 02:10:58 GMT  
		Size: 72.0 MB (71968183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
