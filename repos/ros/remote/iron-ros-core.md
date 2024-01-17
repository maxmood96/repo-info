## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:fc0f0e4fed0aee2ff06801a9b978f343a66def69338bad718fb8159d9e20c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1196018f82130d9326c7ce3d1d328ddcfdc324b9acb0e8fc3cff1313792bbc9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159707976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5c0b0a3565227982e09cad68a0ba53bf89f0141e910ec1a68795cf43db72cf`
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
# Wed, 17 Jan 2024 08:29:16 GMT
ENV ROS_DISTRO=iron
# Wed, 17 Jan 2024 08:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:30:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 17 Jan 2024 08:30:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jan 2024 08:30:05 GMT
CMD ["bash"]
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
	-	`sha256:339f3ed03a2333552f0cb64fb2e1842df2e782ec675734afb453557b9ff752f3`  
		Last Modified: Wed, 17 Jan 2024 08:39:48 GMT  
		Size: 124.2 MB (124213172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db72eabeba6f7e8f878873f28b048ff0363ac35c7c3fee28bd8860b3c6fc485`  
		Last Modified: Wed, 17 Jan 2024 08:39:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:88da2d5aacf22b9a5696b32c4173d0ce934cd8a7a02ca8f64cadd6088d269b3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155092911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b36ea929f271f0894ced283452114de3fc4c363f469108ee8c34f26a54d6edb`
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
# Wed, 17 Jan 2024 08:00:15 GMT
ENV ROS_DISTRO=iron
# Wed, 17 Jan 2024 08:01:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:01:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 17 Jan 2024 08:01:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jan 2024 08:01:08 GMT
CMD ["bash"]
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
	-	`sha256:cc579135df7b7535cbaa3d2a4235dea2748621eba9bdd7e6b4fe84f1fe6cba87`  
		Last Modified: Wed, 17 Jan 2024 08:10:12 GMT  
		Size: 121.7 MB (121673399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeceafbe02e3d7785607584d5e90e5f237d19808231228e55d3eadc438c8f1ff`  
		Last Modified: Wed, 17 Jan 2024 08:09:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
