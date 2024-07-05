## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:156756671f825f68c7936c2241f26278029474ca7989f774decb7cffc4656586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:406f995fef5ec8de51bcf83c34d29b92c15d5a35328b79a6cc72cda2886bc57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211071590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a0d9cd739b1b152a9ecc305fc6a17285a6dacf67686ea1b0bb4a32dd59bdde`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541596f8b358e9f0225f58281f3a5f29192357a2d9eba92a600eb4e7486da20`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 1.2 MB (1198610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904313c44f3c8af3a115d7f73029cf8628f3992e20054ad796c7781e3417adbf`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 5.4 MB (5361726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a0710e8ce116746283a133d532bfc0552b821c541c640314b033605b7efc16`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab8426a021e540c85fbeac7e60cc406e2b6038505811aa7a132de889ee284fb`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb19495c8176c1c1ca74fa7251646aa38ade801d766bc5893d14708c768d452`  
		Last Modified: Fri, 05 Jul 2024 19:58:08 GMT  
		Size: 177.0 MB (176997016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df37cf2580810a1de28e2d3533ee7cee4d9439b281ae37a403f9ed021d1c2c8`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:04a1097c2ea1976b74b26ee1f2bd07b294cf0a04fd7a9bff7e9b9cd7f5318862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26044713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ffe64fc0ed9d0692579308d151cab7195f45ef4f98ac8985104789fce1b2eb`

```dockerfile
```

-	Layers:
	-	`sha256:70cf225b82ce7d40955cdd3a5000a8fb1984f381ed8c610288c77d857d73cd00`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 26.0 MB (26028590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5c21fd839a6e3b6581b8a1a7267ab00554b5bda7f79ec68fd5e20d4217c441`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:7ea2944f49233aa49136153185db5959e6acfd209795adfaf67403b19f479605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186785602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5e76a8a76bd29286c14026097ccc28aa65061dab2502c573a2d21b7410a10f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f30cf37c3fd58825124b0f1bf686ac079d10bcea99ba8b2f6d1b21eacaa54d2`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 1.2 MB (1200145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d046f7fdbe893bfdae348a80dd5560e508012ed4d254d0b451554a52492062`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 4.5 MB (4488723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8c7896dff426ab4df0a37bc9f58570f0376c96a6b25482adba107154dcfca`  
		Last Modified: Fri, 05 Jul 2024 20:02:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68053c27827f8faf9453f43780db0948212bbb2fd5f1cd4bade0f6841a0283c2`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf01d6db61aed61d096a4784518c9f045efa6cc61f20ff23c985ed4b92e77d`  
		Last Modified: Fri, 05 Jul 2024 20:02:18 GMT  
		Size: 157.5 MB (157470886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67194fb46b1c786ab9722506fa148b7c7df2462d50ab143fb103e9e328580345`  
		Last Modified: Fri, 05 Jul 2024 20:02:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:c1132cde1a4e65edac3fbf8d6cbfd9c2814405c2ae229ab62eca34b0dd0843f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25959346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18d0055e1600e729af1ca06899733278fb9363beca4c5ad869d9153fcc8feca`

```dockerfile
```

-	Layers:
	-	`sha256:7a1f5b23e89a758c6f6053ab3bf429e6b1ebf29557a3d68dbff1e98cd8c08f42`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 25.9 MB (25943119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc195ed05ddc13c616d5bafcb17f7a57f8e0fec3fe4a9de875bb559d18f5eb93`  
		Last Modified: Fri, 05 Jul 2024 20:02:13 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b3f3091c2a307515fe9cfeb70961bf8b51fb50d2271a0124d1794c9200d83d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205342947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcdda2db64e31d27975630f071ef7c4c16c8bc08ced9807c40f62a51ed8d41e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
