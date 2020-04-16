## `ros:melodic-ros-base-stretch`

```console
$ docker pull ros@sha256:e9ffbb0372383754f6c4b273c24c84bd457690167b61d1ccb55a24c07ca322b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-stretch` - linux; amd64

```console
$ docker pull ros@sha256:9f56dbb22225db2db880448c9b4e057fe11496cca2aa9cb1c75142fff88adbc9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.6 MB (505567179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d6883e25d870c83eb868f5a1d93e4e4e47459b4025a17e2d3a989d0d37c93e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 21:21:23 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 21:21:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Apr 2020 21:21:27 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Apr 2020 21:22:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 21:22:10 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 21:22:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Apr 2020 21:22:11 GMT
ENV ROS_DISTRO=melodic
# Thu, 16 Apr 2020 21:22:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Apr 2020 21:24:12 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 21:24:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 16 Apr 2020 21:24:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Apr 2020 21:24:15 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 21:25:09 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ae969f13784ebe52e834152ea92cb26a18883e3404ddf60f30c6b98e1fb8c6`  
		Last Modified: Thu, 16 Apr 2020 21:30:11 GMT  
		Size: 10.5 MB (10476657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662ec9220d2a2d487b24618c7157c0668d193413b0d2d28f0e64478bd8fd4a8b`  
		Last Modified: Thu, 16 Apr 2020 21:30:07 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a853d4aaebf8e31ee58374a9488d9fbcd711242e2f6c438972e46c815e295270`  
		Last Modified: Thu, 16 Apr 2020 21:30:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d063711f6ff5a9ceaa9da71900cce5c3757845dcece4cc406075eaae348ebc22`  
		Last Modified: Thu, 16 Apr 2020 21:30:36 GMT  
		Size: 64.8 MB (64785383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fdd58c7ba83f45cfe599bb5f3b64bed1a0157eecec0e1713d557bc80c93e74`  
		Last Modified: Thu, 16 Apr 2020 21:30:05 GMT  
		Size: 242.4 KB (242443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c18c211e7ac5fa48f68dfbad2b25a38cc6bce8f1f30a167394a027b212b0c8`  
		Last Modified: Thu, 16 Apr 2020 21:31:34 GMT  
		Size: 276.2 MB (276209002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d30f1ceb2f53e55f7af652ee6d3f2b7651406e56283d0da4d1bb9c71e2f5e7e`  
		Last Modified: Thu, 16 Apr 2020 21:30:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e123734687a56105f5196a04eac084ed695174e84813658f8f7c89edc36e3`  
		Last Modified: Thu, 16 Apr 2020 21:31:58 GMT  
		Size: 108.5 MB (108475968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c4539a41d93b4f924df02284ab8c3e022b73caf54d6e2ff5561a352638bdcaeb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448633736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0854fc258f715610814299d5c951102415f9e040a9148e68963ac4c45b976390`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:44:49 GMT
ADD file:6d09304a2db2752e78b9ce9610594102dc756aa4cd210f85bbfa21105c7dd88f in / 
# Thu, 16 Apr 2020 02:44:52 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 19:06:52 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 19:06:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Apr 2020 19:06:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Apr 2020 19:08:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 19:08:52 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 19:08:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Apr 2020 19:08:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 16 Apr 2020 19:09:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Apr 2020 19:12:39 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 19:12:45 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 16 Apr 2020 19:12:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Apr 2020 19:12:46 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 19:14:47 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:65d54b492d599e7c785a582a0f70195e1f09f0886e54cb7788f1021f383eb4ed`  
		Last Modified: Thu, 16 Apr 2020 02:51:10 GMT  
		Size: 43.2 MB (43159230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0743cf484cfc563f62e5c414bc921f20ab1762ac6f8e90e998c30191b42760ee`  
		Last Modified: Thu, 16 Apr 2020 19:22:37 GMT  
		Size: 9.8 MB (9774840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8753a544948ad71b7418f891fcc4f5cce283b76876da800b6465c3e403bb346`  
		Last Modified: Thu, 16 Apr 2020 19:22:34 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6d96d88d962f0ef2ccc4aa2abee387c875dc2e30e4e187737223d82feea079`  
		Last Modified: Thu, 16 Apr 2020 19:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8016d4bed04a1fe5d58e152ffe6d8cb92e1cd4bb1d91a4375451446018705ff5`  
		Last Modified: Thu, 16 Apr 2020 19:22:55 GMT  
		Size: 62.1 MB (62094068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be77092016eb5e5cd4796b98493f2d025cc6ace62fd2becf249009355e52971`  
		Last Modified: Thu, 16 Apr 2020 19:22:33 GMT  
		Size: 242.5 KB (242506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54782438f89ca37a4b5802940e1ff50ac8b7b71d88686e9ac69e64c50d3c8e4d`  
		Last Modified: Thu, 16 Apr 2020 19:23:43 GMT  
		Size: 230.4 MB (230402646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde47d8377b4dff34bb041611dec847c01eb96691ac3a7599202a721d307d5d3`  
		Last Modified: Thu, 16 Apr 2020 19:22:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a521d61572507975dac580880eaccd3824a2851a05546ddd6023dc16085f781e`  
		Last Modified: Thu, 16 Apr 2020 19:24:14 GMT  
		Size: 103.0 MB (102958626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
