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
-	[`ros:lyrical`](#roslyrical)
-	[`ros:lyrical-perception`](#roslyrical-perception)
-	[`ros:lyrical-perception-resolute`](#roslyrical-perception-resolute)
-	[`ros:lyrical-ros-base`](#roslyrical-ros-base)
-	[`ros:lyrical-ros-base-resolute`](#roslyrical-ros-base-resolute)
-	[`ros:lyrical-ros-core`](#roslyrical-ros-core)
-	[`ros:lyrical-ros-core-resolute`](#roslyrical-ros-core-resolute)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:5417e56962ff6e15d4cf9b2f78a71a78f3901f47cd78696b575b7eecdb54eb78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:8be79640caf3a89679d80c7666e759816cf59822521b092a5807ea8683bca366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263809499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151f70450bceb3669d183b2cc1ab203055eb68ffda3846794da043dcfb705a93`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:38 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:12 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:47:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:47:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2f449b78b8d36897aea1040c6dd78e2b773973b294be524f49e165bfbe125`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 1.2 MB (1215641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac297fbc77e6a50d3a6d12f6e9262ec93242659e840df00ae124230b06fbac9`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 6.0 MB (5994928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930c26f75b5fbc2a66379d9609e3c60712d47fd16ce99fbc72dd04ee8393370`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 97.3 KB (97321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef0c9426369b52a088411a845380681810dac51295fcd84b599778327158e`  
		Last Modified: Fri, 15 May 2026 21:21:41 GMT  
		Size: 104.9 MB (104865299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fda14f02da11d1ad24cca977186293b353b0009e0aaa7fe7553a281eea6b7`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ceae2a7d4d659c3e00d9310d33157c87730f9d648dcba8dc77ff73c7cd0ebb`  
		Last Modified: Fri, 15 May 2026 21:48:13 GMT  
		Size: 98.2 MB (98158490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31531ad998feab0c14348a2f3fb7c66ecc9a3385e385b1bb90e30b58f0781661`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 396.1 KB (396055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104cd6dd6848fb6f88ffb3a721916d44011eac7250f7287feae59fe29cb0cf8`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e3a45fbfd166e64afe6fce442600ae53ce1f621b2888fdb286be00e3a97fe6`  
		Last Modified: Fri, 15 May 2026 21:48:12 GMT  
		Size: 23.3 MB (23342365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:30d58547933ee45868e8fa03453883a8e8e7ebb0ec0b93ae183fae5b387d733c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23852311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4768145dd3d436fcb1a9323219167849281c6602434056fe7665bb77bb5870ee`

```dockerfile
```

-	Layers:
	-	`sha256:363a9f55d48a24246e89a02a2bc00f00e921f5fc38301c50cd365c7dbf8da48f`  
		Last Modified: Fri, 15 May 2026 21:48:11 GMT  
		Size: 23.8 MB (23835963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4192dbdfef301b27b4334fc806a3d6c2ddf3d12ee0620129f0e547048bfe1ff5`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:40578722c01a48be989affce0bfdeeaccdf2396287ea0d5ab5a7841956698364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256414614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc4da48825af92c60eaf64b725146028ce4174b6cbd1d2e8fea0dd436240e62`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:58 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:38 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:48:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:48:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:48:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014468f30de87eb3d94e1b88324914631a7cb089f3a169ac1fdf744a3559d160`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 1.2 MB (1215772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aa30806c2ef3e7edf65a7b21cd978099a1d8d1f6acae2bf635a2ce301a0c6`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 5.9 MB (5949306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd7a28491d8a8dd0417985b138019425d43e2ace5c9df92c5b58f01fd051db`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 97.4 KB (97415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b7d15ae4637078cf236f336680a72ee13366378f16c6c4bfcb58d37831bfa`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 102.6 MB (102618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eea7f6dffd18476eaf9cdb8a366a0b0f04caf38c5044baf6b36d82d89d68b`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d91a36a7b602068dc784b6706b9396d3c3504d2bdf9ebe81459eae35c25e6`  
		Last Modified: Fri, 15 May 2026 21:49:46 GMT  
		Size: 95.8 MB (95796049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85fdfeb6a9b8e66839dac0357ddab8bbc22ff10da0bf6a5f0ab9d6b201210b3`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 396.1 KB (396058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c77801f09bd7c07ec514e183c99e0ddb6cd1b49e1a007bffc9a58ddc6b437`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049dff30aaed80122a1079259c484d15cbbb5a82c778b9d47d65243b7f8d3077`  
		Last Modified: Fri, 15 May 2026 21:49:45 GMT  
		Size: 22.7 MB (22731799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:4415f07ad6929effc222b1b50f0787f008e96e4c9e4a8d7fbb294a146b2fd934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23865465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1424ab45ccf3fd775ec58923b1ae8191f006f276b63eccc8de24130353b0bbc8`

```dockerfile
```

-	Layers:
	-	`sha256:4aabba477614f3e3fd88475fe6c5d0b5af4424b69b79d2a2c47974ca8c6ff4c5`  
		Last Modified: Fri, 15 May 2026 21:49:45 GMT  
		Size: 23.8 MB (23848980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a4ecc66b5e4ab49904b94b18da8b6a9528935060ba95eb3cdce504f24874f9f`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:68473c0fae864ebda6a327338411227cb68104d2edba143cf03d22ffdece738f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:75b66caa168e592dfcacdb0ad65676620f61622ae00149f7855bd3edbbc4f974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.9 MB (955944828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a31c58c760255a50ca003973f324f4ff8a339d2487fb0e4cf5a9298a1d7f40`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:38 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:12 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:47:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:47:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 22:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2f449b78b8d36897aea1040c6dd78e2b773973b294be524f49e165bfbe125`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 1.2 MB (1215641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac297fbc77e6a50d3a6d12f6e9262ec93242659e840df00ae124230b06fbac9`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 6.0 MB (5994928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930c26f75b5fbc2a66379d9609e3c60712d47fd16ce99fbc72dd04ee8393370`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 97.3 KB (97321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef0c9426369b52a088411a845380681810dac51295fcd84b599778327158e`  
		Last Modified: Fri, 15 May 2026 21:21:41 GMT  
		Size: 104.9 MB (104865299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fda14f02da11d1ad24cca977186293b353b0009e0aaa7fe7553a281eea6b7`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ceae2a7d4d659c3e00d9310d33157c87730f9d648dcba8dc77ff73c7cd0ebb`  
		Last Modified: Fri, 15 May 2026 21:48:13 GMT  
		Size: 98.2 MB (98158490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31531ad998feab0c14348a2f3fb7c66ecc9a3385e385b1bb90e30b58f0781661`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 396.1 KB (396055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104cd6dd6848fb6f88ffb3a721916d44011eac7250f7287feae59fe29cb0cf8`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e3a45fbfd166e64afe6fce442600ae53ce1f621b2888fdb286be00e3a97fe6`  
		Last Modified: Fri, 15 May 2026 21:48:12 GMT  
		Size: 23.3 MB (23342365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f50c0a932fc7dc33c2cfadcb44cfee2b8bcf7fc61f19157d6cd947f5ec55a40`  
		Last Modified: Fri, 15 May 2026 22:16:52 GMT  
		Size: 692.1 MB (692135329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:8c941d09fe8716b88e8f85ec8098efa743dff5efe1c3e3a5fc2239b44ca62078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58945767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ff44447dabefe00b830c455015e52fd1e213bcbab67018367228a4158156b7`

```dockerfile
```

-	Layers:
	-	`sha256:02f1717fcefe8ce1c9a9d36f1dd6656040843971da1e41a9ff7db19a593286b3`  
		Last Modified: Fri, 15 May 2026 22:16:39 GMT  
		Size: 58.9 MB (58936415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c319fb03039d0f42cc164e9381b5a176cce1ebca8738390f5b9d7d25914437db`  
		Last Modified: Fri, 15 May 2026 22:16:37 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8926e0281d9605f2fb95e6216f86246fe11a63802be6c1f0f14e856d5b0725bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.5 MB (916497462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b45c02dc5b9bbbd3963fa680ef46197019c8495ce96ca11818324b045959a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:58 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:38 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:48:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:48:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:48:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014468f30de87eb3d94e1b88324914631a7cb089f3a169ac1fdf744a3559d160`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 1.2 MB (1215772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aa30806c2ef3e7edf65a7b21cd978099a1d8d1f6acae2bf635a2ce301a0c6`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 5.9 MB (5949306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd7a28491d8a8dd0417985b138019425d43e2ace5c9df92c5b58f01fd051db`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 97.4 KB (97415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b7d15ae4637078cf236f336680a72ee13366378f16c6c4bfcb58d37831bfa`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 102.6 MB (102618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eea7f6dffd18476eaf9cdb8a366a0b0f04caf38c5044baf6b36d82d89d68b`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d91a36a7b602068dc784b6706b9396d3c3504d2bdf9ebe81459eae35c25e6`  
		Last Modified: Fri, 15 May 2026 21:49:46 GMT  
		Size: 95.8 MB (95796049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85fdfeb6a9b8e66839dac0357ddab8bbc22ff10da0bf6a5f0ab9d6b201210b3`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 396.1 KB (396058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c77801f09bd7c07ec514e183c99e0ddb6cd1b49e1a007bffc9a58ddc6b437`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049dff30aaed80122a1079259c484d15cbbb5a82c778b9d47d65243b7f8d3077`  
		Last Modified: Fri, 15 May 2026 21:49:45 GMT  
		Size: 22.7 MB (22731799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a259243a3ef5f89db38fec7f6568a367ecff0fadf57d107dd306d4283e3c9ae3`  
		Last Modified: Fri, 15 May 2026 22:17:35 GMT  
		Size: 660.1 MB (660082848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:ddeecca1410601df5694ea3a1fb82d5d11331f6ac240127ace70250f132d8ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58930167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2605fd2dd97236a67f2d6dadf266c081f908e21a1e27fadaa5e31544b7ba6c`

```dockerfile
```

-	Layers:
	-	`sha256:65e1dbe0956f45609fb641835e3d75f6c3235707fea8cc3a1f3694c4f99a7b6d`  
		Last Modified: Fri, 15 May 2026 22:17:18 GMT  
		Size: 58.9 MB (58920736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023f5b82688d0e7f7ed11f028c7a41094134becf055176e138b6eab867e01c56`  
		Last Modified: Fri, 15 May 2026 22:17:15 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:68473c0fae864ebda6a327338411227cb68104d2edba143cf03d22ffdece738f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:75b66caa168e592dfcacdb0ad65676620f61622ae00149f7855bd3edbbc4f974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.9 MB (955944828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a31c58c760255a50ca003973f324f4ff8a339d2487fb0e4cf5a9298a1d7f40`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:38 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:12 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:47:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:47:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 22:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2f449b78b8d36897aea1040c6dd78e2b773973b294be524f49e165bfbe125`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 1.2 MB (1215641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac297fbc77e6a50d3a6d12f6e9262ec93242659e840df00ae124230b06fbac9`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 6.0 MB (5994928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930c26f75b5fbc2a66379d9609e3c60712d47fd16ce99fbc72dd04ee8393370`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 97.3 KB (97321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef0c9426369b52a088411a845380681810dac51295fcd84b599778327158e`  
		Last Modified: Fri, 15 May 2026 21:21:41 GMT  
		Size: 104.9 MB (104865299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fda14f02da11d1ad24cca977186293b353b0009e0aaa7fe7553a281eea6b7`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ceae2a7d4d659c3e00d9310d33157c87730f9d648dcba8dc77ff73c7cd0ebb`  
		Last Modified: Fri, 15 May 2026 21:48:13 GMT  
		Size: 98.2 MB (98158490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31531ad998feab0c14348a2f3fb7c66ecc9a3385e385b1bb90e30b58f0781661`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 396.1 KB (396055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104cd6dd6848fb6f88ffb3a721916d44011eac7250f7287feae59fe29cb0cf8`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e3a45fbfd166e64afe6fce442600ae53ce1f621b2888fdb286be00e3a97fe6`  
		Last Modified: Fri, 15 May 2026 21:48:12 GMT  
		Size: 23.3 MB (23342365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f50c0a932fc7dc33c2cfadcb44cfee2b8bcf7fc61f19157d6cd947f5ec55a40`  
		Last Modified: Fri, 15 May 2026 22:16:52 GMT  
		Size: 692.1 MB (692135329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:8c941d09fe8716b88e8f85ec8098efa743dff5efe1c3e3a5fc2239b44ca62078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58945767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ff44447dabefe00b830c455015e52fd1e213bcbab67018367228a4158156b7`

```dockerfile
```

-	Layers:
	-	`sha256:02f1717fcefe8ce1c9a9d36f1dd6656040843971da1e41a9ff7db19a593286b3`  
		Last Modified: Fri, 15 May 2026 22:16:39 GMT  
		Size: 58.9 MB (58936415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c319fb03039d0f42cc164e9381b5a176cce1ebca8738390f5b9d7d25914437db`  
		Last Modified: Fri, 15 May 2026 22:16:37 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8926e0281d9605f2fb95e6216f86246fe11a63802be6c1f0f14e856d5b0725bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.5 MB (916497462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b45c02dc5b9bbbd3963fa680ef46197019c8495ce96ca11818324b045959a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:58 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:38 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:48:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:48:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:48:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 22:14:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014468f30de87eb3d94e1b88324914631a7cb089f3a169ac1fdf744a3559d160`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 1.2 MB (1215772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aa30806c2ef3e7edf65a7b21cd978099a1d8d1f6acae2bf635a2ce301a0c6`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 5.9 MB (5949306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd7a28491d8a8dd0417985b138019425d43e2ace5c9df92c5b58f01fd051db`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 97.4 KB (97415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b7d15ae4637078cf236f336680a72ee13366378f16c6c4bfcb58d37831bfa`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 102.6 MB (102618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eea7f6dffd18476eaf9cdb8a366a0b0f04caf38c5044baf6b36d82d89d68b`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d91a36a7b602068dc784b6706b9396d3c3504d2bdf9ebe81459eae35c25e6`  
		Last Modified: Fri, 15 May 2026 21:49:46 GMT  
		Size: 95.8 MB (95796049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85fdfeb6a9b8e66839dac0357ddab8bbc22ff10da0bf6a5f0ab9d6b201210b3`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 396.1 KB (396058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c77801f09bd7c07ec514e183c99e0ddb6cd1b49e1a007bffc9a58ddc6b437`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049dff30aaed80122a1079259c484d15cbbb5a82c778b9d47d65243b7f8d3077`  
		Last Modified: Fri, 15 May 2026 21:49:45 GMT  
		Size: 22.7 MB (22731799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a259243a3ef5f89db38fec7f6568a367ecff0fadf57d107dd306d4283e3c9ae3`  
		Last Modified: Fri, 15 May 2026 22:17:35 GMT  
		Size: 660.1 MB (660082848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:ddeecca1410601df5694ea3a1fb82d5d11331f6ac240127ace70250f132d8ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58930167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2605fd2dd97236a67f2d6dadf266c081f908e21a1e27fadaa5e31544b7ba6c`

```dockerfile
```

-	Layers:
	-	`sha256:65e1dbe0956f45609fb641835e3d75f6c3235707fea8cc3a1f3694c4f99a7b6d`  
		Last Modified: Fri, 15 May 2026 22:17:18 GMT  
		Size: 58.9 MB (58920736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:023f5b82688d0e7f7ed11f028c7a41094134becf055176e138b6eab867e01c56`  
		Last Modified: Fri, 15 May 2026 22:17:15 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:5417e56962ff6e15d4cf9b2f78a71a78f3901f47cd78696b575b7eecdb54eb78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:8be79640caf3a89679d80c7666e759816cf59822521b092a5807ea8683bca366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263809499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151f70450bceb3669d183b2cc1ab203055eb68ffda3846794da043dcfb705a93`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:38 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:12 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:47:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:47:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2f449b78b8d36897aea1040c6dd78e2b773973b294be524f49e165bfbe125`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 1.2 MB (1215641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac297fbc77e6a50d3a6d12f6e9262ec93242659e840df00ae124230b06fbac9`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 6.0 MB (5994928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930c26f75b5fbc2a66379d9609e3c60712d47fd16ce99fbc72dd04ee8393370`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 97.3 KB (97321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef0c9426369b52a088411a845380681810dac51295fcd84b599778327158e`  
		Last Modified: Fri, 15 May 2026 21:21:41 GMT  
		Size: 104.9 MB (104865299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fda14f02da11d1ad24cca977186293b353b0009e0aaa7fe7553a281eea6b7`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ceae2a7d4d659c3e00d9310d33157c87730f9d648dcba8dc77ff73c7cd0ebb`  
		Last Modified: Fri, 15 May 2026 21:48:13 GMT  
		Size: 98.2 MB (98158490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31531ad998feab0c14348a2f3fb7c66ecc9a3385e385b1bb90e30b58f0781661`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 396.1 KB (396055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104cd6dd6848fb6f88ffb3a721916d44011eac7250f7287feae59fe29cb0cf8`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e3a45fbfd166e64afe6fce442600ae53ce1f621b2888fdb286be00e3a97fe6`  
		Last Modified: Fri, 15 May 2026 21:48:12 GMT  
		Size: 23.3 MB (23342365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:30d58547933ee45868e8fa03453883a8e8e7ebb0ec0b93ae183fae5b387d733c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23852311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4768145dd3d436fcb1a9323219167849281c6602434056fe7665bb77bb5870ee`

```dockerfile
```

-	Layers:
	-	`sha256:363a9f55d48a24246e89a02a2bc00f00e921f5fc38301c50cd365c7dbf8da48f`  
		Last Modified: Fri, 15 May 2026 21:48:11 GMT  
		Size: 23.8 MB (23835963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4192dbdfef301b27b4334fc806a3d6c2ddf3d12ee0620129f0e547048bfe1ff5`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:40578722c01a48be989affce0bfdeeaccdf2396287ea0d5ab5a7841956698364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256414614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc4da48825af92c60eaf64b725146028ce4174b6cbd1d2e8fea0dd436240e62`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:58 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:38 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:48:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:48:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:48:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014468f30de87eb3d94e1b88324914631a7cb089f3a169ac1fdf744a3559d160`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 1.2 MB (1215772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aa30806c2ef3e7edf65a7b21cd978099a1d8d1f6acae2bf635a2ce301a0c6`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 5.9 MB (5949306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd7a28491d8a8dd0417985b138019425d43e2ace5c9df92c5b58f01fd051db`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 97.4 KB (97415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b7d15ae4637078cf236f336680a72ee13366378f16c6c4bfcb58d37831bfa`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 102.6 MB (102618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eea7f6dffd18476eaf9cdb8a366a0b0f04caf38c5044baf6b36d82d89d68b`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d91a36a7b602068dc784b6706b9396d3c3504d2bdf9ebe81459eae35c25e6`  
		Last Modified: Fri, 15 May 2026 21:49:46 GMT  
		Size: 95.8 MB (95796049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85fdfeb6a9b8e66839dac0357ddab8bbc22ff10da0bf6a5f0ab9d6b201210b3`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 396.1 KB (396058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c77801f09bd7c07ec514e183c99e0ddb6cd1b49e1a007bffc9a58ddc6b437`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049dff30aaed80122a1079259c484d15cbbb5a82c778b9d47d65243b7f8d3077`  
		Last Modified: Fri, 15 May 2026 21:49:45 GMT  
		Size: 22.7 MB (22731799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:4415f07ad6929effc222b1b50f0787f008e96e4c9e4a8d7fbb294a146b2fd934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23865465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1424ab45ccf3fd775ec58923b1ae8191f006f276b63eccc8de24130353b0bbc8`

```dockerfile
```

-	Layers:
	-	`sha256:4aabba477614f3e3fd88475fe6c5d0b5af4424b69b79d2a2c47974ca8c6ff4c5`  
		Last Modified: Fri, 15 May 2026 21:49:45 GMT  
		Size: 23.8 MB (23848980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a4ecc66b5e4ab49904b94b18da8b6a9528935060ba95eb3cdce504f24874f9f`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:5417e56962ff6e15d4cf9b2f78a71a78f3901f47cd78696b575b7eecdb54eb78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:8be79640caf3a89679d80c7666e759816cf59822521b092a5807ea8683bca366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263809499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151f70450bceb3669d183b2cc1ab203055eb68ffda3846794da043dcfb705a93`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:38 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:12 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:47:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:47:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2f449b78b8d36897aea1040c6dd78e2b773973b294be524f49e165bfbe125`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 1.2 MB (1215641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac297fbc77e6a50d3a6d12f6e9262ec93242659e840df00ae124230b06fbac9`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 6.0 MB (5994928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930c26f75b5fbc2a66379d9609e3c60712d47fd16ce99fbc72dd04ee8393370`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 97.3 KB (97321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef0c9426369b52a088411a845380681810dac51295fcd84b599778327158e`  
		Last Modified: Fri, 15 May 2026 21:21:41 GMT  
		Size: 104.9 MB (104865299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fda14f02da11d1ad24cca977186293b353b0009e0aaa7fe7553a281eea6b7`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ceae2a7d4d659c3e00d9310d33157c87730f9d648dcba8dc77ff73c7cd0ebb`  
		Last Modified: Fri, 15 May 2026 21:48:13 GMT  
		Size: 98.2 MB (98158490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31531ad998feab0c14348a2f3fb7c66ecc9a3385e385b1bb90e30b58f0781661`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 396.1 KB (396055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104cd6dd6848fb6f88ffb3a721916d44011eac7250f7287feae59fe29cb0cf8`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e3a45fbfd166e64afe6fce442600ae53ce1f621b2888fdb286be00e3a97fe6`  
		Last Modified: Fri, 15 May 2026 21:48:12 GMT  
		Size: 23.3 MB (23342365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:30d58547933ee45868e8fa03453883a8e8e7ebb0ec0b93ae183fae5b387d733c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23852311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4768145dd3d436fcb1a9323219167849281c6602434056fe7665bb77bb5870ee`

```dockerfile
```

-	Layers:
	-	`sha256:363a9f55d48a24246e89a02a2bc00f00e921f5fc38301c50cd365c7dbf8da48f`  
		Last Modified: Fri, 15 May 2026 21:48:11 GMT  
		Size: 23.8 MB (23835963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4192dbdfef301b27b4334fc806a3d6c2ddf3d12ee0620129f0e547048bfe1ff5`  
		Last Modified: Fri, 15 May 2026 21:48:10 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:40578722c01a48be989affce0bfdeeaccdf2396287ea0d5ab5a7841956698364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256414614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc4da48825af92c60eaf64b725146028ce4174b6cbd1d2e8fea0dd436240e62`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:58 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:38 GMT
CMD ["bash"]
# Fri, 15 May 2026 21:48:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:48:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 15 May 2026 21:48:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 15 May 2026 21:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014468f30de87eb3d94e1b88324914631a7cb089f3a169ac1fdf744a3559d160`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 1.2 MB (1215772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aa30806c2ef3e7edf65a7b21cd978099a1d8d1f6acae2bf635a2ce301a0c6`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 5.9 MB (5949306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd7a28491d8a8dd0417985b138019425d43e2ace5c9df92c5b58f01fd051db`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 97.4 KB (97415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b7d15ae4637078cf236f336680a72ee13366378f16c6c4bfcb58d37831bfa`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 102.6 MB (102618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eea7f6dffd18476eaf9cdb8a366a0b0f04caf38c5044baf6b36d82d89d68b`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d91a36a7b602068dc784b6706b9396d3c3504d2bdf9ebe81459eae35c25e6`  
		Last Modified: Fri, 15 May 2026 21:49:46 GMT  
		Size: 95.8 MB (95796049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85fdfeb6a9b8e66839dac0357ddab8bbc22ff10da0bf6a5f0ab9d6b201210b3`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 396.1 KB (396058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76c77801f09bd7c07ec514e183c99e0ddb6cd1b49e1a007bffc9a58ddc6b437`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049dff30aaed80122a1079259c484d15cbbb5a82c778b9d47d65243b7f8d3077`  
		Last Modified: Fri, 15 May 2026 21:49:45 GMT  
		Size: 22.7 MB (22731799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4415f07ad6929effc222b1b50f0787f008e96e4c9e4a8d7fbb294a146b2fd934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23865465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1424ab45ccf3fd775ec58923b1ae8191f006f276b63eccc8de24130353b0bbc8`

```dockerfile
```

-	Layers:
	-	`sha256:4aabba477614f3e3fd88475fe6c5d0b5af4424b69b79d2a2c47974ca8c6ff4c5`  
		Last Modified: Fri, 15 May 2026 21:49:45 GMT  
		Size: 23.8 MB (23848980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a4ecc66b5e4ab49904b94b18da8b6a9528935060ba95eb3cdce504f24874f9f`  
		Last Modified: Fri, 15 May 2026 21:49:43 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:4cbeac7831833f8d6fa4cb1f9f8e22c188853468e76b3d5b9cc58148a8c8f64b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:25eb7f67dc506ea6d0b20607b7d515c2540184659b6e5a953aa32e95c68038ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141910069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5ff2cf0fc3550f6d97992e902daefb312111dcf16adeb40e66760cf0ddd545`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:38 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2f449b78b8d36897aea1040c6dd78e2b773973b294be524f49e165bfbe125`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 1.2 MB (1215641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac297fbc77e6a50d3a6d12f6e9262ec93242659e840df00ae124230b06fbac9`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 6.0 MB (5994928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930c26f75b5fbc2a66379d9609e3c60712d47fd16ce99fbc72dd04ee8393370`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 97.3 KB (97321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef0c9426369b52a088411a845380681810dac51295fcd84b599778327158e`  
		Last Modified: Fri, 15 May 2026 21:21:41 GMT  
		Size: 104.9 MB (104865299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fda14f02da11d1ad24cca977186293b353b0009e0aaa7fe7553a281eea6b7`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1576e00d0d67e3a7786bbc58fada59f494df83d686e728d09e5180f0cc911378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2260bd209e5895fef62196030eb8c96cf48b1a919b39cc0e7a48d3cc19e0e37`

```dockerfile
```

-	Layers:
	-	`sha256:70821dc7924a8105c6bffa9596291d764662ec8e52b3f7f913970b677c80d3ea`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 17.8 MB (17802893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae29c7b239f1a7945f7b2ea0d568f90f19f08835a41254c7cec5b790549637c`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1c305dd839535098175c5a74801cb6f46d567bae965d06255c3ecb38948ef9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137488202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da437ad6ced3d4358d1b294160910882d2d48a7d861bce0e59c0cf000cdc4dc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:58 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014468f30de87eb3d94e1b88324914631a7cb089f3a169ac1fdf744a3559d160`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 1.2 MB (1215772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aa30806c2ef3e7edf65a7b21cd978099a1d8d1f6acae2bf635a2ce301a0c6`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 5.9 MB (5949306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd7a28491d8a8dd0417985b138019425d43e2ace5c9df92c5b58f01fd051db`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 97.4 KB (97415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b7d15ae4637078cf236f336680a72ee13366378f16c6c4bfcb58d37831bfa`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 102.6 MB (102618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eea7f6dffd18476eaf9cdb8a366a0b0f04caf38c5044baf6b36d82d89d68b`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:643646f92a7fc2d126ef0fd296a0fa5fb7ceb0dcf0113c21a44630adafa3f422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be331f2dffa893dc0153e29beecd1879efa7228d6089406a1c3da7caa6b6cf1`

```dockerfile
```

-	Layers:
	-	`sha256:7cfd9d450c98036fb7be03d024712288a62767f3c55bfc2002c9dc02c9e6fd27`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 17.8 MB (17789238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9d7a480daf84256773f69d71eb314a43a3a8c9142697a75a31ed5214e70720`  
		Last Modified: Fri, 15 May 2026 21:22:03 GMT  
		Size: 14.8 KB (14751 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:4cbeac7831833f8d6fa4cb1f9f8e22c188853468e76b3d5b9cc58148a8c8f64b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:25eb7f67dc506ea6d0b20607b7d515c2540184659b6e5a953aa32e95c68038ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141910069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5ff2cf0fc3550f6d97992e902daefb312111dcf16adeb40e66760cf0ddd545`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:38 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2f449b78b8d36897aea1040c6dd78e2b773973b294be524f49e165bfbe125`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 1.2 MB (1215641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac297fbc77e6a50d3a6d12f6e9262ec93242659e840df00ae124230b06fbac9`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 6.0 MB (5994928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930c26f75b5fbc2a66379d9609e3c60712d47fd16ce99fbc72dd04ee8393370`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 97.3 KB (97321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef0c9426369b52a088411a845380681810dac51295fcd84b599778327158e`  
		Last Modified: Fri, 15 May 2026 21:21:41 GMT  
		Size: 104.9 MB (104865299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fda14f02da11d1ad24cca977186293b353b0009e0aaa7fe7553a281eea6b7`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:1576e00d0d67e3a7786bbc58fada59f494df83d686e728d09e5180f0cc911378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2260bd209e5895fef62196030eb8c96cf48b1a919b39cc0e7a48d3cc19e0e37`

```dockerfile
```

-	Layers:
	-	`sha256:70821dc7924a8105c6bffa9596291d764662ec8e52b3f7f913970b677c80d3ea`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 17.8 MB (17802893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae29c7b239f1a7945f7b2ea0d568f90f19f08835a41254c7cec5b790549637c`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1c305dd839535098175c5a74801cb6f46d567bae965d06255c3ecb38948ef9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137488202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da437ad6ced3d4358d1b294160910882d2d48a7d861bce0e59c0cf000cdc4dc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:58 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014468f30de87eb3d94e1b88324914631a7cb089f3a169ac1fdf744a3559d160`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 1.2 MB (1215772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aa30806c2ef3e7edf65a7b21cd978099a1d8d1f6acae2bf635a2ce301a0c6`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 5.9 MB (5949306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd7a28491d8a8dd0417985b138019425d43e2ace5c9df92c5b58f01fd051db`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 97.4 KB (97415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b7d15ae4637078cf236f336680a72ee13366378f16c6c4bfcb58d37831bfa`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 102.6 MB (102618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eea7f6dffd18476eaf9cdb8a366a0b0f04caf38c5044baf6b36d82d89d68b`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:643646f92a7fc2d126ef0fd296a0fa5fb7ceb0dcf0113c21a44630adafa3f422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be331f2dffa893dc0153e29beecd1879efa7228d6089406a1c3da7caa6b6cf1`

```dockerfile
```

-	Layers:
	-	`sha256:7cfd9d450c98036fb7be03d024712288a62767f3c55bfc2002c9dc02c9e6fd27`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 17.8 MB (17789238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9d7a480daf84256773f69d71eb314a43a3a8c9142697a75a31ed5214e70720`  
		Last Modified: Fri, 15 May 2026 21:22:03 GMT  
		Size: 14.8 KB (14751 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:6513503d0b10e919fbe8134981d4f9d19b5c1f9b045b87a9fe3b0b9e03e7c2a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:d7452f46711eaddadeb4a19e81a3e38fa2bf95ff792059f849efa5e94e2e891e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296020133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ff726b8762c4fad9f9743ac1f83da1f1f939087042b5b93fe97a7c0a17f2f3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae782a0a6284fab5ceff612525d03c2fbafd66097e0159150b22eaacf34ad2e`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110193360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e16aa32a6f9534a9122737424f7b375a0eaff7786e7cf7ba9a29db00fcfd0c`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 420.6 KB (420586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1d37a7b1357585f8769a5f8d1cf601e8e467f7c0572992d06579b525d49786`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135cc175fe2c44a1520fd201bec2fa8a7ca4e4d45a82979677abb1c9e9759159`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 28.1 MB (28068985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:d9e9b81219f2c665bf289ff8b6f64e41fce793f5fe9afd0e31360bdca40a6051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24806888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3389965fc524ceb14afd9c22f9adf105f8675e46fbac5719f8c67edecba3392`

```dockerfile
```

-	Layers:
	-	`sha256:297c78211e937682121d3fa452f5feab0b42dfa1e45ced5bf7d2d0958bf931e6`  
		Last Modified: Tue, 02 Jun 2026 09:15:50 GMT  
		Size: 24.8 MB (24790559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93415d3bec983b8e517f916b69bab409c59dd98f7125022f501eb653114a91a8`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e0e0a8d3dfc4bd619285fdcc995fa184db470358b39908b9b7a1e2fd470750d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284478035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2beda46c225fb76e59d2691134515789368beaa34305f07a4656f83b2e12964b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf587848da08365dc078d9f8848d4c700e5caaba2d9e1b99f5c194ec9efcb6`  
		Last Modified: Tue, 02 Jun 2026 09:24:05 GMT  
		Size: 105.6 MB (105607043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e960a7cf717d5318e8988413707746a9b3250dc72a5dd6d7b9bdc74243bf23`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 420.6 KB (420584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb59913b64666476335b92fd5df610e1cdc74d963f4f226bc9da7f41650a1e9`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20251c2eb0a2c9085ea587ef92b45b43934fa4b247e6b9c3417551e87c1cd82a`  
		Last Modified: Tue, 02 Jun 2026 09:24:04 GMT  
		Size: 27.2 MB (27177935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:5191243aa94ad5530671e9b47f58859857938d1290adccc35ac5288fa54c7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24829280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d90490eea068b87e1b19be14a846532ac88814c0ef12c6c6851ef4e3c0f52eb`

```dockerfile
```

-	Layers:
	-	`sha256:9bdcb5d514af7eb89ca037fcae0bf6117d170187e24fb192264d1f4e242a69ba`  
		Last Modified: Tue, 02 Jun 2026 09:24:03 GMT  
		Size: 24.8 MB (24812814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6923054ddc4bc7764756b1aafd6ddecd708152732604523e66727a0133457e01`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 16.5 KB (16466 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:5b201c72fd65364578eec929c3ba46f4100bcc0e2d7682bb8bf4ac1a282a9fd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:35a50d52f1900f0bd82ec2ff4ef5ab745a379bd121d24bf78ce2005509d78b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081122464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9a41f1bdfc14d3f8e2a25f14469d8a3581ba0251ac4df207332e4fc4174595`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:15:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae782a0a6284fab5ceff612525d03c2fbafd66097e0159150b22eaacf34ad2e`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110193360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e16aa32a6f9534a9122737424f7b375a0eaff7786e7cf7ba9a29db00fcfd0c`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 420.6 KB (420586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1d37a7b1357585f8769a5f8d1cf601e8e467f7c0572992d06579b525d49786`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135cc175fe2c44a1520fd201bec2fa8a7ca4e4d45a82979677abb1c9e9759159`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 28.1 MB (28068985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196a879123d1a0ba3b4bc9bc5927e8f1082c1469548d76d7d4d34a60f9838916`  
		Last Modified: Tue, 02 Jun 2026 10:18:35 GMT  
		Size: 785.1 MB (785102331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:03476dc4b14145d50d5dc9f14cd084207b27214da7ae40f7d0d196f609f0807e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60975646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc9082a760a3c5ac61e21cd2a16decf68e7b0557f088fc17b4c46b8db580a9`

```dockerfile
```

-	Layers:
	-	`sha256:c0dcdea6dafb2c7b0090103ba99845a6be3ef110178a82b22326439a85fec1ce`  
		Last Modified: Tue, 02 Jun 2026 10:18:22 GMT  
		Size: 61.0 MB (60966307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47c67b064ae76fe3190154a8e0e43f35ae8edd71c882d26292b8c31d6f67699`  
		Last Modified: Tue, 02 Jun 2026 10:18:19 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a63f1b99d65f61d357f2c90517ee19cb8ac20deffb150fc7411c1803e1dd3c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.7 MB (983709754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b9d737ffdc7dec611fe7b91ffeebaad4771d1bc1c73386002b17add86f8e16`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf587848da08365dc078d9f8848d4c700e5caaba2d9e1b99f5c194ec9efcb6`  
		Last Modified: Tue, 02 Jun 2026 09:24:05 GMT  
		Size: 105.6 MB (105607043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e960a7cf717d5318e8988413707746a9b3250dc72a5dd6d7b9bdc74243bf23`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 420.6 KB (420584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb59913b64666476335b92fd5df610e1cdc74d963f4f226bc9da7f41650a1e9`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20251c2eb0a2c9085ea587ef92b45b43934fa4b247e6b9c3417551e87c1cd82a`  
		Last Modified: Tue, 02 Jun 2026 09:24:04 GMT  
		Size: 27.2 MB (27177935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd7060f734905a126f9fa98954fe08e6f72cf300329b60024553ff7da0c5aba`  
		Last Modified: Tue, 02 Jun 2026 10:17:17 GMT  
		Size: 699.2 MB (699231719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:170302efc4c417ebe80fa810687bf3556ca493539d37c53561c52b84370697f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60906245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e4455f4155508602b2f18cf4aaec4d8b55a30aaed567c34eadfffda1bafdb`

```dockerfile
```

-	Layers:
	-	`sha256:4f01fe505ecf28fa29ced4382ca8a0805a1e8ad5575f1b94e6b17537a3e2eb4d`  
		Last Modified: Tue, 02 Jun 2026 10:17:06 GMT  
		Size: 60.9 MB (60896826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c174c53dca8fd304686d094eca4ca49afced1c47621f0ad004ebb5e13f4cb68a`  
		Last Modified: Tue, 02 Jun 2026 10:17:03 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:5b201c72fd65364578eec929c3ba46f4100bcc0e2d7682bb8bf4ac1a282a9fd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:35a50d52f1900f0bd82ec2ff4ef5ab745a379bd121d24bf78ce2005509d78b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081122464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9a41f1bdfc14d3f8e2a25f14469d8a3581ba0251ac4df207332e4fc4174595`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:15:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae782a0a6284fab5ceff612525d03c2fbafd66097e0159150b22eaacf34ad2e`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110193360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e16aa32a6f9534a9122737424f7b375a0eaff7786e7cf7ba9a29db00fcfd0c`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 420.6 KB (420586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1d37a7b1357585f8769a5f8d1cf601e8e467f7c0572992d06579b525d49786`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135cc175fe2c44a1520fd201bec2fa8a7ca4e4d45a82979677abb1c9e9759159`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 28.1 MB (28068985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196a879123d1a0ba3b4bc9bc5927e8f1082c1469548d76d7d4d34a60f9838916`  
		Last Modified: Tue, 02 Jun 2026 10:18:35 GMT  
		Size: 785.1 MB (785102331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:03476dc4b14145d50d5dc9f14cd084207b27214da7ae40f7d0d196f609f0807e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60975646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc9082a760a3c5ac61e21cd2a16decf68e7b0557f088fc17b4c46b8db580a9`

```dockerfile
```

-	Layers:
	-	`sha256:c0dcdea6dafb2c7b0090103ba99845a6be3ef110178a82b22326439a85fec1ce`  
		Last Modified: Tue, 02 Jun 2026 10:18:22 GMT  
		Size: 61.0 MB (60966307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47c67b064ae76fe3190154a8e0e43f35ae8edd71c882d26292b8c31d6f67699`  
		Last Modified: Tue, 02 Jun 2026 10:18:19 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a63f1b99d65f61d357f2c90517ee19cb8ac20deffb150fc7411c1803e1dd3c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.7 MB (983709754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b9d737ffdc7dec611fe7b91ffeebaad4771d1bc1c73386002b17add86f8e16`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf587848da08365dc078d9f8848d4c700e5caaba2d9e1b99f5c194ec9efcb6`  
		Last Modified: Tue, 02 Jun 2026 09:24:05 GMT  
		Size: 105.6 MB (105607043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e960a7cf717d5318e8988413707746a9b3250dc72a5dd6d7b9bdc74243bf23`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 420.6 KB (420584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb59913b64666476335b92fd5df610e1cdc74d963f4f226bc9da7f41650a1e9`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20251c2eb0a2c9085ea587ef92b45b43934fa4b247e6b9c3417551e87c1cd82a`  
		Last Modified: Tue, 02 Jun 2026 09:24:04 GMT  
		Size: 27.2 MB (27177935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd7060f734905a126f9fa98954fe08e6f72cf300329b60024553ff7da0c5aba`  
		Last Modified: Tue, 02 Jun 2026 10:17:17 GMT  
		Size: 699.2 MB (699231719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:170302efc4c417ebe80fa810687bf3556ca493539d37c53561c52b84370697f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60906245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36e4455f4155508602b2f18cf4aaec4d8b55a30aaed567c34eadfffda1bafdb`

```dockerfile
```

-	Layers:
	-	`sha256:4f01fe505ecf28fa29ced4382ca8a0805a1e8ad5575f1b94e6b17537a3e2eb4d`  
		Last Modified: Tue, 02 Jun 2026 10:17:06 GMT  
		Size: 60.9 MB (60896826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c174c53dca8fd304686d094eca4ca49afced1c47621f0ad004ebb5e13f4cb68a`  
		Last Modified: Tue, 02 Jun 2026 10:17:03 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:6513503d0b10e919fbe8134981d4f9d19b5c1f9b045b87a9fe3b0b9e03e7c2a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d7452f46711eaddadeb4a19e81a3e38fa2bf95ff792059f849efa5e94e2e891e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296020133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ff726b8762c4fad9f9743ac1f83da1f1f939087042b5b93fe97a7c0a17f2f3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae782a0a6284fab5ceff612525d03c2fbafd66097e0159150b22eaacf34ad2e`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110193360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e16aa32a6f9534a9122737424f7b375a0eaff7786e7cf7ba9a29db00fcfd0c`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 420.6 KB (420586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1d37a7b1357585f8769a5f8d1cf601e8e467f7c0572992d06579b525d49786`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135cc175fe2c44a1520fd201bec2fa8a7ca4e4d45a82979677abb1c9e9759159`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 28.1 MB (28068985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d9e9b81219f2c665bf289ff8b6f64e41fce793f5fe9afd0e31360bdca40a6051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24806888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3389965fc524ceb14afd9c22f9adf105f8675e46fbac5719f8c67edecba3392`

```dockerfile
```

-	Layers:
	-	`sha256:297c78211e937682121d3fa452f5feab0b42dfa1e45ced5bf7d2d0958bf931e6`  
		Last Modified: Tue, 02 Jun 2026 09:15:50 GMT  
		Size: 24.8 MB (24790559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93415d3bec983b8e517f916b69bab409c59dd98f7125022f501eb653114a91a8`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e0e0a8d3dfc4bd619285fdcc995fa184db470358b39908b9b7a1e2fd470750d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284478035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2beda46c225fb76e59d2691134515789368beaa34305f07a4656f83b2e12964b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf587848da08365dc078d9f8848d4c700e5caaba2d9e1b99f5c194ec9efcb6`  
		Last Modified: Tue, 02 Jun 2026 09:24:05 GMT  
		Size: 105.6 MB (105607043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e960a7cf717d5318e8988413707746a9b3250dc72a5dd6d7b9bdc74243bf23`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 420.6 KB (420584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb59913b64666476335b92fd5df610e1cdc74d963f4f226bc9da7f41650a1e9`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20251c2eb0a2c9085ea587ef92b45b43934fa4b247e6b9c3417551e87c1cd82a`  
		Last Modified: Tue, 02 Jun 2026 09:24:04 GMT  
		Size: 27.2 MB (27177935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:5191243aa94ad5530671e9b47f58859857938d1290adccc35ac5288fa54c7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24829280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d90490eea068b87e1b19be14a846532ac88814c0ef12c6c6851ef4e3c0f52eb`

```dockerfile
```

-	Layers:
	-	`sha256:9bdcb5d514af7eb89ca037fcae0bf6117d170187e24fb192264d1f4e242a69ba`  
		Last Modified: Tue, 02 Jun 2026 09:24:03 GMT  
		Size: 24.8 MB (24812814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6923054ddc4bc7764756b1aafd6ddecd708152732604523e66727a0133457e01`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 16.5 KB (16466 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:6513503d0b10e919fbe8134981d4f9d19b5c1f9b045b87a9fe3b0b9e03e7c2a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:d7452f46711eaddadeb4a19e81a3e38fa2bf95ff792059f849efa5e94e2e891e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296020133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ff726b8762c4fad9f9743ac1f83da1f1f939087042b5b93fe97a7c0a17f2f3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae782a0a6284fab5ceff612525d03c2fbafd66097e0159150b22eaacf34ad2e`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110193360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e16aa32a6f9534a9122737424f7b375a0eaff7786e7cf7ba9a29db00fcfd0c`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 420.6 KB (420586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1d37a7b1357585f8769a5f8d1cf601e8e467f7c0572992d06579b525d49786`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135cc175fe2c44a1520fd201bec2fa8a7ca4e4d45a82979677abb1c9e9759159`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 28.1 MB (28068985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d9e9b81219f2c665bf289ff8b6f64e41fce793f5fe9afd0e31360bdca40a6051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24806888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3389965fc524ceb14afd9c22f9adf105f8675e46fbac5719f8c67edecba3392`

```dockerfile
```

-	Layers:
	-	`sha256:297c78211e937682121d3fa452f5feab0b42dfa1e45ced5bf7d2d0958bf931e6`  
		Last Modified: Tue, 02 Jun 2026 09:15:50 GMT  
		Size: 24.8 MB (24790559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93415d3bec983b8e517f916b69bab409c59dd98f7125022f501eb653114a91a8`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 16.3 KB (16329 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e0e0a8d3dfc4bd619285fdcc995fa184db470358b39908b9b7a1e2fd470750d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284478035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2beda46c225fb76e59d2691134515789368beaa34305f07a4656f83b2e12964b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf587848da08365dc078d9f8848d4c700e5caaba2d9e1b99f5c194ec9efcb6`  
		Last Modified: Tue, 02 Jun 2026 09:24:05 GMT  
		Size: 105.6 MB (105607043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e960a7cf717d5318e8988413707746a9b3250dc72a5dd6d7b9bdc74243bf23`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 420.6 KB (420584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb59913b64666476335b92fd5df610e1cdc74d963f4f226bc9da7f41650a1e9`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20251c2eb0a2c9085ea587ef92b45b43934fa4b247e6b9c3417551e87c1cd82a`  
		Last Modified: Tue, 02 Jun 2026 09:24:04 GMT  
		Size: 27.2 MB (27177935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5191243aa94ad5530671e9b47f58859857938d1290adccc35ac5288fa54c7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24829280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d90490eea068b87e1b19be14a846532ac88814c0ef12c6c6851ef4e3c0f52eb`

```dockerfile
```

-	Layers:
	-	`sha256:9bdcb5d514af7eb89ca037fcae0bf6117d170187e24fb192264d1f4e242a69ba`  
		Last Modified: Tue, 02 Jun 2026 09:24:03 GMT  
		Size: 24.8 MB (24812814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6923054ddc4bc7764756b1aafd6ddecd708152732604523e66727a0133457e01`  
		Last Modified: Tue, 02 Jun 2026 09:24:02 GMT  
		Size: 16.5 KB (16466 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:6941e63804cfdc1d5f55d9c1e2a50d1884560c36ff7d6bb63b60b31d8bb6c9d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e6365a9c309a2ad3a9a0526284c451ebda6cf2db0ce02026ded46a749f7fa83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157334687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b07f782190fef3323a313263244ed1b01efe9dcc8df4ed108a3523b93d0014`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:a779e092720bb809b4eb6b2dd010671aeb4602999130aeb57e57a9477e48f3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18499996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05db7422452f9fbcfedbc9609ee146ce64263c4a7f7addb74621635c3c39ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:d9448848711be7fceca4ab0d0e4fcd9f46b2ed9e6b92fdc48cb12b6a652d717b`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 18.5 MB (18485388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2fb01d3c44498276833fc9676c638e9b3573b366c86c3c0b4a40a9b43c1c85`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:68f123c831efa2a0368d89d406446092f0f3a8b7a93e4cdcab1a63d55eae58ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151269956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ce9946e8b91b8ca5118b110dfeaeeff25fd0e54d094582ffb08f90c6e6fcf3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6f5faadf10a48aa1dbbb884cc0ada0d1a3a3f12b65f7c71803ae1d42b93a4b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec3f0362ffd357183e1867501a5fc9270c2d12abcf0662ec5f80775b384b047`

```dockerfile
```

-	Layers:
	-	`sha256:79d7be2339d3fd5dc220cef6585bd2209cc4f8d802b007386dba6fdf598a39de`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 18.5 MB (18459394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87f6d1b18eb8730900a9be04dcb6144e701277b1b8bebede669444c5f404b21`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 14.7 KB (14733 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:6941e63804cfdc1d5f55d9c1e2a50d1884560c36ff7d6bb63b60b31d8bb6c9d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:e6365a9c309a2ad3a9a0526284c451ebda6cf2db0ce02026ded46a749f7fa83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157334687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b07f782190fef3323a313263244ed1b01efe9dcc8df4ed108a3523b93d0014`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:56 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:34 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d846bce4f1d58b89dd53ced91e9a8c29938629724714c2903111b025f7b8a44`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 684.1 KB (684104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82986631414f8d992c60f8ef1660fdc940da635f9881ae73d1d484311b1e9d`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 6.8 MB (6752376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208489ccdf3c28b67e397bbe4b4c73c5ea61c09173396f6493ce87c638341c6`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 94.3 KB (94296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e09158eef99120b1c91819539168e1a8e109f16aa90c3a4396fbbc04550c64`  
		Last Modified: Tue, 02 Jun 2026 08:22:06 GMT  
		Size: 120.1 MB (120070909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407cb113e69c80cfa77b1c36e5180770858ccaf8bc8264dcff91143bf46a776b`  
		Last Modified: Tue, 02 Jun 2026 08:22:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a779e092720bb809b4eb6b2dd010671aeb4602999130aeb57e57a9477e48f3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18499996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05db7422452f9fbcfedbc9609ee146ce64263c4a7f7addb74621635c3c39ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:d9448848711be7fceca4ab0d0e4fcd9f46b2ed9e6b92fdc48cb12b6a652d717b`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 18.5 MB (18485388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2fb01d3c44498276833fc9676c638e9b3573b366c86c3c0b4a40a9b43c1c85`  
		Last Modified: Tue, 02 Jun 2026 08:22:03 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:68f123c831efa2a0368d89d406446092f0f3a8b7a93e4cdcab1a63d55eae58ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151269956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ce9946e8b91b8ca5118b110dfeaeeff25fd0e54d094582ffb08f90c6e6fcf3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:28 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:07 GMT
ENV ROS_DISTRO=jazzy
# Tue, 02 Jun 2026 08:22:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65eab8f59f6a22151e329eff964123e55f5301b98afcbbb273b361f05217e3e`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 684.2 KB (684230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d770d7f7b87f1a642893dbd8f13aafd550b30a4b99c081d576159c56df040f24`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 6.8 MB (6765794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749df0b3035ad88599c3a1daed49df293d59bac4f23000278e1c565660dc585`  
		Last Modified: Tue, 02 Jun 2026 08:22:34 GMT  
		Size: 94.4 KB (94413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9ccb7f9f22425073c365a7b849d32f75f8c5028a5b85615b57c6c11ef6937`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 114.8 MB (114848917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b08bdbc294829b70d4e0c2f4e0c1e50ea14bae24224078e095c47e3de9b1ee8`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6f5faadf10a48aa1dbbb884cc0ada0d1a3a3f12b65f7c71803ae1d42b93a4b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec3f0362ffd357183e1867501a5fc9270c2d12abcf0662ec5f80775b384b047`

```dockerfile
```

-	Layers:
	-	`sha256:79d7be2339d3fd5dc220cef6585bd2209cc4f8d802b007386dba6fdf598a39de`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 18.5 MB (18459394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87f6d1b18eb8730900a9be04dcb6144e701277b1b8bebede669444c5f404b21`  
		Last Modified: Tue, 02 Jun 2026 08:22:35 GMT  
		Size: 14.7 KB (14733 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:ce241352eb294cc26f99fc3b0d5a3aa9777781e6f197a9fc20e109befa08ab89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:97552ea9286484fdd62ac01f9091d7f08778dd8abcae35800ae66f84c89deb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296525362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca1dd27516e3749ee2d2648bf9f7db6092623e968f5c6fef9ba190ec662869e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7591985e47a84095a344162d1c2db751bf489e751dcd4e74636cfe7ce1b56c32`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110196246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097140c3e1ce3192ceaafb4247254801b5536f5ff6e4e935df9b35d20218973`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 384.0 KB (383978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112170637d27b54fc305ed87c92758f6cac238c074fe0c0e11226c3e22c94c3`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36c7d12f9264e8c13e70c4be0a94ec42d19a7fa9ef2e9020fa697cb5aee914`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 27.9 MB (27889252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:da0b9b34cfa4f2e02f46cb4fc2a787b180e0641b84d8016dcd778ce344654314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24756730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd08bdac497a708635a7ef3b13fa4d7f0a33c206dbb9b8070fe0fa5b4fc7296`

```dockerfile
```

-	Layers:
	-	`sha256:a8a0a8146a51875f4d1c7b2dff7bfcb1314329bdd1ce751fe21d86868b5e9778`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 24.7 MB (24740384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741fcf5c9fad5dbc7ff704534dc39fc9955edcba1567c6601e32c35d09516087`  
		Last Modified: Tue, 02 Jun 2026 09:15:47 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:837b40120856c929d7b0bc72c906aa8867506fd90f211d09afd0d9c221529050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284932276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ed99ef2ffe5535866e73b80ee91b3ec4592eb05dfc499de418d75fe7d3d97c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77bfb824aac72d5c1073df5f5acb6b7a3c20d107adec44a222da0c810d8c94`  
		Last Modified: Tue, 02 Jun 2026 09:24:11 GMT  
		Size: 105.6 MB (105609755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4428427f205c2c454f011d2825db888344ddc8501ace447a350671bfef15670a`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 384.0 KB (383972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a251bc17a680222bf4f00827205fce57a7a1229a19ed87b70fb066f99a0c5910`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18e61574b544d7fd789fc4baed9d75abfd91e2912379743520d5aaf7a68bf6`  
		Last Modified: Tue, 02 Jun 2026 09:24:09 GMT  
		Size: 27.0 MB (26997482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:fc1f84921a10b9d8372250c8a0c7383a420b806af7113c19003dbbd81b3b2116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24779128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b424d98817a45c88ad6e9be8319164e8cf15446b0a06493dcbd1391ba2e20`

```dockerfile
```

-	Layers:
	-	`sha256:2c4c5656e0cbb0d23a6940cd6150585c72d47642167049cdd5528bcae835580d`  
		Last Modified: Tue, 02 Jun 2026 09:24:08 GMT  
		Size: 24.8 MB (24762644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b762863b72c4c0fdc52e8ddbef2ec008f88a2585163002ec2ede4de40e2f48d0`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:851d2e0f778cd746eecb2765fc1f554d9de032235028a2e180853373ae2b6e91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:f810ddca7b279158107574c6ce625f1d4eb80fb986b3cafe144c598acfbaa52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081681335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362ce0f64f6743d88da084c703212db1c944cc042e5258487472125f568459b2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:19:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7591985e47a84095a344162d1c2db751bf489e751dcd4e74636cfe7ce1b56c32`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110196246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097140c3e1ce3192ceaafb4247254801b5536f5ff6e4e935df9b35d20218973`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 384.0 KB (383978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112170637d27b54fc305ed87c92758f6cac238c074fe0c0e11226c3e22c94c3`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36c7d12f9264e8c13e70c4be0a94ec42d19a7fa9ef2e9020fa697cb5aee914`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 27.9 MB (27889252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b56b3d05a6b7440849c36aa784af3d0fb9bbb69f3a047146bfa034baad1c063`  
		Last Modified: Tue, 02 Jun 2026 10:22:07 GMT  
		Size: 785.2 MB (785155973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:4096d1734135679309b4c63ea1689e518902195faeaa2747a6471a1f549a4d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60934145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d23a71d829c2df822e0f1972c0656b583e757a0c403f31c67d50752c4c59a3`

```dockerfile
```

-	Layers:
	-	`sha256:caa64c2111d457cd75385ea1933663acd672b4b6c7b7dea3ddbf60fe2a9ebc8a`  
		Last Modified: Tue, 02 Jun 2026 10:21:54 GMT  
		Size: 60.9 MB (60924794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86a8185b6ca87ea0caf5f2eb452203151125c577c4e22124d3aca0a53fa9ac9`  
		Last Modified: Tue, 02 Jun 2026 10:21:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34d5046ade40a0d5efbdc98e2816fc521030db5bc7bc068176eb1016bf597d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.2 MB (984210995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e873546207eda37bb541c2fa4db2dee886491bb6a52a83a19720aa3361d9747a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77bfb824aac72d5c1073df5f5acb6b7a3c20d107adec44a222da0c810d8c94`  
		Last Modified: Tue, 02 Jun 2026 09:24:11 GMT  
		Size: 105.6 MB (105609755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4428427f205c2c454f011d2825db888344ddc8501ace447a350671bfef15670a`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 384.0 KB (383972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a251bc17a680222bf4f00827205fce57a7a1229a19ed87b70fb066f99a0c5910`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18e61574b544d7fd789fc4baed9d75abfd91e2912379743520d5aaf7a68bf6`  
		Last Modified: Tue, 02 Jun 2026 09:24:09 GMT  
		Size: 27.0 MB (26997482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da16fd02efd72c13d52b7df4a570eab94e827361785e920aed1158a42b058cb`  
		Last Modified: Tue, 02 Jun 2026 10:17:31 GMT  
		Size: 699.3 MB (699278719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:99a11441dddef0e0d1aad4f3301d21d75d445d331688b789cb9005bf42eca76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60864750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b87cc50a78cfaf607277e28bd310860f0ade68d9c615d5cda091c494f8631c`

```dockerfile
```

-	Layers:
	-	`sha256:f3a2670857037c0e44fb6c2eba9c9594c5631a0d606dcbd99a1c6536dc77dbd4`  
		Last Modified: Tue, 02 Jun 2026 10:17:19 GMT  
		Size: 60.9 MB (60855318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0af211f7f444ca4f62d4455ae96d0fb095012b14e105cc092e5ebeb557fefb`  
		Last Modified: Tue, 02 Jun 2026 10:17:16 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:851d2e0f778cd746eecb2765fc1f554d9de032235028a2e180853373ae2b6e91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:f810ddca7b279158107574c6ce625f1d4eb80fb986b3cafe144c598acfbaa52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081681335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362ce0f64f6743d88da084c703212db1c944cc042e5258487472125f568459b2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:19:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7591985e47a84095a344162d1c2db751bf489e751dcd4e74636cfe7ce1b56c32`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110196246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097140c3e1ce3192ceaafb4247254801b5536f5ff6e4e935df9b35d20218973`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 384.0 KB (383978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112170637d27b54fc305ed87c92758f6cac238c074fe0c0e11226c3e22c94c3`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36c7d12f9264e8c13e70c4be0a94ec42d19a7fa9ef2e9020fa697cb5aee914`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 27.9 MB (27889252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b56b3d05a6b7440849c36aa784af3d0fb9bbb69f3a047146bfa034baad1c063`  
		Last Modified: Tue, 02 Jun 2026 10:22:07 GMT  
		Size: 785.2 MB (785155973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4096d1734135679309b4c63ea1689e518902195faeaa2747a6471a1f549a4d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60934145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d23a71d829c2df822e0f1972c0656b583e757a0c403f31c67d50752c4c59a3`

```dockerfile
```

-	Layers:
	-	`sha256:caa64c2111d457cd75385ea1933663acd672b4b6c7b7dea3ddbf60fe2a9ebc8a`  
		Last Modified: Tue, 02 Jun 2026 10:21:54 GMT  
		Size: 60.9 MB (60924794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86a8185b6ca87ea0caf5f2eb452203151125c577c4e22124d3aca0a53fa9ac9`  
		Last Modified: Tue, 02 Jun 2026 10:21:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34d5046ade40a0d5efbdc98e2816fc521030db5bc7bc068176eb1016bf597d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.2 MB (984210995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e873546207eda37bb541c2fa4db2dee886491bb6a52a83a19720aa3361d9747a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77bfb824aac72d5c1073df5f5acb6b7a3c20d107adec44a222da0c810d8c94`  
		Last Modified: Tue, 02 Jun 2026 09:24:11 GMT  
		Size: 105.6 MB (105609755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4428427f205c2c454f011d2825db888344ddc8501ace447a350671bfef15670a`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 384.0 KB (383972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a251bc17a680222bf4f00827205fce57a7a1229a19ed87b70fb066f99a0c5910`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18e61574b544d7fd789fc4baed9d75abfd91e2912379743520d5aaf7a68bf6`  
		Last Modified: Tue, 02 Jun 2026 09:24:09 GMT  
		Size: 27.0 MB (26997482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da16fd02efd72c13d52b7df4a570eab94e827361785e920aed1158a42b058cb`  
		Last Modified: Tue, 02 Jun 2026 10:17:31 GMT  
		Size: 699.3 MB (699278719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:99a11441dddef0e0d1aad4f3301d21d75d445d331688b789cb9005bf42eca76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60864750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b87cc50a78cfaf607277e28bd310860f0ade68d9c615d5cda091c494f8631c`

```dockerfile
```

-	Layers:
	-	`sha256:f3a2670857037c0e44fb6c2eba9c9594c5631a0d606dcbd99a1c6536dc77dbd4`  
		Last Modified: Tue, 02 Jun 2026 10:17:19 GMT  
		Size: 60.9 MB (60855318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0af211f7f444ca4f62d4455ae96d0fb095012b14e105cc092e5ebeb557fefb`  
		Last Modified: Tue, 02 Jun 2026 10:17:16 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:ce241352eb294cc26f99fc3b0d5a3aa9777781e6f197a9fc20e109befa08ab89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:97552ea9286484fdd62ac01f9091d7f08778dd8abcae35800ae66f84c89deb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296525362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca1dd27516e3749ee2d2648bf9f7db6092623e968f5c6fef9ba190ec662869e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7591985e47a84095a344162d1c2db751bf489e751dcd4e74636cfe7ce1b56c32`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110196246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097140c3e1ce3192ceaafb4247254801b5536f5ff6e4e935df9b35d20218973`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 384.0 KB (383978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112170637d27b54fc305ed87c92758f6cac238c074fe0c0e11226c3e22c94c3`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36c7d12f9264e8c13e70c4be0a94ec42d19a7fa9ef2e9020fa697cb5aee914`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 27.9 MB (27889252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:da0b9b34cfa4f2e02f46cb4fc2a787b180e0641b84d8016dcd778ce344654314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24756730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd08bdac497a708635a7ef3b13fa4d7f0a33c206dbb9b8070fe0fa5b4fc7296`

```dockerfile
```

-	Layers:
	-	`sha256:a8a0a8146a51875f4d1c7b2dff7bfcb1314329bdd1ce751fe21d86868b5e9778`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 24.7 MB (24740384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741fcf5c9fad5dbc7ff704534dc39fc9955edcba1567c6601e32c35d09516087`  
		Last Modified: Tue, 02 Jun 2026 09:15:47 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:837b40120856c929d7b0bc72c906aa8867506fd90f211d09afd0d9c221529050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284932276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ed99ef2ffe5535866e73b80ee91b3ec4592eb05dfc499de418d75fe7d3d97c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77bfb824aac72d5c1073df5f5acb6b7a3c20d107adec44a222da0c810d8c94`  
		Last Modified: Tue, 02 Jun 2026 09:24:11 GMT  
		Size: 105.6 MB (105609755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4428427f205c2c454f011d2825db888344ddc8501ace447a350671bfef15670a`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 384.0 KB (383972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a251bc17a680222bf4f00827205fce57a7a1229a19ed87b70fb066f99a0c5910`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18e61574b544d7fd789fc4baed9d75abfd91e2912379743520d5aaf7a68bf6`  
		Last Modified: Tue, 02 Jun 2026 09:24:09 GMT  
		Size: 27.0 MB (26997482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fc1f84921a10b9d8372250c8a0c7383a420b806af7113c19003dbbd81b3b2116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24779128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b424d98817a45c88ad6e9be8319164e8cf15446b0a06493dcbd1391ba2e20`

```dockerfile
```

-	Layers:
	-	`sha256:2c4c5656e0cbb0d23a6940cd6150585c72d47642167049cdd5528bcae835580d`  
		Last Modified: Tue, 02 Jun 2026 09:24:08 GMT  
		Size: 24.8 MB (24762644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b762863b72c4c0fdc52e8ddbef2ec008f88a2585163002ec2ede4de40e2f48d0`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:ce241352eb294cc26f99fc3b0d5a3aa9777781e6f197a9fc20e109befa08ab89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:97552ea9286484fdd62ac01f9091d7f08778dd8abcae35800ae66f84c89deb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296525362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca1dd27516e3749ee2d2648bf9f7db6092623e968f5c6fef9ba190ec662869e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7591985e47a84095a344162d1c2db751bf489e751dcd4e74636cfe7ce1b56c32`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110196246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097140c3e1ce3192ceaafb4247254801b5536f5ff6e4e935df9b35d20218973`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 384.0 KB (383978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112170637d27b54fc305ed87c92758f6cac238c074fe0c0e11226c3e22c94c3`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36c7d12f9264e8c13e70c4be0a94ec42d19a7fa9ef2e9020fa697cb5aee914`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 27.9 MB (27889252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:da0b9b34cfa4f2e02f46cb4fc2a787b180e0641b84d8016dcd778ce344654314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24756730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd08bdac497a708635a7ef3b13fa4d7f0a33c206dbb9b8070fe0fa5b4fc7296`

```dockerfile
```

-	Layers:
	-	`sha256:a8a0a8146a51875f4d1c7b2dff7bfcb1314329bdd1ce751fe21d86868b5e9778`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 24.7 MB (24740384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741fcf5c9fad5dbc7ff704534dc39fc9955edcba1567c6601e32c35d09516087`  
		Last Modified: Tue, 02 Jun 2026 09:15:47 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:837b40120856c929d7b0bc72c906aa8867506fd90f211d09afd0d9c221529050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284932276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ed99ef2ffe5535866e73b80ee91b3ec4592eb05dfc499de418d75fe7d3d97c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77bfb824aac72d5c1073df5f5acb6b7a3c20d107adec44a222da0c810d8c94`  
		Last Modified: Tue, 02 Jun 2026 09:24:11 GMT  
		Size: 105.6 MB (105609755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4428427f205c2c454f011d2825db888344ddc8501ace447a350671bfef15670a`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 384.0 KB (383972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a251bc17a680222bf4f00827205fce57a7a1229a19ed87b70fb066f99a0c5910`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18e61574b544d7fd789fc4baed9d75abfd91e2912379743520d5aaf7a68bf6`  
		Last Modified: Tue, 02 Jun 2026 09:24:09 GMT  
		Size: 27.0 MB (26997482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fc1f84921a10b9d8372250c8a0c7383a420b806af7113c19003dbbd81b3b2116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24779128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b424d98817a45c88ad6e9be8319164e8cf15446b0a06493dcbd1391ba2e20`

```dockerfile
```

-	Layers:
	-	`sha256:2c4c5656e0cbb0d23a6940cd6150585c72d47642167049cdd5528bcae835580d`  
		Last Modified: Tue, 02 Jun 2026 09:24:08 GMT  
		Size: 24.8 MB (24762644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b762863b72c4c0fdc52e8ddbef2ec008f88a2585163002ec2ede4de40e2f48d0`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:da1f5b694e3d822a4a0eafe449c386971058df34aa2f3df3f0b23a7ea9f9ac76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:16ca259c8b256c79331a241e758f5b0eb8b64fe5a5953ba97e2b499e1c6725b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158053388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5f3dfb8bfbd589e1910cbaaddd8e71937ef9cf96da241049362ab22e3e22fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1efe88ba089cfaa34054428a27aa7b92a4fcf015bb48555e12377f423ee2fe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18504623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e8eab4cdf2f92c7a58a22c5d48e283779ffac26f110b372020241ab860dfb5`

```dockerfile
```

-	Layers:
	-	`sha256:283e9a91fd543500db6f4166861bcc107ea492e1bbd4447973d5898863669602`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 18.5 MB (18490003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c346c041e403bac4b96cdd9e50f338d2d089267c98d06d5dd49275bb5da5c9a`  
		Last Modified: Tue, 02 Jun 2026 08:22:20 GMT  
		Size: 14.6 KB (14620 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4ff4f51647af6550b50fd6b2b88f2fb5bc32dffea3c298621c827a09ba784662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151938571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04be7631f6d56364f18a6f673429599154c2d9f5ded653d474fdd416dfdc02fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:33479e56baf77ae896f4dcb0e85f121257d5d4eb1c6b3c8a38b98b9974250f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5675d24016197ece0e28f5846899340eea58c5c55467715f09076f1da44f34f0`

```dockerfile
```

-	Layers:
	-	`sha256:c37182ae41b7488ef98ac163d48a495daa33583e2794a7da3c365118057188d0`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 18.5 MB (18464014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb28c3002411c873a47ce179ea222358d467c82e4938378f47d5590a356f8869`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 14.7 KB (14745 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:da1f5b694e3d822a4a0eafe449c386971058df34aa2f3df3f0b23a7ea9f9ac76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:16ca259c8b256c79331a241e758f5b0eb8b64fe5a5953ba97e2b499e1c6725b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158053388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5f3dfb8bfbd589e1910cbaaddd8e71937ef9cf96da241049362ab22e3e22fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1efe88ba089cfaa34054428a27aa7b92a4fcf015bb48555e12377f423ee2fe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18504623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e8eab4cdf2f92c7a58a22c5d48e283779ffac26f110b372020241ab860dfb5`

```dockerfile
```

-	Layers:
	-	`sha256:283e9a91fd543500db6f4166861bcc107ea492e1bbd4447973d5898863669602`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 18.5 MB (18490003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c346c041e403bac4b96cdd9e50f338d2d089267c98d06d5dd49275bb5da5c9a`  
		Last Modified: Tue, 02 Jun 2026 08:22:20 GMT  
		Size: 14.6 KB (14620 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4ff4f51647af6550b50fd6b2b88f2fb5bc32dffea3c298621c827a09ba784662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151938571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04be7631f6d56364f18a6f673429599154c2d9f5ded653d474fdd416dfdc02fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:33479e56baf77ae896f4dcb0e85f121257d5d4eb1c6b3c8a38b98b9974250f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5675d24016197ece0e28f5846899340eea58c5c55467715f09076f1da44f34f0`

```dockerfile
```

-	Layers:
	-	`sha256:c37182ae41b7488ef98ac163d48a495daa33583e2794a7da3c365118057188d0`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 18.5 MB (18464014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb28c3002411c873a47ce179ea222358d467c82e4938378f47d5590a356f8869`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 14.7 KB (14745 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:b1f52aa94aee73f004225d88622ed2885e2ca4793f4dc8992710438cfe9b0269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:ebffd7c6adcde3c6303f0632eb2a3bbefa5277c687189d4b43fbb2eaf7c47b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339655385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8685d999868b860c00cc60c45c93198a60605418fed94cb0a6d88d33993ac189`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Sat, 30 May 2026 00:27:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:28:19 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a66e0e4ba2827013cfdb6d7d0277845dd90d29cf5be6f6b1a2edb35b35b8f8f`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 740.5 KB (740466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d768bea23ca17d73373bced93b07f016d49dc73083020b677ca88820b6e206`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 9.8 MB (9817877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56e888694023b5e25084b3279db49e8acf8dd01b333bc892018778ac0b6217`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 89.6 KB (89573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568aec1aaa0eab51b8b82e80be56f21f3b816a67df5322fffb3616f28e0eaa6d`  
		Last Modified: Sat, 30 May 2026 00:29:04 GMT  
		Size: 136.5 MB (136498683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27deaf91b06f9331b9e482842dd053ce65d106daab5a1476638159a380ccdeab`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf73fcb880fdad57bb9149fe62bb72bc7699322651dd7861846cc93bf6d4cd8`  
		Last Modified: Sat, 30 May 2026 01:14:39 GMT  
		Size: 124.7 MB (124738161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98ddcadc581f4284f2401341e74d96eeb4a8b0c0cffa70f0027f78d6717859`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 374.9 KB (374916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dca66423f9da379a39cc77d5c07fe0ba0b022d4a9d0f0f1bdf2f74d6b68275`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 130.8 KB (130835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf504e38ad1b753e11ce22c64c2a1292309176deb0360051f00e3b8d011be59`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 25.7 MB (25709430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:ac13d7c667b3e5b5923e550e6c2924f5d3c66db47111f71de5619557196f55c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29150209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489aac56c60fb12f8ff1e1fccc2da64c1983bcc15fb126fb83dbe38d8476897b`

```dockerfile
```

-	Layers:
	-	`sha256:87b27261aee59a095152f7795ec83a54620eca7d4a9a58a9d4769d929d59fb4f`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 29.1 MB (29132760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d510f4666455834694e12ab4639c3f662718b503a8cfa4459249fdd8723a95b`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 17.4 KB (17449 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a1c58d9707d8638e25295ecffdad6b0569163f89e741eeeb1ca46b7cdda0b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324407583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf262eb9952e8435db3c947512095d094f11144f0190a1cd6e28d9ce606136f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Sat, 30 May 2026 00:26:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:27:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:27:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:27:47 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2ad364c506093b49a14399caae9c415d779931557582d1064c20883556f3a`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 741.2 KB (741165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f72c9d5baed137ff572cc6144d1b1c3ee48d9da3e8ec830a0a2b85445a8bf`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 9.6 MB (9641306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37666b6096b138cbf3a42a8c82ab2e084f00595ad4f69a0d0541a2255a450ce1`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 90.3 KB (90277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44192943d5ae755decbe581424aa597252ca509537720b2177b1dabb1ec588a9`  
		Last Modified: Sat, 30 May 2026 00:28:29 GMT  
		Size: 129.9 MB (129891737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43a2870356aaff3f0fdef23de031b83b26a6a66afe29f02ed3cdaf6285b0ea`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febeea5348f53a21fe0cc3e79465fbb577084e2a5245c53b4f19de2fbc6dd77`  
		Last Modified: Sat, 30 May 2026 01:14:36 GMT  
		Size: 118.2 MB (118153757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69509140db50f8e6085dd132443c50152cb3b18cbb37424e9e337f0cc9039c9`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 374.9 KB (374930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f65f07e25403ce1a636329c36ec386befaf8605da702e491c52ccb2fd1552`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 130.8 KB (130836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051992ea02b83d9b9d3abce9d9a9297bc29e5518b3d5bf9264b784bbad059354`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 24.7 MB (24654035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:aceda4a3c59c3da902d23035f92a710b56e9420ce4e7843e7ea1f20edaa7356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29214989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48992051392bf1b5555fa9ccd291800d9f7a47248d24fd60048e1e69a374f43c`

```dockerfile
```

-	Layers:
	-	`sha256:f468707c5422a2ffa2917b8a68997e6f8b3aef41168edabfee6f356c792a4545`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 29.2 MB (29197390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e0f3ffb85f88f59189d315ffd3b001b4f237eb6214a12175d74eca17c4d2460`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 17.6 KB (17599 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical`

```console
$ docker pull ros@sha256:b1f52aa94aee73f004225d88622ed2885e2ca4793f4dc8992710438cfe9b0269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical` - linux; amd64

```console
$ docker pull ros@sha256:ebffd7c6adcde3c6303f0632eb2a3bbefa5277c687189d4b43fbb2eaf7c47b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339655385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8685d999868b860c00cc60c45c93198a60605418fed94cb0a6d88d33993ac189`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Sat, 30 May 2026 00:27:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:28:19 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a66e0e4ba2827013cfdb6d7d0277845dd90d29cf5be6f6b1a2edb35b35b8f8f`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 740.5 KB (740466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d768bea23ca17d73373bced93b07f016d49dc73083020b677ca88820b6e206`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 9.8 MB (9817877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56e888694023b5e25084b3279db49e8acf8dd01b333bc892018778ac0b6217`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 89.6 KB (89573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568aec1aaa0eab51b8b82e80be56f21f3b816a67df5322fffb3616f28e0eaa6d`  
		Last Modified: Sat, 30 May 2026 00:29:04 GMT  
		Size: 136.5 MB (136498683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27deaf91b06f9331b9e482842dd053ce65d106daab5a1476638159a380ccdeab`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf73fcb880fdad57bb9149fe62bb72bc7699322651dd7861846cc93bf6d4cd8`  
		Last Modified: Sat, 30 May 2026 01:14:39 GMT  
		Size: 124.7 MB (124738161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98ddcadc581f4284f2401341e74d96eeb4a8b0c0cffa70f0027f78d6717859`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 374.9 KB (374916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dca66423f9da379a39cc77d5c07fe0ba0b022d4a9d0f0f1bdf2f74d6b68275`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 130.8 KB (130835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf504e38ad1b753e11ce22c64c2a1292309176deb0360051f00e3b8d011be59`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 25.7 MB (25709430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical` - unknown; unknown

```console
$ docker pull ros@sha256:ac13d7c667b3e5b5923e550e6c2924f5d3c66db47111f71de5619557196f55c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29150209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489aac56c60fb12f8ff1e1fccc2da64c1983bcc15fb126fb83dbe38d8476897b`

```dockerfile
```

-	Layers:
	-	`sha256:87b27261aee59a095152f7795ec83a54620eca7d4a9a58a9d4769d929d59fb4f`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 29.1 MB (29132760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d510f4666455834694e12ab4639c3f662718b503a8cfa4459249fdd8723a95b`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 17.4 KB (17449 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a1c58d9707d8638e25295ecffdad6b0569163f89e741eeeb1ca46b7cdda0b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324407583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf262eb9952e8435db3c947512095d094f11144f0190a1cd6e28d9ce606136f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Sat, 30 May 2026 00:26:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:27:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:27:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:27:47 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2ad364c506093b49a14399caae9c415d779931557582d1064c20883556f3a`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 741.2 KB (741165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f72c9d5baed137ff572cc6144d1b1c3ee48d9da3e8ec830a0a2b85445a8bf`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 9.6 MB (9641306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37666b6096b138cbf3a42a8c82ab2e084f00595ad4f69a0d0541a2255a450ce1`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 90.3 KB (90277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44192943d5ae755decbe581424aa597252ca509537720b2177b1dabb1ec588a9`  
		Last Modified: Sat, 30 May 2026 00:28:29 GMT  
		Size: 129.9 MB (129891737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43a2870356aaff3f0fdef23de031b83b26a6a66afe29f02ed3cdaf6285b0ea`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febeea5348f53a21fe0cc3e79465fbb577084e2a5245c53b4f19de2fbc6dd77`  
		Last Modified: Sat, 30 May 2026 01:14:36 GMT  
		Size: 118.2 MB (118153757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69509140db50f8e6085dd132443c50152cb3b18cbb37424e9e337f0cc9039c9`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 374.9 KB (374930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f65f07e25403ce1a636329c36ec386befaf8605da702e491c52ccb2fd1552`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 130.8 KB (130836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051992ea02b83d9b9d3abce9d9a9297bc29e5518b3d5bf9264b784bbad059354`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 24.7 MB (24654035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical` - unknown; unknown

```console
$ docker pull ros@sha256:aceda4a3c59c3da902d23035f92a710b56e9420ce4e7843e7ea1f20edaa7356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29214989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48992051392bf1b5555fa9ccd291800d9f7a47248d24fd60048e1e69a374f43c`

```dockerfile
```

-	Layers:
	-	`sha256:f468707c5422a2ffa2917b8a68997e6f8b3aef41168edabfee6f356c792a4545`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 29.2 MB (29197390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e0f3ffb85f88f59189d315ffd3b001b4f237eb6214a12175d74eca17c4d2460`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 17.6 KB (17599 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-perception`

```console
$ docker pull ros@sha256:8cb32004658244c657fa7bb1e9230aef6ed9d4ba8181c863897add71905ff48e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-perception` - linux; amd64

```console
$ docker pull ros@sha256:aa8b68896fa66d5cd0352dde8c6ffae12cedfa2f77679b18a03b0928cabeaa9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1528199615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f503e1121a5e6ba21e76796ac0c71ec4f1ee96af1aca4f05a1a7c7edcbe4dbd9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Sat, 30 May 2026 00:27:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:28:19 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 02:15:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-perception=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a66e0e4ba2827013cfdb6d7d0277845dd90d29cf5be6f6b1a2edb35b35b8f8f`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 740.5 KB (740466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d768bea23ca17d73373bced93b07f016d49dc73083020b677ca88820b6e206`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 9.8 MB (9817877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56e888694023b5e25084b3279db49e8acf8dd01b333bc892018778ac0b6217`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 89.6 KB (89573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568aec1aaa0eab51b8b82e80be56f21f3b816a67df5322fffb3616f28e0eaa6d`  
		Last Modified: Sat, 30 May 2026 00:29:04 GMT  
		Size: 136.5 MB (136498683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27deaf91b06f9331b9e482842dd053ce65d106daab5a1476638159a380ccdeab`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf73fcb880fdad57bb9149fe62bb72bc7699322651dd7861846cc93bf6d4cd8`  
		Last Modified: Sat, 30 May 2026 01:14:39 GMT  
		Size: 124.7 MB (124738161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98ddcadc581f4284f2401341e74d96eeb4a8b0c0cffa70f0027f78d6717859`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 374.9 KB (374916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dca66423f9da379a39cc77d5c07fe0ba0b022d4a9d0f0f1bdf2f74d6b68275`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 130.8 KB (130835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf504e38ad1b753e11ce22c64c2a1292309176deb0360051f00e3b8d011be59`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 25.7 MB (25709430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdfc4f87de9141756f778bd2e5bf768817864213c0d9662ef6994cf323e8e30`  
		Last Modified: Sat, 30 May 2026 02:20:37 GMT  
		Size: 1.2 GB (1188544230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-perception` - unknown; unknown

```console
$ docker pull ros@sha256:6a869d3c781cc22fad04c0662c82f921230b6a8e90e6bf8f563307f0aede6b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64350750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9b7c3cc9ecc9be8799a4a234d6c95129540a504d2889fadec4c80f05d7544f`

```dockerfile
```

-	Layers:
	-	`sha256:a7d08789c88ad0e61effa43386a8ba159b7cf148350f626f8aa1776a89cb70da`  
		Last Modified: Sat, 30 May 2026 02:20:11 GMT  
		Size: 64.3 MB (64341057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc186b991f4d514d9d941a4f053e66b10a06782830e39af71512aafcd10c90d1`  
		Last Modified: Sat, 30 May 2026 02:20:08 GMT  
		Size: 9.7 KB (9693 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:656e1aefe7c8986cd2066641857bc0cfeeae7dcbaaa30b934b13be334c50c9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1471574755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e0dc9ddf7e97f642a85a830eeca1020699156f41a5c0fa52d9387449d5337f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Sat, 30 May 2026 00:26:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:27:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:27:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:27:47 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 02:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-perception=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2ad364c506093b49a14399caae9c415d779931557582d1064c20883556f3a`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 741.2 KB (741165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f72c9d5baed137ff572cc6144d1b1c3ee48d9da3e8ec830a0a2b85445a8bf`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 9.6 MB (9641306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37666b6096b138cbf3a42a8c82ab2e084f00595ad4f69a0d0541a2255a450ce1`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 90.3 KB (90277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44192943d5ae755decbe581424aa597252ca509537720b2177b1dabb1ec588a9`  
		Last Modified: Sat, 30 May 2026 00:28:29 GMT  
		Size: 129.9 MB (129891737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43a2870356aaff3f0fdef23de031b83b26a6a66afe29f02ed3cdaf6285b0ea`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febeea5348f53a21fe0cc3e79465fbb577084e2a5245c53b4f19de2fbc6dd77`  
		Last Modified: Sat, 30 May 2026 01:14:36 GMT  
		Size: 118.2 MB (118153757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69509140db50f8e6085dd132443c50152cb3b18cbb37424e9e337f0cc9039c9`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 374.9 KB (374930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f65f07e25403ce1a636329c36ec386befaf8605da702e491c52ccb2fd1552`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 130.8 KB (130836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051992ea02b83d9b9d3abce9d9a9297bc29e5518b3d5bf9264b784bbad059354`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 24.7 MB (24654035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe61cf293732d8bfbc5f102478fd11ef717e8efc073885e318f7f637d665b3`  
		Last Modified: Sat, 30 May 2026 02:20:42 GMT  
		Size: 1.1 GB (1147167172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e9a6b39c22df807df0a2c5946ca79462d99c04cca9cd0ddbd7751750a775a79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64265046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241f02fc05a7b7178aeacd309964bc7856f2c9bd7fb9ada70bb45beb4b848517`

```dockerfile
```

-	Layers:
	-	`sha256:80580a2398caf1528a846159219ce246e1028a1e271301f9237bd32c09ea5a76`  
		Last Modified: Sat, 30 May 2026 02:20:23 GMT  
		Size: 64.3 MB (64255273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368e29bfae84e8a0f7cb232e8b8269e519b6c2f41b839f3f9a0d642f58240b5d`  
		Last Modified: Sat, 30 May 2026 02:20:20 GMT  
		Size: 9.8 KB (9773 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-perception-resolute`

```console
$ docker pull ros@sha256:8cb32004658244c657fa7bb1e9230aef6ed9d4ba8181c863897add71905ff48e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-perception-resolute` - linux; amd64

```console
$ docker pull ros@sha256:aa8b68896fa66d5cd0352dde8c6ffae12cedfa2f77679b18a03b0928cabeaa9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1528199615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f503e1121a5e6ba21e76796ac0c71ec4f1ee96af1aca4f05a1a7c7edcbe4dbd9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Sat, 30 May 2026 00:27:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:28:19 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 02:15:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-perception=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a66e0e4ba2827013cfdb6d7d0277845dd90d29cf5be6f6b1a2edb35b35b8f8f`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 740.5 KB (740466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d768bea23ca17d73373bced93b07f016d49dc73083020b677ca88820b6e206`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 9.8 MB (9817877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56e888694023b5e25084b3279db49e8acf8dd01b333bc892018778ac0b6217`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 89.6 KB (89573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568aec1aaa0eab51b8b82e80be56f21f3b816a67df5322fffb3616f28e0eaa6d`  
		Last Modified: Sat, 30 May 2026 00:29:04 GMT  
		Size: 136.5 MB (136498683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27deaf91b06f9331b9e482842dd053ce65d106daab5a1476638159a380ccdeab`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf73fcb880fdad57bb9149fe62bb72bc7699322651dd7861846cc93bf6d4cd8`  
		Last Modified: Sat, 30 May 2026 01:14:39 GMT  
		Size: 124.7 MB (124738161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98ddcadc581f4284f2401341e74d96eeb4a8b0c0cffa70f0027f78d6717859`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 374.9 KB (374916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dca66423f9da379a39cc77d5c07fe0ba0b022d4a9d0f0f1bdf2f74d6b68275`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 130.8 KB (130835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf504e38ad1b753e11ce22c64c2a1292309176deb0360051f00e3b8d011be59`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 25.7 MB (25709430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdfc4f87de9141756f778bd2e5bf768817864213c0d9662ef6994cf323e8e30`  
		Last Modified: Sat, 30 May 2026 02:20:37 GMT  
		Size: 1.2 GB (1188544230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-perception-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:6a869d3c781cc22fad04c0662c82f921230b6a8e90e6bf8f563307f0aede6b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64350750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9b7c3cc9ecc9be8799a4a234d6c95129540a504d2889fadec4c80f05d7544f`

```dockerfile
```

-	Layers:
	-	`sha256:a7d08789c88ad0e61effa43386a8ba159b7cf148350f626f8aa1776a89cb70da`  
		Last Modified: Sat, 30 May 2026 02:20:11 GMT  
		Size: 64.3 MB (64341057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc186b991f4d514d9d941a4f053e66b10a06782830e39af71512aafcd10c90d1`  
		Last Modified: Sat, 30 May 2026 02:20:08 GMT  
		Size: 9.7 KB (9693 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-perception-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:656e1aefe7c8986cd2066641857bc0cfeeae7dcbaaa30b934b13be334c50c9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1471574755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e0dc9ddf7e97f642a85a830eeca1020699156f41a5c0fa52d9387449d5337f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Sat, 30 May 2026 00:26:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:27:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:27:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:27:47 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 02:16:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-perception=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2ad364c506093b49a14399caae9c415d779931557582d1064c20883556f3a`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 741.2 KB (741165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f72c9d5baed137ff572cc6144d1b1c3ee48d9da3e8ec830a0a2b85445a8bf`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 9.6 MB (9641306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37666b6096b138cbf3a42a8c82ab2e084f00595ad4f69a0d0541a2255a450ce1`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 90.3 KB (90277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44192943d5ae755decbe581424aa597252ca509537720b2177b1dabb1ec588a9`  
		Last Modified: Sat, 30 May 2026 00:28:29 GMT  
		Size: 129.9 MB (129891737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43a2870356aaff3f0fdef23de031b83b26a6a66afe29f02ed3cdaf6285b0ea`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febeea5348f53a21fe0cc3e79465fbb577084e2a5245c53b4f19de2fbc6dd77`  
		Last Modified: Sat, 30 May 2026 01:14:36 GMT  
		Size: 118.2 MB (118153757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69509140db50f8e6085dd132443c50152cb3b18cbb37424e9e337f0cc9039c9`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 374.9 KB (374930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f65f07e25403ce1a636329c36ec386befaf8605da702e491c52ccb2fd1552`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 130.8 KB (130836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051992ea02b83d9b9d3abce9d9a9297bc29e5518b3d5bf9264b784bbad059354`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 24.7 MB (24654035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfe61cf293732d8bfbc5f102478fd11ef717e8efc073885e318f7f637d665b3`  
		Last Modified: Sat, 30 May 2026 02:20:42 GMT  
		Size: 1.1 GB (1147167172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-perception-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:e9a6b39c22df807df0a2c5946ca79462d99c04cca9cd0ddbd7751750a775a79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64265046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241f02fc05a7b7178aeacd309964bc7856f2c9bd7fb9ada70bb45beb4b848517`

```dockerfile
```

-	Layers:
	-	`sha256:80580a2398caf1528a846159219ce246e1028a1e271301f9237bd32c09ea5a76`  
		Last Modified: Sat, 30 May 2026 02:20:23 GMT  
		Size: 64.3 MB (64255273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368e29bfae84e8a0f7cb232e8b8269e519b6c2f41b839f3f9a0d642f58240b5d`  
		Last Modified: Sat, 30 May 2026 02:20:20 GMT  
		Size: 9.8 KB (9773 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-ros-base`

```console
$ docker pull ros@sha256:b1f52aa94aee73f004225d88622ed2885e2ca4793f4dc8992710438cfe9b0269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:ebffd7c6adcde3c6303f0632eb2a3bbefa5277c687189d4b43fbb2eaf7c47b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339655385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8685d999868b860c00cc60c45c93198a60605418fed94cb0a6d88d33993ac189`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Sat, 30 May 2026 00:27:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:28:19 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a66e0e4ba2827013cfdb6d7d0277845dd90d29cf5be6f6b1a2edb35b35b8f8f`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 740.5 KB (740466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d768bea23ca17d73373bced93b07f016d49dc73083020b677ca88820b6e206`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 9.8 MB (9817877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56e888694023b5e25084b3279db49e8acf8dd01b333bc892018778ac0b6217`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 89.6 KB (89573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568aec1aaa0eab51b8b82e80be56f21f3b816a67df5322fffb3616f28e0eaa6d`  
		Last Modified: Sat, 30 May 2026 00:29:04 GMT  
		Size: 136.5 MB (136498683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27deaf91b06f9331b9e482842dd053ce65d106daab5a1476638159a380ccdeab`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf73fcb880fdad57bb9149fe62bb72bc7699322651dd7861846cc93bf6d4cd8`  
		Last Modified: Sat, 30 May 2026 01:14:39 GMT  
		Size: 124.7 MB (124738161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98ddcadc581f4284f2401341e74d96eeb4a8b0c0cffa70f0027f78d6717859`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 374.9 KB (374916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dca66423f9da379a39cc77d5c07fe0ba0b022d4a9d0f0f1bdf2f74d6b68275`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 130.8 KB (130835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf504e38ad1b753e11ce22c64c2a1292309176deb0360051f00e3b8d011be59`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 25.7 MB (25709430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:ac13d7c667b3e5b5923e550e6c2924f5d3c66db47111f71de5619557196f55c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29150209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489aac56c60fb12f8ff1e1fccc2da64c1983bcc15fb126fb83dbe38d8476897b`

```dockerfile
```

-	Layers:
	-	`sha256:87b27261aee59a095152f7795ec83a54620eca7d4a9a58a9d4769d929d59fb4f`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 29.1 MB (29132760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d510f4666455834694e12ab4639c3f662718b503a8cfa4459249fdd8723a95b`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 17.4 KB (17449 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a1c58d9707d8638e25295ecffdad6b0569163f89e741eeeb1ca46b7cdda0b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324407583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf262eb9952e8435db3c947512095d094f11144f0190a1cd6e28d9ce606136f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Sat, 30 May 2026 00:26:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:27:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:27:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:27:47 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2ad364c506093b49a14399caae9c415d779931557582d1064c20883556f3a`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 741.2 KB (741165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f72c9d5baed137ff572cc6144d1b1c3ee48d9da3e8ec830a0a2b85445a8bf`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 9.6 MB (9641306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37666b6096b138cbf3a42a8c82ab2e084f00595ad4f69a0d0541a2255a450ce1`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 90.3 KB (90277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44192943d5ae755decbe581424aa597252ca509537720b2177b1dabb1ec588a9`  
		Last Modified: Sat, 30 May 2026 00:28:29 GMT  
		Size: 129.9 MB (129891737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43a2870356aaff3f0fdef23de031b83b26a6a66afe29f02ed3cdaf6285b0ea`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febeea5348f53a21fe0cc3e79465fbb577084e2a5245c53b4f19de2fbc6dd77`  
		Last Modified: Sat, 30 May 2026 01:14:36 GMT  
		Size: 118.2 MB (118153757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69509140db50f8e6085dd132443c50152cb3b18cbb37424e9e337f0cc9039c9`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 374.9 KB (374930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f65f07e25403ce1a636329c36ec386befaf8605da702e491c52ccb2fd1552`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 130.8 KB (130836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051992ea02b83d9b9d3abce9d9a9297bc29e5518b3d5bf9264b784bbad059354`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 24.7 MB (24654035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:aceda4a3c59c3da902d23035f92a710b56e9420ce4e7843e7ea1f20edaa7356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29214989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48992051392bf1b5555fa9ccd291800d9f7a47248d24fd60048e1e69a374f43c`

```dockerfile
```

-	Layers:
	-	`sha256:f468707c5422a2ffa2917b8a68997e6f8b3aef41168edabfee6f356c792a4545`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 29.2 MB (29197390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e0f3ffb85f88f59189d315ffd3b001b4f237eb6214a12175d74eca17c4d2460`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 17.6 KB (17599 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-ros-base-resolute`

```console
$ docker pull ros@sha256:b1f52aa94aee73f004225d88622ed2885e2ca4793f4dc8992710438cfe9b0269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-base-resolute` - linux; amd64

```console
$ docker pull ros@sha256:ebffd7c6adcde3c6303f0632eb2a3bbefa5277c687189d4b43fbb2eaf7c47b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339655385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8685d999868b860c00cc60c45c93198a60605418fed94cb0a6d88d33993ac189`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 17:23:53 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4415.tar --tag 26.04
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T17:23:54.324551+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 17:23:54 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4415.tar
# Sat, 30 May 2026 00:27:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:28:19 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:28:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:28:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:28:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:28:19 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f5c5aa4e145204b113f983c003ff8ad6489394294ef95ec030bc94e3daded54`  
		Last Modified: Tue, 21 Apr 2026 18:49:33 GMT  
		Size: 41.6 MB (41554862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c24335ddd46023ff99bd665bd8ea6798464f7bbf501718edcf2eb4696e5f408`  
		Last Modified: Tue, 21 Apr 2026 18:49:35 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a66e0e4ba2827013cfdb6d7d0277845dd90d29cf5be6f6b1a2edb35b35b8f8f`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 740.5 KB (740466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d768bea23ca17d73373bced93b07f016d49dc73083020b677ca88820b6e206`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 9.8 MB (9817877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d56e888694023b5e25084b3279db49e8acf8dd01b333bc892018778ac0b6217`  
		Last Modified: Sat, 30 May 2026 00:29:01 GMT  
		Size: 89.6 KB (89573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568aec1aaa0eab51b8b82e80be56f21f3b816a67df5322fffb3616f28e0eaa6d`  
		Last Modified: Sat, 30 May 2026 00:29:04 GMT  
		Size: 136.5 MB (136498683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27deaf91b06f9331b9e482842dd053ce65d106daab5a1476638159a380ccdeab`  
		Last Modified: Sat, 30 May 2026 00:29:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf73fcb880fdad57bb9149fe62bb72bc7699322651dd7861846cc93bf6d4cd8`  
		Last Modified: Sat, 30 May 2026 01:14:39 GMT  
		Size: 124.7 MB (124738161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb98ddcadc581f4284f2401341e74d96eeb4a8b0c0cffa70f0027f78d6717859`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 374.9 KB (374916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dca66423f9da379a39cc77d5c07fe0ba0b022d4a9d0f0f1bdf2f74d6b68275`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 130.8 KB (130835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf504e38ad1b753e11ce22c64c2a1292309176deb0360051f00e3b8d011be59`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 25.7 MB (25709430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:ac13d7c667b3e5b5923e550e6c2924f5d3c66db47111f71de5619557196f55c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29150209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489aac56c60fb12f8ff1e1fccc2da64c1983bcc15fb126fb83dbe38d8476897b`

```dockerfile
```

-	Layers:
	-	`sha256:87b27261aee59a095152f7795ec83a54620eca7d4a9a58a9d4769d929d59fb4f`  
		Last Modified: Sat, 30 May 2026 01:14:37 GMT  
		Size: 29.1 MB (29132760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d510f4666455834694e12ab4639c3f662718b503a8cfa4459249fdd8723a95b`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 17.4 KB (17449 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-base-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a1c58d9707d8638e25295ecffdad6b0569163f89e741eeeb1ca46b7cdda0b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324407583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf262eb9952e8435db3c947512095d094f11144f0190a1cd6e28d9ce606136f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 15:27:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.4553.tar --tag 26.04
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-04-21T15:27:26.117874+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Tue, 21 Apr 2026 15:27:26 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-5691f940e215a35dc9b91fc1887cae39/images/.temp_layer.control_data.4553.tar
# Sat, 30 May 2026 00:26:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:26:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 May 2026 00:27:46 GMT
ENV ROS_DISTRO=lyrical
# Sat, 30 May 2026 00:27:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 00:27:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 30 May 2026 00:27:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 May 2026 00:27:47 GMT
CMD ["bash"]
# Sat, 30 May 2026 01:13:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 May 2026 01:13:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 30 May 2026 01:13:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 30 May 2026 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2113f8d7eb32748b14581824c1b94cea9ed9a08456312a2e94eddd522d01b927`  
		Last Modified: Tue, 21 Apr 2026 18:49:43 GMT  
		Size: 40.7 MB (40728955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7720058461eb4ae40ed203b9874ab3248bd34ffb9948193e99245229fdbd6f`  
		Last Modified: Tue, 21 Apr 2026 18:49:46 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc2ad364c506093b49a14399caae9c415d779931557582d1064c20883556f3a`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 741.2 KB (741165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f72c9d5baed137ff572cc6144d1b1c3ee48d9da3e8ec830a0a2b85445a8bf`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 9.6 MB (9641306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37666b6096b138cbf3a42a8c82ab2e084f00595ad4f69a0d0541a2255a450ce1`  
		Last Modified: Sat, 30 May 2026 00:28:26 GMT  
		Size: 90.3 KB (90277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44192943d5ae755decbe581424aa597252ca509537720b2177b1dabb1ec588a9`  
		Last Modified: Sat, 30 May 2026 00:28:29 GMT  
		Size: 129.9 MB (129891737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f43a2870356aaff3f0fdef23de031b83b26a6a66afe29f02ed3cdaf6285b0ea`  
		Last Modified: Sat, 30 May 2026 00:28:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febeea5348f53a21fe0cc3e79465fbb577084e2a5245c53b4f19de2fbc6dd77`  
		Last Modified: Sat, 30 May 2026 01:14:36 GMT  
		Size: 118.2 MB (118153757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69509140db50f8e6085dd132443c50152cb3b18cbb37424e9e337f0cc9039c9`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 374.9 KB (374930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f65f07e25403ce1a636329c36ec386befaf8605da702e491c52ccb2fd1552`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 130.8 KB (130836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051992ea02b83d9b9d3abce9d9a9297bc29e5518b3d5bf9264b784bbad059354`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 24.7 MB (24654035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:aceda4a3c59c3da902d23035f92a710b56e9420ce4e7843e7ea1f20edaa7356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29214989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48992051392bf1b5555fa9ccd291800d9f7a47248d24fd60048e1e69a374f43c`

```dockerfile
```

-	Layers:
	-	`sha256:f468707c5422a2ffa2917b8a68997e6f8b3aef41168edabfee6f356c792a4545`  
		Last Modified: Sat, 30 May 2026 01:14:35 GMT  
		Size: 29.2 MB (29197390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e0f3ffb85f88f59189d315ffd3b001b4f237eb6214a12175d74eca17c4d2460`  
		Last Modified: Sat, 30 May 2026 01:14:33 GMT  
		Size: 17.6 KB (17599 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-ros-core`

```console
$ docker pull ros@sha256:35cd26774677a7d16d52ddf951945ec39249620a230a731867fbc1b2c5528a81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:b284cd8ad0e2fdbae28bc8b32763bcc51fa1bfa8d30dffa6907cac4c20e0a02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188678485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896945d08856430f18c0e7592f41d0d68b18f3240bf6fd77bda4bb71cf6c7c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9106.tar --tag 26.04
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9106.tar
# Fri, 19 Jun 2026 01:11:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:05 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
ENV LANG=C.UTF-8
# Fri, 19 Jun 2026 01:12:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 19 Jun 2026 01:12:50 GMT
ENV ROS_DISTRO=lyrical
# Fri, 19 Jun 2026 01:12:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 19 Jun 2026 01:12:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:81e2f2053c8fa702b6863110b55c09e67f6adeb78b4672745958c4d8b3d056c5`  
		Last Modified: Wed, 10 Jun 2026 08:00:11 GMT  
		Size: 41.6 MB (41562239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f56e4c7f2f2a1415c59803638274d488a73b61a8e1f9cbd9cb280327e8d21e`  
		Last Modified: Wed, 10 Jun 2026 08:00:15 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b1770788335db7604bba0ceb7a41f3cc6c19bbd36127093ac28bace3e00d7`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 740.8 KB (740786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e9c2cfcc02849b9506d2d29cb96f6ee38f7aebaf50ab1dc83d009eb71aabc`  
		Last Modified: Fri, 19 Jun 2026 01:13:33 GMT  
		Size: 9.8 MB (9784527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7de4965a0ddc323590e6e47b9a1c7c8543b5f4b15cbf6f8cb37582b4518e54a`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 89.9 KB (89872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca11c3384c15abaac0e22d6c4ac49a8170e954811534a42084f875a7cf0e80f`  
		Last Modified: Fri, 19 Jun 2026 01:13:36 GMT  
		Size: 136.5 MB (136500477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9fc928349304d575f19e26e4713c0e9ab4159bb13cefa8129dfb1c2abe8c9`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:90772d8f5ad2144b3fd5499450aef23a8660776d73b8b19cea04fe1651c939bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22743715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e522b78fef8fb25982c60655ba79d5417bce136c92ebf23b45b6a4d34217a4a8`

```dockerfile
```

-	Layers:
	-	`sha256:1b42c20d4c4fa30bb56ce45aed546a5a99637193ba5bba1b55abf2a01929418f`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 22.7 MB (22728132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64aa8640d790d8ad8db5e3d7c98d44f716d6b4b4143b3c9ec0b11c786d023141`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:04207016a6ef92ae044c153be5feef75fb6ad5b50f248b174250aacc2b6718d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181062230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab98f50882aebd1ebd543911a236c82fc8cb6288ca9dd6a353b903910e62f6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9196.tar --tag 26.04
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9196.tar
# Fri, 19 Jun 2026 01:11:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
ENV LANG=C.UTF-8
# Fri, 19 Jun 2026 01:12:55 GMT
ENV LC_ALL=C.UTF-8
# Fri, 19 Jun 2026 01:12:55 GMT
ENV ROS_DISTRO=lyrical
# Fri, 19 Jun 2026 01:12:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 19 Jun 2026 01:12:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c572f291b2a0cc05a1d523f3dda4d3f1992c3e480debf2e1bc9278aeab115625`  
		Last Modified: Wed, 10 Jun 2026 08:00:25 GMT  
		Size: 40.7 MB (40709186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dda33820b52cf93fd5ff3808c770af252cf0565784b42e52e3dd74e2ebf5b2`  
		Last Modified: Wed, 10 Jun 2026 08:00:29 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4986530f0d3c75ff7820390034f5d3e027407a16c974996b5ded332599d708`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 740.9 KB (740883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65791f49907d0570d76708a6b7fff49950ae25a376454d38f6777a932bacdfb`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 9.6 MB (9605840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0681652efa697f65008a0c4209e2155b9e5cf57e320f77ceba5d9443b4cbd283`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 90.0 KB (89997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b374f8a21b565bdf721c78327461dd298e6749b9b13b05d9f6cabfb073f7bc`  
		Last Modified: Fri, 19 Jun 2026 01:13:37 GMT  
		Size: 129.9 MB (129915744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da7d04141ffff77c744942b698c8f9e8a3641e745c138843a6922858ad57b69`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6c584cb629c967825549a27f4bf7796a017f86f36d060821e08ca9e2861e2837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22716532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06e5e7c60935235d68affcba56428c89dfbbfb17c0560e188c8501a30b67112`

```dockerfile
```

-	Layers:
	-	`sha256:50cb1dd67369a2a06012835610c6f712223ecc272a3c36f568bb50701aafcf7a`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 22.7 MB (22700824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593bef670fc1f1f878df6670a546fec072d19ffe49f9796464d07b1941099d0e`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 15.7 KB (15708 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-ros-core-resolute`

```console
$ docker pull ros@sha256:35cd26774677a7d16d52ddf951945ec39249620a230a731867fbc1b2c5528a81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-core-resolute` - linux; amd64

```console
$ docker pull ros@sha256:b284cd8ad0e2fdbae28bc8b32763bcc51fa1bfa8d30dffa6907cac4c20e0a02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188678485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896945d08856430f18c0e7592f41d0d68b18f3240bf6fd77bda4bb71cf6c7c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9106.tar --tag 26.04
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:30:57.931695+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:30:57 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9106.tar
# Fri, 19 Jun 2026 01:11:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:05 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
ENV LANG=C.UTF-8
# Fri, 19 Jun 2026 01:12:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 19 Jun 2026 01:12:50 GMT
ENV ROS_DISTRO=lyrical
# Fri, 19 Jun 2026 01:12:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 19 Jun 2026 01:12:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 19 Jun 2026 01:12:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:81e2f2053c8fa702b6863110b55c09e67f6adeb78b4672745958c4d8b3d056c5`  
		Last Modified: Wed, 10 Jun 2026 08:00:11 GMT  
		Size: 41.6 MB (41562239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f56e4c7f2f2a1415c59803638274d488a73b61a8e1f9cbd9cb280327e8d21e`  
		Last Modified: Wed, 10 Jun 2026 08:00:15 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b1770788335db7604bba0ceb7a41f3cc6c19bbd36127093ac28bace3e00d7`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 740.8 KB (740786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7e9c2cfcc02849b9506d2d29cb96f6ee38f7aebaf50ab1dc83d009eb71aabc`  
		Last Modified: Fri, 19 Jun 2026 01:13:33 GMT  
		Size: 9.8 MB (9784527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7de4965a0ddc323590e6e47b9a1c7c8543b5f4b15cbf6f8cb37582b4518e54a`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 89.9 KB (89872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca11c3384c15abaac0e22d6c4ac49a8170e954811534a42084f875a7cf0e80f`  
		Last Modified: Fri, 19 Jun 2026 01:13:36 GMT  
		Size: 136.5 MB (136500477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9fc928349304d575f19e26e4713c0e9ab4159bb13cefa8129dfb1c2abe8c9`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:90772d8f5ad2144b3fd5499450aef23a8660776d73b8b19cea04fe1651c939bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22743715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e522b78fef8fb25982c60655ba79d5417bce136c92ebf23b45b6a4d34217a4a8`

```dockerfile
```

-	Layers:
	-	`sha256:1b42c20d4c4fa30bb56ce45aed546a5a99637193ba5bba1b55abf2a01929418f`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 22.7 MB (22728132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64aa8640d790d8ad8db5e3d7c98d44f716d6b4b4143b3c9ec0b11c786d023141`  
		Last Modified: Fri, 19 Jun 2026 01:13:32 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-core-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:04207016a6ef92ae044c153be5feef75fb6ad5b50f248b174250aacc2b6718d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181062230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab98f50882aebd1ebd543911a236c82fc8cb6288ca9dd6a353b903910e62f6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.9196.tar --tag 26.04
# Wed, 10 Jun 2026 03:33:02 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.entrypoint --clear=config.cmd
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.cmd --config.cmd /bin/bash
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --config.env PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=config.labels --config.label org.opencontainers.image.version=26.04 --config.label org.opencontainers.image.title=ubuntu --config.label org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --config.label org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci config --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 --clear=manifest.annotations --manifest.annotation org.opencontainers.image.version=26.04 --manifest.annotation org.opencontainers.image.title=ubuntu --manifest.annotation org.opencontainers.image.created=2026-06-10T03:33:03.035505+00:00 --manifest.annotation org.opencontainers.image.description=The Ubuntu container image maintained by Canonical

Ubuntu is a Debian-based Linux operating system that runs from the desktop to the cloud, to all your internet connected things.
It is the world's most popular operating system across public clouds and OpenStack clouds.
It is the number one platform for containers; from Docker to Kubernetes to LXD, Ubuntu can run your containers at scale.
Fast, secure and simple, Ubuntu powers millions of PCs worldwide.

# Wed, 10 Jun 2026 03:33:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-79fcbede9d5522fcffb04b46daf93b5a/images/.temp_layer.control_data.9196.tar
# Fri, 19 Jun 2026 01:11:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:11:57 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.resolute_all.deb     && echo "a275b9b819874e745a928e83e39c429fa4d607159285c4ef3ebcf75afa732ee3 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
ENV LANG=C.UTF-8
# Fri, 19 Jun 2026 01:12:55 GMT
ENV LC_ALL=C.UTF-8
# Fri, 19 Jun 2026 01:12:55 GMT
ENV ROS_DISTRO=lyrical
# Fri, 19 Jun 2026 01:12:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 19 Jun 2026 01:12:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 19 Jun 2026 01:12:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c572f291b2a0cc05a1d523f3dda4d3f1992c3e480debf2e1bc9278aeab115625`  
		Last Modified: Wed, 10 Jun 2026 08:00:25 GMT  
		Size: 40.7 MB (40709186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dda33820b52cf93fd5ff3808c770af252cf0565784b42e52e3dd74e2ebf5b2`  
		Last Modified: Wed, 10 Jun 2026 08:00:29 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4986530f0d3c75ff7820390034f5d3e027407a16c974996b5ded332599d708`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 740.9 KB (740883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65791f49907d0570d76708a6b7fff49950ae25a376454d38f6777a932bacdfb`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 9.6 MB (9605840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0681652efa697f65008a0c4209e2155b9e5cf57e320f77ceba5d9443b4cbd283`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 90.0 KB (89997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b374f8a21b565bdf721c78327461dd298e6749b9b13b05d9f6cabfb073f7bc`  
		Last Modified: Fri, 19 Jun 2026 01:13:37 GMT  
		Size: 129.9 MB (129915744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da7d04141ffff77c744942b698c8f9e8a3641e745c138843a6922858ad57b69`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:6c584cb629c967825549a27f4bf7796a017f86f36d060821e08ca9e2861e2837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22716532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06e5e7c60935235d68affcba56428c89dfbbfb17c0560e188c8501a30b67112`

```dockerfile
```

-	Layers:
	-	`sha256:50cb1dd67369a2a06012835610c6f712223ecc272a3c36f568bb50701aafcf7a`  
		Last Modified: Fri, 19 Jun 2026 01:13:35 GMT  
		Size: 22.7 MB (22700824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593bef670fc1f1f878df6670a546fec072d19ffe49f9796464d07b1941099d0e`  
		Last Modified: Fri, 19 Jun 2026 01:13:34 GMT  
		Size: 15.7 KB (15708 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:03b21c7e02310c36ee67989187b761b650208ea92eca94845d26c1bb75d8ab5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:e739313b7d2fb1ababd2d333fcdaa84448209b4a3ad36787ac2e6ffab04f7d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312088168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4aab199b4141ca03f141b6644020bab6c2223e12fdbda6c8ccda5736d27363`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:54 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:15:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f800b8b948e2673ed8a226bf87790ce00fed571ccb6c4b173a0cabcca72ffb`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 684.1 KB (684097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1a9e9cde4587bd6cf0f5b0fabcf7d3189d45eccf2f222d367ab918b3546d4`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 6.8 MB (6752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56d831ad55abb49cb53e65cfd1ad9fd5d4fba9814b9ac9e993e50f908fb4da`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 94.3 KB (94255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade12bd0c8da06f9f8cffd3821b01ad33941d8191f1c43b9e32d410c172f35fd`  
		Last Modified: Tue, 02 Jun 2026 08:22:26 GMT  
		Size: 136.3 MB (136275173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36b877151687a62b70993e03d67da073122fab5b4b321e63db93e2c5edbb8`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd736e314821ca6bc39a29747a5901b7a4af9de87fb942b611e0eeb21b5855d`  
		Last Modified: Tue, 02 Jun 2026 09:15:57 GMT  
		Size: 110.2 MB (110198452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3b1b218c3c81f3b6bc9604076e4bd565ec55459d589870fb537c3af1bdaf51`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 375.5 KB (375530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fac4062e9505018fab524f3cb6f79a11f076f20fe34b6b7d2ee7573afc44551`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a696c577f262fe36d1b033fc3f465aad16d27f2e23aa7448c628ee5d60043`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 28.0 MB (27972755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:6896fdacf0d2ed99c41465e01a2b9663fc1dbe8b67478bb20996eee99c71b021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25802586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61545d37d677be67efd0aa52a4a770e60dbcbf3c0b2c0eccbf5287805c6f2c7c`

```dockerfile
```

-	Layers:
	-	`sha256:c18f77d29bb3b6f7ef6442d42c08ab1aea1c0fc3796da25a61a1219225453ab2`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 25.8 MB (25786221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0309052d34ad4f0de264afd8c42f98e496616d63fe0f4294f92430ebbf301f`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6db8780587ca47c71f3f865077964e095c8cd49199fc02bb153484457d3a0c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (299989403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf4c9099568efccdcdf9ce529975fb469621983c0f9878105e51db2bb9ba730`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:29 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c406762b81207255596e095cf975ba8240b31d52ee968dcc75f4c880d0502f`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 684.2 KB (684226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9fba424e9faebc1fe6f68dd31bd1d59510a0e267a489cc349d57160dc34e1`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 6.8 MB (6765708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8afafd31ec8c2a476944df80ebf75303ef613b85a1c437fcaefdca4a63062`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 94.3 KB (94344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcd5fc4c1de0dd8f6a5aa0049688a282ae87bc3d8662fc8c7c043e9a20701a`  
		Last Modified: Tue, 02 Jun 2026 08:23:03 GMT  
		Size: 130.5 MB (130503862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7c1cb0e994f3341efba4e27156f34adb46f0efbda2c5ce962c0235a4f7a3`  
		Last Modified: Tue, 02 Jun 2026 08:23:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839ccbd60cd31fb7491524fb550bd15c57e5c7487e9e85fe75dca92838d1362`  
		Last Modified: Tue, 02 Jun 2026 09:24:31 GMT  
		Size: 105.6 MB (105612317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408525ea7965dba176c91032bc80beea1aae6417206f14d57e6bf0420ed93d88`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 375.5 KB (375527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f00ad1e48967daefe8d637096d70964af44fa44de59419ac56ab3e54eb48bf7`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997608089522005e479a4c0a53a53e6d8e975347849eadd7f98e57f76c100066`  
		Last Modified: Tue, 02 Jun 2026 09:24:29 GMT  
		Size: 27.1 MB (27074294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:bea2e9bc3c8dd4630f03bc02e7231bdf379122020b132bd7c631c65d903a1bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25825186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f70f9e2b593a0a58973922a8bfd23e60a442988a0e8bbad08d6a949f0894cd`

```dockerfile
```

-	Layers:
	-	`sha256:58debcdc1f44dea30a1bfff9a3d47cb8e226d66a8dd5bf6db5f6025f594f1592`  
		Last Modified: Tue, 02 Jun 2026 09:24:30 GMT  
		Size: 25.8 MB (25808685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff13e2379f5b668bcc731262f9ee6f02e993eb3505523741b9d0a608a8e328c`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 16.5 KB (16501 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:bc2b66a6b3694342fdb3d2190bd177e64246d1230451bdea0f755b9f8e3b4aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:f1b0743fb61ffd9855b5754ad20f9a8c383968540bb9530aeb89e3099da85a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1097074076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e272916a7f18110877463cb7d689674cece7253a95639e319d8c70b539c6710`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:54 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:15:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:18:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f800b8b948e2673ed8a226bf87790ce00fed571ccb6c4b173a0cabcca72ffb`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 684.1 KB (684097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1a9e9cde4587bd6cf0f5b0fabcf7d3189d45eccf2f222d367ab918b3546d4`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 6.8 MB (6752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56d831ad55abb49cb53e65cfd1ad9fd5d4fba9814b9ac9e993e50f908fb4da`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 94.3 KB (94255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade12bd0c8da06f9f8cffd3821b01ad33941d8191f1c43b9e32d410c172f35fd`  
		Last Modified: Tue, 02 Jun 2026 08:22:26 GMT  
		Size: 136.3 MB (136275173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36b877151687a62b70993e03d67da073122fab5b4b321e63db93e2c5edbb8`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd736e314821ca6bc39a29747a5901b7a4af9de87fb942b611e0eeb21b5855d`  
		Last Modified: Tue, 02 Jun 2026 09:15:57 GMT  
		Size: 110.2 MB (110198452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3b1b218c3c81f3b6bc9604076e4bd565ec55459d589870fb537c3af1bdaf51`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 375.5 KB (375530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fac4062e9505018fab524f3cb6f79a11f076f20fe34b6b7d2ee7573afc44551`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a696c577f262fe36d1b033fc3f465aad16d27f2e23aa7448c628ee5d60043`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 28.0 MB (27972755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f52f1fc65b742ea6467b319f1e26ef6baa33b5d627f2e71ca5e0fc3df40399`  
		Last Modified: Tue, 02 Jun 2026 10:21:29 GMT  
		Size: 785.0 MB (784985908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:4d866617f63dba25ab2e59589373c8c95a63a8ef93daa176c812a847146a0965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62001217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf3f39c292ad065810fdd916c893d4650a8aeafc66c9b29e5f6120aa9dc58c5`

```dockerfile
```

-	Layers:
	-	`sha256:2a413eacac16155396f5c8625ec4200d78c227cee0a45ed37b41c4244a36cbcf`  
		Last Modified: Tue, 02 Jun 2026 10:21:15 GMT  
		Size: 62.0 MB (61991856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddde8e6390032bba8f86ffb5fe4e146d8dbf5366113ca674146934bbc12f7197`  
		Last Modified: Tue, 02 Jun 2026 10:21:13 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bad9e79fb2cbcaf7f53918b8b1bbc137331a7b0eecaa4dfa0474aeab5bc20466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **999.0 MB (999046831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91b104156784613163df70793d325052fcb8c3a29da8b9986d2e520ae3e553d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:29 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c406762b81207255596e095cf975ba8240b31d52ee968dcc75f4c880d0502f`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 684.2 KB (684226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9fba424e9faebc1fe6f68dd31bd1d59510a0e267a489cc349d57160dc34e1`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 6.8 MB (6765708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8afafd31ec8c2a476944df80ebf75303ef613b85a1c437fcaefdca4a63062`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 94.3 KB (94344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcd5fc4c1de0dd8f6a5aa0049688a282ae87bc3d8662fc8c7c043e9a20701a`  
		Last Modified: Tue, 02 Jun 2026 08:23:03 GMT  
		Size: 130.5 MB (130503862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7c1cb0e994f3341efba4e27156f34adb46f0efbda2c5ce962c0235a4f7a3`  
		Last Modified: Tue, 02 Jun 2026 08:23:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839ccbd60cd31fb7491524fb550bd15c57e5c7487e9e85fe75dca92838d1362`  
		Last Modified: Tue, 02 Jun 2026 09:24:31 GMT  
		Size: 105.6 MB (105612317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408525ea7965dba176c91032bc80beea1aae6417206f14d57e6bf0420ed93d88`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 375.5 KB (375527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f00ad1e48967daefe8d637096d70964af44fa44de59419ac56ab3e54eb48bf7`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997608089522005e479a4c0a53a53e6d8e975347849eadd7f98e57f76c100066`  
		Last Modified: Tue, 02 Jun 2026 09:24:29 GMT  
		Size: 27.1 MB (27074294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85be6d70f44bad3511541dabf046edcf2f204b5b4faaac2b2c31573b2168705c`  
		Last Modified: Tue, 02 Jun 2026 10:17:45 GMT  
		Size: 699.1 MB (699057428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:fe6a69401efbc91ab497bcc79b9bf3b02b275ce13587d2b3eeb5f50240c57ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61932025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e03f6a64d52e42d51414d0a82d65ba94b91ff3a9d9e9966035c043f029733e`

```dockerfile
```

-	Layers:
	-	`sha256:0d5874db2ea2182eb2d18f0e3f894586dfd29b072b374f4d0589e5ef799814e6`  
		Last Modified: Tue, 02 Jun 2026 10:17:31 GMT  
		Size: 61.9 MB (61922584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e5817acfdef624d182bacfbf40158bb2f4d275f63541ef8634620c390f237b`  
		Last Modified: Tue, 02 Jun 2026 10:17:28 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:bc2b66a6b3694342fdb3d2190bd177e64246d1230451bdea0f755b9f8e3b4aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:f1b0743fb61ffd9855b5754ad20f9a8c383968540bb9530aeb89e3099da85a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1097074076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e272916a7f18110877463cb7d689674cece7253a95639e319d8c70b539c6710`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:54 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:15:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:18:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f800b8b948e2673ed8a226bf87790ce00fed571ccb6c4b173a0cabcca72ffb`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 684.1 KB (684097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1a9e9cde4587bd6cf0f5b0fabcf7d3189d45eccf2f222d367ab918b3546d4`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 6.8 MB (6752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56d831ad55abb49cb53e65cfd1ad9fd5d4fba9814b9ac9e993e50f908fb4da`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 94.3 KB (94255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade12bd0c8da06f9f8cffd3821b01ad33941d8191f1c43b9e32d410c172f35fd`  
		Last Modified: Tue, 02 Jun 2026 08:22:26 GMT  
		Size: 136.3 MB (136275173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36b877151687a62b70993e03d67da073122fab5b4b321e63db93e2c5edbb8`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd736e314821ca6bc39a29747a5901b7a4af9de87fb942b611e0eeb21b5855d`  
		Last Modified: Tue, 02 Jun 2026 09:15:57 GMT  
		Size: 110.2 MB (110198452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3b1b218c3c81f3b6bc9604076e4bd565ec55459d589870fb537c3af1bdaf51`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 375.5 KB (375530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fac4062e9505018fab524f3cb6f79a11f076f20fe34b6b7d2ee7573afc44551`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a696c577f262fe36d1b033fc3f465aad16d27f2e23aa7448c628ee5d60043`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 28.0 MB (27972755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f52f1fc65b742ea6467b319f1e26ef6baa33b5d627f2e71ca5e0fc3df40399`  
		Last Modified: Tue, 02 Jun 2026 10:21:29 GMT  
		Size: 785.0 MB (784985908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4d866617f63dba25ab2e59589373c8c95a63a8ef93daa176c812a847146a0965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62001217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf3f39c292ad065810fdd916c893d4650a8aeafc66c9b29e5f6120aa9dc58c5`

```dockerfile
```

-	Layers:
	-	`sha256:2a413eacac16155396f5c8625ec4200d78c227cee0a45ed37b41c4244a36cbcf`  
		Last Modified: Tue, 02 Jun 2026 10:21:15 GMT  
		Size: 62.0 MB (61991856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddde8e6390032bba8f86ffb5fe4e146d8dbf5366113ca674146934bbc12f7197`  
		Last Modified: Tue, 02 Jun 2026 10:21:13 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bad9e79fb2cbcaf7f53918b8b1bbc137331a7b0eecaa4dfa0474aeab5bc20466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **999.0 MB (999046831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91b104156784613163df70793d325052fcb8c3a29da8b9986d2e520ae3e553d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:29 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:14:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c406762b81207255596e095cf975ba8240b31d52ee968dcc75f4c880d0502f`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 684.2 KB (684226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9fba424e9faebc1fe6f68dd31bd1d59510a0e267a489cc349d57160dc34e1`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 6.8 MB (6765708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8afafd31ec8c2a476944df80ebf75303ef613b85a1c437fcaefdca4a63062`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 94.3 KB (94344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcd5fc4c1de0dd8f6a5aa0049688a282ae87bc3d8662fc8c7c043e9a20701a`  
		Last Modified: Tue, 02 Jun 2026 08:23:03 GMT  
		Size: 130.5 MB (130503862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7c1cb0e994f3341efba4e27156f34adb46f0efbda2c5ce962c0235a4f7a3`  
		Last Modified: Tue, 02 Jun 2026 08:23:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839ccbd60cd31fb7491524fb550bd15c57e5c7487e9e85fe75dca92838d1362`  
		Last Modified: Tue, 02 Jun 2026 09:24:31 GMT  
		Size: 105.6 MB (105612317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408525ea7965dba176c91032bc80beea1aae6417206f14d57e6bf0420ed93d88`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 375.5 KB (375527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f00ad1e48967daefe8d637096d70964af44fa44de59419ac56ab3e54eb48bf7`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997608089522005e479a4c0a53a53e6d8e975347849eadd7f98e57f76c100066`  
		Last Modified: Tue, 02 Jun 2026 09:24:29 GMT  
		Size: 27.1 MB (27074294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85be6d70f44bad3511541dabf046edcf2f204b5b4faaac2b2c31573b2168705c`  
		Last Modified: Tue, 02 Jun 2026 10:17:45 GMT  
		Size: 699.1 MB (699057428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fe6a69401efbc91ab497bcc79b9bf3b02b275ce13587d2b3eeb5f50240c57ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61932025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e03f6a64d52e42d51414d0a82d65ba94b91ff3a9d9e9966035c043f029733e`

```dockerfile
```

-	Layers:
	-	`sha256:0d5874db2ea2182eb2d18f0e3f894586dfd29b072b374f4d0589e5ef799814e6`  
		Last Modified: Tue, 02 Jun 2026 10:17:31 GMT  
		Size: 61.9 MB (61922584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e5817acfdef624d182bacfbf40158bb2f4d275f63541ef8634620c390f237b`  
		Last Modified: Tue, 02 Jun 2026 10:17:28 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:03b21c7e02310c36ee67989187b761b650208ea92eca94845d26c1bb75d8ab5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e739313b7d2fb1ababd2d333fcdaa84448209b4a3ad36787ac2e6ffab04f7d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312088168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4aab199b4141ca03f141b6644020bab6c2223e12fdbda6c8ccda5736d27363`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:54 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:15:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f800b8b948e2673ed8a226bf87790ce00fed571ccb6c4b173a0cabcca72ffb`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 684.1 KB (684097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1a9e9cde4587bd6cf0f5b0fabcf7d3189d45eccf2f222d367ab918b3546d4`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 6.8 MB (6752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56d831ad55abb49cb53e65cfd1ad9fd5d4fba9814b9ac9e993e50f908fb4da`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 94.3 KB (94255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade12bd0c8da06f9f8cffd3821b01ad33941d8191f1c43b9e32d410c172f35fd`  
		Last Modified: Tue, 02 Jun 2026 08:22:26 GMT  
		Size: 136.3 MB (136275173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36b877151687a62b70993e03d67da073122fab5b4b321e63db93e2c5edbb8`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd736e314821ca6bc39a29747a5901b7a4af9de87fb942b611e0eeb21b5855d`  
		Last Modified: Tue, 02 Jun 2026 09:15:57 GMT  
		Size: 110.2 MB (110198452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3b1b218c3c81f3b6bc9604076e4bd565ec55459d589870fb537c3af1bdaf51`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 375.5 KB (375530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fac4062e9505018fab524f3cb6f79a11f076f20fe34b6b7d2ee7573afc44551`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a696c577f262fe36d1b033fc3f465aad16d27f2e23aa7448c628ee5d60043`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 28.0 MB (27972755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6896fdacf0d2ed99c41465e01a2b9663fc1dbe8b67478bb20996eee99c71b021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25802586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61545d37d677be67efd0aa52a4a770e60dbcbf3c0b2c0eccbf5287805c6f2c7c`

```dockerfile
```

-	Layers:
	-	`sha256:c18f77d29bb3b6f7ef6442d42c08ab1aea1c0fc3796da25a61a1219225453ab2`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 25.8 MB (25786221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0309052d34ad4f0de264afd8c42f98e496616d63fe0f4294f92430ebbf301f`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6db8780587ca47c71f3f865077964e095c8cd49199fc02bb153484457d3a0c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (299989403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf4c9099568efccdcdf9ce529975fb469621983c0f9878105e51db2bb9ba730`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:29 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c406762b81207255596e095cf975ba8240b31d52ee968dcc75f4c880d0502f`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 684.2 KB (684226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9fba424e9faebc1fe6f68dd31bd1d59510a0e267a489cc349d57160dc34e1`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 6.8 MB (6765708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8afafd31ec8c2a476944df80ebf75303ef613b85a1c437fcaefdca4a63062`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 94.3 KB (94344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcd5fc4c1de0dd8f6a5aa0049688a282ae87bc3d8662fc8c7c043e9a20701a`  
		Last Modified: Tue, 02 Jun 2026 08:23:03 GMT  
		Size: 130.5 MB (130503862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7c1cb0e994f3341efba4e27156f34adb46f0efbda2c5ce962c0235a4f7a3`  
		Last Modified: Tue, 02 Jun 2026 08:23:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839ccbd60cd31fb7491524fb550bd15c57e5c7487e9e85fe75dca92838d1362`  
		Last Modified: Tue, 02 Jun 2026 09:24:31 GMT  
		Size: 105.6 MB (105612317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408525ea7965dba176c91032bc80beea1aae6417206f14d57e6bf0420ed93d88`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 375.5 KB (375527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f00ad1e48967daefe8d637096d70964af44fa44de59419ac56ab3e54eb48bf7`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997608089522005e479a4c0a53a53e6d8e975347849eadd7f98e57f76c100066`  
		Last Modified: Tue, 02 Jun 2026 09:24:29 GMT  
		Size: 27.1 MB (27074294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:bea2e9bc3c8dd4630f03bc02e7231bdf379122020b132bd7c631c65d903a1bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25825186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f70f9e2b593a0a58973922a8bfd23e60a442988a0e8bbad08d6a949f0894cd`

```dockerfile
```

-	Layers:
	-	`sha256:58debcdc1f44dea30a1bfff9a3d47cb8e226d66a8dd5bf6db5f6025f594f1592`  
		Last Modified: Tue, 02 Jun 2026 09:24:30 GMT  
		Size: 25.8 MB (25808685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff13e2379f5b668bcc731262f9ee6f02e993eb3505523741b9d0a608a8e328c`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 16.5 KB (16501 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:03b21c7e02310c36ee67989187b761b650208ea92eca94845d26c1bb75d8ab5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:e739313b7d2fb1ababd2d333fcdaa84448209b4a3ad36787ac2e6ffab04f7d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312088168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4aab199b4141ca03f141b6644020bab6c2223e12fdbda6c8ccda5736d27363`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:54 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:15:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f800b8b948e2673ed8a226bf87790ce00fed571ccb6c4b173a0cabcca72ffb`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 684.1 KB (684097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1a9e9cde4587bd6cf0f5b0fabcf7d3189d45eccf2f222d367ab918b3546d4`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 6.8 MB (6752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56d831ad55abb49cb53e65cfd1ad9fd5d4fba9814b9ac9e993e50f908fb4da`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 94.3 KB (94255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade12bd0c8da06f9f8cffd3821b01ad33941d8191f1c43b9e32d410c172f35fd`  
		Last Modified: Tue, 02 Jun 2026 08:22:26 GMT  
		Size: 136.3 MB (136275173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36b877151687a62b70993e03d67da073122fab5b4b321e63db93e2c5edbb8`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd736e314821ca6bc39a29747a5901b7a4af9de87fb942b611e0eeb21b5855d`  
		Last Modified: Tue, 02 Jun 2026 09:15:57 GMT  
		Size: 110.2 MB (110198452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3b1b218c3c81f3b6bc9604076e4bd565ec55459d589870fb537c3af1bdaf51`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 375.5 KB (375530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fac4062e9505018fab524f3cb6f79a11f076f20fe34b6b7d2ee7573afc44551`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a696c577f262fe36d1b033fc3f465aad16d27f2e23aa7448c628ee5d60043`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 28.0 MB (27972755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6896fdacf0d2ed99c41465e01a2b9663fc1dbe8b67478bb20996eee99c71b021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25802586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61545d37d677be67efd0aa52a4a770e60dbcbf3c0b2c0eccbf5287805c6f2c7c`

```dockerfile
```

-	Layers:
	-	`sha256:c18f77d29bb3b6f7ef6442d42c08ab1aea1c0fc3796da25a61a1219225453ab2`  
		Last Modified: Tue, 02 Jun 2026 09:15:55 GMT  
		Size: 25.8 MB (25786221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0309052d34ad4f0de264afd8c42f98e496616d63fe0f4294f92430ebbf301f`  
		Last Modified: Tue, 02 Jun 2026 09:15:53 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6db8780587ca47c71f3f865077964e095c8cd49199fc02bb153484457d3a0c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (299989403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf4c9099568efccdcdf9ce529975fb469621983c0f9878105e51db2bb9ba730`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:29 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c406762b81207255596e095cf975ba8240b31d52ee968dcc75f4c880d0502f`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 684.2 KB (684226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9fba424e9faebc1fe6f68dd31bd1d59510a0e267a489cc349d57160dc34e1`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 6.8 MB (6765708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8afafd31ec8c2a476944df80ebf75303ef613b85a1c437fcaefdca4a63062`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 94.3 KB (94344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcd5fc4c1de0dd8f6a5aa0049688a282ae87bc3d8662fc8c7c043e9a20701a`  
		Last Modified: Tue, 02 Jun 2026 08:23:03 GMT  
		Size: 130.5 MB (130503862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7c1cb0e994f3341efba4e27156f34adb46f0efbda2c5ce962c0235a4f7a3`  
		Last Modified: Tue, 02 Jun 2026 08:23:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839ccbd60cd31fb7491524fb550bd15c57e5c7487e9e85fe75dca92838d1362`  
		Last Modified: Tue, 02 Jun 2026 09:24:31 GMT  
		Size: 105.6 MB (105612317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408525ea7965dba176c91032bc80beea1aae6417206f14d57e6bf0420ed93d88`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 375.5 KB (375527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f00ad1e48967daefe8d637096d70964af44fa44de59419ac56ab3e54eb48bf7`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997608089522005e479a4c0a53a53e6d8e975347849eadd7f98e57f76c100066`  
		Last Modified: Tue, 02 Jun 2026 09:24:29 GMT  
		Size: 27.1 MB (27074294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:bea2e9bc3c8dd4630f03bc02e7231bdf379122020b132bd7c631c65d903a1bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25825186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f70f9e2b593a0a58973922a8bfd23e60a442988a0e8bbad08d6a949f0894cd`

```dockerfile
```

-	Layers:
	-	`sha256:58debcdc1f44dea30a1bfff9a3d47cb8e226d66a8dd5bf6db5f6025f594f1592`  
		Last Modified: Tue, 02 Jun 2026 09:24:30 GMT  
		Size: 25.8 MB (25808685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff13e2379f5b668bcc731262f9ee6f02e993eb3505523741b9d0a608a8e328c`  
		Last Modified: Tue, 02 Jun 2026 09:24:28 GMT  
		Size: 16.5 KB (16501 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:aa3ab3073d7177076615213f10b652627c6d00fbdb0d2da9bcc27ac7c90fa98a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c6b5b6f1c66aebbacbc5c353e81015bc57dadbd5d475fb104d776ee4116c7b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173538927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4875753e5835c960a46aef181ea2128b03e417965dcba92dad6f77272cf77553`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f800b8b948e2673ed8a226bf87790ce00fed571ccb6c4b173a0cabcca72ffb`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 684.1 KB (684097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1a9e9cde4587bd6cf0f5b0fabcf7d3189d45eccf2f222d367ab918b3546d4`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 6.8 MB (6752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56d831ad55abb49cb53e65cfd1ad9fd5d4fba9814b9ac9e993e50f908fb4da`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 94.3 KB (94255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade12bd0c8da06f9f8cffd3821b01ad33941d8191f1c43b9e32d410c172f35fd`  
		Last Modified: Tue, 02 Jun 2026 08:22:26 GMT  
		Size: 136.3 MB (136275173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36b877151687a62b70993e03d67da073122fab5b4b321e63db93e2c5edbb8`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:d4f68316c56c147462afa7bf298b00ca522168bb13eec158acb81bb8fead26f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19552455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be959f2f4be6a2822447a1135ed4c269cd412660c8fd7a054688aa3196483c`

```dockerfile
```

-	Layers:
	-	`sha256:f15e97baa0d7e5608b7f0d05529776e537cf01a674edb3c07271e48009d8685f`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 19.5 MB (19537834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dddafaab1c7897d4058001a906c1601b50b7819f87b8a3a1a75961adc0d3ec3b`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:de1b758c206e05882d575665a5f0dffcef987389fa1f6c3a6c2f2b3880955590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166924741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd92305ff7d2f376f1cf94fe2e09513ff68c3e29a29cc96b41642df2f5972d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c406762b81207255596e095cf975ba8240b31d52ee968dcc75f4c880d0502f`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 684.2 KB (684226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9fba424e9faebc1fe6f68dd31bd1d59510a0e267a489cc349d57160dc34e1`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 6.8 MB (6765708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8afafd31ec8c2a476944df80ebf75303ef613b85a1c437fcaefdca4a63062`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 94.3 KB (94344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcd5fc4c1de0dd8f6a5aa0049688a282ae87bc3d8662fc8c7c043e9a20701a`  
		Last Modified: Tue, 02 Jun 2026 08:23:03 GMT  
		Size: 130.5 MB (130503862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7c1cb0e994f3341efba4e27156f34adb46f0efbda2c5ce962c0235a4f7a3`  
		Last Modified: Tue, 02 Jun 2026 08:23:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:db3fb153c03aeca727af415fa3ff6fbb4811a249ce800fe942fa6b9a51ce7fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19526797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d42897f458d7fa6bc0ef2ddcacbd4919d5729988df8aa7c3b88fa0f9061bc4d`

```dockerfile
```

-	Layers:
	-	`sha256:dadfbd9b89532e46b66a4dc7677f0e98ae95435671bc86c9075c0d27146cfde6`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 19.5 MB (19512050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9176903f26887f1209af2993320caf7a750a657e7cc5b48ad683d1277cd2050`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:aa3ab3073d7177076615213f10b652627c6d00fbdb0d2da9bcc27ac7c90fa98a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c6b5b6f1c66aebbacbc5c353e81015bc57dadbd5d475fb104d776ee4116c7b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173538927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4875753e5835c960a46aef181ea2128b03e417965dcba92dad6f77272cf77553`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:54 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f800b8b948e2673ed8a226bf87790ce00fed571ccb6c4b173a0cabcca72ffb`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 684.1 KB (684097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb1a9e9cde4587bd6cf0f5b0fabcf7d3189d45eccf2f222d367ab918b3546d4`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 6.8 MB (6752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56d831ad55abb49cb53e65cfd1ad9fd5d4fba9814b9ac9e993e50f908fb4da`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 94.3 KB (94255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade12bd0c8da06f9f8cffd3821b01ad33941d8191f1c43b9e32d410c172f35fd`  
		Last Modified: Tue, 02 Jun 2026 08:22:26 GMT  
		Size: 136.3 MB (136275173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a36b877151687a62b70993e03d67da073122fab5b4b321e63db93e2c5edbb8`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d4f68316c56c147462afa7bf298b00ca522168bb13eec158acb81bb8fead26f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19552455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be959f2f4be6a2822447a1135ed4c269cd412660c8fd7a054688aa3196483c`

```dockerfile
```

-	Layers:
	-	`sha256:f15e97baa0d7e5608b7f0d05529776e537cf01a674edb3c07271e48009d8685f`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 19.5 MB (19537834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dddafaab1c7897d4058001a906c1601b50b7819f87b8a3a1a75961adc0d3ec3b`  
		Last Modified: Tue, 02 Jun 2026 08:22:23 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:de1b758c206e05882d575665a5f0dffcef987389fa1f6c3a6c2f2b3880955590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166924741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd92305ff7d2f376f1cf94fe2e09513ff68c3e29a29cc96b41642df2f5972d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Jun 2026 08:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c406762b81207255596e095cf975ba8240b31d52ee968dcc75f4c880d0502f`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 684.2 KB (684226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b9fba424e9faebc1fe6f68dd31bd1d59510a0e267a489cc349d57160dc34e1`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 6.8 MB (6765708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8afafd31ec8c2a476944df80ebf75303ef613b85a1c437fcaefdca4a63062`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 94.3 KB (94344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbcd5fc4c1de0dd8f6a5aa0049688a282ae87bc3d8662fc8c7c043e9a20701a`  
		Last Modified: Tue, 02 Jun 2026 08:23:03 GMT  
		Size: 130.5 MB (130503862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7c1cb0e994f3341efba4e27156f34adb46f0efbda2c5ce962c0235a4f7a3`  
		Last Modified: Tue, 02 Jun 2026 08:23:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:db3fb153c03aeca727af415fa3ff6fbb4811a249ce800fe942fa6b9a51ce7fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19526797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d42897f458d7fa6bc0ef2ddcacbd4919d5729988df8aa7c3b88fa0f9061bc4d`

```dockerfile
```

-	Layers:
	-	`sha256:dadfbd9b89532e46b66a4dc7677f0e98ae95435671bc86c9075c0d27146cfde6`  
		Last Modified: Tue, 02 Jun 2026 08:23:00 GMT  
		Size: 19.5 MB (19512050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9176903f26887f1209af2993320caf7a750a657e7cc5b48ad683d1277cd2050`  
		Last Modified: Tue, 02 Jun 2026 08:22:59 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json
