## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:469a7ae5a6c4869f8940e736ffadc99c551e926af5bf1ba855003d17f4eade8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:872bcdba24657b7c60e86ff59f67ca485d4feb2f74a13628cc195b25cd4904cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156637650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5674329ee755a152b95dc272381467fc03b0ba6a6f192ed653f75a9b987c1f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7a0c929b90cdbc59c51945e7048addf96d4fe1d056ad03de7f50c53bb3275`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 683.2 KB (683225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b0f84be38266082bf39a65eae2b9ae257266538a89b63f65b773de70a7c94b`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 3.6 MB (3559541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e31627e129edf96cf1d8aa1bdf1803ddcdc1a44632e3dd98212ffec7cee145`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5291007b05b8be4b8b7643e6cd088c9e7a07314b8a45b92ec82c09dedb18dc8a`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf3ed0d059c56b7593399c6cb939d4a2c6032bad2a62c73e1901490d5dec794`  
		Last Modified: Wed, 02 Oct 2024 01:59:17 GMT  
		Size: 122.6 MB (122642555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabf54d65021ba841e554915353f0eab36fe9e3dc62cd759a0a8f8221053badd`  
		Last Modified: Wed, 02 Oct 2024 01:59:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6eaa015c506b5fa1cd5ae0525052e782f99be865e71ec72d3e6988dc2464903f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17823922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5a9665218ca2ebd283905b4921818f328aa112a7795d0a85ee5f65a1c26afe`

```dockerfile
```

-	Layers:
	-	`sha256:bcb7f3a2a0fa9b0aee7f46bac29466e8d5b323922465bcf64a1fccfe6a4591e0`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 17.8 MB (17807777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd196b0f1ffc7df33ca66b5d29456e5541766ca189ab0ad112d78ee4f073fb7`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 16.1 KB (16145 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f7169c9634607f6bcee28d90c6a1b3271139ffde1119b1012be184bf13733331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150605206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6a64c68c915f607c835ea7995ed39ba291df50ac7b114f5b14711a9a1a72b1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729a8513c4ec86780d3d7e8c0d22c4343de25f46d9491c10e38b667b193a52a`  
		Last Modified: Wed, 02 Oct 2024 03:39:11 GMT  
		Size: 683.4 KB (683440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c31f126aab317c208659fa46d07187c05e1d5b12a65a384ba2874f4712c91d6`  
		Last Modified: Wed, 02 Oct 2024 03:39:11 GMT  
		Size: 3.6 MB (3558765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eee2d177bb84dcf907f22436e3fa6e2627496b478315a511ae8595076b8573b`  
		Last Modified: Wed, 02 Oct 2024 03:39:10 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a29dab60a180dac66fb5e855684cdc85b3ed77b9504812b2ec597b9c623242`  
		Last Modified: Wed, 02 Oct 2024 03:39:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0420697c0d4d459eed826f21a285af2cdab39729a3af20e586ae6ec93e3a5e`  
		Last Modified: Wed, 02 Oct 2024 03:40:40 GMT  
		Size: 117.5 MB (117475104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcc451f806caf001c7370e241898a5b972e98108fdb21e0b5a727f0f38643db`  
		Last Modified: Wed, 02 Oct 2024 03:40:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:40592f72459ee968b43d011ed33c0a972e97d01772d303e418e15540154d5fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17798027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e1438a4c82709f7a6899dcad08883341d101b61e219c09982203838f09bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:91edf20d34f3e10a5f7a4c5ea021b230c84bd1b270398f54e5025be54774a1cb`  
		Last Modified: Wed, 02 Oct 2024 03:40:37 GMT  
		Size: 17.8 MB (17781748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2421125d1b05c56ad62a460267ed7bd7815403ebaf1bf56c14257ffb35f213`  
		Last Modified: Wed, 02 Oct 2024 03:40:36 GMT  
		Size: 16.3 KB (16279 bytes)  
		MIME: application/vnd.in-toto+json
