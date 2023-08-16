## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:18d9ac3b698d9a6184a866ea6e69a1164bf542997456a4e9efbccea5f83d813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c0d01ca752cc23ddddb389409680c54fb6c85949c79bc4a3bcdd2a266414a313
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268546213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4bee036752b69abd2271fb9ab494ff987a3923d00c355fc8651896a7dc9b00`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:48:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:48:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:48:30 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 04 Jul 2023 19:48:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:48:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:48:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:00:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:01:02 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b96b181e03e7c00f9ff313a35cb309648ea7a63a12165e78d4298df8d842ef7`  
		Last Modified: Tue, 04 Jul 2023 20:09:20 GMT  
		Size: 1.2 MB (1213029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981b99f5f99f37d026fe791185912ef266fd67d841915968d7f58e1e21aa67dd`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 3.8 MB (3828864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457911032da59063f35f0ed9962d1f7235ab9b54c6a1b2434538945c43049d6d`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca97964148324558ddeb21e9e1395cff5cbcb0443e2d4b59209fa6930ea226d`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199be721033556b61121fd3dc17b7e99b7a7f82492d2272ba5b86f84a9ce7fc2`  
		Last Modified: Tue, 04 Jul 2023 20:12:24 GMT  
		Size: 85.0 MB (84994600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ff985aa05405f2f8956ec07b70eae3f30be79fec5c6d3c1617677f4c3696ac`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 293.8 KB (293837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4dbbe640a7122ac20768a9e899cd6f765aca885c9d8f66066b241d69c62228`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad8cd1c41ec878e1b4d38c0b86b45f871a82ec4c846bc1c940a726af567ffa9`  
		Last Modified: Tue, 04 Jul 2023 20:12:18 GMT  
		Size: 23.7 MB (23672931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:abff66cc26ac456d4f7f24bc13108310663e0f64a9fd24646aa30b2f1ac0e573
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261284786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a339b73410a100e8948f172487e9f0172e70fe9481a4fcf91f19c71521d13`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:16:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:40 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 16 Aug 2023 15:16:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:16:41 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:16:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:30:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:30:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:30:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:30:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb23ce0adf8021e5f112c4ebb6b7985390219367991abf52dc7c9e4a59d4e5`  
		Last Modified: Wed, 16 Aug 2023 15:38:58 GMT  
		Size: 1.2 MB (1214567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9e5d7e79405f9ead5346e83d4f49c73608d784a30ccea5e9f0a1cb44319e56`  
		Last Modified: Wed, 16 Aug 2023 15:38:56 GMT  
		Size: 3.8 MB (3801963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61556f61e2363012e91a6b26a6d4854861844ae4d453b2e94e69a8cedb8bd75c`  
		Last Modified: Wed, 16 Aug 2023 15:38:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341a3b77ddbf45ba0b2711355c528b654f522ef0e6f08211fb17a01e1d8cc114`  
		Last Modified: Wed, 16 Aug 2023 15:38:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a4eda63942c2c3ef94d99c842b03cebea82f1904a1f5b631974a295b7efe37`  
		Last Modified: Wed, 16 Aug 2023 15:41:44 GMT  
		Size: 82.8 MB (82840931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50080694231be65dd9eaf3724f7526680ccbfc58ba778f355aa132dd315de1e`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 299.8 KB (299847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e728607890e153ce62f3d6cefe5ea39753687001587d366b4e723b1434db1fb`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756195b01fe3a6421f90801c97bc4d09c3ce2918293c47f005d0a8a876793811`  
		Last Modified: Wed, 16 Aug 2023 15:41:39 GMT  
		Size: 23.1 MB (23113110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
