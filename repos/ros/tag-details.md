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
$ docker pull ros@sha256:846db6e1cee81e5cb54a23dc5d5f80e55a0d475d55429e04fa37915f35a96456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:252e7914962d04ea3c1e0b74a2aee993a0810a2c7b0e4380ca360510d7d11c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262008279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b07102ad8990d51397310a5c2a99ccac61df66d6f71f7006855345ba9af8c7a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17604984d3c226f9af9ddc4c76bbdbf6329f20bd317bba55ac221a89f78509de`  
		Last Modified: Sat, 17 Aug 2024 04:07:36 GMT  
		Size: 97.9 MB (97936001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759dfa6c3117134cd7385d39c7a1e2f81ff00d294235ac6a16a31ba6bfbdf602`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 336.4 KB (336415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8369f26ac446b6797caae036f291c10f1a09d6c31c0356bf810a96aa00cb38`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1d9a2fd5a80dade3857fa54fcc8475b78c15a96524cac91006be6a427639f`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.8 MB (22825487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:4388c1bfd0ce8378e22b995628e9203539fc6002a0805384672245af4441b24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22690679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9de804a26bb10457cf42f0ca8313f620f1083621c5bb0d56b102e132ded8b6`

```dockerfile
```

-	Layers:
	-	`sha256:d7143bc60a3c3877400ec04e3efe617b29d6bc5ecb8efcf6cb34b1639c657463`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.7 MB (22673557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e274b66c66e82169ce34eb3366fdb49fd1d5f6fdc3c8e8918257376878509d`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 17.1 KB (17122 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f54ebef77411238c363ffa41c70aea5a5b82a9252eb603dc9fe254e8dfcdafd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254487091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7def2430910b25be630d50ae54e362972f05e3303a481678618afa4ef9999f3`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a80cf954f3da0bbead621f6f187a31b68fa9fe9b3f2347e28dbc3ff02bd9b`  
		Last Modified: Fri, 05 Jul 2024 20:42:11 GMT  
		Size: 104.3 MB (104254849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75bcda3628cc9b6c17574b9aa6fe792c98769b671e75adcf704f65de24caec`  
		Last Modified: Fri, 05 Jul 2024 20:42:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4439a92ef939d81c051b27134091b79a13540430388ff45e86d5325966519d3`  
		Last Modified: Fri, 05 Jul 2024 21:13:31 GMT  
		Size: 95.5 MB (95495749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ccd4c7e7ac9c164f4a51eb05822f9c9a40454975e7bb68807b5dca18a1878`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 329.6 KB (329602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e43b591bf8f05661f79aed916d88281ff16bbe1683306bb95ee26cff09e0`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a6c377510a80093944d7501857f77200004ec3481e20b26d7f1e3b8d2be95`  
		Last Modified: Fri, 05 Jul 2024 21:13:30 GMT  
		Size: 22.2 MB (22231077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:401301555f37d6f4b9919d331dbb2b4960db5a9cc5e6e522613a3e5d3b74ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22577041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badfde6436cd6a8bf70d6704bc12e7c369eb9c94463e1be4f552ae66f76dcda5`

```dockerfile
```

-	Layers:
	-	`sha256:d73cc2e273d6f9b5e8669998741db2fbbfe0a5255b1ec1316712b8cc6831ae0c`  
		Last Modified: Fri, 05 Jul 2024 21:13:29 GMT  
		Size: 22.6 MB (22559546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a06c7da23d98936ba075ebee1b2af25a8df694c5917dff8d1239a1eec87bbd2`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 17.5 KB (17495 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:2accf04ab6313eb826a4b185897fb5724894bd50db79270031fe5663e3c812ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:30cf486cd3f11948045fd18cdb6fa778338c142d5f7abe9ec32e9257530c377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.5 MB (953543306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63371e14e0d53aff5126aeef880c96dea62a10d32c8a68540d98bd08fbdf55a7`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17604984d3c226f9af9ddc4c76bbdbf6329f20bd317bba55ac221a89f78509de`  
		Last Modified: Sat, 17 Aug 2024 04:07:36 GMT  
		Size: 97.9 MB (97936001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759dfa6c3117134cd7385d39c7a1e2f81ff00d294235ac6a16a31ba6bfbdf602`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 336.4 KB (336415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8369f26ac446b6797caae036f291c10f1a09d6c31c0356bf810a96aa00cb38`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1d9a2fd5a80dade3857fa54fcc8475b78c15a96524cac91006be6a427639f`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.8 MB (22825487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56ea45ed094c2beaf5aba9df68b40e9c61caf09ab723bafcba20d2bdf2d3d1`  
		Last Modified: Sat, 17 Aug 2024 05:03:05 GMT  
		Size: 691.5 MB (691535027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:420afda6ba38bc2046b1e967e849e432ab4a23aeef6d0ca6d0ded3d24c5bcc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57278510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7bf8f012926616bda590036a7f925e0192c6be3c0831b72ad1d187b2f5673f`

```dockerfile
```

-	Layers:
	-	`sha256:8486c26d631dd874974d8d960ac3dc6668cd1538c46813fec23c32cb27ab6b6e`  
		Last Modified: Sat, 17 Aug 2024 05:02:58 GMT  
		Size: 57.3 MB (57268843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fff7b226ef2c58eac33e5e0b1ed793ad19b7bb354be75b0b240c2c3b0a6817`  
		Last Modified: Sat, 17 Aug 2024 05:02:56 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d2b16e44d76dbcb854fcc0b99f82061537ff92b8eb93bf71fd5400b8449eee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.9 MB (913939947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248d9599dabe2e57eb67b4014aa2fd69ef92228e1dbfe29ebc477cea29125b06`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a80cf954f3da0bbead621f6f187a31b68fa9fe9b3f2347e28dbc3ff02bd9b`  
		Last Modified: Fri, 05 Jul 2024 20:42:11 GMT  
		Size: 104.3 MB (104254849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75bcda3628cc9b6c17574b9aa6fe792c98769b671e75adcf704f65de24caec`  
		Last Modified: Fri, 05 Jul 2024 20:42:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4439a92ef939d81c051b27134091b79a13540430388ff45e86d5325966519d3`  
		Last Modified: Fri, 05 Jul 2024 21:13:31 GMT  
		Size: 95.5 MB (95495749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ccd4c7e7ac9c164f4a51eb05822f9c9a40454975e7bb68807b5dca18a1878`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 329.6 KB (329602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e43b591bf8f05661f79aed916d88281ff16bbe1683306bb95ee26cff09e0`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a6c377510a80093944d7501857f77200004ec3481e20b26d7f1e3b8d2be95`  
		Last Modified: Fri, 05 Jul 2024 21:13:30 GMT  
		Size: 22.2 MB (22231077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c38d1cafe9b3c575c695d60acfdcfb8a3d93189dcd0392ab6700170adba3c1`  
		Last Modified: Fri, 05 Jul 2024 23:35:48 GMT  
		Size: 659.5 MB (659452856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:752677fec29adc76b5168a3947fabd7e403bc1042cfaecb15654b5e0c0c57d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57022234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f419999d559b605477a8437ce23da55ee013564e73d801042186ad50b7fb4be7`

```dockerfile
```

-	Layers:
	-	`sha256:54c93fb447016e5e9808edc714c2786b411bd71f1f0e3f9668473b6f34a8bc7f`  
		Last Modified: Fri, 05 Jul 2024 23:35:36 GMT  
		Size: 57.0 MB (57012206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb544d2b97e6908ddc50f7c65823dd823d17544414c8447aa649843c04b7f13`  
		Last Modified: Fri, 05 Jul 2024 23:35:35 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:2accf04ab6313eb826a4b185897fb5724894bd50db79270031fe5663e3c812ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:30cf486cd3f11948045fd18cdb6fa778338c142d5f7abe9ec32e9257530c377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.5 MB (953543306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63371e14e0d53aff5126aeef880c96dea62a10d32c8a68540d98bd08fbdf55a7`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17604984d3c226f9af9ddc4c76bbdbf6329f20bd317bba55ac221a89f78509de`  
		Last Modified: Sat, 17 Aug 2024 04:07:36 GMT  
		Size: 97.9 MB (97936001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759dfa6c3117134cd7385d39c7a1e2f81ff00d294235ac6a16a31ba6bfbdf602`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 336.4 KB (336415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8369f26ac446b6797caae036f291c10f1a09d6c31c0356bf810a96aa00cb38`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1d9a2fd5a80dade3857fa54fcc8475b78c15a96524cac91006be6a427639f`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.8 MB (22825487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56ea45ed094c2beaf5aba9df68b40e9c61caf09ab723bafcba20d2bdf2d3d1`  
		Last Modified: Sat, 17 Aug 2024 05:03:05 GMT  
		Size: 691.5 MB (691535027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:420afda6ba38bc2046b1e967e849e432ab4a23aeef6d0ca6d0ded3d24c5bcc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57278510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7bf8f012926616bda590036a7f925e0192c6be3c0831b72ad1d187b2f5673f`

```dockerfile
```

-	Layers:
	-	`sha256:8486c26d631dd874974d8d960ac3dc6668cd1538c46813fec23c32cb27ab6b6e`  
		Last Modified: Sat, 17 Aug 2024 05:02:58 GMT  
		Size: 57.3 MB (57268843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fff7b226ef2c58eac33e5e0b1ed793ad19b7bb354be75b0b240c2c3b0a6817`  
		Last Modified: Sat, 17 Aug 2024 05:02:56 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d2b16e44d76dbcb854fcc0b99f82061537ff92b8eb93bf71fd5400b8449eee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.9 MB (913939947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248d9599dabe2e57eb67b4014aa2fd69ef92228e1dbfe29ebc477cea29125b06`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a80cf954f3da0bbead621f6f187a31b68fa9fe9b3f2347e28dbc3ff02bd9b`  
		Last Modified: Fri, 05 Jul 2024 20:42:11 GMT  
		Size: 104.3 MB (104254849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75bcda3628cc9b6c17574b9aa6fe792c98769b671e75adcf704f65de24caec`  
		Last Modified: Fri, 05 Jul 2024 20:42:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4439a92ef939d81c051b27134091b79a13540430388ff45e86d5325966519d3`  
		Last Modified: Fri, 05 Jul 2024 21:13:31 GMT  
		Size: 95.5 MB (95495749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ccd4c7e7ac9c164f4a51eb05822f9c9a40454975e7bb68807b5dca18a1878`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 329.6 KB (329602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e43b591bf8f05661f79aed916d88281ff16bbe1683306bb95ee26cff09e0`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a6c377510a80093944d7501857f77200004ec3481e20b26d7f1e3b8d2be95`  
		Last Modified: Fri, 05 Jul 2024 21:13:30 GMT  
		Size: 22.2 MB (22231077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c38d1cafe9b3c575c695d60acfdcfb8a3d93189dcd0392ab6700170adba3c1`  
		Last Modified: Fri, 05 Jul 2024 23:35:48 GMT  
		Size: 659.5 MB (659452856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:752677fec29adc76b5168a3947fabd7e403bc1042cfaecb15654b5e0c0c57d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57022234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f419999d559b605477a8437ce23da55ee013564e73d801042186ad50b7fb4be7`

```dockerfile
```

-	Layers:
	-	`sha256:54c93fb447016e5e9808edc714c2786b411bd71f1f0e3f9668473b6f34a8bc7f`  
		Last Modified: Fri, 05 Jul 2024 23:35:36 GMT  
		Size: 57.0 MB (57012206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb544d2b97e6908ddc50f7c65823dd823d17544414c8447aa649843c04b7f13`  
		Last Modified: Fri, 05 Jul 2024 23:35:35 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:846db6e1cee81e5cb54a23dc5d5f80e55a0d475d55429e04fa37915f35a96456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:252e7914962d04ea3c1e0b74a2aee993a0810a2c7b0e4380ca360510d7d11c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262008279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b07102ad8990d51397310a5c2a99ccac61df66d6f71f7006855345ba9af8c7a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17604984d3c226f9af9ddc4c76bbdbf6329f20bd317bba55ac221a89f78509de`  
		Last Modified: Sat, 17 Aug 2024 04:07:36 GMT  
		Size: 97.9 MB (97936001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759dfa6c3117134cd7385d39c7a1e2f81ff00d294235ac6a16a31ba6bfbdf602`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 336.4 KB (336415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8369f26ac446b6797caae036f291c10f1a09d6c31c0356bf810a96aa00cb38`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1d9a2fd5a80dade3857fa54fcc8475b78c15a96524cac91006be6a427639f`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.8 MB (22825487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:4388c1bfd0ce8378e22b995628e9203539fc6002a0805384672245af4441b24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22690679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9de804a26bb10457cf42f0ca8313f620f1083621c5bb0d56b102e132ded8b6`

```dockerfile
```

-	Layers:
	-	`sha256:d7143bc60a3c3877400ec04e3efe617b29d6bc5ecb8efcf6cb34b1639c657463`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.7 MB (22673557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e274b66c66e82169ce34eb3366fdb49fd1d5f6fdc3c8e8918257376878509d`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 17.1 KB (17122 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f54ebef77411238c363ffa41c70aea5a5b82a9252eb603dc9fe254e8dfcdafd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254487091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7def2430910b25be630d50ae54e362972f05e3303a481678618afa4ef9999f3`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a80cf954f3da0bbead621f6f187a31b68fa9fe9b3f2347e28dbc3ff02bd9b`  
		Last Modified: Fri, 05 Jul 2024 20:42:11 GMT  
		Size: 104.3 MB (104254849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75bcda3628cc9b6c17574b9aa6fe792c98769b671e75adcf704f65de24caec`  
		Last Modified: Fri, 05 Jul 2024 20:42:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4439a92ef939d81c051b27134091b79a13540430388ff45e86d5325966519d3`  
		Last Modified: Fri, 05 Jul 2024 21:13:31 GMT  
		Size: 95.5 MB (95495749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ccd4c7e7ac9c164f4a51eb05822f9c9a40454975e7bb68807b5dca18a1878`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 329.6 KB (329602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e43b591bf8f05661f79aed916d88281ff16bbe1683306bb95ee26cff09e0`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a6c377510a80093944d7501857f77200004ec3481e20b26d7f1e3b8d2be95`  
		Last Modified: Fri, 05 Jul 2024 21:13:30 GMT  
		Size: 22.2 MB (22231077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:401301555f37d6f4b9919d331dbb2b4960db5a9cc5e6e522613a3e5d3b74ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22577041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badfde6436cd6a8bf70d6704bc12e7c369eb9c94463e1be4f552ae66f76dcda5`

```dockerfile
```

-	Layers:
	-	`sha256:d73cc2e273d6f9b5e8669998741db2fbbfe0a5255b1ec1316712b8cc6831ae0c`  
		Last Modified: Fri, 05 Jul 2024 21:13:29 GMT  
		Size: 22.6 MB (22559546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a06c7da23d98936ba075ebee1b2af25a8df694c5917dff8d1239a1eec87bbd2`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 17.5 KB (17495 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:846db6e1cee81e5cb54a23dc5d5f80e55a0d475d55429e04fa37915f35a96456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:252e7914962d04ea3c1e0b74a2aee993a0810a2c7b0e4380ca360510d7d11c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262008279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b07102ad8990d51397310a5c2a99ccac61df66d6f71f7006855345ba9af8c7a`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17604984d3c226f9af9ddc4c76bbdbf6329f20bd317bba55ac221a89f78509de`  
		Last Modified: Sat, 17 Aug 2024 04:07:36 GMT  
		Size: 97.9 MB (97936001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759dfa6c3117134cd7385d39c7a1e2f81ff00d294235ac6a16a31ba6bfbdf602`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 336.4 KB (336415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8369f26ac446b6797caae036f291c10f1a09d6c31c0356bf810a96aa00cb38`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1d9a2fd5a80dade3857fa54fcc8475b78c15a96524cac91006be6a427639f`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.8 MB (22825487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4388c1bfd0ce8378e22b995628e9203539fc6002a0805384672245af4441b24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22690679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9de804a26bb10457cf42f0ca8313f620f1083621c5bb0d56b102e132ded8b6`

```dockerfile
```

-	Layers:
	-	`sha256:d7143bc60a3c3877400ec04e3efe617b29d6bc5ecb8efcf6cb34b1639c657463`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.7 MB (22673557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e274b66c66e82169ce34eb3366fdb49fd1d5f6fdc3c8e8918257376878509d`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 17.1 KB (17122 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f54ebef77411238c363ffa41c70aea5a5b82a9252eb603dc9fe254e8dfcdafd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254487091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7def2430910b25be630d50ae54e362972f05e3303a481678618afa4ef9999f3`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a80cf954f3da0bbead621f6f187a31b68fa9fe9b3f2347e28dbc3ff02bd9b`  
		Last Modified: Fri, 05 Jul 2024 20:42:11 GMT  
		Size: 104.3 MB (104254849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75bcda3628cc9b6c17574b9aa6fe792c98769b671e75adcf704f65de24caec`  
		Last Modified: Fri, 05 Jul 2024 20:42:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4439a92ef939d81c051b27134091b79a13540430388ff45e86d5325966519d3`  
		Last Modified: Fri, 05 Jul 2024 21:13:31 GMT  
		Size: 95.5 MB (95495749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ccd4c7e7ac9c164f4a51eb05822f9c9a40454975e7bb68807b5dca18a1878`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 329.6 KB (329602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e43b591bf8f05661f79aed916d88281ff16bbe1683306bb95ee26cff09e0`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a6c377510a80093944d7501857f77200004ec3481e20b26d7f1e3b8d2be95`  
		Last Modified: Fri, 05 Jul 2024 21:13:30 GMT  
		Size: 22.2 MB (22231077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:401301555f37d6f4b9919d331dbb2b4960db5a9cc5e6e522613a3e5d3b74ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22577041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badfde6436cd6a8bf70d6704bc12e7c369eb9c94463e1be4f552ae66f76dcda5`

```dockerfile
```

-	Layers:
	-	`sha256:d73cc2e273d6f9b5e8669998741db2fbbfe0a5255b1ec1316712b8cc6831ae0c`  
		Last Modified: Fri, 05 Jul 2024 21:13:29 GMT  
		Size: 22.6 MB (22559546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a06c7da23d98936ba075ebee1b2af25a8df694c5917dff8d1239a1eec87bbd2`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 17.5 KB (17495 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:748d74758a37dce3dcc358fcb028b22a064813e0a8126933a97fa12b62797d4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:273279b99b53fa62526f367def6c25b5c7206ab2e337ceea2fb5132980f385cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140907965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea466fb89f40dfce2ed6aeb308749108a15dc6e631de20851f4557d7073c024`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:15b39854f1b5bec9ba3674052584294e8f3e56a0c0030eb53c18f3eaa8020088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16971353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b0796a1b5b7ac78a492f5feed9c5df97eb3a67431999e5c9aea8de44eba569`

```dockerfile
```

-	Layers:
	-	`sha256:0400f298396fd054345c54aa82f03ad8ed574daf5f8550407d3a6817eb1f69f8`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 17.0 MB (16955216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf2898e14d341110cf49b9c77015ec91699f87226db7a03aaea7ead097ec7c`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bb304aa559114f8d6ef3bb3ef5fe8f4bc7821f33aa35a0cafe13599b732add44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136438911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a208dd7ba1f41e681f280585eb5612d8760911591cb2a24bf9249930e3ed75`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c92e67449590912b6c7755a150613269346b5015b668c99f2db49450f6a8e8`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 1.2 MB (1215007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2693553852f919b16b21546e1d8543a7ad744597e5f6749446017c3790d7277`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 3.6 MB (3595960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9fe7ebd0a06ee011e10d604fd769d9ff4552a42b94b0887d4e53098983bf75`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074b02edbde483a99adecce394a1c8fe6ec4582c39bad3ac5050bd5c6a5466b`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52f3878065eb3ee88c776c4daebe7310fe219adc004d71d843d7ae13921f44b`  
		Last Modified: Sat, 17 Aug 2024 03:57:12 GMT  
		Size: 104.3 MB (104266794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd9444ec78d82b8472db5e98823f37ae6d6f2c2f73640f40d3764e0b2813ae`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:d1223f4ddf4451faa4c5c5462dff7604c1d37c2d30970e35e3f025d94d9dcc8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16958359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3077d0cf67afb7c0b8a112876cc626c8af516835c2867a2761d69a76d60e2c7`

```dockerfile
```

-	Layers:
	-	`sha256:b776e091b066de05a97da896ef568e455fe9d644cc7e98ca0ce17129c1698d27`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 16.9 MB (16941945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c395d30d3b958b8c96887624c748be7b794a266815d6661b27a28169a321a6`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:748d74758a37dce3dcc358fcb028b22a064813e0a8126933a97fa12b62797d4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:273279b99b53fa62526f367def6c25b5c7206ab2e337ceea2fb5132980f385cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140907965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea466fb89f40dfce2ed6aeb308749108a15dc6e631de20851f4557d7073c024`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:15b39854f1b5bec9ba3674052584294e8f3e56a0c0030eb53c18f3eaa8020088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16971353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b0796a1b5b7ac78a492f5feed9c5df97eb3a67431999e5c9aea8de44eba569`

```dockerfile
```

-	Layers:
	-	`sha256:0400f298396fd054345c54aa82f03ad8ed574daf5f8550407d3a6817eb1f69f8`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 17.0 MB (16955216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf2898e14d341110cf49b9c77015ec91699f87226db7a03aaea7ead097ec7c`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bb304aa559114f8d6ef3bb3ef5fe8f4bc7821f33aa35a0cafe13599b732add44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136438911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a208dd7ba1f41e681f280585eb5612d8760911591cb2a24bf9249930e3ed75`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c92e67449590912b6c7755a150613269346b5015b668c99f2db49450f6a8e8`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 1.2 MB (1215007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2693553852f919b16b21546e1d8543a7ad744597e5f6749446017c3790d7277`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 3.6 MB (3595960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9fe7ebd0a06ee011e10d604fd769d9ff4552a42b94b0887d4e53098983bf75`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074b02edbde483a99adecce394a1c8fe6ec4582c39bad3ac5050bd5c6a5466b`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52f3878065eb3ee88c776c4daebe7310fe219adc004d71d843d7ae13921f44b`  
		Last Modified: Sat, 17 Aug 2024 03:57:12 GMT  
		Size: 104.3 MB (104266794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd9444ec78d82b8472db5e98823f37ae6d6f2c2f73640f40d3764e0b2813ae`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:d1223f4ddf4451faa4c5c5462dff7604c1d37c2d30970e35e3f025d94d9dcc8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16958359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3077d0cf67afb7c0b8a112876cc626c8af516835c2867a2761d69a76d60e2c7`

```dockerfile
```

-	Layers:
	-	`sha256:b776e091b066de05a97da896ef568e455fe9d644cc7e98ca0ce17129c1698d27`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 16.9 MB (16941945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c395d30d3b958b8c96887624c748be7b794a266815d6661b27a28169a321a6`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron`

```console
$ docker pull ros@sha256:f23afa26ab4b34e0e5827f905d5b8e4494c5a5d58b1b015607194cf02d9bb221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:379242c95e2fc0df3ff873e7dc4cb8f3897aa799c34c4f898da31e870d9aebbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267704187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60f697ea9cc5a8853a2279d11acebefd2130b382f4a00a29042021cfacc84e9`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2260612a62c0f31d79217253414a964d458d6efc8c2ae28310775a846b4ef7eb`  
		Last Modified: Sat, 17 Aug 2024 04:07:53 GMT  
		Size: 85.0 MB (84960622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51aaf12e1c08fc8b05c2a5161e1c731ea21e84b9187e3219da32145e6cc48c`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 314.3 KB (314269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec4e939c6ec59149c2a1e62f11968df4a13e465b5699fb2dd8fda1a83bee66`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f534547dafd375b4973e1d2f4be09308403de4de6fd383f5b695ed106417f92`  
		Last Modified: Sat, 17 Aug 2024 04:07:52 GMT  
		Size: 23.7 MB (23733896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:b6287828e4497dec4d781c2674ba9e55f149423ae252f89c62bb84b1706d19a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23694026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075206c2478e07f068d4501dbe416605a5c9910f3d68a5f8c4f7095de507a623`

```dockerfile
```

-	Layers:
	-	`sha256:9c8044a86c7e1b23b681096d75a5090eca18d054c46acf0ba095dc28e8c7262d`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 23.7 MB (23676936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2e2da58e9c10f8f9463fdd00b53f5cc33acab8e115a3d6583dc25f70163896`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 17.1 KB (17090 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:56c0d7d90a4b206c1b726b56aa535ea9adea99e187ab26646ae0c3ccc0aa8c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260022791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1281b31359c8bc875f81187fad1e6c9c72ad37fa7bbd36a883fc396c619cdc8`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a65151261e16b95c42cc0f2d0cdb917819146f037a242ecf1ee7b8de2b2ddd`  
		Last Modified: Fri, 05 Jul 2024 20:43:47 GMT  
		Size: 121.8 MB (121776520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c984738d175b26d50ed03560182815a089083eb2a11aa0ab2517627701d45`  
		Last Modified: Fri, 05 Jul 2024 20:43:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d69fd9744647d964d1e8f768f77146a429bc8e68f4b23999fbbfd75418d45`  
		Last Modified: Fri, 05 Jul 2024 21:14:51 GMT  
		Size: 82.6 MB (82644201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d035d7dde10215aba73591f6b955de11b855ddc4ee8e03c29f299a28eb56712b`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 309.1 KB (309119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94d3e4e9957aecb6ab51a45401c5b1743891d5b7cb211e5c53d118cac076de`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6457c9d5cb93d7645f227282b7cd5c54fdfbe843e587de67969dd5beb7ad93`  
		Last Modified: Fri, 05 Jul 2024 21:14:50 GMT  
		Size: 23.1 MB (23117144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:60f667f1fcfd77dd7d02dbeca3198c7c80fd5c02bd866fb1a26c648cf9fe423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23574381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc3252b6ebf92da99d0df6f2af925f6dcfdbedf86bcd9943d32b1942ec7890b`

```dockerfile
```

-	Layers:
	-	`sha256:d11eb8493b25cf6a9a804c33cc3d5b0ff6f97eca723cbd7f0023faa2d34771e6`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 23.6 MB (23556918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7545fe198f2772c095cdf780b2a0538ad4402b8e27fa23dafb6ba1034eb20164`  
		Last Modified: Fri, 05 Jul 2024 21:14:48 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-perception`

```console
$ docker pull ros@sha256:220547ee05159cc790219b009ba236a1b08203fadce9537921eccbc23948ad4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:9785ef1b1ff02aa40830e209dc59d806a48e8a2be616d73f0eb4adfde4ca4d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.0 MB (960012504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede68817b3cc549919bea10f796d79f632dfce030dfe29bc98135dac57e4dde3`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2260612a62c0f31d79217253414a964d458d6efc8c2ae28310775a846b4ef7eb`  
		Last Modified: Sat, 17 Aug 2024 04:07:53 GMT  
		Size: 85.0 MB (84960622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51aaf12e1c08fc8b05c2a5161e1c731ea21e84b9187e3219da32145e6cc48c`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 314.3 KB (314269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec4e939c6ec59149c2a1e62f11968df4a13e465b5699fb2dd8fda1a83bee66`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f534547dafd375b4973e1d2f4be09308403de4de6fd383f5b695ed106417f92`  
		Last Modified: Sat, 17 Aug 2024 04:07:52 GMT  
		Size: 23.7 MB (23733896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b73b09e4bff0c9816a4794e0b1cbe0f022f73432242e06ddb79dfb39d111c`  
		Last Modified: Sat, 17 Aug 2024 05:03:22 GMT  
		Size: 692.3 MB (692308317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:68cbd9aae2bcd60513d99b4c8f2c9d68e4a6df19579f8aa3db86c096b253a3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58260091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9380a4b45d2c0eb7897d2de17394219b68a5c2f68d0194c63507592afdee3461`

```dockerfile
```

-	Layers:
	-	`sha256:419ff3417f702e10b1a70fb31ef60319cfdadf99f944373a7324a48a31ae39d8`  
		Last Modified: Sat, 17 Aug 2024 05:03:11 GMT  
		Size: 58.3 MB (58250450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162a17e4f5223ed6287cfdcade633c9dd2fb33faf874615c3cc1c4817004f624`  
		Last Modified: Sat, 17 Aug 2024 05:03:10 GMT  
		Size: 9.6 KB (9641 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7da21c2f7315db6b1153278dd6f47595a58b6aa195134edd1ba2f9e8029e4db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920196188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd11ed6900f7375590f563df50b6d7c5753208406b85f085ef857b43f69a0314`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a65151261e16b95c42cc0f2d0cdb917819146f037a242ecf1ee7b8de2b2ddd`  
		Last Modified: Fri, 05 Jul 2024 20:43:47 GMT  
		Size: 121.8 MB (121776520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c984738d175b26d50ed03560182815a089083eb2a11aa0ab2517627701d45`  
		Last Modified: Fri, 05 Jul 2024 20:43:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d69fd9744647d964d1e8f768f77146a429bc8e68f4b23999fbbfd75418d45`  
		Last Modified: Fri, 05 Jul 2024 21:14:51 GMT  
		Size: 82.6 MB (82644201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d035d7dde10215aba73591f6b955de11b855ddc4ee8e03c29f299a28eb56712b`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 309.1 KB (309119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94d3e4e9957aecb6ab51a45401c5b1743891d5b7cb211e5c53d118cac076de`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6457c9d5cb93d7645f227282b7cd5c54fdfbe843e587de67969dd5beb7ad93`  
		Last Modified: Fri, 05 Jul 2024 21:14:50 GMT  
		Size: 23.1 MB (23117144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69799820628b45d45a6b4bd29d1e8fff4808119f3dade1703e3f5a01d901923`  
		Last Modified: Fri, 05 Jul 2024 23:42:16 GMT  
		Size: 660.2 MB (660173397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c4d14ec735e30d45167679ede10b2c8bb8e8d9fc3f8abef855e2ccdbda10b9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57998805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eb34605da1df7939e9b3ce404fdcbf7b0d68fefbc1450a68316814a78a1c58`

```dockerfile
```

-	Layers:
	-	`sha256:96d16b69f5c7b95d63887fb880043916aecbfafe108052815d1363a14151963f`  
		Last Modified: Fri, 05 Jul 2024 23:42:05 GMT  
		Size: 58.0 MB (57988803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb26277d9dbc3b03e36ab4f713b6c90ac577dee24f8480666427609ef50c89ae`  
		Last Modified: Fri, 05 Jul 2024 23:42:03 GMT  
		Size: 10.0 KB (10002 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:220547ee05159cc790219b009ba236a1b08203fadce9537921eccbc23948ad4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:9785ef1b1ff02aa40830e209dc59d806a48e8a2be616d73f0eb4adfde4ca4d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.0 MB (960012504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede68817b3cc549919bea10f796d79f632dfce030dfe29bc98135dac57e4dde3`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2260612a62c0f31d79217253414a964d458d6efc8c2ae28310775a846b4ef7eb`  
		Last Modified: Sat, 17 Aug 2024 04:07:53 GMT  
		Size: 85.0 MB (84960622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51aaf12e1c08fc8b05c2a5161e1c731ea21e84b9187e3219da32145e6cc48c`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 314.3 KB (314269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec4e939c6ec59149c2a1e62f11968df4a13e465b5699fb2dd8fda1a83bee66`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f534547dafd375b4973e1d2f4be09308403de4de6fd383f5b695ed106417f92`  
		Last Modified: Sat, 17 Aug 2024 04:07:52 GMT  
		Size: 23.7 MB (23733896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487b73b09e4bff0c9816a4794e0b1cbe0f022f73432242e06ddb79dfb39d111c`  
		Last Modified: Sat, 17 Aug 2024 05:03:22 GMT  
		Size: 692.3 MB (692308317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:68cbd9aae2bcd60513d99b4c8f2c9d68e4a6df19579f8aa3db86c096b253a3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58260091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9380a4b45d2c0eb7897d2de17394219b68a5c2f68d0194c63507592afdee3461`

```dockerfile
```

-	Layers:
	-	`sha256:419ff3417f702e10b1a70fb31ef60319cfdadf99f944373a7324a48a31ae39d8`  
		Last Modified: Sat, 17 Aug 2024 05:03:11 GMT  
		Size: 58.3 MB (58250450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162a17e4f5223ed6287cfdcade633c9dd2fb33faf874615c3cc1c4817004f624`  
		Last Modified: Sat, 17 Aug 2024 05:03:10 GMT  
		Size: 9.6 KB (9641 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7da21c2f7315db6b1153278dd6f47595a58b6aa195134edd1ba2f9e8029e4db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920196188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd11ed6900f7375590f563df50b6d7c5753208406b85f085ef857b43f69a0314`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a65151261e16b95c42cc0f2d0cdb917819146f037a242ecf1ee7b8de2b2ddd`  
		Last Modified: Fri, 05 Jul 2024 20:43:47 GMT  
		Size: 121.8 MB (121776520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c984738d175b26d50ed03560182815a089083eb2a11aa0ab2517627701d45`  
		Last Modified: Fri, 05 Jul 2024 20:43:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d69fd9744647d964d1e8f768f77146a429bc8e68f4b23999fbbfd75418d45`  
		Last Modified: Fri, 05 Jul 2024 21:14:51 GMT  
		Size: 82.6 MB (82644201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d035d7dde10215aba73591f6b955de11b855ddc4ee8e03c29f299a28eb56712b`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 309.1 KB (309119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94d3e4e9957aecb6ab51a45401c5b1743891d5b7cb211e5c53d118cac076de`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6457c9d5cb93d7645f227282b7cd5c54fdfbe843e587de67969dd5beb7ad93`  
		Last Modified: Fri, 05 Jul 2024 21:14:50 GMT  
		Size: 23.1 MB (23117144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69799820628b45d45a6b4bd29d1e8fff4808119f3dade1703e3f5a01d901923`  
		Last Modified: Fri, 05 Jul 2024 23:42:16 GMT  
		Size: 660.2 MB (660173397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:c4d14ec735e30d45167679ede10b2c8bb8e8d9fc3f8abef855e2ccdbda10b9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57998805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eb34605da1df7939e9b3ce404fdcbf7b0d68fefbc1450a68316814a78a1c58`

```dockerfile
```

-	Layers:
	-	`sha256:96d16b69f5c7b95d63887fb880043916aecbfafe108052815d1363a14151963f`  
		Last Modified: Fri, 05 Jul 2024 23:42:05 GMT  
		Size: 58.0 MB (57988803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb26277d9dbc3b03e36ab4f713b6c90ac577dee24f8480666427609ef50c89ae`  
		Last Modified: Fri, 05 Jul 2024 23:42:03 GMT  
		Size: 10.0 KB (10002 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:f23afa26ab4b34e0e5827f905d5b8e4494c5a5d58b1b015607194cf02d9bb221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:379242c95e2fc0df3ff873e7dc4cb8f3897aa799c34c4f898da31e870d9aebbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267704187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60f697ea9cc5a8853a2279d11acebefd2130b382f4a00a29042021cfacc84e9`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2260612a62c0f31d79217253414a964d458d6efc8c2ae28310775a846b4ef7eb`  
		Last Modified: Sat, 17 Aug 2024 04:07:53 GMT  
		Size: 85.0 MB (84960622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51aaf12e1c08fc8b05c2a5161e1c731ea21e84b9187e3219da32145e6cc48c`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 314.3 KB (314269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec4e939c6ec59149c2a1e62f11968df4a13e465b5699fb2dd8fda1a83bee66`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f534547dafd375b4973e1d2f4be09308403de4de6fd383f5b695ed106417f92`  
		Last Modified: Sat, 17 Aug 2024 04:07:52 GMT  
		Size: 23.7 MB (23733896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b6287828e4497dec4d781c2674ba9e55f149423ae252f89c62bb84b1706d19a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23694026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075206c2478e07f068d4501dbe416605a5c9910f3d68a5f8c4f7095de507a623`

```dockerfile
```

-	Layers:
	-	`sha256:9c8044a86c7e1b23b681096d75a5090eca18d054c46acf0ba095dc28e8c7262d`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 23.7 MB (23676936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2e2da58e9c10f8f9463fdd00b53f5cc33acab8e115a3d6583dc25f70163896`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 17.1 KB (17090 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:56c0d7d90a4b206c1b726b56aa535ea9adea99e187ab26646ae0c3ccc0aa8c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260022791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1281b31359c8bc875f81187fad1e6c9c72ad37fa7bbd36a883fc396c619cdc8`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a65151261e16b95c42cc0f2d0cdb917819146f037a242ecf1ee7b8de2b2ddd`  
		Last Modified: Fri, 05 Jul 2024 20:43:47 GMT  
		Size: 121.8 MB (121776520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c984738d175b26d50ed03560182815a089083eb2a11aa0ab2517627701d45`  
		Last Modified: Fri, 05 Jul 2024 20:43:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d69fd9744647d964d1e8f768f77146a429bc8e68f4b23999fbbfd75418d45`  
		Last Modified: Fri, 05 Jul 2024 21:14:51 GMT  
		Size: 82.6 MB (82644201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d035d7dde10215aba73591f6b955de11b855ddc4ee8e03c29f299a28eb56712b`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 309.1 KB (309119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94d3e4e9957aecb6ab51a45401c5b1743891d5b7cb211e5c53d118cac076de`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6457c9d5cb93d7645f227282b7cd5c54fdfbe843e587de67969dd5beb7ad93`  
		Last Modified: Fri, 05 Jul 2024 21:14:50 GMT  
		Size: 23.1 MB (23117144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:60f667f1fcfd77dd7d02dbeca3198c7c80fd5c02bd866fb1a26c648cf9fe423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23574381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc3252b6ebf92da99d0df6f2af925f6dcfdbedf86bcd9943d32b1942ec7890b`

```dockerfile
```

-	Layers:
	-	`sha256:d11eb8493b25cf6a9a804c33cc3d5b0ff6f97eca723cbd7f0023faa2d34771e6`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 23.6 MB (23556918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7545fe198f2772c095cdf780b2a0538ad4402b8e27fa23dafb6ba1034eb20164`  
		Last Modified: Fri, 05 Jul 2024 21:14:48 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:f23afa26ab4b34e0e5827f905d5b8e4494c5a5d58b1b015607194cf02d9bb221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:379242c95e2fc0df3ff873e7dc4cb8f3897aa799c34c4f898da31e870d9aebbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267704187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60f697ea9cc5a8853a2279d11acebefd2130b382f4a00a29042021cfacc84e9`
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
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2260612a62c0f31d79217253414a964d458d6efc8c2ae28310775a846b4ef7eb`  
		Last Modified: Sat, 17 Aug 2024 04:07:53 GMT  
		Size: 85.0 MB (84960622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51aaf12e1c08fc8b05c2a5161e1c731ea21e84b9187e3219da32145e6cc48c`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 314.3 KB (314269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec4e939c6ec59149c2a1e62f11968df4a13e465b5699fb2dd8fda1a83bee66`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f534547dafd375b4973e1d2f4be09308403de4de6fd383f5b695ed106417f92`  
		Last Modified: Sat, 17 Aug 2024 04:07:52 GMT  
		Size: 23.7 MB (23733896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:b6287828e4497dec4d781c2674ba9e55f149423ae252f89c62bb84b1706d19a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23694026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075206c2478e07f068d4501dbe416605a5c9910f3d68a5f8c4f7095de507a623`

```dockerfile
```

-	Layers:
	-	`sha256:9c8044a86c7e1b23b681096d75a5090eca18d054c46acf0ba095dc28e8c7262d`  
		Last Modified: Sat, 17 Aug 2024 04:07:51 GMT  
		Size: 23.7 MB (23676936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2e2da58e9c10f8f9463fdd00b53f5cc33acab8e115a3d6583dc25f70163896`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 17.1 KB (17090 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:56c0d7d90a4b206c1b726b56aa535ea9adea99e187ab26646ae0c3ccc0aa8c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260022791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1281b31359c8bc875f81187fad1e6c9c72ad37fa7bbd36a883fc396c619cdc8`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a65151261e16b95c42cc0f2d0cdb917819146f037a242ecf1ee7b8de2b2ddd`  
		Last Modified: Fri, 05 Jul 2024 20:43:47 GMT  
		Size: 121.8 MB (121776520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c984738d175b26d50ed03560182815a089083eb2a11aa0ab2517627701d45`  
		Last Modified: Fri, 05 Jul 2024 20:43:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4d69fd9744647d964d1e8f768f77146a429bc8e68f4b23999fbbfd75418d45`  
		Last Modified: Fri, 05 Jul 2024 21:14:51 GMT  
		Size: 82.6 MB (82644201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d035d7dde10215aba73591f6b955de11b855ddc4ee8e03c29f299a28eb56712b`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 309.1 KB (309119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94d3e4e9957aecb6ab51a45401c5b1743891d5b7cb211e5c53d118cac076de`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6457c9d5cb93d7645f227282b7cd5c54fdfbe843e587de67969dd5beb7ad93`  
		Last Modified: Fri, 05 Jul 2024 21:14:50 GMT  
		Size: 23.1 MB (23117144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:60f667f1fcfd77dd7d02dbeca3198c7c80fd5c02bd866fb1a26c648cf9fe423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23574381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc3252b6ebf92da99d0df6f2af925f6dcfdbedf86bcd9943d32b1942ec7890b`

```dockerfile
```

-	Layers:
	-	`sha256:d11eb8493b25cf6a9a804c33cc3d5b0ff6f97eca723cbd7f0023faa2d34771e6`  
		Last Modified: Fri, 05 Jul 2024 21:14:49 GMT  
		Size: 23.6 MB (23556918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7545fe198f2772c095cdf780b2a0538ad4402b8e27fa23dafb6ba1034eb20164`  
		Last Modified: Fri, 05 Jul 2024 21:14:48 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:e75d0bfe7d4934999a4a582610be6ed701c0f69912a98284b80dd610648404cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:470d9cb0115a78161cf824b85def04262001805b1f1ab14cbd07c98add0265c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158692960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d412b4cd555d24cfaf001e89d7bc509a6fe98bb746032b5917643d6b83d57b2e`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:8609607003c4720b939439f0209ed05d438fe75a5c2afcff6b1eab79ff3768d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19211837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c3482e8e194737cd6c66c9b846bcfb90aa4fb3efd56de2f5c62b45d018facb`

```dockerfile
```

-	Layers:
	-	`sha256:d0f934708a3c5d7e68b80422d6e274eac590040328b9e7a7951000fcf25d3750`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 19.2 MB (19195726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fa8d79013f66228924ccad02e4de97aa149603d40ed342071140c5b5b7d885`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 16.1 KB (16111 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e3c9c655dfa5fe67c443b2b9bc898ca17572c114d975ceb52478763aff5390f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153953043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63de991a6081d6db0101c69447d299642c2825a561a1b313d3e993ede978ec09`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c92e67449590912b6c7755a150613269346b5015b668c99f2db49450f6a8e8`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 1.2 MB (1215007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2693553852f919b16b21546e1d8543a7ad744597e5f6749446017c3790d7277`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 3.6 MB (3595960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9fe7ebd0a06ee011e10d604fd769d9ff4552a42b94b0887d4e53098983bf75`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074b02edbde483a99adecce394a1c8fe6ec4582c39bad3ac5050bd5c6a5466b`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e846c275a2224773f856f9b21a28de97bec6dda077693b87dcaf52e96edc19`  
		Last Modified: Sat, 17 Aug 2024 03:58:43 GMT  
		Size: 121.8 MB (121780925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e2c8c4e647f8d82c8763714a4bf637af13f75885d5e363efcc3f2ebbbe7110`  
		Last Modified: Sat, 17 Aug 2024 03:58:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:4fe707dd726357ddbdc46b1023f135fe554d60fc4a5dce9ff78b3fc260c7b65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19205085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a00482bb5ad8bbadda3a59d5a72874b7f87a49be5239ab356a6bb8a36479e9`

```dockerfile
```

-	Layers:
	-	`sha256:7b66fc3c414de97be9ad42abcd13788ddd0085366cdd287649f0b8ea3304684b`  
		Last Modified: Sat, 17 Aug 2024 03:58:40 GMT  
		Size: 19.2 MB (19188698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc5609376d2b00a93b2c4db1f9fedc8d4c5481f972014da720aadf5396e7089`  
		Last Modified: Sat, 17 Aug 2024 03:58:39 GMT  
		Size: 16.4 KB (16387 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:e75d0bfe7d4934999a4a582610be6ed701c0f69912a98284b80dd610648404cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:470d9cb0115a78161cf824b85def04262001805b1f1ab14cbd07c98add0265c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158692960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d412b4cd555d24cfaf001e89d7bc509a6fe98bb746032b5917643d6b83d57b2e`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d9e61041779561e8759e9b21520f25e447f1a92ed30c195eb219a07f13ee4`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 1.2 MB (1214749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31984db62cfd1b1dbaba161f2733682243c8c5b4c2468e1daad6254d6013c16`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 3.6 MB (3624656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3578056fdf017095daa4ed44984c20af93d35cedad7516380faadbfcb2c02ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f257981bf051d771ad6b6b8e5bccdb072de3596ae862d0c6932d215b058156f`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2e74ab88c99fb650a0fa0e3dc35ec4dc6d4b17255b75655f4b3db20343e5b3`  
		Last Modified: Sat, 17 Aug 2024 02:02:52 GMT  
		Size: 124.3 MB (124315063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1afb286b7e642399f63285d7292e7f3c8d429fae9fc0bdf8161f0490c6fbc3`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:8609607003c4720b939439f0209ed05d438fe75a5c2afcff6b1eab79ff3768d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19211837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c3482e8e194737cd6c66c9b846bcfb90aa4fb3efd56de2f5c62b45d018facb`

```dockerfile
```

-	Layers:
	-	`sha256:d0f934708a3c5d7e68b80422d6e274eac590040328b9e7a7951000fcf25d3750`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 19.2 MB (19195726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fa8d79013f66228924ccad02e4de97aa149603d40ed342071140c5b5b7d885`  
		Last Modified: Sat, 17 Aug 2024 02:02:50 GMT  
		Size: 16.1 KB (16111 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e3c9c655dfa5fe67c443b2b9bc898ca17572c114d975ceb52478763aff5390f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153953043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63de991a6081d6db0101c69447d299642c2825a561a1b313d3e993ede978ec09`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c92e67449590912b6c7755a150613269346b5015b668c99f2db49450f6a8e8`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 1.2 MB (1215007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2693553852f919b16b21546e1d8543a7ad744597e5f6749446017c3790d7277`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 3.6 MB (3595960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9fe7ebd0a06ee011e10d604fd769d9ff4552a42b94b0887d4e53098983bf75`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074b02edbde483a99adecce394a1c8fe6ec4582c39bad3ac5050bd5c6a5466b`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e846c275a2224773f856f9b21a28de97bec6dda077693b87dcaf52e96edc19`  
		Last Modified: Sat, 17 Aug 2024 03:58:43 GMT  
		Size: 121.8 MB (121780925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e2c8c4e647f8d82c8763714a4bf637af13f75885d5e363efcc3f2ebbbe7110`  
		Last Modified: Sat, 17 Aug 2024 03:58:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4fe707dd726357ddbdc46b1023f135fe554d60fc4a5dce9ff78b3fc260c7b65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19205085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a00482bb5ad8bbadda3a59d5a72874b7f87a49be5239ab356a6bb8a36479e9`

```dockerfile
```

-	Layers:
	-	`sha256:7b66fc3c414de97be9ad42abcd13788ddd0085366cdd287649f0b8ea3304684b`  
		Last Modified: Sat, 17 Aug 2024 03:58:40 GMT  
		Size: 19.2 MB (19188698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc5609376d2b00a93b2c4db1f9fedc8d4c5481f972014da720aadf5396e7089`  
		Last Modified: Sat, 17 Aug 2024 03:58:39 GMT  
		Size: 16.4 KB (16387 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:f0d54d3443969ef7ad54ad57ffbbe8ef5cc672966df9f9fb7f79b9cd7795d71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:a01e85fc9fc80b97b3b79662bd8e82da91b4b1d6fb21bb864da9893a0b74dd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298424609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef05b2818b0ddf0cce170be6e375db0fc00eed69573bf442411ef761d1afb977`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231ab47c15a27b3ce71add215647fa446f7c20c201669fcc618384dd6d359f`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 114.1 MB (114108371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2ddbfff71328815b9d462dc8736b0b948827a0fe49d01ad659e492fab0d824`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 328.5 KB (328524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba5e4c7da887eff6854454625bdb4da2c0747b9a9ec347d090469b6f6b92689`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b1803d5e9a059d8305e0a234086c642f09dc8f07bcf7f2107957f9fe4190bc`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 27.5 MB (27526250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:187ad7fc4bbae3238c55507a686dc780d772a42596cba0414152bb3c4e92df69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23820052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca58dcbb72adcaff253bc957fc95c5431a04acb6fa50f15e9119502907a4df06`

```dockerfile
```

-	Layers:
	-	`sha256:93728604ffc5d564572f8e9b2ad328eebabb53047b103f20c02a0c8b8d05c3bd`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 23.8 MB (23802657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d464e1429494666e0da53900840e5f5840b18dd81714c21453ab283ac772f53a`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7a251672fbbc1277eb289df339bb27fe7ca4f798e7f2119b71d97de6a2e034b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288299376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c737b1155a82074e783a6f09fb2215e2c1ff07a8f6284afef2c0b49684ba6a6`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bcc4261342272a0b424b2401e4e9c1ea3ea48e2a0be3cb37d3d60ce914fda`  
		Last Modified: Fri, 05 Jul 2024 20:47:53 GMT  
		Size: 117.3 MB (117265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64869f6a58555ee8828021c2ebca140ab2ebc780b737e8bcf35b2779cba239`  
		Last Modified: Fri, 05 Jul 2024 20:47:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04377fa51164b0ddeff26326acbec8bcf286902f25984a00ad5b9770309eaa5c`  
		Last Modified: Fri, 05 Jul 2024 21:19:13 GMT  
		Size: 111.0 MB (110952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de20866bb5b0e8c5cd02eb7bdafdbf97e9d2c76e843c86834718b03e927523a7`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 320.7 KB (320662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b3fd79a1b761f8269b08686ff60c0d760bed1b9e7081c0572fbc0314c0d8`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ee15bddfe47248908eaa975ae8811c53faa743b28e8556d61b5a7bf116436`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 26.7 MB (26671682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:39ac5e9060d354fa80829c10da8de61a6cfd87379856a53c054dee96512202d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23710522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bb14036d6a0a74d72276b78af280df67a814c037e0d7ac25bf2054933a8502`

```dockerfile
```

-	Layers:
	-	`sha256:5badc1c185e3056fb4eeaf474a3c97fbc9d6b2d56e18e317c6501f8d7a457397`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 23.7 MB (23692742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1639a8d3bd02ca4eff0ae0411fb33de4967f288aa6ad090f2e5a2e743468bc15`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:b033b43f1b8f568f1aecf2f1a6491358487e3aa72def88bea5e411520d67e757
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:9721a557af20ca112f87b3f4f4f2c90d185c8b124ce14919da6ade8893aa6365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.3 MB (622307110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62e02d29aa74c5427677f8c369119c9a35ea7ac3b1cb6681a94e7cf365a3444`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231ab47c15a27b3ce71add215647fa446f7c20c201669fcc618384dd6d359f`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 114.1 MB (114108371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2ddbfff71328815b9d462dc8736b0b948827a0fe49d01ad659e492fab0d824`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 328.5 KB (328524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba5e4c7da887eff6854454625bdb4da2c0747b9a9ec347d090469b6f6b92689`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b1803d5e9a059d8305e0a234086c642f09dc8f07bcf7f2107957f9fe4190bc`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 27.5 MB (27526250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c66a41979b8169ee20d35dbcff1aeaf0501bf4ed5470b9b381cfcb0fd4dc936`  
		Last Modified: Sat, 17 Aug 2024 05:01:02 GMT  
		Size: 323.9 MB (323882501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:070a4a87ea16ad69f88f56641333bbf78fd659711d25027a5216955b7d49b4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42087818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3112ecae3386112a7ceb210652c2afc032260796e595f81c45a31bb1e27fc6`

```dockerfile
```

-	Layers:
	-	`sha256:693b12a1d382eb76cb7deafc15cf40868d14845be164c4f9bc1f0847a0477068`  
		Last Modified: Sat, 17 Aug 2024 05:00:57 GMT  
		Size: 42.1 MB (42078164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235fb0f78ea7c34accf9303c933f15d8ceda456f5f94467e1f7dd4ecd9f0346f`  
		Last Modified: Sat, 17 Aug 2024 05:00:57 GMT  
		Size: 9.7 KB (9654 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:64e6ec792eff7c3d11f24baf60fb0eba99c3a7f093a70b8ea40bb35301cd1c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.3 MB (565254776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccff6588f7c05f70d285128536b8912d546e14653184acae07d04443318b33d9`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bcc4261342272a0b424b2401e4e9c1ea3ea48e2a0be3cb37d3d60ce914fda`  
		Last Modified: Fri, 05 Jul 2024 20:47:53 GMT  
		Size: 117.3 MB (117265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64869f6a58555ee8828021c2ebca140ab2ebc780b737e8bcf35b2779cba239`  
		Last Modified: Fri, 05 Jul 2024 20:47:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04377fa51164b0ddeff26326acbec8bcf286902f25984a00ad5b9770309eaa5c`  
		Last Modified: Fri, 05 Jul 2024 21:19:13 GMT  
		Size: 111.0 MB (110952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de20866bb5b0e8c5cd02eb7bdafdbf97e9d2c76e843c86834718b03e927523a7`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 320.7 KB (320662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b3fd79a1b761f8269b08686ff60c0d760bed1b9e7081c0572fbc0314c0d8`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ee15bddfe47248908eaa975ae8811c53faa743b28e8556d61b5a7bf116436`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 26.7 MB (26671682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f292cc5e2c1d0ccbfad936c8fff806ac8f3c83d0f44fe829959695f7c85aa114`  
		Last Modified: Fri, 05 Jul 2024 23:53:01 GMT  
		Size: 277.0 MB (276955400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e405f8232bd606164745daf0a13194b463000d9f73fd49adc7e7bfc53d820977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41863716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2c2b8f2ba753e63be83d21547cf8aa3ceada6608e6b30a6f366d597e6f53e9`

```dockerfile
```

-	Layers:
	-	`sha256:726cc8db93af593d08fdec232f81afc286061c7296a3e4cda432fbf27531f650`  
		Last Modified: Fri, 05 Jul 2024 23:52:56 GMT  
		Size: 41.9 MB (41853701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7caadde2ffb44d7d9da6c08b609e069bf4b6b76a5584d3e68679bb422484c28`  
		Last Modified: Fri, 05 Jul 2024 23:52:54 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:b033b43f1b8f568f1aecf2f1a6491358487e3aa72def88bea5e411520d67e757
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:9721a557af20ca112f87b3f4f4f2c90d185c8b124ce14919da6ade8893aa6365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.3 MB (622307110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62e02d29aa74c5427677f8c369119c9a35ea7ac3b1cb6681a94e7cf365a3444`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231ab47c15a27b3ce71add215647fa446f7c20c201669fcc618384dd6d359f`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 114.1 MB (114108371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2ddbfff71328815b9d462dc8736b0b948827a0fe49d01ad659e492fab0d824`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 328.5 KB (328524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba5e4c7da887eff6854454625bdb4da2c0747b9a9ec347d090469b6f6b92689`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b1803d5e9a059d8305e0a234086c642f09dc8f07bcf7f2107957f9fe4190bc`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 27.5 MB (27526250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c66a41979b8169ee20d35dbcff1aeaf0501bf4ed5470b9b381cfcb0fd4dc936`  
		Last Modified: Sat, 17 Aug 2024 05:01:02 GMT  
		Size: 323.9 MB (323882501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:070a4a87ea16ad69f88f56641333bbf78fd659711d25027a5216955b7d49b4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42087818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3112ecae3386112a7ceb210652c2afc032260796e595f81c45a31bb1e27fc6`

```dockerfile
```

-	Layers:
	-	`sha256:693b12a1d382eb76cb7deafc15cf40868d14845be164c4f9bc1f0847a0477068`  
		Last Modified: Sat, 17 Aug 2024 05:00:57 GMT  
		Size: 42.1 MB (42078164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235fb0f78ea7c34accf9303c933f15d8ceda456f5f94467e1f7dd4ecd9f0346f`  
		Last Modified: Sat, 17 Aug 2024 05:00:57 GMT  
		Size: 9.7 KB (9654 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:64e6ec792eff7c3d11f24baf60fb0eba99c3a7f093a70b8ea40bb35301cd1c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.3 MB (565254776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccff6588f7c05f70d285128536b8912d546e14653184acae07d04443318b33d9`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bcc4261342272a0b424b2401e4e9c1ea3ea48e2a0be3cb37d3d60ce914fda`  
		Last Modified: Fri, 05 Jul 2024 20:47:53 GMT  
		Size: 117.3 MB (117265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64869f6a58555ee8828021c2ebca140ab2ebc780b737e8bcf35b2779cba239`  
		Last Modified: Fri, 05 Jul 2024 20:47:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04377fa51164b0ddeff26326acbec8bcf286902f25984a00ad5b9770309eaa5c`  
		Last Modified: Fri, 05 Jul 2024 21:19:13 GMT  
		Size: 111.0 MB (110952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de20866bb5b0e8c5cd02eb7bdafdbf97e9d2c76e843c86834718b03e927523a7`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 320.7 KB (320662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b3fd79a1b761f8269b08686ff60c0d760bed1b9e7081c0572fbc0314c0d8`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ee15bddfe47248908eaa975ae8811c53faa743b28e8556d61b5a7bf116436`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 26.7 MB (26671682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f292cc5e2c1d0ccbfad936c8fff806ac8f3c83d0f44fe829959695f7c85aa114`  
		Last Modified: Fri, 05 Jul 2024 23:53:01 GMT  
		Size: 277.0 MB (276955400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e405f8232bd606164745daf0a13194b463000d9f73fd49adc7e7bfc53d820977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41863716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2c2b8f2ba753e63be83d21547cf8aa3ceada6608e6b30a6f366d597e6f53e9`

```dockerfile
```

-	Layers:
	-	`sha256:726cc8db93af593d08fdec232f81afc286061c7296a3e4cda432fbf27531f650`  
		Last Modified: Fri, 05 Jul 2024 23:52:56 GMT  
		Size: 41.9 MB (41853701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7caadde2ffb44d7d9da6c08b609e069bf4b6b76a5584d3e68679bb422484c28`  
		Last Modified: Fri, 05 Jul 2024 23:52:54 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:f0d54d3443969ef7ad54ad57ffbbe8ef5cc672966df9f9fb7f79b9cd7795d71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:a01e85fc9fc80b97b3b79662bd8e82da91b4b1d6fb21bb864da9893a0b74dd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298424609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef05b2818b0ddf0cce170be6e375db0fc00eed69573bf442411ef761d1afb977`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231ab47c15a27b3ce71add215647fa446f7c20c201669fcc618384dd6d359f`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 114.1 MB (114108371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2ddbfff71328815b9d462dc8736b0b948827a0fe49d01ad659e492fab0d824`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 328.5 KB (328524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba5e4c7da887eff6854454625bdb4da2c0747b9a9ec347d090469b6f6b92689`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b1803d5e9a059d8305e0a234086c642f09dc8f07bcf7f2107957f9fe4190bc`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 27.5 MB (27526250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:187ad7fc4bbae3238c55507a686dc780d772a42596cba0414152bb3c4e92df69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23820052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca58dcbb72adcaff253bc957fc95c5431a04acb6fa50f15e9119502907a4df06`

```dockerfile
```

-	Layers:
	-	`sha256:93728604ffc5d564572f8e9b2ad328eebabb53047b103f20c02a0c8b8d05c3bd`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 23.8 MB (23802657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d464e1429494666e0da53900840e5f5840b18dd81714c21453ab283ac772f53a`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7a251672fbbc1277eb289df339bb27fe7ca4f798e7f2119b71d97de6a2e034b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288299376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c737b1155a82074e783a6f09fb2215e2c1ff07a8f6284afef2c0b49684ba6a6`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bcc4261342272a0b424b2401e4e9c1ea3ea48e2a0be3cb37d3d60ce914fda`  
		Last Modified: Fri, 05 Jul 2024 20:47:53 GMT  
		Size: 117.3 MB (117265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64869f6a58555ee8828021c2ebca140ab2ebc780b737e8bcf35b2779cba239`  
		Last Modified: Fri, 05 Jul 2024 20:47:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04377fa51164b0ddeff26326acbec8bcf286902f25984a00ad5b9770309eaa5c`  
		Last Modified: Fri, 05 Jul 2024 21:19:13 GMT  
		Size: 111.0 MB (110952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de20866bb5b0e8c5cd02eb7bdafdbf97e9d2c76e843c86834718b03e927523a7`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 320.7 KB (320662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b3fd79a1b761f8269b08686ff60c0d760bed1b9e7081c0572fbc0314c0d8`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ee15bddfe47248908eaa975ae8811c53faa743b28e8556d61b5a7bf116436`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 26.7 MB (26671682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:39ac5e9060d354fa80829c10da8de61a6cfd87379856a53c054dee96512202d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23710522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bb14036d6a0a74d72276b78af280df67a814c037e0d7ac25bf2054933a8502`

```dockerfile
```

-	Layers:
	-	`sha256:5badc1c185e3056fb4eeaf474a3c97fbc9d6b2d56e18e317c6501f8d7a457397`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 23.7 MB (23692742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1639a8d3bd02ca4eff0ae0411fb33de4967f288aa6ad090f2e5a2e743468bc15`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:f0d54d3443969ef7ad54ad57ffbbe8ef5cc672966df9f9fb7f79b9cd7795d71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:a01e85fc9fc80b97b3b79662bd8e82da91b4b1d6fb21bb864da9893a0b74dd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298424609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef05b2818b0ddf0cce170be6e375db0fc00eed69573bf442411ef761d1afb977`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231ab47c15a27b3ce71add215647fa446f7c20c201669fcc618384dd6d359f`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 114.1 MB (114108371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2ddbfff71328815b9d462dc8736b0b948827a0fe49d01ad659e492fab0d824`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 328.5 KB (328524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba5e4c7da887eff6854454625bdb4da2c0747b9a9ec347d090469b6f6b92689`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b1803d5e9a059d8305e0a234086c642f09dc8f07bcf7f2107957f9fe4190bc`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 27.5 MB (27526250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:187ad7fc4bbae3238c55507a686dc780d772a42596cba0414152bb3c4e92df69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23820052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca58dcbb72adcaff253bc957fc95c5431a04acb6fa50f15e9119502907a4df06`

```dockerfile
```

-	Layers:
	-	`sha256:93728604ffc5d564572f8e9b2ad328eebabb53047b103f20c02a0c8b8d05c3bd`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 23.8 MB (23802657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d464e1429494666e0da53900840e5f5840b18dd81714c21453ab283ac772f53a`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7a251672fbbc1277eb289df339bb27fe7ca4f798e7f2119b71d97de6a2e034b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288299376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c737b1155a82074e783a6f09fb2215e2c1ff07a8f6284afef2c0b49684ba6a6`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bcc4261342272a0b424b2401e4e9c1ea3ea48e2a0be3cb37d3d60ce914fda`  
		Last Modified: Fri, 05 Jul 2024 20:47:53 GMT  
		Size: 117.3 MB (117265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64869f6a58555ee8828021c2ebca140ab2ebc780b737e8bcf35b2779cba239`  
		Last Modified: Fri, 05 Jul 2024 20:47:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04377fa51164b0ddeff26326acbec8bcf286902f25984a00ad5b9770309eaa5c`  
		Last Modified: Fri, 05 Jul 2024 21:19:13 GMT  
		Size: 111.0 MB (110952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de20866bb5b0e8c5cd02eb7bdafdbf97e9d2c76e843c86834718b03e927523a7`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 320.7 KB (320662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b3fd79a1b761f8269b08686ff60c0d760bed1b9e7081c0572fbc0314c0d8`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ee15bddfe47248908eaa975ae8811c53faa743b28e8556d61b5a7bf116436`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 26.7 MB (26671682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:39ac5e9060d354fa80829c10da8de61a6cfd87379856a53c054dee96512202d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23710522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bb14036d6a0a74d72276b78af280df67a814c037e0d7ac25bf2054933a8502`

```dockerfile
```

-	Layers:
	-	`sha256:5badc1c185e3056fb4eeaf474a3c97fbc9d6b2d56e18e317c6501f8d7a457397`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 23.7 MB (23692742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1639a8d3bd02ca4eff0ae0411fb33de4967f288aa6ad090f2e5a2e743468bc15`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:b51ed536b813977e896125e9ac2e745a74aca3b10847aff5c45093d7f7d80e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c3a9ceff3edfec9fc63459ea92ef5e473510aad5aea29ade4101ab9c839de792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156459027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f9c9d1f4f96f564799ca35fddfbcbe3a650c406c5d27d232736185e4c8f9ec`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ac901699e0aaf04540d695e22d515b703afdeffb7185199f693ca4034507f87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17797751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bc8dcff98f5eda95a4d3e0e3b7865615c87b41426f13ddd65fa44b197343a0`

```dockerfile
```

-	Layers:
	-	`sha256:f70d61afa5d73ea7219344ff9211919e97e842df31c7eb23972807c6554f035b`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 17.8 MB (17781633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4116a48d0697b3b27bd73b6b1d84237eb64296c95b252b6c972becaeb3ac96b1`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0735fa978d810ce18436f4a2a878b85cde76abe4a25c133f1cdc67e3e8f392c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150426224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce3767c071631aca39aa64a13f562d9d09e697506e77acd8acd49f5ae576fd2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a631a99905201093a192b96d6b9344a759bab04da8001fa7f2bd7df0eb20f436`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 682.9 KB (682877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2beccfb7f73210b53f07f3b786019cbd7b54faebe00e559e8511b67575df29`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 3.6 MB (3557897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fdcea445bfe641533a4e4eb218d30dd044e1fb979c59c9ffb8d6d41c654c4`  
		Last Modified: Sat, 17 Aug 2024 04:01:16 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a42c4dd663c96d6c786e46499dedfb50ea24fb2702a2108d9a94cb3aa990a`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dc6c6c7dbc5ee2a9530e7f4b5388510310ae9b6d6fe273f77997dfbdcfc0ba`  
		Last Modified: Sat, 17 Aug 2024 04:01:21 GMT  
		Size: 117.3 MB (117339297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d6f7979d4b52bb159a593e4dbf4ac389e95d564ab873898d95f3809725b7f9`  
		Last Modified: Sat, 17 Aug 2024 04:01:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fe7c3c0fde4bf693112adb1a1f59d7ff0a5fa412e3ad2a465b7ba5eecea4ce5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17771999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85deaf0e71663b95f37b8243dc4908a2ac1ddecd101b4b96aff4bf1fb7bd11bc`

```dockerfile
```

-	Layers:
	-	`sha256:0789beb0fa5f919d5afc90970cae2304758384dddf29a35472eca1287fe91625`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 17.8 MB (17755604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4f87bbde0cb962454bf36059d1cc000ce210c20d307d631020c81626cd706b`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:b51ed536b813977e896125e9ac2e745a74aca3b10847aff5c45093d7f7d80e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c3a9ceff3edfec9fc63459ea92ef5e473510aad5aea29ade4101ab9c839de792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156459027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f9c9d1f4f96f564799ca35fddfbcbe3a650c406c5d27d232736185e4c8f9ec`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ac901699e0aaf04540d695e22d515b703afdeffb7185199f693ca4034507f87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17797751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bc8dcff98f5eda95a4d3e0e3b7865615c87b41426f13ddd65fa44b197343a0`

```dockerfile
```

-	Layers:
	-	`sha256:f70d61afa5d73ea7219344ff9211919e97e842df31c7eb23972807c6554f035b`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 17.8 MB (17781633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4116a48d0697b3b27bd73b6b1d84237eb64296c95b252b6c972becaeb3ac96b1`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0735fa978d810ce18436f4a2a878b85cde76abe4a25c133f1cdc67e3e8f392c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150426224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce3767c071631aca39aa64a13f562d9d09e697506e77acd8acd49f5ae576fd2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a631a99905201093a192b96d6b9344a759bab04da8001fa7f2bd7df0eb20f436`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 682.9 KB (682877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2beccfb7f73210b53f07f3b786019cbd7b54faebe00e559e8511b67575df29`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 3.6 MB (3557897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fdcea445bfe641533a4e4eb218d30dd044e1fb979c59c9ffb8d6d41c654c4`  
		Last Modified: Sat, 17 Aug 2024 04:01:16 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a42c4dd663c96d6c786e46499dedfb50ea24fb2702a2108d9a94cb3aa990a`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dc6c6c7dbc5ee2a9530e7f4b5388510310ae9b6d6fe273f77997dfbdcfc0ba`  
		Last Modified: Sat, 17 Aug 2024 04:01:21 GMT  
		Size: 117.3 MB (117339297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d6f7979d4b52bb159a593e4dbf4ac389e95d564ab873898d95f3809725b7f9`  
		Last Modified: Sat, 17 Aug 2024 04:01:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fe7c3c0fde4bf693112adb1a1f59d7ff0a5fa412e3ad2a465b7ba5eecea4ce5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17771999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85deaf0e71663b95f37b8243dc4908a2ac1ddecd101b4b96aff4bf1fb7bd11bc`

```dockerfile
```

-	Layers:
	-	`sha256:0789beb0fa5f919d5afc90970cae2304758384dddf29a35472eca1287fe91625`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 17.8 MB (17755604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4f87bbde0cb962454bf36059d1cc000ce210c20d307d631020c81626cd706b`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:f0d54d3443969ef7ad54ad57ffbbe8ef5cc672966df9f9fb7f79b9cd7795d71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:a01e85fc9fc80b97b3b79662bd8e82da91b4b1d6fb21bb864da9893a0b74dd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298424609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef05b2818b0ddf0cce170be6e375db0fc00eed69573bf442411ef761d1afb977`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231ab47c15a27b3ce71add215647fa446f7c20c201669fcc618384dd6d359f`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 114.1 MB (114108371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2ddbfff71328815b9d462dc8736b0b948827a0fe49d01ad659e492fab0d824`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 328.5 KB (328524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba5e4c7da887eff6854454625bdb4da2c0747b9a9ec347d090469b6f6b92689`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b1803d5e9a059d8305e0a234086c642f09dc8f07bcf7f2107957f9fe4190bc`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 27.5 MB (27526250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:187ad7fc4bbae3238c55507a686dc780d772a42596cba0414152bb3c4e92df69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23820052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca58dcbb72adcaff253bc957fc95c5431a04acb6fa50f15e9119502907a4df06`

```dockerfile
```

-	Layers:
	-	`sha256:93728604ffc5d564572f8e9b2ad328eebabb53047b103f20c02a0c8b8d05c3bd`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 23.8 MB (23802657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d464e1429494666e0da53900840e5f5840b18dd81714c21453ab283ac772f53a`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7a251672fbbc1277eb289df339bb27fe7ca4f798e7f2119b71d97de6a2e034b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288299376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c737b1155a82074e783a6f09fb2215e2c1ff07a8f6284afef2c0b49684ba6a6`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bcc4261342272a0b424b2401e4e9c1ea3ea48e2a0be3cb37d3d60ce914fda`  
		Last Modified: Fri, 05 Jul 2024 20:47:53 GMT  
		Size: 117.3 MB (117265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64869f6a58555ee8828021c2ebca140ab2ebc780b737e8bcf35b2779cba239`  
		Last Modified: Fri, 05 Jul 2024 20:47:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04377fa51164b0ddeff26326acbec8bcf286902f25984a00ad5b9770309eaa5c`  
		Last Modified: Fri, 05 Jul 2024 21:19:13 GMT  
		Size: 111.0 MB (110952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de20866bb5b0e8c5cd02eb7bdafdbf97e9d2c76e843c86834718b03e927523a7`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 320.7 KB (320662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b3fd79a1b761f8269b08686ff60c0d760bed1b9e7081c0572fbc0314c0d8`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ee15bddfe47248908eaa975ae8811c53faa743b28e8556d61b5a7bf116436`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 26.7 MB (26671682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:39ac5e9060d354fa80829c10da8de61a6cfd87379856a53c054dee96512202d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23710522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bb14036d6a0a74d72276b78af280df67a814c037e0d7ac25bf2054933a8502`

```dockerfile
```

-	Layers:
	-	`sha256:5badc1c185e3056fb4eeaf474a3c97fbc9d6b2d56e18e317c6501f8d7a457397`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 23.7 MB (23692742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1639a8d3bd02ca4eff0ae0411fb33de4967f288aa6ad090f2e5a2e743468bc15`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic`

```console
$ docker pull ros@sha256:655cf34e42f94aa0111f1d872decf5582d91a9ae2dda90b73b7454bbffa55e2c
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
$ docker pull ros@sha256:c7631b6323509f943142bd494abf268127a6807d81bd75e5f1fec2e0cd2caf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263061226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408a67701899f969b3e60f4a0eb58d35defafadadb7f564aadcd939bac6d28d`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:fc58b4b5b47a9daf00a015010b9c405b2bee15fbcedb748dc03ec81728c088fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27594860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4332305b98df7ac49ef214202dd987420519c390e070c0a75a3ae2192efc6d46`

```dockerfile
```

-	Layers:
	-	`sha256:89609352396b765399d331c17b049a4903d13cc7b7165511bde21d8a061ce2e3`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 27.6 MB (27581208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783f1ac79ac7347d7269a070e63dd8d785bba5a1bf91955cdf05d7a0faac1760`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:16f26c7d44fbd3cf3d9e035ff76de360e992cf6fc7e4254290980286774ed4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0057b00ee435f96c6f5be12c690f3189f8a289111f5b5915f940befb9a00f0fd`
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
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:2df235d55b1f2af746ffc7217df4e45535de5e5073e1f5827e6105ab6b528b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c37f348b239028298251d0b86d1db02d5b50229cf5448fcdec29b57d7514c3`

```dockerfile
```

-	Layers:
	-	`sha256:e2a7dbfd0c788d3bf5679e89cf1b8f0005ab4953a8d6db188b14521177558656`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 27.3 MB (27344563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df22184734123eb54b635454f9e7340cea27496039962e972936a206f75ac5`  
		Last Modified: Sat, 17 Aug 2024 04:37:55 GMT  
		Size: 13.7 KB (13746 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d77f21b335488076a87d9a8f8c28b1ebfddca8c05ce0eaa2c6f87f735200f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250130142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0506c22d8fd8347c0efb1e962f146e28d52cf08b67c437661d6fc00d43acfed1`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:507079eb803a28edee0a748fc0f2a7e01baddd285b3911753794c3afb3ae1dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27461621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafbfbddf500b2700b9b02cc29de87c89b1895a7fb99719ecc8bdd4d2f6c4afb`

```dockerfile
```

-	Layers:
	-	`sha256:ac5c0e52276d8f8cd8be47db7acc0f0710cd263c766060f69001cadb7b50512b`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 27.4 MB (27447597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cd9fffa9b07636cc8d1c1fe41f4200966f27178c82192a8f2946f6e2c636155`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 14.0 KB (14024 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:8e2c27e680a912901bbb02dcd346df95d827f0e2b64acef9299a2798d29c4100
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
$ docker pull ros@sha256:61702b8c76b4f7c24532bf40434dadfbefadacec0e40b3ebb7bdf7eb6da97eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.2 MB (834220729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2880310d2194c8b1b0e07527bfe69673b02d184809d18dc03fc970c36f1ab444`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fa10f85d04d0836d1a7c22d2ad13e46571f44a1f1dfaee1c674ca2f6095cc`  
		Last Modified: Sat, 17 Aug 2024 05:03:22 GMT  
		Size: 571.2 MB (571159503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:a5efc55a26a40f301d96620861c7499e45720b8b857b5ab5444205d5de54b75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51767830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98782f46dc4a047d83771b48af03e37df75da7fceed5ae0148ddb82875a139e1`

```dockerfile
```

-	Layers:
	-	`sha256:f1ef0f1b81e9d98b666a3e3555d994d0ea061ec9d4b8e8654fcfe0c4869c295b`  
		Last Modified: Sat, 17 Aug 2024 05:03:07 GMT  
		Size: 51.8 MB (51758491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b4f292f9ed120d34bc2ebe984fd67d9a0ae996a1d82d6fda4708e46ce631d0`  
		Last Modified: Sat, 17 Aug 2024 05:03:05 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:43c1a1a7aa88b2a90ca5d55361090ebd99bd55eeb6c1419bf629f840ccd48761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.1 MB (725142418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ce214f07aa17e207f4a073ee0cedfa0620db9f3394cf02b10a158c4ef69ef9`
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
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e16c522834ddb11992be720d1f536f974b3e32f7ab85bd13d7c1310ca3f38f`  
		Last Modified: Sat, 17 Aug 2024 05:13:55 GMT  
		Size: 496.9 MB (496869266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:0ec620ced06fd208b24ac804fef70a534967f54ef8402e2f2b44384c690afa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51401685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba7336350a27cca0d27f6574c74e2523ae2132c9e6e1f630cfc861cbdd36e8`

```dockerfile
```

-	Layers:
	-	`sha256:fd8662e1afe75503280ba88308b9b29d52a06f230a7f865238d04fbbb5ddff2c`  
		Last Modified: Sat, 17 Aug 2024 05:13:46 GMT  
		Size: 51.4 MB (51392285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81db02321b3ccf7bdcb5e82623c68586bc3639f3bea788e07ce7c0b49343c0a4`  
		Last Modified: Sat, 17 Aug 2024 05:13:44 GMT  
		Size: 9.4 KB (9400 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:98d0f6e6a7e6f14de8f2caebb884d9996a8b9fb1dd9b5ad2350a5426329ef591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783747495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435bcdc37313e5f4e90b9747e5e41b2d0b2389ff11ca071b84450de68fc8118e`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3098a2393d38456687956fd785ce01b3bbccdb0e65189cd422eae46c064a4fbb`  
		Last Modified: Fri, 05 Jul 2024 23:14:28 GMT  
		Size: 533.6 MB (533617353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1f9dcf6da877ad8c47333f4a64916820d6be2295c8836006df3924997815243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51399293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3873ae954d85747a292bb3ef3490ddefeea63f587f43259940ef0f7ab89bf9b5`

```dockerfile
```

-	Layers:
	-	`sha256:227ded306c207b39796058486140a7eb7f27db310ff3ac784de51468a4678137`  
		Last Modified: Fri, 05 Jul 2024 23:14:18 GMT  
		Size: 51.4 MB (51389592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872855a2a4ff89a530372847623f90a890632155b50dd16c50e888694dea1ac7`  
		Last Modified: Fri, 05 Jul 2024 23:14:17 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:8e2c27e680a912901bbb02dcd346df95d827f0e2b64acef9299a2798d29c4100
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
$ docker pull ros@sha256:61702b8c76b4f7c24532bf40434dadfbefadacec0e40b3ebb7bdf7eb6da97eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.2 MB (834220729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2880310d2194c8b1b0e07527bfe69673b02d184809d18dc03fc970c36f1ab444`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fa10f85d04d0836d1a7c22d2ad13e46571f44a1f1dfaee1c674ca2f6095cc`  
		Last Modified: Sat, 17 Aug 2024 05:03:22 GMT  
		Size: 571.2 MB (571159503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:a5efc55a26a40f301d96620861c7499e45720b8b857b5ab5444205d5de54b75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51767830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98782f46dc4a047d83771b48af03e37df75da7fceed5ae0148ddb82875a139e1`

```dockerfile
```

-	Layers:
	-	`sha256:f1ef0f1b81e9d98b666a3e3555d994d0ea061ec9d4b8e8654fcfe0c4869c295b`  
		Last Modified: Sat, 17 Aug 2024 05:03:07 GMT  
		Size: 51.8 MB (51758491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b4f292f9ed120d34bc2ebe984fd67d9a0ae996a1d82d6fda4708e46ce631d0`  
		Last Modified: Sat, 17 Aug 2024 05:03:05 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:43c1a1a7aa88b2a90ca5d55361090ebd99bd55eeb6c1419bf629f840ccd48761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.1 MB (725142418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ce214f07aa17e207f4a073ee0cedfa0620db9f3394cf02b10a158c4ef69ef9`
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
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e16c522834ddb11992be720d1f536f974b3e32f7ab85bd13d7c1310ca3f38f`  
		Last Modified: Sat, 17 Aug 2024 05:13:55 GMT  
		Size: 496.9 MB (496869266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:0ec620ced06fd208b24ac804fef70a534967f54ef8402e2f2b44384c690afa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51401685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba7336350a27cca0d27f6574c74e2523ae2132c9e6e1f630cfc861cbdd36e8`

```dockerfile
```

-	Layers:
	-	`sha256:fd8662e1afe75503280ba88308b9b29d52a06f230a7f865238d04fbbb5ddff2c`  
		Last Modified: Sat, 17 Aug 2024 05:13:46 GMT  
		Size: 51.4 MB (51392285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81db02321b3ccf7bdcb5e82623c68586bc3639f3bea788e07ce7c0b49343c0a4`  
		Last Modified: Sat, 17 Aug 2024 05:13:44 GMT  
		Size: 9.4 KB (9400 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:98d0f6e6a7e6f14de8f2caebb884d9996a8b9fb1dd9b5ad2350a5426329ef591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783747495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435bcdc37313e5f4e90b9747e5e41b2d0b2389ff11ca071b84450de68fc8118e`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3098a2393d38456687956fd785ce01b3bbccdb0e65189cd422eae46c064a4fbb`  
		Last Modified: Fri, 05 Jul 2024 23:14:28 GMT  
		Size: 533.6 MB (533617353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1f9dcf6da877ad8c47333f4a64916820d6be2295c8836006df3924997815243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51399293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3873ae954d85747a292bb3ef3490ddefeea63f587f43259940ef0f7ab89bf9b5`

```dockerfile
```

-	Layers:
	-	`sha256:227ded306c207b39796058486140a7eb7f27db310ff3ac784de51468a4678137`  
		Last Modified: Fri, 05 Jul 2024 23:14:18 GMT  
		Size: 51.4 MB (51389592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872855a2a4ff89a530372847623f90a890632155b50dd16c50e888694dea1ac7`  
		Last Modified: Fri, 05 Jul 2024 23:14:17 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:82abc56fe9e6f5f6a629ddc92f9971266f1ce0b67e0ddc28473366ffe45b80ca
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
$ docker pull ros@sha256:782576ce68a671148560414243d698c554b71c0d5e5732ab0a67551891b9a2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279987122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120ea3b748974369b4b335f3a908cb17af118979f4f1ca981ed99f2b742aaf93`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfc686f3bacdc6d32f924080fa2c9086e4dca5aa5bc4df5e2a19a22eb0f047a`  
		Last Modified: Sat, 17 Aug 2024 04:59:58 GMT  
		Size: 16.9 MB (16925896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:51e691c6daa27ca0d8ba6418b61c889745b1d70efd2f3c50bad8f6ef083018ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29477831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6566fd87815ad05f4c558b343f712f9debaa99f7251fb048ec8c070c060f7065`

```dockerfile
```

-	Layers:
	-	`sha256:ea6c8db06c8395b285d065c892c95dc7a26b69195eff8fe9fab97f56545fbe5e`  
		Last Modified: Sat, 17 Aug 2024 04:59:58 GMT  
		Size: 29.5 MB (29468540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da35892a20fd08cba2fda679005f3aa7cdff252699fd45fe3042c3907a97129`  
		Last Modified: Sat, 17 Aug 2024 04:59:57 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:7d2352b6140d728f1e573022b42a0cb67f83b7a8bba3286c3625831baa01f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243300002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a83584ed1b81627427c8bdb844db2b2b658b29474bd71073e8b39f40e4b478`
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
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6a18f856b355e0ec84a29e8e96a61a46a967df36166795808e267c55320ad`  
		Last Modified: Sat, 17 Aug 2024 05:00:52 GMT  
		Size: 15.0 MB (15026850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:271ff5877fec192e3772389613e043bae0a6f6e6c525abb56737c71f3646af1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29232681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5901a0ea2f264d312d555165dd539667f0a02236f32058bd527082a058f35c`

```dockerfile
```

-	Layers:
	-	`sha256:324a40922421be6b149c6b5fbb6fca3a145f735321a70d86d237d946952d6201`  
		Last Modified: Sat, 17 Aug 2024 05:00:53 GMT  
		Size: 29.2 MB (29223330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b2b57eec9e4954db17498f45f2c516ff4f112bf1a137edb439b84268a599fb`  
		Last Modified: Sat, 17 Aug 2024 05:00:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:06fca6f0434336d8dfc0d33057db97d435ea23c03b352bdb52bcdd6710b60b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266655279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b24886b33d7cb27dd1a09cf6f31ca46d60a0188b3a23807180ae90ef396024`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80754923381ab4d1d85bfd55edc1a227b1080c0769b278c8e3474b1ee5f3997`  
		Last Modified: Fri, 05 Jul 2024 22:57:54 GMT  
		Size: 16.5 MB (16525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:fe7faa9866202b9d2bea6909da022c1966bd6bd7d836660f172320555782b6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29321551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ad37e1450d9c1ad9adf0135ca00312ad58e5a5b5a518e036370bc717aaeb90`

```dockerfile
```

-	Layers:
	-	`sha256:bb3f1d0ba43b0b8539cdbe0ac8c449e0c897e48ef7d91459d267ad77b8d99586`  
		Last Modified: Fri, 05 Jul 2024 22:57:54 GMT  
		Size: 29.3 MB (29311898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68fa0b9eaf9cc70ea05fbd53c37bc3291aa8cdf135273194c473aca87c44449`  
		Last Modified: Fri, 05 Jul 2024 22:57:53 GMT  
		Size: 9.7 KB (9653 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:82abc56fe9e6f5f6a629ddc92f9971266f1ce0b67e0ddc28473366ffe45b80ca
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
$ docker pull ros@sha256:782576ce68a671148560414243d698c554b71c0d5e5732ab0a67551891b9a2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279987122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120ea3b748974369b4b335f3a908cb17af118979f4f1ca981ed99f2b742aaf93`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfc686f3bacdc6d32f924080fa2c9086e4dca5aa5bc4df5e2a19a22eb0f047a`  
		Last Modified: Sat, 17 Aug 2024 04:59:58 GMT  
		Size: 16.9 MB (16925896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:51e691c6daa27ca0d8ba6418b61c889745b1d70efd2f3c50bad8f6ef083018ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29477831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6566fd87815ad05f4c558b343f712f9debaa99f7251fb048ec8c070c060f7065`

```dockerfile
```

-	Layers:
	-	`sha256:ea6c8db06c8395b285d065c892c95dc7a26b69195eff8fe9fab97f56545fbe5e`  
		Last Modified: Sat, 17 Aug 2024 04:59:58 GMT  
		Size: 29.5 MB (29468540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da35892a20fd08cba2fda679005f3aa7cdff252699fd45fe3042c3907a97129`  
		Last Modified: Sat, 17 Aug 2024 04:59:57 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:7d2352b6140d728f1e573022b42a0cb67f83b7a8bba3286c3625831baa01f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243300002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a83584ed1b81627427c8bdb844db2b2b658b29474bd71073e8b39f40e4b478`
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
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6a18f856b355e0ec84a29e8e96a61a46a967df36166795808e267c55320ad`  
		Last Modified: Sat, 17 Aug 2024 05:00:52 GMT  
		Size: 15.0 MB (15026850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:271ff5877fec192e3772389613e043bae0a6f6e6c525abb56737c71f3646af1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29232681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5901a0ea2f264d312d555165dd539667f0a02236f32058bd527082a058f35c`

```dockerfile
```

-	Layers:
	-	`sha256:324a40922421be6b149c6b5fbb6fca3a145f735321a70d86d237d946952d6201`  
		Last Modified: Sat, 17 Aug 2024 05:00:53 GMT  
		Size: 29.2 MB (29223330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b2b57eec9e4954db17498f45f2c516ff4f112bf1a137edb439b84268a599fb`  
		Last Modified: Sat, 17 Aug 2024 05:00:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:06fca6f0434336d8dfc0d33057db97d435ea23c03b352bdb52bcdd6710b60b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266655279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b24886b33d7cb27dd1a09cf6f31ca46d60a0188b3a23807180ae90ef396024`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80754923381ab4d1d85bfd55edc1a227b1080c0769b278c8e3474b1ee5f3997`  
		Last Modified: Fri, 05 Jul 2024 22:57:54 GMT  
		Size: 16.5 MB (16525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:fe7faa9866202b9d2bea6909da022c1966bd6bd7d836660f172320555782b6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29321551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ad37e1450d9c1ad9adf0135ca00312ad58e5a5b5a518e036370bc717aaeb90`

```dockerfile
```

-	Layers:
	-	`sha256:bb3f1d0ba43b0b8539cdbe0ac8c449e0c897e48ef7d91459d267ad77b8d99586`  
		Last Modified: Fri, 05 Jul 2024 22:57:54 GMT  
		Size: 29.3 MB (29311898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68fa0b9eaf9cc70ea05fbd53c37bc3291aa8cdf135273194c473aca87c44449`  
		Last Modified: Fri, 05 Jul 2024 22:57:53 GMT  
		Size: 9.7 KB (9653 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:655cf34e42f94aa0111f1d872decf5582d91a9ae2dda90b73b7454bbffa55e2c
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
$ docker pull ros@sha256:c7631b6323509f943142bd494abf268127a6807d81bd75e5f1fec2e0cd2caf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263061226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408a67701899f969b3e60f4a0eb58d35defafadadb7f564aadcd939bac6d28d`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fc58b4b5b47a9daf00a015010b9c405b2bee15fbcedb748dc03ec81728c088fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27594860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4332305b98df7ac49ef214202dd987420519c390e070c0a75a3ae2192efc6d46`

```dockerfile
```

-	Layers:
	-	`sha256:89609352396b765399d331c17b049a4903d13cc7b7165511bde21d8a061ce2e3`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 27.6 MB (27581208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783f1ac79ac7347d7269a070e63dd8d785bba5a1bf91955cdf05d7a0faac1760`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:16f26c7d44fbd3cf3d9e035ff76de360e992cf6fc7e4254290980286774ed4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0057b00ee435f96c6f5be12c690f3189f8a289111f5b5915f940befb9a00f0fd`
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
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:2df235d55b1f2af746ffc7217df4e45535de5e5073e1f5827e6105ab6b528b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c37f348b239028298251d0b86d1db02d5b50229cf5448fcdec29b57d7514c3`

```dockerfile
```

-	Layers:
	-	`sha256:e2a7dbfd0c788d3bf5679e89cf1b8f0005ab4953a8d6db188b14521177558656`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 27.3 MB (27344563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df22184734123eb54b635454f9e7340cea27496039962e972936a206f75ac5`  
		Last Modified: Sat, 17 Aug 2024 04:37:55 GMT  
		Size: 13.7 KB (13746 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d77f21b335488076a87d9a8f8c28b1ebfddca8c05ce0eaa2c6f87f735200f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250130142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0506c22d8fd8347c0efb1e962f146e28d52cf08b67c437661d6fc00d43acfed1`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:507079eb803a28edee0a748fc0f2a7e01baddd285b3911753794c3afb3ae1dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27461621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafbfbddf500b2700b9b02cc29de87c89b1895a7fb99719ecc8bdd4d2f6c4afb`

```dockerfile
```

-	Layers:
	-	`sha256:ac5c0e52276d8f8cd8be47db7acc0f0710cd263c766060f69001cadb7b50512b`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 27.4 MB (27447597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cd9fffa9b07636cc8d1c1fe41f4200966f27178c82192a8f2946f6e2c636155`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 14.0 KB (14024 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:655cf34e42f94aa0111f1d872decf5582d91a9ae2dda90b73b7454bbffa55e2c
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
$ docker pull ros@sha256:c7631b6323509f943142bd494abf268127a6807d81bd75e5f1fec2e0cd2caf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263061226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408a67701899f969b3e60f4a0eb58d35defafadadb7f564aadcd939bac6d28d`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:fc58b4b5b47a9daf00a015010b9c405b2bee15fbcedb748dc03ec81728c088fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27594860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4332305b98df7ac49ef214202dd987420519c390e070c0a75a3ae2192efc6d46`

```dockerfile
```

-	Layers:
	-	`sha256:89609352396b765399d331c17b049a4903d13cc7b7165511bde21d8a061ce2e3`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 27.6 MB (27581208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783f1ac79ac7347d7269a070e63dd8d785bba5a1bf91955cdf05d7a0faac1760`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:16f26c7d44fbd3cf3d9e035ff76de360e992cf6fc7e4254290980286774ed4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0057b00ee435f96c6f5be12c690f3189f8a289111f5b5915f940befb9a00f0fd`
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
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:2df235d55b1f2af746ffc7217df4e45535de5e5073e1f5827e6105ab6b528b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c37f348b239028298251d0b86d1db02d5b50229cf5448fcdec29b57d7514c3`

```dockerfile
```

-	Layers:
	-	`sha256:e2a7dbfd0c788d3bf5679e89cf1b8f0005ab4953a8d6db188b14521177558656`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 27.3 MB (27344563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df22184734123eb54b635454f9e7340cea27496039962e972936a206f75ac5`  
		Last Modified: Sat, 17 Aug 2024 04:37:55 GMT  
		Size: 13.7 KB (13746 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d77f21b335488076a87d9a8f8c28b1ebfddca8c05ce0eaa2c6f87f735200f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250130142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0506c22d8fd8347c0efb1e962f146e28d52cf08b67c437661d6fc00d43acfed1`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:507079eb803a28edee0a748fc0f2a7e01baddd285b3911753794c3afb3ae1dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27461621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafbfbddf500b2700b9b02cc29de87c89b1895a7fb99719ecc8bdd4d2f6c4afb`

```dockerfile
```

-	Layers:
	-	`sha256:ac5c0e52276d8f8cd8be47db7acc0f0710cd263c766060f69001cadb7b50512b`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 27.4 MB (27447597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cd9fffa9b07636cc8d1c1fe41f4200966f27178c82192a8f2946f6e2c636155`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 14.0 KB (14024 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:862408ffdd836eb441b3726f158a32f6d4e26f49fbda5c822716d55f43412d5b
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
$ docker pull ros@sha256:e53f9fd13c91747c3515c3a85ec56075ca7a514c7363dd29953d77ac708f8dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211088806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe3ea8df787b305e82b2bd150ac62029c175de520cc4fca5d1490d13d0dfd8f`
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:a4e2fa817226360c08f935434f280eb5a49849f7f4dc958e22c7b7711f2f4210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26121031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbdbe4497382e951d563205769c7e00cdcae3e8f15d3e596005f0867842703e`

```dockerfile
```

-	Layers:
	-	`sha256:d2b59b2b3a4fd0107e0bd00551ec211c29f8bdfe60388c4dcdbc1ed618298383`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 26.1 MB (26104908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d146ee1d613fa1acb9052c4a59df7684f02365809983d3c50230410d30ea24f`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:118b7e318e80c9dd3db19659dff04d5107aeffae11996479a82e754068453b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186803981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7c5d9d36881fa46bfc4649c88bf8f8dee70baa13ba302d2691541912d50788`
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:21a8376f977d52d40e9d2cffeabec7480b581e6ceb642a21b3021472d11d2456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26034665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a411540f87187a5e5e162dc7de95bf53077c7cab2c2f30da58dfe6fdd72ae7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e3adc4cfcbbd695b5327ec7f9d53d37d956a2c3b800c0a9b7ace83695460f42`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 26.0 MB (26018436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea628ace720a446206b95a7fa4e06b7e2993d45b4e449009ad3fb9862346a40`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 16.2 KB (16229 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:743c284f23157c9b9e31d8c0bc92b6d4904a4c7ddcbf41bd57a18d090b97e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203920434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7c68ab0f0ecb313bd8476adbbe7e0c0cfecf5121d5b77285634f1ed2c73aab`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:5cef2541aa51813d10e953f0912d6c9ec4d28cb577d39ce2a429d0d4cae1e5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26043384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61bf9369c405e592cb2e925f090da05fab2f7a50ada788ede74c4467a12c5e1`

```dockerfile
```

-	Layers:
	-	`sha256:366c9d783c5112c0dd3d6cb62743e0899d4ebd6f826464098f3084ef8fd5a811`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 26.0 MB (26026984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea59315c8c8a4a4b588dce50f045ac53a273b4c0f28923941f667eae1dbf9f4`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:862408ffdd836eb441b3726f158a32f6d4e26f49fbda5c822716d55f43412d5b
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
$ docker pull ros@sha256:e53f9fd13c91747c3515c3a85ec56075ca7a514c7363dd29953d77ac708f8dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211088806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe3ea8df787b305e82b2bd150ac62029c175de520cc4fca5d1490d13d0dfd8f`
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:a4e2fa817226360c08f935434f280eb5a49849f7f4dc958e22c7b7711f2f4210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26121031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbdbe4497382e951d563205769c7e00cdcae3e8f15d3e596005f0867842703e`

```dockerfile
```

-	Layers:
	-	`sha256:d2b59b2b3a4fd0107e0bd00551ec211c29f8bdfe60388c4dcdbc1ed618298383`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 26.1 MB (26104908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d146ee1d613fa1acb9052c4a59df7684f02365809983d3c50230410d30ea24f`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:118b7e318e80c9dd3db19659dff04d5107aeffae11996479a82e754068453b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186803981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7c5d9d36881fa46bfc4649c88bf8f8dee70baa13ba302d2691541912d50788`
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
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:21a8376f977d52d40e9d2cffeabec7480b581e6ceb642a21b3021472d11d2456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26034665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a411540f87187a5e5e162dc7de95bf53077c7cab2c2f30da58dfe6fdd72ae7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e3adc4cfcbbd695b5327ec7f9d53d37d956a2c3b800c0a9b7ace83695460f42`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 26.0 MB (26018436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea628ace720a446206b95a7fa4e06b7e2993d45b4e449009ad3fb9862346a40`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 16.2 KB (16229 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:743c284f23157c9b9e31d8c0bc92b6d4904a4c7ddcbf41bd57a18d090b97e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203920434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7c68ab0f0ecb313bd8476adbbe7e0c0cfecf5121d5b77285634f1ed2c73aab`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:5cef2541aa51813d10e953f0912d6c9ec4d28cb577d39ce2a429d0d4cae1e5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26043384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61bf9369c405e592cb2e925f090da05fab2f7a50ada788ede74c4467a12c5e1`

```dockerfile
```

-	Layers:
	-	`sha256:366c9d783c5112c0dd3d6cb62743e0899d4ebd6f826464098f3084ef8fd5a811`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 26.0 MB (26026984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea59315c8c8a4a4b588dce50f045ac53a273b4c0f28923941f667eae1dbf9f4`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:7f4ca5ceffb6b1fc9ef40a775cc73b7fb86428aac2c9643f4e524b1905c6c702
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:594cba7093a34ae4c3dcfc4c92f9cae3482a340b5862ad1ec7e8efc5a98f2877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298412289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f875aa41a6f0bb901afb4b04401d77494a8cf2f766ccb3c7ee14c62374825055`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
```

-	Layers:
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03f050a79216294d81d03356aabd6e4abd4924598128d7ea323b9128cc0565`  
		Last Modified: Sat, 17 Aug 2024 04:08:04 GMT  
		Size: 114.1 MB (114108736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e926b2d3bf9abb3fd0e15a5257b583a67cae7c52b9a696426506667837e26bc`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 320.9 KB (320920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f60140c3504caeb6f476b0852b3390c32695e11cdf799985c4253fde45ee5cd`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645072ffb7af51c31166b7ab9edc25ad864b066dbeaf65d8af3bea0d414ebcca`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 27.5 MB (27522529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:059c1ae31ad97fa76a05ab9b31dacfa6b20aba6aa7acf794856ef7780209e331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23845572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c660aab28280c69329ab186d67edffbac0ca48b4d3e1ac16e4131cfdfcd051`

```dockerfile
```

-	Layers:
	-	`sha256:8a27cd29d74c2296921f3e278f7c6c176fad2d69ad912d0aea38a6561ef15ab7`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 23.8 MB (23828433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af852a1c69e2e47506fdfcd1644355e2468a37f02bc272e7a5780a5380df5af1`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7ee6eac5949c9b2592dd617ddf2c9b022b6bfda5f08c03e78171b68e654cf9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288213186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7026da9762ceea4004c7437eb1dd77690415bc5988f34adceaecc9594a851ad`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31c2175f6e9ecbe2c063179e8a46328b43cf72c74eab1ed37301f4e2c34620`  
		Last Modified: Fri, 05 Jul 2024 20:49:21 GMT  
		Size: 117.3 MB (117260265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8d191f93979eb95d46e111543c38c9a5e230be59354a67b050df7dee576514`  
		Last Modified: Fri, 05 Jul 2024 20:49:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0e211c2d874c04c82212c51e030d4d0b957ffdf0731f88f14395ce31aebfa6`  
		Last Modified: Fri, 05 Jul 2024 21:20:38 GMT  
		Size: 111.0 MB (110952482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed28c146690a6b6d0c23e6039516c8a68652b2114c3e7fa132676858c0ea707`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 315.6 KB (315622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65e0e5567bd2dddc8c8313e29ed4dc953966eb0eae751c0c6fdf882562e2fb`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f7c3b40f4c3fa7abe72c030795ccfd8da56d2ce93c1b680b820a0a2c8fc52`  
		Last Modified: Fri, 05 Jul 2024 21:20:37 GMT  
		Size: 26.6 MB (26596158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:fd41f5940abfe5c79e8537024a1b44801397d6416369cede2733c6462b08c39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23738118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fca134fc488ba65d75a89c89d3c65b9ffee3095416c19448aada44d0006359`

```dockerfile
```

-	Layers:
	-	`sha256:980a1d65c0937845d129a0cdc2d2e662f07e53c551c9729ef5026346021a31c4`  
		Last Modified: Fri, 05 Jul 2024 21:20:36 GMT  
		Size: 23.7 MB (23720609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda26cf028227970aeb6fffb2e374eeaf951988369858494b6ec590824a642b5`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:a76f32445d492945f71a4528f44b4d827c4155bd79164516136d598056168f13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:3f2d37055468da6c7188e60edcf3df6ac45b70b47b7de0bf2141f5c4c50e965c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.3 MB (622316797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a1749f83183cf95a2907270f4bcbd0d4b9bcd8b01e2e4a21cd3cc3410d2b51`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03f050a79216294d81d03356aabd6e4abd4924598128d7ea323b9128cc0565`  
		Last Modified: Sat, 17 Aug 2024 04:08:04 GMT  
		Size: 114.1 MB (114108736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e926b2d3bf9abb3fd0e15a5257b583a67cae7c52b9a696426506667837e26bc`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 320.9 KB (320920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f60140c3504caeb6f476b0852b3390c32695e11cdf799985c4253fde45ee5cd`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645072ffb7af51c31166b7ab9edc25ad864b066dbeaf65d8af3bea0d414ebcca`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 27.5 MB (27522529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78361a8dc26dcdd27a5dca24a2261ab5dbd5e3c39df6f3f3a7743d452177b9bc`  
		Last Modified: Sat, 17 Aug 2024 05:01:03 GMT  
		Size: 323.9 MB (323904508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:a1be4bc8fc97bba990687ea44be74dd6740f66c4d83a5ffce56e0c2a5c4a799d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42109146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00eb30528ac32db8d4d5bcbdf5794b344e9b0a1cb427f094f3a0a84bdc1f6b7`

```dockerfile
```

-	Layers:
	-	`sha256:72eebd0a522c1d1dfe25ccb9832e49aaa42511c88a42566048b1033fb2c8bd1b`  
		Last Modified: Sat, 17 Aug 2024 05:00:59 GMT  
		Size: 42.1 MB (42099471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09e4cbd90c1eddd317271b910b71e214019b21342ec050ad25513662e425e53`  
		Last Modified: Sat, 17 Aug 2024 05:00:58 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5adfcf0be037e0486ea8ace6b21f1f2b7d690d028051922c6429cc57b299f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.2 MB (565173371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aba5062482007d0ca60675410a5ae0106c3c58c0245a2c99ae1b47a7da70fb`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31c2175f6e9ecbe2c063179e8a46328b43cf72c74eab1ed37301f4e2c34620`  
		Last Modified: Fri, 05 Jul 2024 20:49:21 GMT  
		Size: 117.3 MB (117260265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8d191f93979eb95d46e111543c38c9a5e230be59354a67b050df7dee576514`  
		Last Modified: Fri, 05 Jul 2024 20:49:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0e211c2d874c04c82212c51e030d4d0b957ffdf0731f88f14395ce31aebfa6`  
		Last Modified: Fri, 05 Jul 2024 21:20:38 GMT  
		Size: 111.0 MB (110952482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed28c146690a6b6d0c23e6039516c8a68652b2114c3e7fa132676858c0ea707`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 315.6 KB (315622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65e0e5567bd2dddc8c8313e29ed4dc953966eb0eae751c0c6fdf882562e2fb`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f7c3b40f4c3fa7abe72c030795ccfd8da56d2ce93c1b680b820a0a2c8fc52`  
		Last Modified: Fri, 05 Jul 2024 21:20:37 GMT  
		Size: 26.6 MB (26596158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7149c896fc2d09209c22d7d3e4ca3e8d66d022c6312b01ccde812cef4528c7`  
		Last Modified: Sat, 06 Jul 2024 00:08:32 GMT  
		Size: 277.0 MB (276960185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:46794aae958acf1c2ff0276d86c89261e7927b2b15a00a502c7f2080280f70bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41906123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887bae5de03a16d10f2c16c9b20d59a329134a4a4fc1e16a6ccbf97eabe3de0d`

```dockerfile
```

-	Layers:
	-	`sha256:a1c4d5a47d6297e67e7c3ab01a17bb50a9f6b6bfdfd7a425ba5392700121160b`  
		Last Modified: Sat, 06 Jul 2024 00:08:26 GMT  
		Size: 41.9 MB (41896087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b195fe2807ecab22bb053979f9e687c233b5b8cfa7c951b16fb823c0604215`  
		Last Modified: Sat, 06 Jul 2024 00:08:24 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:a76f32445d492945f71a4528f44b4d827c4155bd79164516136d598056168f13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:3f2d37055468da6c7188e60edcf3df6ac45b70b47b7de0bf2141f5c4c50e965c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.3 MB (622316797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a1749f83183cf95a2907270f4bcbd0d4b9bcd8b01e2e4a21cd3cc3410d2b51`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03f050a79216294d81d03356aabd6e4abd4924598128d7ea323b9128cc0565`  
		Last Modified: Sat, 17 Aug 2024 04:08:04 GMT  
		Size: 114.1 MB (114108736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e926b2d3bf9abb3fd0e15a5257b583a67cae7c52b9a696426506667837e26bc`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 320.9 KB (320920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f60140c3504caeb6f476b0852b3390c32695e11cdf799985c4253fde45ee5cd`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645072ffb7af51c31166b7ab9edc25ad864b066dbeaf65d8af3bea0d414ebcca`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 27.5 MB (27522529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78361a8dc26dcdd27a5dca24a2261ab5dbd5e3c39df6f3f3a7743d452177b9bc`  
		Last Modified: Sat, 17 Aug 2024 05:01:03 GMT  
		Size: 323.9 MB (323904508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a1be4bc8fc97bba990687ea44be74dd6740f66c4d83a5ffce56e0c2a5c4a799d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42109146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00eb30528ac32db8d4d5bcbdf5794b344e9b0a1cb427f094f3a0a84bdc1f6b7`

```dockerfile
```

-	Layers:
	-	`sha256:72eebd0a522c1d1dfe25ccb9832e49aaa42511c88a42566048b1033fb2c8bd1b`  
		Last Modified: Sat, 17 Aug 2024 05:00:59 GMT  
		Size: 42.1 MB (42099471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09e4cbd90c1eddd317271b910b71e214019b21342ec050ad25513662e425e53`  
		Last Modified: Sat, 17 Aug 2024 05:00:58 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5adfcf0be037e0486ea8ace6b21f1f2b7d690d028051922c6429cc57b299f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.2 MB (565173371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aba5062482007d0ca60675410a5ae0106c3c58c0245a2c99ae1b47a7da70fb`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31c2175f6e9ecbe2c063179e8a46328b43cf72c74eab1ed37301f4e2c34620`  
		Last Modified: Fri, 05 Jul 2024 20:49:21 GMT  
		Size: 117.3 MB (117260265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8d191f93979eb95d46e111543c38c9a5e230be59354a67b050df7dee576514`  
		Last Modified: Fri, 05 Jul 2024 20:49:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0e211c2d874c04c82212c51e030d4d0b957ffdf0731f88f14395ce31aebfa6`  
		Last Modified: Fri, 05 Jul 2024 21:20:38 GMT  
		Size: 111.0 MB (110952482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed28c146690a6b6d0c23e6039516c8a68652b2114c3e7fa132676858c0ea707`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 315.6 KB (315622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65e0e5567bd2dddc8c8313e29ed4dc953966eb0eae751c0c6fdf882562e2fb`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f7c3b40f4c3fa7abe72c030795ccfd8da56d2ce93c1b680b820a0a2c8fc52`  
		Last Modified: Fri, 05 Jul 2024 21:20:37 GMT  
		Size: 26.6 MB (26596158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7149c896fc2d09209c22d7d3e4ca3e8d66d022c6312b01ccde812cef4528c7`  
		Last Modified: Sat, 06 Jul 2024 00:08:32 GMT  
		Size: 277.0 MB (276960185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:46794aae958acf1c2ff0276d86c89261e7927b2b15a00a502c7f2080280f70bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41906123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887bae5de03a16d10f2c16c9b20d59a329134a4a4fc1e16a6ccbf97eabe3de0d`

```dockerfile
```

-	Layers:
	-	`sha256:a1c4d5a47d6297e67e7c3ab01a17bb50a9f6b6bfdfd7a425ba5392700121160b`  
		Last Modified: Sat, 06 Jul 2024 00:08:26 GMT  
		Size: 41.9 MB (41896087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b195fe2807ecab22bb053979f9e687c233b5b8cfa7c951b16fb823c0604215`  
		Last Modified: Sat, 06 Jul 2024 00:08:24 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:7f4ca5ceffb6b1fc9ef40a775cc73b7fb86428aac2c9643f4e524b1905c6c702
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:594cba7093a34ae4c3dcfc4c92f9cae3482a340b5862ad1ec7e8efc5a98f2877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298412289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f875aa41a6f0bb901afb4b04401d77494a8cf2f766ccb3c7ee14c62374825055`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
```

-	Layers:
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03f050a79216294d81d03356aabd6e4abd4924598128d7ea323b9128cc0565`  
		Last Modified: Sat, 17 Aug 2024 04:08:04 GMT  
		Size: 114.1 MB (114108736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e926b2d3bf9abb3fd0e15a5257b583a67cae7c52b9a696426506667837e26bc`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 320.9 KB (320920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f60140c3504caeb6f476b0852b3390c32695e11cdf799985c4253fde45ee5cd`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645072ffb7af51c31166b7ab9edc25ad864b066dbeaf65d8af3bea0d414ebcca`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 27.5 MB (27522529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:059c1ae31ad97fa76a05ab9b31dacfa6b20aba6aa7acf794856ef7780209e331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23845572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c660aab28280c69329ab186d67edffbac0ca48b4d3e1ac16e4131cfdfcd051`

```dockerfile
```

-	Layers:
	-	`sha256:8a27cd29d74c2296921f3e278f7c6c176fad2d69ad912d0aea38a6561ef15ab7`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 23.8 MB (23828433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af852a1c69e2e47506fdfcd1644355e2468a37f02bc272e7a5780a5380df5af1`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7ee6eac5949c9b2592dd617ddf2c9b022b6bfda5f08c03e78171b68e654cf9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288213186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7026da9762ceea4004c7437eb1dd77690415bc5988f34adceaecc9594a851ad`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31c2175f6e9ecbe2c063179e8a46328b43cf72c74eab1ed37301f4e2c34620`  
		Last Modified: Fri, 05 Jul 2024 20:49:21 GMT  
		Size: 117.3 MB (117260265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8d191f93979eb95d46e111543c38c9a5e230be59354a67b050df7dee576514`  
		Last Modified: Fri, 05 Jul 2024 20:49:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0e211c2d874c04c82212c51e030d4d0b957ffdf0731f88f14395ce31aebfa6`  
		Last Modified: Fri, 05 Jul 2024 21:20:38 GMT  
		Size: 111.0 MB (110952482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed28c146690a6b6d0c23e6039516c8a68652b2114c3e7fa132676858c0ea707`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 315.6 KB (315622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65e0e5567bd2dddc8c8313e29ed4dc953966eb0eae751c0c6fdf882562e2fb`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f7c3b40f4c3fa7abe72c030795ccfd8da56d2ce93c1b680b820a0a2c8fc52`  
		Last Modified: Fri, 05 Jul 2024 21:20:37 GMT  
		Size: 26.6 MB (26596158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fd41f5940abfe5c79e8537024a1b44801397d6416369cede2733c6462b08c39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23738118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fca134fc488ba65d75a89c89d3c65b9ffee3095416c19448aada44d0006359`

```dockerfile
```

-	Layers:
	-	`sha256:980a1d65c0937845d129a0cdc2d2e662f07e53c551c9729ef5026346021a31c4`  
		Last Modified: Fri, 05 Jul 2024 21:20:36 GMT  
		Size: 23.7 MB (23720609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda26cf028227970aeb6fffb2e374eeaf951988369858494b6ec590824a642b5`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:7f4ca5ceffb6b1fc9ef40a775cc73b7fb86428aac2c9643f4e524b1905c6c702
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:594cba7093a34ae4c3dcfc4c92f9cae3482a340b5862ad1ec7e8efc5a98f2877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298412289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f875aa41a6f0bb901afb4b04401d77494a8cf2f766ccb3c7ee14c62374825055`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
```

-	Layers:
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03f050a79216294d81d03356aabd6e4abd4924598128d7ea323b9128cc0565`  
		Last Modified: Sat, 17 Aug 2024 04:08:04 GMT  
		Size: 114.1 MB (114108736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e926b2d3bf9abb3fd0e15a5257b583a67cae7c52b9a696426506667837e26bc`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 320.9 KB (320920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f60140c3504caeb6f476b0852b3390c32695e11cdf799985c4253fde45ee5cd`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645072ffb7af51c31166b7ab9edc25ad864b066dbeaf65d8af3bea0d414ebcca`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 27.5 MB (27522529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:059c1ae31ad97fa76a05ab9b31dacfa6b20aba6aa7acf794856ef7780209e331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23845572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c660aab28280c69329ab186d67edffbac0ca48b4d3e1ac16e4131cfdfcd051`

```dockerfile
```

-	Layers:
	-	`sha256:8a27cd29d74c2296921f3e278f7c6c176fad2d69ad912d0aea38a6561ef15ab7`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 23.8 MB (23828433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af852a1c69e2e47506fdfcd1644355e2468a37f02bc272e7a5780a5380df5af1`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7ee6eac5949c9b2592dd617ddf2c9b022b6bfda5f08c03e78171b68e654cf9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288213186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7026da9762ceea4004c7437eb1dd77690415bc5988f34adceaecc9594a851ad`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31c2175f6e9ecbe2c063179e8a46328b43cf72c74eab1ed37301f4e2c34620`  
		Last Modified: Fri, 05 Jul 2024 20:49:21 GMT  
		Size: 117.3 MB (117260265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8d191f93979eb95d46e111543c38c9a5e230be59354a67b050df7dee576514`  
		Last Modified: Fri, 05 Jul 2024 20:49:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0e211c2d874c04c82212c51e030d4d0b957ffdf0731f88f14395ce31aebfa6`  
		Last Modified: Fri, 05 Jul 2024 21:20:38 GMT  
		Size: 111.0 MB (110952482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed28c146690a6b6d0c23e6039516c8a68652b2114c3e7fa132676858c0ea707`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 315.6 KB (315622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65e0e5567bd2dddc8c8313e29ed4dc953966eb0eae751c0c6fdf882562e2fb`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f7c3b40f4c3fa7abe72c030795ccfd8da56d2ce93c1b680b820a0a2c8fc52`  
		Last Modified: Fri, 05 Jul 2024 21:20:37 GMT  
		Size: 26.6 MB (26596158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fd41f5940abfe5c79e8537024a1b44801397d6416369cede2733c6462b08c39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23738118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fca134fc488ba65d75a89c89d3c65b9ffee3095416c19448aada44d0006359`

```dockerfile
```

-	Layers:
	-	`sha256:980a1d65c0937845d129a0cdc2d2e662f07e53c551c9729ef5026346021a31c4`  
		Last Modified: Fri, 05 Jul 2024 21:20:36 GMT  
		Size: 23.7 MB (23720609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda26cf028227970aeb6fffb2e374eeaf951988369858494b6ec590824a642b5`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:cd4d0bf9a5b81e2e69d111f74def72d5e557f9d39f3ce4b81cffefbc763dde24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:2bab17738a780636dcb86f1433549864332d860c4f0987d59fff48adaf42ca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156457664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debe6fc5c9f6cb22d262dcd9f4da2986e3b8be704562927dc3c67ea158b80338`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f73b267ee4afb2b78b98679d1b7855756112b475c822b5e650f21727d11e560d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17820095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d324cc0cabf32bab15d66468aa5b08b299a01ec3dec2d640552a06cc5a18efa`

```dockerfile
```

-	Layers:
	-	`sha256:e52a2fb7d8cfd575bf794db55a89040a81338f6a08eb02b8ef90888d3edf5907`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 17.8 MB (17803955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71dbb7d25636a8a0ff323ffe399e9bfef01fd3e939d2e8e82d5786e761f24ca5`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0503c3cb0cefff6bb65d10f79eb038b1b787536f9cba635c8f53b893e3b7ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150417831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129853cf267bd1d1d0acb529081fe3dcaa0790b1fe8c3e6d3e8ffc048621ea08`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a631a99905201093a192b96d6b9344a759bab04da8001fa7f2bd7df0eb20f436`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 682.9 KB (682877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2beccfb7f73210b53f07f3b786019cbd7b54faebe00e559e8511b67575df29`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 3.6 MB (3557897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fdcea445bfe641533a4e4eb218d30dd044e1fb979c59c9ffb8d6d41c654c4`  
		Last Modified: Sat, 17 Aug 2024 04:01:16 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a42c4dd663c96d6c786e46499dedfb50ea24fb2702a2108d9a94cb3aa990a`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9c04e2bffc1ed794fb172146ff902e16b2168278b07cf37fa39ebba8e09d`  
		Last Modified: Sat, 17 Aug 2024 04:02:49 GMT  
		Size: 117.3 MB (117330906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97270cb5d2135d6378730d2c10ca4fa7c82d05d3108eaef2bfec60d3b45662d`  
		Last Modified: Sat, 17 Aug 2024 04:02:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:91843b20dfe3b63d355b75840cd693f789183104021cf7378c6a03f9c7c93d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17794343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a913b197ad39612d1fcbf729c123a28b5124825a603684bb2137c57a6f628538`

```dockerfile
```

-	Layers:
	-	`sha256:bd093f7c86abf07bf98fa36b887986c9a16008d2bfec0c6c66c8338abb22cd40`  
		Last Modified: Sat, 17 Aug 2024 04:02:46 GMT  
		Size: 17.8 MB (17777926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2fce5d47d4778c24df9f1d404353d5418bc601672d94807d624899ae0f5ccbc`  
		Last Modified: Sat, 17 Aug 2024 04:02:45 GMT  
		Size: 16.4 KB (16417 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:cd4d0bf9a5b81e2e69d111f74def72d5e557f9d39f3ce4b81cffefbc763dde24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:2bab17738a780636dcb86f1433549864332d860c4f0987d59fff48adaf42ca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156457664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debe6fc5c9f6cb22d262dcd9f4da2986e3b8be704562927dc3c67ea158b80338`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f73b267ee4afb2b78b98679d1b7855756112b475c822b5e650f21727d11e560d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17820095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d324cc0cabf32bab15d66468aa5b08b299a01ec3dec2d640552a06cc5a18efa`

```dockerfile
```

-	Layers:
	-	`sha256:e52a2fb7d8cfd575bf794db55a89040a81338f6a08eb02b8ef90888d3edf5907`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 17.8 MB (17803955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71dbb7d25636a8a0ff323ffe399e9bfef01fd3e939d2e8e82d5786e761f24ca5`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0503c3cb0cefff6bb65d10f79eb038b1b787536f9cba635c8f53b893e3b7ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150417831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129853cf267bd1d1d0acb529081fe3dcaa0790b1fe8c3e6d3e8ffc048621ea08`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a631a99905201093a192b96d6b9344a759bab04da8001fa7f2bd7df0eb20f436`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 682.9 KB (682877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2beccfb7f73210b53f07f3b786019cbd7b54faebe00e559e8511b67575df29`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 3.6 MB (3557897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fdcea445bfe641533a4e4eb218d30dd044e1fb979c59c9ffb8d6d41c654c4`  
		Last Modified: Sat, 17 Aug 2024 04:01:16 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a42c4dd663c96d6c786e46499dedfb50ea24fb2702a2108d9a94cb3aa990a`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9c04e2bffc1ed794fb172146ff902e16b2168278b07cf37fa39ebba8e09d`  
		Last Modified: Sat, 17 Aug 2024 04:02:49 GMT  
		Size: 117.3 MB (117330906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97270cb5d2135d6378730d2c10ca4fa7c82d05d3108eaef2bfec60d3b45662d`  
		Last Modified: Sat, 17 Aug 2024 04:02:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:91843b20dfe3b63d355b75840cd693f789183104021cf7378c6a03f9c7c93d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17794343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a913b197ad39612d1fcbf729c123a28b5124825a603684bb2137c57a6f628538`

```dockerfile
```

-	Layers:
	-	`sha256:bd093f7c86abf07bf98fa36b887986c9a16008d2bfec0c6c66c8338abb22cd40`  
		Last Modified: Sat, 17 Aug 2024 04:02:46 GMT  
		Size: 17.8 MB (17777926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2fce5d47d4778c24df9f1d404353d5418bc601672d94807d624899ae0f5ccbc`  
		Last Modified: Sat, 17 Aug 2024 04:02:45 GMT  
		Size: 16.4 KB (16417 bytes)  
		MIME: application/vnd.in-toto+json
