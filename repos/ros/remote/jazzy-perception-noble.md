## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:ae7c5288f5428fbf9c8ef16f008716ea10c3eacaf9c34c9243146c2f428d169a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:93d13d430bde6ab67120af6d1f2d9762a0ecd15e0658dfbd355c40a520737917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1075994110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18634e527c824642340264d5806e8050566df21e011bd4bc7728fde652f39b3d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856e7ce299fcee9f1f0ee919a314c65260713df5a61caabe350642b697b35b11`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 683.8 KB (683821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc18746a5533d47969ff0d25f56bb2b61a3f62151579cd260ac09ca260bd0cac`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.6 MB (3563766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a153b3b139270129259f78f312a065e018a22c46a930c12ab78a2592d4bf169b`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a207cf57c4d6668d75696ca2bc35556218ed85bfbe3dbbd7030e1d6665e1c189`  
		Last Modified: Tue, 03 Jun 2025 13:30:38 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcdf56c08220f4f988aa28ca82d473a8bd0a5242306c12fbfc9c7e18b6ac9d`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 122.9 MB (122913602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4b3cd53cf3537a164c123a0d8254e0b80e52f56035d234a6e65d42be7518b6`  
		Last Modified: Tue, 03 Jun 2025 13:30:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf04a7f9b06fe2a56c215fc10edf46fd90bb41830cd6c87bc8d57ad70c61223`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 110.2 MB (110179225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e937a6fb577cece50c4f88f90863870a324261e9528c79f7637d2001d734734`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 365.5 KB (365549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216314aa5d7e9b6baf300eae6202ded2e9fa7cf9270c1f5eaee88b6b5489842b`  
		Last Modified: Tue, 03 Jun 2025 13:30:36 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2e78128ec2826a9483a8ef34361012afd893f9b34be4be4effc725085b4990`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 28.0 MB (27965546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc075488506156f672f8c855de24ab08153c115c6831fb808388666c586c376f`  
		Last Modified: Tue, 03 Jun 2025 13:35:31 GMT  
		Size: 780.6 MB (780601795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:84be63d480cd0b023280ff4e49781c4ffd268281b4bc5611b5c1866a4f4c0708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbc1614e382829c0b02f77e68e5233b312284fcc0da957369f3a21289fe3589`

```dockerfile
```

-	Layers:
	-	`sha256:5509ad180f49da7940aebb5bfb084f2a224148e5a680f9fa5d9b553c46a0f284`  
		Last Modified: Tue, 03 Jun 2025 16:17:33 GMT  
		Size: 59.8 MB (59848931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab234424b5252b449b20492451972c12264b33773efb0861ffcf1008ec5076a`  
		Last Modified: Tue, 03 Jun 2025 16:17:34 GMT  
		Size: 9.7 KB (9687 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6407036546214510fe15e8534274453157f812c56c7a8c340a0d8e92335aed4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.6 MB (974583884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b3e0fa35b29113ea19fcbd595e5fd4596f16a5a19fd84fb0536365f31356bf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3182864e52220424abbc2ed14f34194efd7a8651cbd58c9013d59badb6ce10bb`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 3.6 MB (3562006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30261ce10ab5a3b7dce5ba78a1a951d5652cbf529e166b904f1bd8067ae7ab`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3ede17908e49502f7fe6ff9399c21b4349b35f3533c331faba1f2970ddeecb`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150505018a99ebf332dac04789ad4a7d39b4e231a8d15f96db811ebcf4e6f83`  
		Last Modified: Tue, 03 Jun 2025 13:31:02 GMT  
		Size: 117.7 MB (117701843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a54c543912af8d6c640321b8e93f681e29172b24dc821c81dd8e1eb9d562a9`  
		Last Modified: Tue, 03 Jun 2025 13:30:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e753917e26be9de671ef2cc8afbe6938606ad95d84796ce47250c6d9d89b8fa`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 105.6 MB (105592211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3329372d459dcc6804f3d709073e87b9de50cd12f0aabd89d54efcf09ce35642`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 365.6 KB (365551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2f748745d1669f8d7ef5c3c3052b08292b9ca9272c01a49f609b7f92a0a620`  
		Last Modified: Tue, 03 Jun 2025 13:30:44 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7efe1143f52f0c17ef6280349b43c537e8b2b5a5e0bf13acf1278f46065faa`  
		Last Modified: Tue, 03 Jun 2025 13:30:59 GMT  
		Size: 27.1 MB (27064554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e4a2603de63f945727820a13386abde4394a44c41d275a60cb45e6e978270`  
		Last Modified: Tue, 03 Jun 2025 16:24:07 GMT  
		Size: 690.8 MB (690756348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:dfd88e35afc1be2b3be83df41527d6f88547180fd4feeb6d48e9f032926f07eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59810364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13b87e8fda725a0b341aff1e19ea44712469c3bec27f75bf63e02d8a28cafa4`

```dockerfile
```

-	Layers:
	-	`sha256:a761d08dc1c7dcceba68cf0d14c12dae18974d65ba024a8ef5cde5eec63524e5`  
		Last Modified: Tue, 03 Jun 2025 16:18:48 GMT  
		Size: 59.8 MB (59800596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e29b8b87193658aa718cea657386bad7356236923710b0780ccefd30383e51b`  
		Last Modified: Tue, 03 Jun 2025 16:18:49 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.in-toto+json
