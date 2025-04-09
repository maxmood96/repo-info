<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:iron`](#rosiron)
-	[`ros:iron-perception`](#rosiron-perception)
-	[`ros:iron-perception-jammy`](#rosiron-perception-jammy)
-	[`ros:iron-ros-base`](#rosiron-ros-base)
-	[`ros:iron-ros-base-jammy`](#rosiron-ros-base-jammy)
-	[`ros:iron-ros-core`](#rosiron-ros-core)
-	[`ros:iron-ros-core-jammy`](#rosiron-ros-core-jammy)
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
-	[`ros:latest`](#roslatest)
-	[`ros:noetic`](#rosnoetic)
-	[`ros:noetic-perception`](#rosnoetic-perception)
-	[`ros:noetic-perception-focal`](#rosnoetic-perception-focal)
-	[`ros:noetic-robot`](#rosnoetic-robot)
-	[`ros:noetic-robot-focal`](#rosnoetic-robot-focal)
-	[`ros:noetic-ros-base`](#rosnoetic-ros-base)
-	[`ros:noetic-ros-base-focal`](#rosnoetic-ros-base-focal)
-	[`ros:noetic-ros-core`](#rosnoetic-ros-core)
-	[`ros:noetic-ros-core-focal`](#rosnoetic-ros-core-focal)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:d62c38c84a37900f373d1cb3a8cb222c0ccdd67ede58f96c8188d6d1e999fb53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:e3cbd214e98aed196ef5d3b4e323c10af6bf5342ef11d320e1efc45712775d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262620951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5d1f659ac7727135201b389078359ae7767d2d04ca8aab26d2788db241f64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e736ce0baf9d51b44d5ead6000c34fa440489dcf492ead6c6cb55b64a4fe1`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 1.2 MB (1213930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc958827a8b499b348349b560b1c2798dda767c94207d3a94a10a8b5842ea0e8`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 3.6 MB (3625591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be3271a91fea9ec7a9ed9e2e17342524d3c263ee0e7c90f47539f41c2366eb`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f0b2aa5a5573254ec6d3bfe78b8827d5fb8a246fbaa9c14eeb580e1706398`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59678e0c4abad5e5af5b3f2ee45704cd2fe32b25cc9397c4755eabd9a3ab70ff`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 106.6 MB (106645773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb2caa05f4f7b95a7e3ad2eed0de31749b03afe8f5d79634db56ae3941f8c6`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3e7333b5e1b4fcd5d4aecd09ad2812faf3f30049ec8ab327864fa88c7bc73`  
		Last Modified: Wed, 09 Apr 2025 02:15:59 GMT  
		Size: 98.0 MB (97953544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c39f4ae51aa3b2e4d542c05f9d0c13c67340b4e4b88516615502cd09b2e82bb`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 355.2 KB (355185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f864d4669b570f14537aafc24dd7efa10ef52af27b79201fcf4d400cdca33`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 2.4 KB (2424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a285cb047fd867d8bee762f192a416c3fd3282d1c18157ecb6e83a2cb5c98`  
		Last Modified: Wed, 09 Apr 2025 02:15:57 GMT  
		Size: 23.3 MB (23289667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:d22e9a88e86a32a2e08c96cc323da8b4c5ce51a5511752351e9da602ce59aae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22933284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e1106f5235ef023a4883e8c551acedc1eaafdad5dc07c3829857d4e43b251e`

```dockerfile
```

-	Layers:
	-	`sha256:a116722b5e1252348307628be5a9da8454220d4ebf0c8642c0df697b9422b7c9`  
		Last Modified: Wed, 09 Apr 2025 02:15:57 GMT  
		Size: 22.9 MB (22916128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9eb5cacb90855c303bd44baaa9319b13992078cfab63d15a172d167729e1ea`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5817f87eac1b5e463dd4f3dd78decc90bbe1eb39261b7bd4f03ee2cdf210a762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255070351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3589c9910d672ec29f1ebf429013fb1ae244356d89b2e5b16dc8d03f33da380`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dc6ed59947c90b653cb852244d8678f5c628a0287a08d61ac58f91cd15623e`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f378741874b2ef719a549823a1ad8ac08f65e893d7e78e8c44dd32aa56ac2`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163ae49ef6d582016a4496c4ac205ec01fba6474497e21655b3690b6264a05f`  
		Last Modified: Wed, 09 Apr 2025 09:11:19 GMT  
		Size: 104.4 MB (104357788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec322fe64af860101529ee59c11078c6c4bf13e33bb86cce625573f864fbaaa4`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9335efb50570b40c8e99d4d8ba1626bdd3c483b88821cadcc2c7951e66c934c`  
		Last Modified: Wed, 09 Apr 2025 15:48:35 GMT  
		Size: 95.5 MB (95507833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d00d661fc473ddb2ed4d4c449bee3578a8dbf5dd5c6b94bdd554db62ec7050`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 355.2 KB (355188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe0ab15fb9ec7776a199f2ec6b805bda50bfa4b7f61d62e1260037f014958b`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3f377ab8d078e1d999c61a1a8eabce42d1e4957ec847196cb1d1d486476773`  
		Last Modified: Wed, 09 Apr 2025 15:48:33 GMT  
		Size: 22.7 MB (22679387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:4df6a38e709f23de5c2d8754b1ff1167f1ffb4f27f1402630ce19b55b5a91dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22946437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0028f0354090c0d0a9de7ff41ecb0d66a6ea86c2017ad5c3df5d2d79021a41`

```dockerfile
```

-	Layers:
	-	`sha256:8e2f56d8c76eaa6ea982fdc97b999ac96859c83174e5cd6b102cb1f047d15241`  
		Last Modified: Wed, 09 Apr 2025 15:48:33 GMT  
		Size: 22.9 MB (22929144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a99656880e0c369d368079b3ab8aa00e83e66aa16656804d87d21584db2d70`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:68b8657b661d4e29830f3144809a8a6656daf57c47549c8cdf3147ede480e722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:c24af323b3c93ed1a6ff6ad812d40a768ef5ba5e65558f34c5deca8db239df9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.4 MB (954418270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b6860b87860c8d5da70a10a82aa97a90cedd96b5451f0f47ce74f5674c94ac`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e736ce0baf9d51b44d5ead6000c34fa440489dcf492ead6c6cb55b64a4fe1`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 1.2 MB (1213930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc958827a8b499b348349b560b1c2798dda767c94207d3a94a10a8b5842ea0e8`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 3.6 MB (3625591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be3271a91fea9ec7a9ed9e2e17342524d3c263ee0e7c90f47539f41c2366eb`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f0b2aa5a5573254ec6d3bfe78b8827d5fb8a246fbaa9c14eeb580e1706398`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59678e0c4abad5e5af5b3f2ee45704cd2fe32b25cc9397c4755eabd9a3ab70ff`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 106.6 MB (106645773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb2caa05f4f7b95a7e3ad2eed0de31749b03afe8f5d79634db56ae3941f8c6`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3e7333b5e1b4fcd5d4aecd09ad2812faf3f30049ec8ab327864fa88c7bc73`  
		Last Modified: Wed, 09 Apr 2025 02:15:59 GMT  
		Size: 98.0 MB (97953544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c39f4ae51aa3b2e4d542c05f9d0c13c67340b4e4b88516615502cd09b2e82bb`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 355.2 KB (355185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f864d4669b570f14537aafc24dd7efa10ef52af27b79201fcf4d400cdca33`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 2.4 KB (2424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a285cb047fd867d8bee762f192a416c3fd3282d1c18157ecb6e83a2cb5c98`  
		Last Modified: Wed, 09 Apr 2025 02:15:57 GMT  
		Size: 23.3 MB (23289667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5614adae6eb17faccc3f3b5551aef68519ea2579a1f842c3d5acd2d58b94ce77`  
		Last Modified: Wed, 09 Apr 2025 03:14:32 GMT  
		Size: 691.8 MB (691797319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:8094ae77133205931dc93b60edc0678c5430775ce1a0203b866990b44a87feed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57550700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c855c0c1a741804a9c1f3713d57f9b29144d82f87466626372b5c01c2279fdf5`

```dockerfile
```

-	Layers:
	-	`sha256:058e3270ae56e6e1e7b16239b9c42b5c67e9882a9f678a7f22e2b5af8ea6abe4`  
		Last Modified: Wed, 09 Apr 2025 03:14:20 GMT  
		Size: 57.5 MB (57540999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d17b98fe6d7afbfd835e4f8d6862904171e99184a90080eaaa6b3a3807dfa12`  
		Last Modified: Wed, 09 Apr 2025 03:14:19 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f20ff5afd5447ffedbf85aac8d1e759228160e6dc3e5b463e6d4e7e9597deecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.9 MB (920930825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66015e6af6cb96aa05f610c74b7c52dde9baadd558a846d2bbbf784c0adc8a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926f36c9b7b151d496c801225ee7599eb5a8b9b724136c3f5e16b117476669d`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 1.2 MB (1208081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6a4a0853d9c07e7a7b7e748902799150df963c6d6c838f9689a1221332395`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 3.6 MB (3596329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeeed08a57b27403fa9fe9538ce4160740d4ec04e65be4ed90fbb9ac2bb25df`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf01b92f5fca1f33ea542127260bc8758f57c788ac4d6d9346acea13a47675`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8e209955f92010bb513e324647114f2359e3b4f0c03936550a6734d9f53e4`  
		Last Modified: Mon, 10 Mar 2025 18:24:56 GMT  
		Size: 110.5 MB (110522121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804f4e59511abf9df55102f7c8e0af1ed796adc901b8d302319e1239f269c737`  
		Last Modified: Mon, 10 Mar 2025 18:24:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7508b4e2599475e76914a14ddd797e71dda721ec44f4eaab8bce1a7fb39c0419`  
		Last Modified: Mon, 10 Mar 2025 19:14:23 GMT  
		Size: 95.5 MB (95504266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f37179274d39275f985eb073fab1065c89de9eed79fe218a81beda489d967c`  
		Last Modified: Mon, 10 Mar 2025 19:14:20 GMT  
		Size: 353.9 KB (353944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ff50873b42f1e7360840ce1eb3222c691b624aa3b0c67897c9454dd6c7639`  
		Last Modified: Mon, 10 Mar 2025 19:14:20 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a7b530f1173d3c0eeb841d87100ae95325f1fb5d39bb878125ccd0c01fac3`  
		Last Modified: Mon, 10 Mar 2025 19:14:21 GMT  
		Size: 22.7 MB (22676455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf28ea9806567b9aeb3b1968e7643fc307f6dcf5f5b082897fc88e4b44aaa35`  
		Last Modified: Mon, 10 Mar 2025 20:44:58 GMT  
		Size: 659.7 MB (659706533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:2262f6a3e8850a1fd68cc87528619d79de20591a462e199c4acd30ee0885c1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57531927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc17ce53fe7f7ae521ad02b76a4d02c43e492be56b75fa892f3bd6de8d1e2e32`

```dockerfile
```

-	Layers:
	-	`sha256:a8ddcf8c052cf0372099ef2cd47a09fc2d2466ffb36f34347ac944288daf23c2`  
		Last Modified: Mon, 10 Mar 2025 20:44:44 GMT  
		Size: 57.5 MB (57522146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc1ff8899b4756071e729e5353b523c64fe9bdbc0a518415e26dddc955b3a75`  
		Last Modified: Mon, 10 Mar 2025 20:44:42 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:68b8657b661d4e29830f3144809a8a6656daf57c47549c8cdf3147ede480e722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c24af323b3c93ed1a6ff6ad812d40a768ef5ba5e65558f34c5deca8db239df9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.4 MB (954418270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b6860b87860c8d5da70a10a82aa97a90cedd96b5451f0f47ce74f5674c94ac`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e736ce0baf9d51b44d5ead6000c34fa440489dcf492ead6c6cb55b64a4fe1`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 1.2 MB (1213930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc958827a8b499b348349b560b1c2798dda767c94207d3a94a10a8b5842ea0e8`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 3.6 MB (3625591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be3271a91fea9ec7a9ed9e2e17342524d3c263ee0e7c90f47539f41c2366eb`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f0b2aa5a5573254ec6d3bfe78b8827d5fb8a246fbaa9c14eeb580e1706398`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59678e0c4abad5e5af5b3f2ee45704cd2fe32b25cc9397c4755eabd9a3ab70ff`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 106.6 MB (106645773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb2caa05f4f7b95a7e3ad2eed0de31749b03afe8f5d79634db56ae3941f8c6`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3e7333b5e1b4fcd5d4aecd09ad2812faf3f30049ec8ab327864fa88c7bc73`  
		Last Modified: Wed, 09 Apr 2025 02:15:59 GMT  
		Size: 98.0 MB (97953544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c39f4ae51aa3b2e4d542c05f9d0c13c67340b4e4b88516615502cd09b2e82bb`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 355.2 KB (355185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f864d4669b570f14537aafc24dd7efa10ef52af27b79201fcf4d400cdca33`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 2.4 KB (2424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a285cb047fd867d8bee762f192a416c3fd3282d1c18157ecb6e83a2cb5c98`  
		Last Modified: Wed, 09 Apr 2025 02:15:57 GMT  
		Size: 23.3 MB (23289667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5614adae6eb17faccc3f3b5551aef68519ea2579a1f842c3d5acd2d58b94ce77`  
		Last Modified: Wed, 09 Apr 2025 03:14:32 GMT  
		Size: 691.8 MB (691797319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:8094ae77133205931dc93b60edc0678c5430775ce1a0203b866990b44a87feed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57550700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c855c0c1a741804a9c1f3713d57f9b29144d82f87466626372b5c01c2279fdf5`

```dockerfile
```

-	Layers:
	-	`sha256:058e3270ae56e6e1e7b16239b9c42b5c67e9882a9f678a7f22e2b5af8ea6abe4`  
		Last Modified: Wed, 09 Apr 2025 03:14:20 GMT  
		Size: 57.5 MB (57540999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d17b98fe6d7afbfd835e4f8d6862904171e99184a90080eaaa6b3a3807dfa12`  
		Last Modified: Wed, 09 Apr 2025 03:14:19 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f20ff5afd5447ffedbf85aac8d1e759228160e6dc3e5b463e6d4e7e9597deecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.9 MB (920930825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66015e6af6cb96aa05f610c74b7c52dde9baadd558a846d2bbbf784c0adc8a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926f36c9b7b151d496c801225ee7599eb5a8b9b724136c3f5e16b117476669d`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 1.2 MB (1208081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6a4a0853d9c07e7a7b7e748902799150df963c6d6c838f9689a1221332395`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 3.6 MB (3596329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeeed08a57b27403fa9fe9538ce4160740d4ec04e65be4ed90fbb9ac2bb25df`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf01b92f5fca1f33ea542127260bc8758f57c788ac4d6d9346acea13a47675`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8e209955f92010bb513e324647114f2359e3b4f0c03936550a6734d9f53e4`  
		Last Modified: Mon, 10 Mar 2025 18:24:56 GMT  
		Size: 110.5 MB (110522121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804f4e59511abf9df55102f7c8e0af1ed796adc901b8d302319e1239f269c737`  
		Last Modified: Mon, 10 Mar 2025 18:24:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7508b4e2599475e76914a14ddd797e71dda721ec44f4eaab8bce1a7fb39c0419`  
		Last Modified: Mon, 10 Mar 2025 19:14:23 GMT  
		Size: 95.5 MB (95504266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f37179274d39275f985eb073fab1065c89de9eed79fe218a81beda489d967c`  
		Last Modified: Mon, 10 Mar 2025 19:14:20 GMT  
		Size: 353.9 KB (353944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ff50873b42f1e7360840ce1eb3222c691b624aa3b0c67897c9454dd6c7639`  
		Last Modified: Mon, 10 Mar 2025 19:14:20 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a7b530f1173d3c0eeb841d87100ae95325f1fb5d39bb878125ccd0c01fac3`  
		Last Modified: Mon, 10 Mar 2025 19:14:21 GMT  
		Size: 22.7 MB (22676455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf28ea9806567b9aeb3b1968e7643fc307f6dcf5f5b082897fc88e4b44aaa35`  
		Last Modified: Mon, 10 Mar 2025 20:44:58 GMT  
		Size: 659.7 MB (659706533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:2262f6a3e8850a1fd68cc87528619d79de20591a462e199c4acd30ee0885c1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57531927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc17ce53fe7f7ae521ad02b76a4d02c43e492be56b75fa892f3bd6de8d1e2e32`

```dockerfile
```

-	Layers:
	-	`sha256:a8ddcf8c052cf0372099ef2cd47a09fc2d2466ffb36f34347ac944288daf23c2`  
		Last Modified: Mon, 10 Mar 2025 20:44:44 GMT  
		Size: 57.5 MB (57522146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc1ff8899b4756071e729e5353b523c64fe9bdbc0a518415e26dddc955b3a75`  
		Last Modified: Mon, 10 Mar 2025 20:44:42 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:d62c38c84a37900f373d1cb3a8cb222c0ccdd67ede58f96c8188d6d1e999fb53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e3cbd214e98aed196ef5d3b4e323c10af6bf5342ef11d320e1efc45712775d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262620951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5d1f659ac7727135201b389078359ae7767d2d04ca8aab26d2788db241f64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e736ce0baf9d51b44d5ead6000c34fa440489dcf492ead6c6cb55b64a4fe1`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 1.2 MB (1213930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc958827a8b499b348349b560b1c2798dda767c94207d3a94a10a8b5842ea0e8`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 3.6 MB (3625591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be3271a91fea9ec7a9ed9e2e17342524d3c263ee0e7c90f47539f41c2366eb`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f0b2aa5a5573254ec6d3bfe78b8827d5fb8a246fbaa9c14eeb580e1706398`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59678e0c4abad5e5af5b3f2ee45704cd2fe32b25cc9397c4755eabd9a3ab70ff`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 106.6 MB (106645773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb2caa05f4f7b95a7e3ad2eed0de31749b03afe8f5d79634db56ae3941f8c6`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3e7333b5e1b4fcd5d4aecd09ad2812faf3f30049ec8ab327864fa88c7bc73`  
		Last Modified: Wed, 09 Apr 2025 02:15:59 GMT  
		Size: 98.0 MB (97953544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c39f4ae51aa3b2e4d542c05f9d0c13c67340b4e4b88516615502cd09b2e82bb`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 355.2 KB (355185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f864d4669b570f14537aafc24dd7efa10ef52af27b79201fcf4d400cdca33`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 2.4 KB (2424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a285cb047fd867d8bee762f192a416c3fd3282d1c18157ecb6e83a2cb5c98`  
		Last Modified: Wed, 09 Apr 2025 02:15:57 GMT  
		Size: 23.3 MB (23289667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d22e9a88e86a32a2e08c96cc323da8b4c5ce51a5511752351e9da602ce59aae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22933284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e1106f5235ef023a4883e8c551acedc1eaafdad5dc07c3829857d4e43b251e`

```dockerfile
```

-	Layers:
	-	`sha256:a116722b5e1252348307628be5a9da8454220d4ebf0c8642c0df697b9422b7c9`  
		Last Modified: Wed, 09 Apr 2025 02:15:57 GMT  
		Size: 22.9 MB (22916128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9eb5cacb90855c303bd44baaa9319b13992078cfab63d15a172d167729e1ea`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5817f87eac1b5e463dd4f3dd78decc90bbe1eb39261b7bd4f03ee2cdf210a762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255070351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3589c9910d672ec29f1ebf429013fb1ae244356d89b2e5b16dc8d03f33da380`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dc6ed59947c90b653cb852244d8678f5c628a0287a08d61ac58f91cd15623e`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f378741874b2ef719a549823a1ad8ac08f65e893d7e78e8c44dd32aa56ac2`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163ae49ef6d582016a4496c4ac205ec01fba6474497e21655b3690b6264a05f`  
		Last Modified: Wed, 09 Apr 2025 09:11:19 GMT  
		Size: 104.4 MB (104357788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec322fe64af860101529ee59c11078c6c4bf13e33bb86cce625573f864fbaaa4`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9335efb50570b40c8e99d4d8ba1626bdd3c483b88821cadcc2c7951e66c934c`  
		Last Modified: Wed, 09 Apr 2025 15:48:35 GMT  
		Size: 95.5 MB (95507833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d00d661fc473ddb2ed4d4c449bee3578a8dbf5dd5c6b94bdd554db62ec7050`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 355.2 KB (355188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe0ab15fb9ec7776a199f2ec6b805bda50bfa4b7f61d62e1260037f014958b`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3f377ab8d078e1d999c61a1a8eabce42d1e4957ec847196cb1d1d486476773`  
		Last Modified: Wed, 09 Apr 2025 15:48:33 GMT  
		Size: 22.7 MB (22679387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:4df6a38e709f23de5c2d8754b1ff1167f1ffb4f27f1402630ce19b55b5a91dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22946437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0028f0354090c0d0a9de7ff41ecb0d66a6ea86c2017ad5c3df5d2d79021a41`

```dockerfile
```

-	Layers:
	-	`sha256:8e2f56d8c76eaa6ea982fdc97b999ac96859c83174e5cd6b102cb1f047d15241`  
		Last Modified: Wed, 09 Apr 2025 15:48:33 GMT  
		Size: 22.9 MB (22929144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a99656880e0c369d368079b3ab8aa00e83e66aa16656804d87d21584db2d70`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:d62c38c84a37900f373d1cb3a8cb222c0ccdd67ede58f96c8188d6d1e999fb53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:e3cbd214e98aed196ef5d3b4e323c10af6bf5342ef11d320e1efc45712775d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262620951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c5d1f659ac7727135201b389078359ae7767d2d04ca8aab26d2788db241f64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e736ce0baf9d51b44d5ead6000c34fa440489dcf492ead6c6cb55b64a4fe1`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 1.2 MB (1213930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc958827a8b499b348349b560b1c2798dda767c94207d3a94a10a8b5842ea0e8`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 3.6 MB (3625591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be3271a91fea9ec7a9ed9e2e17342524d3c263ee0e7c90f47539f41c2366eb`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f0b2aa5a5573254ec6d3bfe78b8827d5fb8a246fbaa9c14eeb580e1706398`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59678e0c4abad5e5af5b3f2ee45704cd2fe32b25cc9397c4755eabd9a3ab70ff`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 106.6 MB (106645773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb2caa05f4f7b95a7e3ad2eed0de31749b03afe8f5d79634db56ae3941f8c6`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b3e7333b5e1b4fcd5d4aecd09ad2812faf3f30049ec8ab327864fa88c7bc73`  
		Last Modified: Wed, 09 Apr 2025 02:15:59 GMT  
		Size: 98.0 MB (97953544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c39f4ae51aa3b2e4d542c05f9d0c13c67340b4e4b88516615502cd09b2e82bb`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 355.2 KB (355185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74f864d4669b570f14537aafc24dd7efa10ef52af27b79201fcf4d400cdca33`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 2.4 KB (2424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a285cb047fd867d8bee762f192a416c3fd3282d1c18157ecb6e83a2cb5c98`  
		Last Modified: Wed, 09 Apr 2025 02:15:57 GMT  
		Size: 23.3 MB (23289667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:d22e9a88e86a32a2e08c96cc323da8b4c5ce51a5511752351e9da602ce59aae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22933284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e1106f5235ef023a4883e8c551acedc1eaafdad5dc07c3829857d4e43b251e`

```dockerfile
```

-	Layers:
	-	`sha256:a116722b5e1252348307628be5a9da8454220d4ebf0c8642c0df697b9422b7c9`  
		Last Modified: Wed, 09 Apr 2025 02:15:57 GMT  
		Size: 22.9 MB (22916128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9eb5cacb90855c303bd44baaa9319b13992078cfab63d15a172d167729e1ea`  
		Last Modified: Wed, 09 Apr 2025 02:15:56 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5817f87eac1b5e463dd4f3dd78decc90bbe1eb39261b7bd4f03ee2cdf210a762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255070351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3589c9910d672ec29f1ebf429013fb1ae244356d89b2e5b16dc8d03f33da380`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dc6ed59947c90b653cb852244d8678f5c628a0287a08d61ac58f91cd15623e`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f378741874b2ef719a549823a1ad8ac08f65e893d7e78e8c44dd32aa56ac2`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163ae49ef6d582016a4496c4ac205ec01fba6474497e21655b3690b6264a05f`  
		Last Modified: Wed, 09 Apr 2025 09:11:19 GMT  
		Size: 104.4 MB (104357788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec322fe64af860101529ee59c11078c6c4bf13e33bb86cce625573f864fbaaa4`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9335efb50570b40c8e99d4d8ba1626bdd3c483b88821cadcc2c7951e66c934c`  
		Last Modified: Wed, 09 Apr 2025 15:48:35 GMT  
		Size: 95.5 MB (95507833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d00d661fc473ddb2ed4d4c449bee3578a8dbf5dd5c6b94bdd554db62ec7050`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 355.2 KB (355188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe0ab15fb9ec7776a199f2ec6b805bda50bfa4b7f61d62e1260037f014958b`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3f377ab8d078e1d999c61a1a8eabce42d1e4957ec847196cb1d1d486476773`  
		Last Modified: Wed, 09 Apr 2025 15:48:33 GMT  
		Size: 22.7 MB (22679387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4df6a38e709f23de5c2d8754b1ff1167f1ffb4f27f1402630ce19b55b5a91dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22946437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0028f0354090c0d0a9de7ff41ecb0d66a6ea86c2017ad5c3df5d2d79021a41`

```dockerfile
```

-	Layers:
	-	`sha256:8e2f56d8c76eaa6ea982fdc97b999ac96859c83174e5cd6b102cb1f047d15241`  
		Last Modified: Wed, 09 Apr 2025 15:48:33 GMT  
		Size: 22.9 MB (22929144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a99656880e0c369d368079b3ab8aa00e83e66aa16656804d87d21584db2d70`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:5ce697976d4fd5e209e3825f259c0739200806a2ae7b121d9987906b904e09cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c70abc7df27d282a393c3223f9f73a69fa8b5621aca238d7c53e9cbff0d203bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141020131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369ad11ee949de80e1372e3cffe6af698d8f3389145bc60aa8e912d4c76d5c55`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=humble
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e736ce0baf9d51b44d5ead6000c34fa440489dcf492ead6c6cb55b64a4fe1`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 1.2 MB (1213930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc958827a8b499b348349b560b1c2798dda767c94207d3a94a10a8b5842ea0e8`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 3.6 MB (3625591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be3271a91fea9ec7a9ed9e2e17342524d3c263ee0e7c90f47539f41c2366eb`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f0b2aa5a5573254ec6d3bfe78b8827d5fb8a246fbaa9c14eeb580e1706398`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59678e0c4abad5e5af5b3f2ee45704cd2fe32b25cc9397c4755eabd9a3ab70ff`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 106.6 MB (106645773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb2caa05f4f7b95a7e3ad2eed0de31749b03afe8f5d79634db56ae3941f8c6`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:89173ee0f9c4d3581784ecab2746e1ca759e449535ddcf4d16224c571df6c954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17148109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec3eee04982c4e1ebeea2c756bd1ac846999547715b38008b7d40e2bb5d1a02`

```dockerfile
```

-	Layers:
	-	`sha256:8c9b2c9c0e5f161d016dae18c3e2b5cbf659b6f7b0b07b84f42c8b43a04c0d85`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 17.1 MB (17131718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc16592db763361b1548111e815c0274d7aed3c96b32c63b53b42b1ca6238a9`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3feb7c459f5991a1568c6a6d82cb336d0b9b25e5ec371f8da8fdabc3045aa579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136525481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773cd12d5e31f9469bc697d60320acd00efc798ddd0e9cd8441d0f02b6c1a7f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=humble
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dc6ed59947c90b653cb852244d8678f5c628a0287a08d61ac58f91cd15623e`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f378741874b2ef719a549823a1ad8ac08f65e893d7e78e8c44dd32aa56ac2`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163ae49ef6d582016a4496c4ac205ec01fba6474497e21655b3690b6264a05f`  
		Last Modified: Wed, 09 Apr 2025 09:11:19 GMT  
		Size: 104.4 MB (104357788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec322fe64af860101529ee59c11078c6c4bf13e33bb86cce625573f864fbaaa4`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:61b74c7be27d67ab3b5688f60aea9889d9d424d8892d91f49a6d1eb60311117f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78b68f5ef47a2e513977f761abfaf4f6f43460603d897607cbd5231ad869374`

```dockerfile
```

-	Layers:
	-	`sha256:87e9a14e64adc2dc579476cf17fe7f89ac718d8ec98a7154540d934aa334ec31`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 17.1 MB (17118357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75677f13111d09237b2b388d308f30590a4454c7792c27aeca0593645090a27c`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:5ce697976d4fd5e209e3825f259c0739200806a2ae7b121d9987906b904e09cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c70abc7df27d282a393c3223f9f73a69fa8b5621aca238d7c53e9cbff0d203bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141020131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369ad11ee949de80e1372e3cffe6af698d8f3389145bc60aa8e912d4c76d5c55`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=humble
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e736ce0baf9d51b44d5ead6000c34fa440489dcf492ead6c6cb55b64a4fe1`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 1.2 MB (1213930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc958827a8b499b348349b560b1c2798dda767c94207d3a94a10a8b5842ea0e8`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 3.6 MB (3625591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be3271a91fea9ec7a9ed9e2e17342524d3c263ee0e7c90f47539f41c2366eb`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f0b2aa5a5573254ec6d3bfe78b8827d5fb8a246fbaa9c14eeb580e1706398`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59678e0c4abad5e5af5b3f2ee45704cd2fe32b25cc9397c4755eabd9a3ab70ff`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 106.6 MB (106645773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb2caa05f4f7b95a7e3ad2eed0de31749b03afe8f5d79634db56ae3941f8c6`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:89173ee0f9c4d3581784ecab2746e1ca759e449535ddcf4d16224c571df6c954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17148109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec3eee04982c4e1ebeea2c756bd1ac846999547715b38008b7d40e2bb5d1a02`

```dockerfile
```

-	Layers:
	-	`sha256:8c9b2c9c0e5f161d016dae18c3e2b5cbf659b6f7b0b07b84f42c8b43a04c0d85`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 17.1 MB (17131718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc16592db763361b1548111e815c0274d7aed3c96b32c63b53b42b1ca6238a9`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3feb7c459f5991a1568c6a6d82cb336d0b9b25e5ec371f8da8fdabc3045aa579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136525481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773cd12d5e31f9469bc697d60320acd00efc798ddd0e9cd8441d0f02b6c1a7f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=humble
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dc6ed59947c90b653cb852244d8678f5c628a0287a08d61ac58f91cd15623e`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f378741874b2ef719a549823a1ad8ac08f65e893d7e78e8c44dd32aa56ac2`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163ae49ef6d582016a4496c4ac205ec01fba6474497e21655b3690b6264a05f`  
		Last Modified: Wed, 09 Apr 2025 09:11:19 GMT  
		Size: 104.4 MB (104357788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec322fe64af860101529ee59c11078c6c4bf13e33bb86cce625573f864fbaaa4`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:61b74c7be27d67ab3b5688f60aea9889d9d424d8892d91f49a6d1eb60311117f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78b68f5ef47a2e513977f761abfaf4f6f43460603d897607cbd5231ad869374`

```dockerfile
```

-	Layers:
	-	`sha256:87e9a14e64adc2dc579476cf17fe7f89ac718d8ec98a7154540d934aa334ec31`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 17.1 MB (17118357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75677f13111d09237b2b388d308f30590a4454c7792c27aeca0593645090a27c`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron`

```console
$ docker pull ros@sha256:dad3689190929a744c752e22afc537941281589319cf8ddc53dace56e4e77c08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:cbc62dcad96543658418e453f653564b1d2de9f7e07c1c364677d30c875d93e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267783981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8667f453785555730325cc280970ff18ff8faf60032d2162ff1e20fd14bf175a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925f3794b44a9c41a9dca97fc337e0c078057b6b8c8e08cb8589fda8c1aa1c8c`  
		Last Modified: Wed, 09 Apr 2025 02:16:08 GMT  
		Size: 85.0 MB (84978995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacefee13185173d4ff01dd7548b15ef2db6729cb16fd3a87143b1971b05eef7`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 326.3 KB (326342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40fa4dc66e5a94bf73c46024d39ad45c210cd3922fe6551205e89fdff9f6b83`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bdc7458748f6ca3dfa37fda6f04b5681ee7af8822f522ebad0672c98b74a6e`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23734603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:512f1d9c9af4c68806f7ae6dbe8005fe8c8cc6d82b482631f8212ac27a61df8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23738300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fd46e65de82e8225ea0ea59699f2c7cdae83bff91ef51ff473607bd60408b1`

```dockerfile
```

-	Layers:
	-	`sha256:0558e1beb895c5631840e7f9cdc870aece52f165285a0db85baab88ffb3578d9`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23721176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c955dfa67de3fc24d7d948c5a54362876c9f6d9b3317cf3a6160053b424a4d`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 17.1 KB (17124 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2c9bc845b2e32ac28aea3c87a434a0e0a003d3121df0a3c7a292d9f6a3a36a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260106494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1eb46fb86bc04f694d3c32d991a6d78eb43d4cf3101280616e02762cc4bf353`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203623a863f43e1e4b881948129cab8d7bea8980b186a2d5f73e12abefec75d1`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc3526ae0181f5bb51d08158c52a09b96e0f34319c8364f538ceb688698cf50`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec78c40c286de9039f4431dff10337f00059c57c3081b33d466230bb34c6168`  
		Last Modified: Wed, 09 Apr 2025 09:13:03 GMT  
		Size: 121.8 MB (121827814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5e3f6f19fdee885ac03b2133333e7dd66ccf52adc2d22fdc1c85140516d6f8`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf78a7404654cefd6c73cdea6c92c9504507fb337d1b192c319f5ebe576a1d6b`  
		Last Modified: Wed, 09 Apr 2025 15:50:16 GMT  
		Size: 82.7 MB (82653174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc443957dc455b1a1b37a2ee16ee89f84b943588123e09669f383265d60ad47`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 326.3 KB (326346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f136d44d7462d06b25723dc55af10787ae5eee9327affd0edfe09ac6ecf6488`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b176733e755d05394cf45d34f8bad771ac2328c723da26437741a03c84b041`  
		Last Modified: Wed, 09 Apr 2025 15:50:14 GMT  
		Size: 23.1 MB (23127398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:d3cd64e42592e0e7ce725ceccc8192b25dcfc56eb1b5cdb1d00f334849b6ffac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23751636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7b91c77dae12c4d830848562854e2221d6363f130b7995b6321dcb6d9fb6c`

```dockerfile
```

-	Layers:
	-	`sha256:62d7fe04ef80474d978763c35f0eec010b16a3db7a78fef0930391e2b0b62cf6`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 23.7 MB (23734375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22c8cddd75c64cc105847d3fae0700a846c44599589251903698b241e95db28`  
		Last Modified: Wed, 09 Apr 2025 15:50:12 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-perception`

```console
$ docker pull ros@sha256:d1a2b33bdcd099e3565d9e4f2a39529abe460f2395c3a2f6820a92201c6af462
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:527d413b7a38527c8ede72afda05120c09a53da68cb9878bb29caab384d170ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.2 MB (960245890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e703c5b2ab8d143a5edaac7528296e4c39d5fe28fda627b61f2db47effff0cf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925f3794b44a9c41a9dca97fc337e0c078057b6b8c8e08cb8589fda8c1aa1c8c`  
		Last Modified: Wed, 09 Apr 2025 02:16:08 GMT  
		Size: 85.0 MB (84978995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacefee13185173d4ff01dd7548b15ef2db6729cb16fd3a87143b1971b05eef7`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 326.3 KB (326342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40fa4dc66e5a94bf73c46024d39ad45c210cd3922fe6551205e89fdff9f6b83`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bdc7458748f6ca3dfa37fda6f04b5681ee7af8822f522ebad0672c98b74a6e`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23734603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb51f26a8b26812a2523ac94a4b24d2f93d58f1ecfe70f1cb6e42c3e58b8d276`  
		Last Modified: Wed, 09 Apr 2025 03:14:44 GMT  
		Size: 692.5 MB (692461909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:bc1a5e055290e92dcea49441cb61b69c60ff5ec03ca6b26789031932eb4bd66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58344159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d43f1af5c5bc3fa785f0b17ecbf0d8afdcca3c08f5ff93827ec6162204923e`

```dockerfile
```

-	Layers:
	-	`sha256:08f818f83b45126a611bbbb8fb31de67529ea2897ffae0963ba1640e52d972c1`  
		Last Modified: Wed, 09 Apr 2025 03:14:31 GMT  
		Size: 58.3 MB (58334484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200ec83f06dd4d7a37297f6efb7392a536e05a259aaa21801256cb8575acbd8d`  
		Last Modified: Wed, 09 Apr 2025 03:14:31 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cbaa86e8a45585b2bcbc690a52c1b2798129bf4047dd474617ebe0c8f1ec3320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **926.6 MB (926620069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894e004ccca54067200332367d17da5bdbd641fc8825b78223361c663d973388`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926f36c9b7b151d496c801225ee7599eb5a8b9b724136c3f5e16b117476669d`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 1.2 MB (1208081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6a4a0853d9c07e7a7b7e748902799150df963c6d6c838f9689a1221332395`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 3.6 MB (3596329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d7b8158f3e4d0bc00f0b83b4f7652632ca53aa97593b50614e361a8057b00`  
		Last Modified: Mon, 10 Mar 2025 18:23:23 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95bfa72cbcd78f679175ba71dd1855fc3b7d01686c288428c1ad9a99e928d5`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad630b2a2b3a1b904d5d02d598bffc5bf6b3a0f69e400bc074b2aab1de0843`  
		Last Modified: Mon, 10 Mar 2025 18:23:28 GMT  
		Size: 128.0 MB (128007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18262b00390f040cf294eaa509d4f779a9ffbf41db0b492fe510f0f29a3f3e4c`  
		Last Modified: Mon, 10 Mar 2025 18:23:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5c7877c93243b37cf8b45f86ec8b6290502659cbe29af959c30149f5c60a06`  
		Last Modified: Mon, 10 Mar 2025 19:16:04 GMT  
		Size: 82.7 MB (82654646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a812bd506442907c24e01b27b154cd30e8a55e68af94b0fc14284e66b5e308`  
		Last Modified: Mon, 10 Mar 2025 19:15:49 GMT  
		Size: 325.7 KB (325737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68ac77cafd0228867e12f7999aa66b727821f31bae2a8832b99adfddc8294e`  
		Last Modified: Mon, 10 Mar 2025 19:15:49 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a279769da580b8f51b38b6159e86548d6be6d076b0f43cfd7b70e9f4984c2`  
		Last Modified: Mon, 10 Mar 2025 19:15:51 GMT  
		Size: 23.1 MB (23128942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2ce3bda5312ffaae67b78c7660f99036e413fce80b39f4a853905c961e0ca8`  
		Last Modified: Mon, 10 Mar 2025 21:11:09 GMT  
		Size: 660.3 MB (660334235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:39e7c87ef52a014ec74aca2afd7b624ee21660721f2d0f305a1a16daa1be91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58340015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b82336b15144e78628795bb2eae49545aed07639c3f8cfc9ccc1b3a3209bf3`

```dockerfile
```

-	Layers:
	-	`sha256:e0d4c4c9c8d66e31a7e0f4680b7117bcbd372a7a8b9793d274cd686b35c619a1`  
		Last Modified: Mon, 10 Mar 2025 21:10:52 GMT  
		Size: 58.3 MB (58330260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6997ed05957d94ed34d7f0542e622c353fd198aae8c01212c2d3299f04f63f21`  
		Last Modified: Mon, 10 Mar 2025 21:10:50 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:d1a2b33bdcd099e3565d9e4f2a39529abe460f2395c3a2f6820a92201c6af462
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:527d413b7a38527c8ede72afda05120c09a53da68cb9878bb29caab384d170ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.2 MB (960245890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e703c5b2ab8d143a5edaac7528296e4c39d5fe28fda627b61f2db47effff0cf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925f3794b44a9c41a9dca97fc337e0c078057b6b8c8e08cb8589fda8c1aa1c8c`  
		Last Modified: Wed, 09 Apr 2025 02:16:08 GMT  
		Size: 85.0 MB (84978995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacefee13185173d4ff01dd7548b15ef2db6729cb16fd3a87143b1971b05eef7`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 326.3 KB (326342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40fa4dc66e5a94bf73c46024d39ad45c210cd3922fe6551205e89fdff9f6b83`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bdc7458748f6ca3dfa37fda6f04b5681ee7af8822f522ebad0672c98b74a6e`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23734603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb51f26a8b26812a2523ac94a4b24d2f93d58f1ecfe70f1cb6e42c3e58b8d276`  
		Last Modified: Wed, 09 Apr 2025 03:14:44 GMT  
		Size: 692.5 MB (692461909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:bc1a5e055290e92dcea49441cb61b69c60ff5ec03ca6b26789031932eb4bd66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58344159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d43f1af5c5bc3fa785f0b17ecbf0d8afdcca3c08f5ff93827ec6162204923e`

```dockerfile
```

-	Layers:
	-	`sha256:08f818f83b45126a611bbbb8fb31de67529ea2897ffae0963ba1640e52d972c1`  
		Last Modified: Wed, 09 Apr 2025 03:14:31 GMT  
		Size: 58.3 MB (58334484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200ec83f06dd4d7a37297f6efb7392a536e05a259aaa21801256cb8575acbd8d`  
		Last Modified: Wed, 09 Apr 2025 03:14:31 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cbaa86e8a45585b2bcbc690a52c1b2798129bf4047dd474617ebe0c8f1ec3320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **926.6 MB (926620069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894e004ccca54067200332367d17da5bdbd641fc8825b78223361c663d973388`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926f36c9b7b151d496c801225ee7599eb5a8b9b724136c3f5e16b117476669d`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 1.2 MB (1208081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6a4a0853d9c07e7a7b7e748902799150df963c6d6c838f9689a1221332395`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 3.6 MB (3596329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d7b8158f3e4d0bc00f0b83b4f7652632ca53aa97593b50614e361a8057b00`  
		Last Modified: Mon, 10 Mar 2025 18:23:23 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95bfa72cbcd78f679175ba71dd1855fc3b7d01686c288428c1ad9a99e928d5`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad630b2a2b3a1b904d5d02d598bffc5bf6b3a0f69e400bc074b2aab1de0843`  
		Last Modified: Mon, 10 Mar 2025 18:23:28 GMT  
		Size: 128.0 MB (128007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18262b00390f040cf294eaa509d4f779a9ffbf41db0b492fe510f0f29a3f3e4c`  
		Last Modified: Mon, 10 Mar 2025 18:23:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5c7877c93243b37cf8b45f86ec8b6290502659cbe29af959c30149f5c60a06`  
		Last Modified: Mon, 10 Mar 2025 19:16:04 GMT  
		Size: 82.7 MB (82654646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a812bd506442907c24e01b27b154cd30e8a55e68af94b0fc14284e66b5e308`  
		Last Modified: Mon, 10 Mar 2025 19:15:49 GMT  
		Size: 325.7 KB (325737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68ac77cafd0228867e12f7999aa66b727821f31bae2a8832b99adfddc8294e`  
		Last Modified: Mon, 10 Mar 2025 19:15:49 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a279769da580b8f51b38b6159e86548d6be6d076b0f43cfd7b70e9f4984c2`  
		Last Modified: Mon, 10 Mar 2025 19:15:51 GMT  
		Size: 23.1 MB (23128942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2ce3bda5312ffaae67b78c7660f99036e413fce80b39f4a853905c961e0ca8`  
		Last Modified: Mon, 10 Mar 2025 21:11:09 GMT  
		Size: 660.3 MB (660334235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:39e7c87ef52a014ec74aca2afd7b624ee21660721f2d0f305a1a16daa1be91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58340015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b82336b15144e78628795bb2eae49545aed07639c3f8cfc9ccc1b3a3209bf3`

```dockerfile
```

-	Layers:
	-	`sha256:e0d4c4c9c8d66e31a7e0f4680b7117bcbd372a7a8b9793d274cd686b35c619a1`  
		Last Modified: Mon, 10 Mar 2025 21:10:52 GMT  
		Size: 58.3 MB (58330260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6997ed05957d94ed34d7f0542e622c353fd198aae8c01212c2d3299f04f63f21`  
		Last Modified: Mon, 10 Mar 2025 21:10:50 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:dad3689190929a744c752e22afc537941281589319cf8ddc53dace56e4e77c08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:cbc62dcad96543658418e453f653564b1d2de9f7e07c1c364677d30c875d93e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267783981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8667f453785555730325cc280970ff18ff8faf60032d2162ff1e20fd14bf175a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925f3794b44a9c41a9dca97fc337e0c078057b6b8c8e08cb8589fda8c1aa1c8c`  
		Last Modified: Wed, 09 Apr 2025 02:16:08 GMT  
		Size: 85.0 MB (84978995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacefee13185173d4ff01dd7548b15ef2db6729cb16fd3a87143b1971b05eef7`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 326.3 KB (326342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40fa4dc66e5a94bf73c46024d39ad45c210cd3922fe6551205e89fdff9f6b83`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bdc7458748f6ca3dfa37fda6f04b5681ee7af8822f522ebad0672c98b74a6e`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23734603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:512f1d9c9af4c68806f7ae6dbe8005fe8c8cc6d82b482631f8212ac27a61df8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23738300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fd46e65de82e8225ea0ea59699f2c7cdae83bff91ef51ff473607bd60408b1`

```dockerfile
```

-	Layers:
	-	`sha256:0558e1beb895c5631840e7f9cdc870aece52f165285a0db85baab88ffb3578d9`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23721176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c955dfa67de3fc24d7d948c5a54362876c9f6d9b3317cf3a6160053b424a4d`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 17.1 KB (17124 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2c9bc845b2e32ac28aea3c87a434a0e0a003d3121df0a3c7a292d9f6a3a36a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260106494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1eb46fb86bc04f694d3c32d991a6d78eb43d4cf3101280616e02762cc4bf353`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203623a863f43e1e4b881948129cab8d7bea8980b186a2d5f73e12abefec75d1`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc3526ae0181f5bb51d08158c52a09b96e0f34319c8364f538ceb688698cf50`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec78c40c286de9039f4431dff10337f00059c57c3081b33d466230bb34c6168`  
		Last Modified: Wed, 09 Apr 2025 09:13:03 GMT  
		Size: 121.8 MB (121827814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5e3f6f19fdee885ac03b2133333e7dd66ccf52adc2d22fdc1c85140516d6f8`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf78a7404654cefd6c73cdea6c92c9504507fb337d1b192c319f5ebe576a1d6b`  
		Last Modified: Wed, 09 Apr 2025 15:50:16 GMT  
		Size: 82.7 MB (82653174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc443957dc455b1a1b37a2ee16ee89f84b943588123e09669f383265d60ad47`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 326.3 KB (326346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f136d44d7462d06b25723dc55af10787ae5eee9327affd0edfe09ac6ecf6488`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b176733e755d05394cf45d34f8bad771ac2328c723da26437741a03c84b041`  
		Last Modified: Wed, 09 Apr 2025 15:50:14 GMT  
		Size: 23.1 MB (23127398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d3cd64e42592e0e7ce725ceccc8192b25dcfc56eb1b5cdb1d00f334849b6ffac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23751636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7b91c77dae12c4d830848562854e2221d6363f130b7995b6321dcb6d9fb6c`

```dockerfile
```

-	Layers:
	-	`sha256:62d7fe04ef80474d978763c35f0eec010b16a3db7a78fef0930391e2b0b62cf6`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 23.7 MB (23734375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22c8cddd75c64cc105847d3fae0700a846c44599589251903698b241e95db28`  
		Last Modified: Wed, 09 Apr 2025 15:50:12 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:dad3689190929a744c752e22afc537941281589319cf8ddc53dace56e4e77c08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:cbc62dcad96543658418e453f653564b1d2de9f7e07c1c364677d30c875d93e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267783981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8667f453785555730325cc280970ff18ff8faf60032d2162ff1e20fd14bf175a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925f3794b44a9c41a9dca97fc337e0c078057b6b8c8e08cb8589fda8c1aa1c8c`  
		Last Modified: Wed, 09 Apr 2025 02:16:08 GMT  
		Size: 85.0 MB (84978995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacefee13185173d4ff01dd7548b15ef2db6729cb16fd3a87143b1971b05eef7`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 326.3 KB (326342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40fa4dc66e5a94bf73c46024d39ad45c210cd3922fe6551205e89fdff9f6b83`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bdc7458748f6ca3dfa37fda6f04b5681ee7af8822f522ebad0672c98b74a6e`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23734603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:512f1d9c9af4c68806f7ae6dbe8005fe8c8cc6d82b482631f8212ac27a61df8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23738300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fd46e65de82e8225ea0ea59699f2c7cdae83bff91ef51ff473607bd60408b1`

```dockerfile
```

-	Layers:
	-	`sha256:0558e1beb895c5631840e7f9cdc870aece52f165285a0db85baab88ffb3578d9`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23721176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c955dfa67de3fc24d7d948c5a54362876c9f6d9b3317cf3a6160053b424a4d`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 17.1 KB (17124 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2c9bc845b2e32ac28aea3c87a434a0e0a003d3121df0a3c7a292d9f6a3a36a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260106494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1eb46fb86bc04f694d3c32d991a6d78eb43d4cf3101280616e02762cc4bf353`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203623a863f43e1e4b881948129cab8d7bea8980b186a2d5f73e12abefec75d1`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc3526ae0181f5bb51d08158c52a09b96e0f34319c8364f538ceb688698cf50`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec78c40c286de9039f4431dff10337f00059c57c3081b33d466230bb34c6168`  
		Last Modified: Wed, 09 Apr 2025 09:13:03 GMT  
		Size: 121.8 MB (121827814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5e3f6f19fdee885ac03b2133333e7dd66ccf52adc2d22fdc1c85140516d6f8`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf78a7404654cefd6c73cdea6c92c9504507fb337d1b192c319f5ebe576a1d6b`  
		Last Modified: Wed, 09 Apr 2025 15:50:16 GMT  
		Size: 82.7 MB (82653174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc443957dc455b1a1b37a2ee16ee89f84b943588123e09669f383265d60ad47`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 326.3 KB (326346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f136d44d7462d06b25723dc55af10787ae5eee9327affd0edfe09ac6ecf6488`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b176733e755d05394cf45d34f8bad771ac2328c723da26437741a03c84b041`  
		Last Modified: Wed, 09 Apr 2025 15:50:14 GMT  
		Size: 23.1 MB (23127398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:d3cd64e42592e0e7ce725ceccc8192b25dcfc56eb1b5cdb1d00f334849b6ffac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23751636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7b91c77dae12c4d830848562854e2221d6363f130b7995b6321dcb6d9fb6c`

```dockerfile
```

-	Layers:
	-	`sha256:62d7fe04ef80474d978763c35f0eec010b16a3db7a78fef0930391e2b0b62cf6`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 23.7 MB (23734375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22c8cddd75c64cc105847d3fae0700a846c44599589251903698b241e95db28`  
		Last Modified: Wed, 09 Apr 2025 15:50:12 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:e6f605d0f86aaf1e3da8d7a8d618a38cb65ba6ff8183e6d2d63f24a78afa9b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:70d5036081281c33d01b7a397d706c4b22c46ec7359659271ecb59469f24dc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158741608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cfc4cc1935f650cf5db05be31aeb394e8b0d15f829755db45adc5e293bf52a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:2f7300f6a28bfafc568dc6d4f92e704241cf6bb3dc9f8ef14f7cd7a8d839c8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19242256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccb440c2f41b957fb6f869ec764c58c788fca64854ff84da0fdc34e232a3932`

```dockerfile
```

-	Layers:
	-	`sha256:8512acde24b888671239fd31dbe59d9654128f22ea970edf0167c2be6b521c29`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 19.2 MB (19225851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e671102472b9cf10097bf426a18c9c5771e38544b7bd98f02c5a6b98c2c0c9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dafb1235408b5776b1cc23ef27fa1d676d03741f826f5e21ef29bcffe52b6185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153997147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997dd26dc1ed64ff82b82216ff9cae31700501be14627e9524440e98f0fbba1d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203623a863f43e1e4b881948129cab8d7bea8980b186a2d5f73e12abefec75d1`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc3526ae0181f5bb51d08158c52a09b96e0f34319c8364f538ceb688698cf50`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec78c40c286de9039f4431dff10337f00059c57c3081b33d466230bb34c6168`  
		Last Modified: Wed, 09 Apr 2025 09:13:03 GMT  
		Size: 121.8 MB (121827814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5e3f6f19fdee885ac03b2133333e7dd66ccf52adc2d22fdc1c85140516d6f8`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:acba8ba5fa9515cf7c16a12e7160010b05ec5be283ad0525aa62426a65656066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19235271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1dc8fbb8858531f0d2a0483c32537ed045f6e5d95e121080f1bc70185e98b8`

```dockerfile
```

-	Layers:
	-	`sha256:90c3859bcd49f030bbcf395f359a1361341c71772e4b253fdd1527231652eefa`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 19.2 MB (19218726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f523d0f5febf0105d402cb773e5ecbf75c4420ef23aa7e0891bab9aca3ecbf6`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:e6f605d0f86aaf1e3da8d7a8d618a38cb65ba6ff8183e6d2d63f24a78afa9b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:70d5036081281c33d01b7a397d706c4b22c46ec7359659271ecb59469f24dc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158741608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cfc4cc1935f650cf5db05be31aeb394e8b0d15f829755db45adc5e293bf52a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:2f7300f6a28bfafc568dc6d4f92e704241cf6bb3dc9f8ef14f7cd7a8d839c8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19242256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccb440c2f41b957fb6f869ec764c58c788fca64854ff84da0fdc34e232a3932`

```dockerfile
```

-	Layers:
	-	`sha256:8512acde24b888671239fd31dbe59d9654128f22ea970edf0167c2be6b521c29`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 19.2 MB (19225851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e671102472b9cf10097bf426a18c9c5771e38544b7bd98f02c5a6b98c2c0c9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dafb1235408b5776b1cc23ef27fa1d676d03741f826f5e21ef29bcffe52b6185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153997147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997dd26dc1ed64ff82b82216ff9cae31700501be14627e9524440e98f0fbba1d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203623a863f43e1e4b881948129cab8d7bea8980b186a2d5f73e12abefec75d1`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc3526ae0181f5bb51d08158c52a09b96e0f34319c8364f538ceb688698cf50`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec78c40c286de9039f4431dff10337f00059c57c3081b33d466230bb34c6168`  
		Last Modified: Wed, 09 Apr 2025 09:13:03 GMT  
		Size: 121.8 MB (121827814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5e3f6f19fdee885ac03b2133333e7dd66ccf52adc2d22fdc1c85140516d6f8`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:acba8ba5fa9515cf7c16a12e7160010b05ec5be283ad0525aa62426a65656066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19235271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1dc8fbb8858531f0d2a0483c32537ed045f6e5d95e121080f1bc70185e98b8`

```dockerfile
```

-	Layers:
	-	`sha256:90c3859bcd49f030bbcf395f359a1361341c71772e4b253fdd1527231652eefa`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 19.2 MB (19218726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f523d0f5febf0105d402cb773e5ecbf75c4420ef23aa7e0891bab9aca3ecbf6`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:9749355a0760334fa5ea3c660f2de1ecc5e8a5af8047e4bbaa9afa8a7843da80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:561bc71a341d9fbbd9033130e6169e694b7b65b1421fc275fcd1dbbd2c642e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295272900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c91a9db1d4fc2a12994eecbd53314dd033c5736121813e86f1fbe63c08e8b`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99045de81e0ba6719056bf2f0ce498cbf21af1b487ae254a8029468870d7c38`  
		Last Modified: Wed, 09 Apr 2025 02:16:15 GMT  
		Size: 110.2 MB (110168410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b46bb8ea31ea3e10dd20185d404b80ee03662025531244d5d3b6d61fced8ce`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 356.2 KB (356177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4841899d1cdb57bc04b3bbf79194535ab00343424557f75d8cccce9707527e0`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af3af51f9bcc09e226669a67bbb42e8b545ad11919419b32b21fe4800926a9`  
		Last Modified: Wed, 09 Apr 2025 02:16:13 GMT  
		Size: 28.0 MB (27956829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:bbd0c9bb7264a59bef954e2ab06327ddf888c5e16944205d6d37c9b10d02b910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23873558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6d4da1096826cfcdfa4642bb1209351096b952fe72ad6b14bfa910012603a`

```dockerfile
```

-	Layers:
	-	`sha256:d037ff389fdf436000187f50d596eee4e1b48f1831027d14f67349308fe3597a`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 23.9 MB (23856129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9757a312f6b889d67ccabe5e9cf0a8bb60aeadd421d16cbc25b95a39c233f7db`  
		Last Modified: Wed, 09 Apr 2025 02:16:11 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d595b8976f0b5119d374417bc2a702c13ce73bceeb7339b5013ee430e64799e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283730024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d837f6fc140dfe7bff23330f794cc63f7342fd87fcca57c21efd0dcb3d9d12f`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51db1d103846823a3853812410eb4b9bd8f5b3617f9aecc91125cf41829688c`  
		Last Modified: Wed, 09 Apr 2025 09:15:19 GMT  
		Size: 117.6 MB (117629816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6afbed0c982bda3351b79854d33ca654f92ce16f4a3e1f4a6cccc802ca0c67`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33b60cccfa6e20c4f0cbe401b3aa68469d974314165628c6b0a5c9f657bf8ef`  
		Last Modified: Wed, 09 Apr 2025 15:53:05 GMT  
		Size: 105.6 MB (105592543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2658de70d02b6e6aa725cf85a7fb82de72d74f9db5f084d807c493e28ecf8f12`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 356.2 KB (356171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249d37e4f0bc9edcb6b72103b259bef7281147ee0a52a7b76b3fdf64b789de89`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22198870635e9bffbbdbcb985a3cb5f54ed99b3ba235edadac2e73de50feead`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 27.1 MB (27054339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:66b5ce3015f296a2f74d14dc1c57ed5422ae90b49dd75bac08ffac49eb52e2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23896263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8356baa88c23b40176e255283b4dd73f5cdcbb8e80196749c8ed31f03760dc`

```dockerfile
```

-	Layers:
	-	`sha256:77ec9aa048cc157a919eacbeef9a5d6a025ddcca0afaa16102b6116c7ff4b3f6`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 23.9 MB (23878685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd8b0a7dfded98791c294b62bfa5c74a8688e976cf84b777cb6d75a9aceafa8`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:7731d9676770843e6d1f1a5f9e989490a3c634a7dd22abacc57c64271ee50b4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:2298bd92415ab3a9702f503fa35a7dad4f009aa5210a88cfe9e4a558547c28c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1075531426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56802615053ca7d472937df8ae4c11ff5dbe66a3f44a9d62e3e1d888908e3ad7`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99045de81e0ba6719056bf2f0ce498cbf21af1b487ae254a8029468870d7c38`  
		Last Modified: Wed, 09 Apr 2025 02:16:15 GMT  
		Size: 110.2 MB (110168410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b46bb8ea31ea3e10dd20185d404b80ee03662025531244d5d3b6d61fced8ce`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 356.2 KB (356177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4841899d1cdb57bc04b3bbf79194535ab00343424557f75d8cccce9707527e0`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af3af51f9bcc09e226669a67bbb42e8b545ad11919419b32b21fe4800926a9`  
		Last Modified: Wed, 09 Apr 2025 02:16:13 GMT  
		Size: 28.0 MB (27956829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428434e7ffeb8017262e3b1286db7c486b98c3195187e6000a568a6ea5d9db33`  
		Last Modified: Wed, 09 Apr 2025 03:15:36 GMT  
		Size: 780.3 MB (780258526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:5141b3e55a351877bc258ef122a482db1515184871929685e615225c6e929d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59587792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a36bc1e7a7653368578c0ac19722dfcd9635dd8507e2c75499a03eb5142dd6`

```dockerfile
```

-	Layers:
	-	`sha256:c50bfb92867bb80407aa76aaba6bd159488111f912d49fde438a6e44ace2a385`  
		Last Modified: Wed, 09 Apr 2025 03:15:21 GMT  
		Size: 59.6 MB (59578104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0537445cdd5239ac7e990bda2073966e75f6437c98f2ccec7f5b0c956478b8`  
		Last Modified: Wed, 09 Apr 2025 03:15:20 GMT  
		Size: 9.7 KB (9688 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:81ac72456d9a8e12b2b3333e45badbde0028dde5686be7115b9881f93ff02b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.5 MB (985482880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5d8ee7a4818fa8088a6c8f9aa6ff9ab7d03f30a6a3630e9982421618c238ec`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab5679ebed679dd3df1e6843c6b8f39fa8e45a051661cbb57e6e0b119a3cfb3`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 680.6 KB (680594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f185985e6550bd84d688dd66ba0a96385e0d1ad37d682fe238a7a01c0d8901`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 3.6 MB (3560303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc221ca73075ddc99f91aee5566348bad0f2cd626764c842b72eb0aab3c0115`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb1b676ccfe7049a341da1d054040b9421e7c6f7efced7ab1bf2aca22d5831`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d831e1a4059e2f42ef51fb31bbc35c38063fdc8eccaa465d49821f79dd0a5aa`  
		Last Modified: Mon, 10 Mar 2025 18:20:36 GMT  
		Size: 125.6 MB (125620540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a9d5a529cd232eba1f6392b838c02adaeaa7a2e4965c850a645b0fd30779e0`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95cd021138d293a95e1efb05e7151fdb92ba15e342e95c3f967053ea9d344d`  
		Last Modified: Mon, 10 Mar 2025 19:20:44 GMT  
		Size: 107.9 MB (107946403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064f4d52c2edc9c08866ae50fcbbb32034c3f128b5b08290f6708bf281df33eb`  
		Last Modified: Mon, 10 Mar 2025 19:20:41 GMT  
		Size: 354.1 KB (354071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543e0e820e45d15b9790572f0cbb4f75877868440e4356c77e3b8f764f11a26`  
		Last Modified: Mon, 10 Mar 2025 19:20:41 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3025a4c0e9527e73815bb3e033f887f1ea6b8cd397368161af1ab7b535b964e`  
		Last Modified: Mon, 10 Mar 2025 19:20:42 GMT  
		Size: 27.1 MB (27056165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f974526e6f7d17dc0a8a75c480c9e92ef7cfc79329734be08de8af1a608fcc6`  
		Last Modified: Mon, 10 Mar 2025 20:57:48 GMT  
		Size: 691.4 MB (691366296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:dd43b8c9cecb829ad53dea162cf32f0f3124e1bd0acbdb80a14b64fb47cf3969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59521009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6e5f464ecaab8a849f68e29f30de6b0b8ba81d6c040cf3bd768f093556a99`

```dockerfile
```

-	Layers:
	-	`sha256:cd26d40e61506302358db55bc4411fc1fe9f86073b3720cb961b6459e9026d10`  
		Last Modified: Mon, 10 Mar 2025 20:57:34 GMT  
		Size: 59.5 MB (59511241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850019d24860ff63c629ff7d21d671634bf951611f1141e000cd58cb58d1cde5`  
		Last Modified: Mon, 10 Mar 2025 20:57:32 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:7731d9676770843e6d1f1a5f9e989490a3c634a7dd22abacc57c64271ee50b4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:2298bd92415ab3a9702f503fa35a7dad4f009aa5210a88cfe9e4a558547c28c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1075531426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56802615053ca7d472937df8ae4c11ff5dbe66a3f44a9d62e3e1d888908e3ad7`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99045de81e0ba6719056bf2f0ce498cbf21af1b487ae254a8029468870d7c38`  
		Last Modified: Wed, 09 Apr 2025 02:16:15 GMT  
		Size: 110.2 MB (110168410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b46bb8ea31ea3e10dd20185d404b80ee03662025531244d5d3b6d61fced8ce`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 356.2 KB (356177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4841899d1cdb57bc04b3bbf79194535ab00343424557f75d8cccce9707527e0`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af3af51f9bcc09e226669a67bbb42e8b545ad11919419b32b21fe4800926a9`  
		Last Modified: Wed, 09 Apr 2025 02:16:13 GMT  
		Size: 28.0 MB (27956829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428434e7ffeb8017262e3b1286db7c486b98c3195187e6000a568a6ea5d9db33`  
		Last Modified: Wed, 09 Apr 2025 03:15:36 GMT  
		Size: 780.3 MB (780258526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5141b3e55a351877bc258ef122a482db1515184871929685e615225c6e929d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59587792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a36bc1e7a7653368578c0ac19722dfcd9635dd8507e2c75499a03eb5142dd6`

```dockerfile
```

-	Layers:
	-	`sha256:c50bfb92867bb80407aa76aaba6bd159488111f912d49fde438a6e44ace2a385`  
		Last Modified: Wed, 09 Apr 2025 03:15:21 GMT  
		Size: 59.6 MB (59578104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0537445cdd5239ac7e990bda2073966e75f6437c98f2ccec7f5b0c956478b8`  
		Last Modified: Wed, 09 Apr 2025 03:15:20 GMT  
		Size: 9.7 KB (9688 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:81ac72456d9a8e12b2b3333e45badbde0028dde5686be7115b9881f93ff02b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.5 MB (985482880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5d8ee7a4818fa8088a6c8f9aa6ff9ab7d03f30a6a3630e9982421618c238ec`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab5679ebed679dd3df1e6843c6b8f39fa8e45a051661cbb57e6e0b119a3cfb3`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 680.6 KB (680594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f185985e6550bd84d688dd66ba0a96385e0d1ad37d682fe238a7a01c0d8901`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 3.6 MB (3560303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc221ca73075ddc99f91aee5566348bad0f2cd626764c842b72eb0aab3c0115`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb1b676ccfe7049a341da1d054040b9421e7c6f7efced7ab1bf2aca22d5831`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d831e1a4059e2f42ef51fb31bbc35c38063fdc8eccaa465d49821f79dd0a5aa`  
		Last Modified: Mon, 10 Mar 2025 18:20:36 GMT  
		Size: 125.6 MB (125620540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a9d5a529cd232eba1f6392b838c02adaeaa7a2e4965c850a645b0fd30779e0`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95cd021138d293a95e1efb05e7151fdb92ba15e342e95c3f967053ea9d344d`  
		Last Modified: Mon, 10 Mar 2025 19:20:44 GMT  
		Size: 107.9 MB (107946403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064f4d52c2edc9c08866ae50fcbbb32034c3f128b5b08290f6708bf281df33eb`  
		Last Modified: Mon, 10 Mar 2025 19:20:41 GMT  
		Size: 354.1 KB (354071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543e0e820e45d15b9790572f0cbb4f75877868440e4356c77e3b8f764f11a26`  
		Last Modified: Mon, 10 Mar 2025 19:20:41 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3025a4c0e9527e73815bb3e033f887f1ea6b8cd397368161af1ab7b535b964e`  
		Last Modified: Mon, 10 Mar 2025 19:20:42 GMT  
		Size: 27.1 MB (27056165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f974526e6f7d17dc0a8a75c480c9e92ef7cfc79329734be08de8af1a608fcc6`  
		Last Modified: Mon, 10 Mar 2025 20:57:48 GMT  
		Size: 691.4 MB (691366296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:dd43b8c9cecb829ad53dea162cf32f0f3124e1bd0acbdb80a14b64fb47cf3969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59521009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6e5f464ecaab8a849f68e29f30de6b0b8ba81d6c040cf3bd768f093556a99`

```dockerfile
```

-	Layers:
	-	`sha256:cd26d40e61506302358db55bc4411fc1fe9f86073b3720cb961b6459e9026d10`  
		Last Modified: Mon, 10 Mar 2025 20:57:34 GMT  
		Size: 59.5 MB (59511241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850019d24860ff63c629ff7d21d671634bf951611f1141e000cd58cb58d1cde5`  
		Last Modified: Mon, 10 Mar 2025 20:57:32 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:9749355a0760334fa5ea3c660f2de1ecc5e8a5af8047e4bbaa9afa8a7843da80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:561bc71a341d9fbbd9033130e6169e694b7b65b1421fc275fcd1dbbd2c642e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295272900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c91a9db1d4fc2a12994eecbd53314dd033c5736121813e86f1fbe63c08e8b`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99045de81e0ba6719056bf2f0ce498cbf21af1b487ae254a8029468870d7c38`  
		Last Modified: Wed, 09 Apr 2025 02:16:15 GMT  
		Size: 110.2 MB (110168410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b46bb8ea31ea3e10dd20185d404b80ee03662025531244d5d3b6d61fced8ce`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 356.2 KB (356177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4841899d1cdb57bc04b3bbf79194535ab00343424557f75d8cccce9707527e0`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af3af51f9bcc09e226669a67bbb42e8b545ad11919419b32b21fe4800926a9`  
		Last Modified: Wed, 09 Apr 2025 02:16:13 GMT  
		Size: 28.0 MB (27956829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:bbd0c9bb7264a59bef954e2ab06327ddf888c5e16944205d6d37c9b10d02b910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23873558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6d4da1096826cfcdfa4642bb1209351096b952fe72ad6b14bfa910012603a`

```dockerfile
```

-	Layers:
	-	`sha256:d037ff389fdf436000187f50d596eee4e1b48f1831027d14f67349308fe3597a`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 23.9 MB (23856129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9757a312f6b889d67ccabe5e9cf0a8bb60aeadd421d16cbc25b95a39c233f7db`  
		Last Modified: Wed, 09 Apr 2025 02:16:11 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d595b8976f0b5119d374417bc2a702c13ce73bceeb7339b5013ee430e64799e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283730024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d837f6fc140dfe7bff23330f794cc63f7342fd87fcca57c21efd0dcb3d9d12f`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51db1d103846823a3853812410eb4b9bd8f5b3617f9aecc91125cf41829688c`  
		Last Modified: Wed, 09 Apr 2025 09:15:19 GMT  
		Size: 117.6 MB (117629816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6afbed0c982bda3351b79854d33ca654f92ce16f4a3e1f4a6cccc802ca0c67`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33b60cccfa6e20c4f0cbe401b3aa68469d974314165628c6b0a5c9f657bf8ef`  
		Last Modified: Wed, 09 Apr 2025 15:53:05 GMT  
		Size: 105.6 MB (105592543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2658de70d02b6e6aa725cf85a7fb82de72d74f9db5f084d807c493e28ecf8f12`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 356.2 KB (356171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249d37e4f0bc9edcb6b72103b259bef7281147ee0a52a7b76b3fdf64b789de89`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22198870635e9bffbbdbcb985a3cb5f54ed99b3ba235edadac2e73de50feead`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 27.1 MB (27054339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:66b5ce3015f296a2f74d14dc1c57ed5422ae90b49dd75bac08ffac49eb52e2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23896263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8356baa88c23b40176e255283b4dd73f5cdcbb8e80196749c8ed31f03760dc`

```dockerfile
```

-	Layers:
	-	`sha256:77ec9aa048cc157a919eacbeef9a5d6a025ddcca0afaa16102b6116c7ff4b3f6`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 23.9 MB (23878685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd8b0a7dfded98791c294b62bfa5c74a8688e976cf84b777cb6d75a9aceafa8`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:9749355a0760334fa5ea3c660f2de1ecc5e8a5af8047e4bbaa9afa8a7843da80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:561bc71a341d9fbbd9033130e6169e694b7b65b1421fc275fcd1dbbd2c642e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295272900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c91a9db1d4fc2a12994eecbd53314dd033c5736121813e86f1fbe63c08e8b`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99045de81e0ba6719056bf2f0ce498cbf21af1b487ae254a8029468870d7c38`  
		Last Modified: Wed, 09 Apr 2025 02:16:15 GMT  
		Size: 110.2 MB (110168410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b46bb8ea31ea3e10dd20185d404b80ee03662025531244d5d3b6d61fced8ce`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 356.2 KB (356177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4841899d1cdb57bc04b3bbf79194535ab00343424557f75d8cccce9707527e0`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af3af51f9bcc09e226669a67bbb42e8b545ad11919419b32b21fe4800926a9`  
		Last Modified: Wed, 09 Apr 2025 02:16:13 GMT  
		Size: 28.0 MB (27956829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:bbd0c9bb7264a59bef954e2ab06327ddf888c5e16944205d6d37c9b10d02b910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23873558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6d4da1096826cfcdfa4642bb1209351096b952fe72ad6b14bfa910012603a`

```dockerfile
```

-	Layers:
	-	`sha256:d037ff389fdf436000187f50d596eee4e1b48f1831027d14f67349308fe3597a`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 23.9 MB (23856129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9757a312f6b889d67ccabe5e9cf0a8bb60aeadd421d16cbc25b95a39c233f7db`  
		Last Modified: Wed, 09 Apr 2025 02:16:11 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d595b8976f0b5119d374417bc2a702c13ce73bceeb7339b5013ee430e64799e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283730024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d837f6fc140dfe7bff23330f794cc63f7342fd87fcca57c21efd0dcb3d9d12f`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51db1d103846823a3853812410eb4b9bd8f5b3617f9aecc91125cf41829688c`  
		Last Modified: Wed, 09 Apr 2025 09:15:19 GMT  
		Size: 117.6 MB (117629816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6afbed0c982bda3351b79854d33ca654f92ce16f4a3e1f4a6cccc802ca0c67`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33b60cccfa6e20c4f0cbe401b3aa68469d974314165628c6b0a5c9f657bf8ef`  
		Last Modified: Wed, 09 Apr 2025 15:53:05 GMT  
		Size: 105.6 MB (105592543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2658de70d02b6e6aa725cf85a7fb82de72d74f9db5f084d807c493e28ecf8f12`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 356.2 KB (356171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249d37e4f0bc9edcb6b72103b259bef7281147ee0a52a7b76b3fdf64b789de89`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22198870635e9bffbbdbcb985a3cb5f54ed99b3ba235edadac2e73de50feead`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 27.1 MB (27054339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:66b5ce3015f296a2f74d14dc1c57ed5422ae90b49dd75bac08ffac49eb52e2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23896263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8356baa88c23b40176e255283b4dd73f5cdcbb8e80196749c8ed31f03760dc`

```dockerfile
```

-	Layers:
	-	`sha256:77ec9aa048cc157a919eacbeef9a5d6a025ddcca0afaa16102b6116c7ff4b3f6`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 23.9 MB (23878685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd8b0a7dfded98791c294b62bfa5c74a8688e976cf84b777cb6d75a9aceafa8`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:93d5671e39b68673412b8afffaeba610d19f62a2290b61ac4687b46a62242531
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:9744fbcc62881fcea353bad7738aca958a88d44a276be7ccb4f80a477f695e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156789041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3891cdac5a34c4785b06deadd61a5aad696e2b64ef94db02049c32dde5e6c3e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=jazzy
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ae2c87782438c9f18082db68730eeddf0982801f9f1128b7fad27b61a685da98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17847209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b670a0a218271b6fe8031421379c69f9fe5ef702176483949c223bd531a7559`

```dockerfile
```

-	Layers:
	-	`sha256:5607db8b7b0bb9adff5d601bc2d8d1b8e96f590b14f02df6e49e02e136a62063`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 17.8 MB (17830837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ea2efc84fa43ccb604cf8617c7d39ed37ba7176cb1198e6f72fb356be5e8ef`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b89807411b41fa7766361c6e17d2282796913885ea71ec728a0e49919f4b630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150724548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae657899e4eb01c905ea7639f6594ee477884d9ede2807bd55c019b11bae85a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=jazzy
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51db1d103846823a3853812410eb4b9bd8f5b3617f9aecc91125cf41829688c`  
		Last Modified: Wed, 09 Apr 2025 09:15:19 GMT  
		Size: 117.6 MB (117629816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6afbed0c982bda3351b79854d33ca654f92ce16f4a3e1f4a6cccc802ca0c67`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:5d64d4a1f39def3c4b7048011054fd9715bd115fe2d3472e1077c4f3e04dae3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17821355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe291e2c5b46377026b72fc245bc2f73b2d455fd711f9c97aab155e3a3c45a15`

```dockerfile
```

-	Layers:
	-	`sha256:d697dd51d4871833a999066a2281dfbe334d36a6cc7b57b1a5e2726664ab1113`  
		Last Modified: Wed, 09 Apr 2025 09:15:17 GMT  
		Size: 17.8 MB (17804843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcef873807bc0d49dff7062ad4d28990f545f79fb8da068e281fa76abbe7ffdb`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:93d5671e39b68673412b8afffaeba610d19f62a2290b61ac4687b46a62242531
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:9744fbcc62881fcea353bad7738aca958a88d44a276be7ccb4f80a477f695e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156789041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3891cdac5a34c4785b06deadd61a5aad696e2b64ef94db02049c32dde5e6c3e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=jazzy
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ae2c87782438c9f18082db68730eeddf0982801f9f1128b7fad27b61a685da98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17847209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b670a0a218271b6fe8031421379c69f9fe5ef702176483949c223bd531a7559`

```dockerfile
```

-	Layers:
	-	`sha256:5607db8b7b0bb9adff5d601bc2d8d1b8e96f590b14f02df6e49e02e136a62063`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 17.8 MB (17830837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ea2efc84fa43ccb604cf8617c7d39ed37ba7176cb1198e6f72fb356be5e8ef`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b89807411b41fa7766361c6e17d2282796913885ea71ec728a0e49919f4b630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150724548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae657899e4eb01c905ea7639f6594ee477884d9ede2807bd55c019b11bae85a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=jazzy
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51db1d103846823a3853812410eb4b9bd8f5b3617f9aecc91125cf41829688c`  
		Last Modified: Wed, 09 Apr 2025 09:15:19 GMT  
		Size: 117.6 MB (117629816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6afbed0c982bda3351b79854d33ca654f92ce16f4a3e1f4a6cccc802ca0c67`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5d64d4a1f39def3c4b7048011054fd9715bd115fe2d3472e1077c4f3e04dae3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17821355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe291e2c5b46377026b72fc245bc2f73b2d455fd711f9c97aab155e3a3c45a15`

```dockerfile
```

-	Layers:
	-	`sha256:d697dd51d4871833a999066a2281dfbe334d36a6cc7b57b1a5e2726664ab1113`  
		Last Modified: Wed, 09 Apr 2025 09:15:17 GMT  
		Size: 17.8 MB (17804843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcef873807bc0d49dff7062ad4d28990f545f79fb8da068e281fa76abbe7ffdb`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:9749355a0760334fa5ea3c660f2de1ecc5e8a5af8047e4bbaa9afa8a7843da80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:561bc71a341d9fbbd9033130e6169e694b7b65b1421fc275fcd1dbbd2c642e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295272900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c91a9db1d4fc2a12994eecbd53314dd033c5736121813e86f1fbe63c08e8b`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99045de81e0ba6719056bf2f0ce498cbf21af1b487ae254a8029468870d7c38`  
		Last Modified: Wed, 09 Apr 2025 02:16:15 GMT  
		Size: 110.2 MB (110168410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b46bb8ea31ea3e10dd20185d404b80ee03662025531244d5d3b6d61fced8ce`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 356.2 KB (356177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4841899d1cdb57bc04b3bbf79194535ab00343424557f75d8cccce9707527e0`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af3af51f9bcc09e226669a67bbb42e8b545ad11919419b32b21fe4800926a9`  
		Last Modified: Wed, 09 Apr 2025 02:16:13 GMT  
		Size: 28.0 MB (27956829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:bbd0c9bb7264a59bef954e2ab06327ddf888c5e16944205d6d37c9b10d02b910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23873558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6d4da1096826cfcdfa4642bb1209351096b952fe72ad6b14bfa910012603a`

```dockerfile
```

-	Layers:
	-	`sha256:d037ff389fdf436000187f50d596eee4e1b48f1831027d14f67349308fe3597a`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 23.9 MB (23856129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9757a312f6b889d67ccabe5e9cf0a8bb60aeadd421d16cbc25b95a39c233f7db`  
		Last Modified: Wed, 09 Apr 2025 02:16:11 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d595b8976f0b5119d374417bc2a702c13ce73bceeb7339b5013ee430e64799e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283730024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d837f6fc140dfe7bff23330f794cc63f7342fd87fcca57c21efd0dcb3d9d12f`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51db1d103846823a3853812410eb4b9bd8f5b3617f9aecc91125cf41829688c`  
		Last Modified: Wed, 09 Apr 2025 09:15:19 GMT  
		Size: 117.6 MB (117629816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6afbed0c982bda3351b79854d33ca654f92ce16f4a3e1f4a6cccc802ca0c67`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33b60cccfa6e20c4f0cbe401b3aa68469d974314165628c6b0a5c9f657bf8ef`  
		Last Modified: Wed, 09 Apr 2025 15:53:05 GMT  
		Size: 105.6 MB (105592543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2658de70d02b6e6aa725cf85a7fb82de72d74f9db5f084d807c493e28ecf8f12`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 356.2 KB (356171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249d37e4f0bc9edcb6b72103b259bef7281147ee0a52a7b76b3fdf64b789de89`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22198870635e9bffbbdbcb985a3cb5f54ed99b3ba235edadac2e73de50feead`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 27.1 MB (27054339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:66b5ce3015f296a2f74d14dc1c57ed5422ae90b49dd75bac08ffac49eb52e2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23896263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8356baa88c23b40176e255283b4dd73f5cdcbb8e80196749c8ed31f03760dc`

```dockerfile
```

-	Layers:
	-	`sha256:77ec9aa048cc157a919eacbeef9a5d6a025ddcca0afaa16102b6116c7ff4b3f6`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 23.9 MB (23878685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd8b0a7dfded98791c294b62bfa5c74a8688e976cf84b777cb6d75a9aceafa8`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic`

```console
$ docker pull ros@sha256:6465a56f03f72033905bd7c537d29848c14c78e087bab45ea30181f3ca06ded3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:274cafb4228a90240a38e98eb7b469071d8912de039db739bc5a683b0008e345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263117266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445e4e9450d813702fa00d57b2bace32ecd24a584b6093d57ca2cf4b06fd2e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Wed, 09 Apr 2025 02:15:48 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:894d6d306f4a156faef3730e7718f84b3f6a7e61a7ac87f59db565eb55c2b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27620532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b93e73bd53bcf0cba37d3bb0c53db0aed971446443b64039246ecd9c552df9`

```dockerfile
```

-	Layers:
	-	`sha256:ae2cb33b1ab49a18cd94355d1e94171e5d5904a2f7886c1a45b833b63804f3be`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 27.6 MB (27606846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19f11b316561bc9402681823319dbab7b17538ca6eab782b6c261f95d0e2708`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:7f06923620dcb14829611b10907cc82c55a7b333c9318bfeb53cd8ad907fc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228333887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6480a80e46afc8bd51cd981ff94aa3fab93b996f1f7de2b88dc118703d16488`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:18e13ecba12a87f54a9f386ce6fec1aeeec342d51cebc59f93687d200660c0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27383622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a59e628885a870a5e4c547949eb356a8207eefb673574a207d30cc44edc84c`

```dockerfile
```

-	Layers:
	-	`sha256:8766d60d6a90fdccae930bfb00cf53eea623068ac6966e1518c6e114ae3fed15`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 27.4 MB (27369842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d36c37521d0d18b0e266ef7e93c98217a617d45aee5ca476c23b1b6c605339c5`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5626d190770d234143954698dddf98a9cb97a3429922bc05e310d034c5ee7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1a8972be4098e73a367bc535112949e47c4dbd1e183fa1e6f87ea23060dcac`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:90249cede2082d3aca1db98135b1ab6e429caf1bbf08b4fa8bccdabcafd0925c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27570563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c578189226a60b3bda679cb5b90bde0c4f7744d0f14b14b8d36142d77e5d57c`

```dockerfile
```

-	Layers:
	-	`sha256:d75e6f47c4ab5594fbea0ec4966288fd99af3dd31e0e15bc514e31ce7c4a43ca`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 27.6 MB (27556755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa8fdd93e74bccd7e121aacd19ef9d4f55868eff3f212e02c656d6ece48bd74`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:1af3db41095a745c30265af92c66042cfa77c0e752cfc8316b4227cadd70ba89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:ad53566f8860108545de1e7a9ec08674c6662a7040bc14285167f4b5e59ec6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.1 MB (947079134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d7c1b575a3a4be2b512a2a1347867dd7e52acd766a7e4ececf13911a30f813`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Wed, 09 Apr 2025 02:15:48 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e8c3b14c608ecb2e865a0de678b74f5794f6d1027a965462403f1b83582b0`  
		Last Modified: Wed, 09 Apr 2025 03:15:43 GMT  
		Size: 684.0 MB (683961868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c42c6cd3b6ece2f67cdfd1c894fdc6a4473a4435191fe53345e7cbcdb2c2e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52718030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e1e5cf94431d2ab4a6c9405cce7c8686d06afa3ef4cfd860f028e3f27d7f67`

```dockerfile
```

-	Layers:
	-	`sha256:2cad68b96b92d88b145401da2716d5827c0f781f72f1005117185c9918ca388d`  
		Last Modified: Wed, 09 Apr 2025 03:15:29 GMT  
		Size: 52.7 MB (52708657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99da4e34c7a38b9050b7d5debf517fb04bab793919f282acd327df3707f666`  
		Last Modified: Wed, 09 Apr 2025 03:15:27 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:e369bf14da3d93f9be6ad671f4681b2b488f5f0056278a79723286d2ed2d239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.2 MB (725206547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424465548bb231bcb31875ce6e38c94dcfbef64f744da6db98b9817377cb28ce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22052e0f4af1fa1026f671cc3091c7c92fc31d9da9086335d89ec24f1c013474`  
		Last Modified: Wed, 09 Apr 2025 13:46:00 GMT  
		Size: 496.9 MB (496872660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1fbf1d0fe5a65fae05c1ee79bb1d59394c0124d36e81e95300cf6b280254b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51466276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cf80209972ecf4daf80b36ce0363eab1a75c5f046a99fe0518fb41a37470a9`

```dockerfile
```

-	Layers:
	-	`sha256:350b1e9cb0d117c5c2ba18f2ba57f6d6ba9d0e72c5c2e793bad9e8f84b8e72e7`  
		Last Modified: Wed, 09 Apr 2025 13:45:50 GMT  
		Size: 51.5 MB (51456843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98581e073cf87a2627f231fe098612edf517b2e20ad820129c446e3afc1f74fb`  
		Last Modified: Wed, 09 Apr 2025 13:45:48 GMT  
		Size: 9.4 KB (9433 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cfcdafb6ae6c5e1c85e054202ee9571e286b88fe215dcad96e2920cf7f3bf7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.0 MB (902042260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e17c4f0db3b8edd25decb5455db77a82b8508882492faacbd0032b51909045e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8498e3ff194372ace8e0d6adab098ede6183b5fc569779a0da961fce617ec1aa`  
		Last Modified: Wed, 09 Apr 2025 18:53:26 GMT  
		Size: 651.8 MB (651806563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e53bdc49d292ca610d7c65ea39ca39d81e6e3db349619076484eb33e90501621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52577752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99522e5bf9afe7bc5271fb30273274c04615e345ca72b41c861478851d82d7b`

```dockerfile
```

-	Layers:
	-	`sha256:0fab2f8af0fefd387cd98b46db31acb42237fcb69539a5c90c9b6a494e6789e4`  
		Last Modified: Wed, 09 Apr 2025 18:53:13 GMT  
		Size: 52.6 MB (52568298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbb944e96c1e06942dbdd8eb1150a055a3c839522f5cd6454f7096b5409e75b`  
		Last Modified: Wed, 09 Apr 2025 18:53:11 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:1af3db41095a745c30265af92c66042cfa77c0e752cfc8316b4227cadd70ba89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:ad53566f8860108545de1e7a9ec08674c6662a7040bc14285167f4b5e59ec6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.1 MB (947079134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d7c1b575a3a4be2b512a2a1347867dd7e52acd766a7e4ececf13911a30f813`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Wed, 09 Apr 2025 02:15:48 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e8c3b14c608ecb2e865a0de678b74f5794f6d1027a965462403f1b83582b0`  
		Last Modified: Wed, 09 Apr 2025 03:15:43 GMT  
		Size: 684.0 MB (683961868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:c42c6cd3b6ece2f67cdfd1c894fdc6a4473a4435191fe53345e7cbcdb2c2e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52718030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e1e5cf94431d2ab4a6c9405cce7c8686d06afa3ef4cfd860f028e3f27d7f67`

```dockerfile
```

-	Layers:
	-	`sha256:2cad68b96b92d88b145401da2716d5827c0f781f72f1005117185c9918ca388d`  
		Last Modified: Wed, 09 Apr 2025 03:15:29 GMT  
		Size: 52.7 MB (52708657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99da4e34c7a38b9050b7d5debf517fb04bab793919f282acd327df3707f666`  
		Last Modified: Wed, 09 Apr 2025 03:15:27 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:e369bf14da3d93f9be6ad671f4681b2b488f5f0056278a79723286d2ed2d239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.2 MB (725206547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424465548bb231bcb31875ce6e38c94dcfbef64f744da6db98b9817377cb28ce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22052e0f4af1fa1026f671cc3091c7c92fc31d9da9086335d89ec24f1c013474`  
		Last Modified: Wed, 09 Apr 2025 13:46:00 GMT  
		Size: 496.9 MB (496872660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1fbf1d0fe5a65fae05c1ee79bb1d59394c0124d36e81e95300cf6b280254b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51466276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cf80209972ecf4daf80b36ce0363eab1a75c5f046a99fe0518fb41a37470a9`

```dockerfile
```

-	Layers:
	-	`sha256:350b1e9cb0d117c5c2ba18f2ba57f6d6ba9d0e72c5c2e793bad9e8f84b8e72e7`  
		Last Modified: Wed, 09 Apr 2025 13:45:50 GMT  
		Size: 51.5 MB (51456843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98581e073cf87a2627f231fe098612edf517b2e20ad820129c446e3afc1f74fb`  
		Last Modified: Wed, 09 Apr 2025 13:45:48 GMT  
		Size: 9.4 KB (9433 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cfcdafb6ae6c5e1c85e054202ee9571e286b88fe215dcad96e2920cf7f3bf7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.0 MB (902042260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e17c4f0db3b8edd25decb5455db77a82b8508882492faacbd0032b51909045e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8498e3ff194372ace8e0d6adab098ede6183b5fc569779a0da961fce617ec1aa`  
		Last Modified: Wed, 09 Apr 2025 18:53:26 GMT  
		Size: 651.8 MB (651806563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:e53bdc49d292ca610d7c65ea39ca39d81e6e3db349619076484eb33e90501621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52577752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99522e5bf9afe7bc5271fb30273274c04615e345ca72b41c861478851d82d7b`

```dockerfile
```

-	Layers:
	-	`sha256:0fab2f8af0fefd387cd98b46db31acb42237fcb69539a5c90c9b6a494e6789e4`  
		Last Modified: Wed, 09 Apr 2025 18:53:13 GMT  
		Size: 52.6 MB (52568298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbb944e96c1e06942dbdd8eb1150a055a3c839522f5cd6454f7096b5409e75b`  
		Last Modified: Wed, 09 Apr 2025 18:53:11 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:8a8402ac39bc8d0be5b9b261d691c9e970340507a1974929a9f1e7a6b0f54e3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:588666ac574852c0f1e259190bd806ae1b99ccc6619005bc24910c151627d1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280042321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a03753484f8bbac88f933035da74157dfb24e98d5563aaea5b3af4313dbb369`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Wed, 09 Apr 2025 02:15:48 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdca47db82ecc28269b7fa68385af6120c48afac7a12c7f0bf95e28dbf6686ee`  
		Last Modified: Wed, 09 Apr 2025 03:11:52 GMT  
		Size: 16.9 MB (16925055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:e33bfdee69c472d8bb814caec0491e35a8e073bf211b390190568141f5b7c44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29512790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4623b560e03238cf86606821f7e0c697279853c8a048aa0a90ad881dcbc5522c`

```dockerfile
```

-	Layers:
	-	`sha256:29c4cb4ef7b34b8d9940a27971d2cfd5b9fa4febd04f8b4db127d4e1915acb0b`  
		Last Modified: Wed, 09 Apr 2025 03:11:52 GMT  
		Size: 29.5 MB (29503464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee60d0a4acbc42cd0154cd6d608c3a47d7092fc6da7c4ce3dc2f11ed155102d7`  
		Last Modified: Wed, 09 Apr 2025 03:11:51 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:247ba19cb640d3a017c255d5541301625006985570bba1f05720f7ecef9074f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243357623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db32f83b400706cf730c41647acfbe4fdc88306c1407aacb9119bde20cfc438`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce917e8cec917422e9b6a79f9f49112806fda0cdaab6fce81b17bf63c04f209`  
		Last Modified: Wed, 09 Apr 2025 13:33:42 GMT  
		Size: 15.0 MB (15023736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:626b755c3618c71ae52bd438d05ec6a346a47b35e9711c9388564dc93da89c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29267106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec5ef38941e671f87b984b4f5304b2e2fdc2e9b2a7d5e768e9541cd6eb84876`

```dockerfile
```

-	Layers:
	-	`sha256:a8d06991796052382e033ebfa50cf0b80e437ffc3ba2325350464f47b9f0b403`  
		Last Modified: Wed, 09 Apr 2025 13:33:42 GMT  
		Size: 29.3 MB (29257720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456bf4bb66d9bbece5d2fe1cbb27ba6703dfb4db9c4c1696359ed701022b9af5`  
		Last Modified: Wed, 09 Apr 2025 13:33:41 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fd8eaa825e35a53b192e94ea3ba2eab3bdcc643490951ba174bef67c7ff79832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266760448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61658de4f350c408e30eb759999297306caf15df5319b470cfe4352a3d4fa324`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc18e7f8f3ae2ac59eca56e522da5ed43f809e3579b4b75a48316034dc1e44`  
		Last Modified: Wed, 09 Apr 2025 18:41:37 GMT  
		Size: 16.5 MB (16524751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:30c0ba04fe310f092169fdff39ed518bacd834606fcf538560502f7342d8a4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29461629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26885debb52feb76793555af5cb2ddbeb619a1f6c7e4a755bea97f7562e2c9d4`

```dockerfile
```

-	Layers:
	-	`sha256:727d7b00a4d318636171b5fec68d750197abb14a42696eeed770eae6d211718b`  
		Last Modified: Wed, 09 Apr 2025 18:41:38 GMT  
		Size: 29.5 MB (29452223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f67eea5ebd299fbd5b2b27021fc5f37a22e5d4fef3370f153efd7844dbbd781`  
		Last Modified: Wed, 09 Apr 2025 18:41:36 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:8a8402ac39bc8d0be5b9b261d691c9e970340507a1974929a9f1e7a6b0f54e3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:588666ac574852c0f1e259190bd806ae1b99ccc6619005bc24910c151627d1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280042321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a03753484f8bbac88f933035da74157dfb24e98d5563aaea5b3af4313dbb369`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Wed, 09 Apr 2025 02:15:48 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdca47db82ecc28269b7fa68385af6120c48afac7a12c7f0bf95e28dbf6686ee`  
		Last Modified: Wed, 09 Apr 2025 03:11:52 GMT  
		Size: 16.9 MB (16925055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:e33bfdee69c472d8bb814caec0491e35a8e073bf211b390190568141f5b7c44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29512790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4623b560e03238cf86606821f7e0c697279853c8a048aa0a90ad881dcbc5522c`

```dockerfile
```

-	Layers:
	-	`sha256:29c4cb4ef7b34b8d9940a27971d2cfd5b9fa4febd04f8b4db127d4e1915acb0b`  
		Last Modified: Wed, 09 Apr 2025 03:11:52 GMT  
		Size: 29.5 MB (29503464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee60d0a4acbc42cd0154cd6d608c3a47d7092fc6da7c4ce3dc2f11ed155102d7`  
		Last Modified: Wed, 09 Apr 2025 03:11:51 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:247ba19cb640d3a017c255d5541301625006985570bba1f05720f7ecef9074f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243357623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db32f83b400706cf730c41647acfbe4fdc88306c1407aacb9119bde20cfc438`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce917e8cec917422e9b6a79f9f49112806fda0cdaab6fce81b17bf63c04f209`  
		Last Modified: Wed, 09 Apr 2025 13:33:42 GMT  
		Size: 15.0 MB (15023736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:626b755c3618c71ae52bd438d05ec6a346a47b35e9711c9388564dc93da89c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29267106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec5ef38941e671f87b984b4f5304b2e2fdc2e9b2a7d5e768e9541cd6eb84876`

```dockerfile
```

-	Layers:
	-	`sha256:a8d06991796052382e033ebfa50cf0b80e437ffc3ba2325350464f47b9f0b403`  
		Last Modified: Wed, 09 Apr 2025 13:33:42 GMT  
		Size: 29.3 MB (29257720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456bf4bb66d9bbece5d2fe1cbb27ba6703dfb4db9c4c1696359ed701022b9af5`  
		Last Modified: Wed, 09 Apr 2025 13:33:41 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fd8eaa825e35a53b192e94ea3ba2eab3bdcc643490951ba174bef67c7ff79832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266760448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61658de4f350c408e30eb759999297306caf15df5319b470cfe4352a3d4fa324`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc18e7f8f3ae2ac59eca56e522da5ed43f809e3579b4b75a48316034dc1e44`  
		Last Modified: Wed, 09 Apr 2025 18:41:37 GMT  
		Size: 16.5 MB (16524751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:30c0ba04fe310f092169fdff39ed518bacd834606fcf538560502f7342d8a4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29461629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26885debb52feb76793555af5cb2ddbeb619a1f6c7e4a755bea97f7562e2c9d4`

```dockerfile
```

-	Layers:
	-	`sha256:727d7b00a4d318636171b5fec68d750197abb14a42696eeed770eae6d211718b`  
		Last Modified: Wed, 09 Apr 2025 18:41:38 GMT  
		Size: 29.5 MB (29452223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f67eea5ebd299fbd5b2b27021fc5f37a22e5d4fef3370f153efd7844dbbd781`  
		Last Modified: Wed, 09 Apr 2025 18:41:36 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:6465a56f03f72033905bd7c537d29848c14c78e087bab45ea30181f3ca06ded3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:274cafb4228a90240a38e98eb7b469071d8912de039db739bc5a683b0008e345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263117266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445e4e9450d813702fa00d57b2bace32ecd24a584b6093d57ca2cf4b06fd2e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Wed, 09 Apr 2025 02:15:48 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:894d6d306f4a156faef3730e7718f84b3f6a7e61a7ac87f59db565eb55c2b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27620532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b93e73bd53bcf0cba37d3bb0c53db0aed971446443b64039246ecd9c552df9`

```dockerfile
```

-	Layers:
	-	`sha256:ae2cb33b1ab49a18cd94355d1e94171e5d5904a2f7886c1a45b833b63804f3be`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 27.6 MB (27606846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19f11b316561bc9402681823319dbab7b17538ca6eab782b6c261f95d0e2708`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:7f06923620dcb14829611b10907cc82c55a7b333c9318bfeb53cd8ad907fc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228333887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6480a80e46afc8bd51cd981ff94aa3fab93b996f1f7de2b88dc118703d16488`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:18e13ecba12a87f54a9f386ce6fec1aeeec342d51cebc59f93687d200660c0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27383622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a59e628885a870a5e4c547949eb356a8207eefb673574a207d30cc44edc84c`

```dockerfile
```

-	Layers:
	-	`sha256:8766d60d6a90fdccae930bfb00cf53eea623068ac6966e1518c6e114ae3fed15`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 27.4 MB (27369842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d36c37521d0d18b0e266ef7e93c98217a617d45aee5ca476c23b1b6c605339c5`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5626d190770d234143954698dddf98a9cb97a3429922bc05e310d034c5ee7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1a8972be4098e73a367bc535112949e47c4dbd1e183fa1e6f87ea23060dcac`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:90249cede2082d3aca1db98135b1ab6e429caf1bbf08b4fa8bccdabcafd0925c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27570563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c578189226a60b3bda679cb5b90bde0c4f7744d0f14b14b8d36142d77e5d57c`

```dockerfile
```

-	Layers:
	-	`sha256:d75e6f47c4ab5594fbea0ec4966288fd99af3dd31e0e15bc514e31ce7c4a43ca`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 27.6 MB (27556755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa8fdd93e74bccd7e121aacd19ef9d4f55868eff3f212e02c656d6ece48bd74`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:6465a56f03f72033905bd7c537d29848c14c78e087bab45ea30181f3ca06ded3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:274cafb4228a90240a38e98eb7b469071d8912de039db739bc5a683b0008e345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263117266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445e4e9450d813702fa00d57b2bace32ecd24a584b6093d57ca2cf4b06fd2e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Wed, 09 Apr 2025 02:15:48 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:894d6d306f4a156faef3730e7718f84b3f6a7e61a7ac87f59db565eb55c2b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27620532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b93e73bd53bcf0cba37d3bb0c53db0aed971446443b64039246ecd9c552df9`

```dockerfile
```

-	Layers:
	-	`sha256:ae2cb33b1ab49a18cd94355d1e94171e5d5904a2f7886c1a45b833b63804f3be`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 27.6 MB (27606846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19f11b316561bc9402681823319dbab7b17538ca6eab782b6c261f95d0e2708`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:7f06923620dcb14829611b10907cc82c55a7b333c9318bfeb53cd8ad907fc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228333887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6480a80e46afc8bd51cd981ff94aa3fab93b996f1f7de2b88dc118703d16488`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:18e13ecba12a87f54a9f386ce6fec1aeeec342d51cebc59f93687d200660c0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27383622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a59e628885a870a5e4c547949eb356a8207eefb673574a207d30cc44edc84c`

```dockerfile
```

-	Layers:
	-	`sha256:8766d60d6a90fdccae930bfb00cf53eea623068ac6966e1518c6e114ae3fed15`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 27.4 MB (27369842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d36c37521d0d18b0e266ef7e93c98217a617d45aee5ca476c23b1b6c605339c5`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5626d190770d234143954698dddf98a9cb97a3429922bc05e310d034c5ee7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1a8972be4098e73a367bc535112949e47c4dbd1e183fa1e6f87ea23060dcac`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:90249cede2082d3aca1db98135b1ab6e429caf1bbf08b4fa8bccdabcafd0925c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27570563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c578189226a60b3bda679cb5b90bde0c4f7744d0f14b14b8d36142d77e5d57c`

```dockerfile
```

-	Layers:
	-	`sha256:d75e6f47c4ab5594fbea0ec4966288fd99af3dd31e0e15bc514e31ce7c4a43ca`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 27.6 MB (27556755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa8fdd93e74bccd7e121aacd19ef9d4f55868eff3f212e02c656d6ece48bd74`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:9879882c8bc0d413196d642b4d6472d48aca8e71904095165130b6ad997cb005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e3ee73327a6c0b9fcc0d0417f497efd32bdd1fb805eedc6cb9ac569a74106ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211140864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4322e50775a7c49dcdea57f96c4f54a779e8ae843ab3585f21def61bd84b6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f4c31b8b90bd7e7521a693330759356bfd3a2a2a33e93163f474e52d8878c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26143714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b714883d7de56c37684a771cbf4fc78714590ee1dd0648a263545c517f80e8cb`

```dockerfile
```

-	Layers:
	-	`sha256:1e714282d84d7ce6bd446b3b0a913a7fdc97e18fd7cba34d59d962e35b020bd2`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 26.1 MB (26127337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9dc9e7dadf0400d5163e43754c73c9e03fb1674775b61a4727c541ea31a051`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:151b9235253426a0d8e7655e9bfbae714abe57ba72caeb42dec05744ba16c1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186866495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd4efad2dd6ff7af9c5ec58d3379e00fdad60531ffa040973347a4452589d9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6e8b44927476ef189f622ca00c9fb5e9bb851eec69e78e75634e3eea58720b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26056807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba816d41d03aed709f0b2decbc51c6450d406ac842f5c800e17f053a9384bc5b`

```dockerfile
```

-	Layers:
	-	`sha256:a9ac5d1d21afcfb57c58e67437ba9a2f2e7941be62277aafa75e7edf5011dabe`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 26.0 MB (26040318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb27a049109432dba7aeb4f84280414ead6bbb0d9f67f35c6af454dc3dbf1ef`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 16.5 KB (16489 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0f7de31ac9a71ebf9ebca0bf424fa4343ae519c76bd4b050de1f573191397a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204005332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ac5c2cfabd3fd3599fb21adaea30c6dfa43fb474de5a21de1366025e0b43a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:34f5d25371f8858ec64b5b90e6a02a87290490571242bb5f2eb693d20c242aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26065587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6116132cc84451c0715ce6d9193b941c50145a233232866fc290ccea8e9cb7e`

```dockerfile
```

-	Layers:
	-	`sha256:27167fa2a14e9cf15daff2f6310176e962d915900aacb47474061a6874ee4f24`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 26.0 MB (26049070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec7aed39508320d33a62deae1dd7261a6270fcade2f287ea90dffb8f5004a26`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:9879882c8bc0d413196d642b4d6472d48aca8e71904095165130b6ad997cb005
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:e3ee73327a6c0b9fcc0d0417f497efd32bdd1fb805eedc6cb9ac569a74106ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211140864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4322e50775a7c49dcdea57f96c4f54a779e8ae843ab3585f21def61bd84b6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Wed, 09 Apr 2025 01:21:03 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Wed, 09 Apr 2025 01:21:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:f4c31b8b90bd7e7521a693330759356bfd3a2a2a33e93163f474e52d8878c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26143714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b714883d7de56c37684a771cbf4fc78714590ee1dd0648a263545c517f80e8cb`

```dockerfile
```

-	Layers:
	-	`sha256:1e714282d84d7ce6bd446b3b0a913a7fdc97e18fd7cba34d59d962e35b020bd2`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 26.1 MB (26127337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9dc9e7dadf0400d5163e43754c73c9e03fb1674775b61a4727c541ea31a051`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:151b9235253426a0d8e7655e9bfbae714abe57ba72caeb42dec05744ba16c1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186866495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd4efad2dd6ff7af9c5ec58d3379e00fdad60531ffa040973347a4452589d9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Wed, 09 Apr 2025 12:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Wed, 09 Apr 2025 12:06:07 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:6e8b44927476ef189f622ca00c9fb5e9bb851eec69e78e75634e3eea58720b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26056807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba816d41d03aed709f0b2decbc51c6450d406ac842f5c800e17f053a9384bc5b`

```dockerfile
```

-	Layers:
	-	`sha256:a9ac5d1d21afcfb57c58e67437ba9a2f2e7941be62277aafa75e7edf5011dabe`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 26.0 MB (26040318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb27a049109432dba7aeb4f84280414ead6bbb0d9f67f35c6af454dc3dbf1ef`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 16.5 KB (16489 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0f7de31ac9a71ebf9ebca0bf424fa4343ae519c76bd4b050de1f573191397a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204005332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ac5c2cfabd3fd3599fb21adaea30c6dfa43fb474de5a21de1366025e0b43a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Wed, 09 Apr 2025 09:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Wed, 09 Apr 2025 09:09:11 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:34f5d25371f8858ec64b5b90e6a02a87290490571242bb5f2eb693d20c242aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26065587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6116132cc84451c0715ce6d9193b941c50145a233232866fc290ccea8e9cb7e`

```dockerfile
```

-	Layers:
	-	`sha256:27167fa2a14e9cf15daff2f6310176e962d915900aacb47474061a6874ee4f24`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 26.0 MB (26049070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec7aed39508320d33a62deae1dd7261a6270fcade2f287ea90dffb8f5004a26`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:494e6af9aa6f9d68674f886a5ab7ee638218aaa163150f674513d42ef09fb6f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:d13ffac35796e54aa42b7a21b88ee955c1145f3402cecec85612abcd7918990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295245503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912c842a4d49b0b9d92c954407b57f345b46bd030ae9ebbe566f49d68b4ded3a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9da1b5048f08150019e977d6e262db7577c0ddca858e147df7d9bf93f79da`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 683.6 KB (683556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e54389289d908213d0e62f13c72b2001cc525190c511ba09dfad5c8b084fb`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 3.6 MB (3563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5382010868ddf658e88e6bffad5d0ce76a6a6a6b354b9cce80c97e508cb63`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b64bc19922e1f6345f2b4e899c22ff3b9b37a905b50f5c6e0784ada292f34`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee44a6aadcf0d84954979ffc4c8878dd6ea0ef9a78cb99a31bced6981ef5ed`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 122.8 MB (122794979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48198ad8c8df02f87473863271fe668e6d78defe02d55c43b7168acc66a4ecc2`  
		Last Modified: Wed, 09 Apr 2025 01:20:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa100ae83b33f4a00647f4b3dc436a7eed071ab68f18a6142f712d0c9494f234`  
		Last Modified: Wed, 09 Apr 2025 02:48:53 GMT  
		Size: 110.2 MB (110171845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666490107601b7f396f20994e344057fd40294b1dd92231b664ee7c1891c960`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 338.1 KB (338060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785cc6e2f10ee0b8f089cc0aa88c5953ea75ba381b07211777ce66d9dd2231ed`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc80d84363dd2e6e993857b7b92a78ab887b160a51889507644e5631a9ae4d90`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 28.0 MB (27971330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:b87601e7c0e4423ab4aee54236027627d8aaabb244d3b8b3b72732261f437479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23842704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b9a25f25f8e121a157fc317fec8bdf8c81b96dac72debd3ba70cccc64b87f`

```dockerfile
```

-	Layers:
	-	`sha256:0f3278fe6bdbd870ca9558a781eec6129bbdcd5617674ee4cdca44ad19a42c8c`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 23.8 MB (23825531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a06df7eca501cc5b6bad5ac6b27c6a4e0f4653c365c5f83b05c3db2d9459ba`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:97fa7c3fa68dfebbce0b528b0c1af309e79b5a11a66439b98faa891e6067a69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283726192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3bf1c4c42b0f39c5edb2233c098b47eca10b96b0aa3a9fe24ee31dbbf39d73`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a60662d472c0013b6b8d0ea8420230ca63c5a5cc05908698fa85ce4d690d0c`  
		Last Modified: Wed, 09 Apr 2025 09:16:43 GMT  
		Size: 117.6 MB (117638537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c91896a405184701e3d8a7ccd13bb50b4678fd39d67f09c91da7542824b3c9`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9af466fad2f65e605b90e86db4c3ddcc8167fe2a0eafabfe3be94dfbfaa7f`  
		Last Modified: Wed, 09 Apr 2025 15:54:53 GMT  
		Size: 105.6 MB (105595325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5c94d4c8356be193c6875cb17e4c4820fcba1569c0569a48c7dbd73b8f9ac`  
		Last Modified: Wed, 09 Apr 2025 15:54:51 GMT  
		Size: 338.1 KB (338058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d33a92e1576144cea07ccfea2ddf7551cef8851883f7b4632198fa3d8db85c`  
		Last Modified: Wed, 09 Apr 2025 15:54:50 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42682e414427c952a849a517769a2a9330a32f2a861c581ed4ef05222f31dc83`  
		Last Modified: Wed, 09 Apr 2025 15:54:52 GMT  
		Size: 27.1 MB (27057105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:0c27edcee39479c73854211193e79bc49ebb8ec058233abcc182d045f0acb033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23865385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a9629b17a579f604e195a9ed04ef7cddfae02b6acb5d620f2c27915293e659`

```dockerfile
```

-	Layers:
	-	`sha256:b5ac138ec0c5ec3081078624554ff778435334f32befc9be7291929b418221ca`  
		Last Modified: Wed, 09 Apr 2025 15:54:51 GMT  
		Size: 23.8 MB (23848075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036d8cecede9934cb0de979b1532749a82bfe265b6518a702246beaa7c7cad0f`  
		Last Modified: Wed, 09 Apr 2025 15:54:50 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:f62b5344ab18155d0f05c24889e6aef12cceb53caa950ab65f4662b1a28b54f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:356929b6d36543977d1339667e0d85478b4ec7bfd26bf4c4147366c5e68517be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.5 MB (661475842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49319845efbee64b4bfe8730cc4ec94c16117ed90721e658d2e1bc99bfc3dfa2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9da1b5048f08150019e977d6e262db7577c0ddca858e147df7d9bf93f79da`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 683.6 KB (683556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e54389289d908213d0e62f13c72b2001cc525190c511ba09dfad5c8b084fb`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 3.6 MB (3563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5382010868ddf658e88e6bffad5d0ce76a6a6a6b354b9cce80c97e508cb63`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b64bc19922e1f6345f2b4e899c22ff3b9b37a905b50f5c6e0784ada292f34`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee44a6aadcf0d84954979ffc4c8878dd6ea0ef9a78cb99a31bced6981ef5ed`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 122.8 MB (122794979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48198ad8c8df02f87473863271fe668e6d78defe02d55c43b7168acc66a4ecc2`  
		Last Modified: Wed, 09 Apr 2025 01:20:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa100ae83b33f4a00647f4b3dc436a7eed071ab68f18a6142f712d0c9494f234`  
		Last Modified: Wed, 09 Apr 2025 02:48:53 GMT  
		Size: 110.2 MB (110171845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666490107601b7f396f20994e344057fd40294b1dd92231b664ee7c1891c960`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 338.1 KB (338060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785cc6e2f10ee0b8f089cc0aa88c5953ea75ba381b07211777ce66d9dd2231ed`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc80d84363dd2e6e993857b7b92a78ab887b160a51889507644e5631a9ae4d90`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 28.0 MB (27971330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd86e13bdf954f20585bde2ebc36397f6ed75124ad70f65a8f0c5354df402b4`  
		Last Modified: Wed, 09 Apr 2025 03:13:11 GMT  
		Size: 366.2 MB (366230339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:6a977f3fc06ed4d524f31fbddd6484deb1c23873d606a320eedcf710c51117ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642c307e24a559a7393027bdd8b81f52135c1c34470942e93cd9f5364f64a09d`

```dockerfile
```

-	Layers:
	-	`sha256:7422534f18797de1f55698c82e457834537c28ec8c755a28f8f04ef9b39c35a9`  
		Last Modified: Wed, 09 Apr 2025 03:13:05 GMT  
		Size: 42.1 MB (42141448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1c660d473c97b348755a2e4866c34de5605703829aac164ad3af1381ec17604`  
		Last Modified: Wed, 09 Apr 2025 03:13:05 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:513bd218619c119495b1fcce5492f386f0682201996e7393d8bcedca30375e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.2 MB (576246050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72bb8edd0d2a8f4bb5e921bb7bbf98f4af979e2267575bea4a9af83b9ab547c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab5679ebed679dd3df1e6843c6b8f39fa8e45a051661cbb57e6e0b119a3cfb3`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 680.6 KB (680594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f185985e6550bd84d688dd66ba0a96385e0d1ad37d682fe238a7a01c0d8901`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 3.6 MB (3560303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc221ca73075ddc99f91aee5566348bad0f2cd626764c842b72eb0aab3c0115`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb1b676ccfe7049a341da1d054040b9421e7c6f7efced7ab1bf2aca22d5831`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b44689c8c5f80874ceb853f0ed27781711765c4a547ae76561a1dd01f51e12`  
		Last Modified: Mon, 10 Mar 2025 18:19:01 GMT  
		Size: 125.7 MB (125738121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8e47468d6afb7fb6cdfa6a743dc16aebbc27006635613a6083459f600f817`  
		Last Modified: Mon, 10 Mar 2025 18:18:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c8ee1b225c7641ae06b9b1a4257c64ce1962e2d0ede51f7f24e293d961ad32`  
		Last Modified: Mon, 10 Mar 2025 19:23:42 GMT  
		Size: 107.9 MB (107947875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe112d87c57e9e1a35952bff43c440e479425cbb2072bb30d46ec5e48ef1d5ed`  
		Last Modified: Mon, 10 Mar 2025 19:23:38 GMT  
		Size: 336.7 KB (336664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a8f72395d7a538089f03dda01a55179ebe826230899d893a424d7c1f459b2d`  
		Last Modified: Mon, 10 Mar 2025 19:23:38 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdaad10511d6e7fe76c649ec4b3289a2d957beee577fb92766e4a0f76d2f91`  
		Last Modified: Mon, 10 Mar 2025 19:23:40 GMT  
		Size: 27.1 MB (27053598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccf49c0175b5f99e9175cfc7527624ecc5d3482279ebac616c6abe404e220c3`  
		Last Modified: Mon, 10 Mar 2025 20:31:45 GMT  
		Size: 282.0 MB (282030404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:51c768f23fb5b6395809d7e493ee9553237dbe743324c48e2aed982d728fd483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42198532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ed227686c0cee77d229a94071bacc0141b6a4f5b24f3bbe40dd6dd8058938b`

```dockerfile
```

-	Layers:
	-	`sha256:9a23e993c71cc1fcb5c73d3dfc0d96a2b5ddafe923be525c20a98e8070574eea`  
		Last Modified: Mon, 10 Mar 2025 20:31:41 GMT  
		Size: 42.2 MB (42188742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6db7221d71869234341cecf4fc8d3abc3e7db23da1388e27be6e8f38b6a701`  
		Last Modified: Mon, 10 Mar 2025 20:31:39 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:f62b5344ab18155d0f05c24889e6aef12cceb53caa950ab65f4662b1a28b54f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:356929b6d36543977d1339667e0d85478b4ec7bfd26bf4c4147366c5e68517be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.5 MB (661475842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49319845efbee64b4bfe8730cc4ec94c16117ed90721e658d2e1bc99bfc3dfa2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9da1b5048f08150019e977d6e262db7577c0ddca858e147df7d9bf93f79da`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 683.6 KB (683556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e54389289d908213d0e62f13c72b2001cc525190c511ba09dfad5c8b084fb`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 3.6 MB (3563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5382010868ddf658e88e6bffad5d0ce76a6a6a6b354b9cce80c97e508cb63`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b64bc19922e1f6345f2b4e899c22ff3b9b37a905b50f5c6e0784ada292f34`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee44a6aadcf0d84954979ffc4c8878dd6ea0ef9a78cb99a31bced6981ef5ed`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 122.8 MB (122794979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48198ad8c8df02f87473863271fe668e6d78defe02d55c43b7168acc66a4ecc2`  
		Last Modified: Wed, 09 Apr 2025 01:20:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa100ae83b33f4a00647f4b3dc436a7eed071ab68f18a6142f712d0c9494f234`  
		Last Modified: Wed, 09 Apr 2025 02:48:53 GMT  
		Size: 110.2 MB (110171845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666490107601b7f396f20994e344057fd40294b1dd92231b664ee7c1891c960`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 338.1 KB (338060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785cc6e2f10ee0b8f089cc0aa88c5953ea75ba381b07211777ce66d9dd2231ed`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc80d84363dd2e6e993857b7b92a78ab887b160a51889507644e5631a9ae4d90`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 28.0 MB (27971330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd86e13bdf954f20585bde2ebc36397f6ed75124ad70f65a8f0c5354df402b4`  
		Last Modified: Wed, 09 Apr 2025 03:13:11 GMT  
		Size: 366.2 MB (366230339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6a977f3fc06ed4d524f31fbddd6484deb1c23873d606a320eedcf710c51117ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642c307e24a559a7393027bdd8b81f52135c1c34470942e93cd9f5364f64a09d`

```dockerfile
```

-	Layers:
	-	`sha256:7422534f18797de1f55698c82e457834537c28ec8c755a28f8f04ef9b39c35a9`  
		Last Modified: Wed, 09 Apr 2025 03:13:05 GMT  
		Size: 42.1 MB (42141448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1c660d473c97b348755a2e4866c34de5605703829aac164ad3af1381ec17604`  
		Last Modified: Wed, 09 Apr 2025 03:13:05 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:513bd218619c119495b1fcce5492f386f0682201996e7393d8bcedca30375e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.2 MB (576246050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72bb8edd0d2a8f4bb5e921bb7bbf98f4af979e2267575bea4a9af83b9ab547c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab5679ebed679dd3df1e6843c6b8f39fa8e45a051661cbb57e6e0b119a3cfb3`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 680.6 KB (680594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f185985e6550bd84d688dd66ba0a96385e0d1ad37d682fe238a7a01c0d8901`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 3.6 MB (3560303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc221ca73075ddc99f91aee5566348bad0f2cd626764c842b72eb0aab3c0115`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb1b676ccfe7049a341da1d054040b9421e7c6f7efced7ab1bf2aca22d5831`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b44689c8c5f80874ceb853f0ed27781711765c4a547ae76561a1dd01f51e12`  
		Last Modified: Mon, 10 Mar 2025 18:19:01 GMT  
		Size: 125.7 MB (125738121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8e47468d6afb7fb6cdfa6a743dc16aebbc27006635613a6083459f600f817`  
		Last Modified: Mon, 10 Mar 2025 18:18:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c8ee1b225c7641ae06b9b1a4257c64ce1962e2d0ede51f7f24e293d961ad32`  
		Last Modified: Mon, 10 Mar 2025 19:23:42 GMT  
		Size: 107.9 MB (107947875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe112d87c57e9e1a35952bff43c440e479425cbb2072bb30d46ec5e48ef1d5ed`  
		Last Modified: Mon, 10 Mar 2025 19:23:38 GMT  
		Size: 336.7 KB (336664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a8f72395d7a538089f03dda01a55179ebe826230899d893a424d7c1f459b2d`  
		Last Modified: Mon, 10 Mar 2025 19:23:38 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdaad10511d6e7fe76c649ec4b3289a2d957beee577fb92766e4a0f76d2f91`  
		Last Modified: Mon, 10 Mar 2025 19:23:40 GMT  
		Size: 27.1 MB (27053598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccf49c0175b5f99e9175cfc7527624ecc5d3482279ebac616c6abe404e220c3`  
		Last Modified: Mon, 10 Mar 2025 20:31:45 GMT  
		Size: 282.0 MB (282030404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:51c768f23fb5b6395809d7e493ee9553237dbe743324c48e2aed982d728fd483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42198532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ed227686c0cee77d229a94071bacc0141b6a4f5b24f3bbe40dd6dd8058938b`

```dockerfile
```

-	Layers:
	-	`sha256:9a23e993c71cc1fcb5c73d3dfc0d96a2b5ddafe923be525c20a98e8070574eea`  
		Last Modified: Mon, 10 Mar 2025 20:31:41 GMT  
		Size: 42.2 MB (42188742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6db7221d71869234341cecf4fc8d3abc3e7db23da1388e27be6e8f38b6a701`  
		Last Modified: Mon, 10 Mar 2025 20:31:39 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:494e6af9aa6f9d68674f886a5ab7ee638218aaa163150f674513d42ef09fb6f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d13ffac35796e54aa42b7a21b88ee955c1145f3402cecec85612abcd7918990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295245503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912c842a4d49b0b9d92c954407b57f345b46bd030ae9ebbe566f49d68b4ded3a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9da1b5048f08150019e977d6e262db7577c0ddca858e147df7d9bf93f79da`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 683.6 KB (683556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e54389289d908213d0e62f13c72b2001cc525190c511ba09dfad5c8b084fb`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 3.6 MB (3563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5382010868ddf658e88e6bffad5d0ce76a6a6a6b354b9cce80c97e508cb63`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b64bc19922e1f6345f2b4e899c22ff3b9b37a905b50f5c6e0784ada292f34`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee44a6aadcf0d84954979ffc4c8878dd6ea0ef9a78cb99a31bced6981ef5ed`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 122.8 MB (122794979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48198ad8c8df02f87473863271fe668e6d78defe02d55c43b7168acc66a4ecc2`  
		Last Modified: Wed, 09 Apr 2025 01:20:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa100ae83b33f4a00647f4b3dc436a7eed071ab68f18a6142f712d0c9494f234`  
		Last Modified: Wed, 09 Apr 2025 02:48:53 GMT  
		Size: 110.2 MB (110171845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666490107601b7f396f20994e344057fd40294b1dd92231b664ee7c1891c960`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 338.1 KB (338060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785cc6e2f10ee0b8f089cc0aa88c5953ea75ba381b07211777ce66d9dd2231ed`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc80d84363dd2e6e993857b7b92a78ab887b160a51889507644e5631a9ae4d90`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 28.0 MB (27971330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b87601e7c0e4423ab4aee54236027627d8aaabb244d3b8b3b72732261f437479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23842704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b9a25f25f8e121a157fc317fec8bdf8c81b96dac72debd3ba70cccc64b87f`

```dockerfile
```

-	Layers:
	-	`sha256:0f3278fe6bdbd870ca9558a781eec6129bbdcd5617674ee4cdca44ad19a42c8c`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 23.8 MB (23825531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a06df7eca501cc5b6bad5ac6b27c6a4e0f4653c365c5f83b05c3db2d9459ba`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:97fa7c3fa68dfebbce0b528b0c1af309e79b5a11a66439b98faa891e6067a69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283726192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3bf1c4c42b0f39c5edb2233c098b47eca10b96b0aa3a9fe24ee31dbbf39d73`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a60662d472c0013b6b8d0ea8420230ca63c5a5cc05908698fa85ce4d690d0c`  
		Last Modified: Wed, 09 Apr 2025 09:16:43 GMT  
		Size: 117.6 MB (117638537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c91896a405184701e3d8a7ccd13bb50b4678fd39d67f09c91da7542824b3c9`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9af466fad2f65e605b90e86db4c3ddcc8167fe2a0eafabfe3be94dfbfaa7f`  
		Last Modified: Wed, 09 Apr 2025 15:54:53 GMT  
		Size: 105.6 MB (105595325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5c94d4c8356be193c6875cb17e4c4820fcba1569c0569a48c7dbd73b8f9ac`  
		Last Modified: Wed, 09 Apr 2025 15:54:51 GMT  
		Size: 338.1 KB (338058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d33a92e1576144cea07ccfea2ddf7551cef8851883f7b4632198fa3d8db85c`  
		Last Modified: Wed, 09 Apr 2025 15:54:50 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42682e414427c952a849a517769a2a9330a32f2a861c581ed4ef05222f31dc83`  
		Last Modified: Wed, 09 Apr 2025 15:54:52 GMT  
		Size: 27.1 MB (27057105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0c27edcee39479c73854211193e79bc49ebb8ec058233abcc182d045f0acb033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23865385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a9629b17a579f604e195a9ed04ef7cddfae02b6acb5d620f2c27915293e659`

```dockerfile
```

-	Layers:
	-	`sha256:b5ac138ec0c5ec3081078624554ff778435334f32befc9be7291929b418221ca`  
		Last Modified: Wed, 09 Apr 2025 15:54:51 GMT  
		Size: 23.8 MB (23848075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036d8cecede9934cb0de979b1532749a82bfe265b6518a702246beaa7c7cad0f`  
		Last Modified: Wed, 09 Apr 2025 15:54:50 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:494e6af9aa6f9d68674f886a5ab7ee638218aaa163150f674513d42ef09fb6f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:d13ffac35796e54aa42b7a21b88ee955c1145f3402cecec85612abcd7918990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295245503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912c842a4d49b0b9d92c954407b57f345b46bd030ae9ebbe566f49d68b4ded3a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9da1b5048f08150019e977d6e262db7577c0ddca858e147df7d9bf93f79da`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 683.6 KB (683556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e54389289d908213d0e62f13c72b2001cc525190c511ba09dfad5c8b084fb`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 3.6 MB (3563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5382010868ddf658e88e6bffad5d0ce76a6a6a6b354b9cce80c97e508cb63`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b64bc19922e1f6345f2b4e899c22ff3b9b37a905b50f5c6e0784ada292f34`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee44a6aadcf0d84954979ffc4c8878dd6ea0ef9a78cb99a31bced6981ef5ed`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 122.8 MB (122794979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48198ad8c8df02f87473863271fe668e6d78defe02d55c43b7168acc66a4ecc2`  
		Last Modified: Wed, 09 Apr 2025 01:20:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa100ae83b33f4a00647f4b3dc436a7eed071ab68f18a6142f712d0c9494f234`  
		Last Modified: Wed, 09 Apr 2025 02:48:53 GMT  
		Size: 110.2 MB (110171845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666490107601b7f396f20994e344057fd40294b1dd92231b664ee7c1891c960`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 338.1 KB (338060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785cc6e2f10ee0b8f089cc0aa88c5953ea75ba381b07211777ce66d9dd2231ed`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc80d84363dd2e6e993857b7b92a78ab887b160a51889507644e5631a9ae4d90`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 28.0 MB (27971330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b87601e7c0e4423ab4aee54236027627d8aaabb244d3b8b3b72732261f437479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23842704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111b9a25f25f8e121a157fc317fec8bdf8c81b96dac72debd3ba70cccc64b87f`

```dockerfile
```

-	Layers:
	-	`sha256:0f3278fe6bdbd870ca9558a781eec6129bbdcd5617674ee4cdca44ad19a42c8c`  
		Last Modified: Wed, 09 Apr 2025 02:48:50 GMT  
		Size: 23.8 MB (23825531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a06df7eca501cc5b6bad5ac6b27c6a4e0f4653c365c5f83b05c3db2d9459ba`  
		Last Modified: Wed, 09 Apr 2025 02:48:49 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:97fa7c3fa68dfebbce0b528b0c1af309e79b5a11a66439b98faa891e6067a69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283726192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3bf1c4c42b0f39c5edb2233c098b47eca10b96b0aa3a9fe24ee31dbbf39d73`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a60662d472c0013b6b8d0ea8420230ca63c5a5cc05908698fa85ce4d690d0c`  
		Last Modified: Wed, 09 Apr 2025 09:16:43 GMT  
		Size: 117.6 MB (117638537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c91896a405184701e3d8a7ccd13bb50b4678fd39d67f09c91da7542824b3c9`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9af466fad2f65e605b90e86db4c3ddcc8167fe2a0eafabfe3be94dfbfaa7f`  
		Last Modified: Wed, 09 Apr 2025 15:54:53 GMT  
		Size: 105.6 MB (105595325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5c94d4c8356be193c6875cb17e4c4820fcba1569c0569a48c7dbd73b8f9ac`  
		Last Modified: Wed, 09 Apr 2025 15:54:51 GMT  
		Size: 338.1 KB (338058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d33a92e1576144cea07ccfea2ddf7551cef8851883f7b4632198fa3d8db85c`  
		Last Modified: Wed, 09 Apr 2025 15:54:50 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42682e414427c952a849a517769a2a9330a32f2a861c581ed4ef05222f31dc83`  
		Last Modified: Wed, 09 Apr 2025 15:54:52 GMT  
		Size: 27.1 MB (27057105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0c27edcee39479c73854211193e79bc49ebb8ec058233abcc182d045f0acb033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23865385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a9629b17a579f604e195a9ed04ef7cddfae02b6acb5d620f2c27915293e659`

```dockerfile
```

-	Layers:
	-	`sha256:b5ac138ec0c5ec3081078624554ff778435334f32befc9be7291929b418221ca`  
		Last Modified: Wed, 09 Apr 2025 15:54:51 GMT  
		Size: 23.8 MB (23848075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036d8cecede9934cb0de979b1532749a82bfe265b6518a702246beaa7c7cad0f`  
		Last Modified: Wed, 09 Apr 2025 15:54:50 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:f2b4765659d16dd4f1f6b393dd83dae59fead9170d040fc1cf9decafac98cbd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f189a8beab995fe6d4089037e6271b18a135f54e4c5419094ea5521654eedbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156761814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4812ff35af762386f778c6dbac497fcb7e5e5e37f4867538d3bc93ba91e3742d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9da1b5048f08150019e977d6e262db7577c0ddca858e147df7d9bf93f79da`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 683.6 KB (683556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e54389289d908213d0e62f13c72b2001cc525190c511ba09dfad5c8b084fb`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 3.6 MB (3563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5382010868ddf658e88e6bffad5d0ce76a6a6a6b354b9cce80c97e508cb63`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b64bc19922e1f6345f2b4e899c22ff3b9b37a905b50f5c6e0784ada292f34`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee44a6aadcf0d84954979ffc4c8878dd6ea0ef9a78cb99a31bced6981ef5ed`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 122.8 MB (122794979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48198ad8c8df02f87473863271fe668e6d78defe02d55c43b7168acc66a4ecc2`  
		Last Modified: Wed, 09 Apr 2025 01:20:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1b5482fe1e1507f49fe013bec9a5b1996e805753c0deb290c5c9939b8ce83695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17796623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b0b800c933cc35c5239b6571e84eeadf2b87fb6a29d9d26655a2a6f8c8eea`

```dockerfile
```

-	Layers:
	-	`sha256:d41a9071eb7d8ecac362ae42915cdc2eaff4c34da8c42cd96c9125a509167f4e`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 17.8 MB (17780229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245f7e10fcd0db42ea9e7f2ef2b0a51d1d3dbb59a050fee13607d17031cd83a8`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:039b42fb976a37a22f30d3bfc94c097eadf24c3bb2eee27c65e12891434e2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150733271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0f09b2208f9cde4993678acbeb8729636c3665064cb42ba6e04fd9c6eda3a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a60662d472c0013b6b8d0ea8420230ca63c5a5cc05908698fa85ce4d690d0c`  
		Last Modified: Wed, 09 Apr 2025 09:16:43 GMT  
		Size: 117.6 MB (117638537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c91896a405184701e3d8a7ccd13bb50b4678fd39d67f09c91da7542824b3c9`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:06ba545c0b8c795b2a0ec3fecbe6b769cf1d5b4c8e73b90d605a448ef378f632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17770769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543a87320a7b02c76e6f3c2fa8cdf0b359904c9187b660cded059bf5c37f845`

```dockerfile
```

-	Layers:
	-	`sha256:3a1208b322e6587034825646df2cdf09a099cefcb877bc438a58fa52e688fcf8`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 17.8 MB (17754235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c1de3b281c6ace12bb55b923a352190f112efc43cfe5dfb03b24d1b54373a2`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 16.5 KB (16534 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:f2b4765659d16dd4f1f6b393dd83dae59fead9170d040fc1cf9decafac98cbd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:f189a8beab995fe6d4089037e6271b18a135f54e4c5419094ea5521654eedbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156761814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4812ff35af762386f778c6dbac497fcb7e5e5e37f4867538d3bc93ba91e3742d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9da1b5048f08150019e977d6e262db7577c0ddca858e147df7d9bf93f79da`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 683.6 KB (683556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e54389289d908213d0e62f13c72b2001cc525190c511ba09dfad5c8b084fb`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 3.6 MB (3563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5382010868ddf658e88e6bffad5d0ce76a6a6a6b354b9cce80c97e508cb63`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b64bc19922e1f6345f2b4e899c22ff3b9b37a905b50f5c6e0784ada292f34`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee44a6aadcf0d84954979ffc4c8878dd6ea0ef9a78cb99a31bced6981ef5ed`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 122.8 MB (122794979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48198ad8c8df02f87473863271fe668e6d78defe02d55c43b7168acc66a4ecc2`  
		Last Modified: Wed, 09 Apr 2025 01:20:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1b5482fe1e1507f49fe013bec9a5b1996e805753c0deb290c5c9939b8ce83695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17796623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b0b800c933cc35c5239b6571e84eeadf2b87fb6a29d9d26655a2a6f8c8eea`

```dockerfile
```

-	Layers:
	-	`sha256:d41a9071eb7d8ecac362ae42915cdc2eaff4c34da8c42cd96c9125a509167f4e`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 17.8 MB (17780229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245f7e10fcd0db42ea9e7f2ef2b0a51d1d3dbb59a050fee13607d17031cd83a8`  
		Last Modified: Wed, 09 Apr 2025 01:20:46 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:039b42fb976a37a22f30d3bfc94c097eadf24c3bb2eee27c65e12891434e2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150733271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0f09b2208f9cde4993678acbeb8729636c3665064cb42ba6e04fd9c6eda3a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a60662d472c0013b6b8d0ea8420230ca63c5a5cc05908698fa85ce4d690d0c`  
		Last Modified: Wed, 09 Apr 2025 09:16:43 GMT  
		Size: 117.6 MB (117638537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c91896a405184701e3d8a7ccd13bb50b4678fd39d67f09c91da7542824b3c9`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:06ba545c0b8c795b2a0ec3fecbe6b769cf1d5b4c8e73b90d605a448ef378f632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17770769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543a87320a7b02c76e6f3c2fa8cdf0b359904c9187b660cded059bf5c37f845`

```dockerfile
```

-	Layers:
	-	`sha256:3a1208b322e6587034825646df2cdf09a099cefcb877bc438a58fa52e688fcf8`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 17.8 MB (17754235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c1de3b281c6ace12bb55b923a352190f112efc43cfe5dfb03b24d1b54373a2`  
		Last Modified: Wed, 09 Apr 2025 09:16:39 GMT  
		Size: 16.5 KB (16534 bytes)  
		MIME: application/vnd.in-toto+json
