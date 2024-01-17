## `ros:latest`

```console
$ docker pull ros@sha256:32358ce5b8429734427b0df9d84a1e5ca5983cb006c9b25b3262113608ee1721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:52e27b46c352d7ee113f60b05590bb089628a17ef648fff6992ca363c5e14945
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263483592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f3523df2281fb6f394eff31576312717929f5bfe17a8e4c0d99beb7d48cc11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:19:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:19:27 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 17 Jan 2024 08:19:28 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 17 Jan 2024 08:19:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 08:19:28 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Jan 2024 08:19:28 GMT
ENV ROS_DISTRO=humble
# Wed, 17 Jan 2024 08:20:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:20:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 17 Jan 2024 08:20:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jan 2024 08:20:40 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 08:21:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:21:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Jan 2024 08:21:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 17 Jan 2024 08:21:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da4158c1796fdf3290b33130c94d61658490350332349edfc8ce4efb7e40b2`  
		Last Modified: Wed, 17 Jan 2024 08:37:03 GMT  
		Size: 1.2 MB (1216199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b255e5b6ecd708d89a94cf949aa22e792def44df162bda933a732cd23166e`  
		Last Modified: Wed, 17 Jan 2024 08:37:02 GMT  
		Size: 3.8 MB (3828998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b54915a2b753d73bef87bb311bba508a235517ea06f823ed945e7780c6ea501`  
		Last Modified: Wed, 17 Jan 2024 08:37:00 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58126d36f7fcdeee8c0634c3db008d3bd373292caf67204befb405e4be3d24a9`  
		Last Modified: Wed, 17 Jan 2024 08:37:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97700998902fe3cf78ee31dc4b12fb50680c5b89b483b8834fc5c932d39d0618`  
		Last Modified: Wed, 17 Jan 2024 08:37:17 GMT  
		Size: 106.4 MB (106428745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac56751ee73bb7dc9cbfb4e806872e2f392887db15d0ad9ffd727155acb5ee1`  
		Last Modified: Wed, 17 Jan 2024 08:37:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1dc098dfcc8f368164ddc2a6f9cedc7698b90f41899f1b45ac5954a471af31d`  
		Last Modified: Wed, 17 Jan 2024 08:37:39 GMT  
		Size: 98.1 MB (98136867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07a30cafa2e3e8c3647a0db7dd4136a9572ebc37f87d6bb50dbe5a7c446593f`  
		Last Modified: Wed, 17 Jan 2024 08:37:26 GMT  
		Size: 325.4 KB (325357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea0326a92d35837a5d344625fb3c8b5528f9e7992325eb2441c968d0a49c98f`  
		Last Modified: Wed, 17 Jan 2024 08:37:25 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a51f45e64f8b565c257257233be679395c92f8b471e6a3c018fc20b02030e74`  
		Last Modified: Wed, 17 Jan 2024 08:37:29 GMT  
		Size: 23.1 MB (23095311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1dc719929532011dff8a777cd4f411575e7f363eabb60739d38750482afc2c3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256093905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a24884b45bfcfc2d9fdafebbf3728f41bdf95283b33c4e06d44fcea6eeafcd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:48:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:48:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:48:41 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 17 Jan 2024 07:48:42 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 17 Jan 2024 07:48:42 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 07:48:42 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Jan 2024 07:48:42 GMT
ENV ROS_DISTRO=humble
# Wed, 17 Jan 2024 07:49:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:49:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 17 Jan 2024 07:49:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jan 2024 07:49:53 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 07:50:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:50:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Jan 2024 07:50:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 17 Jan 2024 07:50:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4f514e1260adbe3ba8baa42d4f9a9086cbf9299b6d7068882e8d30aa12bcc9`  
		Last Modified: Wed, 17 Jan 2024 08:07:32 GMT  
		Size: 1.2 MB (1216488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d9d057bcf8336ad1f73b5ec5765daed816a52ca71ae19bbd18af57e1a96379`  
		Last Modified: Wed, 17 Jan 2024 08:07:30 GMT  
		Size: 3.8 MB (3800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819b9998df89ce1f731210a11883797f464f3864c0bd79591c8fef249460cd00`  
		Last Modified: Wed, 17 Jan 2024 08:07:29 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fc651ee741faeba360c00a4c5d5afe3336c6b7ae929afb46d5223fc3f1cec9`  
		Last Modified: Wed, 17 Jan 2024 08:07:29 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d60da904ac3e7ba10977fbf3cce0cc59c9cc456b202741181b1289953bb645b`  
		Last Modified: Wed, 17 Jan 2024 08:07:50 GMT  
		Size: 104.1 MB (104144903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5158be10ed797ee6962ad87492a29fc9ff8f0ce6e1d7743fd289d9976638199e`  
		Last Modified: Wed, 17 Jan 2024 08:07:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcedfcc0d17e12a9e018a6dada689bcce11cd94558bb53001879f22a3c12b0f`  
		Last Modified: Wed, 17 Jan 2024 08:08:09 GMT  
		Size: 95.7 MB (95684553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a744fa4869e7e7d5ba6415e9efdaa888a8831f41897d0132d9812c3cb54e49d`  
		Last Modified: Wed, 17 Jan 2024 08:07:58 GMT  
		Size: 325.4 KB (325363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a9f493d20d86f1429681cac261294e79520ad7cce4ce9cb5f39e5970c49f79`  
		Last Modified: Wed, 17 Jan 2024 08:07:58 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ae0ed4358e778ab8d69d8aa558f967f4a9f70b14473a6ffa24a1bbb53012d7`  
		Last Modified: Wed, 17 Jan 2024 08:08:02 GMT  
		Size: 22.5 MB (22517090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
