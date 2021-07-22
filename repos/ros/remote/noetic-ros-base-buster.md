## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:3e68643ebaf0308e702c8df1245ce7e178d83800c1872ee369f38b572f3d835d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:6aea7247bac4cb0aeb1792cb141ab3008ac272e24c56eab3ddebc1bf8dc1539d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463217170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7863284678344dc36f900367d88af5fc116dfd0332fcf3ec755da65843afca`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:25 GMT
ADD file:a232795a746e5842d1a864a00462be6bd86543aeed8d06d2830dd955a4c1b3fc in / 
# Wed, 23 Jun 2021 00:20:25 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 16:54:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 16:54:05 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 23 Jun 2021 16:54:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 23 Jun 2021 16:54:07 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 16:54:07 GMT
ENV LC_ALL=C.UTF-8
# Wed, 23 Jun 2021 16:54:07 GMT
ENV ROS_DISTRO=noetic
# Wed, 23 Jun 2021 16:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 16:55:11 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 23 Jun 2021 16:55:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 23 Jun 2021 16:55:11 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 16:55:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 16:55:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 23 Jun 2021 16:56:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bc3020d05f1e08b41f1c5d54650a157b1690cde7fedb1fafbc9cda70ee2ec5c`  
		Last Modified: Wed, 23 Jun 2021 00:25:08 GMT  
		Size: 50.4 MB (50435617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368710b5d60bd3571596105db24587dc7641662961cd8565f0ab308ea71c8716`  
		Last Modified: Wed, 23 Jun 2021 17:00:59 GMT  
		Size: 10.9 MB (10891785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c851fa0b21cd231e582f810f8c19cefe3e82acfd0b381ee63df5ad2ea6d405`  
		Last Modified: Wed, 23 Jun 2021 17:00:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d911fa207ab982f2d18b595a9cbd025da0e7d7b99a38329c00d496ae74e5c57`  
		Last Modified: Wed, 23 Jun 2021 17:00:57 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf3cb86fc6e74480b1bed2f10d298288eaef33b5c4a44e36c5723bed2d7d603`  
		Last Modified: Wed, 23 Jun 2021 17:01:36 GMT  
		Size: 239.0 MB (239043542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6807ff55dd30ea5a41adf5345578639e51e44f6cac1d76453af573795d8367d9`  
		Last Modified: Wed, 23 Jun 2021 17:00:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda640c7cc970da7dc489bbd348f6d10ca8aadea00bb348b143454fef3f798f1`  
		Last Modified: Wed, 23 Jun 2021 17:01:59 GMT  
		Size: 86.6 MB (86566646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6b8e0c86f409efb0b6383db70437892d4daca00797115f65c9c22a2ed27322`  
		Last Modified: Wed, 23 Jun 2021 17:01:45 GMT  
		Size: 302.4 KB (302359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7aeca0ec3c658ebff801eb589b5d7083dafb559be63ecbf3a4f0ed4cb127398`  
		Last Modified: Wed, 23 Jun 2021 17:02:00 GMT  
		Size: 76.0 MB (75974809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5f0b088ea3ad6583bce9a0b1cb2ccb7eecbb695506638a1859eb557129b1a9c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.1 MB (403090275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe382bffc979be1588137624468ff19d7d43de757da5568ea0ec88fb391d5bd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:59 GMT
ADD file:3e8e075f08a6b727602af05c539f43648a48663cbb3a88eeba310cfc32c01d78 in / 
# Thu, 22 Jul 2021 00:40:00 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:23:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:23:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 22 Jul 2021 12:23:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 22 Jul 2021 12:23:13 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 12:23:13 GMT
ENV LC_ALL=C.UTF-8
# Thu, 22 Jul 2021 12:23:13 GMT
ENV ROS_DISTRO=noetic
# Thu, 22 Jul 2021 12:24:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:24:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 22 Jul 2021 12:24:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 22 Jul 2021 12:24:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:24:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:24:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 22 Jul 2021 12:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d272b0d8f7c4fd0caf0ef022ce544cfe3800e349a73b585f82837e6526a4247e`  
		Last Modified: Thu, 22 Jul 2021 00:45:18 GMT  
		Size: 49.2 MB (49222109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be023b22932cf47a4eb2115be15d3539f42a9ba7f9e98e522ed582fea89d40ee`  
		Last Modified: Thu, 22 Jul 2021 12:30:33 GMT  
		Size: 10.9 MB (10883239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb89b3f136886dea2466ea37659c55816ee15ebbf27efcfa566bbfc6a0384ab2`  
		Last Modified: Thu, 22 Jul 2021 12:30:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524675b4de3d1ee20d4a04933115962a10c720490abede3b8f36e10eaca5459`  
		Last Modified: Thu, 22 Jul 2021 12:30:31 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fbd2e0d882c66b95029d4dfcf0c4e74d13cda2c7384b2a05c68ede1a772f1a`  
		Last Modified: Thu, 22 Jul 2021 12:31:04 GMT  
		Size: 184.2 MB (184228886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5d957f3309d21e8071f4420302d491f5888cc1cda7dc47be23381343b24229`  
		Last Modified: Thu, 22 Jul 2021 12:30:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1abb177db0c6957e16f2623b80172d001eda36151c5c11fb362295292e0770`  
		Last Modified: Thu, 22 Jul 2021 12:31:24 GMT  
		Size: 84.4 MB (84358083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f870b59a8cbee52a2156009d6000e43da6e47aa64620f552a819fe668656e4`  
		Last Modified: Thu, 22 Jul 2021 12:31:13 GMT  
		Size: 307.5 KB (307547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1425c523ebd4c20244bcc2aa541c97cde933812583ffa085a0eb7f47503c35`  
		Last Modified: Thu, 22 Jul 2021 12:31:23 GMT  
		Size: 74.1 MB (74087996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
