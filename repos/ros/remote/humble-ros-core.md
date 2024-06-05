## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:d1505884e26c595d0410f4da743ace5ee0d5e8261a6006607dcdbf605d971eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:55bb3916b01217b7274926908328b69ae5c14c75deff49f74f8a9551a7068847
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141994039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2f6be46ffd1566129e707f61e72a52a8551fa520ad81f992959fcd252ed89e`
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
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
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
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c0165a6efc1c0756d8145889db522dc01fe6cb2710649478ce65e2eadc6c426
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137660776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1eee9fb6b724836f7969a80a2e20c7f6af017352d17cc0bd538120cc9d4993`
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
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
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
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
