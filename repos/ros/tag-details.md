<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
-	[`ros:kilted`](#roskilted)
-	[`ros:kilted-perception`](#roskilted-perception)
-	[`ros:kilted-perception-noble`](#roskilted-perception-noble)
-	[`ros:kilted-ros-base`](#roskilted-ros-base)
-	[`ros:kilted-ros-base-noble`](#roskilted-ros-base-noble)
-	[`ros:kilted-ros-core`](#roskilted-ros-core)
-	[`ros:kilted-ros-core-noble`](#roskilted-ros-core-noble)
-	[`ros:latest`](#roslatest)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:2fe6fec19fbac9c94794c7fa4afc83099f5372659dd1871f01b6d54f6701ddc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:4fa26d473f0c4e50bd5d4fa8d385b26630676920c924a417a18b7a41e04eab3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263208026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740779815936a7561668680ba884b066f0bf3319bf1ee9ab5bf896d531fb8ab2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:50 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:56:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:56:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:56:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:56:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f147c465ef3441f6a6fadaa4bf3dd1b68d753988b404893e8e575a24a013be1`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 1.2 MB (1214139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b6a798b5088fee7bc0bfb188bdd445113b407842d17edf502e09f2fc1b536`  
		Last Modified: Thu, 15 Jan 2026 22:41:25 GMT  
		Size: 6.0 MB (5992568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd839ce83db999d5035a7a3825b0dfa72a58cb764b8a8ea0c500fbed89b583b`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 97.2 KB (97222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e1824e50f15537f4e31add7722621bc890f927e27f1505e54da0b51bc4c1b`  
		Last Modified: Thu, 15 Jan 2026 22:41:37 GMT  
		Size: 104.7 MB (104703723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dabda1f44ba2f0c461142f451ba75451f7348aa265fbe6a04dd0ff2654448d`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aaf05f7e4717206bdef277969fefae295f0aeb84ad86377ce147c6e467ce29`  
		Last Modified: Fri, 16 Jan 2026 00:57:48 GMT  
		Size: 98.0 MB (97958403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e9ae4043d817eb2f5f8b33584b61dd9859d8733be7d8c069ae9efe648e3d28`  
		Last Modified: Fri, 16 Jan 2026 00:57:39 GMT  
		Size: 383.1 KB (383080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c9c540e89d0a29bced540968ac923c8677aab6a43d85b536f173a4e668d7a7`  
		Last Modified: Fri, 16 Jan 2026 00:57:39 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89d0b0792ec60ed6744e3a288f76caa6009884e44c6cd98add8055465bd325c`  
		Last Modified: Fri, 16 Jan 2026 00:57:41 GMT  
		Size: 23.3 MB (23319499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:aa933c8e518a0957b5d75eabf9a9d944ffef65154129fdc80bf16c8ef69e0b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23718026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702e1eb956143c1266f08db67e1428a7aa854ef2c008cea0d0fd078f8254d261`

```dockerfile
```

-	Layers:
	-	`sha256:6d9864a6e563ad5d671df9ee0da42cee27b5fb301939a5c33536b20dd8774fdf`  
		Last Modified: Fri, 16 Jan 2026 02:18:18 GMT  
		Size: 23.7 MB (23701678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbdadcda1ef6b67b0128dac459f2d914df58cd209ba96d2d65c29e2d938d352`  
		Last Modified: Fri, 16 Jan 2026 02:18:19 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:38771a82f3f7af8e867334a6110f283255167d887893d87617a46f3c5555460d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255774896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583c68d3026497bd28cef7239430c93c8be2e49248ff1947a1cce9133a90399d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:42:04 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:59:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:59:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:59:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4eaed05c1178f3c3abdac8710778abf118d80e3bc2740ff1270b8e4316b14`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 1.2 MB (1214255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8fdf13cb39747e8c67471f5fd7e7eb6060b2cf311a7e56c64f6ea8a77a5b63`  
		Last Modified: Thu, 15 Jan 2026 22:42:39 GMT  
		Size: 5.9 MB (5943245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e54e499a91704d69c814930daaf58f6daab8d4e90cb5515d9292d6adf0420`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 97.3 KB (97262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01a8729ed4ffcbfea0a8f2b6e3d75fb2b3d6fbca0adae54bdcca438384f878`  
		Last Modified: Thu, 15 Jan 2026 22:42:54 GMT  
		Size: 102.5 MB (102461954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb96ce313cf0c46ab959a2078235f16180a94cb84463bf95ee21b57ddee0bd9`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a9f60ba1df891822ce0d8130763f31a13c443b9ebfe1c0e440fcd3e6c191f`  
		Last Modified: Fri, 16 Jan 2026 01:01:07 GMT  
		Size: 95.6 MB (95570423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1972aab6a9eb97320567f599408f1b3c042d45b4d5cf98a47df3fae37d322ba5`  
		Last Modified: Fri, 16 Jan 2026 01:00:53 GMT  
		Size: 383.1 KB (383089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d7bad824db54a24fe8e28696df6152c09a70dad3ed062036f227f5166cdcf`  
		Last Modified: Fri, 16 Jan 2026 01:00:53 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7449e37e4f9d95d850d1345d99e92afc5b1075877cd1809b099c884e46a26eb8`  
		Last Modified: Fri, 16 Jan 2026 01:00:45 GMT  
		Size: 22.7 MB (22718477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:4f1b53d074e8106bee8df3dd1348aecc01acdb88b5713f6d58d5cbb95f00ca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23731180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f217e4a500bf2a6b963a0ef6ba1d3139d3f88e6367917ec0f6a5a0ce3105b6dd`

```dockerfile
```

-	Layers:
	-	`sha256:aab5123d0d538aa35b3293ef2f7a8d14547dcf5126765bc3aad2990382a98430`  
		Last Modified: Fri, 16 Jan 2026 02:18:46 GMT  
		Size: 23.7 MB (23714695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac45bcf889e7b5f4a0a3b5e12fad178e59d3d9f30e3707f54af751ca9c87d822`  
		Last Modified: Fri, 16 Jan 2026 02:18:47 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:f14906d4a3ca82fa13ec7f8c79d237a04f6a14d47b69564f25eac6903d319d91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:4e413449e965df0365d69f8c3d1ba8cfcce7462055b2e9f553946038c8fb889f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.3 MB (955267423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59770bcd3cb81de41bcfcb45df3b1cd13f144652a4103b9c8a561013c176d044`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Tue, 13 Jan 2026 00:59:37 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Tue, 13 Jan 2026 00:59:38 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Tue, 13 Jan 2026 00:59:38 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Tue, 13 Jan 2026 00:59:46 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Tue, 13 Jan 2026 00:56:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Tue, 13 Jan 2026 00:59:46 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Tue, 13 Jan 2026 00:59:39 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Tue, 13 Jan 2026 00:59:40 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Tue, 13 Jan 2026 00:59:45 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0d0741124ce4b0fb32492f0eb411c68db26f35feb0021f90eb30e7d54f867`  
		Last Modified: Tue, 13 Jan 2026 07:24:30 GMT  
		Size: 692.1 MB (692078563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:beb8f658a1af83eb45d4c219d7a6dddd8461f1e6b5ea407917e43aa8cd78d417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58779844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b398c9069f37afa0b64dea4ee59863980189e9bd72350262c9e4f2856040857`

```dockerfile
```

-	Layers:
	-	`sha256:3c05b9e971b9f7a4606bc635dfdf55c3ac7a74cf9a4f7f7b93590ddc2e8daf03`  
		Last Modified: Wed, 14 Jan 2026 02:57:21 GMT  
		Size: 58.8 MB (58770492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a507faa299531991695a31b8854ae95bdd28604e7ac848e2dde9065c3bedf8f9`  
		Last Modified: Wed, 14 Jan 2026 02:57:11 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ec183011cf6e60839ceb21854426cef343bcef506019abed261c30357f959409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.8 MB (915797607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9d2f3550dab7e144828cc7546b305d487aa457c6f459bffdc4c1036ff187f2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Tue, 13 Jan 2026 01:05:47 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Tue, 13 Jan 2026 01:05:45 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Tue, 13 Jan 2026 01:05:43 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Tue, 13 Jan 2026 01:05:57 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Tue, 13 Jan 2026 01:05:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Tue, 13 Jan 2026 01:05:20 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Tue, 13 Jan 2026 01:05:13 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Tue, 13 Jan 2026 01:05:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Tue, 13 Jan 2026 01:05:15 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11e17f04355c02a9eadea3e0924ee22951e0a76af18b90e7a44e2cfada4c52`  
		Last Modified: Tue, 13 Jan 2026 09:40:38 GMT  
		Size: 660.1 MB (660050278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:20b8cc1b1082051f1c1937e4002197a0acdd8ee796f9d9b17dd686ade332e9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58764245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215b91a017e92d95162e756c7abc222791ac87f692ccc607510a10866c6f48b`

```dockerfile
```

-	Layers:
	-	`sha256:6e41f5d137270010cee9c967c7b1f18ec19e7de3cbe729d862fed5b6a2859920`  
		Last Modified: Wed, 14 Jan 2026 04:05:52 GMT  
		Size: 58.8 MB (58754813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0b1e8fd8dd6d89eda990d19a48a4735fd6141dee4434e2b642439d6a90f13e`  
		Last Modified: Tue, 13 Jan 2026 14:24:44 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:f14906d4a3ca82fa13ec7f8c79d237a04f6a14d47b69564f25eac6903d319d91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:4e413449e965df0365d69f8c3d1ba8cfcce7462055b2e9f553946038c8fb889f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.3 MB (955267423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59770bcd3cb81de41bcfcb45df3b1cd13f144652a4103b9c8a561013c176d044`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:17:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Tue, 13 Jan 2026 00:59:37 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Tue, 13 Jan 2026 00:59:38 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Tue, 13 Jan 2026 00:59:38 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Tue, 13 Jan 2026 00:59:46 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Tue, 13 Jan 2026 00:56:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Tue, 13 Jan 2026 00:59:46 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Tue, 13 Jan 2026 00:59:39 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Tue, 13 Jan 2026 00:59:40 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Tue, 13 Jan 2026 00:59:45 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0d0741124ce4b0fb32492f0eb411c68db26f35feb0021f90eb30e7d54f867`  
		Last Modified: Tue, 13 Jan 2026 07:24:30 GMT  
		Size: 692.1 MB (692078563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:beb8f658a1af83eb45d4c219d7a6dddd8461f1e6b5ea407917e43aa8cd78d417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58779844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b398c9069f37afa0b64dea4ee59863980189e9bd72350262c9e4f2856040857`

```dockerfile
```

-	Layers:
	-	`sha256:3c05b9e971b9f7a4606bc635dfdf55c3ac7a74cf9a4f7f7b93590ddc2e8daf03`  
		Last Modified: Wed, 14 Jan 2026 02:57:21 GMT  
		Size: 58.8 MB (58770492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a507faa299531991695a31b8854ae95bdd28604e7ac848e2dde9065c3bedf8f9`  
		Last Modified: Wed, 14 Jan 2026 02:57:11 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ec183011cf6e60839ceb21854426cef343bcef506019abed261c30357f959409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.8 MB (915797607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9d2f3550dab7e144828cc7546b305d487aa457c6f459bffdc4c1036ff187f2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:33:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Tue, 13 Jan 2026 01:05:47 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Tue, 13 Jan 2026 01:05:45 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Tue, 13 Jan 2026 01:05:43 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Tue, 13 Jan 2026 01:05:57 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Tue, 13 Jan 2026 01:05:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Tue, 13 Jan 2026 01:05:20 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Tue, 13 Jan 2026 01:05:13 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Tue, 13 Jan 2026 01:05:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Tue, 13 Jan 2026 01:05:15 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11e17f04355c02a9eadea3e0924ee22951e0a76af18b90e7a44e2cfada4c52`  
		Last Modified: Tue, 13 Jan 2026 09:40:38 GMT  
		Size: 660.1 MB (660050278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:20b8cc1b1082051f1c1937e4002197a0acdd8ee796f9d9b17dd686ade332e9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58764245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0215b91a017e92d95162e756c7abc222791ac87f692ccc607510a10866c6f48b`

```dockerfile
```

-	Layers:
	-	`sha256:6e41f5d137270010cee9c967c7b1f18ec19e7de3cbe729d862fed5b6a2859920`  
		Last Modified: Wed, 14 Jan 2026 04:05:52 GMT  
		Size: 58.8 MB (58754813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0b1e8fd8dd6d89eda990d19a48a4735fd6141dee4434e2b642439d6a90f13e`  
		Last Modified: Tue, 13 Jan 2026 14:24:44 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:2fe6fec19fbac9c94794c7fa4afc83099f5372659dd1871f01b6d54f6701ddc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:4fa26d473f0c4e50bd5d4fa8d385b26630676920c924a417a18b7a41e04eab3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263208026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740779815936a7561668680ba884b066f0bf3319bf1ee9ab5bf896d531fb8ab2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:50 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:56:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:56:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:56:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:56:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f147c465ef3441f6a6fadaa4bf3dd1b68d753988b404893e8e575a24a013be1`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 1.2 MB (1214139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b6a798b5088fee7bc0bfb188bdd445113b407842d17edf502e09f2fc1b536`  
		Last Modified: Thu, 15 Jan 2026 22:41:25 GMT  
		Size: 6.0 MB (5992568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd839ce83db999d5035a7a3825b0dfa72a58cb764b8a8ea0c500fbed89b583b`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 97.2 KB (97222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e1824e50f15537f4e31add7722621bc890f927e27f1505e54da0b51bc4c1b`  
		Last Modified: Thu, 15 Jan 2026 22:41:37 GMT  
		Size: 104.7 MB (104703723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dabda1f44ba2f0c461142f451ba75451f7348aa265fbe6a04dd0ff2654448d`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aaf05f7e4717206bdef277969fefae295f0aeb84ad86377ce147c6e467ce29`  
		Last Modified: Fri, 16 Jan 2026 00:57:48 GMT  
		Size: 98.0 MB (97958403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e9ae4043d817eb2f5f8b33584b61dd9859d8733be7d8c069ae9efe648e3d28`  
		Last Modified: Fri, 16 Jan 2026 00:57:39 GMT  
		Size: 383.1 KB (383080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c9c540e89d0a29bced540968ac923c8677aab6a43d85b536f173a4e668d7a7`  
		Last Modified: Fri, 16 Jan 2026 00:57:39 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89d0b0792ec60ed6744e3a288f76caa6009884e44c6cd98add8055465bd325c`  
		Last Modified: Fri, 16 Jan 2026 00:57:41 GMT  
		Size: 23.3 MB (23319499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:aa933c8e518a0957b5d75eabf9a9d944ffef65154129fdc80bf16c8ef69e0b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23718026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702e1eb956143c1266f08db67e1428a7aa854ef2c008cea0d0fd078f8254d261`

```dockerfile
```

-	Layers:
	-	`sha256:6d9864a6e563ad5d671df9ee0da42cee27b5fb301939a5c33536b20dd8774fdf`  
		Last Modified: Fri, 16 Jan 2026 02:18:18 GMT  
		Size: 23.7 MB (23701678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbdadcda1ef6b67b0128dac459f2d914df58cd209ba96d2d65c29e2d938d352`  
		Last Modified: Fri, 16 Jan 2026 02:18:19 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:38771a82f3f7af8e867334a6110f283255167d887893d87617a46f3c5555460d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255774896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583c68d3026497bd28cef7239430c93c8be2e49248ff1947a1cce9133a90399d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:42:04 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:59:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:59:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:59:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4eaed05c1178f3c3abdac8710778abf118d80e3bc2740ff1270b8e4316b14`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 1.2 MB (1214255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8fdf13cb39747e8c67471f5fd7e7eb6060b2cf311a7e56c64f6ea8a77a5b63`  
		Last Modified: Thu, 15 Jan 2026 22:42:39 GMT  
		Size: 5.9 MB (5943245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e54e499a91704d69c814930daaf58f6daab8d4e90cb5515d9292d6adf0420`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 97.3 KB (97262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01a8729ed4ffcbfea0a8f2b6e3d75fb2b3d6fbca0adae54bdcca438384f878`  
		Last Modified: Thu, 15 Jan 2026 22:42:54 GMT  
		Size: 102.5 MB (102461954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb96ce313cf0c46ab959a2078235f16180a94cb84463bf95ee21b57ddee0bd9`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a9f60ba1df891822ce0d8130763f31a13c443b9ebfe1c0e440fcd3e6c191f`  
		Last Modified: Fri, 16 Jan 2026 01:01:07 GMT  
		Size: 95.6 MB (95570423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1972aab6a9eb97320567f599408f1b3c042d45b4d5cf98a47df3fae37d322ba5`  
		Last Modified: Fri, 16 Jan 2026 01:00:53 GMT  
		Size: 383.1 KB (383089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d7bad824db54a24fe8e28696df6152c09a70dad3ed062036f227f5166cdcf`  
		Last Modified: Fri, 16 Jan 2026 01:00:53 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7449e37e4f9d95d850d1345d99e92afc5b1075877cd1809b099c884e46a26eb8`  
		Last Modified: Fri, 16 Jan 2026 01:00:45 GMT  
		Size: 22.7 MB (22718477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:4f1b53d074e8106bee8df3dd1348aecc01acdb88b5713f6d58d5cbb95f00ca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23731180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f217e4a500bf2a6b963a0ef6ba1d3139d3f88e6367917ec0f6a5a0ce3105b6dd`

```dockerfile
```

-	Layers:
	-	`sha256:aab5123d0d538aa35b3293ef2f7a8d14547dcf5126765bc3aad2990382a98430`  
		Last Modified: Fri, 16 Jan 2026 02:18:46 GMT  
		Size: 23.7 MB (23714695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac45bcf889e7b5f4a0a3b5e12fad178e59d3d9f30e3707f54af751ca9c87d822`  
		Last Modified: Fri, 16 Jan 2026 02:18:47 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:2fe6fec19fbac9c94794c7fa4afc83099f5372659dd1871f01b6d54f6701ddc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:4fa26d473f0c4e50bd5d4fa8d385b26630676920c924a417a18b7a41e04eab3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263208026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740779815936a7561668680ba884b066f0bf3319bf1ee9ab5bf896d531fb8ab2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:50 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:56:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:56:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:56:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:56:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f147c465ef3441f6a6fadaa4bf3dd1b68d753988b404893e8e575a24a013be1`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 1.2 MB (1214139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b6a798b5088fee7bc0bfb188bdd445113b407842d17edf502e09f2fc1b536`  
		Last Modified: Thu, 15 Jan 2026 22:41:25 GMT  
		Size: 6.0 MB (5992568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd839ce83db999d5035a7a3825b0dfa72a58cb764b8a8ea0c500fbed89b583b`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 97.2 KB (97222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e1824e50f15537f4e31add7722621bc890f927e27f1505e54da0b51bc4c1b`  
		Last Modified: Thu, 15 Jan 2026 22:41:37 GMT  
		Size: 104.7 MB (104703723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dabda1f44ba2f0c461142f451ba75451f7348aa265fbe6a04dd0ff2654448d`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aaf05f7e4717206bdef277969fefae295f0aeb84ad86377ce147c6e467ce29`  
		Last Modified: Fri, 16 Jan 2026 00:57:48 GMT  
		Size: 98.0 MB (97958403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e9ae4043d817eb2f5f8b33584b61dd9859d8733be7d8c069ae9efe648e3d28`  
		Last Modified: Fri, 16 Jan 2026 00:57:39 GMT  
		Size: 383.1 KB (383080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c9c540e89d0a29bced540968ac923c8677aab6a43d85b536f173a4e668d7a7`  
		Last Modified: Fri, 16 Jan 2026 00:57:39 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89d0b0792ec60ed6744e3a288f76caa6009884e44c6cd98add8055465bd325c`  
		Last Modified: Fri, 16 Jan 2026 00:57:41 GMT  
		Size: 23.3 MB (23319499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:aa933c8e518a0957b5d75eabf9a9d944ffef65154129fdc80bf16c8ef69e0b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23718026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702e1eb956143c1266f08db67e1428a7aa854ef2c008cea0d0fd078f8254d261`

```dockerfile
```

-	Layers:
	-	`sha256:6d9864a6e563ad5d671df9ee0da42cee27b5fb301939a5c33536b20dd8774fdf`  
		Last Modified: Fri, 16 Jan 2026 02:18:18 GMT  
		Size: 23.7 MB (23701678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbdadcda1ef6b67b0128dac459f2d914df58cd209ba96d2d65c29e2d938d352`  
		Last Modified: Fri, 16 Jan 2026 02:18:19 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:38771a82f3f7af8e867334a6110f283255167d887893d87617a46f3c5555460d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255774896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583c68d3026497bd28cef7239430c93c8be2e49248ff1947a1cce9133a90399d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:42:04 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:59:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:59:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:59:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4eaed05c1178f3c3abdac8710778abf118d80e3bc2740ff1270b8e4316b14`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 1.2 MB (1214255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8fdf13cb39747e8c67471f5fd7e7eb6060b2cf311a7e56c64f6ea8a77a5b63`  
		Last Modified: Thu, 15 Jan 2026 22:42:39 GMT  
		Size: 5.9 MB (5943245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e54e499a91704d69c814930daaf58f6daab8d4e90cb5515d9292d6adf0420`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 97.3 KB (97262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01a8729ed4ffcbfea0a8f2b6e3d75fb2b3d6fbca0adae54bdcca438384f878`  
		Last Modified: Thu, 15 Jan 2026 22:42:54 GMT  
		Size: 102.5 MB (102461954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb96ce313cf0c46ab959a2078235f16180a94cb84463bf95ee21b57ddee0bd9`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a9f60ba1df891822ce0d8130763f31a13c443b9ebfe1c0e440fcd3e6c191f`  
		Last Modified: Fri, 16 Jan 2026 01:01:07 GMT  
		Size: 95.6 MB (95570423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1972aab6a9eb97320567f599408f1b3c042d45b4d5cf98a47df3fae37d322ba5`  
		Last Modified: Fri, 16 Jan 2026 01:00:53 GMT  
		Size: 383.1 KB (383089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d7bad824db54a24fe8e28696df6152c09a70dad3ed062036f227f5166cdcf`  
		Last Modified: Fri, 16 Jan 2026 01:00:53 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7449e37e4f9d95d850d1345d99e92afc5b1075877cd1809b099c884e46a26eb8`  
		Last Modified: Fri, 16 Jan 2026 01:00:45 GMT  
		Size: 22.7 MB (22718477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4f1b53d074e8106bee8df3dd1348aecc01acdb88b5713f6d58d5cbb95f00ca5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23731180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f217e4a500bf2a6b963a0ef6ba1d3139d3f88e6367917ec0f6a5a0ce3105b6dd`

```dockerfile
```

-	Layers:
	-	`sha256:aab5123d0d538aa35b3293ef2f7a8d14547dcf5126765bc3aad2990382a98430`  
		Last Modified: Fri, 16 Jan 2026 02:18:46 GMT  
		Size: 23.7 MB (23714695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac45bcf889e7b5f4a0a3b5e12fad178e59d3d9f30e3707f54af751ca9c87d822`  
		Last Modified: Fri, 16 Jan 2026 02:18:47 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:cd9f3331edf8c29d61e091e76654eb1161c7971ff443b1a00e3244bd62e37051
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f69b5539fceb0e0129a08a4e5cffc7582b77c0205929d55a6cb3346ebecee432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141544514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672cbb3e4dc690aa49ad38bbfad559d3e83e013d9789a378e65126aad5c0f71b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f147c465ef3441f6a6fadaa4bf3dd1b68d753988b404893e8e575a24a013be1`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 1.2 MB (1214139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b6a798b5088fee7bc0bfb188bdd445113b407842d17edf502e09f2fc1b536`  
		Last Modified: Thu, 15 Jan 2026 22:41:25 GMT  
		Size: 6.0 MB (5992568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd839ce83db999d5035a7a3825b0dfa72a58cb764b8a8ea0c500fbed89b583b`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 97.2 KB (97222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e1824e50f15537f4e31add7722621bc890f927e27f1505e54da0b51bc4c1b`  
		Last Modified: Thu, 15 Jan 2026 22:41:37 GMT  
		Size: 104.7 MB (104703723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dabda1f44ba2f0c461142f451ba75451f7348aa265fbe6a04dd0ff2654448d`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:4fc3d5fcfbb3581dce7815009c262c42533eb9c376a299da43240c7034cc07b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17696040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ae6d258fc9e421f1f32bde317f386912b70388378ed0f2996dce493e33e66d`

```dockerfile
```

-	Layers:
	-	`sha256:28c9ab24b1fe7b7ba054f5b971dcdb7bb3ba1e4314773cb4c19cec7d0be5ac5c`  
		Last Modified: Fri, 16 Jan 2026 02:18:30 GMT  
		Size: 17.7 MB (17681426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31ca1e20c455cfe5d6984f0d68f5676a5c2dbbf3bccd9b974330e170880b679`  
		Last Modified: Fri, 16 Jan 2026 02:18:31 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ef0f3eb0afa05f59e72564ba6118301accf1df33b16de448e0792364fb0f564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137100411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd15eec77a38217628e23ef12d87b0407c945f512c375f04ea91b271913b32c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:42:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4eaed05c1178f3c3abdac8710778abf118d80e3bc2740ff1270b8e4316b14`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 1.2 MB (1214255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8fdf13cb39747e8c67471f5fd7e7eb6060b2cf311a7e56c64f6ea8a77a5b63`  
		Last Modified: Thu, 15 Jan 2026 22:42:39 GMT  
		Size: 5.9 MB (5943245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e54e499a91704d69c814930daaf58f6daab8d4e90cb5515d9292d6adf0420`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 97.3 KB (97262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01a8729ed4ffcbfea0a8f2b6e3d75fb2b3d6fbca0adae54bdcca438384f878`  
		Last Modified: Thu, 15 Jan 2026 22:42:54 GMT  
		Size: 102.5 MB (102461954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb96ce313cf0c46ab959a2078235f16180a94cb84463bf95ee21b57ddee0bd9`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:967382a1c38611b9bc0172b342bd0c773f400c564463104dca8878394dbc7b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17682510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bff8c8c6b1315cebd5e9c254b4c74f23dafc92e2428cf39b498ba788c947232`

```dockerfile
```

-	Layers:
	-	`sha256:3751c79de9911e1a26a0311151c9fcd345deae4e47a1cb73c31798b7d7133bf8`  
		Last Modified: Fri, 16 Jan 2026 02:18:49 GMT  
		Size: 17.7 MB (17667771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e6846c0bec695a5b996cbd814e6a782dfcfaee6fe4f04fc6d079242e1ad9ca`  
		Last Modified: Fri, 16 Jan 2026 02:18:50 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:cd9f3331edf8c29d61e091e76654eb1161c7971ff443b1a00e3244bd62e37051
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:f69b5539fceb0e0129a08a4e5cffc7582b77c0205929d55a6cb3346ebecee432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141544514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672cbb3e4dc690aa49ad38bbfad559d3e83e013d9789a378e65126aad5c0f71b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:40:50 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:40:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f147c465ef3441f6a6fadaa4bf3dd1b68d753988b404893e8e575a24a013be1`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 1.2 MB (1214139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b6a798b5088fee7bc0bfb188bdd445113b407842d17edf502e09f2fc1b536`  
		Last Modified: Thu, 15 Jan 2026 22:41:25 GMT  
		Size: 6.0 MB (5992568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd839ce83db999d5035a7a3825b0dfa72a58cb764b8a8ea0c500fbed89b583b`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 97.2 KB (97222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1e1824e50f15537f4e31add7722621bc890f927e27f1505e54da0b51bc4c1b`  
		Last Modified: Thu, 15 Jan 2026 22:41:37 GMT  
		Size: 104.7 MB (104703723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dabda1f44ba2f0c461142f451ba75451f7348aa265fbe6a04dd0ff2654448d`  
		Last Modified: Thu, 15 Jan 2026 22:41:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4fc3d5fcfbb3581dce7815009c262c42533eb9c376a299da43240c7034cc07b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17696040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ae6d258fc9e421f1f32bde317f386912b70388378ed0f2996dce493e33e66d`

```dockerfile
```

-	Layers:
	-	`sha256:28c9ab24b1fe7b7ba054f5b971dcdb7bb3ba1e4314773cb4c19cec7d0be5ac5c`  
		Last Modified: Fri, 16 Jan 2026 02:18:30 GMT  
		Size: 17.7 MB (17681426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31ca1e20c455cfe5d6984f0d68f5676a5c2dbbf3bccd9b974330e170880b679`  
		Last Modified: Fri, 16 Jan 2026 02:18:31 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ef0f3eb0afa05f59e72564ba6118301accf1df33b16de448e0792364fb0f564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137100411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd15eec77a38217628e23ef12d87b0407c945f512c375f04ea91b271913b32c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:42:04 GMT
ENV ROS_DISTRO=humble
# Thu, 15 Jan 2026 22:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:42:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:42:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4eaed05c1178f3c3abdac8710778abf118d80e3bc2740ff1270b8e4316b14`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 1.2 MB (1214255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8fdf13cb39747e8c67471f5fd7e7eb6060b2cf311a7e56c64f6ea8a77a5b63`  
		Last Modified: Thu, 15 Jan 2026 22:42:39 GMT  
		Size: 5.9 MB (5943245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e54e499a91704d69c814930daaf58f6daab8d4e90cb5515d9292d6adf0420`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 97.3 KB (97262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01a8729ed4ffcbfea0a8f2b6e3d75fb2b3d6fbca0adae54bdcca438384f878`  
		Last Modified: Thu, 15 Jan 2026 22:42:54 GMT  
		Size: 102.5 MB (102461954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb96ce313cf0c46ab959a2078235f16180a94cb84463bf95ee21b57ddee0bd9`  
		Last Modified: Thu, 15 Jan 2026 22:42:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:967382a1c38611b9bc0172b342bd0c773f400c564463104dca8878394dbc7b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17682510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bff8c8c6b1315cebd5e9c254b4c74f23dafc92e2428cf39b498ba788c947232`

```dockerfile
```

-	Layers:
	-	`sha256:3751c79de9911e1a26a0311151c9fcd345deae4e47a1cb73c31798b7d7133bf8`  
		Last Modified: Fri, 16 Jan 2026 02:18:49 GMT  
		Size: 17.7 MB (17667771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e6846c0bec695a5b996cbd814e6a782dfcfaee6fe4f04fc6d079242e1ad9ca`  
		Last Modified: Fri, 16 Jan 2026 02:18:50 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:af9454f13d342c58bb9f3364424e3e7026184e59a47de75f915d241cb7ec6666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:f3dba6618d45181f7a68cb3f2b9a9da9d52c3315d805fb99687123a80eff10df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296053963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fbe811330cd2f7e3c52c4a6d4369c0581f7679d8b5d48c8cd6e5f20c017302`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:05 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:57:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97c22d0e00b55e0e76a4395fe1b24e90d3b47b63ba12fa85f4711cb8358053`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 684.0 KB (683988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a7fb7868e491005250578970a3f67cb03fc46599910002a9d21bfb3dc79d2`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 6.7 MB (6747519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e5ddd305d765e1f55231776d7dff9595c9b0ea45bd0343566a5ad40f68dc1`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 94.2 KB (94189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75495656f22ab4b88f855531eff7ac03bbc6c08aeac9b335721f9a63b952eaeb`  
		Last Modified: Thu, 15 Jan 2026 22:41:48 GMT  
		Size: 120.2 MB (120220982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23510d5a445e9cf17fa443c4c1c91b8f41ddab3939641059429f56d90b302b`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a2d5b61aaf7e2e0547a70431b18a46188a6e920efa30a196e73b6b9abd45f4`  
		Last Modified: Fri, 16 Jan 2026 00:58:27 GMT  
		Size: 110.2 MB (110183100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758dc4c4511d77e8139294b47787d28096781d5b2ef8f4caf1144e9fbe6f561`  
		Last Modified: Fri, 16 Jan 2026 00:58:16 GMT  
		Size: 390.3 KB (390326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda5a314ef599a1d2f9db599331d5bf2e05dc8c9b658de57954f6a5f24d246ad`  
		Last Modified: Fri, 16 Jan 2026 00:58:16 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673747666502f74a4c28e3b441004032e9d058d9b70a031ca3606ea0644f87b3`  
		Last Modified: Fri, 16 Jan 2026 00:58:21 GMT  
		Size: 28.0 MB (28005148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:489faad951607a6a8c266763d0b39d81613d6c0d08896cb14c2cad83a06b29de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24561461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44151c680004f3aef9280bfa546fa843c046063206bb85940671f664c80d210`

```dockerfile
```

-	Layers:
	-	`sha256:efcf6f164767bef316bca6384f77c11bf81a593e100ed0155c2e78cbecd59ea9`  
		Last Modified: Fri, 16 Jan 2026 02:18:41 GMT  
		Size: 24.5 MB (24544841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f8acd13b1ba88981339bf29e7b8665c281a468711d5d8e259e6fd22a3713d0`  
		Last Modified: Fri, 16 Jan 2026 02:18:42 GMT  
		Size: 16.6 KB (16620 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93482033b6cf937dcc1e404218b02213b008f7036e4aa2add797dbef8b63f6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284482132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98deedb66635f35717a5c1b6b33bf4b90b9b61668da1541760a28bc494f25da5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:00:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:00:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcffa1213fa57586fd8eaccb12bf58db71567acfe6beb2604ce14a7fce49350`  
		Last Modified: Thu, 15 Jan 2026 22:44:40 GMT  
		Size: 684.1 KB (684123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d2c4ddc36db2e4f53f41ed5aae6e0d424f34360990c6490205b5a1a3dd1d`  
		Last Modified: Thu, 15 Jan 2026 22:44:42 GMT  
		Size: 6.8 MB (6761160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2a4235e2d4774a07bc75a44ba91842de78e74f47130b4f9ae6772c1b3ef31`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 94.3 KB (94272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963243806f290c98f3cd72253b9a344178c64bd19c4076a4d0fc0fe366cb4d75`  
		Last Modified: Thu, 15 Jan 2026 22:44:57 GMT  
		Size: 115.0 MB (114993652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99dc06e4d3709628f00f7c925bb0aaf1e36c23f5295a0ce0a3bb297c1265d1`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ded0d19c79a23e1eb3c9c493b71bc3aaf47b095d79cdf0da647eb55203289a`  
		Last Modified: Fri, 16 Jan 2026 01:01:42 GMT  
		Size: 105.6 MB (105592399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a29344c731ff62579c4b41928a004f7229c263244eb3cf2e9cfa02ee6a82911`  
		Last Modified: Fri, 16 Jan 2026 01:01:32 GMT  
		Size: 390.3 KB (390338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdb3e21e95af01abb665679711c101cb346091241dab45013bb305b86c3f28`  
		Last Modified: Fri, 16 Jan 2026 01:01:32 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215247acb520778e621dccad3a665d57a8e8bd9d18e532c921fde7b876b7e46`  
		Last Modified: Fri, 16 Jan 2026 01:01:35 GMT  
		Size: 27.1 MB (27099655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:ba47a82a66bf9e3371eec41b3ec9dfb28946205921edc356aa608730d92d45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5ec4280e4f026f58488178410f21315f441a865dd169e428cc9b45d79f1262`

```dockerfile
```

-	Layers:
	-	`sha256:1fe22c8f0fdab48afe6837bd75771d82729a93a29acc734e78affd64a685e1ec`  
		Last Modified: Fri, 16 Jan 2026 02:19:11 GMT  
		Size: 24.6 MB (24567114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf5e37218976a68acdbf1ed803bbb3f4e017f73018f64b38c22700e39db988f`  
		Last Modified: Fri, 16 Jan 2026 02:19:12 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:23ac13cf396221df5cd83dd0b636d920b23ed9b0651c25ba061c0881a90de458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:fdfa5ace8d17e58758391a86579b8e59eb8be21ce6461ae34311dc9854178342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080404531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f17afa977e9553bf8f9d364af72bbbc94a03684c231ebe65e75e3420c16111b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Tue, 13 Jan 2026 01:15:21 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Tue, 13 Jan 2026 01:15:22 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Tue, 13 Jan 2026 01:15:20 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Tue, 13 Jan 2026 01:26:16 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Tue, 13 Jan 2026 01:15:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Tue, 13 Jan 2026 02:15:47 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Tue, 13 Jan 2026 01:15:19 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Tue, 13 Jan 2026 01:15:18 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Tue, 13 Jan 2026 01:15:21 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bace735bfd1b5a18bc9885894ac02044ab2640d66910d38779034a0f110c984a`  
		Last Modified: Tue, 13 Jan 2026 09:22:26 GMT  
		Size: 784.5 MB (784466755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:5da1f098830431730c35068caf61beb59e75268e96b28158e3af6be140b246b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8127ae88fe25268781a0baac627c8d614e8de9bf7c94b195d98770541698c6e`

```dockerfile
```

-	Layers:
	-	`sha256:a0aae68ce3687e68b79a811d89042cea004876b89bc43c7b058ee6e1be35956d`  
		Last Modified: Tue, 13 Jan 2026 13:42:34 GMT  
		Size: 60.7 MB (60706022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78dc0fdcdbe6caa1e02fcc1bb56ec272f8bde016e1d8f49fba170da78496c021`  
		Last Modified: Tue, 13 Jan 2026 13:42:27 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:938f6facaf3810263df124947e631d03e075f5c535f56263274bceae993b75cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.9 MB (978876409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d90f810db0dd1f5f69d47386e8b01c828cde37a2545a362e14a97276f499e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Tue, 13 Jan 2026 02:19:54 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Tue, 13 Jan 2026 02:23:28 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Tue, 13 Jan 2026 03:01:38 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Tue, 13 Jan 2026 03:01:33 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f7f5e89623d6ff02f526197860623344d614b00161b33893d9822c2cced15`  
		Last Modified: Wed, 14 Jan 2026 11:10:25 GMT  
		Size: 694.5 MB (694492997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:4e1ffd49122ba0d4cd551a720ad25a563c6d760cf536511898c390c807b819dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f44731e791978aefb0dd67afb2c84b5951cc6ef71452f4ff0f500a15123f0c`

```dockerfile
```

-	Layers:
	-	`sha256:4d7f0359dd9afa8d1d7b4f1a150ae315c5e631d568fe619014ce90bbe8a7c5a0`  
		Last Modified: Fri, 14 Nov 2025 01:36:53 GMT  
		Size: 60.6 MB (60636547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234858944fcb5e1cc376a120a72ad87bb19b675630a0be21aca85e44b0c454d4`  
		Last Modified: Thu, 15 Jan 2026 06:02:42 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:23ac13cf396221df5cd83dd0b636d920b23ed9b0651c25ba061c0881a90de458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:fdfa5ace8d17e58758391a86579b8e59eb8be21ce6461ae34311dc9854178342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080404531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f17afa977e9553bf8f9d364af72bbbc94a03684c231ebe65e75e3420c16111b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Tue, 13 Jan 2026 01:15:21 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Tue, 13 Jan 2026 01:15:22 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Tue, 13 Jan 2026 01:15:20 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Tue, 13 Jan 2026 01:26:16 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Tue, 13 Jan 2026 01:15:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Tue, 13 Jan 2026 02:15:47 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Tue, 13 Jan 2026 01:15:19 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Tue, 13 Jan 2026 01:15:18 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Tue, 13 Jan 2026 01:15:21 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bace735bfd1b5a18bc9885894ac02044ab2640d66910d38779034a0f110c984a`  
		Last Modified: Tue, 13 Jan 2026 09:22:26 GMT  
		Size: 784.5 MB (784466755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5da1f098830431730c35068caf61beb59e75268e96b28158e3af6be140b246b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8127ae88fe25268781a0baac627c8d614e8de9bf7c94b195d98770541698c6e`

```dockerfile
```

-	Layers:
	-	`sha256:a0aae68ce3687e68b79a811d89042cea004876b89bc43c7b058ee6e1be35956d`  
		Last Modified: Tue, 13 Jan 2026 13:42:34 GMT  
		Size: 60.7 MB (60706022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78dc0fdcdbe6caa1e02fcc1bb56ec272f8bde016e1d8f49fba170da78496c021`  
		Last Modified: Tue, 13 Jan 2026 13:42:27 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:938f6facaf3810263df124947e631d03e075f5c535f56263274bceae993b75cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.9 MB (978876409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d90f810db0dd1f5f69d47386e8b01c828cde37a2545a362e14a97276f499e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Tue, 13 Jan 2026 02:19:54 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Tue, 13 Jan 2026 02:23:28 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Tue, 13 Jan 2026 03:01:38 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Tue, 13 Jan 2026 02:19:49 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Tue, 13 Jan 2026 03:01:33 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f7f5e89623d6ff02f526197860623344d614b00161b33893d9822c2cced15`  
		Last Modified: Wed, 14 Jan 2026 11:10:25 GMT  
		Size: 694.5 MB (694492997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4e1ffd49122ba0d4cd551a720ad25a563c6d760cf536511898c390c807b819dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f44731e791978aefb0dd67afb2c84b5951cc6ef71452f4ff0f500a15123f0c`

```dockerfile
```

-	Layers:
	-	`sha256:4d7f0359dd9afa8d1d7b4f1a150ae315c5e631d568fe619014ce90bbe8a7c5a0`  
		Last Modified: Fri, 14 Nov 2025 01:36:53 GMT  
		Size: 60.6 MB (60636547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234858944fcb5e1cc376a120a72ad87bb19b675630a0be21aca85e44b0c454d4`  
		Last Modified: Thu, 15 Jan 2026 06:02:42 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:af9454f13d342c58bb9f3364424e3e7026184e59a47de75f915d241cb7ec6666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:f3dba6618d45181f7a68cb3f2b9a9da9d52c3315d805fb99687123a80eff10df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296053963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fbe811330cd2f7e3c52c4a6d4369c0581f7679d8b5d48c8cd6e5f20c017302`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:05 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:57:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97c22d0e00b55e0e76a4395fe1b24e90d3b47b63ba12fa85f4711cb8358053`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 684.0 KB (683988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a7fb7868e491005250578970a3f67cb03fc46599910002a9d21bfb3dc79d2`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 6.7 MB (6747519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e5ddd305d765e1f55231776d7dff9595c9b0ea45bd0343566a5ad40f68dc1`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 94.2 KB (94189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75495656f22ab4b88f855531eff7ac03bbc6c08aeac9b335721f9a63b952eaeb`  
		Last Modified: Thu, 15 Jan 2026 22:41:48 GMT  
		Size: 120.2 MB (120220982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23510d5a445e9cf17fa443c4c1c91b8f41ddab3939641059429f56d90b302b`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a2d5b61aaf7e2e0547a70431b18a46188a6e920efa30a196e73b6b9abd45f4`  
		Last Modified: Fri, 16 Jan 2026 00:58:27 GMT  
		Size: 110.2 MB (110183100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758dc4c4511d77e8139294b47787d28096781d5b2ef8f4caf1144e9fbe6f561`  
		Last Modified: Fri, 16 Jan 2026 00:58:16 GMT  
		Size: 390.3 KB (390326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda5a314ef599a1d2f9db599331d5bf2e05dc8c9b658de57954f6a5f24d246ad`  
		Last Modified: Fri, 16 Jan 2026 00:58:16 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673747666502f74a4c28e3b441004032e9d058d9b70a031ca3606ea0644f87b3`  
		Last Modified: Fri, 16 Jan 2026 00:58:21 GMT  
		Size: 28.0 MB (28005148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:489faad951607a6a8c266763d0b39d81613d6c0d08896cb14c2cad83a06b29de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24561461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44151c680004f3aef9280bfa546fa843c046063206bb85940671f664c80d210`

```dockerfile
```

-	Layers:
	-	`sha256:efcf6f164767bef316bca6384f77c11bf81a593e100ed0155c2e78cbecd59ea9`  
		Last Modified: Fri, 16 Jan 2026 02:18:41 GMT  
		Size: 24.5 MB (24544841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f8acd13b1ba88981339bf29e7b8665c281a468711d5d8e259e6fd22a3713d0`  
		Last Modified: Fri, 16 Jan 2026 02:18:42 GMT  
		Size: 16.6 KB (16620 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93482033b6cf937dcc1e404218b02213b008f7036e4aa2add797dbef8b63f6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284482132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98deedb66635f35717a5c1b6b33bf4b90b9b61668da1541760a28bc494f25da5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:00:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:00:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcffa1213fa57586fd8eaccb12bf58db71567acfe6beb2604ce14a7fce49350`  
		Last Modified: Thu, 15 Jan 2026 22:44:40 GMT  
		Size: 684.1 KB (684123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d2c4ddc36db2e4f53f41ed5aae6e0d424f34360990c6490205b5a1a3dd1d`  
		Last Modified: Thu, 15 Jan 2026 22:44:42 GMT  
		Size: 6.8 MB (6761160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2a4235e2d4774a07bc75a44ba91842de78e74f47130b4f9ae6772c1b3ef31`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 94.3 KB (94272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963243806f290c98f3cd72253b9a344178c64bd19c4076a4d0fc0fe366cb4d75`  
		Last Modified: Thu, 15 Jan 2026 22:44:57 GMT  
		Size: 115.0 MB (114993652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99dc06e4d3709628f00f7c925bb0aaf1e36c23f5295a0ce0a3bb297c1265d1`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ded0d19c79a23e1eb3c9c493b71bc3aaf47b095d79cdf0da647eb55203289a`  
		Last Modified: Fri, 16 Jan 2026 01:01:42 GMT  
		Size: 105.6 MB (105592399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a29344c731ff62579c4b41928a004f7229c263244eb3cf2e9cfa02ee6a82911`  
		Last Modified: Fri, 16 Jan 2026 01:01:32 GMT  
		Size: 390.3 KB (390338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdb3e21e95af01abb665679711c101cb346091241dab45013bb305b86c3f28`  
		Last Modified: Fri, 16 Jan 2026 01:01:32 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215247acb520778e621dccad3a665d57a8e8bd9d18e532c921fde7b876b7e46`  
		Last Modified: Fri, 16 Jan 2026 01:01:35 GMT  
		Size: 27.1 MB (27099655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:ba47a82a66bf9e3371eec41b3ec9dfb28946205921edc356aa608730d92d45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5ec4280e4f026f58488178410f21315f441a865dd169e428cc9b45d79f1262`

```dockerfile
```

-	Layers:
	-	`sha256:1fe22c8f0fdab48afe6837bd75771d82729a93a29acc734e78affd64a685e1ec`  
		Last Modified: Fri, 16 Jan 2026 02:19:11 GMT  
		Size: 24.6 MB (24567114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf5e37218976a68acdbf1ed803bbb3f4e017f73018f64b38c22700e39db988f`  
		Last Modified: Fri, 16 Jan 2026 02:19:12 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:af9454f13d342c58bb9f3364424e3e7026184e59a47de75f915d241cb7ec6666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:f3dba6618d45181f7a68cb3f2b9a9da9d52c3315d805fb99687123a80eff10df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296053963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fbe811330cd2f7e3c52c4a6d4369c0581f7679d8b5d48c8cd6e5f20c017302`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:05 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:57:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97c22d0e00b55e0e76a4395fe1b24e90d3b47b63ba12fa85f4711cb8358053`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 684.0 KB (683988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a7fb7868e491005250578970a3f67cb03fc46599910002a9d21bfb3dc79d2`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 6.7 MB (6747519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e5ddd305d765e1f55231776d7dff9595c9b0ea45bd0343566a5ad40f68dc1`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 94.2 KB (94189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75495656f22ab4b88f855531eff7ac03bbc6c08aeac9b335721f9a63b952eaeb`  
		Last Modified: Thu, 15 Jan 2026 22:41:48 GMT  
		Size: 120.2 MB (120220982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23510d5a445e9cf17fa443c4c1c91b8f41ddab3939641059429f56d90b302b`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a2d5b61aaf7e2e0547a70431b18a46188a6e920efa30a196e73b6b9abd45f4`  
		Last Modified: Fri, 16 Jan 2026 00:58:27 GMT  
		Size: 110.2 MB (110183100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758dc4c4511d77e8139294b47787d28096781d5b2ef8f4caf1144e9fbe6f561`  
		Last Modified: Fri, 16 Jan 2026 00:58:16 GMT  
		Size: 390.3 KB (390326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda5a314ef599a1d2f9db599331d5bf2e05dc8c9b658de57954f6a5f24d246ad`  
		Last Modified: Fri, 16 Jan 2026 00:58:16 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673747666502f74a4c28e3b441004032e9d058d9b70a031ca3606ea0644f87b3`  
		Last Modified: Fri, 16 Jan 2026 00:58:21 GMT  
		Size: 28.0 MB (28005148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:489faad951607a6a8c266763d0b39d81613d6c0d08896cb14c2cad83a06b29de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24561461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44151c680004f3aef9280bfa546fa843c046063206bb85940671f664c80d210`

```dockerfile
```

-	Layers:
	-	`sha256:efcf6f164767bef316bca6384f77c11bf81a593e100ed0155c2e78cbecd59ea9`  
		Last Modified: Fri, 16 Jan 2026 02:18:41 GMT  
		Size: 24.5 MB (24544841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f8acd13b1ba88981339bf29e7b8665c281a468711d5d8e259e6fd22a3713d0`  
		Last Modified: Fri, 16 Jan 2026 02:18:42 GMT  
		Size: 16.6 KB (16620 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93482033b6cf937dcc1e404218b02213b008f7036e4aa2add797dbef8b63f6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284482132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98deedb66635f35717a5c1b6b33bf4b90b9b61668da1541760a28bc494f25da5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:00:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:00:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcffa1213fa57586fd8eaccb12bf58db71567acfe6beb2604ce14a7fce49350`  
		Last Modified: Thu, 15 Jan 2026 22:44:40 GMT  
		Size: 684.1 KB (684123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d2c4ddc36db2e4f53f41ed5aae6e0d424f34360990c6490205b5a1a3dd1d`  
		Last Modified: Thu, 15 Jan 2026 22:44:42 GMT  
		Size: 6.8 MB (6761160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2a4235e2d4774a07bc75a44ba91842de78e74f47130b4f9ae6772c1b3ef31`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 94.3 KB (94272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963243806f290c98f3cd72253b9a344178c64bd19c4076a4d0fc0fe366cb4d75`  
		Last Modified: Thu, 15 Jan 2026 22:44:57 GMT  
		Size: 115.0 MB (114993652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99dc06e4d3709628f00f7c925bb0aaf1e36c23f5295a0ce0a3bb297c1265d1`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ded0d19c79a23e1eb3c9c493b71bc3aaf47b095d79cdf0da647eb55203289a`  
		Last Modified: Fri, 16 Jan 2026 01:01:42 GMT  
		Size: 105.6 MB (105592399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a29344c731ff62579c4b41928a004f7229c263244eb3cf2e9cfa02ee6a82911`  
		Last Modified: Fri, 16 Jan 2026 01:01:32 GMT  
		Size: 390.3 KB (390338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdb3e21e95af01abb665679711c101cb346091241dab45013bb305b86c3f28`  
		Last Modified: Fri, 16 Jan 2026 01:01:32 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215247acb520778e621dccad3a665d57a8e8bd9d18e532c921fde7b876b7e46`  
		Last Modified: Fri, 16 Jan 2026 01:01:35 GMT  
		Size: 27.1 MB (27099655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ba47a82a66bf9e3371eec41b3ec9dfb28946205921edc356aa608730d92d45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5ec4280e4f026f58488178410f21315f441a865dd169e428cc9b45d79f1262`

```dockerfile
```

-	Layers:
	-	`sha256:1fe22c8f0fdab48afe6837bd75771d82729a93a29acc734e78affd64a685e1ec`  
		Last Modified: Fri, 16 Jan 2026 02:19:11 GMT  
		Size: 24.6 MB (24567114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf5e37218976a68acdbf1ed803bbb3f4e017f73018f64b38c22700e39db988f`  
		Last Modified: Fri, 16 Jan 2026 02:19:12 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:71b21e1390c09b35f73999111c61b7fe75d51bb4a5217d27a4bdd72fa9e21ca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d22508ec16651e1719c347630de078a2627d97667d60f9efeb91271298e7e4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157472885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc26263419dba1dbf419e1eb7c55c3033836cdc79171cf4c24d2f1f11f3b544`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97c22d0e00b55e0e76a4395fe1b24e90d3b47b63ba12fa85f4711cb8358053`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 684.0 KB (683988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a7fb7868e491005250578970a3f67cb03fc46599910002a9d21bfb3dc79d2`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 6.7 MB (6747519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e5ddd305d765e1f55231776d7dff9595c9b0ea45bd0343566a5ad40f68dc1`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 94.2 KB (94189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75495656f22ab4b88f855531eff7ac03bbc6c08aeac9b335721f9a63b952eaeb`  
		Last Modified: Thu, 15 Jan 2026 22:41:48 GMT  
		Size: 120.2 MB (120220982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23510d5a445e9cf17fa443c4c1c91b8f41ddab3939641059429f56d90b302b`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:718bacb15f35078b0f28d8b6047d5c326fe40fe47fd37142e7b8512656dbcdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c07be828c2fac7a05fbe19e8c0d476f19a510ed25c4e30c61b9941793b847b6`

```dockerfile
```

-	Layers:
	-	`sha256:6dca5a67023b62c342e40a64f5d0717f56e26a2eb18cc49dd99ee95a1d8b9248`  
		Last Modified: Fri, 16 Jan 2026 02:18:55 GMT  
		Size: 18.3 MB (18301254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d33a19228a0f7b7e5affac08b64dd7b3018d9918f08433340ad526703e3352b`  
		Last Modified: Fri, 16 Jan 2026 02:18:56 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:25f346d4dbf19305ea83113abb49583cb9327ec9c001a11028a62a8bc046ec5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151397228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98868b6a2a3d210a3b8da7ba7f82445bc7c98c3122feca22287a21dd940849b7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcffa1213fa57586fd8eaccb12bf58db71567acfe6beb2604ce14a7fce49350`  
		Last Modified: Thu, 15 Jan 2026 22:44:40 GMT  
		Size: 684.1 KB (684123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d2c4ddc36db2e4f53f41ed5aae6e0d424f34360990c6490205b5a1a3dd1d`  
		Last Modified: Thu, 15 Jan 2026 22:44:42 GMT  
		Size: 6.8 MB (6761160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2a4235e2d4774a07bc75a44ba91842de78e74f47130b4f9ae6772c1b3ef31`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 94.3 KB (94272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963243806f290c98f3cd72253b9a344178c64bd19c4076a4d0fc0fe366cb4d75`  
		Last Modified: Thu, 15 Jan 2026 22:44:57 GMT  
		Size: 115.0 MB (114993652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99dc06e4d3709628f00f7c925bb0aaf1e36c23f5295a0ce0a3bb297c1265d1`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:244624508e6ef55aaeba85735fa4607485b5b4edef248eab60e6a551218e88c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18289984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981da7bd5f5fa9436399bdfe216f1a2714f1211b91630059a9109f1d3f89c5a`

```dockerfile
```

-	Layers:
	-	`sha256:9337bd5620a9882a694b82a266e8d2edd29bfbdbf6693e5ae60367f41a2407be`  
		Last Modified: Fri, 16 Jan 2026 02:19:14 GMT  
		Size: 18.3 MB (18275260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6852199e7efbbfe0640b063a1e2afe61733440d39d665644169a40f486ca6e8`  
		Last Modified: Fri, 16 Jan 2026 02:19:15 GMT  
		Size: 14.7 KB (14724 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:71b21e1390c09b35f73999111c61b7fe75d51bb4a5217d27a4bdd72fa9e21ca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:d22508ec16651e1719c347630de078a2627d97667d60f9efeb91271298e7e4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157472885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc26263419dba1dbf419e1eb7c55c3033836cdc79171cf4c24d2f1f11f3b544`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97c22d0e00b55e0e76a4395fe1b24e90d3b47b63ba12fa85f4711cb8358053`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 684.0 KB (683988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a7fb7868e491005250578970a3f67cb03fc46599910002a9d21bfb3dc79d2`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 6.7 MB (6747519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e5ddd305d765e1f55231776d7dff9595c9b0ea45bd0343566a5ad40f68dc1`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 94.2 KB (94189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75495656f22ab4b88f855531eff7ac03bbc6c08aeac9b335721f9a63b952eaeb`  
		Last Modified: Thu, 15 Jan 2026 22:41:48 GMT  
		Size: 120.2 MB (120220982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23510d5a445e9cf17fa443c4c1c91b8f41ddab3939641059429f56d90b302b`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:718bacb15f35078b0f28d8b6047d5c326fe40fe47fd37142e7b8512656dbcdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c07be828c2fac7a05fbe19e8c0d476f19a510ed25c4e30c61b9941793b847b6`

```dockerfile
```

-	Layers:
	-	`sha256:6dca5a67023b62c342e40a64f5d0717f56e26a2eb18cc49dd99ee95a1d8b9248`  
		Last Modified: Fri, 16 Jan 2026 02:18:55 GMT  
		Size: 18.3 MB (18301254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d33a19228a0f7b7e5affac08b64dd7b3018d9918f08433340ad526703e3352b`  
		Last Modified: Fri, 16 Jan 2026 02:18:56 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:25f346d4dbf19305ea83113abb49583cb9327ec9c001a11028a62a8bc046ec5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151397228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98868b6a2a3d210a3b8da7ba7f82445bc7c98c3122feca22287a21dd940849b7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcffa1213fa57586fd8eaccb12bf58db71567acfe6beb2604ce14a7fce49350`  
		Last Modified: Thu, 15 Jan 2026 22:44:40 GMT  
		Size: 684.1 KB (684123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d2c4ddc36db2e4f53f41ed5aae6e0d424f34360990c6490205b5a1a3dd1d`  
		Last Modified: Thu, 15 Jan 2026 22:44:42 GMT  
		Size: 6.8 MB (6761160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2a4235e2d4774a07bc75a44ba91842de78e74f47130b4f9ae6772c1b3ef31`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 94.3 KB (94272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963243806f290c98f3cd72253b9a344178c64bd19c4076a4d0fc0fe366cb4d75`  
		Last Modified: Thu, 15 Jan 2026 22:44:57 GMT  
		Size: 115.0 MB (114993652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99dc06e4d3709628f00f7c925bb0aaf1e36c23f5295a0ce0a3bb297c1265d1`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:244624508e6ef55aaeba85735fa4607485b5b4edef248eab60e6a551218e88c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18289984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0981da7bd5f5fa9436399bdfe216f1a2714f1211b91630059a9109f1d3f89c5a`

```dockerfile
```

-	Layers:
	-	`sha256:9337bd5620a9882a694b82a266e8d2edd29bfbdbf6693e5ae60367f41a2407be`  
		Last Modified: Fri, 16 Jan 2026 02:19:14 GMT  
		Size: 18.3 MB (18275260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6852199e7efbbfe0640b063a1e2afe61733440d39d665644169a40f486ca6e8`  
		Last Modified: Fri, 16 Jan 2026 02:19:15 GMT  
		Size: 14.7 KB (14724 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:4e0197b33afe3a4f6e881e1478d79fa9b374a8e2a155209678eba09d53ad460d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:9e0739f8d0c7b66dd78c61853d0f8d3803c53bff95f8384226a061556cf81784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296892761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cad5147080770cde20dab3d15b86eb33c5ba126674235c2f4fbfa73957ca86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:41:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:36 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fae7f48a46da951e313f18a6daf495d637bd45e1d4f7d040911c1f2ee7b972`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc1c27f9559dd6ff1cdbfe218890a4794f42a6099b771506e057d7764a7720`  
		Last Modified: Thu, 15 Jan 2026 22:42:11 GMT  
		Size: 6.7 MB (6747522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21f7fe8d5212d488b694908db57f4df8b1edd9165e7ef82d3b595cb236521`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 94.2 KB (94176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b77d824f0ae70e13124dcbd7bfd2d9fac9328ca8a3a90e3f5993a9b4afe030`  
		Last Modified: Thu, 15 Jan 2026 22:42:27 GMT  
		Size: 121.0 MB (121016025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206cf29389588b7b19b55414eb210e1dd6f08621c5925cc97783e2512e2448b`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4139627acf1d2dfacd85fc36c6189af287834fafc74629ff2615296c058bf3da`  
		Last Modified: Fri, 16 Jan 2026 00:58:59 GMT  
		Size: 110.2 MB (110187099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e2efff092f53ee7789ee08cbb160b3b85b87524a06744e8e91cab9cf9ca171`  
		Last Modified: Fri, 16 Jan 2026 00:58:50 GMT  
		Size: 371.7 KB (371744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723794c7050a1b79f891d804f844d9e39317679cba5ca2031f687bca2592df7b`  
		Last Modified: Fri, 16 Jan 2026 00:58:50 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06850daf351b3a2227558f1f02fa276838ebc17e954b4895c983ca9efa734cbb`  
		Last Modified: Fri, 16 Jan 2026 00:58:54 GMT  
		Size: 28.1 MB (28063475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:88c7a9fb1d1e64d01df3cf05229a4b9c9e803860bcfa123bc4958b6720acfe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24600251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66db517cc6a7ebecdab82a2812cf460be1665864b80237f96fe73da203108045`

```dockerfile
```

-	Layers:
	-	`sha256:f0459c0d1e93f372bc00f9de10850f232cac56d0bdd746a4ac7b794e60636578`  
		Last Modified: Fri, 16 Jan 2026 02:19:06 GMT  
		Size: 24.6 MB (24583904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814a4b4c3e95a6478b13dfc14eb736461afc47c6f7070915ccc6b04b85762a95`  
		Last Modified: Fri, 16 Jan 2026 02:19:07 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d40086d2c2c1539b1a8eee67e35a0d1cd7104a23813a8bfc2098d7323f14581c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285260217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84f27d37d0626e98ab374aad076c6fc617065002dc2aa185faaf91f22385b9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:41 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:44:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:24 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0ffeb8abf9f69d9152d9ddf05b3d9bf0abd0da07487f555fca9183c211600`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 684.1 KB (684101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec456ec14866e45cf8752da07321782d64ae4e50014222025f952c73348f74`  
		Last Modified: Thu, 15 Jan 2026 22:45:03 GMT  
		Size: 6.8 MB (6761200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535702c99d332d44232b15396c6984e051db229f065200199d57a426a3e62760`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 94.3 KB (94254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41213d7b9319bb10daf024007dce1857fe9d550536f830b9d1d7646b1c9007`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 115.7 MB (115742618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee8712744d000fd48a2c882b325511146d3667fa87b4546ad01002eb3efcd4`  
		Last Modified: Thu, 15 Jan 2026 22:45:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fe46905465de7cdf7df0c256bc882a5c6f6bce00a12443b384513c5446e4ec`  
		Last Modified: Fri, 16 Jan 2026 01:02:10 GMT  
		Size: 105.6 MB (105595239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09271007bf03040fc00ce410c5798e4c25d9a95699468661d096af654f19d170`  
		Last Modified: Fri, 16 Jan 2026 01:02:03 GMT  
		Size: 371.7 KB (371749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53da40f77632a2aede7a153c740aa61a40ad8c211cd72001665ddd01a1f91a58`  
		Last Modified: Fri, 16 Jan 2026 01:02:03 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf3e21264a6cf710a3de027e72eb48ed241babcb1b8c1ba3d0457d768260a11`  
		Last Modified: Fri, 16 Jan 2026 01:02:06 GMT  
		Size: 27.1 MB (27144525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:a488e8c6562c5bf506883d9347416992ef055c6c2882ab8215a6c78a25ca4f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24622649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cdb796ffdafb23da6b45ed06f8bf1fef5d600da824ab8d268824b74ad35f59`

```dockerfile
```

-	Layers:
	-	`sha256:42ea77cedb88eb06075335c1896ee3a19f0b13156db6a51af9f9153d82234249`  
		Last Modified: Fri, 16 Jan 2026 02:19:36 GMT  
		Size: 24.6 MB (24606165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cac50e00f17e0383ef1f9fe799d22b586da1fbc5372c1220ef1e3bcc7142dc9`  
		Last Modified: Fri, 16 Jan 2026 02:19:37 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:597eb7c1b6ef46d03c1306786771714cef4064d5654887ca996713712185a190
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:39acb6f9dbe66091f760eb26611744af06f98cc62d21a8ebb6e826ceea4ab104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1095999495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3065d8b3834d1c8b2fa54e8585dca47f3a383187ecf1ab1ad05190a0ea929`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Tue, 13 Jan 2026 03:24:54 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Tue, 13 Jan 2026 03:24:55 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Tue, 13 Jan 2026 03:24:54 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Tue, 13 Jan 2026 02:33:32 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Tue, 13 Jan 2026 03:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Tue, 13 Jan 2026 03:24:59 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Tue, 13 Jan 2026 02:26:11 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Tue, 13 Jan 2026 03:24:56 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Tue, 13 Jan 2026 03:24:58 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe6b475c9d5d0fec8f295a27b9c88c7e104854439857ec2508c68a04327c933`  
		Last Modified: Thu, 15 Jan 2026 06:57:35 GMT  
		Size: 785.0 MB (784968985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:49b431be399ca5fe716018c10a722888c1fa293c5be0710962d4a84c3257101b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3e84ea6271ee0ddf4c85b11145a84b6e7efe869fc8a1a05673e392f0ef2c1a`

```dockerfile
```

-	Layers:
	-	`sha256:4846b83d86f5b32056c650890347f732ff8a4c09aaad50f312de07d40693ab51`  
		Last Modified: Thu, 15 Jan 2026 08:19:53 GMT  
		Size: 60.8 MB (60822416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e11511c30e26ba831e3130603c6135fa399dce361debb54e7debc7755ac46e`  
		Last Modified: Thu, 15 Jan 2026 08:19:49 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d69e6b68fbf0b451f2d2916f8320507c33e47620dea9c9609ff663bb0e5bd47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.3 MB (994340523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67faf80aeacd3fac0059ebc1e8ab26ce58f1016a22fea364f281a5d6103c1f51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Tue, 13 Jan 2026 01:00:11 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Tue, 13 Jan 2026 01:00:14 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Tue, 13 Jan 2026 01:00:20 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Wed, 14 Jan 2026 08:58:05 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Tue, 13 Jan 2026 01:00:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Tue, 13 Jan 2026 23:34:51 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Tue, 13 Jan 2026 01:00:41 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Tue, 13 Jan 2026 01:00:43 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Tue, 13 Jan 2026 23:34:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ec05d315c3cb7241734afa22b2b434a0e74d932c29d5d3e00d0d27e8b1a342`  
		Last Modified: Fri, 14 Nov 2025 01:37:11 GMT  
		Size: 695.0 MB (694963924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:03337ba5432546dcb0a55a48d697155319d747795cc06ec0447dcc510d22d2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760579d59a40d6d4b825b88fe7a6a01c47c48a4ac352b70eb03ac1622161c190`

```dockerfile
```

-	Layers:
	-	`sha256:d5dc70d9db7a43715963e98a03df7919d4e1749a716a4262a67bba890d0ce0e7`  
		Last Modified: Fri, 14 Nov 2025 01:36:59 GMT  
		Size: 60.8 MB (60752941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813bbfb4e7dd5d9cfaffd99d1a7feba515a6390671be13bda5c0949e7effd486`  
		Last Modified: Fri, 14 Nov 2025 01:36:55 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:597eb7c1b6ef46d03c1306786771714cef4064d5654887ca996713712185a190
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:39acb6f9dbe66091f760eb26611744af06f98cc62d21a8ebb6e826ceea4ab104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1095999495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3065d8b3834d1c8b2fa54e8585dca47f3a383187ecf1ab1ad05190a0ea929`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Tue, 13 Jan 2026 03:24:54 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Tue, 13 Jan 2026 03:24:55 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Tue, 13 Jan 2026 03:24:54 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Tue, 13 Jan 2026 02:33:32 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Tue, 13 Jan 2026 03:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Tue, 13 Jan 2026 03:24:59 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Tue, 13 Jan 2026 02:26:11 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Tue, 13 Jan 2026 03:24:56 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Tue, 13 Jan 2026 03:24:58 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe6b475c9d5d0fec8f295a27b9c88c7e104854439857ec2508c68a04327c933`  
		Last Modified: Thu, 15 Jan 2026 06:57:35 GMT  
		Size: 785.0 MB (784968985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:49b431be399ca5fe716018c10a722888c1fa293c5be0710962d4a84c3257101b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3e84ea6271ee0ddf4c85b11145a84b6e7efe869fc8a1a05673e392f0ef2c1a`

```dockerfile
```

-	Layers:
	-	`sha256:4846b83d86f5b32056c650890347f732ff8a4c09aaad50f312de07d40693ab51`  
		Last Modified: Thu, 15 Jan 2026 08:19:53 GMT  
		Size: 60.8 MB (60822416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e11511c30e26ba831e3130603c6135fa399dce361debb54e7debc7755ac46e`  
		Last Modified: Thu, 15 Jan 2026 08:19:49 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d69e6b68fbf0b451f2d2916f8320507c33e47620dea9c9609ff663bb0e5bd47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.3 MB (994340523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67faf80aeacd3fac0059ebc1e8ab26ce58f1016a22fea364f281a5d6103c1f51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Tue, 13 Jan 2026 01:00:11 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Tue, 13 Jan 2026 01:00:14 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Tue, 13 Jan 2026 01:00:20 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Wed, 14 Jan 2026 08:58:05 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Tue, 13 Jan 2026 01:00:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Tue, 13 Jan 2026 23:34:51 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Tue, 13 Jan 2026 01:00:41 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Tue, 13 Jan 2026 01:00:43 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Tue, 13 Jan 2026 23:34:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ec05d315c3cb7241734afa22b2b434a0e74d932c29d5d3e00d0d27e8b1a342`  
		Last Modified: Fri, 14 Nov 2025 01:37:11 GMT  
		Size: 695.0 MB (694963924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:03337ba5432546dcb0a55a48d697155319d747795cc06ec0447dcc510d22d2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760579d59a40d6d4b825b88fe7a6a01c47c48a4ac352b70eb03ac1622161c190`

```dockerfile
```

-	Layers:
	-	`sha256:d5dc70d9db7a43715963e98a03df7919d4e1749a716a4262a67bba890d0ce0e7`  
		Last Modified: Fri, 14 Nov 2025 01:36:59 GMT  
		Size: 60.8 MB (60752941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813bbfb4e7dd5d9cfaffd99d1a7feba515a6390671be13bda5c0949e7effd486`  
		Last Modified: Fri, 14 Nov 2025 01:36:55 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:4e0197b33afe3a4f6e881e1478d79fa9b374a8e2a155209678eba09d53ad460d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:9e0739f8d0c7b66dd78c61853d0f8d3803c53bff95f8384226a061556cf81784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296892761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cad5147080770cde20dab3d15b86eb33c5ba126674235c2f4fbfa73957ca86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:41:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:36 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fae7f48a46da951e313f18a6daf495d637bd45e1d4f7d040911c1f2ee7b972`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc1c27f9559dd6ff1cdbfe218890a4794f42a6099b771506e057d7764a7720`  
		Last Modified: Thu, 15 Jan 2026 22:42:11 GMT  
		Size: 6.7 MB (6747522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21f7fe8d5212d488b694908db57f4df8b1edd9165e7ef82d3b595cb236521`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 94.2 KB (94176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b77d824f0ae70e13124dcbd7bfd2d9fac9328ca8a3a90e3f5993a9b4afe030`  
		Last Modified: Thu, 15 Jan 2026 22:42:27 GMT  
		Size: 121.0 MB (121016025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206cf29389588b7b19b55414eb210e1dd6f08621c5925cc97783e2512e2448b`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4139627acf1d2dfacd85fc36c6189af287834fafc74629ff2615296c058bf3da`  
		Last Modified: Fri, 16 Jan 2026 00:58:59 GMT  
		Size: 110.2 MB (110187099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e2efff092f53ee7789ee08cbb160b3b85b87524a06744e8e91cab9cf9ca171`  
		Last Modified: Fri, 16 Jan 2026 00:58:50 GMT  
		Size: 371.7 KB (371744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723794c7050a1b79f891d804f844d9e39317679cba5ca2031f687bca2592df7b`  
		Last Modified: Fri, 16 Jan 2026 00:58:50 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06850daf351b3a2227558f1f02fa276838ebc17e954b4895c983ca9efa734cbb`  
		Last Modified: Fri, 16 Jan 2026 00:58:54 GMT  
		Size: 28.1 MB (28063475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:88c7a9fb1d1e64d01df3cf05229a4b9c9e803860bcfa123bc4958b6720acfe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24600251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66db517cc6a7ebecdab82a2812cf460be1665864b80237f96fe73da203108045`

```dockerfile
```

-	Layers:
	-	`sha256:f0459c0d1e93f372bc00f9de10850f232cac56d0bdd746a4ac7b794e60636578`  
		Last Modified: Fri, 16 Jan 2026 02:19:06 GMT  
		Size: 24.6 MB (24583904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814a4b4c3e95a6478b13dfc14eb736461afc47c6f7070915ccc6b04b85762a95`  
		Last Modified: Fri, 16 Jan 2026 02:19:07 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d40086d2c2c1539b1a8eee67e35a0d1cd7104a23813a8bfc2098d7323f14581c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285260217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84f27d37d0626e98ab374aad076c6fc617065002dc2aa185faaf91f22385b9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:41 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:44:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:24 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0ffeb8abf9f69d9152d9ddf05b3d9bf0abd0da07487f555fca9183c211600`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 684.1 KB (684101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec456ec14866e45cf8752da07321782d64ae4e50014222025f952c73348f74`  
		Last Modified: Thu, 15 Jan 2026 22:45:03 GMT  
		Size: 6.8 MB (6761200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535702c99d332d44232b15396c6984e051db229f065200199d57a426a3e62760`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 94.3 KB (94254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41213d7b9319bb10daf024007dce1857fe9d550536f830b9d1d7646b1c9007`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 115.7 MB (115742618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee8712744d000fd48a2c882b325511146d3667fa87b4546ad01002eb3efcd4`  
		Last Modified: Thu, 15 Jan 2026 22:45:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fe46905465de7cdf7df0c256bc882a5c6f6bce00a12443b384513c5446e4ec`  
		Last Modified: Fri, 16 Jan 2026 01:02:10 GMT  
		Size: 105.6 MB (105595239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09271007bf03040fc00ce410c5798e4c25d9a95699468661d096af654f19d170`  
		Last Modified: Fri, 16 Jan 2026 01:02:03 GMT  
		Size: 371.7 KB (371749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53da40f77632a2aede7a153c740aa61a40ad8c211cd72001665ddd01a1f91a58`  
		Last Modified: Fri, 16 Jan 2026 01:02:03 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf3e21264a6cf710a3de027e72eb48ed241babcb1b8c1ba3d0457d768260a11`  
		Last Modified: Fri, 16 Jan 2026 01:02:06 GMT  
		Size: 27.1 MB (27144525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:a488e8c6562c5bf506883d9347416992ef055c6c2882ab8215a6c78a25ca4f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24622649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cdb796ffdafb23da6b45ed06f8bf1fef5d600da824ab8d268824b74ad35f59`

```dockerfile
```

-	Layers:
	-	`sha256:42ea77cedb88eb06075335c1896ee3a19f0b13156db6a51af9f9153d82234249`  
		Last Modified: Fri, 16 Jan 2026 02:19:36 GMT  
		Size: 24.6 MB (24606165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cac50e00f17e0383ef1f9fe799d22b586da1fbc5372c1220ef1e3bcc7142dc9`  
		Last Modified: Fri, 16 Jan 2026 02:19:37 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:4e0197b33afe3a4f6e881e1478d79fa9b374a8e2a155209678eba09d53ad460d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:9e0739f8d0c7b66dd78c61853d0f8d3803c53bff95f8384226a061556cf81784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296892761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cad5147080770cde20dab3d15b86eb33c5ba126674235c2f4fbfa73957ca86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:41:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:36 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fae7f48a46da951e313f18a6daf495d637bd45e1d4f7d040911c1f2ee7b972`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc1c27f9559dd6ff1cdbfe218890a4794f42a6099b771506e057d7764a7720`  
		Last Modified: Thu, 15 Jan 2026 22:42:11 GMT  
		Size: 6.7 MB (6747522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21f7fe8d5212d488b694908db57f4df8b1edd9165e7ef82d3b595cb236521`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 94.2 KB (94176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b77d824f0ae70e13124dcbd7bfd2d9fac9328ca8a3a90e3f5993a9b4afe030`  
		Last Modified: Thu, 15 Jan 2026 22:42:27 GMT  
		Size: 121.0 MB (121016025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206cf29389588b7b19b55414eb210e1dd6f08621c5925cc97783e2512e2448b`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4139627acf1d2dfacd85fc36c6189af287834fafc74629ff2615296c058bf3da`  
		Last Modified: Fri, 16 Jan 2026 00:58:59 GMT  
		Size: 110.2 MB (110187099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e2efff092f53ee7789ee08cbb160b3b85b87524a06744e8e91cab9cf9ca171`  
		Last Modified: Fri, 16 Jan 2026 00:58:50 GMT  
		Size: 371.7 KB (371744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723794c7050a1b79f891d804f844d9e39317679cba5ca2031f687bca2592df7b`  
		Last Modified: Fri, 16 Jan 2026 00:58:50 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06850daf351b3a2227558f1f02fa276838ebc17e954b4895c983ca9efa734cbb`  
		Last Modified: Fri, 16 Jan 2026 00:58:54 GMT  
		Size: 28.1 MB (28063475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:88c7a9fb1d1e64d01df3cf05229a4b9c9e803860bcfa123bc4958b6720acfe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24600251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66db517cc6a7ebecdab82a2812cf460be1665864b80237f96fe73da203108045`

```dockerfile
```

-	Layers:
	-	`sha256:f0459c0d1e93f372bc00f9de10850f232cac56d0bdd746a4ac7b794e60636578`  
		Last Modified: Fri, 16 Jan 2026 02:19:06 GMT  
		Size: 24.6 MB (24583904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814a4b4c3e95a6478b13dfc14eb736461afc47c6f7070915ccc6b04b85762a95`  
		Last Modified: Fri, 16 Jan 2026 02:19:07 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d40086d2c2c1539b1a8eee67e35a0d1cd7104a23813a8bfc2098d7323f14581c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285260217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84f27d37d0626e98ab374aad076c6fc617065002dc2aa185faaf91f22385b9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:41 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:44:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:24 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0ffeb8abf9f69d9152d9ddf05b3d9bf0abd0da07487f555fca9183c211600`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 684.1 KB (684101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec456ec14866e45cf8752da07321782d64ae4e50014222025f952c73348f74`  
		Last Modified: Thu, 15 Jan 2026 22:45:03 GMT  
		Size: 6.8 MB (6761200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535702c99d332d44232b15396c6984e051db229f065200199d57a426a3e62760`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 94.3 KB (94254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41213d7b9319bb10daf024007dce1857fe9d550536f830b9d1d7646b1c9007`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 115.7 MB (115742618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee8712744d000fd48a2c882b325511146d3667fa87b4546ad01002eb3efcd4`  
		Last Modified: Thu, 15 Jan 2026 22:45:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fe46905465de7cdf7df0c256bc882a5c6f6bce00a12443b384513c5446e4ec`  
		Last Modified: Fri, 16 Jan 2026 01:02:10 GMT  
		Size: 105.6 MB (105595239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09271007bf03040fc00ce410c5798e4c25d9a95699468661d096af654f19d170`  
		Last Modified: Fri, 16 Jan 2026 01:02:03 GMT  
		Size: 371.7 KB (371749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53da40f77632a2aede7a153c740aa61a40ad8c211cd72001665ddd01a1f91a58`  
		Last Modified: Fri, 16 Jan 2026 01:02:03 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf3e21264a6cf710a3de027e72eb48ed241babcb1b8c1ba3d0457d768260a11`  
		Last Modified: Fri, 16 Jan 2026 01:02:06 GMT  
		Size: 27.1 MB (27144525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a488e8c6562c5bf506883d9347416992ef055c6c2882ab8215a6c78a25ca4f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24622649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cdb796ffdafb23da6b45ed06f8bf1fef5d600da824ab8d268824b74ad35f59`

```dockerfile
```

-	Layers:
	-	`sha256:42ea77cedb88eb06075335c1896ee3a19f0b13156db6a51af9f9153d82234249`  
		Last Modified: Fri, 16 Jan 2026 02:19:36 GMT  
		Size: 24.6 MB (24606165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cac50e00f17e0383ef1f9fe799d22b586da1fbc5372c1220ef1e3bcc7142dc9`  
		Last Modified: Fri, 16 Jan 2026 02:19:37 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:3b2031f3e7211aeda15e1a346dba08ca40d8c3eaed7f68649e50dbefd481c260
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:ccaa6f44bb6543305056958567a8ebba7ddf065b0f1a5fff08b3361205a4dd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158267923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f06769f43a6813b7f42ba251a46efbb2685c5f0fbf074c7e1d935c9238911f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:41:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fae7f48a46da951e313f18a6daf495d637bd45e1d4f7d040911c1f2ee7b972`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc1c27f9559dd6ff1cdbfe218890a4794f42a6099b771506e057d7764a7720`  
		Last Modified: Thu, 15 Jan 2026 22:42:11 GMT  
		Size: 6.7 MB (6747522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21f7fe8d5212d488b694908db57f4df8b1edd9165e7ef82d3b595cb236521`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 94.2 KB (94176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b77d824f0ae70e13124dcbd7bfd2d9fac9328ca8a3a90e3f5993a9b4afe030`  
		Last Modified: Thu, 15 Jan 2026 22:42:27 GMT  
		Size: 121.0 MB (121016025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206cf29389588b7b19b55414eb210e1dd6f08621c5925cc97783e2512e2448b`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:85b7e6cd34c91543e0f0ffcb7f8fa9f61f3b12feb6a692745d79f5b3ca18c10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18348040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e21f669779c98ec19bb21942417dd61ddef48f8dbbfadc4bea62294a961b7a3`

```dockerfile
```

-	Layers:
	-	`sha256:d7c40d424370efa0acc5aecc4219175171e6e03118b0a7d8b55ceedd852d5882`  
		Last Modified: Fri, 16 Jan 2026 02:19:21 GMT  
		Size: 18.3 MB (18333431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830fb208c958f36b2165a2897f06eab6e7d1c92c665b3cd56c4fbf3c97b0ad24`  
		Last Modified: Fri, 16 Jan 2026 02:19:22 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fad38bb0bc4e1350966b47502c707f6f61fc390a54596713a0f777249956d790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152146193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d8114399e27e481f4ca8cee2610b3271c3204d53b453244a025f9cf4758397`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:41 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:44:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0ffeb8abf9f69d9152d9ddf05b3d9bf0abd0da07487f555fca9183c211600`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 684.1 KB (684101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec456ec14866e45cf8752da07321782d64ae4e50014222025f952c73348f74`  
		Last Modified: Thu, 15 Jan 2026 22:45:03 GMT  
		Size: 6.8 MB (6761200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535702c99d332d44232b15396c6984e051db229f065200199d57a426a3e62760`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 94.3 KB (94254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41213d7b9319bb10daf024007dce1857fe9d550536f830b9d1d7646b1c9007`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 115.7 MB (115742618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee8712744d000fd48a2c882b325511146d3667fa87b4546ad01002eb3efcd4`  
		Last Modified: Thu, 15 Jan 2026 22:45:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:22f1afcce613dc8e7d6f964acb72a975b5fb8a8cbf9d4913257327ae7c2655e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18322171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe5d10b04fb69189179c45c43b71b7adff576ed6fc6b80262a27ab0ef1c69a5`

```dockerfile
```

-	Layers:
	-	`sha256:c3fe08ae49d307ea43de5ad84e7dc36726df01168a389a3744bd98c0f2597479`  
		Last Modified: Fri, 16 Jan 2026 02:19:44 GMT  
		Size: 18.3 MB (18307437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2214cbfdb1bb403257859a5c52d342af1acefab9e254a3ee9eacb419462ce31b`  
		Last Modified: Fri, 16 Jan 2026 02:19:45 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:3b2031f3e7211aeda15e1a346dba08ca40d8c3eaed7f68649e50dbefd481c260
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:ccaa6f44bb6543305056958567a8ebba7ddf065b0f1a5fff08b3361205a4dd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158267923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f06769f43a6813b7f42ba251a46efbb2685c5f0fbf074c7e1d935c9238911f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:36 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:41:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fae7f48a46da951e313f18a6daf495d637bd45e1d4f7d040911c1f2ee7b972`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc1c27f9559dd6ff1cdbfe218890a4794f42a6099b771506e057d7764a7720`  
		Last Modified: Thu, 15 Jan 2026 22:42:11 GMT  
		Size: 6.7 MB (6747522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21f7fe8d5212d488b694908db57f4df8b1edd9165e7ef82d3b595cb236521`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 94.2 KB (94176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b77d824f0ae70e13124dcbd7bfd2d9fac9328ca8a3a90e3f5993a9b4afe030`  
		Last Modified: Thu, 15 Jan 2026 22:42:27 GMT  
		Size: 121.0 MB (121016025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206cf29389588b7b19b55414eb210e1dd6f08621c5925cc97783e2512e2448b`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:85b7e6cd34c91543e0f0ffcb7f8fa9f61f3b12feb6a692745d79f5b3ca18c10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18348040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e21f669779c98ec19bb21942417dd61ddef48f8dbbfadc4bea62294a961b7a3`

```dockerfile
```

-	Layers:
	-	`sha256:d7c40d424370efa0acc5aecc4219175171e6e03118b0a7d8b55ceedd852d5882`  
		Last Modified: Fri, 16 Jan 2026 02:19:21 GMT  
		Size: 18.3 MB (18333431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:830fb208c958f36b2165a2897f06eab6e7d1c92c665b3cd56c4fbf3c97b0ad24`  
		Last Modified: Fri, 16 Jan 2026 02:19:22 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fad38bb0bc4e1350966b47502c707f6f61fc390a54596713a0f777249956d790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152146193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d8114399e27e481f4ca8cee2610b3271c3204d53b453244a025f9cf4758397`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:41 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:24 GMT
ENV ROS_DISTRO=kilted
# Thu, 15 Jan 2026 22:44:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0ffeb8abf9f69d9152d9ddf05b3d9bf0abd0da07487f555fca9183c211600`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 684.1 KB (684101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec456ec14866e45cf8752da07321782d64ae4e50014222025f952c73348f74`  
		Last Modified: Thu, 15 Jan 2026 22:45:03 GMT  
		Size: 6.8 MB (6761200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535702c99d332d44232b15396c6984e051db229f065200199d57a426a3e62760`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 94.3 KB (94254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41213d7b9319bb10daf024007dce1857fe9d550536f830b9d1d7646b1c9007`  
		Last Modified: Thu, 15 Jan 2026 22:45:16 GMT  
		Size: 115.7 MB (115742618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee8712744d000fd48a2c882b325511146d3667fa87b4546ad01002eb3efcd4`  
		Last Modified: Thu, 15 Jan 2026 22:45:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:22f1afcce613dc8e7d6f964acb72a975b5fb8a8cbf9d4913257327ae7c2655e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18322171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe5d10b04fb69189179c45c43b71b7adff576ed6fc6b80262a27ab0ef1c69a5`

```dockerfile
```

-	Layers:
	-	`sha256:c3fe08ae49d307ea43de5ad84e7dc36726df01168a389a3744bd98c0f2597479`  
		Last Modified: Fri, 16 Jan 2026 02:19:44 GMT  
		Size: 18.3 MB (18307437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2214cbfdb1bb403257859a5c52d342af1acefab9e254a3ee9eacb419462ce31b`  
		Last Modified: Fri, 16 Jan 2026 02:19:45 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:af9454f13d342c58bb9f3364424e3e7026184e59a47de75f915d241cb7ec6666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:f3dba6618d45181f7a68cb3f2b9a9da9d52c3315d805fb99687123a80eff10df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296053963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fbe811330cd2f7e3c52c4a6d4369c0581f7679d8b5d48c8cd6e5f20c017302`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:40:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:05 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:05 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:57:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:57:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:57:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:57:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d97c22d0e00b55e0e76a4395fe1b24e90d3b47b63ba12fa85f4711cb8358053`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 684.0 KB (683988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a7fb7868e491005250578970a3f67cb03fc46599910002a9d21bfb3dc79d2`  
		Last Modified: Thu, 15 Jan 2026 22:41:39 GMT  
		Size: 6.7 MB (6747519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e5ddd305d765e1f55231776d7dff9595c9b0ea45bd0343566a5ad40f68dc1`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 94.2 KB (94189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75495656f22ab4b88f855531eff7ac03bbc6c08aeac9b335721f9a63b952eaeb`  
		Last Modified: Thu, 15 Jan 2026 22:41:48 GMT  
		Size: 120.2 MB (120220982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23510d5a445e9cf17fa443c4c1c91b8f41ddab3939641059429f56d90b302b`  
		Last Modified: Thu, 15 Jan 2026 22:41:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a2d5b61aaf7e2e0547a70431b18a46188a6e920efa30a196e73b6b9abd45f4`  
		Last Modified: Fri, 16 Jan 2026 00:58:27 GMT  
		Size: 110.2 MB (110183100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8758dc4c4511d77e8139294b47787d28096781d5b2ef8f4caf1144e9fbe6f561`  
		Last Modified: Fri, 16 Jan 2026 00:58:16 GMT  
		Size: 390.3 KB (390326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda5a314ef599a1d2f9db599331d5bf2e05dc8c9b658de57954f6a5f24d246ad`  
		Last Modified: Fri, 16 Jan 2026 00:58:16 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673747666502f74a4c28e3b441004032e9d058d9b70a031ca3606ea0644f87b3`  
		Last Modified: Fri, 16 Jan 2026 00:58:21 GMT  
		Size: 28.0 MB (28005148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:489faad951607a6a8c266763d0b39d81613d6c0d08896cb14c2cad83a06b29de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24561461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44151c680004f3aef9280bfa546fa843c046063206bb85940671f664c80d210`

```dockerfile
```

-	Layers:
	-	`sha256:efcf6f164767bef316bca6384f77c11bf81a593e100ed0155c2e78cbecd59ea9`  
		Last Modified: Fri, 16 Jan 2026 02:18:41 GMT  
		Size: 24.5 MB (24544841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f8acd13b1ba88981339bf29e7b8665c281a468711d5d8e259e6fd22a3713d0`  
		Last Modified: Fri, 16 Jan 2026 02:18:42 GMT  
		Size: 16.6 KB (16620 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93482033b6cf937dcc1e404218b02213b008f7036e4aa2add797dbef8b63f6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284482132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98deedb66635f35717a5c1b6b33bf4b90b9b61668da1541760a28bc494f25da5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:01 GMT
ENV ROS_DISTRO=jazzy
# Thu, 15 Jan 2026 22:44:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:00:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:00:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:00:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:00:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcffa1213fa57586fd8eaccb12bf58db71567acfe6beb2604ce14a7fce49350`  
		Last Modified: Thu, 15 Jan 2026 22:44:40 GMT  
		Size: 684.1 KB (684123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d2c4ddc36db2e4f53f41ed5aae6e0d424f34360990c6490205b5a1a3dd1d`  
		Last Modified: Thu, 15 Jan 2026 22:44:42 GMT  
		Size: 6.8 MB (6761160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2a4235e2d4774a07bc75a44ba91842de78e74f47130b4f9ae6772c1b3ef31`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 94.3 KB (94272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963243806f290c98f3cd72253b9a344178c64bd19c4076a4d0fc0fe366cb4d75`  
		Last Modified: Thu, 15 Jan 2026 22:44:57 GMT  
		Size: 115.0 MB (114993652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99dc06e4d3709628f00f7c925bb0aaf1e36c23f5295a0ce0a3bb297c1265d1`  
		Last Modified: Thu, 15 Jan 2026 22:44:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ded0d19c79a23e1eb3c9c493b71bc3aaf47b095d79cdf0da647eb55203289a`  
		Last Modified: Fri, 16 Jan 2026 01:01:42 GMT  
		Size: 105.6 MB (105592399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a29344c731ff62579c4b41928a004f7229c263244eb3cf2e9cfa02ee6a82911`  
		Last Modified: Fri, 16 Jan 2026 01:01:32 GMT  
		Size: 390.3 KB (390338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdb3e21e95af01abb665679711c101cb346091241dab45013bb305b86c3f28`  
		Last Modified: Fri, 16 Jan 2026 01:01:32 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a215247acb520778e621dccad3a665d57a8e8bd9d18e532c921fde7b876b7e46`  
		Last Modified: Fri, 16 Jan 2026 01:01:35 GMT  
		Size: 27.1 MB (27099655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:ba47a82a66bf9e3371eec41b3ec9dfb28946205921edc356aa608730d92d45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5ec4280e4f026f58488178410f21315f441a865dd169e428cc9b45d79f1262`

```dockerfile
```

-	Layers:
	-	`sha256:1fe22c8f0fdab48afe6837bd75771d82729a93a29acc734e78affd64a685e1ec`  
		Last Modified: Fri, 16 Jan 2026 02:19:11 GMT  
		Size: 24.6 MB (24567114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf5e37218976a68acdbf1ed803bbb3f4e017f73018f64b38c22700e39db988f`  
		Last Modified: Fri, 16 Jan 2026 02:19:12 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:e9868b11c447ebe7d96de318281652fbde5f881a6d918037363772cb216ebb45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:0358858d92326a489fc804735ed5ca3234bbac05b9287990d76c46a259f52041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324895138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89545a1401c5c5dd27da58db684417a8589ac75a6930ed52790d743fd3d19294`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:41:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:59 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:58:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:58:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:58:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967b3bea28a190de2abdf7c583b9e2b113486381b15ce00e1bb91c9c58c7026`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 684.0 KB (684002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e126b2b2995cf775c0d4c7132e48cc59964feb7907083276ec56e4887393982`  
		Last Modified: Thu, 15 Jan 2026 22:42:41 GMT  
		Size: 6.7 MB (6747551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18b8569b1a8cc779459c80d4f6fe5de9295d36844ee1136e7c0f679a38d436`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 94.2 KB (94195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81824252ed26645e4cda94990da14222e41928058bbb7b3049257c78f69ab5ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:56 GMT  
		Size: 149.3 MB (149258662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38af2ca8fd7a12110b28f79aec36ece2ed6d1deb02337ced830f83efc91a62c`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f49599d4013baaab168de3657e56f1a064b0c2b3905abef079ce53580b55fc`  
		Last Modified: Fri, 16 Jan 2026 00:59:55 GMT  
		Size: 110.2 MB (110187905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803c8199c566f7183c9af620273eaa14079f91449307d2f85488be3e5b8e31c`  
		Last Modified: Fri, 16 Jan 2026 00:59:47 GMT  
		Size: 364.1 KB (364083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6037797cc4818e4cb6c652d9119165eb136a640dc847c7a40b2a255d82140d78`  
		Last Modified: Fri, 16 Jan 2026 00:59:47 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6e075818bb92799b42233693868bc52253c0460cd5c0e34ea859c07eb2f032`  
		Last Modified: Fri, 16 Jan 2026 00:59:50 GMT  
		Size: 27.8 MB (27830020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:0909ce67644b3bab13463a71aa6f9e981e2e187022e60ef9b8cbaaad03935a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25699011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b916b8e46b524b26de20e043f4e2fed111ddefdfe51bc3db56e9dac335205b78`

```dockerfile
```

-	Layers:
	-	`sha256:9ecceda629293cd8071874563df336cee41e97acbb6142fd065e37ac09144a77`  
		Last Modified: Fri, 16 Jan 2026 02:19:34 GMT  
		Size: 25.7 MB (25682647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3d376c3c92ce9b464afe89b4cfb7c629da8bf85fca826b6be3f88a5b7f6e93`  
		Last Modified: Fri, 16 Jan 2026 02:19:35 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:81c71294829ca2f68c2f5dccb482e2ad86989f10e297a710c8e98d5408bce385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312875893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8292860f47d9ade8e2fdc86cb4b23a6c2cfd586e6d0dda17874d9297a0ebde02`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:58 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:42 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:01:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7bce41f2844e04d79191a3a4c295cceebd907050fdd985904094c9ba0d985`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e13d723b56be5d113451d0159f2a683e7ddac92cc7b441e356a56355ff611f`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 6.8 MB (6761189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897c68b882e54cfb023792aa6fe744ee9e750aa8568087884c4fb4ab09101ad`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 94.3 KB (94257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36529be7c1d16a05a9345b5d7fe602935226342c7f00f326043ca6356711d8b3`  
		Last Modified: Thu, 15 Jan 2026 22:45:37 GMT  
		Size: 143.6 MB (143598736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca3447fca213716c45fecc334db425ccb842ed9d7e99dadaea901c500b2d79`  
		Last Modified: Thu, 15 Jan 2026 22:45:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d0315754ad467c0f84a51bcca420f9d00efc89dd6b14a66ca9b67d15cc1515`  
		Last Modified: Fri, 16 Jan 2026 01:02:49 GMT  
		Size: 105.6 MB (105595993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d98324865d792dbec7fdb6bca34a68a242ff693752ea91e79792218d79eb584`  
		Last Modified: Fri, 16 Jan 2026 01:02:42 GMT  
		Size: 364.1 KB (364075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90a40e53a65c744875af2e18cbb0eaa9054b3b722a5cbb8ead531fbd150be6f`  
		Last Modified: Fri, 16 Jan 2026 01:02:42 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63502b76303910712c34ce860754310acbc8ecacdb2103d23eda093422cc82fe`  
		Last Modified: Fri, 16 Jan 2026 01:02:44 GMT  
		Size: 26.9 MB (26911011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:a1b5bd7b8e9c69f87b63f3bc6027af2740dcb73babc868272daac09819f37b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25721607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e66317b9ddc7c9918532d1125d277207524e7577c41b1d90645ad7f420af9b`

```dockerfile
```

-	Layers:
	-	`sha256:20a29c1b578495a9aa8a2c361c2c383a0002adb9930920daf6b6f9a6fafeb7f8`  
		Last Modified: Fri, 16 Jan 2026 02:20:07 GMT  
		Size: 25.7 MB (25705105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa5771aa61e4f4274fac2fc7d47a1d3a13b759c62a1d445d2b443c06b14acf`  
		Last Modified: Fri, 16 Jan 2026 02:20:08 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:e15e22a7b12d83bd8e74a87010080adb9c697187a4e7919b3f1107b0dec458f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:be9194c01daebb513760ea0807f691b37f62841a4a5be177ec3222524e330fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1109207168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b2635343eeff54fff474edeafc2f1dadfc528f4d028fd9c95b354832a3130`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Tue, 13 Jan 2026 01:30:40 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Tue, 13 Jan 2026 01:30:38 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Tue, 13 Jan 2026 01:30:37 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Tue, 13 Jan 2026 01:30:38 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Tue, 13 Jan 2026 01:30:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Tue, 13 Jan 2026 01:30:37 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Tue, 13 Jan 2026 01:30:10 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Tue, 13 Jan 2026 01:30:10 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Tue, 13 Jan 2026 01:30:18 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9384e3c026a30291bf2ecbebae43f7737e26f758c5e65826a7d7988f7ac77`  
		Last Modified: Wed, 14 Jan 2026 21:50:52 GMT  
		Size: 784.5 MB (784531548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:8ca951d20e89c222764cbcb0b4331902ba1c3b085a4bf2f39dd6365614ed4b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61913258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2947e13ed1bac2da29d09b83220014ae1b8a2ededb2169110dc3fd7a4c1db3`

```dockerfile
```

-	Layers:
	-	`sha256:52578280739f10315a8e65bdc4774e09575922556d6a284cdd6e14c9d8b27acf`  
		Last Modified: Fri, 14 Nov 2025 01:21:25 GMT  
		Size: 61.9 MB (61903897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf96a68f2d59ab1e7f9f8918eddc4c5eac8939a3bf23497a75c3746d4467f6f`  
		Last Modified: Fri, 14 Nov 2025 01:21:22 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:74c1149c7a5c1bef22da018fae466515e000a344da879394d76676e2c69b76ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1007216187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bda908390a724e838225ade5c6d650df196f05eb7cf27a5828bb628444179b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Tue, 13 Jan 2026 05:56:39 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Tue, 13 Jan 2026 05:57:08 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Tue, 13 Jan 2026 05:56:48 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Tue, 13 Jan 2026 09:29:07 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Tue, 13 Jan 2026 05:57:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Tue, 13 Jan 2026 09:29:05 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Tue, 13 Jan 2026 05:57:23 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Tue, 13 Jan 2026 05:57:30 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Tue, 13 Jan 2026 09:29:02 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ce4a548a9e278afac869dc062059bbbf762381ef3136c4835c8f663eddb426`  
		Last Modified: Wed, 14 Jan 2026 04:02:04 GMT  
		Size: 694.6 MB (694565732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:ed822594c7d69eb4c75dabd13d741dd7cc5b5eb3949da7e742836660fcbcccf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61844060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925f4f20ea9d6203be5ef243fa96c9321d6ce00d17aa52eecdd9449ed120bd00`

```dockerfile
```

-	Layers:
	-	`sha256:a42fa6f66f50eaaf261bb413c076f2545dfc6ff742ef782c9f519d25ba3e9d10`  
		Last Modified: Wed, 14 Jan 2026 04:01:59 GMT  
		Size: 61.8 MB (61834619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ed22bcee0de118946955cada52b3078043306650cacd0d92f09dd9b709e64f`  
		Last Modified: Wed, 14 Jan 2026 04:01:39 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:e15e22a7b12d83bd8e74a87010080adb9c697187a4e7919b3f1107b0dec458f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:be9194c01daebb513760ea0807f691b37f62841a4a5be177ec3222524e330fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1109207168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2b2635343eeff54fff474edeafc2f1dadfc528f4d028fd9c95b354832a3130`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Tue, 13 Jan 2026 01:30:40 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Tue, 13 Jan 2026 01:30:38 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Tue, 13 Jan 2026 01:30:37 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Tue, 13 Jan 2026 01:30:38 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Tue, 13 Jan 2026 01:30:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Tue, 13 Jan 2026 01:30:37 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Tue, 13 Jan 2026 01:30:10 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Tue, 13 Jan 2026 01:30:10 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Tue, 13 Jan 2026 01:30:18 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9384e3c026a30291bf2ecbebae43f7737e26f758c5e65826a7d7988f7ac77`  
		Last Modified: Wed, 14 Jan 2026 21:50:52 GMT  
		Size: 784.5 MB (784531548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8ca951d20e89c222764cbcb0b4331902ba1c3b085a4bf2f39dd6365614ed4b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61913258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2947e13ed1bac2da29d09b83220014ae1b8a2ededb2169110dc3fd7a4c1db3`

```dockerfile
```

-	Layers:
	-	`sha256:52578280739f10315a8e65bdc4774e09575922556d6a284cdd6e14c9d8b27acf`  
		Last Modified: Fri, 14 Nov 2025 01:21:25 GMT  
		Size: 61.9 MB (61903897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf96a68f2d59ab1e7f9f8918eddc4c5eac8939a3bf23497a75c3746d4467f6f`  
		Last Modified: Fri, 14 Nov 2025 01:21:22 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:74c1149c7a5c1bef22da018fae466515e000a344da879394d76676e2c69b76ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1007216187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bda908390a724e838225ade5c6d650df196f05eb7cf27a5828bb628444179b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:35:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Tue, 13 Jan 2026 05:56:39 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Tue, 13 Jan 2026 05:57:08 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Tue, 13 Jan 2026 05:56:48 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Tue, 13 Jan 2026 09:29:07 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Tue, 13 Jan 2026 05:57:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Tue, 13 Jan 2026 09:29:05 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Tue, 13 Jan 2026 05:57:23 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Tue, 13 Jan 2026 05:57:30 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Tue, 13 Jan 2026 09:29:02 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ce4a548a9e278afac869dc062059bbbf762381ef3136c4835c8f663eddb426`  
		Last Modified: Wed, 14 Jan 2026 04:02:04 GMT  
		Size: 694.6 MB (694565732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ed822594c7d69eb4c75dabd13d741dd7cc5b5eb3949da7e742836660fcbcccf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61844060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925f4f20ea9d6203be5ef243fa96c9321d6ce00d17aa52eecdd9449ed120bd00`

```dockerfile
```

-	Layers:
	-	`sha256:a42fa6f66f50eaaf261bb413c076f2545dfc6ff742ef782c9f519d25ba3e9d10`  
		Last Modified: Wed, 14 Jan 2026 04:01:59 GMT  
		Size: 61.8 MB (61834619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ed22bcee0de118946955cada52b3078043306650cacd0d92f09dd9b709e64f`  
		Last Modified: Wed, 14 Jan 2026 04:01:39 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:e9868b11c447ebe7d96de318281652fbde5f881a6d918037363772cb216ebb45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0358858d92326a489fc804735ed5ca3234bbac05b9287990d76c46a259f52041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324895138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89545a1401c5c5dd27da58db684417a8589ac75a6930ed52790d743fd3d19294`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:41:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:59 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:58:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:58:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:58:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967b3bea28a190de2abdf7c583b9e2b113486381b15ce00e1bb91c9c58c7026`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 684.0 KB (684002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e126b2b2995cf775c0d4c7132e48cc59964feb7907083276ec56e4887393982`  
		Last Modified: Thu, 15 Jan 2026 22:42:41 GMT  
		Size: 6.7 MB (6747551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18b8569b1a8cc779459c80d4f6fe5de9295d36844ee1136e7c0f679a38d436`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 94.2 KB (94195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81824252ed26645e4cda94990da14222e41928058bbb7b3049257c78f69ab5ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:56 GMT  
		Size: 149.3 MB (149258662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38af2ca8fd7a12110b28f79aec36ece2ed6d1deb02337ced830f83efc91a62c`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f49599d4013baaab168de3657e56f1a064b0c2b3905abef079ce53580b55fc`  
		Last Modified: Fri, 16 Jan 2026 00:59:55 GMT  
		Size: 110.2 MB (110187905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803c8199c566f7183c9af620273eaa14079f91449307d2f85488be3e5b8e31c`  
		Last Modified: Fri, 16 Jan 2026 00:59:47 GMT  
		Size: 364.1 KB (364083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6037797cc4818e4cb6c652d9119165eb136a640dc847c7a40b2a255d82140d78`  
		Last Modified: Fri, 16 Jan 2026 00:59:47 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6e075818bb92799b42233693868bc52253c0460cd5c0e34ea859c07eb2f032`  
		Last Modified: Fri, 16 Jan 2026 00:59:50 GMT  
		Size: 27.8 MB (27830020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0909ce67644b3bab13463a71aa6f9e981e2e187022e60ef9b8cbaaad03935a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25699011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b916b8e46b524b26de20e043f4e2fed111ddefdfe51bc3db56e9dac335205b78`

```dockerfile
```

-	Layers:
	-	`sha256:9ecceda629293cd8071874563df336cee41e97acbb6142fd065e37ac09144a77`  
		Last Modified: Fri, 16 Jan 2026 02:19:34 GMT  
		Size: 25.7 MB (25682647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3d376c3c92ce9b464afe89b4cfb7c629da8bf85fca826b6be3f88a5b7f6e93`  
		Last Modified: Fri, 16 Jan 2026 02:19:35 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:81c71294829ca2f68c2f5dccb482e2ad86989f10e297a710c8e98d5408bce385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312875893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8292860f47d9ade8e2fdc86cb4b23a6c2cfd586e6d0dda17874d9297a0ebde02`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:58 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:42 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:01:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7bce41f2844e04d79191a3a4c295cceebd907050fdd985904094c9ba0d985`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e13d723b56be5d113451d0159f2a683e7ddac92cc7b441e356a56355ff611f`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 6.8 MB (6761189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897c68b882e54cfb023792aa6fe744ee9e750aa8568087884c4fb4ab09101ad`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 94.3 KB (94257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36529be7c1d16a05a9345b5d7fe602935226342c7f00f326043ca6356711d8b3`  
		Last Modified: Thu, 15 Jan 2026 22:45:37 GMT  
		Size: 143.6 MB (143598736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca3447fca213716c45fecc334db425ccb842ed9d7e99dadaea901c500b2d79`  
		Last Modified: Thu, 15 Jan 2026 22:45:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d0315754ad467c0f84a51bcca420f9d00efc89dd6b14a66ca9b67d15cc1515`  
		Last Modified: Fri, 16 Jan 2026 01:02:49 GMT  
		Size: 105.6 MB (105595993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d98324865d792dbec7fdb6bca34a68a242ff693752ea91e79792218d79eb584`  
		Last Modified: Fri, 16 Jan 2026 01:02:42 GMT  
		Size: 364.1 KB (364075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90a40e53a65c744875af2e18cbb0eaa9054b3b722a5cbb8ead531fbd150be6f`  
		Last Modified: Fri, 16 Jan 2026 01:02:42 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63502b76303910712c34ce860754310acbc8ecacdb2103d23eda093422cc82fe`  
		Last Modified: Fri, 16 Jan 2026 01:02:44 GMT  
		Size: 26.9 MB (26911011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:a1b5bd7b8e9c69f87b63f3bc6027af2740dcb73babc868272daac09819f37b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25721607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e66317b9ddc7c9918532d1125d277207524e7577c41b1d90645ad7f420af9b`

```dockerfile
```

-	Layers:
	-	`sha256:20a29c1b578495a9aa8a2c361c2c383a0002adb9930920daf6b6f9a6fafeb7f8`  
		Last Modified: Fri, 16 Jan 2026 02:20:07 GMT  
		Size: 25.7 MB (25705105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa5771aa61e4f4274fac2fc7d47a1d3a13b759c62a1d445d2b443c06b14acf`  
		Last Modified: Fri, 16 Jan 2026 02:20:08 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:e9868b11c447ebe7d96de318281652fbde5f881a6d918037363772cb216ebb45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:0358858d92326a489fc804735ed5ca3234bbac05b9287990d76c46a259f52041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324895138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89545a1401c5c5dd27da58db684417a8589ac75a6930ed52790d743fd3d19294`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:41:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:59 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 00:58:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:58:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 00:58:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 00:58:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967b3bea28a190de2abdf7c583b9e2b113486381b15ce00e1bb91c9c58c7026`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 684.0 KB (684002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e126b2b2995cf775c0d4c7132e48cc59964feb7907083276ec56e4887393982`  
		Last Modified: Thu, 15 Jan 2026 22:42:41 GMT  
		Size: 6.7 MB (6747551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18b8569b1a8cc779459c80d4f6fe5de9295d36844ee1136e7c0f679a38d436`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 94.2 KB (94195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81824252ed26645e4cda94990da14222e41928058bbb7b3049257c78f69ab5ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:56 GMT  
		Size: 149.3 MB (149258662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38af2ca8fd7a12110b28f79aec36ece2ed6d1deb02337ced830f83efc91a62c`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f49599d4013baaab168de3657e56f1a064b0c2b3905abef079ce53580b55fc`  
		Last Modified: Fri, 16 Jan 2026 00:59:55 GMT  
		Size: 110.2 MB (110187905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803c8199c566f7183c9af620273eaa14079f91449307d2f85488be3e5b8e31c`  
		Last Modified: Fri, 16 Jan 2026 00:59:47 GMT  
		Size: 364.1 KB (364083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6037797cc4818e4cb6c652d9119165eb136a640dc847c7a40b2a255d82140d78`  
		Last Modified: Fri, 16 Jan 2026 00:59:47 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6e075818bb92799b42233693868bc52253c0460cd5c0e34ea859c07eb2f032`  
		Last Modified: Fri, 16 Jan 2026 00:59:50 GMT  
		Size: 27.8 MB (27830020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0909ce67644b3bab13463a71aa6f9e981e2e187022e60ef9b8cbaaad03935a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25699011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b916b8e46b524b26de20e043f4e2fed111ddefdfe51bc3db56e9dac335205b78`

```dockerfile
```

-	Layers:
	-	`sha256:9ecceda629293cd8071874563df336cee41e97acbb6142fd065e37ac09144a77`  
		Last Modified: Fri, 16 Jan 2026 02:19:34 GMT  
		Size: 25.7 MB (25682647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3d376c3c92ce9b464afe89b4cfb7c629da8bf85fca826b6be3f88a5b7f6e93`  
		Last Modified: Fri, 16 Jan 2026 02:19:35 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:81c71294829ca2f68c2f5dccb482e2ad86989f10e297a710c8e98d5408bce385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312875893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8292860f47d9ade8e2fdc86cb4b23a6c2cfd586e6d0dda17874d9297a0ebde02`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:58 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:42 GMT
CMD ["bash"]
# Fri, 16 Jan 2026 01:01:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:01:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 16 Jan 2026 01:01:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 16 Jan 2026 01:01:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7bce41f2844e04d79191a3a4c295cceebd907050fdd985904094c9ba0d985`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e13d723b56be5d113451d0159f2a683e7ddac92cc7b441e356a56355ff611f`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 6.8 MB (6761189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897c68b882e54cfb023792aa6fe744ee9e750aa8568087884c4fb4ab09101ad`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 94.3 KB (94257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36529be7c1d16a05a9345b5d7fe602935226342c7f00f326043ca6356711d8b3`  
		Last Modified: Thu, 15 Jan 2026 22:45:37 GMT  
		Size: 143.6 MB (143598736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca3447fca213716c45fecc334db425ccb842ed9d7e99dadaea901c500b2d79`  
		Last Modified: Thu, 15 Jan 2026 22:45:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d0315754ad467c0f84a51bcca420f9d00efc89dd6b14a66ca9b67d15cc1515`  
		Last Modified: Fri, 16 Jan 2026 01:02:49 GMT  
		Size: 105.6 MB (105595993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d98324865d792dbec7fdb6bca34a68a242ff693752ea91e79792218d79eb584`  
		Last Modified: Fri, 16 Jan 2026 01:02:42 GMT  
		Size: 364.1 KB (364075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90a40e53a65c744875af2e18cbb0eaa9054b3b722a5cbb8ead531fbd150be6f`  
		Last Modified: Fri, 16 Jan 2026 01:02:42 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63502b76303910712c34ce860754310acbc8ecacdb2103d23eda093422cc82fe`  
		Last Modified: Fri, 16 Jan 2026 01:02:44 GMT  
		Size: 26.9 MB (26911011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a1b5bd7b8e9c69f87b63f3bc6027af2740dcb73babc868272daac09819f37b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25721607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e66317b9ddc7c9918532d1125d277207524e7577c41b1d90645ad7f420af9b`

```dockerfile
```

-	Layers:
	-	`sha256:20a29c1b578495a9aa8a2c361c2c383a0002adb9930920daf6b6f9a6fafeb7f8`  
		Last Modified: Fri, 16 Jan 2026 02:20:07 GMT  
		Size: 25.7 MB (25705105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa5771aa61e4f4274fac2fc7d47a1d3a13b759c62a1d445d2b443c06b14acf`  
		Last Modified: Fri, 16 Jan 2026 02:20:08 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:c450e30428d9dffbb52e82d77fa57f08fd2b0cbd1721d85426f0346dd6170779
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:4414971f5ba776be6949205af31c175460c08a41fe5e6aa69086e636ee56e008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186510618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f565248a907b92a0f6c34420b8df6821862f65fd82ab4405571a012c39529`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:41:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967b3bea28a190de2abdf7c583b9e2b113486381b15ce00e1bb91c9c58c7026`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 684.0 KB (684002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e126b2b2995cf775c0d4c7132e48cc59964feb7907083276ec56e4887393982`  
		Last Modified: Thu, 15 Jan 2026 22:42:41 GMT  
		Size: 6.7 MB (6747551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18b8569b1a8cc779459c80d4f6fe5de9295d36844ee1136e7c0f679a38d436`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 94.2 KB (94195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81824252ed26645e4cda94990da14222e41928058bbb7b3049257c78f69ab5ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:56 GMT  
		Size: 149.3 MB (149258662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38af2ca8fd7a12110b28f79aec36ece2ed6d1deb02337ced830f83efc91a62c`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:b5c81055704fce3b7ee80b28a937e91c0ed9242e28ec80dca2261cde40d08431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19476848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a542861638fd5e676f82fa7b504c53dcf9acd0bba27a875dbf6afa99cb3ed97`

```dockerfile
```

-	Layers:
	-	`sha256:f1dfcc508e0530ba986bad5d0dfa8b3eacf5b1fdd09cbe2c0c993723a4f1d6ee`  
		Last Modified: Fri, 16 Jan 2026 02:19:47 GMT  
		Size: 19.5 MB (19462226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb6aca053d64d959a9bfb9a9023c16453c90588ee55d26ae9f46a43e5ce2d71`  
		Last Modified: Fri, 16 Jan 2026 02:19:48 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3bdb6c79e51eeb3cd62a34f7638349f2e3e7506be37296da98f13627cb347cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180002320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029ad93554f7b9323204a37820ef6a7dbab75033c4de7285a53a0deff6d47ca7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:58 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7bce41f2844e04d79191a3a4c295cceebd907050fdd985904094c9ba0d985`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e13d723b56be5d113451d0159f2a683e7ddac92cc7b441e356a56355ff611f`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 6.8 MB (6761189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897c68b882e54cfb023792aa6fe744ee9e750aa8568087884c4fb4ab09101ad`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 94.3 KB (94257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36529be7c1d16a05a9345b5d7fe602935226342c7f00f326043ca6356711d8b3`  
		Last Modified: Thu, 15 Jan 2026 22:45:37 GMT  
		Size: 143.6 MB (143598736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca3447fca213716c45fecc334db425ccb842ed9d7e99dadaea901c500b2d79`  
		Last Modified: Thu, 15 Jan 2026 22:45:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:3726244eac85e63f8332f9aa5f98da0985cf301242acb7ce7510418098691967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9afb3630348f57d5e7a27b2c5680abcccb7cf1d3e836ccd3383de79c8ffc04`

```dockerfile
```

-	Layers:
	-	`sha256:5826054e3a58ccce8bdae4e8589aa61bb8718823c53f76cb2918cd81cae9bb7b`  
		Last Modified: Fri, 16 Jan 2026 02:20:11 GMT  
		Size: 19.4 MB (19436430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa80eef061cda18f04b7734dd969bc324d502fd5f74d136f2c435ce0d487bb8`  
		Last Modified: Fri, 16 Jan 2026 02:20:12 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:c450e30428d9dffbb52e82d77fa57f08fd2b0cbd1721d85426f0346dd6170779
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:4414971f5ba776be6949205af31c175460c08a41fe5e6aa69086e636ee56e008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186510618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f565248a907b92a0f6c34420b8df6821862f65fd82ab4405571a012c39529`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:40:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:41:59 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:41:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:41:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:41:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967b3bea28a190de2abdf7c583b9e2b113486381b15ce00e1bb91c9c58c7026`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 684.0 KB (684002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e126b2b2995cf775c0d4c7132e48cc59964feb7907083276ec56e4887393982`  
		Last Modified: Thu, 15 Jan 2026 22:42:41 GMT  
		Size: 6.7 MB (6747551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18b8569b1a8cc779459c80d4f6fe5de9295d36844ee1136e7c0f679a38d436`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 94.2 KB (94195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81824252ed26645e4cda94990da14222e41928058bbb7b3049257c78f69ab5ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:56 GMT  
		Size: 149.3 MB (149258662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38af2ca8fd7a12110b28f79aec36ece2ed6d1deb02337ced830f83efc91a62c`  
		Last Modified: Thu, 15 Jan 2026 22:42:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b5c81055704fce3b7ee80b28a937e91c0ed9242e28ec80dca2261cde40d08431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19476848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a542861638fd5e676f82fa7b504c53dcf9acd0bba27a875dbf6afa99cb3ed97`

```dockerfile
```

-	Layers:
	-	`sha256:f1dfcc508e0530ba986bad5d0dfa8b3eacf5b1fdd09cbe2c0c993723a4f1d6ee`  
		Last Modified: Fri, 16 Jan 2026 02:19:47 GMT  
		Size: 19.5 MB (19462226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb6aca053d64d959a9bfb9a9023c16453c90588ee55d26ae9f46a43e5ce2d71`  
		Last Modified: Fri, 16 Jan 2026 02:19:48 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3bdb6c79e51eeb3cd62a34f7638349f2e3e7506be37296da98f13627cb347cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180002320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029ad93554f7b9323204a37820ef6a7dbab75033c4de7285a53a0deff6d47ca7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:43:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:58 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 15 Jan 2026 22:44:42 GMT
ENV ROS_DISTRO=rolling
# Thu, 15 Jan 2026 22:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:44:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 15 Jan 2026 22:44:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7bce41f2844e04d79191a3a4c295cceebd907050fdd985904094c9ba0d985`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e13d723b56be5d113451d0159f2a683e7ddac92cc7b441e356a56355ff611f`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 6.8 MB (6761189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897c68b882e54cfb023792aa6fe744ee9e750aa8568087884c4fb4ab09101ad`  
		Last Modified: Thu, 15 Jan 2026 22:45:25 GMT  
		Size: 94.3 KB (94257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36529be7c1d16a05a9345b5d7fe602935226342c7f00f326043ca6356711d8b3`  
		Last Modified: Thu, 15 Jan 2026 22:45:37 GMT  
		Size: 143.6 MB (143598736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ca3447fca213716c45fecc334db425ccb842ed9d7e99dadaea901c500b2d79`  
		Last Modified: Thu, 15 Jan 2026 22:45:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:3726244eac85e63f8332f9aa5f98da0985cf301242acb7ce7510418098691967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19451177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9afb3630348f57d5e7a27b2c5680abcccb7cf1d3e836ccd3383de79c8ffc04`

```dockerfile
```

-	Layers:
	-	`sha256:5826054e3a58ccce8bdae4e8589aa61bb8718823c53f76cb2918cd81cae9bb7b`  
		Last Modified: Fri, 16 Jan 2026 02:20:11 GMT  
		Size: 19.4 MB (19436430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa80eef061cda18f04b7734dd969bc324d502fd5f74d136f2c435ce0d487bb8`  
		Last Modified: Fri, 16 Jan 2026 02:20:12 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json
