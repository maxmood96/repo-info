## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:b20c43524763f53f983bd5fd1708924b19b2da16ca8ae91a2dc607ae541ea20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:e0a2a63b2abd217a2cb98b885fd56adbf432b140683158bb364d937d90580db9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.3 MB (448275778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3717b28c10ed23925f280d8624093213be2d144bbd616dd18609a47037cb57`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:37:59 GMT
ADD file:ef36fee25b0bd1d99979ecb8d54b206cec33d4e8fd2232189f0d8e5ab9754798 in / 
# Thu, 21 Jan 2021 03:38:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:05 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:26:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:02:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:02:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 11:02:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 11:02:32 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 11:02:32 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 11:02:33 GMT
ENV ROS_DISTRO=melodic
# Thu, 21 Jan 2021 11:05:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:05:50 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 11:05:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 11:05:50 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 11:06:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:06:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 11:07:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:08:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d519e2592276828ca171d85e0532899cd4f98c70f5c697b45fa2e126e9f9fe49`  
		Last Modified: Thu, 21 Jan 2021 03:40:27 GMT  
		Size: 26.7 MB (26709716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d2dfcfa9cd230ed3c47defec2670d45081598c721dd85cafc34ea459f970e`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3afe92c540b778c64ca316d1e679d55d2d2e812e450f516a808ee591f0c3f77`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea992ddb93cee91b21cf19902eb7c0780191f8454157802d68fe834ad6c72d5`  
		Last Modified: Thu, 21 Jan 2021 08:49:44 GMT  
		Size: 840.0 KB (840038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe549b7120b83770f6772179d9e937e479567ac1297ed6808a3c029da14a498`  
		Last Modified: Thu, 21 Jan 2021 11:44:40 GMT  
		Size: 4.9 MB (4870380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3148dcdae1e4da81fc90c6c4dc4ca6a3612c7176d9a53c61cf366eb77428c96`  
		Last Modified: Thu, 21 Jan 2021 11:44:39 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97022b250a6f8d2ce144f6af08d49d2315bc186f0aefe044b72b6221046660b5`  
		Last Modified: Thu, 21 Jan 2021 11:44:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5f0e3dbbabad092e0eca391faecfd40a766ec66cfc52873b3e646c4b28624e`  
		Last Modified: Thu, 21 Jan 2021 11:45:31 GMT  
		Size: 259.3 MB (259348853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4861edf5d2c91e3cf3bbd7b66c900178c66707bf5eb9a9225846f17d457659`  
		Last Modified: Thu, 21 Jan 2021 11:44:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1487fd48d9e8b625af56d96beaf411cd973b8abbfe2c99c62d70e2da49976f5f`  
		Last Modified: Thu, 21 Jan 2021 11:46:04 GMT  
		Size: 70.2 MB (70210490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66d4d7c21a40f83cefd470b534b90fb735be7cdf630aad736bab4064e094224`  
		Last Modified: Thu, 21 Jan 2021 11:45:49 GMT  
		Size: 244.7 KB (244730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69955244f09b3b422392c01e273ff9e6948a5e920b5b1b4c407e547c8da14ebf`  
		Last Modified: Thu, 21 Jan 2021 11:46:09 GMT  
		Size: 75.0 MB (74987751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052472ffc6344c3e2838098cfbafe60af58d8a4765250b3024131b9b53e4658e`  
		Last Modified: Thu, 21 Jan 2021 11:46:21 GMT  
		Size: 11.1 MB (11060968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:a48d15f4cd4cd66ad849c4a88f77af336d89e0b5f3441e0a441d21fdf8f46c69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395872493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4d2c49db786aa0829321e149ff1455a565b4cacc919f5c97ab0593b0ae277b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:15:18 GMT
ADD file:270f582b851314ab60dfbbc136c8e36ec44a11ecba1448403947ce72b0f9c06a in / 
# Thu, 21 Jan 2021 03:15:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:15:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:15:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:15:27 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:30:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:31:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:31:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 04:31:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 04:31:16 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 04:31:18 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 04:31:19 GMT
ENV ROS_DISTRO=melodic
# Thu, 21 Jan 2021 04:34:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:34:39 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 04:34:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 04:34:41 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 04:35:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 04:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:37:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d8bd15f2f6189f24e8f1b5dc573a293c963565ab012ca6a42e51a3023e72e7e`  
		Last Modified: Thu, 21 Jan 2021 03:18:06 GMT  
		Size: 22.3 MB (22291204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e961f21c7ea83c265a6de2897b8255e9e03cf1d39b74fb208b4ca936c6a53c5`  
		Last Modified: Thu, 21 Jan 2021 03:18:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b017766c8f695603aa5da2f534135bd1fbe253f667ef6faa77a77c66be9ba9f5`  
		Last Modified: Thu, 21 Jan 2021 03:18:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb7679849b59188f62bf017de9112158370c1d2eee07a8d614ba382cf612b62`  
		Last Modified: Thu, 21 Jan 2021 05:12:20 GMT  
		Size: 841.2 KB (841181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd1c8ec76e1cf5b551b2db58eb684cae7c4a3219c7175d85b4bf9ea4e5fe998`  
		Last Modified: Thu, 21 Jan 2021 05:12:19 GMT  
		Size: 4.1 MB (4085304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf27b43dde6748aae4a2d48a18d094192f874983a13d5046c161f02d3e11ab77`  
		Last Modified: Thu, 21 Jan 2021 05:12:16 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3331cdb0247821fb1bee41928bad1bbc5ed592cc12bbf4231a4fc73d5fbc3668`  
		Last Modified: Thu, 21 Jan 2021 05:12:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6e907b6a25c975ec7df5ea0e052e876a9240a0ba005ec9567f9cff4ec0bf76`  
		Last Modified: Thu, 21 Jan 2021 05:13:28 GMT  
		Size: 238.9 MB (238858209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c3aad0df547a9dbab2ff8eafc39fb1fb18ed1142b42ec2fe715364426040b2`  
		Last Modified: Thu, 21 Jan 2021 05:12:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a045fe81fe6a997f99b44f1309fab3bca03096d3ac72d32cc7305f56e28ba9d5`  
		Last Modified: Thu, 21 Jan 2021 05:13:55 GMT  
		Size: 54.7 MB (54685291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bed2ac9eafd52a3e8676e666162cb862f05128ea8a0ade7fb76ba57658e93bd`  
		Last Modified: Thu, 21 Jan 2021 05:13:40 GMT  
		Size: 244.8 KB (244755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918e7c4382226442371dbc99bb4a624d5adf61ce51ece504aae8d03e7afed0ac`  
		Last Modified: Thu, 21 Jan 2021 05:14:01 GMT  
		Size: 64.7 MB (64742789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa4f04750a609b47d910230a71580a96b18211dd22ace55c1b2abd1abf6aaec`  
		Last Modified: Thu, 21 Jan 2021 05:14:19 GMT  
		Size: 10.1 MB (10120879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6f0cfe6452a95cbc50f8b9e07e0720085d792b2328b3eadc93d10a9f0bd462c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422588173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5882256c56686c65261e2753c32a7cd6f7eae26bc6465eed51b342b20c60d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 03:12:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:13:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:13:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 03:13:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 04 Mar 2021 03:13:16 GMT
ENV LANG=C.UTF-8
# Thu, 04 Mar 2021 03:13:17 GMT
ENV LC_ALL=C.UTF-8
# Thu, 04 Mar 2021 03:13:17 GMT
ENV ROS_DISTRO=melodic
# Thu, 04 Mar 2021 03:15:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:15:55 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 04 Mar 2021 03:15:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 04 Mar 2021 03:15:57 GMT
CMD ["bash"]
# Thu, 04 Mar 2021 03:16:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:16:46 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 04 Mar 2021 03:17:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:18:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb395c83b2a400ee825ab384f2c51674c732ff599742e127b5639756b0cc7a8b`  
		Last Modified: Thu, 04 Mar 2021 04:00:41 GMT  
		Size: 840.9 KB (840907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3418e9c274d60c6f142b25861afead56aafa5ece244d451cab264c52961bc618`  
		Last Modified: Thu, 04 Mar 2021 04:00:40 GMT  
		Size: 4.5 MB (4453487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee6263fb6dc4f04d5d149d5aa0d9932daea95f32e0478a12a5e66a986a1931`  
		Last Modified: Thu, 04 Mar 2021 04:00:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8e05aa8adaaca88884b382bafe4f0be06ae98213b2218241a2902c79e1cfee`  
		Last Modified: Thu, 04 Mar 2021 04:00:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555500c77492e3762a37fca4a8c00f0b77bbf70f9e460aa0dcfb94c4d8ecea80`  
		Last Modified: Thu, 04 Mar 2021 04:01:42 GMT  
		Size: 252.3 MB (252315934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2937675ccb8ca23fe751124dde72dbaaad5c4a092de0ffcc1b7af3b251b6572`  
		Last Modified: Thu, 04 Mar 2021 04:00:40 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb96dea428d115d3554ab519eca3ca07ee50c4e4a07d4043db89bfffe8307fc`  
		Last Modified: Thu, 04 Mar 2021 04:02:09 GMT  
		Size: 63.0 MB (63046732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11261de657a2e1ed5792d69678a31419bd2c864498d84882af82a553315acac7`  
		Last Modified: Thu, 04 Mar 2021 04:01:54 GMT  
		Size: 248.1 KB (248089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867b19bf0adda4b4f1f09cd750ba09c21013e567d6f72a48da8ead280a33a4ab`  
		Last Modified: Thu, 04 Mar 2021 04:02:12 GMT  
		Size: 67.2 MB (67223742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f288d63fd6e6a9df72c367ab93ee25b0402feabfb8632de46b61ea04c5677b32`  
		Last Modified: Thu, 04 Mar 2021 04:02:25 GMT  
		Size: 10.7 MB (10724352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
