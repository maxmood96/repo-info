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
$ docker pull ros@sha256:f0300c9cef207d18b33629cabcfe3dc0b23255b7a41a126fe047ed4449494740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:5865a4ea85c1b0e548707f25f5e816fa1a5f2c885c2f2b6db9c418e9a3caa6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263554294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718c0a4486a6aa164b79edaa44c9f165460ffbb0281b7e819cd421445845a0d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:58:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:58:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:58:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 05:59:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a53e9f9de03d6c034c610e08dc70cceccb90d9c98f414880a140ea8da931364`  
		Last Modified: Tue, 16 Apr 2024 06:26:58 GMT  
		Size: 98.1 MB (98144815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32be56bd237bb233aa7f0b0607fe10d70ff1b5d77663f5a63010eb2092a3819f`  
		Last Modified: Tue, 16 Apr 2024 06:26:44 GMT  
		Size: 316.5 KB (316546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282750c3b13e653a477b3c260ec106304999a833a29510dff2fcdedc692080bd`  
		Last Modified: Tue, 16 Apr 2024 06:26:43 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289549d7f60f97bb94619fa3d17f212efe6f81c43b4aaa3b4af8e9b86c7555b`  
		Last Modified: Tue, 16 Apr 2024 06:26:47 GMT  
		Size: 23.1 MB (23101278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:801c95e60a6b8f045975fc2874233834a56cd244777b050aa61a09504151fa94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256171515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed940c284a110dd2cf289e8a68ab71a64a0ce9b24687d3da3e179e2bf401253`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:12:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:12:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:12:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:12:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09ab4678d1ee12b412975a8af36009ee6d3d376a4fdece02890d890896e400b`  
		Last Modified: Tue, 16 Apr 2024 04:30:16 GMT  
		Size: 95.7 MB (95688558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644937a0a1280b2fa65eacfe6512948da1340c7f0defb67b2c9794460b79767`  
		Last Modified: Tue, 16 Apr 2024 04:30:06 GMT  
		Size: 316.5 KB (316541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61648cee52d405e737ad1ba192bbb3bf964c074f4699e4e7c9a994affee263`  
		Last Modified: Tue, 16 Apr 2024 04:30:07 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6a0221c852ee06a60c52341c9d399c4d645c4f9b320ba89399d36d3385d7b`  
		Last Modified: Tue, 16 Apr 2024 04:30:09 GMT  
		Size: 22.5 MB (22520996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:f6758a3f69f9467b4787d796ebdd7f7bc80e48ee8711927abca07b33cefd8031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:1d79a35a22fafc6ffa68872325824a50cadd71a62b9d905ce98e83622b29af6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.1 MB (955055167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267f36f318885eeac089d57766d8256dc0748da93c2f16ab6bedb6c604a83880`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:58:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:58:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:58:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 05:59:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:07:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a53e9f9de03d6c034c610e08dc70cceccb90d9c98f414880a140ea8da931364`  
		Last Modified: Tue, 16 Apr 2024 06:26:58 GMT  
		Size: 98.1 MB (98144815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32be56bd237bb233aa7f0b0607fe10d70ff1b5d77663f5a63010eb2092a3819f`  
		Last Modified: Tue, 16 Apr 2024 06:26:44 GMT  
		Size: 316.5 KB (316546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282750c3b13e653a477b3c260ec106304999a833a29510dff2fcdedc692080bd`  
		Last Modified: Tue, 16 Apr 2024 06:26:43 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289549d7f60f97bb94619fa3d17f212efe6f81c43b4aaa3b4af8e9b86c7555b`  
		Last Modified: Tue, 16 Apr 2024 06:26:47 GMT  
		Size: 23.1 MB (23101278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9453c9487179fa17fe3f9ad4c74f5d920e79eb3295c1bdbeeca9aaabca9f05`  
		Last Modified: Tue, 16 Apr 2024 06:28:41 GMT  
		Size: 691.5 MB (691500873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b1c1fd8fe542e5007cf7734c73270b4f5458f52b7b98765e2b606d7e884b0856
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915585208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6f7ed4e233758f8fba13b37b0222799d3cf260635322f105352724ec737ce3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:12:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:12:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:12:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:12:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:22:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09ab4678d1ee12b412975a8af36009ee6d3d376a4fdece02890d890896e400b`  
		Last Modified: Tue, 16 Apr 2024 04:30:16 GMT  
		Size: 95.7 MB (95688558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644937a0a1280b2fa65eacfe6512948da1340c7f0defb67b2c9794460b79767`  
		Last Modified: Tue, 16 Apr 2024 04:30:06 GMT  
		Size: 316.5 KB (316541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61648cee52d405e737ad1ba192bbb3bf964c074f4699e4e7c9a994affee263`  
		Last Modified: Tue, 16 Apr 2024 04:30:07 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6a0221c852ee06a60c52341c9d399c4d645c4f9b320ba89399d36d3385d7b`  
		Last Modified: Tue, 16 Apr 2024 04:30:09 GMT  
		Size: 22.5 MB (22520996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6db9f9bccc5c84e81e23a37638cf8f21bd6998766ea335de084742b3f40cb1a`  
		Last Modified: Tue, 16 Apr 2024 04:31:42 GMT  
		Size: 659.4 MB (659413693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:f6758a3f69f9467b4787d796ebdd7f7bc80e48ee8711927abca07b33cefd8031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1d79a35a22fafc6ffa68872325824a50cadd71a62b9d905ce98e83622b29af6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.1 MB (955055167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267f36f318885eeac089d57766d8256dc0748da93c2f16ab6bedb6c604a83880`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:58:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:58:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:58:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 05:59:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:07:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a53e9f9de03d6c034c610e08dc70cceccb90d9c98f414880a140ea8da931364`  
		Last Modified: Tue, 16 Apr 2024 06:26:58 GMT  
		Size: 98.1 MB (98144815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32be56bd237bb233aa7f0b0607fe10d70ff1b5d77663f5a63010eb2092a3819f`  
		Last Modified: Tue, 16 Apr 2024 06:26:44 GMT  
		Size: 316.5 KB (316546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282750c3b13e653a477b3c260ec106304999a833a29510dff2fcdedc692080bd`  
		Last Modified: Tue, 16 Apr 2024 06:26:43 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289549d7f60f97bb94619fa3d17f212efe6f81c43b4aaa3b4af8e9b86c7555b`  
		Last Modified: Tue, 16 Apr 2024 06:26:47 GMT  
		Size: 23.1 MB (23101278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9453c9487179fa17fe3f9ad4c74f5d920e79eb3295c1bdbeeca9aaabca9f05`  
		Last Modified: Tue, 16 Apr 2024 06:28:41 GMT  
		Size: 691.5 MB (691500873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b1c1fd8fe542e5007cf7734c73270b4f5458f52b7b98765e2b606d7e884b0856
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915585208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6f7ed4e233758f8fba13b37b0222799d3cf260635322f105352724ec737ce3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:12:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:12:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:12:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:12:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:22:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09ab4678d1ee12b412975a8af36009ee6d3d376a4fdece02890d890896e400b`  
		Last Modified: Tue, 16 Apr 2024 04:30:16 GMT  
		Size: 95.7 MB (95688558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644937a0a1280b2fa65eacfe6512948da1340c7f0defb67b2c9794460b79767`  
		Last Modified: Tue, 16 Apr 2024 04:30:06 GMT  
		Size: 316.5 KB (316541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61648cee52d405e737ad1ba192bbb3bf964c074f4699e4e7c9a994affee263`  
		Last Modified: Tue, 16 Apr 2024 04:30:07 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6a0221c852ee06a60c52341c9d399c4d645c4f9b320ba89399d36d3385d7b`  
		Last Modified: Tue, 16 Apr 2024 04:30:09 GMT  
		Size: 22.5 MB (22520996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6db9f9bccc5c84e81e23a37638cf8f21bd6998766ea335de084742b3f40cb1a`  
		Last Modified: Tue, 16 Apr 2024 04:31:42 GMT  
		Size: 659.4 MB (659413693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:f0300c9cef207d18b33629cabcfe3dc0b23255b7a41a126fe047ed4449494740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:5865a4ea85c1b0e548707f25f5e816fa1a5f2c885c2f2b6db9c418e9a3caa6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263554294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718c0a4486a6aa164b79edaa44c9f165460ffbb0281b7e819cd421445845a0d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:58:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:58:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:58:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 05:59:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a53e9f9de03d6c034c610e08dc70cceccb90d9c98f414880a140ea8da931364`  
		Last Modified: Tue, 16 Apr 2024 06:26:58 GMT  
		Size: 98.1 MB (98144815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32be56bd237bb233aa7f0b0607fe10d70ff1b5d77663f5a63010eb2092a3819f`  
		Last Modified: Tue, 16 Apr 2024 06:26:44 GMT  
		Size: 316.5 KB (316546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282750c3b13e653a477b3c260ec106304999a833a29510dff2fcdedc692080bd`  
		Last Modified: Tue, 16 Apr 2024 06:26:43 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289549d7f60f97bb94619fa3d17f212efe6f81c43b4aaa3b4af8e9b86c7555b`  
		Last Modified: Tue, 16 Apr 2024 06:26:47 GMT  
		Size: 23.1 MB (23101278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:801c95e60a6b8f045975fc2874233834a56cd244777b050aa61a09504151fa94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256171515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed940c284a110dd2cf289e8a68ab71a64a0ce9b24687d3da3e179e2bf401253`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:12:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:12:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:12:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:12:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09ab4678d1ee12b412975a8af36009ee6d3d376a4fdece02890d890896e400b`  
		Last Modified: Tue, 16 Apr 2024 04:30:16 GMT  
		Size: 95.7 MB (95688558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644937a0a1280b2fa65eacfe6512948da1340c7f0defb67b2c9794460b79767`  
		Last Modified: Tue, 16 Apr 2024 04:30:06 GMT  
		Size: 316.5 KB (316541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61648cee52d405e737ad1ba192bbb3bf964c074f4699e4e7c9a994affee263`  
		Last Modified: Tue, 16 Apr 2024 04:30:07 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6a0221c852ee06a60c52341c9d399c4d645c4f9b320ba89399d36d3385d7b`  
		Last Modified: Tue, 16 Apr 2024 04:30:09 GMT  
		Size: 22.5 MB (22520996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:f0300c9cef207d18b33629cabcfe3dc0b23255b7a41a126fe047ed4449494740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:5865a4ea85c1b0e548707f25f5e816fa1a5f2c885c2f2b6db9c418e9a3caa6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263554294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718c0a4486a6aa164b79edaa44c9f165460ffbb0281b7e819cd421445845a0d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:58:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:58:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:58:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 05:59:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a53e9f9de03d6c034c610e08dc70cceccb90d9c98f414880a140ea8da931364`  
		Last Modified: Tue, 16 Apr 2024 06:26:58 GMT  
		Size: 98.1 MB (98144815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32be56bd237bb233aa7f0b0607fe10d70ff1b5d77663f5a63010eb2092a3819f`  
		Last Modified: Tue, 16 Apr 2024 06:26:44 GMT  
		Size: 316.5 KB (316546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282750c3b13e653a477b3c260ec106304999a833a29510dff2fcdedc692080bd`  
		Last Modified: Tue, 16 Apr 2024 06:26:43 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289549d7f60f97bb94619fa3d17f212efe6f81c43b4aaa3b4af8e9b86c7555b`  
		Last Modified: Tue, 16 Apr 2024 06:26:47 GMT  
		Size: 23.1 MB (23101278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:801c95e60a6b8f045975fc2874233834a56cd244777b050aa61a09504151fa94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256171515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed940c284a110dd2cf289e8a68ab71a64a0ce9b24687d3da3e179e2bf401253`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:12:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:12:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:12:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:12:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09ab4678d1ee12b412975a8af36009ee6d3d376a4fdece02890d890896e400b`  
		Last Modified: Tue, 16 Apr 2024 04:30:16 GMT  
		Size: 95.7 MB (95688558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644937a0a1280b2fa65eacfe6512948da1340c7f0defb67b2c9794460b79767`  
		Last Modified: Tue, 16 Apr 2024 04:30:06 GMT  
		Size: 316.5 KB (316541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61648cee52d405e737ad1ba192bbb3bf964c074f4699e4e7c9a994affee263`  
		Last Modified: Tue, 16 Apr 2024 04:30:07 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6a0221c852ee06a60c52341c9d399c4d645c4f9b320ba89399d36d3385d7b`  
		Last Modified: Tue, 16 Apr 2024 04:30:09 GMT  
		Size: 22.5 MB (22520996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:22cd499dba0929c34121be8cc1ad1a5dd882dec6a73c789563c7e057d696fb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:04b7706431613a9f96f52722afea5ddb5b8cc7cfca21f7788ea2f64113106c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141989176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9e9ea97bbfd2afb0ef16979f5e610bbe87d9bcbf6a4e336a1665bf9020f079`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:94ee9c8f3470277b6263b9a1e92b7f77687362e1088dbc96a9cfa8671ce6c85a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137642939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04fcf1a72be6f817692bdb3deafea66dc10f0ad09fcb5f8b7dbe6833a66289b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:22cd499dba0929c34121be8cc1ad1a5dd882dec6a73c789563c7e057d696fb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:04b7706431613a9f96f52722afea5ddb5b8cc7cfca21f7788ea2f64113106c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141989176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9e9ea97bbfd2afb0ef16979f5e610bbe87d9bcbf6a4e336a1665bf9020f079`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:94ee9c8f3470277b6263b9a1e92b7f77687362e1088dbc96a9cfa8671ce6c85a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137642939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04fcf1a72be6f817692bdb3deafea66dc10f0ad09fcb5f8b7dbe6833a66289b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:a0ad16c1f6c05c306d54701f58c074fad269e3ab4729e5aa9204a3dcd2f78904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:1ae402199a2ebd0051846c168556dbaa7fcfa55d10dde07d76fd5ddb955a5ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268950751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fa1b6c4bfab7ddd0fee2d0a48836d96091c80d0847f743b73dc332898b0421`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:07:26 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 06:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:08:15 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:08:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:08:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:09:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727b503e9d63f1b3aeb6612958d9a4232c958077d92ca9573074954db20ce689`  
		Last Modified: Tue, 16 Apr 2024 06:29:10 GMT  
		Size: 124.3 MB (124253346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5622b9e20b4fc93b6cd8461b90c909b335a8850a708ef14b35ca233c62080273`  
		Last Modified: Tue, 16 Apr 2024 06:28:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a87942f9d01dfde36dea2865ef2eaf530bfbee41622f8219995d49b3887132`  
		Last Modified: Tue, 16 Apr 2024 06:29:29 GMT  
		Size: 85.2 MB (85171843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd24d9cec1c5a6d7f6341dabe522c7320bd9e43fca6fff9476c135303463376`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 303.1 KB (303063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe0fc7dc345e163298196053abe2e4b66f4d5a64025a62fa91c99fda6ecbe99`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa65e7c084726567829c16beec4011e5319e724d8dd2d7926764cd0c42906d5`  
		Last Modified: Tue, 16 Apr 2024 06:29:22 GMT  
		Size: 23.7 MB (23733464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:843e23952d90e4a3276f7d70f39ebf750a57199558c9b8929678873235532082
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261437296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781cdf661615ad74e6487da82ec5b15bc71399de6cebd9252c61062bb0dae5f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:22:35 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 04:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:22 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:23:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:23:22 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:23:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:23:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:24:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5d5ecc9595a1354b977a8c6539b21f9f10617e634ffec2c2b4cd3829cbda5`  
		Last Modified: Tue, 16 Apr 2024 04:32:05 GMT  
		Size: 121.7 MB (121742019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1940bcead61acceacf0b309cca3527216d8a4e3760dd527f596e3dfe7e52ce`  
		Last Modified: Tue, 16 Apr 2024 04:31:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441faad2245eb58df35d4666f35a9c96bcb1efce87245957d7c2544c15b7921`  
		Last Modified: Tue, 16 Apr 2024 04:32:26 GMT  
		Size: 82.8 MB (82848126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefaf205056cc4a47796d83cc8aa33b0a133aabdeacb31e5849a229bd913cb8`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 303.1 KB (303069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e2526138d639016cab5460e48f1e9781b7615736945037d5e823d35aa8a61b`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d64acab4807aebf316411a4d1fee5638d1ed3b786841c344a056528ec7f61`  
		Last Modified: Tue, 16 Apr 2024 04:32:22 GMT  
		Size: 23.1 MB (23121700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:14b54efb5b038620894ba193950c19874d6fdd810cac5d1c90be80913f338f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:b1612f2d5802ee018b198a8e5e36cd7f69d6b7aa7db31abbbc422027fba38318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961137482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6733b127bd9d56da7f62cd03a7e635e0106d8f12770bb88bb61f002697a31084`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:07:26 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 06:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:08:15 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:08:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:08:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:09:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:10:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727b503e9d63f1b3aeb6612958d9a4232c958077d92ca9573074954db20ce689`  
		Last Modified: Tue, 16 Apr 2024 06:29:10 GMT  
		Size: 124.3 MB (124253346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5622b9e20b4fc93b6cd8461b90c909b335a8850a708ef14b35ca233c62080273`  
		Last Modified: Tue, 16 Apr 2024 06:28:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a87942f9d01dfde36dea2865ef2eaf530bfbee41622f8219995d49b3887132`  
		Last Modified: Tue, 16 Apr 2024 06:29:29 GMT  
		Size: 85.2 MB (85171843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd24d9cec1c5a6d7f6341dabe522c7320bd9e43fca6fff9476c135303463376`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 303.1 KB (303063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe0fc7dc345e163298196053abe2e4b66f4d5a64025a62fa91c99fda6ecbe99`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa65e7c084726567829c16beec4011e5319e724d8dd2d7926764cd0c42906d5`  
		Last Modified: Tue, 16 Apr 2024 06:29:22 GMT  
		Size: 23.7 MB (23733464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717d8f0250367f7940e3f481008dc5663b7a1c658b91be4aa1b5becc01376294`  
		Last Modified: Tue, 16 Apr 2024 06:31:10 GMT  
		Size: 692.2 MB (692186731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1a9bf08167d13e21b50e3cf531e79c9c3781be33177a4c76d9659413e911a474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921517165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a987cc7bbfe0d0c3dd356a100352223a0f502486ad5b6ca1208582d7f6deadf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:22:35 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 04:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:22 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:23:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:23:22 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:23:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:23:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:24:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:25:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5d5ecc9595a1354b977a8c6539b21f9f10617e634ffec2c2b4cd3829cbda5`  
		Last Modified: Tue, 16 Apr 2024 04:32:05 GMT  
		Size: 121.7 MB (121742019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1940bcead61acceacf0b309cca3527216d8a4e3760dd527f596e3dfe7e52ce`  
		Last Modified: Tue, 16 Apr 2024 04:31:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441faad2245eb58df35d4666f35a9c96bcb1efce87245957d7c2544c15b7921`  
		Last Modified: Tue, 16 Apr 2024 04:32:26 GMT  
		Size: 82.8 MB (82848126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefaf205056cc4a47796d83cc8aa33b0a133aabdeacb31e5849a229bd913cb8`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 303.1 KB (303069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e2526138d639016cab5460e48f1e9781b7615736945037d5e823d35aa8a61b`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d64acab4807aebf316411a4d1fee5638d1ed3b786841c344a056528ec7f61`  
		Last Modified: Tue, 16 Apr 2024 04:32:22 GMT  
		Size: 23.1 MB (23121700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f52d98979e196d4191ffa91c0c5d79baf40a78af94ef50f4fe8f4dda38410c`  
		Last Modified: Tue, 16 Apr 2024 04:34:12 GMT  
		Size: 660.1 MB (660079869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:14b54efb5b038620894ba193950c19874d6fdd810cac5d1c90be80913f338f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b1612f2d5802ee018b198a8e5e36cd7f69d6b7aa7db31abbbc422027fba38318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961137482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6733b127bd9d56da7f62cd03a7e635e0106d8f12770bb88bb61f002697a31084`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:07:26 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 06:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:08:15 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:08:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:08:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:09:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:10:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727b503e9d63f1b3aeb6612958d9a4232c958077d92ca9573074954db20ce689`  
		Last Modified: Tue, 16 Apr 2024 06:29:10 GMT  
		Size: 124.3 MB (124253346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5622b9e20b4fc93b6cd8461b90c909b335a8850a708ef14b35ca233c62080273`  
		Last Modified: Tue, 16 Apr 2024 06:28:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a87942f9d01dfde36dea2865ef2eaf530bfbee41622f8219995d49b3887132`  
		Last Modified: Tue, 16 Apr 2024 06:29:29 GMT  
		Size: 85.2 MB (85171843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd24d9cec1c5a6d7f6341dabe522c7320bd9e43fca6fff9476c135303463376`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 303.1 KB (303063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe0fc7dc345e163298196053abe2e4b66f4d5a64025a62fa91c99fda6ecbe99`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa65e7c084726567829c16beec4011e5319e724d8dd2d7926764cd0c42906d5`  
		Last Modified: Tue, 16 Apr 2024 06:29:22 GMT  
		Size: 23.7 MB (23733464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717d8f0250367f7940e3f481008dc5663b7a1c658b91be4aa1b5becc01376294`  
		Last Modified: Tue, 16 Apr 2024 06:31:10 GMT  
		Size: 692.2 MB (692186731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1a9bf08167d13e21b50e3cf531e79c9c3781be33177a4c76d9659413e911a474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921517165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a987cc7bbfe0d0c3dd356a100352223a0f502486ad5b6ca1208582d7f6deadf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:22:35 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 04:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:22 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:23:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:23:22 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:23:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:23:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:24:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:25:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5d5ecc9595a1354b977a8c6539b21f9f10617e634ffec2c2b4cd3829cbda5`  
		Last Modified: Tue, 16 Apr 2024 04:32:05 GMT  
		Size: 121.7 MB (121742019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1940bcead61acceacf0b309cca3527216d8a4e3760dd527f596e3dfe7e52ce`  
		Last Modified: Tue, 16 Apr 2024 04:31:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441faad2245eb58df35d4666f35a9c96bcb1efce87245957d7c2544c15b7921`  
		Last Modified: Tue, 16 Apr 2024 04:32:26 GMT  
		Size: 82.8 MB (82848126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefaf205056cc4a47796d83cc8aa33b0a133aabdeacb31e5849a229bd913cb8`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 303.1 KB (303069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e2526138d639016cab5460e48f1e9781b7615736945037d5e823d35aa8a61b`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d64acab4807aebf316411a4d1fee5638d1ed3b786841c344a056528ec7f61`  
		Last Modified: Tue, 16 Apr 2024 04:32:22 GMT  
		Size: 23.1 MB (23121700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f52d98979e196d4191ffa91c0c5d79baf40a78af94ef50f4fe8f4dda38410c`  
		Last Modified: Tue, 16 Apr 2024 04:34:12 GMT  
		Size: 660.1 MB (660079869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:a0ad16c1f6c05c306d54701f58c074fad269e3ab4729e5aa9204a3dcd2f78904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1ae402199a2ebd0051846c168556dbaa7fcfa55d10dde07d76fd5ddb955a5ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268950751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fa1b6c4bfab7ddd0fee2d0a48836d96091c80d0847f743b73dc332898b0421`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:07:26 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 06:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:08:15 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:08:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:08:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:09:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727b503e9d63f1b3aeb6612958d9a4232c958077d92ca9573074954db20ce689`  
		Last Modified: Tue, 16 Apr 2024 06:29:10 GMT  
		Size: 124.3 MB (124253346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5622b9e20b4fc93b6cd8461b90c909b335a8850a708ef14b35ca233c62080273`  
		Last Modified: Tue, 16 Apr 2024 06:28:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a87942f9d01dfde36dea2865ef2eaf530bfbee41622f8219995d49b3887132`  
		Last Modified: Tue, 16 Apr 2024 06:29:29 GMT  
		Size: 85.2 MB (85171843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd24d9cec1c5a6d7f6341dabe522c7320bd9e43fca6fff9476c135303463376`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 303.1 KB (303063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe0fc7dc345e163298196053abe2e4b66f4d5a64025a62fa91c99fda6ecbe99`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa65e7c084726567829c16beec4011e5319e724d8dd2d7926764cd0c42906d5`  
		Last Modified: Tue, 16 Apr 2024 06:29:22 GMT  
		Size: 23.7 MB (23733464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:843e23952d90e4a3276f7d70f39ebf750a57199558c9b8929678873235532082
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261437296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781cdf661615ad74e6487da82ec5b15bc71399de6cebd9252c61062bb0dae5f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:22:35 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 04:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:22 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:23:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:23:22 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:23:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:23:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:24:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5d5ecc9595a1354b977a8c6539b21f9f10617e634ffec2c2b4cd3829cbda5`  
		Last Modified: Tue, 16 Apr 2024 04:32:05 GMT  
		Size: 121.7 MB (121742019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1940bcead61acceacf0b309cca3527216d8a4e3760dd527f596e3dfe7e52ce`  
		Last Modified: Tue, 16 Apr 2024 04:31:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441faad2245eb58df35d4666f35a9c96bcb1efce87245957d7c2544c15b7921`  
		Last Modified: Tue, 16 Apr 2024 04:32:26 GMT  
		Size: 82.8 MB (82848126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefaf205056cc4a47796d83cc8aa33b0a133aabdeacb31e5849a229bd913cb8`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 303.1 KB (303069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e2526138d639016cab5460e48f1e9781b7615736945037d5e823d35aa8a61b`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d64acab4807aebf316411a4d1fee5638d1ed3b786841c344a056528ec7f61`  
		Last Modified: Tue, 16 Apr 2024 04:32:22 GMT  
		Size: 23.1 MB (23121700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:a0ad16c1f6c05c306d54701f58c074fad269e3ab4729e5aa9204a3dcd2f78904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1ae402199a2ebd0051846c168556dbaa7fcfa55d10dde07d76fd5ddb955a5ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268950751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fa1b6c4bfab7ddd0fee2d0a48836d96091c80d0847f743b73dc332898b0421`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:07:26 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 06:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:08:15 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:08:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:08:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:09:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727b503e9d63f1b3aeb6612958d9a4232c958077d92ca9573074954db20ce689`  
		Last Modified: Tue, 16 Apr 2024 06:29:10 GMT  
		Size: 124.3 MB (124253346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5622b9e20b4fc93b6cd8461b90c909b335a8850a708ef14b35ca233c62080273`  
		Last Modified: Tue, 16 Apr 2024 06:28:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a87942f9d01dfde36dea2865ef2eaf530bfbee41622f8219995d49b3887132`  
		Last Modified: Tue, 16 Apr 2024 06:29:29 GMT  
		Size: 85.2 MB (85171843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd24d9cec1c5a6d7f6341dabe522c7320bd9e43fca6fff9476c135303463376`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 303.1 KB (303063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe0fc7dc345e163298196053abe2e4b66f4d5a64025a62fa91c99fda6ecbe99`  
		Last Modified: Tue, 16 Apr 2024 06:29:19 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa65e7c084726567829c16beec4011e5319e724d8dd2d7926764cd0c42906d5`  
		Last Modified: Tue, 16 Apr 2024 06:29:22 GMT  
		Size: 23.7 MB (23733464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:843e23952d90e4a3276f7d70f39ebf750a57199558c9b8929678873235532082
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261437296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781cdf661615ad74e6487da82ec5b15bc71399de6cebd9252c61062bb0dae5f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:22:35 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 04:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:22 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:23:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:23:22 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:23:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:23:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:24:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5d5ecc9595a1354b977a8c6539b21f9f10617e634ffec2c2b4cd3829cbda5`  
		Last Modified: Tue, 16 Apr 2024 04:32:05 GMT  
		Size: 121.7 MB (121742019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1940bcead61acceacf0b309cca3527216d8a4e3760dd527f596e3dfe7e52ce`  
		Last Modified: Tue, 16 Apr 2024 04:31:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441faad2245eb58df35d4666f35a9c96bcb1efce87245957d7c2544c15b7921`  
		Last Modified: Tue, 16 Apr 2024 04:32:26 GMT  
		Size: 82.8 MB (82848126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefaf205056cc4a47796d83cc8aa33b0a133aabdeacb31e5849a229bd913cb8`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 303.1 KB (303069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e2526138d639016cab5460e48f1e9781b7615736945037d5e823d35aa8a61b`  
		Last Modified: Tue, 16 Apr 2024 04:32:19 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d64acab4807aebf316411a4d1fee5638d1ed3b786841c344a056528ec7f61`  
		Last Modified: Tue, 16 Apr 2024 04:32:22 GMT  
		Size: 23.1 MB (23121700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:70b62b2186d3bd963fea9172769a6a8ac9547693920014e28f83405b60f830fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:b1d5ad13219d333978f8b788fae9b15a26cf44246044f9ca7ff125ea5a019eda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159739866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff21f182b013823cb26f9384595a54f6ca4c4a2d211dbfded45a4bea81ce8015`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:07:26 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 06:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:08:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727b503e9d63f1b3aeb6612958d9a4232c958077d92ca9573074954db20ce689`  
		Last Modified: Tue, 16 Apr 2024 06:29:10 GMT  
		Size: 124.3 MB (124253346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5622b9e20b4fc93b6cd8461b90c909b335a8850a708ef14b35ca233c62080273`  
		Last Modified: Tue, 16 Apr 2024 06:28:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4ff3ae744326962ba7cc823dd3d74c64d9e4e70c39c5914fd53bbef4d19f0017
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155161913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd71c56b95eadf5053b02d6bc4eece87b3c38ce040564970ed516434f33417cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:22:35 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 04:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:22 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:23:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:23:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5d5ecc9595a1354b977a8c6539b21f9f10617e634ffec2c2b4cd3829cbda5`  
		Last Modified: Tue, 16 Apr 2024 04:32:05 GMT  
		Size: 121.7 MB (121742019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1940bcead61acceacf0b309cca3527216d8a4e3760dd527f596e3dfe7e52ce`  
		Last Modified: Tue, 16 Apr 2024 04:31:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:70b62b2186d3bd963fea9172769a6a8ac9547693920014e28f83405b60f830fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b1d5ad13219d333978f8b788fae9b15a26cf44246044f9ca7ff125ea5a019eda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159739866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff21f182b013823cb26f9384595a54f6ca4c4a2d211dbfded45a4bea81ce8015`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:07:26 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 06:08:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:08:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:08:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:08:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727b503e9d63f1b3aeb6612958d9a4232c958077d92ca9573074954db20ce689`  
		Last Modified: Tue, 16 Apr 2024 06:29:10 GMT  
		Size: 124.3 MB (124253346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5622b9e20b4fc93b6cd8461b90c909b335a8850a708ef14b35ca233c62080273`  
		Last Modified: Tue, 16 Apr 2024 06:28:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4ff3ae744326962ba7cc823dd3d74c64d9e4e70c39c5914fd53bbef4d19f0017
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155161913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd71c56b95eadf5053b02d6bc4eece87b3c38ce040564970ed516434f33417cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:22:35 GMT
ENV ROS_DISTRO=iron
# Tue, 16 Apr 2024 04:23:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:23:22 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:23:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:23:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5d5ecc9595a1354b977a8c6539b21f9f10617e634ffec2c2b4cd3829cbda5`  
		Last Modified: Tue, 16 Apr 2024 04:32:05 GMT  
		Size: 121.7 MB (121742019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1940bcead61acceacf0b309cca3527216d8a4e3760dd527f596e3dfe7e52ce`  
		Last Modified: Tue, 16 Apr 2024 04:31:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:f0300c9cef207d18b33629cabcfe3dc0b23255b7a41a126fe047ed4449494740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:5865a4ea85c1b0e548707f25f5e816fa1a5f2c885c2f2b6db9c418e9a3caa6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263554294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718c0a4486a6aa164b79edaa44c9f165460ffbb0281b7e819cd421445845a0d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:58:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:58:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:58:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 05:59:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a53e9f9de03d6c034c610e08dc70cceccb90d9c98f414880a140ea8da931364`  
		Last Modified: Tue, 16 Apr 2024 06:26:58 GMT  
		Size: 98.1 MB (98144815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32be56bd237bb233aa7f0b0607fe10d70ff1b5d77663f5a63010eb2092a3819f`  
		Last Modified: Tue, 16 Apr 2024 06:26:44 GMT  
		Size: 316.5 KB (316546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282750c3b13e653a477b3c260ec106304999a833a29510dff2fcdedc692080bd`  
		Last Modified: Tue, 16 Apr 2024 06:26:43 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289549d7f60f97bb94619fa3d17f212efe6f81c43b4aaa3b4af8e9b86c7555b`  
		Last Modified: Tue, 16 Apr 2024 06:26:47 GMT  
		Size: 23.1 MB (23101278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:801c95e60a6b8f045975fc2874233834a56cd244777b050aa61a09504151fa94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256171515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed940c284a110dd2cf289e8a68ab71a64a0ce9b24687d3da3e179e2bf401253`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 04:12:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:12:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:12:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 04:12:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09ab4678d1ee12b412975a8af36009ee6d3d376a4fdece02890d890896e400b`  
		Last Modified: Tue, 16 Apr 2024 04:30:16 GMT  
		Size: 95.7 MB (95688558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3644937a0a1280b2fa65eacfe6512948da1340c7f0defb67b2c9794460b79767`  
		Last Modified: Tue, 16 Apr 2024 04:30:06 GMT  
		Size: 316.5 KB (316541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd61648cee52d405e737ad1ba192bbb3bf964c074f4699e4e7c9a994affee263`  
		Last Modified: Tue, 16 Apr 2024 04:30:07 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6a0221c852ee06a60c52341c9d399c4d645c4f9b320ba89399d36d3385d7b`  
		Last Modified: Tue, 16 Apr 2024 04:30:09 GMT  
		Size: 22.5 MB (22520996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:20b337f10f4275a6d589388cf8f72a7216de2ba3632b10d9d05c205c65446b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:a98aba6bd66e748c00ac8e3f49301a705098d21895e3b8083810128b4970de85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264727228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff1104ff05bfbfd2cae96418b8bf424f39900b1ac3078547614b0578cb6783`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:47:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7127f4302b5d7690e9128f8a7051575604639251e3a4fb770aecf12f4eb09`  
		Last Modified: Tue, 16 Apr 2024 06:24:25 GMT  
		Size: 50.9 MB (50942064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c0401b1d83939b2f027a6560c4dc65fd7a4a4b6cc4ab6b73986a90c70a3df`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 320.3 KB (320347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a527f20b46de848ab8d7d47519a866273776636a5ed05c0b5ad9776327ef4`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 1.1 MB (1130655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:635eb1391a3b8bb1fc42b87569f1f2dffdaf3c80c160a640d94f308330021e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229839090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc577849b266aeb15413942ea0a869d4b9dedab59d86a27b31202dd1302abaf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 02:01:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7425da53f3c1d55c83d3a606a99acd8eef02039870d76d98ebede0619d0b2122`  
		Last Modified: Tue, 16 Apr 2024 02:12:36 GMT  
		Size: 40.5 MB (40505672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafaaf4238382826bc4dfb255028df6bc9ddc8bc776e38844ae4d49eb012aa8`  
		Last Modified: Tue, 16 Apr 2024 02:12:30 GMT  
		Size: 320.4 KB (320353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5043f2ccdd491f51c214414dedd2bcfa681447f1a87169fc8c9be6ad8ce99d5`  
		Last Modified: Tue, 16 Apr 2024 02:12:31 GMT  
		Size: 1.1 MB (1061815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:10c849400e59d70fd0382b5451aff7f989e32640d4abb0afbc11e4cd93f120ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251966661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5231a09af0bed0887118754f7797c9ed15471a9b98876bae2afd0f72656b6ca2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 03:59:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68cf2dcea72a76f4194585b5fe94ebc6ceed16911250d44186a9f060b3e832d`  
		Last Modified: Tue, 16 Apr 2024 04:28:03 GMT  
		Size: 45.2 MB (45207668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5333b432eed5e9067399472b766459ecaab72e2d23c9d5fd42d70f4275594`  
		Last Modified: Tue, 16 Apr 2024 04:27:57 GMT  
		Size: 320.4 KB (320355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f6a82e2dc62e74bac15cfaa0678c5f0076676fd02435d94d9e26f7a92bca`  
		Last Modified: Tue, 16 Apr 2024 04:27:58 GMT  
		Size: 1.1 MB (1115135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:f1001b7cb91777fa78f8fd7a319ef2481f82fee9f88048d6d52366046a671325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:52461efe4708b02006dd49cd166a62531e5c577ae371925b98208f8117cd1de4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835400194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c35d716844b824480907e9c138bbba6ac87639d51b452b59ecab78c12eb8df`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:47:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7127f4302b5d7690e9128f8a7051575604639251e3a4fb770aecf12f4eb09`  
		Last Modified: Tue, 16 Apr 2024 06:24:25 GMT  
		Size: 50.9 MB (50942064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c0401b1d83939b2f027a6560c4dc65fd7a4a4b6cc4ab6b73986a90c70a3df`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 320.3 KB (320347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a527f20b46de848ab8d7d47519a866273776636a5ed05c0b5ad9776327ef4`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 1.1 MB (1130655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531aa000bd3c3c147ba8e3f84106e3c508cbc4b17a3ade6e46fa307b41acd091`  
		Last Modified: Tue, 16 Apr 2024 06:26:09 GMT  
		Size: 570.7 MB (570672966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:ef7e32a6ce7acd63476f8d04cd7ef23ec7efa0c832e331acddff9aa93e92c923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.4 MB (726358755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745951cff819f3351020204f437fa6cfb5449cf161af0be80d3faa13cbbb7b94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 02:01:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:11:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7425da53f3c1d55c83d3a606a99acd8eef02039870d76d98ebede0619d0b2122`  
		Last Modified: Tue, 16 Apr 2024 02:12:36 GMT  
		Size: 40.5 MB (40505672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafaaf4238382826bc4dfb255028df6bc9ddc8bc776e38844ae4d49eb012aa8`  
		Last Modified: Tue, 16 Apr 2024 02:12:30 GMT  
		Size: 320.4 KB (320353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5043f2ccdd491f51c214414dedd2bcfa681447f1a87169fc8c9be6ad8ce99d5`  
		Last Modified: Tue, 16 Apr 2024 02:12:31 GMT  
		Size: 1.1 MB (1061815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8197fdca42d04a72358dc0be5dd3de41f3ba70f664cf6c117adf0d041563dc7b`  
		Last Modified: Tue, 16 Apr 2024 02:14:17 GMT  
		Size: 496.5 MB (496519665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d98bbfd83b227a42b3355642681f4c99bf3bdb7df1bc55c790af943cb1f8e65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785606448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224e629bb73af675852edeb4cae73685fbb15e18846e2593ab5556aed4c013e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 03:59:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:09:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68cf2dcea72a76f4194585b5fe94ebc6ceed16911250d44186a9f060b3e832d`  
		Last Modified: Tue, 16 Apr 2024 04:28:03 GMT  
		Size: 45.2 MB (45207668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5333b432eed5e9067399472b766459ecaab72e2d23c9d5fd42d70f4275594`  
		Last Modified: Tue, 16 Apr 2024 04:27:57 GMT  
		Size: 320.4 KB (320355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f6a82e2dc62e74bac15cfaa0678c5f0076676fd02435d94d9e26f7a92bca`  
		Last Modified: Tue, 16 Apr 2024 04:27:58 GMT  
		Size: 1.1 MB (1115135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7702a3540858594d7cb89a451c6531d55f33384d21aa12c1df41981f9b1541ae`  
		Last Modified: Tue, 16 Apr 2024 04:29:34 GMT  
		Size: 533.6 MB (533639787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:f1001b7cb91777fa78f8fd7a319ef2481f82fee9f88048d6d52366046a671325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:52461efe4708b02006dd49cd166a62531e5c577ae371925b98208f8117cd1de4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835400194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c35d716844b824480907e9c138bbba6ac87639d51b452b59ecab78c12eb8df`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:47:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7127f4302b5d7690e9128f8a7051575604639251e3a4fb770aecf12f4eb09`  
		Last Modified: Tue, 16 Apr 2024 06:24:25 GMT  
		Size: 50.9 MB (50942064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c0401b1d83939b2f027a6560c4dc65fd7a4a4b6cc4ab6b73986a90c70a3df`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 320.3 KB (320347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a527f20b46de848ab8d7d47519a866273776636a5ed05c0b5ad9776327ef4`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 1.1 MB (1130655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531aa000bd3c3c147ba8e3f84106e3c508cbc4b17a3ade6e46fa307b41acd091`  
		Last Modified: Tue, 16 Apr 2024 06:26:09 GMT  
		Size: 570.7 MB (570672966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:ef7e32a6ce7acd63476f8d04cd7ef23ec7efa0c832e331acddff9aa93e92c923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.4 MB (726358755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745951cff819f3351020204f437fa6cfb5449cf161af0be80d3faa13cbbb7b94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 02:01:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:11:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7425da53f3c1d55c83d3a606a99acd8eef02039870d76d98ebede0619d0b2122`  
		Last Modified: Tue, 16 Apr 2024 02:12:36 GMT  
		Size: 40.5 MB (40505672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafaaf4238382826bc4dfb255028df6bc9ddc8bc776e38844ae4d49eb012aa8`  
		Last Modified: Tue, 16 Apr 2024 02:12:30 GMT  
		Size: 320.4 KB (320353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5043f2ccdd491f51c214414dedd2bcfa681447f1a87169fc8c9be6ad8ce99d5`  
		Last Modified: Tue, 16 Apr 2024 02:12:31 GMT  
		Size: 1.1 MB (1061815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8197fdca42d04a72358dc0be5dd3de41f3ba70f664cf6c117adf0d041563dc7b`  
		Last Modified: Tue, 16 Apr 2024 02:14:17 GMT  
		Size: 496.5 MB (496519665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d98bbfd83b227a42b3355642681f4c99bf3bdb7df1bc55c790af943cb1f8e65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785606448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224e629bb73af675852edeb4cae73685fbb15e18846e2593ab5556aed4c013e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 03:59:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:09:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68cf2dcea72a76f4194585b5fe94ebc6ceed16911250d44186a9f060b3e832d`  
		Last Modified: Tue, 16 Apr 2024 04:28:03 GMT  
		Size: 45.2 MB (45207668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5333b432eed5e9067399472b766459ecaab72e2d23c9d5fd42d70f4275594`  
		Last Modified: Tue, 16 Apr 2024 04:27:57 GMT  
		Size: 320.4 KB (320355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f6a82e2dc62e74bac15cfaa0678c5f0076676fd02435d94d9e26f7a92bca`  
		Last Modified: Tue, 16 Apr 2024 04:27:58 GMT  
		Size: 1.1 MB (1115135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7702a3540858594d7cb89a451c6531d55f33384d21aa12c1df41981f9b1541ae`  
		Last Modified: Tue, 16 Apr 2024 04:29:34 GMT  
		Size: 533.6 MB (533639787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:0e12e4db836e78c74c4b04c6d16f185d9a18d2b13cf5580747efa075eb6dc6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:94ce7a8cb1e0def4d19c38cb748a5e60a28488ae99cbd86db3aae407828d8eb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281656031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11334be85f176e5cd6a6e2b6d3b3ab6d2c5ec17528b96d75c3623826b7e1234`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:47:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:48:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7127f4302b5d7690e9128f8a7051575604639251e3a4fb770aecf12f4eb09`  
		Last Modified: Tue, 16 Apr 2024 06:24:25 GMT  
		Size: 50.9 MB (50942064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c0401b1d83939b2f027a6560c4dc65fd7a4a4b6cc4ab6b73986a90c70a3df`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 320.3 KB (320347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a527f20b46de848ab8d7d47519a866273776636a5ed05c0b5ad9776327ef4`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 1.1 MB (1130655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086a1e2c552b5fe21217c7ce46bcef156f5e0bbd974d452858f8d61789eed5b2`  
		Last Modified: Tue, 16 Apr 2024 06:24:40 GMT  
		Size: 16.9 MB (16928803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:7c55f162c417cd349f779bdfc988311975ec0477d0d49f05ed3a697f92edc994
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244868275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e78b81d1a89f6e7567f38a44a1bb78d6d8b8e69025f6fb9bb58cf152a98cba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 02:01:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:02:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7425da53f3c1d55c83d3a606a99acd8eef02039870d76d98ebede0619d0b2122`  
		Last Modified: Tue, 16 Apr 2024 02:12:36 GMT  
		Size: 40.5 MB (40505672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafaaf4238382826bc4dfb255028df6bc9ddc8bc776e38844ae4d49eb012aa8`  
		Last Modified: Tue, 16 Apr 2024 02:12:30 GMT  
		Size: 320.4 KB (320353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5043f2ccdd491f51c214414dedd2bcfa681447f1a87169fc8c9be6ad8ce99d5`  
		Last Modified: Tue, 16 Apr 2024 02:12:31 GMT  
		Size: 1.1 MB (1061815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b965427e7dad94e871a58f764dd5b91570b53ee2e8dbbccd207152f92858190`  
		Last Modified: Tue, 16 Apr 2024 02:12:48 GMT  
		Size: 15.0 MB (15029185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fa1baeffb4d38cf59435c559c7a0060fdb2ab58326aa6df8d3be3d1888c72d3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268496977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e33c59ff21f927eca9d17ed6685d15f340eb59eb9e7659d37df8ced1d75e33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 03:59:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68cf2dcea72a76f4194585b5fe94ebc6ceed16911250d44186a9f060b3e832d`  
		Last Modified: Tue, 16 Apr 2024 04:28:03 GMT  
		Size: 45.2 MB (45207668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5333b432eed5e9067399472b766459ecaab72e2d23c9d5fd42d70f4275594`  
		Last Modified: Tue, 16 Apr 2024 04:27:57 GMT  
		Size: 320.4 KB (320355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f6a82e2dc62e74bac15cfaa0678c5f0076676fd02435d94d9e26f7a92bca`  
		Last Modified: Tue, 16 Apr 2024 04:27:58 GMT  
		Size: 1.1 MB (1115135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005786016daaff69431be743c70c7bb4b9ab753f2225c3c48eca3955f60e6411`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 16.5 MB (16530316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:0e12e4db836e78c74c4b04c6d16f185d9a18d2b13cf5580747efa075eb6dc6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:94ce7a8cb1e0def4d19c38cb748a5e60a28488ae99cbd86db3aae407828d8eb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281656031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11334be85f176e5cd6a6e2b6d3b3ab6d2c5ec17528b96d75c3623826b7e1234`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:47:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:48:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7127f4302b5d7690e9128f8a7051575604639251e3a4fb770aecf12f4eb09`  
		Last Modified: Tue, 16 Apr 2024 06:24:25 GMT  
		Size: 50.9 MB (50942064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c0401b1d83939b2f027a6560c4dc65fd7a4a4b6cc4ab6b73986a90c70a3df`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 320.3 KB (320347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a527f20b46de848ab8d7d47519a866273776636a5ed05c0b5ad9776327ef4`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 1.1 MB (1130655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086a1e2c552b5fe21217c7ce46bcef156f5e0bbd974d452858f8d61789eed5b2`  
		Last Modified: Tue, 16 Apr 2024 06:24:40 GMT  
		Size: 16.9 MB (16928803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:7c55f162c417cd349f779bdfc988311975ec0477d0d49f05ed3a697f92edc994
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244868275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e78b81d1a89f6e7567f38a44a1bb78d6d8b8e69025f6fb9bb58cf152a98cba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 02:01:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:02:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7425da53f3c1d55c83d3a606a99acd8eef02039870d76d98ebede0619d0b2122`  
		Last Modified: Tue, 16 Apr 2024 02:12:36 GMT  
		Size: 40.5 MB (40505672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafaaf4238382826bc4dfb255028df6bc9ddc8bc776e38844ae4d49eb012aa8`  
		Last Modified: Tue, 16 Apr 2024 02:12:30 GMT  
		Size: 320.4 KB (320353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5043f2ccdd491f51c214414dedd2bcfa681447f1a87169fc8c9be6ad8ce99d5`  
		Last Modified: Tue, 16 Apr 2024 02:12:31 GMT  
		Size: 1.1 MB (1061815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b965427e7dad94e871a58f764dd5b91570b53ee2e8dbbccd207152f92858190`  
		Last Modified: Tue, 16 Apr 2024 02:12:48 GMT  
		Size: 15.0 MB (15029185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fa1baeffb4d38cf59435c559c7a0060fdb2ab58326aa6df8d3be3d1888c72d3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268496977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e33c59ff21f927eca9d17ed6685d15f340eb59eb9e7659d37df8ced1d75e33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 03:59:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68cf2dcea72a76f4194585b5fe94ebc6ceed16911250d44186a9f060b3e832d`  
		Last Modified: Tue, 16 Apr 2024 04:28:03 GMT  
		Size: 45.2 MB (45207668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5333b432eed5e9067399472b766459ecaab72e2d23c9d5fd42d70f4275594`  
		Last Modified: Tue, 16 Apr 2024 04:27:57 GMT  
		Size: 320.4 KB (320355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f6a82e2dc62e74bac15cfaa0678c5f0076676fd02435d94d9e26f7a92bca`  
		Last Modified: Tue, 16 Apr 2024 04:27:58 GMT  
		Size: 1.1 MB (1115135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005786016daaff69431be743c70c7bb4b9ab753f2225c3c48eca3955f60e6411`  
		Last Modified: Tue, 16 Apr 2024 04:28:15 GMT  
		Size: 16.5 MB (16530316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:20b337f10f4275a6d589388cf8f72a7216de2ba3632b10d9d05c205c65446b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:a98aba6bd66e748c00ac8e3f49301a705098d21895e3b8083810128b4970de85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264727228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff1104ff05bfbfd2cae96418b8bf424f39900b1ac3078547614b0578cb6783`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:47:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7127f4302b5d7690e9128f8a7051575604639251e3a4fb770aecf12f4eb09`  
		Last Modified: Tue, 16 Apr 2024 06:24:25 GMT  
		Size: 50.9 MB (50942064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c0401b1d83939b2f027a6560c4dc65fd7a4a4b6cc4ab6b73986a90c70a3df`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 320.3 KB (320347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a527f20b46de848ab8d7d47519a866273776636a5ed05c0b5ad9776327ef4`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 1.1 MB (1130655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:635eb1391a3b8bb1fc42b87569f1f2dffdaf3c80c160a640d94f308330021e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229839090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc577849b266aeb15413942ea0a869d4b9dedab59d86a27b31202dd1302abaf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 02:01:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7425da53f3c1d55c83d3a606a99acd8eef02039870d76d98ebede0619d0b2122`  
		Last Modified: Tue, 16 Apr 2024 02:12:36 GMT  
		Size: 40.5 MB (40505672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafaaf4238382826bc4dfb255028df6bc9ddc8bc776e38844ae4d49eb012aa8`  
		Last Modified: Tue, 16 Apr 2024 02:12:30 GMT  
		Size: 320.4 KB (320353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5043f2ccdd491f51c214414dedd2bcfa681447f1a87169fc8c9be6ad8ce99d5`  
		Last Modified: Tue, 16 Apr 2024 02:12:31 GMT  
		Size: 1.1 MB (1061815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:10c849400e59d70fd0382b5451aff7f989e32640d4abb0afbc11e4cd93f120ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251966661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5231a09af0bed0887118754f7797c9ed15471a9b98876bae2afd0f72656b6ca2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 03:59:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68cf2dcea72a76f4194585b5fe94ebc6ceed16911250d44186a9f060b3e832d`  
		Last Modified: Tue, 16 Apr 2024 04:28:03 GMT  
		Size: 45.2 MB (45207668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5333b432eed5e9067399472b766459ecaab72e2d23c9d5fd42d70f4275594`  
		Last Modified: Tue, 16 Apr 2024 04:27:57 GMT  
		Size: 320.4 KB (320355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f6a82e2dc62e74bac15cfaa0678c5f0076676fd02435d94d9e26f7a92bca`  
		Last Modified: Tue, 16 Apr 2024 04:27:58 GMT  
		Size: 1.1 MB (1115135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:20b337f10f4275a6d589388cf8f72a7216de2ba3632b10d9d05c205c65446b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:a98aba6bd66e748c00ac8e3f49301a705098d21895e3b8083810128b4970de85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264727228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff1104ff05bfbfd2cae96418b8bf424f39900b1ac3078547614b0578cb6783`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 05:47:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7127f4302b5d7690e9128f8a7051575604639251e3a4fb770aecf12f4eb09`  
		Last Modified: Tue, 16 Apr 2024 06:24:25 GMT  
		Size: 50.9 MB (50942064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c0401b1d83939b2f027a6560c4dc65fd7a4a4b6cc4ab6b73986a90c70a3df`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 320.3 KB (320347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a527f20b46de848ab8d7d47519a866273776636a5ed05c0b5ad9776327ef4`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 1.1 MB (1130655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:635eb1391a3b8bb1fc42b87569f1f2dffdaf3c80c160a640d94f308330021e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229839090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc577849b266aeb15413942ea0a869d4b9dedab59d86a27b31202dd1302abaf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 02:01:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7425da53f3c1d55c83d3a606a99acd8eef02039870d76d98ebede0619d0b2122`  
		Last Modified: Tue, 16 Apr 2024 02:12:36 GMT  
		Size: 40.5 MB (40505672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafaaf4238382826bc4dfb255028df6bc9ddc8bc776e38844ae4d49eb012aa8`  
		Last Modified: Tue, 16 Apr 2024 02:12:30 GMT  
		Size: 320.4 KB (320353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5043f2ccdd491f51c214414dedd2bcfa681447f1a87169fc8c9be6ad8ce99d5`  
		Last Modified: Tue, 16 Apr 2024 02:12:31 GMT  
		Size: 1.1 MB (1061815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:10c849400e59d70fd0382b5451aff7f989e32640d4abb0afbc11e4cd93f120ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251966661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5231a09af0bed0887118754f7797c9ed15471a9b98876bae2afd0f72656b6ca2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 03:59:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68cf2dcea72a76f4194585b5fe94ebc6ceed16911250d44186a9f060b3e832d`  
		Last Modified: Tue, 16 Apr 2024 04:28:03 GMT  
		Size: 45.2 MB (45207668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5333b432eed5e9067399472b766459ecaab72e2d23c9d5fd42d70f4275594`  
		Last Modified: Tue, 16 Apr 2024 04:27:57 GMT  
		Size: 320.4 KB (320355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f6a82e2dc62e74bac15cfaa0678c5f0076676fd02435d94d9e26f7a92bca`  
		Last Modified: Tue, 16 Apr 2024 04:27:58 GMT  
		Size: 1.1 MB (1115135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:114d2e20f05b10e5817f3b749ef94f361a33e503c991e019ec4dff0b2b1fef20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d1e196ff69ec963adbb02205932140ad2bfa60648356c457ea3a5f9ad4ae4bc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212334162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713ee668ee8724c7d1e6c9005232dd20b3c0c64ff3548c66ca0afde66ee2ebc5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:c6f2b37a82320fa4fc45681e4bbaa7e30ee1003e1ce14983f852c4ecd648f0fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187951250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff102039bcae610ae2e322091be6a93bffcf28d49fd1b07cb28bf61ccc5f7e4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e681636c6d110834bb7020010a7d8c300f8e8604c6f3553babf82a0e6f70e339
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205323503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81412ffff8171740fe1719a5b808d20715becbfc29f663ab4e7c8e11a559dbf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:114d2e20f05b10e5817f3b749ef94f361a33e503c991e019ec4dff0b2b1fef20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:d1e196ff69ec963adbb02205932140ad2bfa60648356c457ea3a5f9ad4ae4bc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212334162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713ee668ee8724c7d1e6c9005232dd20b3c0c64ff3548c66ca0afde66ee2ebc5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:c6f2b37a82320fa4fc45681e4bbaa7e30ee1003e1ce14983f852c4ecd648f0fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187951250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff102039bcae610ae2e322091be6a93bffcf28d49fd1b07cb28bf61ccc5f7e4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e681636c6d110834bb7020010a7d8c300f8e8604c6f3553babf82a0e6f70e339
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205323503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81412ffff8171740fe1719a5b808d20715becbfc29f663ab4e7c8e11a559dbf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:831fa3f0bb3667c510d945bccfa86847f67d807aaae74342a61bc3a983719f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:006f1bf0463e6ceed83c958309755351388938b38488eec5869304b1fa472357
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297362221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769f9a27571ab5dd3d244ea50e1dc3d8f483b144edad110b1ed6f11d7aea2abc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:14:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:14:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:14:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6f4b1b2354371c3b3662f463dc6cea88bf654b1fcbfb21b79391736e633de`  
		Last Modified: Tue, 16 Apr 2024 06:32:02 GMT  
		Size: 114.4 MB (114384650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660034266ff49dea642e331c01516c78c452605d29ea904978898465cba6c041`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 308.3 KB (308319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5f31453040c4a6ec4d9aa45f377ca84e64ab9aadc50bb0f5bf265e4a50ec7`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cac77dcdb816a2bf142cc9fd94c312e1e1aaacf48147b55c853774c1c62d40`  
		Last Modified: Tue, 16 Apr 2024 06:31:50 GMT  
		Size: 24.4 MB (24443788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:000b81e6da49e1f0256da726cc181f63fc32a0f78e39a324f0fe102d0ca46b58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261285551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadf267e725c3e714572c03a376080374c097e2dc8c0ce3bbc0284bcede79b44`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:41:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22617ce11378da240c6c3c2d18629fda2e590c45b400e949a44d573d6a253b6`  
		Last Modified: Wed, 06 Mar 2024 04:52:18 GMT  
		Size: 82.8 MB (82847601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ff893af2fe38cffe84ae31fb677aee96349177f954359202fd1afcdf4369a9`  
		Last Modified: Wed, 06 Mar 2024 04:52:09 GMT  
		Size: 290.6 KB (290613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f60849007555690da1a453d4d2f31d579c5d33baa9b38ffa06965f26253d68`  
		Last Modified: Wed, 06 Mar 2024 04:52:08 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14bdb55b7e2e569bf3e0be77e1de5a0c4a81597776cd6bada36fe0a393dd18`  
		Last Modified: Wed, 06 Mar 2024 04:52:13 GMT  
		Size: 23.1 MB (23101809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:83e35c16711e1aeca1d751b1d44f59e6ceee3100b6699e233c8b78b3a63093d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:2b4095ccbaa7b360055d1e33f65605db23a23b4c5c63d13667878b802f1e4063
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1033040266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ebe5f2366c7a7fd00ab88d976e433afc37e0f6112cfba9f9aaba137b9aee01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:14:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:14:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:14:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:22:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6f4b1b2354371c3b3662f463dc6cea88bf654b1fcbfb21b79391736e633de`  
		Last Modified: Tue, 16 Apr 2024 06:32:02 GMT  
		Size: 114.4 MB (114384650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660034266ff49dea642e331c01516c78c452605d29ea904978898465cba6c041`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 308.3 KB (308319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5f31453040c4a6ec4d9aa45f377ca84e64ab9aadc50bb0f5bf265e4a50ec7`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cac77dcdb816a2bf142cc9fd94c312e1e1aaacf48147b55c853774c1c62d40`  
		Last Modified: Tue, 16 Apr 2024 06:31:50 GMT  
		Size: 24.4 MB (24443788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e69740ba09b1706be29844449e22b0006825b2ef9afcb606ca9c37d7ac125`  
		Last Modified: Tue, 16 Apr 2024 06:33:48 GMT  
		Size: 735.7 MB (735678045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4259d9b103503475428d4989db5e3e204a5ed983f858367c7f7d2a5546ec9677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921511052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faf749378f7d3c487285ab57195a30d81fb923b7ffa5c69912330704323541`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:41:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:43:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22617ce11378da240c6c3c2d18629fda2e590c45b400e949a44d573d6a253b6`  
		Last Modified: Wed, 06 Mar 2024 04:52:18 GMT  
		Size: 82.8 MB (82847601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ff893af2fe38cffe84ae31fb677aee96349177f954359202fd1afcdf4369a9`  
		Last Modified: Wed, 06 Mar 2024 04:52:09 GMT  
		Size: 290.6 KB (290613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f60849007555690da1a453d4d2f31d579c5d33baa9b38ffa06965f26253d68`  
		Last Modified: Wed, 06 Mar 2024 04:52:08 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14bdb55b7e2e569bf3e0be77e1de5a0c4a81597776cd6bada36fe0a393dd18`  
		Last Modified: Wed, 06 Mar 2024 04:52:13 GMT  
		Size: 23.1 MB (23101809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6ab0121874393f8ac4aa565f897b4fdb4b5b30e2d98fc102a4e7140944e6e`  
		Last Modified: Wed, 06 Mar 2024 04:53:52 GMT  
		Size: 660.2 MB (660225501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:f6f5745c356ea8c451fd1ae323968d7840a1301092164eb691980d188c632c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:2b4095ccbaa7b360055d1e33f65605db23a23b4c5c63d13667878b802f1e4063
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1033040266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ebe5f2366c7a7fd00ab88d976e433afc37e0f6112cfba9f9aaba137b9aee01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:14:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:14:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:14:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:22:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6f4b1b2354371c3b3662f463dc6cea88bf654b1fcbfb21b79391736e633de`  
		Last Modified: Tue, 16 Apr 2024 06:32:02 GMT  
		Size: 114.4 MB (114384650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660034266ff49dea642e331c01516c78c452605d29ea904978898465cba6c041`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 308.3 KB (308319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5f31453040c4a6ec4d9aa45f377ca84e64ab9aadc50bb0f5bf265e4a50ec7`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cac77dcdb816a2bf142cc9fd94c312e1e1aaacf48147b55c853774c1c62d40`  
		Last Modified: Tue, 16 Apr 2024 06:31:50 GMT  
		Size: 24.4 MB (24443788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e69740ba09b1706be29844449e22b0006825b2ef9afcb606ca9c37d7ac125`  
		Last Modified: Tue, 16 Apr 2024 06:33:48 GMT  
		Size: 735.7 MB (735678045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:831fa3f0bb3667c510d945bccfa86847f67d807aaae74342a61bc3a983719f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:006f1bf0463e6ceed83c958309755351388938b38488eec5869304b1fa472357
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297362221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769f9a27571ab5dd3d244ea50e1dc3d8f483b144edad110b1ed6f11d7aea2abc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:14:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:14:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:14:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6f4b1b2354371c3b3662f463dc6cea88bf654b1fcbfb21b79391736e633de`  
		Last Modified: Tue, 16 Apr 2024 06:32:02 GMT  
		Size: 114.4 MB (114384650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660034266ff49dea642e331c01516c78c452605d29ea904978898465cba6c041`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 308.3 KB (308319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5f31453040c4a6ec4d9aa45f377ca84e64ab9aadc50bb0f5bf265e4a50ec7`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cac77dcdb816a2bf142cc9fd94c312e1e1aaacf48147b55c853774c1c62d40`  
		Last Modified: Tue, 16 Apr 2024 06:31:50 GMT  
		Size: 24.4 MB (24443788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:000b81e6da49e1f0256da726cc181f63fc32a0f78e39a324f0fe102d0ca46b58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261285551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadf267e725c3e714572c03a376080374c097e2dc8c0ce3bbc0284bcede79b44`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:41:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22617ce11378da240c6c3c2d18629fda2e590c45b400e949a44d573d6a253b6`  
		Last Modified: Wed, 06 Mar 2024 04:52:18 GMT  
		Size: 82.8 MB (82847601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ff893af2fe38cffe84ae31fb677aee96349177f954359202fd1afcdf4369a9`  
		Last Modified: Wed, 06 Mar 2024 04:52:09 GMT  
		Size: 290.6 KB (290613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f60849007555690da1a453d4d2f31d579c5d33baa9b38ffa06965f26253d68`  
		Last Modified: Wed, 06 Mar 2024 04:52:08 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14bdb55b7e2e569bf3e0be77e1de5a0c4a81597776cd6bada36fe0a393dd18`  
		Last Modified: Wed, 06 Mar 2024 04:52:13 GMT  
		Size: 23.1 MB (23101809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:0e50cf8105d52c67fc8413a1cc5984d0c7fd87bc551babc66ffe01d5a2304b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:006f1bf0463e6ceed83c958309755351388938b38488eec5869304b1fa472357
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297362221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769f9a27571ab5dd3d244ea50e1dc3d8f483b144edad110b1ed6f11d7aea2abc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:14:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:14:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:14:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6f4b1b2354371c3b3662f463dc6cea88bf654b1fcbfb21b79391736e633de`  
		Last Modified: Tue, 16 Apr 2024 06:32:02 GMT  
		Size: 114.4 MB (114384650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660034266ff49dea642e331c01516c78c452605d29ea904978898465cba6c041`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 308.3 KB (308319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5f31453040c4a6ec4d9aa45f377ca84e64ab9aadc50bb0f5bf265e4a50ec7`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cac77dcdb816a2bf142cc9fd94c312e1e1aaacf48147b55c853774c1c62d40`  
		Last Modified: Tue, 16 Apr 2024 06:31:50 GMT  
		Size: 24.4 MB (24443788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:1bf08093555c25f69101e6325b4a71c1363d23c3fae35d64b53f5cc23909ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:33936969862bd17bb1275c212cd7c459d51a0ae92d4c7e6782c1922963d6e383
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158222987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecaba7eafbffdb4d8e3f7d8ceb3d7285ce65e384f6a50f79f43349b0127c907`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5d4d17f39682d3bfd32d842801e2909be503388975252d5bb46ef68a3166724a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155043033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea638ed33f92eaf96d9e2509eca402a6fed2eab43244bddac1719f86ba1a51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:bd4a6fba256bcfd01e04a2a7879f63caabce80ec9d0507ad086ea67050bf2eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:33936969862bd17bb1275c212cd7c459d51a0ae92d4c7e6782c1922963d6e383
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158222987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecaba7eafbffdb4d8e3f7d8ceb3d7285ce65e384f6a50f79f43349b0127c907`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
