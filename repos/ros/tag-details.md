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
$ docker pull ros@sha256:e1af917f820be2e14ebacd00e503b3f40b1287e89119391e45873c98e61e45c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:d6574666fdd21d19b03ff6076d1bccac9acd2193ca59ce66ee813c27fe0a393a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262575654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf306e26ba0843f5d704692b8b327249e5db63f982ad7fd7ea6903e7677439b2`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc3f3fda5033a747f4a1ec31069170d4ca68a86959654bd6d66aa04d272005b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 1.2 MB (1207573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9d8461cf4a7456a6bb953604596f7705b4d671b209d38e4cc6679e4a40a52b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 3.6 MB (3625025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9d2f77ec1a79d387e31fbbd4f09afe459288d5d31a37e070d9ed20fa7aa77b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b473f6b69e3e1138f395fcc51ad215c50c1ff082c4ac233cd667d2314eba451`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7736667635de13df8ee65e968cfe0f8a29613c479af29c0b81cab777c7f56bae`  
		Last Modified: Tue, 04 Feb 2025 04:31:24 GMT  
		Size: 106.6 MB (106612459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e07623aac56c94d57a3409f91154f7e37f058d58ac7a3bfda82734fd192f5c`  
		Last Modified: Tue, 04 Feb 2025 04:31:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726033011fa4e598cf994e76eb5f8a6b8d23167836e44f1314d7b99effc07c17`  
		Last Modified: Tue, 04 Feb 2025 05:26:55 GMT  
		Size: 98.0 MB (97950928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c5691fcc72019ac31a877904b867333878f615e5cbcba3c315c11b06937a9`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 349.5 KB (349547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ac1ca67067e3dfa4c16b9e13f64baa5dad4e6b1edd27a7b3eaa440be7d325`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ea86b324fe2cda680c1dd3831bb148b05ba29045c2c331f1e7e1a51ea7e343`  
		Last Modified: Tue, 04 Feb 2025 05:26:54 GMT  
		Size: 23.3 MB (23289302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:752706dc193c7b4440c127acad7a083f961ba7a50e54600392df5edcc127ca08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22916182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8852f7e5f9bbec4c1fdadb4afe5efa5d091707658ebe42c6ed00796d111736`

```dockerfile
```

-	Layers:
	-	`sha256:6419770c864e6c71920561349fe82f8e03a1c41204b5d6f5be71cd244ab75c6f`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 22.9 MB (22899026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd662c2bacad1d1e39bc1232c3cddedb4e1b52df4fa76082051ca0c11a62346c`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ca05128afeb4e4f0d38f0f070825224dcee2c0267787324cc83a514eec9cb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255013436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae24e7f3083145188e9a54e82aaae6847935def7ec05645d07c20f1af24e6c45`
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
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f491672b4b85aa805dff5d8975f4622301f42ca0a3c1d30101ad344e29dfdaed`  
		Last Modified: Tue, 04 Feb 2025 14:45:30 GMT  
		Size: 104.3 MB (104317718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe65565d1bb8cecba8a32487fd77ed001f41c465c3620d4d37906559a0a176f`  
		Last Modified: Tue, 04 Feb 2025 14:45:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c846ed6e7090aaa2ccff9e11e01c5b9378e709da84f1c2ffec0d4f61a156079`  
		Last Modified: Tue, 04 Feb 2025 22:00:32 GMT  
		Size: 95.5 MB (95503766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8a1e693ddbe548da76d4517f817b1b21ea2d1369cb638dcf03834e35617b0`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 349.6 KB (349572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f23a74087b67d1aa71de7e1b3ae636d64b8f51624905cfa1f259e8fa063ae`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bff3d112e4aa5c0ed4b3bc5f8861d5f256d8e26c812aae599c9990aa9eb612`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.7 MB (22675669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:87bf0341b684c5d1dd3a4f388d3b0c88435f39b67409374d43f50e25f4b99020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22929335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b95eca43db85d42679163104a70bf50de818bbad157bde6ca5bb473017e54f`

```dockerfile
```

-	Layers:
	-	`sha256:fbfb10bd3842c990dc808dde2f7c3b1b7e40de9c6fd4ac61249b25fd83b4b6fe`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.9 MB (22912042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ca9a39c3cfdf84f0e435c61e6c4d11158737219ec616d3f56fd636f54012c8`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:80dfc9ff2ada919636ef0038dbb65a8b24ef89ac4cd8126bf59271f743033966
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:c77eda74a754d4c524cec964915039e03d481d1ea48c4910d574bcd767866a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.6 MB (954581186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cbd73b8471c0fd212efc2644580e776706062de6f04228783f2c19b6caa5de`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc3f3fda5033a747f4a1ec31069170d4ca68a86959654bd6d66aa04d272005b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 1.2 MB (1207573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9d8461cf4a7456a6bb953604596f7705b4d671b209d38e4cc6679e4a40a52b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 3.6 MB (3625025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9d2f77ec1a79d387e31fbbd4f09afe459288d5d31a37e070d9ed20fa7aa77b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b473f6b69e3e1138f395fcc51ad215c50c1ff082c4ac233cd667d2314eba451`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7736667635de13df8ee65e968cfe0f8a29613c479af29c0b81cab777c7f56bae`  
		Last Modified: Tue, 04 Feb 2025 04:31:24 GMT  
		Size: 106.6 MB (106612459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e07623aac56c94d57a3409f91154f7e37f058d58ac7a3bfda82734fd192f5c`  
		Last Modified: Tue, 04 Feb 2025 04:31:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726033011fa4e598cf994e76eb5f8a6b8d23167836e44f1314d7b99effc07c17`  
		Last Modified: Tue, 04 Feb 2025 05:26:55 GMT  
		Size: 98.0 MB (97950928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c5691fcc72019ac31a877904b867333878f615e5cbcba3c315c11b06937a9`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 349.5 KB (349547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ac1ca67067e3dfa4c16b9e13f64baa5dad4e6b1edd27a7b3eaa440be7d325`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ea86b324fe2cda680c1dd3831bb148b05ba29045c2c331f1e7e1a51ea7e343`  
		Last Modified: Tue, 04 Feb 2025 05:26:54 GMT  
		Size: 23.3 MB (23289302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a6b09646f76213c67e7350a4fbcdd52eaccbc8f206176889cbd3e8b710a980`  
		Last Modified: Tue, 04 Feb 2025 06:17:58 GMT  
		Size: 692.0 MB (692005532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3f1cb5744e995ac50d50567d00be2bc562e418c4731d34aedb59a06718a56b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f15e3e884574297f7362f78f25aa08797030d4f25475f10236a64c72b18d59d`

```dockerfile
```

-	Layers:
	-	`sha256:a9c593a5d46786265686afa39d31e616e1b59194117bfd83164e5edc467d1d51`  
		Last Modified: Tue, 04 Feb 2025 06:17:42 GMT  
		Size: 57.5 MB (57523657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c834d3825c60c3fba606890e49af93371922552a4be5bd15f488e602ae4897b`  
		Last Modified: Tue, 04 Feb 2025 06:17:41 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ce9fce651b1b7e57892cc37e93c5da5f239190177099afc7b611e05b7974a745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.1 MB (915116387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898051f2cffb2ceccfb65e03d0f98eb82dad71571a1c9cc4f91758a444e60560`
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
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f491672b4b85aa805dff5d8975f4622301f42ca0a3c1d30101ad344e29dfdaed`  
		Last Modified: Tue, 04 Feb 2025 14:45:30 GMT  
		Size: 104.3 MB (104317718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe65565d1bb8cecba8a32487fd77ed001f41c465c3620d4d37906559a0a176f`  
		Last Modified: Tue, 04 Feb 2025 14:45:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c846ed6e7090aaa2ccff9e11e01c5b9378e709da84f1c2ffec0d4f61a156079`  
		Last Modified: Tue, 04 Feb 2025 22:00:32 GMT  
		Size: 95.5 MB (95503766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8a1e693ddbe548da76d4517f817b1b21ea2d1369cb638dcf03834e35617b0`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 349.6 KB (349572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f23a74087b67d1aa71de7e1b3ae636d64b8f51624905cfa1f259e8fa063ae`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bff3d112e4aa5c0ed4b3bc5f8861d5f256d8e26c812aae599c9990aa9eb612`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.7 MB (22675669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ebccbb27f9e1f73d9824c54daf871d05341b4be32713f2dc771e3743f61eb7`  
		Last Modified: Wed, 05 Feb 2025 03:36:09 GMT  
		Size: 660.1 MB (660102951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:49cd1b5b344e78a9014f5441dfe07f42965f5c4496dde4955ce208ba9e23531e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57529274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112163f8855b0f4e19fb3c1ea11699fd1a76d7e33f205e4c4f724b111e4e06ab`

```dockerfile
```

-	Layers:
	-	`sha256:e9f3ae10bbe313c74ffae3e1decaa1f5f5f2595033f296e791ae6a2e10335dcf`  
		Last Modified: Wed, 05 Feb 2025 03:35:57 GMT  
		Size: 57.5 MB (57519493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b24f7262d56db1c673fc662100487d109df41caf53abfdeba906ee647a70bf1`  
		Last Modified: Wed, 05 Feb 2025 03:35:55 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:80dfc9ff2ada919636ef0038dbb65a8b24ef89ac4cd8126bf59271f743033966
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c77eda74a754d4c524cec964915039e03d481d1ea48c4910d574bcd767866a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.6 MB (954581186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cbd73b8471c0fd212efc2644580e776706062de6f04228783f2c19b6caa5de`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc3f3fda5033a747f4a1ec31069170d4ca68a86959654bd6d66aa04d272005b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 1.2 MB (1207573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9d8461cf4a7456a6bb953604596f7705b4d671b209d38e4cc6679e4a40a52b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 3.6 MB (3625025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9d2f77ec1a79d387e31fbbd4f09afe459288d5d31a37e070d9ed20fa7aa77b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b473f6b69e3e1138f395fcc51ad215c50c1ff082c4ac233cd667d2314eba451`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7736667635de13df8ee65e968cfe0f8a29613c479af29c0b81cab777c7f56bae`  
		Last Modified: Tue, 04 Feb 2025 04:31:24 GMT  
		Size: 106.6 MB (106612459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e07623aac56c94d57a3409f91154f7e37f058d58ac7a3bfda82734fd192f5c`  
		Last Modified: Tue, 04 Feb 2025 04:31:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726033011fa4e598cf994e76eb5f8a6b8d23167836e44f1314d7b99effc07c17`  
		Last Modified: Tue, 04 Feb 2025 05:26:55 GMT  
		Size: 98.0 MB (97950928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c5691fcc72019ac31a877904b867333878f615e5cbcba3c315c11b06937a9`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 349.5 KB (349547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ac1ca67067e3dfa4c16b9e13f64baa5dad4e6b1edd27a7b3eaa440be7d325`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ea86b324fe2cda680c1dd3831bb148b05ba29045c2c331f1e7e1a51ea7e343`  
		Last Modified: Tue, 04 Feb 2025 05:26:54 GMT  
		Size: 23.3 MB (23289302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a6b09646f76213c67e7350a4fbcdd52eaccbc8f206176889cbd3e8b710a980`  
		Last Modified: Tue, 04 Feb 2025 06:17:58 GMT  
		Size: 692.0 MB (692005532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:3f1cb5744e995ac50d50567d00be2bc562e418c4731d34aedb59a06718a56b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f15e3e884574297f7362f78f25aa08797030d4f25475f10236a64c72b18d59d`

```dockerfile
```

-	Layers:
	-	`sha256:a9c593a5d46786265686afa39d31e616e1b59194117bfd83164e5edc467d1d51`  
		Last Modified: Tue, 04 Feb 2025 06:17:42 GMT  
		Size: 57.5 MB (57523657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c834d3825c60c3fba606890e49af93371922552a4be5bd15f488e602ae4897b`  
		Last Modified: Tue, 04 Feb 2025 06:17:41 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ce9fce651b1b7e57892cc37e93c5da5f239190177099afc7b611e05b7974a745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.1 MB (915116387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898051f2cffb2ceccfb65e03d0f98eb82dad71571a1c9cc4f91758a444e60560`
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
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f491672b4b85aa805dff5d8975f4622301f42ca0a3c1d30101ad344e29dfdaed`  
		Last Modified: Tue, 04 Feb 2025 14:45:30 GMT  
		Size: 104.3 MB (104317718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe65565d1bb8cecba8a32487fd77ed001f41c465c3620d4d37906559a0a176f`  
		Last Modified: Tue, 04 Feb 2025 14:45:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c846ed6e7090aaa2ccff9e11e01c5b9378e709da84f1c2ffec0d4f61a156079`  
		Last Modified: Tue, 04 Feb 2025 22:00:32 GMT  
		Size: 95.5 MB (95503766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8a1e693ddbe548da76d4517f817b1b21ea2d1369cb638dcf03834e35617b0`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 349.6 KB (349572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f23a74087b67d1aa71de7e1b3ae636d64b8f51624905cfa1f259e8fa063ae`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bff3d112e4aa5c0ed4b3bc5f8861d5f256d8e26c812aae599c9990aa9eb612`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.7 MB (22675669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ebccbb27f9e1f73d9824c54daf871d05341b4be32713f2dc771e3743f61eb7`  
		Last Modified: Wed, 05 Feb 2025 03:36:09 GMT  
		Size: 660.1 MB (660102951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:49cd1b5b344e78a9014f5441dfe07f42965f5c4496dde4955ce208ba9e23531e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57529274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112163f8855b0f4e19fb3c1ea11699fd1a76d7e33f205e4c4f724b111e4e06ab`

```dockerfile
```

-	Layers:
	-	`sha256:e9f3ae10bbe313c74ffae3e1decaa1f5f5f2595033f296e791ae6a2e10335dcf`  
		Last Modified: Wed, 05 Feb 2025 03:35:57 GMT  
		Size: 57.5 MB (57519493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b24f7262d56db1c673fc662100487d109df41caf53abfdeba906ee647a70bf1`  
		Last Modified: Wed, 05 Feb 2025 03:35:55 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:e1af917f820be2e14ebacd00e503b3f40b1287e89119391e45873c98e61e45c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d6574666fdd21d19b03ff6076d1bccac9acd2193ca59ce66ee813c27fe0a393a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262575654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf306e26ba0843f5d704692b8b327249e5db63f982ad7fd7ea6903e7677439b2`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc3f3fda5033a747f4a1ec31069170d4ca68a86959654bd6d66aa04d272005b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 1.2 MB (1207573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9d8461cf4a7456a6bb953604596f7705b4d671b209d38e4cc6679e4a40a52b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 3.6 MB (3625025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9d2f77ec1a79d387e31fbbd4f09afe459288d5d31a37e070d9ed20fa7aa77b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b473f6b69e3e1138f395fcc51ad215c50c1ff082c4ac233cd667d2314eba451`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7736667635de13df8ee65e968cfe0f8a29613c479af29c0b81cab777c7f56bae`  
		Last Modified: Tue, 04 Feb 2025 04:31:24 GMT  
		Size: 106.6 MB (106612459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e07623aac56c94d57a3409f91154f7e37f058d58ac7a3bfda82734fd192f5c`  
		Last Modified: Tue, 04 Feb 2025 04:31:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726033011fa4e598cf994e76eb5f8a6b8d23167836e44f1314d7b99effc07c17`  
		Last Modified: Tue, 04 Feb 2025 05:26:55 GMT  
		Size: 98.0 MB (97950928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c5691fcc72019ac31a877904b867333878f615e5cbcba3c315c11b06937a9`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 349.5 KB (349547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ac1ca67067e3dfa4c16b9e13f64baa5dad4e6b1edd27a7b3eaa440be7d325`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ea86b324fe2cda680c1dd3831bb148b05ba29045c2c331f1e7e1a51ea7e343`  
		Last Modified: Tue, 04 Feb 2025 05:26:54 GMT  
		Size: 23.3 MB (23289302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:752706dc193c7b4440c127acad7a083f961ba7a50e54600392df5edcc127ca08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22916182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8852f7e5f9bbec4c1fdadb4afe5efa5d091707658ebe42c6ed00796d111736`

```dockerfile
```

-	Layers:
	-	`sha256:6419770c864e6c71920561349fe82f8e03a1c41204b5d6f5be71cd244ab75c6f`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 22.9 MB (22899026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd662c2bacad1d1e39bc1232c3cddedb4e1b52df4fa76082051ca0c11a62346c`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ca05128afeb4e4f0d38f0f070825224dcee2c0267787324cc83a514eec9cb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255013436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae24e7f3083145188e9a54e82aaae6847935def7ec05645d07c20f1af24e6c45`
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
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f491672b4b85aa805dff5d8975f4622301f42ca0a3c1d30101ad344e29dfdaed`  
		Last Modified: Tue, 04 Feb 2025 14:45:30 GMT  
		Size: 104.3 MB (104317718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe65565d1bb8cecba8a32487fd77ed001f41c465c3620d4d37906559a0a176f`  
		Last Modified: Tue, 04 Feb 2025 14:45:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c846ed6e7090aaa2ccff9e11e01c5b9378e709da84f1c2ffec0d4f61a156079`  
		Last Modified: Tue, 04 Feb 2025 22:00:32 GMT  
		Size: 95.5 MB (95503766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8a1e693ddbe548da76d4517f817b1b21ea2d1369cb638dcf03834e35617b0`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 349.6 KB (349572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f23a74087b67d1aa71de7e1b3ae636d64b8f51624905cfa1f259e8fa063ae`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bff3d112e4aa5c0ed4b3bc5f8861d5f256d8e26c812aae599c9990aa9eb612`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.7 MB (22675669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:87bf0341b684c5d1dd3a4f388d3b0c88435f39b67409374d43f50e25f4b99020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22929335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b95eca43db85d42679163104a70bf50de818bbad157bde6ca5bb473017e54f`

```dockerfile
```

-	Layers:
	-	`sha256:fbfb10bd3842c990dc808dde2f7c3b1b7e40de9c6fd4ac61249b25fd83b4b6fe`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.9 MB (22912042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ca9a39c3cfdf84f0e435c61e6c4d11158737219ec616d3f56fd636f54012c8`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:e1af917f820be2e14ebacd00e503b3f40b1287e89119391e45873c98e61e45c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:d6574666fdd21d19b03ff6076d1bccac9acd2193ca59ce66ee813c27fe0a393a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262575654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf306e26ba0843f5d704692b8b327249e5db63f982ad7fd7ea6903e7677439b2`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc3f3fda5033a747f4a1ec31069170d4ca68a86959654bd6d66aa04d272005b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 1.2 MB (1207573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9d8461cf4a7456a6bb953604596f7705b4d671b209d38e4cc6679e4a40a52b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 3.6 MB (3625025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9d2f77ec1a79d387e31fbbd4f09afe459288d5d31a37e070d9ed20fa7aa77b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b473f6b69e3e1138f395fcc51ad215c50c1ff082c4ac233cd667d2314eba451`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7736667635de13df8ee65e968cfe0f8a29613c479af29c0b81cab777c7f56bae`  
		Last Modified: Tue, 04 Feb 2025 04:31:24 GMT  
		Size: 106.6 MB (106612459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e07623aac56c94d57a3409f91154f7e37f058d58ac7a3bfda82734fd192f5c`  
		Last Modified: Tue, 04 Feb 2025 04:31:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726033011fa4e598cf994e76eb5f8a6b8d23167836e44f1314d7b99effc07c17`  
		Last Modified: Tue, 04 Feb 2025 05:26:55 GMT  
		Size: 98.0 MB (97950928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c5691fcc72019ac31a877904b867333878f615e5cbcba3c315c11b06937a9`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 349.5 KB (349547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ac1ca67067e3dfa4c16b9e13f64baa5dad4e6b1edd27a7b3eaa440be7d325`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ea86b324fe2cda680c1dd3831bb148b05ba29045c2c331f1e7e1a51ea7e343`  
		Last Modified: Tue, 04 Feb 2025 05:26:54 GMT  
		Size: 23.3 MB (23289302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:752706dc193c7b4440c127acad7a083f961ba7a50e54600392df5edcc127ca08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22916182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8852f7e5f9bbec4c1fdadb4afe5efa5d091707658ebe42c6ed00796d111736`

```dockerfile
```

-	Layers:
	-	`sha256:6419770c864e6c71920561349fe82f8e03a1c41204b5d6f5be71cd244ab75c6f`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 22.9 MB (22899026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd662c2bacad1d1e39bc1232c3cddedb4e1b52df4fa76082051ca0c11a62346c`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ca05128afeb4e4f0d38f0f070825224dcee2c0267787324cc83a514eec9cb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255013436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae24e7f3083145188e9a54e82aaae6847935def7ec05645d07c20f1af24e6c45`
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
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f491672b4b85aa805dff5d8975f4622301f42ca0a3c1d30101ad344e29dfdaed`  
		Last Modified: Tue, 04 Feb 2025 14:45:30 GMT  
		Size: 104.3 MB (104317718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe65565d1bb8cecba8a32487fd77ed001f41c465c3620d4d37906559a0a176f`  
		Last Modified: Tue, 04 Feb 2025 14:45:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c846ed6e7090aaa2ccff9e11e01c5b9378e709da84f1c2ffec0d4f61a156079`  
		Last Modified: Tue, 04 Feb 2025 22:00:32 GMT  
		Size: 95.5 MB (95503766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8a1e693ddbe548da76d4517f817b1b21ea2d1369cb638dcf03834e35617b0`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 349.6 KB (349572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f23a74087b67d1aa71de7e1b3ae636d64b8f51624905cfa1f259e8fa063ae`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bff3d112e4aa5c0ed4b3bc5f8861d5f256d8e26c812aae599c9990aa9eb612`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.7 MB (22675669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:87bf0341b684c5d1dd3a4f388d3b0c88435f39b67409374d43f50e25f4b99020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22929335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b95eca43db85d42679163104a70bf50de818bbad157bde6ca5bb473017e54f`

```dockerfile
```

-	Layers:
	-	`sha256:fbfb10bd3842c990dc808dde2f7c3b1b7e40de9c6fd4ac61249b25fd83b4b6fe`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.9 MB (22912042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ca9a39c3cfdf84f0e435c61e6c4d11158737219ec616d3f56fd636f54012c8`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:a2612da764af45e1fb38fc028f3113b779e8507f5e556b0a143372923f3aa6bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:8dbe3a67254c3073c19943c5049e72be6db9154e56d322a97818020b2f4dd488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148433552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f616bd18c3e5d9a943349a67f47bf70317850a5a9dc38c9d4177109ba3523e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6a79aeb6571349bd0ed39d022974bd75ce6cd8a8fb16abc081979f49eb047c`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 1.2 MB (1208095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad511e33582dd506cff877292e878fa641e74fc75c6b05d646f02a8591ff6375`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 3.6 MB (3625056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cae3cbe2ca7852f81be5faded91257ec73279265656d13ab374d2b575abf05`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea7840eaa99bd262f11e2fa84632a1f7ba2a6fba94652d5e4272e9a11794793`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad57cd4eadaac8aeec4e7509e5fd14d30569d2e25cdba0bb834a763bf11cb3`  
		Last Modified: Mon, 10 Mar 2025 18:13:47 GMT  
		Size: 114.1 MB (114061990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82474f94165ca84f75e2d760c63690d4ca308855187afbce52058b83f50ffa2`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:db7bc0a5d05320fbb4906b521b8d9da6e26e8eb6aa864fc48cf860f1a6258994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17133639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4098d7e3151baba9cdb29a6965d49a3f9d8f3caf7fb650fea5cae0f12c6be86f`

```dockerfile
```

-	Layers:
	-	`sha256:b0ed53ba8e4cb459558b31ead673e25933ad751cfc63ad29fa9236fda2c50e81`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 17.1 MB (17117248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591723d676a96e3281e418b6f1804f8f194570ae0bf29867c2cf93f4ab2fac91`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3521cba9eba15ea916dee2f02c692e5af52c10d84769e3f2bb09b1dfc919393f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142687189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726e828639952a77e9eeb490bbea44ded50b44ab8515b7dd1c9eee7e7fbe5663`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:75dab6f34142165c2a7014caff86c9e91268128f1a8cff14670df263d25d5009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17120417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18837126796282060c11cff971e9b55d4ab1752e170a9094309e9e1625b30cfc`

```dockerfile
```

-	Layers:
	-	`sha256:ad99b5798d1abcb03974d78123cc03c460035f9e49766fb20e37edbd521f91e1`  
		Last Modified: Mon, 10 Mar 2025 18:24:53 GMT  
		Size: 17.1 MB (17103887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cbdadda0486228f4ed192372863450ac40e7982f64e3c33baf07d2ef3053737`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 16.5 KB (16530 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:a2612da764af45e1fb38fc028f3113b779e8507f5e556b0a143372923f3aa6bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:8dbe3a67254c3073c19943c5049e72be6db9154e56d322a97818020b2f4dd488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148433552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f616bd18c3e5d9a943349a67f47bf70317850a5a9dc38c9d4177109ba3523e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6a79aeb6571349bd0ed39d022974bd75ce6cd8a8fb16abc081979f49eb047c`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 1.2 MB (1208095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad511e33582dd506cff877292e878fa641e74fc75c6b05d646f02a8591ff6375`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 3.6 MB (3625056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cae3cbe2ca7852f81be5faded91257ec73279265656d13ab374d2b575abf05`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea7840eaa99bd262f11e2fa84632a1f7ba2a6fba94652d5e4272e9a11794793`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad57cd4eadaac8aeec4e7509e5fd14d30569d2e25cdba0bb834a763bf11cb3`  
		Last Modified: Mon, 10 Mar 2025 18:13:47 GMT  
		Size: 114.1 MB (114061990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82474f94165ca84f75e2d760c63690d4ca308855187afbce52058b83f50ffa2`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:db7bc0a5d05320fbb4906b521b8d9da6e26e8eb6aa864fc48cf860f1a6258994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17133639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4098d7e3151baba9cdb29a6965d49a3f9d8f3caf7fb650fea5cae0f12c6be86f`

```dockerfile
```

-	Layers:
	-	`sha256:b0ed53ba8e4cb459558b31ead673e25933ad751cfc63ad29fa9236fda2c50e81`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 17.1 MB (17117248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591723d676a96e3281e418b6f1804f8f194570ae0bf29867c2cf93f4ab2fac91`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3521cba9eba15ea916dee2f02c692e5af52c10d84769e3f2bb09b1dfc919393f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142687189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726e828639952a77e9eeb490bbea44ded50b44ab8515b7dd1c9eee7e7fbe5663`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:75dab6f34142165c2a7014caff86c9e91268128f1a8cff14670df263d25d5009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17120417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18837126796282060c11cff971e9b55d4ab1752e170a9094309e9e1625b30cfc`

```dockerfile
```

-	Layers:
	-	`sha256:ad99b5798d1abcb03974d78123cc03c460035f9e49766fb20e37edbd521f91e1`  
		Last Modified: Mon, 10 Mar 2025 18:24:53 GMT  
		Size: 17.1 MB (17103887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cbdadda0486228f4ed192372863450ac40e7982f64e3c33baf07d2ef3053737`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 16.5 KB (16530 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron`

```console
$ docker pull ros@sha256:337f4fbb7fe3dbcca1e11cb68b9c01c9960b69a304657b5c7a156252b563c3f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:632a5aac59584ab5bb0e06d04a5e39418ebf2353236fc015daa44a4b040b58d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267763467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922b59e7539bea06cab6e83e21efc0b8bcd0f082a25d2b72ac99056ee573c6b9`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84978cd4920dbb6ce11792e880709796810884d9945087cff06a0b57cf496ca`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 1.2 MB (1207606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8477dd187360dc43e3f8b3b9094455579676d805dba6e105e0bba7d5ff67cfb`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 3.6 MB (3625035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37fe4809b99d383618c439a60815c0606887006924f154f8fd0209d279bed7`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeae0ad7c3a66464a0e67535cabdddec74030230337cfcd74e28118e7096df9`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f68e1fb716a6f991cef2069792082fcf733f82146983818f7b61cb9254eef4`  
		Last Modified: Tue, 04 Feb 2025 04:32:53 GMT  
		Size: 124.4 MB (124355396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834eacd2fda9baf4d52ab0b35cf309f08a7ce54cc18714f117e36ffebf7f583`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526137aab8eabb030282d4cd36a82d84f0c98f7e226cf70b0a70555c16350261`  
		Last Modified: Tue, 04 Feb 2025 05:26:44 GMT  
		Size: 85.0 MB (84977086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e786d9035575d521ab8b98957006a642cdf3e9f87a7cc100de30768e0e494`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 321.9 KB (321949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449373c6d3c93d44e06855012381e095988cc78668a7d4e2295d11c598a245c`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86111058d79ae057cc88f50bad018887961928fe6dd06ef2cc66f303b0015c30`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23735561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:0f2a5c4bd2272c4809de2465576673b7e95bd96520b16ee5b47843a9bef7a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23735695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdb4edf36e22a3a5e107167f9c1cb525396ad29994ae7f103df6508c358bd83`

```dockerfile
```

-	Layers:
	-	`sha256:06d23bdd842d459cea3aaa27f2e94a10035256d473eba4ceec69a7c08d68ceaa`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23718572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246f9008e3f1ac54635b14820165dfc6645009b893dcbbc986ec4c678bb7f41d`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 17.1 KB (17123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1f93c23fd385eeb7f2448909022dcc705439832d58377e80170620a6b118ee62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260096340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116cf9176634313710c9c257bc70f0e67bfed60a08f586e83cf7eae4bff7fd2f`
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfece1d5df372ac2f8404edb6ab6f04310cb7578f9e31329eb26ebc084f487a`  
		Last Modified: Tue, 04 Feb 2025 14:47:10 GMT  
		Size: 121.8 MB (121825178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9250bf185b1a4c8850fefbdb740dcf3f379adf745c3255f7a8407fa0a57f1dc`  
		Last Modified: Tue, 04 Feb 2025 14:47:07 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ded77ac56df8a405c3c26852271748c1e71a81c45ee63a0d55740630ad56d7`  
		Last Modified: Tue, 04 Feb 2025 22:02:00 GMT  
		Size: 82.7 MB (82654236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4004f3b862a873c62b82c3b21e9865458c2c533493f0e0e9683cbe10414ede5a`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 322.0 KB (321974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d17c1a13e6b326395e65fd406b1ab982bb3aeaa3a440bb38ae18f1c0ff6175`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a6e0521a8e25a70f9ea7a1a52c29b5da861405a6379670fd3f6fead37eab0`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.1 MB (23128256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:e8c2fc9d83559f2f3e36e6c2a48cba90ce18ae2ea3ebf51a73551d24af38a5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23749032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44580c6c7f266f61f7649004fefe827613fafaaa442c70fac2c29752de442124`

```dockerfile
```

-	Layers:
	-	`sha256:97e6f5b1972232505dfe34e04419da2a3a4b4802daadce5e0f9b75cad636fa0e`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.7 MB (23731771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3772758b0b9985d008ab1a3526ed8e73d520fdc9ba11f7d6449da0679804aad`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-perception`

```console
$ docker pull ros@sha256:8bd0d32ba6aff214b8083ba10f14b50e9e5278cbdbffe0b40a98adf5a888b53b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:bc340a3623ebbd3fe5b54c34c93c08b4678162d06571ac9cecc2e22852f22011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.4 MB (960393789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dbff14113ebd665f83d451f89f83f9809940a0470ab6da67f6ec6eff650ba9`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84978cd4920dbb6ce11792e880709796810884d9945087cff06a0b57cf496ca`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 1.2 MB (1207606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8477dd187360dc43e3f8b3b9094455579676d805dba6e105e0bba7d5ff67cfb`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 3.6 MB (3625035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37fe4809b99d383618c439a60815c0606887006924f154f8fd0209d279bed7`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeae0ad7c3a66464a0e67535cabdddec74030230337cfcd74e28118e7096df9`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f68e1fb716a6f991cef2069792082fcf733f82146983818f7b61cb9254eef4`  
		Last Modified: Tue, 04 Feb 2025 04:32:53 GMT  
		Size: 124.4 MB (124355396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834eacd2fda9baf4d52ab0b35cf309f08a7ce54cc18714f117e36ffebf7f583`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526137aab8eabb030282d4cd36a82d84f0c98f7e226cf70b0a70555c16350261`  
		Last Modified: Tue, 04 Feb 2025 05:26:44 GMT  
		Size: 85.0 MB (84977086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e786d9035575d521ab8b98957006a642cdf3e9f87a7cc100de30768e0e494`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 321.9 KB (321949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449373c6d3c93d44e06855012381e095988cc78668a7d4e2295d11c598a245c`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86111058d79ae057cc88f50bad018887961928fe6dd06ef2cc66f303b0015c30`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23735561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da94dc45dbdb0078da869c53a65178d2d3219dcc8424b074f058e789baa6e6b2`  
		Last Modified: Tue, 04 Feb 2025 06:18:16 GMT  
		Size: 692.6 MB (692630322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3c89255c9843aee1e48386feaf02c878684785c8fbe4b7530c51c5ad44c8bd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58341315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b62dae043b9ba3c9b61b588fc794db708ef7c23f384f49aea7c2404c165824c`

```dockerfile
```

-	Layers:
	-	`sha256:be435e71cd61a6de7cdf9d95b7433d6f5e6ca4f82b9d309356d9c4a2454ce7b1`  
		Last Modified: Tue, 04 Feb 2025 06:18:00 GMT  
		Size: 58.3 MB (58331640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67565e969885c8068adb136f3586258dafdb8af3c56373d7132a137b939a6ab6`  
		Last Modified: Tue, 04 Feb 2025 06:17:58 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c2d646af6511ab428a2ba7117da03ca084621c34687c9aaa7570672765024156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.8 MB (920822770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17370a663650148bc07b68ff1b14d5ced6075680c25d322f40cd6918f883c96`
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfece1d5df372ac2f8404edb6ab6f04310cb7578f9e31329eb26ebc084f487a`  
		Last Modified: Tue, 04 Feb 2025 14:47:10 GMT  
		Size: 121.8 MB (121825178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9250bf185b1a4c8850fefbdb740dcf3f379adf745c3255f7a8407fa0a57f1dc`  
		Last Modified: Tue, 04 Feb 2025 14:47:07 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ded77ac56df8a405c3c26852271748c1e71a81c45ee63a0d55740630ad56d7`  
		Last Modified: Tue, 04 Feb 2025 22:02:00 GMT  
		Size: 82.7 MB (82654236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4004f3b862a873c62b82c3b21e9865458c2c533493f0e0e9683cbe10414ede5a`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 322.0 KB (321974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d17c1a13e6b326395e65fd406b1ab982bb3aeaa3a440bb38ae18f1c0ff6175`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a6e0521a8e25a70f9ea7a1a52c29b5da861405a6379670fd3f6fead37eab0`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.1 MB (23128256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015ec4af46888f62648318abad124a0d38a2737e066e7b246a8838cbc0f3114`  
		Last Modified: Wed, 05 Feb 2025 03:41:09 GMT  
		Size: 660.7 MB (660726430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:68d9f40c89126ca023d59f5a8387f9a0a5a8f732f332b2bd0aa8d12039ef1242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58337410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04468e939411fd563b8c55d6757a4cc3566d5833a9a14cb75d3a0ffa8809ad4`

```dockerfile
```

-	Layers:
	-	`sha256:35f150f237de2487144fab9d9b62f4b595dea43f3b95ad8c2da448722cf807ac`  
		Last Modified: Wed, 05 Feb 2025 03:40:58 GMT  
		Size: 58.3 MB (58327655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f507137f1eb5fdee1d4065c364e4477c5b82aa2279e9fc02fccf973cd4edd1e1`  
		Last Modified: Wed, 05 Feb 2025 03:40:56 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:8bd0d32ba6aff214b8083ba10f14b50e9e5278cbdbffe0b40a98adf5a888b53b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:bc340a3623ebbd3fe5b54c34c93c08b4678162d06571ac9cecc2e22852f22011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.4 MB (960393789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dbff14113ebd665f83d451f89f83f9809940a0470ab6da67f6ec6eff650ba9`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84978cd4920dbb6ce11792e880709796810884d9945087cff06a0b57cf496ca`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 1.2 MB (1207606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8477dd187360dc43e3f8b3b9094455579676d805dba6e105e0bba7d5ff67cfb`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 3.6 MB (3625035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37fe4809b99d383618c439a60815c0606887006924f154f8fd0209d279bed7`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeae0ad7c3a66464a0e67535cabdddec74030230337cfcd74e28118e7096df9`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f68e1fb716a6f991cef2069792082fcf733f82146983818f7b61cb9254eef4`  
		Last Modified: Tue, 04 Feb 2025 04:32:53 GMT  
		Size: 124.4 MB (124355396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834eacd2fda9baf4d52ab0b35cf309f08a7ce54cc18714f117e36ffebf7f583`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526137aab8eabb030282d4cd36a82d84f0c98f7e226cf70b0a70555c16350261`  
		Last Modified: Tue, 04 Feb 2025 05:26:44 GMT  
		Size: 85.0 MB (84977086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e786d9035575d521ab8b98957006a642cdf3e9f87a7cc100de30768e0e494`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 321.9 KB (321949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449373c6d3c93d44e06855012381e095988cc78668a7d4e2295d11c598a245c`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86111058d79ae057cc88f50bad018887961928fe6dd06ef2cc66f303b0015c30`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23735561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da94dc45dbdb0078da869c53a65178d2d3219dcc8424b074f058e789baa6e6b2`  
		Last Modified: Tue, 04 Feb 2025 06:18:16 GMT  
		Size: 692.6 MB (692630322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:3c89255c9843aee1e48386feaf02c878684785c8fbe4b7530c51c5ad44c8bd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58341315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b62dae043b9ba3c9b61b588fc794db708ef7c23f384f49aea7c2404c165824c`

```dockerfile
```

-	Layers:
	-	`sha256:be435e71cd61a6de7cdf9d95b7433d6f5e6ca4f82b9d309356d9c4a2454ce7b1`  
		Last Modified: Tue, 04 Feb 2025 06:18:00 GMT  
		Size: 58.3 MB (58331640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67565e969885c8068adb136f3586258dafdb8af3c56373d7132a137b939a6ab6`  
		Last Modified: Tue, 04 Feb 2025 06:17:58 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c2d646af6511ab428a2ba7117da03ca084621c34687c9aaa7570672765024156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.8 MB (920822770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17370a663650148bc07b68ff1b14d5ced6075680c25d322f40cd6918f883c96`
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfece1d5df372ac2f8404edb6ab6f04310cb7578f9e31329eb26ebc084f487a`  
		Last Modified: Tue, 04 Feb 2025 14:47:10 GMT  
		Size: 121.8 MB (121825178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9250bf185b1a4c8850fefbdb740dcf3f379adf745c3255f7a8407fa0a57f1dc`  
		Last Modified: Tue, 04 Feb 2025 14:47:07 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ded77ac56df8a405c3c26852271748c1e71a81c45ee63a0d55740630ad56d7`  
		Last Modified: Tue, 04 Feb 2025 22:02:00 GMT  
		Size: 82.7 MB (82654236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4004f3b862a873c62b82c3b21e9865458c2c533493f0e0e9683cbe10414ede5a`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 322.0 KB (321974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d17c1a13e6b326395e65fd406b1ab982bb3aeaa3a440bb38ae18f1c0ff6175`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a6e0521a8e25a70f9ea7a1a52c29b5da861405a6379670fd3f6fead37eab0`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.1 MB (23128256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015ec4af46888f62648318abad124a0d38a2737e066e7b246a8838cbc0f3114`  
		Last Modified: Wed, 05 Feb 2025 03:41:09 GMT  
		Size: 660.7 MB (660726430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:68d9f40c89126ca023d59f5a8387f9a0a5a8f732f332b2bd0aa8d12039ef1242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58337410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04468e939411fd563b8c55d6757a4cc3566d5833a9a14cb75d3a0ffa8809ad4`

```dockerfile
```

-	Layers:
	-	`sha256:35f150f237de2487144fab9d9b62f4b595dea43f3b95ad8c2da448722cf807ac`  
		Last Modified: Wed, 05 Feb 2025 03:40:58 GMT  
		Size: 58.3 MB (58327655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f507137f1eb5fdee1d4065c364e4477c5b82aa2279e9fc02fccf973cd4edd1e1`  
		Last Modified: Wed, 05 Feb 2025 03:40:56 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:337f4fbb7fe3dbcca1e11cb68b9c01c9960b69a304657b5c7a156252b563c3f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:632a5aac59584ab5bb0e06d04a5e39418ebf2353236fc015daa44a4b040b58d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267763467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922b59e7539bea06cab6e83e21efc0b8bcd0f082a25d2b72ac99056ee573c6b9`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84978cd4920dbb6ce11792e880709796810884d9945087cff06a0b57cf496ca`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 1.2 MB (1207606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8477dd187360dc43e3f8b3b9094455579676d805dba6e105e0bba7d5ff67cfb`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 3.6 MB (3625035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37fe4809b99d383618c439a60815c0606887006924f154f8fd0209d279bed7`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeae0ad7c3a66464a0e67535cabdddec74030230337cfcd74e28118e7096df9`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f68e1fb716a6f991cef2069792082fcf733f82146983818f7b61cb9254eef4`  
		Last Modified: Tue, 04 Feb 2025 04:32:53 GMT  
		Size: 124.4 MB (124355396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834eacd2fda9baf4d52ab0b35cf309f08a7ce54cc18714f117e36ffebf7f583`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526137aab8eabb030282d4cd36a82d84f0c98f7e226cf70b0a70555c16350261`  
		Last Modified: Tue, 04 Feb 2025 05:26:44 GMT  
		Size: 85.0 MB (84977086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e786d9035575d521ab8b98957006a642cdf3e9f87a7cc100de30768e0e494`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 321.9 KB (321949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449373c6d3c93d44e06855012381e095988cc78668a7d4e2295d11c598a245c`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86111058d79ae057cc88f50bad018887961928fe6dd06ef2cc66f303b0015c30`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23735561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0f2a5c4bd2272c4809de2465576673b7e95bd96520b16ee5b47843a9bef7a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23735695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdb4edf36e22a3a5e107167f9c1cb525396ad29994ae7f103df6508c358bd83`

```dockerfile
```

-	Layers:
	-	`sha256:06d23bdd842d459cea3aaa27f2e94a10035256d473eba4ceec69a7c08d68ceaa`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23718572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246f9008e3f1ac54635b14820165dfc6645009b893dcbbc986ec4c678bb7f41d`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 17.1 KB (17123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1f93c23fd385eeb7f2448909022dcc705439832d58377e80170620a6b118ee62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260096340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116cf9176634313710c9c257bc70f0e67bfed60a08f586e83cf7eae4bff7fd2f`
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfece1d5df372ac2f8404edb6ab6f04310cb7578f9e31329eb26ebc084f487a`  
		Last Modified: Tue, 04 Feb 2025 14:47:10 GMT  
		Size: 121.8 MB (121825178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9250bf185b1a4c8850fefbdb740dcf3f379adf745c3255f7a8407fa0a57f1dc`  
		Last Modified: Tue, 04 Feb 2025 14:47:07 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ded77ac56df8a405c3c26852271748c1e71a81c45ee63a0d55740630ad56d7`  
		Last Modified: Tue, 04 Feb 2025 22:02:00 GMT  
		Size: 82.7 MB (82654236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4004f3b862a873c62b82c3b21e9865458c2c533493f0e0e9683cbe10414ede5a`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 322.0 KB (321974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d17c1a13e6b326395e65fd406b1ab982bb3aeaa3a440bb38ae18f1c0ff6175`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a6e0521a8e25a70f9ea7a1a52c29b5da861405a6379670fd3f6fead37eab0`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.1 MB (23128256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:e8c2fc9d83559f2f3e36e6c2a48cba90ce18ae2ea3ebf51a73551d24af38a5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23749032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44580c6c7f266f61f7649004fefe827613fafaaa442c70fac2c29752de442124`

```dockerfile
```

-	Layers:
	-	`sha256:97e6f5b1972232505dfe34e04419da2a3a4b4802daadce5e0f9b75cad636fa0e`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.7 MB (23731771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3772758b0b9985d008ab1a3526ed8e73d520fdc9ba11f7d6449da0679804aad`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:337f4fbb7fe3dbcca1e11cb68b9c01c9960b69a304657b5c7a156252b563c3f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:632a5aac59584ab5bb0e06d04a5e39418ebf2353236fc015daa44a4b040b58d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267763467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922b59e7539bea06cab6e83e21efc0b8bcd0f082a25d2b72ac99056ee573c6b9`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84978cd4920dbb6ce11792e880709796810884d9945087cff06a0b57cf496ca`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 1.2 MB (1207606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8477dd187360dc43e3f8b3b9094455579676d805dba6e105e0bba7d5ff67cfb`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 3.6 MB (3625035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37fe4809b99d383618c439a60815c0606887006924f154f8fd0209d279bed7`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeae0ad7c3a66464a0e67535cabdddec74030230337cfcd74e28118e7096df9`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f68e1fb716a6f991cef2069792082fcf733f82146983818f7b61cb9254eef4`  
		Last Modified: Tue, 04 Feb 2025 04:32:53 GMT  
		Size: 124.4 MB (124355396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834eacd2fda9baf4d52ab0b35cf309f08a7ce54cc18714f117e36ffebf7f583`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526137aab8eabb030282d4cd36a82d84f0c98f7e226cf70b0a70555c16350261`  
		Last Modified: Tue, 04 Feb 2025 05:26:44 GMT  
		Size: 85.0 MB (84977086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e786d9035575d521ab8b98957006a642cdf3e9f87a7cc100de30768e0e494`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 321.9 KB (321949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9449373c6d3c93d44e06855012381e095988cc78668a7d4e2295d11c598a245c`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86111058d79ae057cc88f50bad018887961928fe6dd06ef2cc66f303b0015c30`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23735561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:0f2a5c4bd2272c4809de2465576673b7e95bd96520b16ee5b47843a9bef7a92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23735695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdb4edf36e22a3a5e107167f9c1cb525396ad29994ae7f103df6508c358bd83`

```dockerfile
```

-	Layers:
	-	`sha256:06d23bdd842d459cea3aaa27f2e94a10035256d473eba4ceec69a7c08d68ceaa`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 23.7 MB (23718572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246f9008e3f1ac54635b14820165dfc6645009b893dcbbc986ec4c678bb7f41d`  
		Last Modified: Tue, 04 Feb 2025 05:26:43 GMT  
		Size: 17.1 KB (17123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1f93c23fd385eeb7f2448909022dcc705439832d58377e80170620a6b118ee62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260096340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116cf9176634313710c9c257bc70f0e67bfed60a08f586e83cf7eae4bff7fd2f`
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfece1d5df372ac2f8404edb6ab6f04310cb7578f9e31329eb26ebc084f487a`  
		Last Modified: Tue, 04 Feb 2025 14:47:10 GMT  
		Size: 121.8 MB (121825178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9250bf185b1a4c8850fefbdb740dcf3f379adf745c3255f7a8407fa0a57f1dc`  
		Last Modified: Tue, 04 Feb 2025 14:47:07 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ded77ac56df8a405c3c26852271748c1e71a81c45ee63a0d55740630ad56d7`  
		Last Modified: Tue, 04 Feb 2025 22:02:00 GMT  
		Size: 82.7 MB (82654236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4004f3b862a873c62b82c3b21e9865458c2c533493f0e0e9683cbe10414ede5a`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 322.0 KB (321974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d17c1a13e6b326395e65fd406b1ab982bb3aeaa3a440bb38ae18f1c0ff6175`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a6e0521a8e25a70f9ea7a1a52c29b5da861405a6379670fd3f6fead37eab0`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.1 MB (23128256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e8c2fc9d83559f2f3e36e6c2a48cba90ce18ae2ea3ebf51a73551d24af38a5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23749032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44580c6c7f266f61f7649004fefe827613fafaaa442c70fac2c29752de442124`

```dockerfile
```

-	Layers:
	-	`sha256:97e6f5b1972232505dfe34e04419da2a3a4b4802daadce5e0f9b75cad636fa0e`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.7 MB (23731771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3772758b0b9985d008ab1a3526ed8e73d520fdc9ba11f7d6449da0679804aad`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:441d0ba8bd198e95442c5fd9198398a7b0ac0c4fa542152c45736fe4a68ae8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:58f6287ab43a0c3b4804204a3c311df1a02e215fb13dac983239071ef8e826c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166181016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506232f31e0a12872988917a0c2550439ce486991b9b6173af6e92c28ba3530f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3462f71d2a0e18954d5184197e3d81efd3f0f9532354e4efe8a9c00e89b52f9d`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 1.2 MB (1208107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613b3bdd3f675c9e6f115690c98f70841a8d5409c2abca2142578b657f0fdafe`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 3.6 MB (3625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c84f42f76f81695686241b905d92e4291c9c1f2e464b66234a989764d3ff2f6`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f679410b03e667d0a75866f5f27e525633bfd06e12beab159454064db254c8b2`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9ddb9e9f15efe8ba457c6acec0d3f45b8e95c55dd3ce4eb51a949a9d1c1ea2`  
		Last Modified: Mon, 10 Mar 2025 18:13:41 GMT  
		Size: 131.8 MB (131807751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65600ace7adaf01c69182fded1b02b1ddb5154b6e699eca14753a650c912b5`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:9eadae4e25ceccf4ed71a119d7fa5662b93f3843b875597ec98c4a9938645ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19240932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7949a0d14571bd43ec956379d297b022657f167ca720f9c51f1a098730957aa`

```dockerfile
```

-	Layers:
	-	`sha256:c09981bb3df254f09de1b812a69166e9491c28c0870e18f25bc09938d6b3c457`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 19.2 MB (19224527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342eaf2dcc9e29a5c90b7e584d799f2fd9f97d7e6e49894c73c1a0bba9d6dc47`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:395e82bac03665e95ce2fc4e0fbdd7309d934c49a6b32df758be968b27d12311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160174087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaa32b146bf75ca5682fffccc3e4c942bcb4b6e33951eb9d5a2b503e25f5e08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1b1a26de1f9fd0065cb8c9fe0444c34f0af9a2bdadc0629ad8594853432b3330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19233947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666d8589c7edea49e23cd3e3944491b72e377037e97e33cbf546a634471d63d5`

```dockerfile
```

-	Layers:
	-	`sha256:51173e6e9a615c6eec568c02d61d5d82bc81f464c5f841a7be1e214c790e4bd4`  
		Last Modified: Mon, 10 Mar 2025 18:23:25 GMT  
		Size: 19.2 MB (19217402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1898f397cd64e25737f39a5c39bee7febdf3176972f7e11f5c028f72b30077c8`  
		Last Modified: Mon, 10 Mar 2025 18:23:23 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:441d0ba8bd198e95442c5fd9198398a7b0ac0c4fa542152c45736fe4a68ae8ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:58f6287ab43a0c3b4804204a3c311df1a02e215fb13dac983239071ef8e826c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166181016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506232f31e0a12872988917a0c2550439ce486991b9b6173af6e92c28ba3530f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3462f71d2a0e18954d5184197e3d81efd3f0f9532354e4efe8a9c00e89b52f9d`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 1.2 MB (1208107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613b3bdd3f675c9e6f115690c98f70841a8d5409c2abca2142578b657f0fdafe`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 3.6 MB (3625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c84f42f76f81695686241b905d92e4291c9c1f2e464b66234a989764d3ff2f6`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f679410b03e667d0a75866f5f27e525633bfd06e12beab159454064db254c8b2`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9ddb9e9f15efe8ba457c6acec0d3f45b8e95c55dd3ce4eb51a949a9d1c1ea2`  
		Last Modified: Mon, 10 Mar 2025 18:13:41 GMT  
		Size: 131.8 MB (131807751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65600ace7adaf01c69182fded1b02b1ddb5154b6e699eca14753a650c912b5`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:9eadae4e25ceccf4ed71a119d7fa5662b93f3843b875597ec98c4a9938645ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19240932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7949a0d14571bd43ec956379d297b022657f167ca720f9c51f1a098730957aa`

```dockerfile
```

-	Layers:
	-	`sha256:c09981bb3df254f09de1b812a69166e9491c28c0870e18f25bc09938d6b3c457`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 19.2 MB (19224527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342eaf2dcc9e29a5c90b7e584d799f2fd9f97d7e6e49894c73c1a0bba9d6dc47`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:395e82bac03665e95ce2fc4e0fbdd7309d934c49a6b32df758be968b27d12311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160174087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaa32b146bf75ca5682fffccc3e4c942bcb4b6e33951eb9d5a2b503e25f5e08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:1b1a26de1f9fd0065cb8c9fe0444c34f0af9a2bdadc0629ad8594853432b3330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19233947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666d8589c7edea49e23cd3e3944491b72e377037e97e33cbf546a634471d63d5`

```dockerfile
```

-	Layers:
	-	`sha256:51173e6e9a615c6eec568c02d61d5d82bc81f464c5f841a7be1e214c790e4bd4`  
		Last Modified: Mon, 10 Mar 2025 18:23:25 GMT  
		Size: 19.2 MB (19217402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1898f397cd64e25737f39a5c39bee7febdf3176972f7e11f5c028f72b30077c8`  
		Last Modified: Mon, 10 Mar 2025 18:23:23 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:ed03918373b3b3a4d20d370b923bd52246eb64eafc541dba69b6a5e44925d140
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:96d5754c47b0032826090ec497025edef5a93c19b6407bf2adedcb9f0ef8d063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298554379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f76aeda510e24a146e8050c2ef156bad8d7db83d21f23bf3dc90c414a28565d`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f799811f78900d918566ae506e59f609131fc9aa2aadc0a20363c8431be72735`  
		Last Modified: Tue, 04 Feb 2025 05:27:05 GMT  
		Size: 112.5 MB (112548960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790abc014da9d08e679732b7bf93439b6e1c80b04e9389763566899abffe958f`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 348.3 KB (348305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17046dc54a215d05863c5f4578045d09e9165e2191a2689eaec75723fb8cb07a`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd799659eddfe3d7cb6e5fbf2cc059a3222acba665831b5b363d072093b4719`  
		Last Modified: Tue, 04 Feb 2025 05:27:04 GMT  
		Size: 28.0 MB (27963262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:0d2945b7e87333941a7ca8980aace82f7cf2aa02e9a0ba2a11566d9434bbff87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23858410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e3014569ef327fd2cff0bb664f764d9a8443a8f0f0d1aae493ce2d3a9264e7`

```dockerfile
```

-	Layers:
	-	`sha256:1a237a26c69f81885e6602e06d1975aa182dd0833533249f5631d25dab5dc3fa`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 23.8 MB (23840981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9e206ec3660a2243f88f61216f7669a6ca6efcf7dc32867a510aad3001af05`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfe1ad7d60f64486f4041563a8b2753a6c7020436978b600b60b938bdda4f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286083730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4582c4aebe338698d689bac08591e4086fbe7cc1afabe451e304bd000ae0f45a`
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
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63319eccea3c72ab6d7d949469263856d4536e9cd706ea95737df417a0844d47`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 679.9 KB (679880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398c28a986a6ad00e38d58018c1164a49f100005ed75bf86b35f690f439ea7e`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 3.6 MB (3559788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df9da01336e4108fa26e6b36a069895325f27ba04a1fec9c91ff35c84097ae`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f58c34793503cf5ba16f4d4fc8ce2e5b169468c3ab1534db58be9aef1c8cfd`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f850ce01846867a763779ca58d7bcd68a406bcc06d83d5f336df9f1af04d89b`  
		Last Modified: Tue, 04 Feb 2025 14:49:58 GMT  
		Size: 117.6 MB (117595132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74950aa3433684e07f35a319dae2d5b2c9194e38d014e3888c3c2c24bec843`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1b23617d0853ed5a82180013d21d276e99021dd317a022ba92434e181df22`  
		Last Modified: Tue, 04 Feb 2025 22:04:56 GMT  
		Size: 107.9 MB (107945853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83452a074608a4c581e2d883714478c1bd0639a3c85b8b69e1d061f1d59baa`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 349.1 KB (349149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cf2b9d680488073e25fd14f7cc38713758bbf5c42e19eba260082becdef26`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0ff6b4898d5f98f2fded332804af4b40d7b47c66907a152822cb5e2fd0db20`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 27.1 MB (27055422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:b0f549c4a4a67ade5d6067541acabd2a92def39a8a9e51eee58b9a6bfd1d5393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23881115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76afd84f90b734ba676a426745090b13cf61ac20e4c2fd3dcc7123da0210192`

```dockerfile
```

-	Layers:
	-	`sha256:71d012fa673cbc42e4590589aecd9421ec8193c125231a1552e332531a5b82ad`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 23.9 MB (23863537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73b2a8d85339d6d04db2fe4fa2e7c80b79cd9fafa0ef14d41027db4eafbef74`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:8fca844ef649359c9e26795380f8084222f463467658aa03cd9f3801c7b64c27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:1572554627d941b95dce4ffc8303a358bb9c3dd5102bf31db492a4d611154125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1079731337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901365dedcf2223e1f2b3cfab10464a3a401e424b72ab7d2c3a63d30043900dc`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f799811f78900d918566ae506e59f609131fc9aa2aadc0a20363c8431be72735`  
		Last Modified: Tue, 04 Feb 2025 05:27:05 GMT  
		Size: 112.5 MB (112548960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790abc014da9d08e679732b7bf93439b6e1c80b04e9389763566899abffe958f`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 348.3 KB (348305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17046dc54a215d05863c5f4578045d09e9165e2191a2689eaec75723fb8cb07a`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd799659eddfe3d7cb6e5fbf2cc059a3222acba665831b5b363d072093b4719`  
		Last Modified: Tue, 04 Feb 2025 05:27:04 GMT  
		Size: 28.0 MB (27963262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544ba78693a91ef0030d341fc55c6be950f1c82fbb25a3c279cf4f6120b4206f`  
		Last Modified: Tue, 04 Feb 2025 06:18:14 GMT  
		Size: 781.2 MB (781176958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:722788fbe3c9791c5e70652bf2defbc1c5ce352150987f8f8d2fc723e0a1b758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59572652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a59ee6e9738718605654bb9261f2e8c75f1deda0dcb0120437277756cf126a`

```dockerfile
```

-	Layers:
	-	`sha256:c21aad716a39812b49f3433961b0a6beec8f8de5ef19ad8cd10f24d840ac6c75`  
		Last Modified: Tue, 04 Feb 2025 06:18:03 GMT  
		Size: 59.6 MB (59562964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c834a428b6de21d4fe30efbb5e78642b82984cbe4afd27a86c5bc8f121c23ffd`  
		Last Modified: Tue, 04 Feb 2025 06:18:02 GMT  
		Size: 9.7 KB (9688 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3bd1a67280a5daf89a7800d9823e574b93b4c824ff6fe35af185677f9b9a994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.4 MB (977422326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5342fb846691467c02d438192cdee325edccc145312d00ad18c33a9c1eb690`
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
	-	`sha256:63319eccea3c72ab6d7d949469263856d4536e9cd706ea95737df417a0844d47`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 679.9 KB (679880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398c28a986a6ad00e38d58018c1164a49f100005ed75bf86b35f690f439ea7e`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 3.6 MB (3559788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df9da01336e4108fa26e6b36a069895325f27ba04a1fec9c91ff35c84097ae`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f58c34793503cf5ba16f4d4fc8ce2e5b169468c3ab1534db58be9aef1c8cfd`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f850ce01846867a763779ca58d7bcd68a406bcc06d83d5f336df9f1af04d89b`  
		Last Modified: Tue, 04 Feb 2025 14:49:58 GMT  
		Size: 117.6 MB (117595132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74950aa3433684e07f35a319dae2d5b2c9194e38d014e3888c3c2c24bec843`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1b23617d0853ed5a82180013d21d276e99021dd317a022ba92434e181df22`  
		Last Modified: Tue, 04 Feb 2025 22:04:56 GMT  
		Size: 107.9 MB (107945853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83452a074608a4c581e2d883714478c1bd0639a3c85b8b69e1d061f1d59baa`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 349.1 KB (349149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cf2b9d680488073e25fd14f7cc38713758bbf5c42e19eba260082becdef26`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0ff6b4898d5f98f2fded332804af4b40d7b47c66907a152822cb5e2fd0db20`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 27.1 MB (27055422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b0be361a73f37b76ff368119b44430ced2a6e53c5f223b293c9e58ca559e12`  
		Last Modified: Wed, 05 Feb 2025 03:54:51 GMT  
		Size: 691.3 MB (691338596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:90414b8d1a2fb77fa6d0c72f7d1a92478f21589e083e27f63fc630540547b77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59526735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b927f67b1b937a61bd21df1b0aa4f1bdc3a1b1431d10e3ae4efb21da42180625`

```dockerfile
```

-	Layers:
	-	`sha256:b32120b9351bdc8d942d72598151a4803098c15687909ebb8eead540f5b32089`  
		Last Modified: Wed, 05 Feb 2025 03:54:40 GMT  
		Size: 59.5 MB (59516968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b03ed190939014db04247f278a6ff24822dcab334853d5c73f2cdf882a9266`  
		Last Modified: Wed, 05 Feb 2025 03:54:38 GMT  
		Size: 9.8 KB (9767 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:8fca844ef649359c9e26795380f8084222f463467658aa03cd9f3801c7b64c27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:1572554627d941b95dce4ffc8303a358bb9c3dd5102bf31db492a4d611154125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1079731337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901365dedcf2223e1f2b3cfab10464a3a401e424b72ab7d2c3a63d30043900dc`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f799811f78900d918566ae506e59f609131fc9aa2aadc0a20363c8431be72735`  
		Last Modified: Tue, 04 Feb 2025 05:27:05 GMT  
		Size: 112.5 MB (112548960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790abc014da9d08e679732b7bf93439b6e1c80b04e9389763566899abffe958f`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 348.3 KB (348305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17046dc54a215d05863c5f4578045d09e9165e2191a2689eaec75723fb8cb07a`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd799659eddfe3d7cb6e5fbf2cc059a3222acba665831b5b363d072093b4719`  
		Last Modified: Tue, 04 Feb 2025 05:27:04 GMT  
		Size: 28.0 MB (27963262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544ba78693a91ef0030d341fc55c6be950f1c82fbb25a3c279cf4f6120b4206f`  
		Last Modified: Tue, 04 Feb 2025 06:18:14 GMT  
		Size: 781.2 MB (781176958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:722788fbe3c9791c5e70652bf2defbc1c5ce352150987f8f8d2fc723e0a1b758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59572652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a59ee6e9738718605654bb9261f2e8c75f1deda0dcb0120437277756cf126a`

```dockerfile
```

-	Layers:
	-	`sha256:c21aad716a39812b49f3433961b0a6beec8f8de5ef19ad8cd10f24d840ac6c75`  
		Last Modified: Tue, 04 Feb 2025 06:18:03 GMT  
		Size: 59.6 MB (59562964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c834a428b6de21d4fe30efbb5e78642b82984cbe4afd27a86c5bc8f121c23ffd`  
		Last Modified: Tue, 04 Feb 2025 06:18:02 GMT  
		Size: 9.7 KB (9688 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3bd1a67280a5daf89a7800d9823e574b93b4c824ff6fe35af185677f9b9a994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.4 MB (977422326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5342fb846691467c02d438192cdee325edccc145312d00ad18c33a9c1eb690`
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
	-	`sha256:63319eccea3c72ab6d7d949469263856d4536e9cd706ea95737df417a0844d47`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 679.9 KB (679880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398c28a986a6ad00e38d58018c1164a49f100005ed75bf86b35f690f439ea7e`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 3.6 MB (3559788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df9da01336e4108fa26e6b36a069895325f27ba04a1fec9c91ff35c84097ae`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f58c34793503cf5ba16f4d4fc8ce2e5b169468c3ab1534db58be9aef1c8cfd`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f850ce01846867a763779ca58d7bcd68a406bcc06d83d5f336df9f1af04d89b`  
		Last Modified: Tue, 04 Feb 2025 14:49:58 GMT  
		Size: 117.6 MB (117595132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74950aa3433684e07f35a319dae2d5b2c9194e38d014e3888c3c2c24bec843`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1b23617d0853ed5a82180013d21d276e99021dd317a022ba92434e181df22`  
		Last Modified: Tue, 04 Feb 2025 22:04:56 GMT  
		Size: 107.9 MB (107945853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83452a074608a4c581e2d883714478c1bd0639a3c85b8b69e1d061f1d59baa`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 349.1 KB (349149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cf2b9d680488073e25fd14f7cc38713758bbf5c42e19eba260082becdef26`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0ff6b4898d5f98f2fded332804af4b40d7b47c66907a152822cb5e2fd0db20`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 27.1 MB (27055422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b0be361a73f37b76ff368119b44430ced2a6e53c5f223b293c9e58ca559e12`  
		Last Modified: Wed, 05 Feb 2025 03:54:51 GMT  
		Size: 691.3 MB (691338596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:90414b8d1a2fb77fa6d0c72f7d1a92478f21589e083e27f63fc630540547b77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59526735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b927f67b1b937a61bd21df1b0aa4f1bdc3a1b1431d10e3ae4efb21da42180625`

```dockerfile
```

-	Layers:
	-	`sha256:b32120b9351bdc8d942d72598151a4803098c15687909ebb8eead540f5b32089`  
		Last Modified: Wed, 05 Feb 2025 03:54:40 GMT  
		Size: 59.5 MB (59516968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b03ed190939014db04247f278a6ff24822dcab334853d5c73f2cdf882a9266`  
		Last Modified: Wed, 05 Feb 2025 03:54:38 GMT  
		Size: 9.8 KB (9767 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:ed03918373b3b3a4d20d370b923bd52246eb64eafc541dba69b6a5e44925d140
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:96d5754c47b0032826090ec497025edef5a93c19b6407bf2adedcb9f0ef8d063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298554379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f76aeda510e24a146e8050c2ef156bad8d7db83d21f23bf3dc90c414a28565d`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f799811f78900d918566ae506e59f609131fc9aa2aadc0a20363c8431be72735`  
		Last Modified: Tue, 04 Feb 2025 05:27:05 GMT  
		Size: 112.5 MB (112548960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790abc014da9d08e679732b7bf93439b6e1c80b04e9389763566899abffe958f`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 348.3 KB (348305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17046dc54a215d05863c5f4578045d09e9165e2191a2689eaec75723fb8cb07a`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd799659eddfe3d7cb6e5fbf2cc059a3222acba665831b5b363d072093b4719`  
		Last Modified: Tue, 04 Feb 2025 05:27:04 GMT  
		Size: 28.0 MB (27963262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0d2945b7e87333941a7ca8980aace82f7cf2aa02e9a0ba2a11566d9434bbff87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23858410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e3014569ef327fd2cff0bb664f764d9a8443a8f0f0d1aae493ce2d3a9264e7`

```dockerfile
```

-	Layers:
	-	`sha256:1a237a26c69f81885e6602e06d1975aa182dd0833533249f5631d25dab5dc3fa`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 23.8 MB (23840981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9e206ec3660a2243f88f61216f7669a6ca6efcf7dc32867a510aad3001af05`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfe1ad7d60f64486f4041563a8b2753a6c7020436978b600b60b938bdda4f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286083730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4582c4aebe338698d689bac08591e4086fbe7cc1afabe451e304bd000ae0f45a`
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
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63319eccea3c72ab6d7d949469263856d4536e9cd706ea95737df417a0844d47`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 679.9 KB (679880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398c28a986a6ad00e38d58018c1164a49f100005ed75bf86b35f690f439ea7e`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 3.6 MB (3559788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df9da01336e4108fa26e6b36a069895325f27ba04a1fec9c91ff35c84097ae`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f58c34793503cf5ba16f4d4fc8ce2e5b169468c3ab1534db58be9aef1c8cfd`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f850ce01846867a763779ca58d7bcd68a406bcc06d83d5f336df9f1af04d89b`  
		Last Modified: Tue, 04 Feb 2025 14:49:58 GMT  
		Size: 117.6 MB (117595132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74950aa3433684e07f35a319dae2d5b2c9194e38d014e3888c3c2c24bec843`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1b23617d0853ed5a82180013d21d276e99021dd317a022ba92434e181df22`  
		Last Modified: Tue, 04 Feb 2025 22:04:56 GMT  
		Size: 107.9 MB (107945853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83452a074608a4c581e2d883714478c1bd0639a3c85b8b69e1d061f1d59baa`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 349.1 KB (349149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cf2b9d680488073e25fd14f7cc38713758bbf5c42e19eba260082becdef26`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0ff6b4898d5f98f2fded332804af4b40d7b47c66907a152822cb5e2fd0db20`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 27.1 MB (27055422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b0f549c4a4a67ade5d6067541acabd2a92def39a8a9e51eee58b9a6bfd1d5393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23881115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76afd84f90b734ba676a426745090b13cf61ac20e4c2fd3dcc7123da0210192`

```dockerfile
```

-	Layers:
	-	`sha256:71d012fa673cbc42e4590589aecd9421ec8193c125231a1552e332531a5b82ad`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 23.9 MB (23863537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73b2a8d85339d6d04db2fe4fa2e7c80b79cd9fafa0ef14d41027db4eafbef74`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:ed03918373b3b3a4d20d370b923bd52246eb64eafc541dba69b6a5e44925d140
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:96d5754c47b0032826090ec497025edef5a93c19b6407bf2adedcb9f0ef8d063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298554379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f76aeda510e24a146e8050c2ef156bad8d7db83d21f23bf3dc90c414a28565d`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f799811f78900d918566ae506e59f609131fc9aa2aadc0a20363c8431be72735`  
		Last Modified: Tue, 04 Feb 2025 05:27:05 GMT  
		Size: 112.5 MB (112548960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790abc014da9d08e679732b7bf93439b6e1c80b04e9389763566899abffe958f`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 348.3 KB (348305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17046dc54a215d05863c5f4578045d09e9165e2191a2689eaec75723fb8cb07a`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd799659eddfe3d7cb6e5fbf2cc059a3222acba665831b5b363d072093b4719`  
		Last Modified: Tue, 04 Feb 2025 05:27:04 GMT  
		Size: 28.0 MB (27963262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0d2945b7e87333941a7ca8980aace82f7cf2aa02e9a0ba2a11566d9434bbff87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23858410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e3014569ef327fd2cff0bb664f764d9a8443a8f0f0d1aae493ce2d3a9264e7`

```dockerfile
```

-	Layers:
	-	`sha256:1a237a26c69f81885e6602e06d1975aa182dd0833533249f5631d25dab5dc3fa`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 23.8 MB (23840981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9e206ec3660a2243f88f61216f7669a6ca6efcf7dc32867a510aad3001af05`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfe1ad7d60f64486f4041563a8b2753a6c7020436978b600b60b938bdda4f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286083730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4582c4aebe338698d689bac08591e4086fbe7cc1afabe451e304bd000ae0f45a`
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
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63319eccea3c72ab6d7d949469263856d4536e9cd706ea95737df417a0844d47`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 679.9 KB (679880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398c28a986a6ad00e38d58018c1164a49f100005ed75bf86b35f690f439ea7e`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 3.6 MB (3559788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df9da01336e4108fa26e6b36a069895325f27ba04a1fec9c91ff35c84097ae`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f58c34793503cf5ba16f4d4fc8ce2e5b169468c3ab1534db58be9aef1c8cfd`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f850ce01846867a763779ca58d7bcd68a406bcc06d83d5f336df9f1af04d89b`  
		Last Modified: Tue, 04 Feb 2025 14:49:58 GMT  
		Size: 117.6 MB (117595132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74950aa3433684e07f35a319dae2d5b2c9194e38d014e3888c3c2c24bec843`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1b23617d0853ed5a82180013d21d276e99021dd317a022ba92434e181df22`  
		Last Modified: Tue, 04 Feb 2025 22:04:56 GMT  
		Size: 107.9 MB (107945853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83452a074608a4c581e2d883714478c1bd0639a3c85b8b69e1d061f1d59baa`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 349.1 KB (349149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cf2b9d680488073e25fd14f7cc38713758bbf5c42e19eba260082becdef26`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0ff6b4898d5f98f2fded332804af4b40d7b47c66907a152822cb5e2fd0db20`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 27.1 MB (27055422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b0f549c4a4a67ade5d6067541acabd2a92def39a8a9e51eee58b9a6bfd1d5393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23881115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76afd84f90b734ba676a426745090b13cf61ac20e4c2fd3dcc7123da0210192`

```dockerfile
```

-	Layers:
	-	`sha256:71d012fa673cbc42e4590589aecd9421ec8193c125231a1552e332531a5b82ad`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 23.9 MB (23863537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73b2a8d85339d6d04db2fe4fa2e7c80b79cd9fafa0ef14d41027db4eafbef74`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:e5d2bc5949733dd701546bf9387697e982f3998c887c58dcd9af9dd3c3561a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c4fd41d15ae74842bab65bda041d06a81c995482927a7df6b7c88d4208adc6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166129116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3f68a19c2c3e62204f3d6ebd8e9fc84ee8c851c677a75efb23f50401060b3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeea575c80af2e65fe04975f11edd4e921b04d3147a50068c5a5969bee6bafb3`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 680.3 KB (680324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4025c1e6627435e8c8b5d54ace9042ffc9abb779f9949a39e0c91708aac130`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 3.6 MB (3561468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199dff8e77acdbc33a1bde2acbdc1481733c8d72a039fe2915eb196af9159582`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b349db87fd4d4f170f5c76740209f134b55e13f869500cb7f89b880c0b205114`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260dd0d00b496f4a4ee25f954e0fe78b05b9fa66549124673f930393e7aad709`  
		Last Modified: Mon, 10 Mar 2025 18:13:41 GMT  
		Size: 132.1 MB (132130563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe62c3fa6ae8df69810304838608966ed5075f03e07c7afa99eb32abebba528`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:64c31e0281bf00440dc8d87e9acd3f1df31d2092aae0cd6c3797b8772f007a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17827876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65362918d940b2809d571119cf061af6bca702143a5351f97ef7fc804931096`

```dockerfile
```

-	Layers:
	-	`sha256:f4f2e7c4cb26c10f220da05df188db8a4fa5702a0b978852506d73a20636e7a7`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 17.8 MB (17811504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2146b511be3b88257614d0f3d48aac9d98c306109c90443f32f0b03506eaff9`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2fad18cb74d16242525279e44c3fb0fe969deb5b630bce3c690e7d8ab3535739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158757505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264be025260ff1763b69674ba554f6a34cb7de805804e2fb8c0317fbab4bbfcd`
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

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fe558021bfa3322eeb16d6d945fbfbf8016d4a478e82d81eba16b77d995acbf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17802022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cb55077b9b95eb97ae39e85012560e845ce6cc1c9ee291cf6b0db59e6266bf`

```dockerfile
```

-	Layers:
	-	`sha256:4d1cacb35726ea88903b435ccd7f13d0c1fcae4c6d1dc3428b052110090ed0b0`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 17.8 MB (17785510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b43a019bd57286721cd8892989ae862e4b9cf3e0bcb159d31d255a891794ad`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:e5d2bc5949733dd701546bf9387697e982f3998c887c58dcd9af9dd3c3561a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c4fd41d15ae74842bab65bda041d06a81c995482927a7df6b7c88d4208adc6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.1 MB (166129116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3f68a19c2c3e62204f3d6ebd8e9fc84ee8c851c677a75efb23f50401060b3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeea575c80af2e65fe04975f11edd4e921b04d3147a50068c5a5969bee6bafb3`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 680.3 KB (680324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4025c1e6627435e8c8b5d54ace9042ffc9abb779f9949a39e0c91708aac130`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 3.6 MB (3561468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199dff8e77acdbc33a1bde2acbdc1481733c8d72a039fe2915eb196af9159582`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b349db87fd4d4f170f5c76740209f134b55e13f869500cb7f89b880c0b205114`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260dd0d00b496f4a4ee25f954e0fe78b05b9fa66549124673f930393e7aad709`  
		Last Modified: Mon, 10 Mar 2025 18:13:41 GMT  
		Size: 132.1 MB (132130563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe62c3fa6ae8df69810304838608966ed5075f03e07c7afa99eb32abebba528`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:64c31e0281bf00440dc8d87e9acd3f1df31d2092aae0cd6c3797b8772f007a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17827876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65362918d940b2809d571119cf061af6bca702143a5351f97ef7fc804931096`

```dockerfile
```

-	Layers:
	-	`sha256:f4f2e7c4cb26c10f220da05df188db8a4fa5702a0b978852506d73a20636e7a7`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 17.8 MB (17811504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2146b511be3b88257614d0f3d48aac9d98c306109c90443f32f0b03506eaff9`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2fad18cb74d16242525279e44c3fb0fe969deb5b630bce3c690e7d8ab3535739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158757505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264be025260ff1763b69674ba554f6a34cb7de805804e2fb8c0317fbab4bbfcd`
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

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fe558021bfa3322eeb16d6d945fbfbf8016d4a478e82d81eba16b77d995acbf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17802022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cb55077b9b95eb97ae39e85012560e845ce6cc1c9ee291cf6b0db59e6266bf`

```dockerfile
```

-	Layers:
	-	`sha256:4d1cacb35726ea88903b435ccd7f13d0c1fcae4c6d1dc3428b052110090ed0b0`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 17.8 MB (17785510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b43a019bd57286721cd8892989ae862e4b9cf3e0bcb159d31d255a891794ad`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:ed03918373b3b3a4d20d370b923bd52246eb64eafc541dba69b6a5e44925d140
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:96d5754c47b0032826090ec497025edef5a93c19b6407bf2adedcb9f0ef8d063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298554379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f76aeda510e24a146e8050c2ef156bad8d7db83d21f23bf3dc90c414a28565d`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f799811f78900d918566ae506e59f609131fc9aa2aadc0a20363c8431be72735`  
		Last Modified: Tue, 04 Feb 2025 05:27:05 GMT  
		Size: 112.5 MB (112548960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790abc014da9d08e679732b7bf93439b6e1c80b04e9389763566899abffe958f`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 348.3 KB (348305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17046dc54a215d05863c5f4578045d09e9165e2191a2689eaec75723fb8cb07a`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd799659eddfe3d7cb6e5fbf2cc059a3222acba665831b5b363d072093b4719`  
		Last Modified: Tue, 04 Feb 2025 05:27:04 GMT  
		Size: 28.0 MB (27963262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:0d2945b7e87333941a7ca8980aace82f7cf2aa02e9a0ba2a11566d9434bbff87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23858410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e3014569ef327fd2cff0bb664f764d9a8443a8f0f0d1aae493ce2d3a9264e7`

```dockerfile
```

-	Layers:
	-	`sha256:1a237a26c69f81885e6602e06d1975aa182dd0833533249f5631d25dab5dc3fa`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 23.8 MB (23840981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9e206ec3660a2243f88f61216f7669a6ca6efcf7dc32867a510aad3001af05`  
		Last Modified: Tue, 04 Feb 2025 05:27:03 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfe1ad7d60f64486f4041563a8b2753a6c7020436978b600b60b938bdda4f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286083730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4582c4aebe338698d689bac08591e4086fbe7cc1afabe451e304bd000ae0f45a`
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
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63319eccea3c72ab6d7d949469263856d4536e9cd706ea95737df417a0844d47`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 679.9 KB (679880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398c28a986a6ad00e38d58018c1164a49f100005ed75bf86b35f690f439ea7e`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 3.6 MB (3559788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25df9da01336e4108fa26e6b36a069895325f27ba04a1fec9c91ff35c84097ae`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f58c34793503cf5ba16f4d4fc8ce2e5b169468c3ab1534db58be9aef1c8cfd`  
		Last Modified: Tue, 04 Feb 2025 14:49:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f850ce01846867a763779ca58d7bcd68a406bcc06d83d5f336df9f1af04d89b`  
		Last Modified: Tue, 04 Feb 2025 14:49:58 GMT  
		Size: 117.6 MB (117595132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74950aa3433684e07f35a319dae2d5b2c9194e38d014e3888c3c2c24bec843`  
		Last Modified: Tue, 04 Feb 2025 14:49:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1b23617d0853ed5a82180013d21d276e99021dd317a022ba92434e181df22`  
		Last Modified: Tue, 04 Feb 2025 22:04:56 GMT  
		Size: 107.9 MB (107945853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83452a074608a4c581e2d883714478c1bd0639a3c85b8b69e1d061f1d59baa`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 349.1 KB (349149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cf2b9d680488073e25fd14f7cc38713758bbf5c42e19eba260082becdef26`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0ff6b4898d5f98f2fded332804af4b40d7b47c66907a152822cb5e2fd0db20`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 27.1 MB (27055422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:b0f549c4a4a67ade5d6067541acabd2a92def39a8a9e51eee58b9a6bfd1d5393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23881115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76afd84f90b734ba676a426745090b13cf61ac20e4c2fd3dcc7123da0210192`

```dockerfile
```

-	Layers:
	-	`sha256:71d012fa673cbc42e4590589aecd9421ec8193c125231a1552e332531a5b82ad`  
		Last Modified: Tue, 04 Feb 2025 22:04:54 GMT  
		Size: 23.9 MB (23863537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73b2a8d85339d6d04db2fe4fa2e7c80b79cd9fafa0ef14d41027db4eafbef74`  
		Last Modified: Tue, 04 Feb 2025 22:04:53 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic`

```console
$ docker pull ros@sha256:456b9a58b63e259c388fb59d8f6c1db6b17967f7b515ebb5aefffb4eb2fba888
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
$ docker pull ros@sha256:24ff52d34ab601679f1c783ddc76ab65d0ed3abe011969b659e12544320e5529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263082762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36930c7e3fb8d74fc8caf149572e686ff6536ecbce01e6fce4def98bea7cf5c`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627070c22110350c23cc50089a841b8c4257eb28ce66dea53acf5039c3230e34`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 1.2 MB (1198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8728cedb8ba29fe02ce989c70421066de64c666b6a99582f25178d88aa15436`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 5.4 MB (5361869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127793489f3bb50eb05db40cab2ed332c4a29fd05b34138da31541fbd7e63b1`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87538de7941b612134ab50edd68c6e0f52c6f7ddfedb7fb0c5130b6a6ca0ae77`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11090410af8961388a4a44a929c9fbc8eb6000dac2075e09c4392d7ec0a60ae4`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 177.0 MB (177040113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07f0bec1e43c18cd93acea1d11ffd7fc0409d8b06afa3a0c107f8ad80b105a`  
		Last Modified: Wed, 16 Oct 2024 16:18:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a60a3d4f5d8a2ba79f6b17c46970171ea46e7dbc4f8a206d7ce90d28b64e0`  
		Last Modified: Wed, 16 Oct 2024 16:52:11 GMT  
		Size: 50.7 MB (50721153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb065133b9b742d6bbbca49aa896b94a18f93aa7c33c890cfb3e6b73cb0f53`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 331.3 KB (331289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272267b4195536b2a923055b1e37c0166a7414c13ab20177450be71783a6c666`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 916.0 KB (915988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:7534e1102db6fa8364771006961a05c05197aef2de7c978b00e7a2bcfe12faa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27608503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0012e651d7967eb1bba01aa0e7b560e68f0fbd9aaeadc0096126b1f561db4ef6`

```dockerfile
```

-	Layers:
	-	`sha256:c9912d0d53a7c301dc7275a2f952e6f82b44921b0248bdfc4d4cd4c958bd7126`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 27.6 MB (27594813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7118bcec179b41f121295fec5f259cde05401067095f8b0f6c22535897169636`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 13.7 KB (13690 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:665efd9c21f6e7dd7e1ecd97e6f9b421775e63b55167828fb04dfdeff26aa088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228288413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bd77e448977f3464d7b7411f33d0f7e7db4181e0c68af48c71a9bd3c34404b`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:9bc66574adabc536cff0ca51f33d6a859efc2166256401492dbe4d2c742aeb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27371952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778fd253c2c9f0084aad03ac5f3d8d49a375c0ac42f7d25966b0cc12d841f319`

```dockerfile
```

-	Layers:
	-	`sha256:158c083e6830094fc49e0429b98e613165957001bccd5c321f312f6b09d3e584`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 27.4 MB (27358168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed656d35de762e9baed95088a4d31b34a03cdc9ad04dccbd81dc4ea4b1763cc`  
		Last Modified: Wed, 16 Oct 2024 03:18:50 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e317c94efc821597009d9fb3fa5a0db8fee08a8a9d010852986b9c13e6988c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250189216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03e6c05479a847440a256d79340ecccf68bee3d3c012b07dbf18b94a8d13193`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7692d171772b08f5a9d0dc4a7b1ae51b870e77829dd8e7c0a62b1f9817239`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 1.2 MB (1198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f9119823a2bf386bf829a11e39290d3f3441a7210eb39b4a7342f8481643ac`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 5.3 MB (5342090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39a30d323d034154408ec363b1f3afbe72ed9d424be55808a92a6309b120d`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da5b2e66f57fc3b781b4d81c9514dee9b08decd9306330cd58833771758139`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70554c999e53a1aad7c55aafc6f0ddb8095bd7b1eb3c0dc38e07aec7896ae2cf`  
		Last Modified: Wed, 16 Oct 2024 04:13:13 GMT  
		Size: 171.5 MB (171452633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdb47098b878011f0003ad6c94e50363b2156e2bb6951fa21f9012a17f1bcf`  
		Last Modified: Wed, 16 Oct 2024 04:13:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2103d332713160aa2196205de34c2914b0072edd6edfd48482dbb2d4a3d6`  
		Last Modified: Wed, 16 Oct 2024 06:04:28 GMT  
		Size: 45.0 MB (44990886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38185782b6690ae35720744a5321274a8651237c9d6900cebc10a000409af2e5`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 331.3 KB (331287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843243ae0d09c7eda36f37ac0bc9801a113bf37beb05fae37942f88241e275c`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 897.3 KB (897322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:d7f07c89fc0129e2bc9f71244b1268d8bb57d4dd4bb75c39e92aff6bb4f70694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27558911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b6391e8cfeba2048a60ff13c4dd745bfca46b0d85bce4c5e87c1cc065abe62`

```dockerfile
```

-	Layers:
	-	`sha256:8dc7119ced5dc25252d4e6119082fe12de268a860443343a56495e723d0bca38`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 27.5 MB (27545099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e2265e87cc5692dd2c4402c7bbff074b3cf227f920f9cc95d923bbccec1eb7`  
		Last Modified: Wed, 16 Oct 2024 06:04:26 GMT  
		Size: 13.8 KB (13812 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:d44729fa9c62ef25a7e2e1bed25587d3225fc00d87da7c2e62acbb83876f979e
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
$ docker pull ros@sha256:37d9069e76e6ff7e4899e02e133f275550f975b618e43549df2c843ee1125d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.2 MB (834246421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7c7f9e89ae9d0b865b4ffb142d11c42b76a112ed2b644bfed29df90e4b1ac`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627070c22110350c23cc50089a841b8c4257eb28ce66dea53acf5039c3230e34`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 1.2 MB (1198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8728cedb8ba29fe02ce989c70421066de64c666b6a99582f25178d88aa15436`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 5.4 MB (5361869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127793489f3bb50eb05db40cab2ed332c4a29fd05b34138da31541fbd7e63b1`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87538de7941b612134ab50edd68c6e0f52c6f7ddfedb7fb0c5130b6a6ca0ae77`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11090410af8961388a4a44a929c9fbc8eb6000dac2075e09c4392d7ec0a60ae4`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 177.0 MB (177040113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07f0bec1e43c18cd93acea1d11ffd7fc0409d8b06afa3a0c107f8ad80b105a`  
		Last Modified: Wed, 16 Oct 2024 16:18:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a60a3d4f5d8a2ba79f6b17c46970171ea46e7dbc4f8a206d7ce90d28b64e0`  
		Last Modified: Wed, 16 Oct 2024 16:52:11 GMT  
		Size: 50.7 MB (50721153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb065133b9b742d6bbbca49aa896b94a18f93aa7c33c890cfb3e6b73cb0f53`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 331.3 KB (331289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272267b4195536b2a923055b1e37c0166a7414c13ab20177450be71783a6c666`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 916.0 KB (915988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee6c6e59fce0e16d0f3d326f1d155c60b0e1299d05a50121e91e77b474e6b70`  
		Last Modified: Wed, 16 Oct 2024 17:40:05 GMT  
		Size: 571.2 MB (571163659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:484ae3d7703cd9196cd102483161d0b7186e59dbf22b85d5fab7de197db007e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51781537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bbb65726b8a9e050feb3fa92d0302d96cf814e80d52891abc6f3ba85b468e9`

```dockerfile
```

-	Layers:
	-	`sha256:45cf0bd887bfb0a9d0d4475ef23af02a232638c98c52991d04f2053de337d84f`  
		Last Modified: Wed, 16 Oct 2024 17:39:58 GMT  
		Size: 51.8 MB (51772160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2007b29cd2d3707f184206d8eb6d98b88ce3c07950eecade7713d537424a3fe3`  
		Last Modified: Wed, 16 Oct 2024 17:39:57 GMT  
		Size: 9.4 KB (9377 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:4e3c192434111446b5e289bbbbed4b0627f6b022d247614e1b5c615079df54c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.2 MB (725162922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6722522b64e2199faf06f62ebdd9ec102d857518c64fcb4f5f35c45544a5d9`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1949580a963a0afcdb9b0814bbfc7b5e0dc62740075d4abdb4a5b82b36229b`  
		Last Modified: Wed, 16 Oct 2024 04:19:59 GMT  
		Size: 496.9 MB (496874509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:2a56749f526b236ae91d2d30d45dad202afec2ebf09d945c1bb2f89b4bc5b13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51415392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91eadbd4a2c3aa9c33f9764822985eb8f3594865a0491e9c38c39618be6b98b0`

```dockerfile
```

-	Layers:
	-	`sha256:51c8eda415d83c183b49d4002ff8cc36d5a9a3613207945774f72915b53049f1`  
		Last Modified: Wed, 16 Oct 2024 04:19:50 GMT  
		Size: 51.4 MB (51405954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c38dd0da5fb9be55744dbdfc895056e1c5e33edd01adbde39a997a878a511f`  
		Last Modified: Wed, 16 Oct 2024 04:19:48 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:364bad00eca83a084626d6145fa589e973df5978f1972255b5af001eee8654bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.2 MB (784244009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0145d5ec4d37eb11978212c957841941de63bde015aad96e690c6d73c9bba57`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7692d171772b08f5a9d0dc4a7b1ae51b870e77829dd8e7c0a62b1f9817239`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 1.2 MB (1198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f9119823a2bf386bf829a11e39290d3f3441a7210eb39b4a7342f8481643ac`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 5.3 MB (5342090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39a30d323d034154408ec363b1f3afbe72ed9d424be55808a92a6309b120d`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da5b2e66f57fc3b781b4d81c9514dee9b08decd9306330cd58833771758139`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70554c999e53a1aad7c55aafc6f0ddb8095bd7b1eb3c0dc38e07aec7896ae2cf`  
		Last Modified: Wed, 16 Oct 2024 04:13:13 GMT  
		Size: 171.5 MB (171452633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdb47098b878011f0003ad6c94e50363b2156e2bb6951fa21f9012a17f1bcf`  
		Last Modified: Wed, 16 Oct 2024 04:13:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2103d332713160aa2196205de34c2914b0072edd6edfd48482dbb2d4a3d6`  
		Last Modified: Wed, 16 Oct 2024 06:04:28 GMT  
		Size: 45.0 MB (44990886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38185782b6690ae35720744a5321274a8651237c9d6900cebc10a000409af2e5`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 331.3 KB (331287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843243ae0d09c7eda36f37ac0bc9801a113bf37beb05fae37942f88241e275c`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 897.3 KB (897322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db189cc6360c266d7a1ffd1e118ed31d7aa4d94fbf89e2b9f61d27b2d708de5`  
		Last Modified: Wed, 16 Oct 2024 07:02:30 GMT  
		Size: 534.1 MB (534054793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:2089ccdb5ec87560873e2f9d8e237f15e4cc8864ee9712ba7644899c84496df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51649410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5115b9310434c9796c32f026487d0c5585b7fe94d4198caee54e37ad186f9c`

```dockerfile
```

-	Layers:
	-	`sha256:4fd23be3534fa2862d1002174000006566928f2d321b781242cc41b027c4e398`  
		Last Modified: Wed, 16 Oct 2024 07:02:20 GMT  
		Size: 51.6 MB (51639952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cba67582c70ecd2b1eb3c0bc40ac7048edea9bc21f872b199feedd5079197cb`  
		Last Modified: Wed, 16 Oct 2024 07:02:18 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:d44729fa9c62ef25a7e2e1bed25587d3225fc00d87da7c2e62acbb83876f979e
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
$ docker pull ros@sha256:37d9069e76e6ff7e4899e02e133f275550f975b618e43549df2c843ee1125d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.2 MB (834246421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7c7f9e89ae9d0b865b4ffb142d11c42b76a112ed2b644bfed29df90e4b1ac`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627070c22110350c23cc50089a841b8c4257eb28ce66dea53acf5039c3230e34`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 1.2 MB (1198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8728cedb8ba29fe02ce989c70421066de64c666b6a99582f25178d88aa15436`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 5.4 MB (5361869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127793489f3bb50eb05db40cab2ed332c4a29fd05b34138da31541fbd7e63b1`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87538de7941b612134ab50edd68c6e0f52c6f7ddfedb7fb0c5130b6a6ca0ae77`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11090410af8961388a4a44a929c9fbc8eb6000dac2075e09c4392d7ec0a60ae4`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 177.0 MB (177040113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07f0bec1e43c18cd93acea1d11ffd7fc0409d8b06afa3a0c107f8ad80b105a`  
		Last Modified: Wed, 16 Oct 2024 16:18:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a60a3d4f5d8a2ba79f6b17c46970171ea46e7dbc4f8a206d7ce90d28b64e0`  
		Last Modified: Wed, 16 Oct 2024 16:52:11 GMT  
		Size: 50.7 MB (50721153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb065133b9b742d6bbbca49aa896b94a18f93aa7c33c890cfb3e6b73cb0f53`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 331.3 KB (331289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272267b4195536b2a923055b1e37c0166a7414c13ab20177450be71783a6c666`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 916.0 KB (915988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee6c6e59fce0e16d0f3d326f1d155c60b0e1299d05a50121e91e77b474e6b70`  
		Last Modified: Wed, 16 Oct 2024 17:40:05 GMT  
		Size: 571.2 MB (571163659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:484ae3d7703cd9196cd102483161d0b7186e59dbf22b85d5fab7de197db007e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51781537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bbb65726b8a9e050feb3fa92d0302d96cf814e80d52891abc6f3ba85b468e9`

```dockerfile
```

-	Layers:
	-	`sha256:45cf0bd887bfb0a9d0d4475ef23af02a232638c98c52991d04f2053de337d84f`  
		Last Modified: Wed, 16 Oct 2024 17:39:58 GMT  
		Size: 51.8 MB (51772160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2007b29cd2d3707f184206d8eb6d98b88ce3c07950eecade7713d537424a3fe3`  
		Last Modified: Wed, 16 Oct 2024 17:39:57 GMT  
		Size: 9.4 KB (9377 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:4e3c192434111446b5e289bbbbed4b0627f6b022d247614e1b5c615079df54c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.2 MB (725162922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6722522b64e2199faf06f62ebdd9ec102d857518c64fcb4f5f35c45544a5d9`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1949580a963a0afcdb9b0814bbfc7b5e0dc62740075d4abdb4a5b82b36229b`  
		Last Modified: Wed, 16 Oct 2024 04:19:59 GMT  
		Size: 496.9 MB (496874509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:2a56749f526b236ae91d2d30d45dad202afec2ebf09d945c1bb2f89b4bc5b13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51415392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91eadbd4a2c3aa9c33f9764822985eb8f3594865a0491e9c38c39618be6b98b0`

```dockerfile
```

-	Layers:
	-	`sha256:51c8eda415d83c183b49d4002ff8cc36d5a9a3613207945774f72915b53049f1`  
		Last Modified: Wed, 16 Oct 2024 04:19:50 GMT  
		Size: 51.4 MB (51405954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c38dd0da5fb9be55744dbdfc895056e1c5e33edd01adbde39a997a878a511f`  
		Last Modified: Wed, 16 Oct 2024 04:19:48 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:364bad00eca83a084626d6145fa589e973df5978f1972255b5af001eee8654bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.2 MB (784244009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0145d5ec4d37eb11978212c957841941de63bde015aad96e690c6d73c9bba57`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7692d171772b08f5a9d0dc4a7b1ae51b870e77829dd8e7c0a62b1f9817239`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 1.2 MB (1198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f9119823a2bf386bf829a11e39290d3f3441a7210eb39b4a7342f8481643ac`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 5.3 MB (5342090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39a30d323d034154408ec363b1f3afbe72ed9d424be55808a92a6309b120d`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da5b2e66f57fc3b781b4d81c9514dee9b08decd9306330cd58833771758139`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70554c999e53a1aad7c55aafc6f0ddb8095bd7b1eb3c0dc38e07aec7896ae2cf`  
		Last Modified: Wed, 16 Oct 2024 04:13:13 GMT  
		Size: 171.5 MB (171452633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdb47098b878011f0003ad6c94e50363b2156e2bb6951fa21f9012a17f1bcf`  
		Last Modified: Wed, 16 Oct 2024 04:13:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2103d332713160aa2196205de34c2914b0072edd6edfd48482dbb2d4a3d6`  
		Last Modified: Wed, 16 Oct 2024 06:04:28 GMT  
		Size: 45.0 MB (44990886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38185782b6690ae35720744a5321274a8651237c9d6900cebc10a000409af2e5`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 331.3 KB (331287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843243ae0d09c7eda36f37ac0bc9801a113bf37beb05fae37942f88241e275c`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 897.3 KB (897322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db189cc6360c266d7a1ffd1e118ed31d7aa4d94fbf89e2b9f61d27b2d708de5`  
		Last Modified: Wed, 16 Oct 2024 07:02:30 GMT  
		Size: 534.1 MB (534054793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:2089ccdb5ec87560873e2f9d8e237f15e4cc8864ee9712ba7644899c84496df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51649410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5115b9310434c9796c32f026487d0c5585b7fe94d4198caee54e37ad186f9c`

```dockerfile
```

-	Layers:
	-	`sha256:4fd23be3534fa2862d1002174000006566928f2d321b781242cc41b027c4e398`  
		Last Modified: Wed, 16 Oct 2024 07:02:20 GMT  
		Size: 51.6 MB (51639952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cba67582c70ecd2b1eb3c0bc40ac7048edea9bc21f872b199feedd5079197cb`  
		Last Modified: Wed, 16 Oct 2024 07:02:18 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:f937665254139ed2b8f4808ca4c548e2f2070cf5c608e59646b898d2a5f236d5
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
$ docker pull ros@sha256:d91e519e95f0b8b2db0b4cdd27fd945440d3188145ac8ee6f8076e298e30d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280008678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91424a21f01d49712381ed4ec9492922a1c592f0db2041adb37fb139d23294fb`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627070c22110350c23cc50089a841b8c4257eb28ce66dea53acf5039c3230e34`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 1.2 MB (1198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8728cedb8ba29fe02ce989c70421066de64c666b6a99582f25178d88aa15436`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 5.4 MB (5361869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127793489f3bb50eb05db40cab2ed332c4a29fd05b34138da31541fbd7e63b1`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87538de7941b612134ab50edd68c6e0f52c6f7ddfedb7fb0c5130b6a6ca0ae77`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11090410af8961388a4a44a929c9fbc8eb6000dac2075e09c4392d7ec0a60ae4`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 177.0 MB (177040113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07f0bec1e43c18cd93acea1d11ffd7fc0409d8b06afa3a0c107f8ad80b105a`  
		Last Modified: Wed, 16 Oct 2024 16:18:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a60a3d4f5d8a2ba79f6b17c46970171ea46e7dbc4f8a206d7ce90d28b64e0`  
		Last Modified: Wed, 16 Oct 2024 16:52:11 GMT  
		Size: 50.7 MB (50721153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb065133b9b742d6bbbca49aa896b94a18f93aa7c33c890cfb3e6b73cb0f53`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 331.3 KB (331289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272267b4195536b2a923055b1e37c0166a7414c13ab20177450be71783a6c666`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 916.0 KB (915988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9d9237bb39bb101226779bd2f01dab6f3b6aff4e0c8fc10c46469431cf4046`  
		Last Modified: Wed, 16 Oct 2024 17:36:40 GMT  
		Size: 16.9 MB (16925916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:3cf0b425d1c22db00808aeb39d5d3fde0d4c6e39884070e8146afd788f768dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29491473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ac62215124cb3578c207e6bd59eb20bd2e39d0f9bda4dbbc9941c26e96e0da`

```dockerfile
```

-	Layers:
	-	`sha256:34dcef24a3df80a39bae3735bf5e3f9b3fa6f890723da83cfe868a9cb3fb217f`  
		Last Modified: Wed, 16 Oct 2024 17:36:40 GMT  
		Size: 29.5 MB (29482145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06faaa779bface7b979a8bb2887c7c3afec9c59dd4fd4099851c90bf5426166`  
		Last Modified: Wed, 16 Oct 2024 17:36:39 GMT  
		Size: 9.3 KB (9328 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:e66a7229a6e41943d5d92e32ced3e41419860b76577ae17ae49ba0fc3c67fdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243313694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad79328eaa1883562a8fbae9d2c4d9d0385591e22c72bad81e62ded14ffe5fb5`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a516110ed97a8a9c62bc914fa45ffa19c58e02fc5aa3b09f5f24402e2014fb5`  
		Last Modified: Wed, 16 Oct 2024 04:07:09 GMT  
		Size: 15.0 MB (15025281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:68570be7ced8626254f62462eeb9bf9b465048b44fecc79effdef5f9832b7262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29246325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b71494b6d37b215bf54b5a742df626a31af502742d8a95164c4c62e6174c1`

```dockerfile
```

-	Layers:
	-	`sha256:32b49dd89be20c5af9d2aab4e96989d4572aa7ee7094c8a4e7e95d01ebc770f7`  
		Last Modified: Wed, 16 Oct 2024 04:07:09 GMT  
		Size: 29.2 MB (29236935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb4bda7c098c3bbf1cc0d3c49cc430385167dc11410dddb7b747b5ae1e4c517`  
		Last Modified: Wed, 16 Oct 2024 04:07:07 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a2656272b0d5a0339bb058920703f0e459958a14a563fd5399f30400463f95fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266714763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23da81ce6994f2b702cbb2eb2e3cb1061e85cde4cae8c6ea5f2b85042e3e7e22`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7692d171772b08f5a9d0dc4a7b1ae51b870e77829dd8e7c0a62b1f9817239`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 1.2 MB (1198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f9119823a2bf386bf829a11e39290d3f3441a7210eb39b4a7342f8481643ac`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 5.3 MB (5342090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39a30d323d034154408ec363b1f3afbe72ed9d424be55808a92a6309b120d`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da5b2e66f57fc3b781b4d81c9514dee9b08decd9306330cd58833771758139`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70554c999e53a1aad7c55aafc6f0ddb8095bd7b1eb3c0dc38e07aec7896ae2cf`  
		Last Modified: Wed, 16 Oct 2024 04:13:13 GMT  
		Size: 171.5 MB (171452633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdb47098b878011f0003ad6c94e50363b2156e2bb6951fa21f9012a17f1bcf`  
		Last Modified: Wed, 16 Oct 2024 04:13:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2103d332713160aa2196205de34c2914b0072edd6edfd48482dbb2d4a3d6`  
		Last Modified: Wed, 16 Oct 2024 06:04:28 GMT  
		Size: 45.0 MB (44990886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38185782b6690ae35720744a5321274a8651237c9d6900cebc10a000409af2e5`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 331.3 KB (331287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843243ae0d09c7eda36f37ac0bc9801a113bf37beb05fae37942f88241e275c`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 897.3 KB (897322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562ebad0d899b2bb76a94924c63b4828f32ec62d002e22bb27c12ef016824b17`  
		Last Modified: Wed, 16 Oct 2024 06:51:19 GMT  
		Size: 16.5 MB (16525547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:5e0c69f753483a9b0aac48698d4332e7dd42daef7d96b5d8f966d3ba1af2a7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29440689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703aba797d97946e2f244b1a36067f5cb7dea8e33bdb3644600e74634560ad2b`

```dockerfile
```

-	Layers:
	-	`sha256:03d0a06781a1903992c1a35c53b2b80c4e66ece9bb6315275774522a7804df6e`  
		Last Modified: Wed, 16 Oct 2024 06:51:19 GMT  
		Size: 29.4 MB (29431279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aaba00a0cedf7f43546495e768fea4c0730efda9d4d573bbd8882fc6494f149`  
		Last Modified: Wed, 16 Oct 2024 06:51:18 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:f937665254139ed2b8f4808ca4c548e2f2070cf5c608e59646b898d2a5f236d5
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
$ docker pull ros@sha256:d91e519e95f0b8b2db0b4cdd27fd945440d3188145ac8ee6f8076e298e30d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280008678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91424a21f01d49712381ed4ec9492922a1c592f0db2041adb37fb139d23294fb`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627070c22110350c23cc50089a841b8c4257eb28ce66dea53acf5039c3230e34`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 1.2 MB (1198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8728cedb8ba29fe02ce989c70421066de64c666b6a99582f25178d88aa15436`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 5.4 MB (5361869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127793489f3bb50eb05db40cab2ed332c4a29fd05b34138da31541fbd7e63b1`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87538de7941b612134ab50edd68c6e0f52c6f7ddfedb7fb0c5130b6a6ca0ae77`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11090410af8961388a4a44a929c9fbc8eb6000dac2075e09c4392d7ec0a60ae4`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 177.0 MB (177040113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07f0bec1e43c18cd93acea1d11ffd7fc0409d8b06afa3a0c107f8ad80b105a`  
		Last Modified: Wed, 16 Oct 2024 16:18:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a60a3d4f5d8a2ba79f6b17c46970171ea46e7dbc4f8a206d7ce90d28b64e0`  
		Last Modified: Wed, 16 Oct 2024 16:52:11 GMT  
		Size: 50.7 MB (50721153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb065133b9b742d6bbbca49aa896b94a18f93aa7c33c890cfb3e6b73cb0f53`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 331.3 KB (331289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272267b4195536b2a923055b1e37c0166a7414c13ab20177450be71783a6c666`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 916.0 KB (915988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9d9237bb39bb101226779bd2f01dab6f3b6aff4e0c8fc10c46469431cf4046`  
		Last Modified: Wed, 16 Oct 2024 17:36:40 GMT  
		Size: 16.9 MB (16925916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:3cf0b425d1c22db00808aeb39d5d3fde0d4c6e39884070e8146afd788f768dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29491473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ac62215124cb3578c207e6bd59eb20bd2e39d0f9bda4dbbc9941c26e96e0da`

```dockerfile
```

-	Layers:
	-	`sha256:34dcef24a3df80a39bae3735bf5e3f9b3fa6f890723da83cfe868a9cb3fb217f`  
		Last Modified: Wed, 16 Oct 2024 17:36:40 GMT  
		Size: 29.5 MB (29482145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06faaa779bface7b979a8bb2887c7c3afec9c59dd4fd4099851c90bf5426166`  
		Last Modified: Wed, 16 Oct 2024 17:36:39 GMT  
		Size: 9.3 KB (9328 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:e66a7229a6e41943d5d92e32ced3e41419860b76577ae17ae49ba0fc3c67fdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243313694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad79328eaa1883562a8fbae9d2c4d9d0385591e22c72bad81e62ded14ffe5fb5`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a516110ed97a8a9c62bc914fa45ffa19c58e02fc5aa3b09f5f24402e2014fb5`  
		Last Modified: Wed, 16 Oct 2024 04:07:09 GMT  
		Size: 15.0 MB (15025281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:68570be7ced8626254f62462eeb9bf9b465048b44fecc79effdef5f9832b7262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29246325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b71494b6d37b215bf54b5a742df626a31af502742d8a95164c4c62e6174c1`

```dockerfile
```

-	Layers:
	-	`sha256:32b49dd89be20c5af9d2aab4e96989d4572aa7ee7094c8a4e7e95d01ebc770f7`  
		Last Modified: Wed, 16 Oct 2024 04:07:09 GMT  
		Size: 29.2 MB (29236935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb4bda7c098c3bbf1cc0d3c49cc430385167dc11410dddb7b747b5ae1e4c517`  
		Last Modified: Wed, 16 Oct 2024 04:07:07 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a2656272b0d5a0339bb058920703f0e459958a14a563fd5399f30400463f95fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266714763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23da81ce6994f2b702cbb2eb2e3cb1061e85cde4cae8c6ea5f2b85042e3e7e22`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7692d171772b08f5a9d0dc4a7b1ae51b870e77829dd8e7c0a62b1f9817239`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 1.2 MB (1198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f9119823a2bf386bf829a11e39290d3f3441a7210eb39b4a7342f8481643ac`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 5.3 MB (5342090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39a30d323d034154408ec363b1f3afbe72ed9d424be55808a92a6309b120d`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da5b2e66f57fc3b781b4d81c9514dee9b08decd9306330cd58833771758139`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70554c999e53a1aad7c55aafc6f0ddb8095bd7b1eb3c0dc38e07aec7896ae2cf`  
		Last Modified: Wed, 16 Oct 2024 04:13:13 GMT  
		Size: 171.5 MB (171452633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdb47098b878011f0003ad6c94e50363b2156e2bb6951fa21f9012a17f1bcf`  
		Last Modified: Wed, 16 Oct 2024 04:13:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2103d332713160aa2196205de34c2914b0072edd6edfd48482dbb2d4a3d6`  
		Last Modified: Wed, 16 Oct 2024 06:04:28 GMT  
		Size: 45.0 MB (44990886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38185782b6690ae35720744a5321274a8651237c9d6900cebc10a000409af2e5`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 331.3 KB (331287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843243ae0d09c7eda36f37ac0bc9801a113bf37beb05fae37942f88241e275c`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 897.3 KB (897322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562ebad0d899b2bb76a94924c63b4828f32ec62d002e22bb27c12ef016824b17`  
		Last Modified: Wed, 16 Oct 2024 06:51:19 GMT  
		Size: 16.5 MB (16525547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:5e0c69f753483a9b0aac48698d4332e7dd42daef7d96b5d8f966d3ba1af2a7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29440689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703aba797d97946e2f244b1a36067f5cb7dea8e33bdb3644600e74634560ad2b`

```dockerfile
```

-	Layers:
	-	`sha256:03d0a06781a1903992c1a35c53b2b80c4e66ece9bb6315275774522a7804df6e`  
		Last Modified: Wed, 16 Oct 2024 06:51:19 GMT  
		Size: 29.4 MB (29431279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aaba00a0cedf7f43546495e768fea4c0730efda9d4d573bbd8882fc6494f149`  
		Last Modified: Wed, 16 Oct 2024 06:51:18 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:456b9a58b63e259c388fb59d8f6c1db6b17967f7b515ebb5aefffb4eb2fba888
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
$ docker pull ros@sha256:24ff52d34ab601679f1c783ddc76ab65d0ed3abe011969b659e12544320e5529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263082762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36930c7e3fb8d74fc8caf149572e686ff6536ecbce01e6fce4def98bea7cf5c`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627070c22110350c23cc50089a841b8c4257eb28ce66dea53acf5039c3230e34`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 1.2 MB (1198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8728cedb8ba29fe02ce989c70421066de64c666b6a99582f25178d88aa15436`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 5.4 MB (5361869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127793489f3bb50eb05db40cab2ed332c4a29fd05b34138da31541fbd7e63b1`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87538de7941b612134ab50edd68c6e0f52c6f7ddfedb7fb0c5130b6a6ca0ae77`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11090410af8961388a4a44a929c9fbc8eb6000dac2075e09c4392d7ec0a60ae4`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 177.0 MB (177040113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07f0bec1e43c18cd93acea1d11ffd7fc0409d8b06afa3a0c107f8ad80b105a`  
		Last Modified: Wed, 16 Oct 2024 16:18:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a60a3d4f5d8a2ba79f6b17c46970171ea46e7dbc4f8a206d7ce90d28b64e0`  
		Last Modified: Wed, 16 Oct 2024 16:52:11 GMT  
		Size: 50.7 MB (50721153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb065133b9b742d6bbbca49aa896b94a18f93aa7c33c890cfb3e6b73cb0f53`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 331.3 KB (331289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272267b4195536b2a923055b1e37c0166a7414c13ab20177450be71783a6c666`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 916.0 KB (915988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:7534e1102db6fa8364771006961a05c05197aef2de7c978b00e7a2bcfe12faa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27608503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0012e651d7967eb1bba01aa0e7b560e68f0fbd9aaeadc0096126b1f561db4ef6`

```dockerfile
```

-	Layers:
	-	`sha256:c9912d0d53a7c301dc7275a2f952e6f82b44921b0248bdfc4d4cd4c958bd7126`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 27.6 MB (27594813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7118bcec179b41f121295fec5f259cde05401067095f8b0f6c22535897169636`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 13.7 KB (13690 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:665efd9c21f6e7dd7e1ecd97e6f9b421775e63b55167828fb04dfdeff26aa088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228288413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bd77e448977f3464d7b7411f33d0f7e7db4181e0c68af48c71a9bd3c34404b`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:9bc66574adabc536cff0ca51f33d6a859efc2166256401492dbe4d2c742aeb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27371952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778fd253c2c9f0084aad03ac5f3d8d49a375c0ac42f7d25966b0cc12d841f319`

```dockerfile
```

-	Layers:
	-	`sha256:158c083e6830094fc49e0429b98e613165957001bccd5c321f312f6b09d3e584`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 27.4 MB (27358168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed656d35de762e9baed95088a4d31b34a03cdc9ad04dccbd81dc4ea4b1763cc`  
		Last Modified: Wed, 16 Oct 2024 03:18:50 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e317c94efc821597009d9fb3fa5a0db8fee08a8a9d010852986b9c13e6988c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250189216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03e6c05479a847440a256d79340ecccf68bee3d3c012b07dbf18b94a8d13193`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7692d171772b08f5a9d0dc4a7b1ae51b870e77829dd8e7c0a62b1f9817239`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 1.2 MB (1198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f9119823a2bf386bf829a11e39290d3f3441a7210eb39b4a7342f8481643ac`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 5.3 MB (5342090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39a30d323d034154408ec363b1f3afbe72ed9d424be55808a92a6309b120d`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da5b2e66f57fc3b781b4d81c9514dee9b08decd9306330cd58833771758139`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70554c999e53a1aad7c55aafc6f0ddb8095bd7b1eb3c0dc38e07aec7896ae2cf`  
		Last Modified: Wed, 16 Oct 2024 04:13:13 GMT  
		Size: 171.5 MB (171452633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdb47098b878011f0003ad6c94e50363b2156e2bb6951fa21f9012a17f1bcf`  
		Last Modified: Wed, 16 Oct 2024 04:13:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2103d332713160aa2196205de34c2914b0072edd6edfd48482dbb2d4a3d6`  
		Last Modified: Wed, 16 Oct 2024 06:04:28 GMT  
		Size: 45.0 MB (44990886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38185782b6690ae35720744a5321274a8651237c9d6900cebc10a000409af2e5`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 331.3 KB (331287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843243ae0d09c7eda36f37ac0bc9801a113bf37beb05fae37942f88241e275c`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 897.3 KB (897322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d7f07c89fc0129e2bc9f71244b1268d8bb57d4dd4bb75c39e92aff6bb4f70694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27558911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b6391e8cfeba2048a60ff13c4dd745bfca46b0d85bce4c5e87c1cc065abe62`

```dockerfile
```

-	Layers:
	-	`sha256:8dc7119ced5dc25252d4e6119082fe12de268a860443343a56495e723d0bca38`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 27.5 MB (27545099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e2265e87cc5692dd2c4402c7bbff074b3cf227f920f9cc95d923bbccec1eb7`  
		Last Modified: Wed, 16 Oct 2024 06:04:26 GMT  
		Size: 13.8 KB (13812 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:456b9a58b63e259c388fb59d8f6c1db6b17967f7b515ebb5aefffb4eb2fba888
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
$ docker pull ros@sha256:24ff52d34ab601679f1c783ddc76ab65d0ed3abe011969b659e12544320e5529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263082762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36930c7e3fb8d74fc8caf149572e686ff6536ecbce01e6fce4def98bea7cf5c`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627070c22110350c23cc50089a841b8c4257eb28ce66dea53acf5039c3230e34`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 1.2 MB (1198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8728cedb8ba29fe02ce989c70421066de64c666b6a99582f25178d88aa15436`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 5.4 MB (5361869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127793489f3bb50eb05db40cab2ed332c4a29fd05b34138da31541fbd7e63b1`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87538de7941b612134ab50edd68c6e0f52c6f7ddfedb7fb0c5130b6a6ca0ae77`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11090410af8961388a4a44a929c9fbc8eb6000dac2075e09c4392d7ec0a60ae4`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 177.0 MB (177040113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07f0bec1e43c18cd93acea1d11ffd7fc0409d8b06afa3a0c107f8ad80b105a`  
		Last Modified: Wed, 16 Oct 2024 16:18:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a60a3d4f5d8a2ba79f6b17c46970171ea46e7dbc4f8a206d7ce90d28b64e0`  
		Last Modified: Wed, 16 Oct 2024 16:52:11 GMT  
		Size: 50.7 MB (50721153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb065133b9b742d6bbbca49aa896b94a18f93aa7c33c890cfb3e6b73cb0f53`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 331.3 KB (331289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272267b4195536b2a923055b1e37c0166a7414c13ab20177450be71783a6c666`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 916.0 KB (915988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:7534e1102db6fa8364771006961a05c05197aef2de7c978b00e7a2bcfe12faa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27608503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0012e651d7967eb1bba01aa0e7b560e68f0fbd9aaeadc0096126b1f561db4ef6`

```dockerfile
```

-	Layers:
	-	`sha256:c9912d0d53a7c301dc7275a2f952e6f82b44921b0248bdfc4d4cd4c958bd7126`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 27.6 MB (27594813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7118bcec179b41f121295fec5f259cde05401067095f8b0f6c22535897169636`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 13.7 KB (13690 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:665efd9c21f6e7dd7e1ecd97e6f9b421775e63b55167828fb04dfdeff26aa088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228288413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bd77e448977f3464d7b7411f33d0f7e7db4181e0c68af48c71a9bd3c34404b`
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
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:9bc66574adabc536cff0ca51f33d6a859efc2166256401492dbe4d2c742aeb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27371952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778fd253c2c9f0084aad03ac5f3d8d49a375c0ac42f7d25966b0cc12d841f319`

```dockerfile
```

-	Layers:
	-	`sha256:158c083e6830094fc49e0429b98e613165957001bccd5c321f312f6b09d3e584`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 27.4 MB (27358168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed656d35de762e9baed95088a4d31b34a03cdc9ad04dccbd81dc4ea4b1763cc`  
		Last Modified: Wed, 16 Oct 2024 03:18:50 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e317c94efc821597009d9fb3fa5a0db8fee08a8a9d010852986b9c13e6988c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250189216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03e6c05479a847440a256d79340ecccf68bee3d3c012b07dbf18b94a8d13193`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7692d171772b08f5a9d0dc4a7b1ae51b870e77829dd8e7c0a62b1f9817239`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 1.2 MB (1198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f9119823a2bf386bf829a11e39290d3f3441a7210eb39b4a7342f8481643ac`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 5.3 MB (5342090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39a30d323d034154408ec363b1f3afbe72ed9d424be55808a92a6309b120d`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da5b2e66f57fc3b781b4d81c9514dee9b08decd9306330cd58833771758139`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70554c999e53a1aad7c55aafc6f0ddb8095bd7b1eb3c0dc38e07aec7896ae2cf`  
		Last Modified: Wed, 16 Oct 2024 04:13:13 GMT  
		Size: 171.5 MB (171452633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdb47098b878011f0003ad6c94e50363b2156e2bb6951fa21f9012a17f1bcf`  
		Last Modified: Wed, 16 Oct 2024 04:13:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2103d332713160aa2196205de34c2914b0072edd6edfd48482dbb2d4a3d6`  
		Last Modified: Wed, 16 Oct 2024 06:04:28 GMT  
		Size: 45.0 MB (44990886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38185782b6690ae35720744a5321274a8651237c9d6900cebc10a000409af2e5`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 331.3 KB (331287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843243ae0d09c7eda36f37ac0bc9801a113bf37beb05fae37942f88241e275c`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 897.3 KB (897322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:d7f07c89fc0129e2bc9f71244b1268d8bb57d4dd4bb75c39e92aff6bb4f70694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27558911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b6391e8cfeba2048a60ff13c4dd745bfca46b0d85bce4c5e87c1cc065abe62`

```dockerfile
```

-	Layers:
	-	`sha256:8dc7119ced5dc25252d4e6119082fe12de268a860443343a56495e723d0bca38`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 27.5 MB (27545099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e2265e87cc5692dd2c4402c7bbff074b3cf227f920f9cc95d923bbccec1eb7`  
		Last Modified: Wed, 16 Oct 2024 06:04:26 GMT  
		Size: 13.8 KB (13812 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:4e654b1839d79e613d0a393fc49c5bdb01a0a7aa8dac5517804ee57a4815ebb8
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
$ docker pull ros@sha256:7d6ca3817633bb47b79586aa8e706ddb7f042871e5942b2704b701eaa42c1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216275831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eba44f69107ee478fe9cdcdcf61af311b30cd2e2238cd7bcfdd450f467d08cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7281aa604e720b5eaf7e72404849690d72fa5effb15608d2a303b3882f13c9dc`  
		Last Modified: Mon, 10 Mar 2025 18:14:14 GMT  
		Size: 1.2 MB (1191587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a18ba426e6ea26c8fd790e38fecd6025373c25669dd4315eeb94f7ed6599d`  
		Last Modified: Mon, 10 Mar 2025 18:14:14 GMT  
		Size: 5.4 MB (5361910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e537c3c3ddc4adb3cc0de8338089b7d98cf338a1a97a138514e61d335c0a0ddf`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493688bad29a80f481679ba66e7b0d6fcb8fd23852d6436d0d44395070278bf5`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23863567396658bbea590c4eba5622c43ca5757b6235b1c39638f702d1783627`  
		Last Modified: Mon, 10 Mar 2025 18:14:20 GMT  
		Size: 182.2 MB (182208805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab278496cd9deb6d829558f60bad9417912d96a69106575b781f28c587248b6`  
		Last Modified: Mon, 10 Mar 2025 18:14:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1cee193e3cf55a547b51bf7b9cd93b5cda6cc68af4c78689dfe8dcfff3d3007e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6679ee1502c9df3be8dad2bdc9989cc8c76d1c92ef7058373ad233d522ff006d`

```dockerfile
```

-	Layers:
	-	`sha256:ed70aa069ce6da22da1f2b5c384617667bb87a6ecf8b9a3a9f328507e25c6114`  
		Last Modified: Mon, 10 Mar 2025 18:14:15 GMT  
		Size: 26.1 MB (26125935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fbde5065217803f7c41c39a3e63e07859f8027fb2b78dd749b165ccee46493`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 16.4 KB (16376 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:67dd1583c8a38e517b3953bab5bd4ae4a131d8a7b759eecb1d0019627e97e3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191225876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dfeb0e7c29ad80d58da20b821ad53923a89344a32967371c19e30c4be88f4d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63403fc54a5c95851d7b7b8c40144a5f9a318cee65813dfc14eefc11288ef1ac`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 1.2 MB (1191602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7a32017f42f62156bbd13034c1e560d3c291b3c7d26b31a2a57871131c347`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 4.5 MB (4487460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eb69a80d32b5cdb468886f797acdf344eee06f2f9f6510e9d48a41316f3fd0`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d74eccd6b688697b2abb8ed4135c32d6faf5a9c10eeb053f449ad68fa905c`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254f2e42a794615ac4855d623b55a398152062f1f9e286f1c15fe9c7042b870`  
		Last Modified: Mon, 10 Mar 2025 18:22:03 GMT  
		Size: 161.9 MB (161923934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac45b8cd6234ec64252da29a03ffda622d8cb517602f6f5af6d4956033de55d`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:063537f27200090830b26f444de82ce21f42d3ff7e4f8c1b8a1f318ed3682923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26055405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362c61cfa73d7232b534164bb603ae5fb41313922a61b5f964885d6ce69638e0`

```dockerfile
```

-	Layers:
	-	`sha256:05e6a6902d0f9a30c5f7c9fa2748ffa839bbe323e1f074da0349f1e8c8df08d5`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 26.0 MB (26038916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62411d0dbf00af3dd535c69dcba9dd0eded57daff34b54aa9a6e95e6cc0125ab`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 16.5 KB (16489 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8f4841dced005577d18cd81b26f1fcc8a02132b497876e3aa89e53e21cc34ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208220339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d426ded96d38709672df6adcda90679455d55634253e5d4fb53da2054cb59c4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2121f1f68d1125f94e05d5d5f8eb016a4d81ece6993d4e7c57bfe5ad26044844`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 1.2 MB (1191456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88b5cd2df85b5bf6fb6fb1ce3368e75445a74bb65bca8e0b7c862ee326d6a7`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 5.3 MB (5342153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc415fb12ec5c88f126a927064c087cfe92feb936886efa41626024d640a7ce1`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c2b989b81c9cede611618c4b68d5118f857fe6d7eb371449bfe5467122384a`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4605f7e1eea47d341d92031419819b83d0405500f6bf1c118e732be197d7e9a`  
		Last Modified: Mon, 10 Mar 2025 18:29:24 GMT  
		Size: 175.7 MB (175710430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca092e0891945ffc24a56747a902585fab1a46bf29aa20e37747360dead81d5`  
		Last Modified: Mon, 10 Mar 2025 18:29:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:75cde1ea8a736c0b29eb43e3e31d960a4963e35585d045a23a34443b06706b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d9076878575223ebd5faad124520b2761a94459fb98822734c28f591827f7d`

```dockerfile
```

-	Layers:
	-	`sha256:f6f7ebe863d8066db648f08ba919f1c3db871a36b1a5608ec0a7cb2a902095ae`  
		Last Modified: Mon, 10 Mar 2025 18:29:18 GMT  
		Size: 26.0 MB (26047668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23866d8db4dff5fe835c471621039286a99ed5f4bb75312ec0d70bf47b0a7b92`  
		Last Modified: Mon, 10 Mar 2025 18:29:16 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:4e654b1839d79e613d0a393fc49c5bdb01a0a7aa8dac5517804ee57a4815ebb8
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
$ docker pull ros@sha256:7d6ca3817633bb47b79586aa8e706ddb7f042871e5942b2704b701eaa42c1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216275831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eba44f69107ee478fe9cdcdcf61af311b30cd2e2238cd7bcfdd450f467d08cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7281aa604e720b5eaf7e72404849690d72fa5effb15608d2a303b3882f13c9dc`  
		Last Modified: Mon, 10 Mar 2025 18:14:14 GMT  
		Size: 1.2 MB (1191587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a18ba426e6ea26c8fd790e38fecd6025373c25669dd4315eeb94f7ed6599d`  
		Last Modified: Mon, 10 Mar 2025 18:14:14 GMT  
		Size: 5.4 MB (5361910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e537c3c3ddc4adb3cc0de8338089b7d98cf338a1a97a138514e61d335c0a0ddf`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493688bad29a80f481679ba66e7b0d6fcb8fd23852d6436d0d44395070278bf5`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23863567396658bbea590c4eba5622c43ca5757b6235b1c39638f702d1783627`  
		Last Modified: Mon, 10 Mar 2025 18:14:20 GMT  
		Size: 182.2 MB (182208805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab278496cd9deb6d829558f60bad9417912d96a69106575b781f28c587248b6`  
		Last Modified: Mon, 10 Mar 2025 18:14:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1cee193e3cf55a547b51bf7b9cd93b5cda6cc68af4c78689dfe8dcfff3d3007e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6679ee1502c9df3be8dad2bdc9989cc8c76d1c92ef7058373ad233d522ff006d`

```dockerfile
```

-	Layers:
	-	`sha256:ed70aa069ce6da22da1f2b5c384617667bb87a6ecf8b9a3a9f328507e25c6114`  
		Last Modified: Mon, 10 Mar 2025 18:14:15 GMT  
		Size: 26.1 MB (26125935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fbde5065217803f7c41c39a3e63e07859f8027fb2b78dd749b165ccee46493`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 16.4 KB (16376 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:67dd1583c8a38e517b3953bab5bd4ae4a131d8a7b759eecb1d0019627e97e3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191225876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dfeb0e7c29ad80d58da20b821ad53923a89344a32967371c19e30c4be88f4d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63403fc54a5c95851d7b7b8c40144a5f9a318cee65813dfc14eefc11288ef1ac`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 1.2 MB (1191602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7a32017f42f62156bbd13034c1e560d3c291b3c7d26b31a2a57871131c347`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 4.5 MB (4487460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eb69a80d32b5cdb468886f797acdf344eee06f2f9f6510e9d48a41316f3fd0`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d74eccd6b688697b2abb8ed4135c32d6faf5a9c10eeb053f449ad68fa905c`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254f2e42a794615ac4855d623b55a398152062f1f9e286f1c15fe9c7042b870`  
		Last Modified: Mon, 10 Mar 2025 18:22:03 GMT  
		Size: 161.9 MB (161923934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac45b8cd6234ec64252da29a03ffda622d8cb517602f6f5af6d4956033de55d`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:063537f27200090830b26f444de82ce21f42d3ff7e4f8c1b8a1f318ed3682923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26055405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362c61cfa73d7232b534164bb603ae5fb41313922a61b5f964885d6ce69638e0`

```dockerfile
```

-	Layers:
	-	`sha256:05e6a6902d0f9a30c5f7c9fa2748ffa839bbe323e1f074da0349f1e8c8df08d5`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 26.0 MB (26038916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62411d0dbf00af3dd535c69dcba9dd0eded57daff34b54aa9a6e95e6cc0125ab`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 16.5 KB (16489 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8f4841dced005577d18cd81b26f1fcc8a02132b497876e3aa89e53e21cc34ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208220339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d426ded96d38709672df6adcda90679455d55634253e5d4fb53da2054cb59c4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2121f1f68d1125f94e05d5d5f8eb016a4d81ece6993d4e7c57bfe5ad26044844`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 1.2 MB (1191456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88b5cd2df85b5bf6fb6fb1ce3368e75445a74bb65bca8e0b7c862ee326d6a7`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 5.3 MB (5342153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc415fb12ec5c88f126a927064c087cfe92feb936886efa41626024d640a7ce1`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c2b989b81c9cede611618c4b68d5118f857fe6d7eb371449bfe5467122384a`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4605f7e1eea47d341d92031419819b83d0405500f6bf1c118e732be197d7e9a`  
		Last Modified: Mon, 10 Mar 2025 18:29:24 GMT  
		Size: 175.7 MB (175710430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca092e0891945ffc24a56747a902585fab1a46bf29aa20e37747360dead81d5`  
		Last Modified: Mon, 10 Mar 2025 18:29:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:75cde1ea8a736c0b29eb43e3e31d960a4963e35585d045a23a34443b06706b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d9076878575223ebd5faad124520b2761a94459fb98822734c28f591827f7d`

```dockerfile
```

-	Layers:
	-	`sha256:f6f7ebe863d8066db648f08ba919f1c3db871a36b1a5608ec0a7cb2a902095ae`  
		Last Modified: Mon, 10 Mar 2025 18:29:18 GMT  
		Size: 26.0 MB (26047668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23866d8db4dff5fe835c471621039286a99ed5f4bb75312ec0d70bf47b0a7b92`  
		Last Modified: Mon, 10 Mar 2025 18:29:16 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:42f7b5ac83c674286dcc2e055226b8fb6deff6f2dcc57e82f58dc7b6ac335f96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:9ea1938d30d851fa79df496aeca4d144b2492a1155b7c063e9da80e7f73ebc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298690837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73009468a2afb304f6c7660197b1d222909f4754d698f432e4b91690683df5a5`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3b2484efd73305009117d35bdc14769dac7cc55a59591b622561a50646fbc`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 683.9 KB (683912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9ee196cfb19dc0d61a08117b1827bc75c1072281719ccd336f9acb1b3c93cd`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 3.6 MB (3560517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d977c02a44f1802debe1eee8710a41198847b4c0d9e6ea5c4a9e893d37a19c8`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2dc8ecf92fab78948452397647f0e17ff6de87b314612dd9030f699ce17b85`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a665f5b789f6618a5b5333bfaeced39dfa1da05d2fc4bcbe994b40c0050630`  
		Last Modified: Sat, 16 Nov 2024 02:57:59 GMT  
		Size: 122.7 MB (122680298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f731aa396c65b6542509fea891d58ddab177bae76da2dbcb1dbeecf8be19de`  
		Last Modified: Sat, 16 Nov 2024 02:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2931749fcbc5a8423464f2953dac75c839bba7110eb40057b47c9609f91bb21`  
		Last Modified: Sat, 16 Nov 2024 03:51:21 GMT  
		Size: 114.1 MB (114148980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db366bc2268cda50986b7cae4fa1ddabd7b92d8a85d54daad5f28244f0442207`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 326.7 KB (326714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402345e6fb621ea7619b1d18f51c5deb245660494444030ab446d6990881169b`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf1712afa1cbeccd1a8995ce8a47f9c4754bd0b3c4127270986815107f4f39`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 27.5 MB (27533744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:8605e5d64f9bf695bd474e9eaa1984c153a4a977d27d4472c5467be934d6a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23938670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306f92f38f4937f45e8ebaf2fade1ee690fa3b0c3332f161cb7301e12b15448b`

```dockerfile
```

-	Layers:
	-	`sha256:00a0a36b7f27c40b04d0159f5793a5e9b6bb1a08fd3559c4947bae0096b5555d`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 23.9 MB (23921497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaaa58a5ef3f1a86a2da48bd9e723d2576dc7e62838c6bfc6942c577ffdbbfb`  
		Last Modified: Sat, 16 Nov 2024 03:51:14 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3816010eca888366190324e68b6f07908e34a99af9de61e47d8e2447a9306643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288675915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f59d954e709ebeb4b464484a200658dce24ed33b71a0505ffd44a9622f54a`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81328307e6050d58a3786b0d8d4e0e280336fcbe5e12ed33eafac0e62f39b3c6`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 684.0 KB (683965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dc71d0f9b404e0afdeede800f6310ebab3be587e6a707bfd42f238d09438d`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336756432be3b9f7f44dd7afbc515faeb978872819b168b6908d418b86736edb`  
		Last Modified: Sat, 16 Nov 2024 03:42:13 GMT  
		Size: 117.5 MB (117515664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870e1f30b2d734ef09cf0ddbc60a50570d5c677f7f244597cd0092ccc28a9734`  
		Last Modified: Sat, 16 Nov 2024 03:42:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6924bb4685c143af5e2bec8959405bd94b82464901eb4ebdd3aedde9908dd1aa`  
		Last Modified: Sat, 16 Nov 2024 04:50:07 GMT  
		Size: 111.0 MB (111007847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7125737b4604e0deee24622b4f35e76bb2a81ea469185a71a4f100a1b17a02b`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 326.7 KB (326708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0549a9b72e086e413b36d2ba5a9a97fc7e361f45714c5af076739e3a30b02d`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8e30c16d2403bfc5a15fba00e5199f46f4591a1eee5d2275906979cf66b30`  
		Last Modified: Sat, 16 Nov 2024 04:50:06 GMT  
		Size: 26.7 MB (26685018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:168cc9da852dfd921589fd0ef6c9923580989080fdb3a1cbe3c38a8e0e2632af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23961372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc732bd5a1356f65079513c8c21328422fc745eb346c6df8edc093784223f083`

```dockerfile
```

-	Layers:
	-	`sha256:2bde361a6a2dac60ee9f7699306abdf35f518b420977d20f3dea5be3d351daae`  
		Last Modified: Sat, 16 Nov 2024 04:50:05 GMT  
		Size: 23.9 MB (23944062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450cfc3d353da63b52ae578cbdf62d291199fe48b1d634f73e1bb91c24ada593`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:fd4856890f393fb9decea5e8702aafbd5532b5ecf07b2706f6aa01e40fe100ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:315337a06b69f6678c8773374eddf8aa35e1ab56384f4a31bbb0b8c80a94261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622519658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4217e8facf7ecdc1b6d5742e89554806b21854b5d2d29920d2eabcfb38e2f806`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3b2484efd73305009117d35bdc14769dac7cc55a59591b622561a50646fbc`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 683.9 KB (683912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9ee196cfb19dc0d61a08117b1827bc75c1072281719ccd336f9acb1b3c93cd`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 3.6 MB (3560517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d977c02a44f1802debe1eee8710a41198847b4c0d9e6ea5c4a9e893d37a19c8`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2dc8ecf92fab78948452397647f0e17ff6de87b314612dd9030f699ce17b85`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a665f5b789f6618a5b5333bfaeced39dfa1da05d2fc4bcbe994b40c0050630`  
		Last Modified: Sat, 16 Nov 2024 02:57:59 GMT  
		Size: 122.7 MB (122680298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f731aa396c65b6542509fea891d58ddab177bae76da2dbcb1dbeecf8be19de`  
		Last Modified: Sat, 16 Nov 2024 02:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2931749fcbc5a8423464f2953dac75c839bba7110eb40057b47c9609f91bb21`  
		Last Modified: Sat, 16 Nov 2024 03:51:21 GMT  
		Size: 114.1 MB (114148980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db366bc2268cda50986b7cae4fa1ddabd7b92d8a85d54daad5f28244f0442207`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 326.7 KB (326714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402345e6fb621ea7619b1d18f51c5deb245660494444030ab446d6990881169b`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf1712afa1cbeccd1a8995ce8a47f9c4754bd0b3c4127270986815107f4f39`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 27.5 MB (27533744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5f636870ad92a36baf93c222c95e78aeb655783c385e4c1b34c8ad6b8ebb1d`  
		Last Modified: Sat, 16 Nov 2024 04:52:06 GMT  
		Size: 323.8 MB (323828821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:7ce003391087f45497ec64c8824303a1dfa47981d09a934ea686a3d29882736f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42249702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9b192222b483b5012d9ae47fb1963fbae4ce09c29fc73a49243b44563488c4`

```dockerfile
```

-	Layers:
	-	`sha256:ae1feacd240265766b6b07159d3e582f409eb2efdc04171057a43794fe612d32`  
		Last Modified: Sat, 16 Nov 2024 04:51:58 GMT  
		Size: 42.2 MB (42239992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e52f2442d84a46fc407a0b2385607e9fc0d72308da77c064c521ae7b133841d`  
		Last Modified: Sat, 16 Nov 2024 04:51:56 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7a94b7db3b1be8fb2e831399e910e51ec8f5deb1d557cd0262c337ceacd3ca89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565670470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7b2cccb7a2ce75d7b110d4f678d3910d712c88d36c07680cdee1c390ccbd84`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81328307e6050d58a3786b0d8d4e0e280336fcbe5e12ed33eafac0e62f39b3c6`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 684.0 KB (683965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dc71d0f9b404e0afdeede800f6310ebab3be587e6a707bfd42f238d09438d`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336756432be3b9f7f44dd7afbc515faeb978872819b168b6908d418b86736edb`  
		Last Modified: Sat, 16 Nov 2024 03:42:13 GMT  
		Size: 117.5 MB (117515664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870e1f30b2d734ef09cf0ddbc60a50570d5c677f7f244597cd0092ccc28a9734`  
		Last Modified: Sat, 16 Nov 2024 03:42:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6924bb4685c143af5e2bec8959405bd94b82464901eb4ebdd3aedde9908dd1aa`  
		Last Modified: Sat, 16 Nov 2024 04:50:07 GMT  
		Size: 111.0 MB (111007847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7125737b4604e0deee24622b4f35e76bb2a81ea469185a71a4f100a1b17a02b`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 326.7 KB (326708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0549a9b72e086e413b36d2ba5a9a97fc7e361f45714c5af076739e3a30b02d`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8e30c16d2403bfc5a15fba00e5199f46f4591a1eee5d2275906979cf66b30`  
		Last Modified: Sat, 16 Nov 2024 04:50:06 GMT  
		Size: 26.7 MB (26685018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c666d99c3684fc94bde4a3ffc855b0531e32378be05043ef1e46456f43005a`  
		Last Modified: Sat, 16 Nov 2024 06:09:27 GMT  
		Size: 277.0 MB (276994555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:b3e2e1bc3e3636e6af3e3de3cf921fd07c65a56b8fc579bc5f24e08a52fd1249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42246919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2e744c8bc88af49433dfb062c323b56878be14b00b81d037a37276ca1cf745`

```dockerfile
```

-	Layers:
	-	`sha256:d7013a2972f834c1d3266202edaf2fda5bbd571e07feddea42a4bd6ff5b28b46`  
		Last Modified: Sat, 16 Nov 2024 06:09:22 GMT  
		Size: 42.2 MB (42237129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adbf7b5374f52bb97eb4921b165bb92c4f0be4615cdeec62c9fdfb1edf699598`  
		Last Modified: Sat, 16 Nov 2024 06:09:20 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:fd4856890f393fb9decea5e8702aafbd5532b5ecf07b2706f6aa01e40fe100ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:315337a06b69f6678c8773374eddf8aa35e1ab56384f4a31bbb0b8c80a94261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622519658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4217e8facf7ecdc1b6d5742e89554806b21854b5d2d29920d2eabcfb38e2f806`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3b2484efd73305009117d35bdc14769dac7cc55a59591b622561a50646fbc`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 683.9 KB (683912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9ee196cfb19dc0d61a08117b1827bc75c1072281719ccd336f9acb1b3c93cd`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 3.6 MB (3560517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d977c02a44f1802debe1eee8710a41198847b4c0d9e6ea5c4a9e893d37a19c8`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2dc8ecf92fab78948452397647f0e17ff6de87b314612dd9030f699ce17b85`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a665f5b789f6618a5b5333bfaeced39dfa1da05d2fc4bcbe994b40c0050630`  
		Last Modified: Sat, 16 Nov 2024 02:57:59 GMT  
		Size: 122.7 MB (122680298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f731aa396c65b6542509fea891d58ddab177bae76da2dbcb1dbeecf8be19de`  
		Last Modified: Sat, 16 Nov 2024 02:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2931749fcbc5a8423464f2953dac75c839bba7110eb40057b47c9609f91bb21`  
		Last Modified: Sat, 16 Nov 2024 03:51:21 GMT  
		Size: 114.1 MB (114148980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db366bc2268cda50986b7cae4fa1ddabd7b92d8a85d54daad5f28244f0442207`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 326.7 KB (326714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402345e6fb621ea7619b1d18f51c5deb245660494444030ab446d6990881169b`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf1712afa1cbeccd1a8995ce8a47f9c4754bd0b3c4127270986815107f4f39`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 27.5 MB (27533744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5f636870ad92a36baf93c222c95e78aeb655783c385e4c1b34c8ad6b8ebb1d`  
		Last Modified: Sat, 16 Nov 2024 04:52:06 GMT  
		Size: 323.8 MB (323828821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7ce003391087f45497ec64c8824303a1dfa47981d09a934ea686a3d29882736f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42249702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9b192222b483b5012d9ae47fb1963fbae4ce09c29fc73a49243b44563488c4`

```dockerfile
```

-	Layers:
	-	`sha256:ae1feacd240265766b6b07159d3e582f409eb2efdc04171057a43794fe612d32`  
		Last Modified: Sat, 16 Nov 2024 04:51:58 GMT  
		Size: 42.2 MB (42239992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e52f2442d84a46fc407a0b2385607e9fc0d72308da77c064c521ae7b133841d`  
		Last Modified: Sat, 16 Nov 2024 04:51:56 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7a94b7db3b1be8fb2e831399e910e51ec8f5deb1d557cd0262c337ceacd3ca89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565670470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7b2cccb7a2ce75d7b110d4f678d3910d712c88d36c07680cdee1c390ccbd84`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81328307e6050d58a3786b0d8d4e0e280336fcbe5e12ed33eafac0e62f39b3c6`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 684.0 KB (683965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dc71d0f9b404e0afdeede800f6310ebab3be587e6a707bfd42f238d09438d`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336756432be3b9f7f44dd7afbc515faeb978872819b168b6908d418b86736edb`  
		Last Modified: Sat, 16 Nov 2024 03:42:13 GMT  
		Size: 117.5 MB (117515664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870e1f30b2d734ef09cf0ddbc60a50570d5c677f7f244597cd0092ccc28a9734`  
		Last Modified: Sat, 16 Nov 2024 03:42:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6924bb4685c143af5e2bec8959405bd94b82464901eb4ebdd3aedde9908dd1aa`  
		Last Modified: Sat, 16 Nov 2024 04:50:07 GMT  
		Size: 111.0 MB (111007847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7125737b4604e0deee24622b4f35e76bb2a81ea469185a71a4f100a1b17a02b`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 326.7 KB (326708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0549a9b72e086e413b36d2ba5a9a97fc7e361f45714c5af076739e3a30b02d`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8e30c16d2403bfc5a15fba00e5199f46f4591a1eee5d2275906979cf66b30`  
		Last Modified: Sat, 16 Nov 2024 04:50:06 GMT  
		Size: 26.7 MB (26685018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c666d99c3684fc94bde4a3ffc855b0531e32378be05043ef1e46456f43005a`  
		Last Modified: Sat, 16 Nov 2024 06:09:27 GMT  
		Size: 277.0 MB (276994555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b3e2e1bc3e3636e6af3e3de3cf921fd07c65a56b8fc579bc5f24e08a52fd1249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42246919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2e744c8bc88af49433dfb062c323b56878be14b00b81d037a37276ca1cf745`

```dockerfile
```

-	Layers:
	-	`sha256:d7013a2972f834c1d3266202edaf2fda5bbd571e07feddea42a4bd6ff5b28b46`  
		Last Modified: Sat, 16 Nov 2024 06:09:22 GMT  
		Size: 42.2 MB (42237129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adbf7b5374f52bb97eb4921b165bb92c4f0be4615cdeec62c9fdfb1edf699598`  
		Last Modified: Sat, 16 Nov 2024 06:09:20 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:42f7b5ac83c674286dcc2e055226b8fb6deff6f2dcc57e82f58dc7b6ac335f96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:9ea1938d30d851fa79df496aeca4d144b2492a1155b7c063e9da80e7f73ebc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298690837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73009468a2afb304f6c7660197b1d222909f4754d698f432e4b91690683df5a5`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3b2484efd73305009117d35bdc14769dac7cc55a59591b622561a50646fbc`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 683.9 KB (683912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9ee196cfb19dc0d61a08117b1827bc75c1072281719ccd336f9acb1b3c93cd`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 3.6 MB (3560517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d977c02a44f1802debe1eee8710a41198847b4c0d9e6ea5c4a9e893d37a19c8`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2dc8ecf92fab78948452397647f0e17ff6de87b314612dd9030f699ce17b85`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a665f5b789f6618a5b5333bfaeced39dfa1da05d2fc4bcbe994b40c0050630`  
		Last Modified: Sat, 16 Nov 2024 02:57:59 GMT  
		Size: 122.7 MB (122680298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f731aa396c65b6542509fea891d58ddab177bae76da2dbcb1dbeecf8be19de`  
		Last Modified: Sat, 16 Nov 2024 02:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2931749fcbc5a8423464f2953dac75c839bba7110eb40057b47c9609f91bb21`  
		Last Modified: Sat, 16 Nov 2024 03:51:21 GMT  
		Size: 114.1 MB (114148980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db366bc2268cda50986b7cae4fa1ddabd7b92d8a85d54daad5f28244f0442207`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 326.7 KB (326714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402345e6fb621ea7619b1d18f51c5deb245660494444030ab446d6990881169b`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf1712afa1cbeccd1a8995ce8a47f9c4754bd0b3c4127270986815107f4f39`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 27.5 MB (27533744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:8605e5d64f9bf695bd474e9eaa1984c153a4a977d27d4472c5467be934d6a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23938670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306f92f38f4937f45e8ebaf2fade1ee690fa3b0c3332f161cb7301e12b15448b`

```dockerfile
```

-	Layers:
	-	`sha256:00a0a36b7f27c40b04d0159f5793a5e9b6bb1a08fd3559c4947bae0096b5555d`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 23.9 MB (23921497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaaa58a5ef3f1a86a2da48bd9e723d2576dc7e62838c6bfc6942c577ffdbbfb`  
		Last Modified: Sat, 16 Nov 2024 03:51:14 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3816010eca888366190324e68b6f07908e34a99af9de61e47d8e2447a9306643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288675915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f59d954e709ebeb4b464484a200658dce24ed33b71a0505ffd44a9622f54a`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81328307e6050d58a3786b0d8d4e0e280336fcbe5e12ed33eafac0e62f39b3c6`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 684.0 KB (683965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dc71d0f9b404e0afdeede800f6310ebab3be587e6a707bfd42f238d09438d`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336756432be3b9f7f44dd7afbc515faeb978872819b168b6908d418b86736edb`  
		Last Modified: Sat, 16 Nov 2024 03:42:13 GMT  
		Size: 117.5 MB (117515664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870e1f30b2d734ef09cf0ddbc60a50570d5c677f7f244597cd0092ccc28a9734`  
		Last Modified: Sat, 16 Nov 2024 03:42:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6924bb4685c143af5e2bec8959405bd94b82464901eb4ebdd3aedde9908dd1aa`  
		Last Modified: Sat, 16 Nov 2024 04:50:07 GMT  
		Size: 111.0 MB (111007847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7125737b4604e0deee24622b4f35e76bb2a81ea469185a71a4f100a1b17a02b`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 326.7 KB (326708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0549a9b72e086e413b36d2ba5a9a97fc7e361f45714c5af076739e3a30b02d`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8e30c16d2403bfc5a15fba00e5199f46f4591a1eee5d2275906979cf66b30`  
		Last Modified: Sat, 16 Nov 2024 04:50:06 GMT  
		Size: 26.7 MB (26685018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:168cc9da852dfd921589fd0ef6c9923580989080fdb3a1cbe3c38a8e0e2632af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23961372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc732bd5a1356f65079513c8c21328422fc745eb346c6df8edc093784223f083`

```dockerfile
```

-	Layers:
	-	`sha256:2bde361a6a2dac60ee9f7699306abdf35f518b420977d20f3dea5be3d351daae`  
		Last Modified: Sat, 16 Nov 2024 04:50:05 GMT  
		Size: 23.9 MB (23944062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450cfc3d353da63b52ae578cbdf62d291199fe48b1d634f73e1bb91c24ada593`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:42f7b5ac83c674286dcc2e055226b8fb6deff6f2dcc57e82f58dc7b6ac335f96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:9ea1938d30d851fa79df496aeca4d144b2492a1155b7c063e9da80e7f73ebc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298690837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73009468a2afb304f6c7660197b1d222909f4754d698f432e4b91690683df5a5`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3b2484efd73305009117d35bdc14769dac7cc55a59591b622561a50646fbc`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 683.9 KB (683912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9ee196cfb19dc0d61a08117b1827bc75c1072281719ccd336f9acb1b3c93cd`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 3.6 MB (3560517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d977c02a44f1802debe1eee8710a41198847b4c0d9e6ea5c4a9e893d37a19c8`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2dc8ecf92fab78948452397647f0e17ff6de87b314612dd9030f699ce17b85`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a665f5b789f6618a5b5333bfaeced39dfa1da05d2fc4bcbe994b40c0050630`  
		Last Modified: Sat, 16 Nov 2024 02:57:59 GMT  
		Size: 122.7 MB (122680298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f731aa396c65b6542509fea891d58ddab177bae76da2dbcb1dbeecf8be19de`  
		Last Modified: Sat, 16 Nov 2024 02:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2931749fcbc5a8423464f2953dac75c839bba7110eb40057b47c9609f91bb21`  
		Last Modified: Sat, 16 Nov 2024 03:51:21 GMT  
		Size: 114.1 MB (114148980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db366bc2268cda50986b7cae4fa1ddabd7b92d8a85d54daad5f28244f0442207`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 326.7 KB (326714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402345e6fb621ea7619b1d18f51c5deb245660494444030ab446d6990881169b`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf1712afa1cbeccd1a8995ce8a47f9c4754bd0b3c4127270986815107f4f39`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 27.5 MB (27533744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8605e5d64f9bf695bd474e9eaa1984c153a4a977d27d4472c5467be934d6a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23938670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306f92f38f4937f45e8ebaf2fade1ee690fa3b0c3332f161cb7301e12b15448b`

```dockerfile
```

-	Layers:
	-	`sha256:00a0a36b7f27c40b04d0159f5793a5e9b6bb1a08fd3559c4947bae0096b5555d`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 23.9 MB (23921497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaaa58a5ef3f1a86a2da48bd9e723d2576dc7e62838c6bfc6942c577ffdbbfb`  
		Last Modified: Sat, 16 Nov 2024 03:51:14 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3816010eca888366190324e68b6f07908e34a99af9de61e47d8e2447a9306643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288675915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f59d954e709ebeb4b464484a200658dce24ed33b71a0505ffd44a9622f54a`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81328307e6050d58a3786b0d8d4e0e280336fcbe5e12ed33eafac0e62f39b3c6`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 684.0 KB (683965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dc71d0f9b404e0afdeede800f6310ebab3be587e6a707bfd42f238d09438d`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336756432be3b9f7f44dd7afbc515faeb978872819b168b6908d418b86736edb`  
		Last Modified: Sat, 16 Nov 2024 03:42:13 GMT  
		Size: 117.5 MB (117515664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870e1f30b2d734ef09cf0ddbc60a50570d5c677f7f244597cd0092ccc28a9734`  
		Last Modified: Sat, 16 Nov 2024 03:42:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6924bb4685c143af5e2bec8959405bd94b82464901eb4ebdd3aedde9908dd1aa`  
		Last Modified: Sat, 16 Nov 2024 04:50:07 GMT  
		Size: 111.0 MB (111007847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7125737b4604e0deee24622b4f35e76bb2a81ea469185a71a4f100a1b17a02b`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 326.7 KB (326708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0549a9b72e086e413b36d2ba5a9a97fc7e361f45714c5af076739e3a30b02d`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8e30c16d2403bfc5a15fba00e5199f46f4591a1eee5d2275906979cf66b30`  
		Last Modified: Sat, 16 Nov 2024 04:50:06 GMT  
		Size: 26.7 MB (26685018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:168cc9da852dfd921589fd0ef6c9923580989080fdb3a1cbe3c38a8e0e2632af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23961372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc732bd5a1356f65079513c8c21328422fc745eb346c6df8edc093784223f083`

```dockerfile
```

-	Layers:
	-	`sha256:2bde361a6a2dac60ee9f7699306abdf35f518b420977d20f3dea5be3d351daae`  
		Last Modified: Sat, 16 Nov 2024 04:50:05 GMT  
		Size: 23.9 MB (23944062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450cfc3d353da63b52ae578cbdf62d291199fe48b1d634f73e1bb91c24ada593`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:11dfbf875a5453b1b0ceb4a47f4bdf6590fb86dfd39d8612298a2433a7ee96b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:8c9fc809eb8ea2e76edf1d0407406ace8e9bf582441be2ce9939955e8ccb8043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166192203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7dad43d602d258cb7f34fa2e3625955887ce0f215e8e46e604a68ad7ff94420`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e8d3973a6431bf06ae2429fe6043d68076f680d6b9e838871fea0dda80d8a`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 680.3 KB (680326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623b736b410baa5a5818f62b08b2007dd9842030d9973045f5f90da7ee66c55`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 3.6 MB (3561526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2b2c3a23f9902ed270bb51f69b99a73d85d366f06f5a32a28256af861b69d0`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4fa6db600a3081b7a0db34679e3c98dc51777a5ba600aafc114cd49bf17f75`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad0c45362760291479652f2f15e1f417e3217c27d636ba16b628a3a019d7da`  
		Last Modified: Mon, 10 Mar 2025 18:13:42 GMT  
		Size: 132.2 MB (132193590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d9ebb38bcee87c07ca2ae9f32b3c83fd24b46271f5b8317239ea3c4ec23240`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fbeca46ddd84e1e032f5ad08f1a8ac7fd40556c174ec2bea08b9aa85d902029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17766893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b1571f6ecdcb15e61749149f52d36906b1f775e11fbf70ad4a792095b5b67d`

```dockerfile
```

-	Layers:
	-	`sha256:84cb15a154b9ca3645346d64f0482ffe7e6d19610e3c2b64bbe801f500798c2d`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 17.8 MB (17750499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e515b1f18393d7bf6ee59b413d093d53d8e53140b412a75e05ac70e62640c670`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7135212fa26f4a3989e9c6c319a1872f7ffcbc55b11bd20ad05fd2c760f83042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158875086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0c3cf3e24f9fa881fcc8872cf03718b1113178b0fdd3d6bb7ff43aad4aadc3`
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

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fc748dd0d6ae598edab8e919aa10aa3ec4bbf2587bcdb919e0ba7d39c5287a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17859205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de9d744b3a964279a90b58f36cbbd6ea93468bb529a489a81f9daa5ed6c18c1`

```dockerfile
```

-	Layers:
	-	`sha256:a6a02918c557b3bcbaa3b92f58a5e06173abac6dbb3bff3d16068dd796ebb4c9`  
		Last Modified: Mon, 10 Mar 2025 18:18:58 GMT  
		Size: 17.8 MB (17842671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da693c7ee458d527d35d61d7438df7c719cbce7253c117c2f8c41a51a2fa6604`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 16.5 KB (16534 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:11dfbf875a5453b1b0ceb4a47f4bdf6590fb86dfd39d8612298a2433a7ee96b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:8c9fc809eb8ea2e76edf1d0407406ace8e9bf582441be2ce9939955e8ccb8043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166192203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7dad43d602d258cb7f34fa2e3625955887ce0f215e8e46e604a68ad7ff94420`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e8d3973a6431bf06ae2429fe6043d68076f680d6b9e838871fea0dda80d8a`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 680.3 KB (680326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623b736b410baa5a5818f62b08b2007dd9842030d9973045f5f90da7ee66c55`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 3.6 MB (3561526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2b2c3a23f9902ed270bb51f69b99a73d85d366f06f5a32a28256af861b69d0`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4fa6db600a3081b7a0db34679e3c98dc51777a5ba600aafc114cd49bf17f75`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad0c45362760291479652f2f15e1f417e3217c27d636ba16b628a3a019d7da`  
		Last Modified: Mon, 10 Mar 2025 18:13:42 GMT  
		Size: 132.2 MB (132193590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d9ebb38bcee87c07ca2ae9f32b3c83fd24b46271f5b8317239ea3c4ec23240`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fbeca46ddd84e1e032f5ad08f1a8ac7fd40556c174ec2bea08b9aa85d902029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17766893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b1571f6ecdcb15e61749149f52d36906b1f775e11fbf70ad4a792095b5b67d`

```dockerfile
```

-	Layers:
	-	`sha256:84cb15a154b9ca3645346d64f0482ffe7e6d19610e3c2b64bbe801f500798c2d`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 17.8 MB (17750499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e515b1f18393d7bf6ee59b413d093d53d8e53140b412a75e05ac70e62640c670`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7135212fa26f4a3989e9c6c319a1872f7ffcbc55b11bd20ad05fd2c760f83042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158875086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0c3cf3e24f9fa881fcc8872cf03718b1113178b0fdd3d6bb7ff43aad4aadc3`
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

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fc748dd0d6ae598edab8e919aa10aa3ec4bbf2587bcdb919e0ba7d39c5287a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17859205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de9d744b3a964279a90b58f36cbbd6ea93468bb529a489a81f9daa5ed6c18c1`

```dockerfile
```

-	Layers:
	-	`sha256:a6a02918c557b3bcbaa3b92f58a5e06173abac6dbb3bff3d16068dd796ebb4c9`  
		Last Modified: Mon, 10 Mar 2025 18:18:58 GMT  
		Size: 17.8 MB (17842671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da693c7ee458d527d35d61d7438df7c719cbce7253c117c2f8c41a51a2fa6604`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 16.5 KB (16534 bytes)  
		MIME: application/vnd.in-toto+json
