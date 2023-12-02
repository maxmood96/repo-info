## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:a3c3a64387415b81f24df2cd911e3850ffd2f70eda174704d00ba30f2d9a73ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:95c8d7e760bdace352b40801d74d82c74c8d8a3d517ab91626dded6b7838e04c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268919994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a01f270fe50dde28a60ac9e407b2c2170d6b4b06d3c541ef576064037cd47cc`
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
# Sat, 02 Dec 2023 05:51:06 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 05:52:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:52:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:52:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:52:51 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:53:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:53:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:55970dcb7fa90692b2898147d21e6b7e0f5e68377f2c76abc9cc9835b3e1c54e`  
		Last Modified: Sat, 02 Dec 2023 06:04:48 GMT  
		Size: 124.2 MB (124216210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8396d9129ad2c371dc2833e37d47be0334635d73ad57281ba8a3ea3c7165c891`  
		Last Modified: Sat, 02 Dec 2023 06:04:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eac5058ff99e0df90c1b680752035609ff5033e07aa0a5f924c7e1ac26d5a1b`  
		Last Modified: Sat, 02 Dec 2023 06:05:07 GMT  
		Size: 85.2 MB (85169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab40920f7ffd72d0a2db3dcd77869f4c5a5600fb81e29fc3186fd083b935ec9f`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 308.6 KB (308556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a2108c2c74486e73d941900a61a2f2a535d73a636419fc1627781e539737be`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c284bd6fd5658111dd8e8df3c8543c1340de31d5bd21b3b438ad3a5daaea0d`  
		Last Modified: Sat, 02 Dec 2023 06:05:00 GMT  
		Size: 23.7 MB (23732633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b23155291265f94ee17b584be3440583e953306c71a1067227a77ebacdceaa1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261368382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0873a406c54079c1be0f2e77a219bbf94c35101a78fe9565cf09e19a497f42d`
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
# Sat, 02 Dec 2023 06:48:57 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 06:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:49:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:49:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:50:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:50:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:50:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:50:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:08c07f727a0cfab8f804fb7d07d7775fec316e6bed370e382264495262155e7d`  
		Last Modified: Sat, 02 Dec 2023 07:01:21 GMT  
		Size: 121.7 MB (121673366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431aa29c67a95ca2aa991d33932727e74558d1c93adc588818163d8f34c75daf`  
		Last Modified: Sat, 02 Dec 2023 07:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889362a5c51bef9df737c5c551cb027da6dc6d40a76eb42c0ef20e43c503ee9`  
		Last Modified: Sat, 02 Dec 2023 07:01:40 GMT  
		Size: 82.8 MB (82845418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efdecdc5548e93ba799103042e04c09a1d67b083a3afa7a62e202a9e33c209f`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 308.6 KB (308560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b73f54309b9404ff54005ee91f4524e46e522491de3eac3ae30c1b47524002`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdce5f40277a21f604fdbb7966d2529d8b25ac2026cd156bc813cc4d8e0f8c`  
		Last Modified: Sat, 02 Dec 2023 07:01:35 GMT  
		Size: 23.1 MB (23119969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
