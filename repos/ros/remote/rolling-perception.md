## `ros:rolling-perception`

```console
$ docker pull ros@sha256:c3b9de96afd998985405c66768cc2e87343206e53d7d5a9d7e8b3ceaf5f87dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:00c3aea9aad41711ddb60050b8a4d6f1114f8370e3e6460f14653163019ed342
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.0 MB (959952492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6618534412ccce52ecb646d3aa1d11ec218b591d6d46f2e9c6ac5babdea74180`
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
# Wed, 17 Jan 2024 08:32:57 GMT
ENV ROS_DISTRO=rolling
# Wed, 17 Jan 2024 08:33:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:33:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 17 Jan 2024 08:33:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jan 2024 08:33:44 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 08:34:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:34:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Jan 2024 08:34:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 17 Jan 2024 08:34:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:36:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:f5a5659743feffddfb01f87d766890de801c4c7f1a26370239d6e38a43bd22be`  
		Last Modified: Wed, 17 Jan 2024 08:42:17 GMT  
		Size: 124.3 MB (124269922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475cf9b00226572e4cc0bb72978548e1a7fae558c89de2245d1ca2d04adb4498`  
		Last Modified: Wed, 17 Jan 2024 08:41:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae60f0f993902e985f85ef9aa0d3f26e11ad6bad13886051bd9abe2e6393867`  
		Last Modified: Wed, 17 Jan 2024 08:42:36 GMT  
		Size: 85.2 MB (85172823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b5d171117eb251797a29464588be1119e66412866c15daf55e9731b35cf538`  
		Last Modified: Wed, 17 Jan 2024 08:42:26 GMT  
		Size: 303.2 KB (303190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e656bbe6d7203484f91f0f6c9d60a487aa0b4782cbac6b621f4691b712e80cc1`  
		Last Modified: Wed, 17 Jan 2024 08:42:26 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ea7602a43223702ea65d223cb030e2e90b28574a9fb53751879eed15f3c032`  
		Last Modified: Wed, 17 Jan 2024 08:42:30 GMT  
		Size: 23.8 MB (23778663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f3218e7ce1db7d69864c45771e12ceea6eb1c4ec10215bd4c0f1ac945ecd6`  
		Last Modified: Wed, 17 Jan 2024 08:44:17 GMT  
		Size: 690.9 MB (690930584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7171935d5ed34337cbfb97def027cafe538f3edf28ee936915518a12d64ea5ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920225392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055ae91c299149ba632abe1564e2a4062460a1a48faf44926316f0de84d3110d`
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
# Wed, 17 Jan 2024 08:03:46 GMT
ENV ROS_DISTRO=rolling
# Wed, 17 Jan 2024 08:04:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:04:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 17 Jan 2024 08:04:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jan 2024 08:04:29 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 08:04:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:04:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Jan 2024 08:04:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 17 Jan 2024 08:05:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:06:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e58caec8dd087d8e1ed6efc48224598f716cc7976083f6615b8a042d9fc7d467`  
		Last Modified: Wed, 17 Jan 2024 08:12:21 GMT  
		Size: 121.7 MB (121734454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e256a27c5414220858590d5b7c58e4c68917fa9f188d725fa890e9601f8f7110`  
		Last Modified: Wed, 17 Jan 2024 08:12:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8289354b83d1f77bc3ee09caf7cae9cb67742bc196020e2fd6dc005b480204`  
		Last Modified: Wed, 17 Jan 2024 08:12:37 GMT  
		Size: 82.8 MB (82846906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42de26c8903bd9839ea6d485042cb23fe5718f1e03893ec52c8ca9fdc502c82`  
		Last Modified: Wed, 17 Jan 2024 08:12:29 GMT  
		Size: 303.2 KB (303175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efda7125186c8e0c13a562e8c22fc0e56722efba9bc499fc95b602ab9fbe72`  
		Last Modified: Wed, 17 Jan 2024 08:12:28 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f140e0b991ecaafaa31329d324571f0d2ad2c9696ea572c5f7f570767d27d69d`  
		Last Modified: Wed, 17 Jan 2024 08:12:32 GMT  
		Size: 23.2 MB (23164288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6d5b71211fb4848b7c3fd481d9757399e5e5c274c5d1b23e6eea49f0e6a45`  
		Last Modified: Wed, 17 Jan 2024 08:14:03 GMT  
		Size: 658.8 MB (658754572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
