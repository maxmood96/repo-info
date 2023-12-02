## `ros:latest`

```console
$ docker pull ros@sha256:c2f05668bc47f0c29de8a062e858b4d292328c9a8ab5d3a4578989dfe5a47991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:15dbc5efef92470bd7998b50de6cb878b2b42122c45141beedff16ed68371072
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263475791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f430a3a98e1d1077d42502cbd151c0570d0ff47b4378a56585ca1c8749929fbc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:30:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:30:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:31:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57968e329ced147f78a11c69c9cd74f92b334c69380d6ebf3adc06e69dcb8174`  
		Last Modified: Sat, 02 Dec 2023 06:02:38 GMT  
		Size: 98.1 MB (98135742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57236380704a693bf951c36f099cc471cb04f9b903274748f681edd88f30abb`  
		Last Modified: Sat, 02 Dec 2023 06:02:25 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23037007ece943d7f15c0f6426263385c4047ae880b538f481f4595aec37af78`  
		Last Modified: Sat, 02 Dec 2023 06:02:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac8a3380ba7335b0de60247b803ba619fa658e6b91face35adcdd2f387e25`  
		Last Modified: Sat, 02 Dec 2023 06:02:28 GMT  
		Size: 23.1 MB (23094946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2ca8f5ca27eec486ec33659c99e37b1f7460b644fb090e33041205d9a32d1261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256103479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1212a2909e03ae80c1f2ab71d19622de52cfd7740b02a750aece6ca616bb0555`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:38:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:38:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:38:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109606fc1cf4f571739382eda69dd7629b266ddb7b108f59718296836d31e1cf`  
		Last Modified: Sat, 02 Dec 2023 06:59:12 GMT  
		Size: 95.7 MB (95685282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c752ed94011d4054bd9ab9659ba8bd3fed9ece70cb476d960a6fc2db7fae55`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5dfebc2c0d59cdd3bb9da21d144fe2edbb6ad79841baa31521626c14e74aa0`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c320048bffeec8ead9a46877e6bbe02f4abf89a70dffcc2c23dd65eff458b`  
		Last Modified: Sat, 02 Dec 2023 06:59:04 GMT  
		Size: 22.5 MB (22517964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
