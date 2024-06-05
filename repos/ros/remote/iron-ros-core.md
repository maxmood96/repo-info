## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:b5aa946df59ad6a1373c9eb9a5922f2e1021c7bdd7838f913e7de0c01a1b6c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:54b9b4503b7f616afcf3e48e957afd418f08aacb6dd934af6c29fbb469dbe737
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159757578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0702e44c3057dc0490d6bdc723e1140a79f23c8d02a7869f7e10a9ac4cec9fa0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:06:24 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 06:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:07:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:07:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54e95d67c63dbf0cf8f753642cfe16d08165c0ef6bd6d75b0b04dbca492494`  
		Last Modified: Wed, 05 Jun 2024 06:28:41 GMT  
		Size: 124.3 MB (124271471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178042e3b461503d611ef9ed1a289773f1b1cc2d271d007759b4d512390717a`  
		Last Modified: Wed, 05 Jun 2024 06:28:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f4edcd06dfd87f5ef6cee1fdb2a7894cd2e257394d249d1715e77b7ce3e81d34
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155179954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76990d93dbe0ea01669a568a80f5501b1c7eb2b6706dfc3fb11a0132a026a2c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:29:03 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 05:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:29:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:29:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:29:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2e13045d4af22e2a09809ec5ad219bd0e69a32734c4302f98ed338a2ae3aae`  
		Last Modified: Wed, 05 Jun 2024 05:53:14 GMT  
		Size: 121.8 MB (121755785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad376ac5d1a80d5e0f2c80959f053279c8ed358dde21e81fc687d3c864da7d`  
		Last Modified: Wed, 05 Jun 2024 05:52:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
