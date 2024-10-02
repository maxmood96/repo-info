## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:cb27fa84e560382a6b913df155b999d0844738f6b53fe58cd986a98aa05f7fa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:bfd9a73cf1290948eff58aa5af5315e4339358dba332f591b96e50739d91bd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622469546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7ad8f761e45b548b700530d08c6d56bd00162a799cdaedcae148a8b7c66c0b`
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
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0c6c38e15c192672b68d75d6192383f7a919d5d1ff90b8ed1771807316a162b1`  
		Last Modified: Wed, 02 Oct 2024 03:00:13 GMT  
		Size: 114.1 MB (114130061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ef0b3b2aab6184add5a51f40b423ef6a6fa44966f0e1cfa3b6f72177ac68e`  
		Last Modified: Wed, 02 Oct 2024 03:00:10 GMT  
		Size: 322.6 KB (322628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83652cd031f602624bcae5cc022fb8e4769e6c2fbfe21a43be230559644a5391`  
		Last Modified: Wed, 02 Oct 2024 03:00:10 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177231517727644738b63fa94929c8340d19694db793cddf6c44be44f848aa2c`  
		Last Modified: Wed, 02 Oct 2024 03:00:11 GMT  
		Size: 27.5 MB (27532027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c2f1e4eea7409619571f0dac27d7cddfa38aead629603c1f36152fe0fffed7`  
		Last Modified: Wed, 02 Oct 2024 03:59:42 GMT  
		Size: 323.8 MB (323844726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8cb8179a9bd9c396ae2d840f0bf45b39c28e850051c3fcacd9413d5934be22a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42138853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80308d73fd99051824613b38c2d0eafb8a34a81ab12841169cd5345a69c4ec26`

```dockerfile
```

-	Layers:
	-	`sha256:3005687a252bd5b6e9c43696171c029076550ad7f68e9f62b84fe62854e41332`  
		Last Modified: Wed, 02 Oct 2024 03:59:38 GMT  
		Size: 42.1 MB (42129172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25724242417e818dba1666d08678153929e4d998f4a0db1a46388de4a7ececc7`  
		Last Modified: Wed, 02 Oct 2024 03:59:38 GMT  
		Size: 9.7 KB (9681 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:20e76a220322715517981080fee65cdd490b29b208ff7a85f212827a27407e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.6 MB (565575616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94b936d82cac70d4de6b25a5c409f7a9d15df891b7a45b7a0d7243db6955f3a`
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
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:17f8a4f55897eea800d38351218d0e2e6c664b30b0d25991c5a2e330420cbec6`  
		Last Modified: Wed, 02 Oct 2024 06:10:19 GMT  
		Size: 111.0 MB (110969214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a60ff2cdd3f422d1dcc99ca25637a97954cbe329c4da1950d9512111c7e4d2`  
		Last Modified: Wed, 02 Oct 2024 06:10:16 GMT  
		Size: 322.6 KB (322636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3e98785aec8b4135098102e2b9595b11343d0073f8b9cb17eb11a401dda4ec`  
		Last Modified: Wed, 02 Oct 2024 06:10:16 GMT  
		Size: 2.4 KB (2427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174862ae8973943e788bdcc435acfd8ba1165c034cb680f161493958deaa9e52`  
		Last Modified: Wed, 02 Oct 2024 06:10:17 GMT  
		Size: 26.7 MB (26684154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749aab14d8cbace1558fbf0a64fe903adae38a90050b21e7a013982b75424ad`  
		Last Modified: Wed, 02 Oct 2024 07:46:09 GMT  
		Size: 277.0 MB (276991979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d1432e8c5691a14ce840a03eefaf40c3b29030958f1ca77f537ae7778b3c8f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42137026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10040e8897922e38996bdc29a86290ee0ece7051208755ce46a89924bff67ace`

```dockerfile
```

-	Layers:
	-	`sha256:5966705d6f4932db58ee0927f4e50c5d186fd0451bdb1abe8444b011f688aa90`  
		Last Modified: Wed, 02 Oct 2024 07:46:03 GMT  
		Size: 42.1 MB (42127265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89bceebb7a8f48c438f09afa38527b295c619ac7d9899fa5d2bdc94fe434ca9`  
		Last Modified: Wed, 02 Oct 2024 07:46:01 GMT  
		Size: 9.8 KB (9761 bytes)  
		MIME: application/vnd.in-toto+json
