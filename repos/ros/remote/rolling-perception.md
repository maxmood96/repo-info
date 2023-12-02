## `ros:rolling-perception`

```console
$ docker pull ros@sha256:926b1d08083e1bc09891617da3fab01c1b816879d76a79379eb306710881327c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:cc7066833e4bc91cf30a6ff2071e0507e1850e433ab947bb7db9765baf817514
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.9 MB (959931532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9398061bf4afb5deaf168bc397874a59dcb0509c5226b74875a75883c030ad99`
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
# Sat, 02 Dec 2023 05:55:52 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 05:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:56:37 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:56:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:56:37 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:56:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:57:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:57:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:58:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:b70cdec7f7f494d3cb2ea302a0b42630c0353133474a693a309d1b5950b3d1b1`  
		Last Modified: Sat, 02 Dec 2023 06:07:11 GMT  
		Size: 124.3 MB (124271649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb056cc69d86752a925eb68c836ad08186757af76db68041db5eb1da10a0e15`  
		Last Modified: Sat, 02 Dec 2023 06:06:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e7b257add838be46a798525b40ef3b18fea490caf612f09c1151ebbe6f7a6`  
		Last Modified: Sat, 02 Dec 2023 06:07:31 GMT  
		Size: 85.2 MB (85172080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf0a91322021b1c4e36dd3a6fb62d30b3c54e6098d0755a4f5bdfc328aa0040`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 302.3 KB (302307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f42b45f4e05e21e47e74869b5b88a9964383d8448055d257f47a34694c6eae0`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7f58f28f44789d5600868e9ca68910d022964a421870c5b3bbbb5ae9cb08c`  
		Last Modified: Sat, 02 Dec 2023 06:07:24 GMT  
		Size: 23.8 MB (23778449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f623afbab66cfa921bc142fdbc3182c107255770f7586d5fbe97df35f8d24890`  
		Last Modified: Sat, 02 Dec 2023 06:09:08 GMT  
		Size: 690.9 MB (690913680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8493f256e99822754a625976fbff3141dc8252f937f64b9c1417d3f79e0e1159
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920230507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736dbef879b4aeea4ad4246294caa41444baa768529c4d49fc9572bdabc36cd`
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
# Sat, 02 Dec 2023 06:52:29 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 06:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:53:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:53:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:53:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:53:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:55:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c9c57f456ff177333c5356ffa95267bf81ffda007282ce077aefc6dad7287b95`  
		Last Modified: Sat, 02 Dec 2023 07:03:49 GMT  
		Size: 121.7 MB (121738352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea17e58cc534987e4066afb39789529299e5bc0f0963a20f3a8e3abb5798f5`  
		Last Modified: Sat, 02 Dec 2023 07:03:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d83f0b90f7994538015346ea0103817e07f6da588cecd5abbe0dd1627ebc4ac`  
		Last Modified: Sat, 02 Dec 2023 07:04:06 GMT  
		Size: 82.8 MB (82848039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c43d34c57d89c613359ac8be6efbbcf83426b61e4b6af0fb3066fec67df503`  
		Last Modified: Sat, 02 Dec 2023 07:03:57 GMT  
		Size: 302.3 KB (302296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a216765a08949157ffe626c1703f66b7e09f03610e3d0424d53cefaa986f0877`  
		Last Modified: Sat, 02 Dec 2023 07:03:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca613d7f9aa91e5aa03a762cb8204133388b9cf71737c8afb097c084023b36`  
		Last Modified: Sat, 02 Dec 2023 07:04:01 GMT  
		Size: 23.2 MB (23164918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210a93a5bf952bcc123fcfc114a7b4639054f592c0d48f290cc2bd7c0bced571`  
		Last Modified: Sat, 02 Dec 2023 07:05:39 GMT  
		Size: 658.8 MB (658755836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
