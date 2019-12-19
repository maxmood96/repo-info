## `ros:latest`

```console
$ docker pull ros@sha256:a912aad98413dc5801772339f748a5c6a4977f7899e454d13bb844a05a7d259c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:651aca230deb1169e231851d25ffb5b36688404685c374e0f323fc897738274c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.8 MB (419820444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1250f3f920f875f6b2bc8a4a326e915d83ba92071f53402bfee352396a2ebcc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:35 GMT
ADD file:a48a5dc1b9dbfc632f6cf86fe27b770b63f07a115c98c4465dc184e303a4efa1 in / 
# Thu, 31 Oct 2019 22:20:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:37 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:35:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:35:42 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:35:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 31 Oct 2019 23:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 31 Oct 2019 23:36:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:36:51 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2019 23:36:51 GMT
ENV LC_ALL=C.UTF-8
# Thu, 31 Oct 2019 23:37:00 GMT
RUN rosdep init     && rosdep update
# Thu, 31 Oct 2019 23:37:00 GMT
ENV ROS_DISTRO=melodic
# Thu, 31 Oct 2019 23:40:14 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:40:15 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 31 Oct 2019 23:40:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 31 Oct 2019 23:40:16 GMT
CMD ["bash"]
# Thu, 31 Oct 2019 23:41:39 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ddbc47eeb70dc7f08e410a6667948b87ff3883024eb41478b44ef9a81bf400c`  
		Last Modified: Wed, 30 Oct 2019 00:25:34 GMT  
		Size: 26.7 MB (26688847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbdc448b7263673926b8fe2e88491e5083a8b4b06ddfabf311f2fc5f27e2ff`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 35.4 KB (35362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b70e3904492c753652606df4726430426f42ea56e06ea924d6fea7ae162a1`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d437916d5781043432f2d72608049dcf74ddbd27daa01a25fa63c8f1b9adc4`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9b01e3e432647233f9f035261d029b8747860c89497091395a3385eb8ed7ff`  
		Last Modified: Thu, 31 Oct 2019 23:56:28 GMT  
		Size: 837.3 KB (837344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fb7e096fb19a76ff587feaff77fd96d62aa1a9827cd2da7c7dbccae43ce293`  
		Last Modified: Thu, 31 Oct 2019 23:56:29 GMT  
		Size: 6.8 MB (6776244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516bdffd8ca21a3c0ff804eaf5721cd22a1adc90b21df568c1f20cd56f5c9c8e`  
		Last Modified: Thu, 31 Oct 2019 23:56:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60339fb0d35d575b6ed15f38b9b98d3da747d2df9e7c49b1dfdfbf96bc51a49a`  
		Last Modified: Thu, 31 Oct 2019 23:56:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f443a7a7d6ca1c302f8bc37ca9a3680d4b900bf850eaa2971bab6d5d74ebbf16`  
		Last Modified: Thu, 31 Oct 2019 23:56:42 GMT  
		Size: 55.1 MB (55059632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fa796f177cf039457e16cdefa80513cc6a774e1d856c7dee0e1b43a7afda0b`  
		Last Modified: Thu, 31 Oct 2019 23:56:26 GMT  
		Size: 432.8 KB (432773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6960f5a11411c332a54546cb616050312a57fdd8010c5a6df55fc6441dc4b48a`  
		Last Modified: Thu, 31 Oct 2019 23:57:24 GMT  
		Size: 261.7 MB (261655911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f77b2b02e40a07d89e3ce1d91b1f5865c9004e65b40696cca2c75dabd04cb9`  
		Last Modified: Thu, 31 Oct 2019 23:56:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc5942e3fe617dcb8b6fb59a1e4dad8ba632de0a6bc9f5558f310178e6a0ad7`  
		Last Modified: Thu, 31 Oct 2019 23:57:47 GMT  
		Size: 68.3 MB (68331487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm variant v7

```console
$ docker pull ros@sha256:ccfe308c17a0e677ecc384052b23e469680d809e45f2aa635d45ffabf6da2a6c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372218761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d463c5c602806461c174727773f1f51c9e8cc6bf7e8ef9df0efcbf0eed86e211`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:211c99393be1268cacabaeba24ec112fb96088bd06524239515f33cbe3de2d46
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350489846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6625e231f3571b520ae330594c160fd4dbe67f971aadb4f1ddaf405c6cbaf0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:28:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:28:36 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:28:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 31 Oct 2019 23:28:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 31 Oct 2019 23:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:29:51 GMT
ENV LANG=C.UTF-8
# Thu, 31 Oct 2019 23:29:51 GMT
ENV LC_ALL=C.UTF-8
# Thu, 31 Oct 2019 23:30:09 GMT
RUN rosdep init     && rosdep update
# Thu, 31 Oct 2019 23:30:09 GMT
ENV ROS_DISTRO=melodic
# Thu, 31 Oct 2019 23:33:17 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:33:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 31 Oct 2019 23:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 31 Oct 2019 23:33:27 GMT
CMD ["bash"]
# Thu, 31 Oct 2019 23:34:46 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b26a9f66c6d06a0b61908fc5ae522ef1d40f49507b344c85bfeca37e056ddf8`  
		Last Modified: Thu, 31 Oct 2019 23:53:12 GMT  
		Size: 837.8 KB (837784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46637339d4876ccd94fa6cf185787053d210ea7671bd037b1cc685f639694b99`  
		Last Modified: Thu, 31 Oct 2019 23:53:12 GMT  
		Size: 6.1 MB (6093384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b0986006f87a1dd1179f2a70f0c2e45cc4e05cd20efec9df579260c32eea9`  
		Last Modified: Thu, 31 Oct 2019 23:53:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9690f53d678ab501a0f5ccceced3d957bab3f1a38ced8cb247bca3be89039247`  
		Last Modified: Thu, 31 Oct 2019 23:53:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15da28666899a4aa50257b37de5918c7f07f7db6fa81d5d2f14a5eb3755c435d`  
		Last Modified: Thu, 31 Oct 2019 23:53:26 GMT  
		Size: 52.8 MB (52831522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1c0f9558971467bab1b8a1c2154458de0466a667501c6dcb2261bcec837491`  
		Last Modified: Thu, 31 Oct 2019 23:53:10 GMT  
		Size: 432.8 KB (432811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38309afe4efb92d963c50db1db71d365c928407d68c681b44f730ccfd1c95e99`  
		Last Modified: Thu, 31 Oct 2019 23:54:13 GMT  
		Size: 203.7 MB (203698274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf59a4edb742add8b245acdb6ffaefb00a747d9e6812651a2601e7efc47c0fe`  
		Last Modified: Thu, 31 Oct 2019 23:53:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca70e2ac1a897857766a33b3e58dfaeb6bf68fe80fc54284cb85ee98feacec2`  
		Last Modified: Thu, 31 Oct 2019 23:54:41 GMT  
		Size: 62.8 MB (62839599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
