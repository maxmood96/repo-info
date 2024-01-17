## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:0b468eb3a871dc7e1414ed6731e5f9be4b53842a9c8c7f1be686cd6a1d3df36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:246f2d8ae89430c056f08108579a4e353350e4d7a23f0de15eebefec16d845ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159764725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f40ace2332806cdd72be8cb35fef9de0cae2632fca66e9257ec14603ebb727`
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

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8e5ffc75f47c47dc9c330095cff0c62306fc784fe73ba575e321dce44daeeb19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155153965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e1356a8ec0ce5b19f900a0d803ef9c09b623a6a3ed154c8ff2ba700abd131a`
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
