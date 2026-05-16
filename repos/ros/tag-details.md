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
$ docker pull ros@sha256:eac11a5285beeb1e1884e71f7091c610e08452e823bfb3f43afaa334375325f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:1c3e6fcf78d686d404a825f32902359fd898c01596b17c3354c91b8931b29e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296624907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41d5c7490a1b1f0c2395aa100b32d431ed52a0c11b293644ac2270f727b6063`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d79ab55df243721787bae594a1869e32111c3fceaedf29d6c4916281b829e3`  
		Last Modified: Mon, 11 May 2026 19:13:12 GMT  
		Size: 110.7 MB (110661006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefa18366212cb7871cc063fe2189897ae3ede04c35065e1041761e727a04552`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 414.0 KB (414006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437c42b38e5dd4ff52978453169e4760ca982ed52358da77cf1428e1d0a35dc`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626295b76a9867451fd495dd438f1ca2575ab6ec87675aebb1b6e00ab43fa94`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 28.1 MB (28068784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:d915bd300681c6e58f23127c8cc0ab1491860713c1ca865459ba1917cb50f7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24807454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2697aaa028236a6efbe85f1f380bcc63263008ca7f97d22eba6ea829b8a3f1`

```dockerfile
```

-	Layers:
	-	`sha256:66765b0ae9a51a477b76dbb9ebf1cbafb71d4eea908797708288df58da1d3eb1`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 24.8 MB (24790833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929ab4c70f88b50c8a6a4c73812d6e5917e8e1fe47d308a0c6635f4f1c80554`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c22b11ae86c58ddc90ce067c7641f3eb501f18d7808be1afb030f3cbcbbcd94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285097578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbc602fd948b667d652b3b27cd93c4d7895631148083dae39e2fbf77960f5e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:10:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:10:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:10:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ef13a8256deb85c6ab6c779a50cae10e54bde2a7710d853fbc47767a135020`  
		Last Modified: Mon, 11 May 2026 19:11:38 GMT  
		Size: 106.1 MB (106088503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e204c60f127cbe48970ee27259bf80d1c1ad40e5b4f1f7833f50fa8468c99`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 414.0 KB (414004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f824c1438b2e0ad2054bdea0f885c631c4527adf75a317d1de5d764fb90bb3`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fdcf0407801b47e4bd3f232539f37ff6b13700e812eafeb81b0ff220bd8dc`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 27.2 MB (27178247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:47dc7b5b22b38978662411b3415c57faa57c97711f1aac5c7bd58b912e5f36a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24829870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6794c54b8ba603a582971278891bd3a70adb4ca46a7cf338bdc88657bb46b96a`

```dockerfile
```

-	Layers:
	-	`sha256:536e5e23b46b254ea67818466ec32d5d9e0e63d1c8d85b502fb5d5164c5347f3`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 24.8 MB (24813100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1dacd6cdc2beafe25edc8cb9a256766663e91f4b13f94979e74972f7f090598`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:f412f8df4962e6dc579614aca091ede18fa00fb2c6059876282844fe8af07151
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:1c35184faff5565838285a9db9c6baa33a61fb91106f2f2454f6981ab334c849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081434248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b72117bb7b4047614b58ca55a535c6201414f69543bc9aa5e85b2c61e3321a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:12:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d79ab55df243721787bae594a1869e32111c3fceaedf29d6c4916281b829e3`  
		Last Modified: Mon, 11 May 2026 19:13:12 GMT  
		Size: 110.7 MB (110661006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefa18366212cb7871cc063fe2189897ae3ede04c35065e1041761e727a04552`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 414.0 KB (414006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437c42b38e5dd4ff52978453169e4760ca982ed52358da77cf1428e1d0a35dc`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626295b76a9867451fd495dd438f1ca2575ab6ec87675aebb1b6e00ab43fa94`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 28.1 MB (28068784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4640b83eb291263d8fda37113525b335f47bb0162699941f39387d29872231f`  
		Last Modified: Mon, 11 May 2026 20:15:43 GMT  
		Size: 784.8 MB (784809341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c14163a6e81b9eddee217bbb6ce1c594e914f27b550d8d0c245c6da4edd71b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60974792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3256715cc88463d3817dc1e373c747df39026a6d5aa798a014720e36717d459`

```dockerfile
```

-	Layers:
	-	`sha256:4ce51c8c5351d0d442998b7f5d0be890947450514524ed06ca47b31add780740`  
		Last Modified: Mon, 11 May 2026 20:15:27 GMT  
		Size: 61.0 MB (60965453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a2afc85dff5086683306a95832eb05bc442b8576ceb3d5001738ae0da1d008`  
		Last Modified: Mon, 11 May 2026 20:15:24 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3e802f089163d4e95e49acb9faa4305dfc514e71e6f38cb3b36ca144b2eb6994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 MB (984011579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28797e96fee39d4fe724e8459af2043c8c1843dd50295fd5765be5984a1519e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:10:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:10:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:10:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:13:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ef13a8256deb85c6ab6c779a50cae10e54bde2a7710d853fbc47767a135020`  
		Last Modified: Mon, 11 May 2026 19:11:38 GMT  
		Size: 106.1 MB (106088503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e204c60f127cbe48970ee27259bf80d1c1ad40e5b4f1f7833f50fa8468c99`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 414.0 KB (414004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f824c1438b2e0ad2054bdea0f885c631c4527adf75a317d1de5d764fb90bb3`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fdcf0407801b47e4bd3f232539f37ff6b13700e812eafeb81b0ff220bd8dc`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 27.2 MB (27178247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755f8136493ff290781635874e2968eeeef4de3189dc6d5cac9f7a92ee0e034d`  
		Last Modified: Mon, 11 May 2026 20:16:47 GMT  
		Size: 698.9 MB (698914001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:b02f59c72098e60762aa33da5a2422e0e55bd8b146f105ec1365b821223c0e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60905387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c537faebae8884066db5476f9c9bb5c099c14d30fe8e1224d90c3ba3fc40092a`

```dockerfile
```

-	Layers:
	-	`sha256:87156aef9397e47eeff8049980d0816f33f14a8b252978de1592b020c9e6d988`  
		Last Modified: Mon, 11 May 2026 20:16:34 GMT  
		Size: 60.9 MB (60895968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45385e82a599ca93889539a95c402fa1ef8ea8f8be54b282ada5cda17a2f60be`  
		Last Modified: Mon, 11 May 2026 20:16:31 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:f412f8df4962e6dc579614aca091ede18fa00fb2c6059876282844fe8af07151
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:1c35184faff5565838285a9db9c6baa33a61fb91106f2f2454f6981ab334c849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081434248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b72117bb7b4047614b58ca55a535c6201414f69543bc9aa5e85b2c61e3321a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:12:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d79ab55df243721787bae594a1869e32111c3fceaedf29d6c4916281b829e3`  
		Last Modified: Mon, 11 May 2026 19:13:12 GMT  
		Size: 110.7 MB (110661006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefa18366212cb7871cc063fe2189897ae3ede04c35065e1041761e727a04552`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 414.0 KB (414006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437c42b38e5dd4ff52978453169e4760ca982ed52358da77cf1428e1d0a35dc`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626295b76a9867451fd495dd438f1ca2575ab6ec87675aebb1b6e00ab43fa94`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 28.1 MB (28068784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4640b83eb291263d8fda37113525b335f47bb0162699941f39387d29872231f`  
		Last Modified: Mon, 11 May 2026 20:15:43 GMT  
		Size: 784.8 MB (784809341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c14163a6e81b9eddee217bbb6ce1c594e914f27b550d8d0c245c6da4edd71b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60974792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3256715cc88463d3817dc1e373c747df39026a6d5aa798a014720e36717d459`

```dockerfile
```

-	Layers:
	-	`sha256:4ce51c8c5351d0d442998b7f5d0be890947450514524ed06ca47b31add780740`  
		Last Modified: Mon, 11 May 2026 20:15:27 GMT  
		Size: 61.0 MB (60965453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a2afc85dff5086683306a95832eb05bc442b8576ceb3d5001738ae0da1d008`  
		Last Modified: Mon, 11 May 2026 20:15:24 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3e802f089163d4e95e49acb9faa4305dfc514e71e6f38cb3b36ca144b2eb6994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 MB (984011579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28797e96fee39d4fe724e8459af2043c8c1843dd50295fd5765be5984a1519e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:10:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:10:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:10:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:13:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ef13a8256deb85c6ab6c779a50cae10e54bde2a7710d853fbc47767a135020`  
		Last Modified: Mon, 11 May 2026 19:11:38 GMT  
		Size: 106.1 MB (106088503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e204c60f127cbe48970ee27259bf80d1c1ad40e5b4f1f7833f50fa8468c99`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 414.0 KB (414004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f824c1438b2e0ad2054bdea0f885c631c4527adf75a317d1de5d764fb90bb3`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fdcf0407801b47e4bd3f232539f37ff6b13700e812eafeb81b0ff220bd8dc`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 27.2 MB (27178247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755f8136493ff290781635874e2968eeeef4de3189dc6d5cac9f7a92ee0e034d`  
		Last Modified: Mon, 11 May 2026 20:16:47 GMT  
		Size: 698.9 MB (698914001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b02f59c72098e60762aa33da5a2422e0e55bd8b146f105ec1365b821223c0e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60905387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c537faebae8884066db5476f9c9bb5c099c14d30fe8e1224d90c3ba3fc40092a`

```dockerfile
```

-	Layers:
	-	`sha256:87156aef9397e47eeff8049980d0816f33f14a8b252978de1592b020c9e6d988`  
		Last Modified: Mon, 11 May 2026 20:16:34 GMT  
		Size: 60.9 MB (60895968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45385e82a599ca93889539a95c402fa1ef8ea8f8be54b282ada5cda17a2f60be`  
		Last Modified: Mon, 11 May 2026 20:16:31 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:eac11a5285beeb1e1884e71f7091c610e08452e823bfb3f43afaa334375325f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1c3e6fcf78d686d404a825f32902359fd898c01596b17c3354c91b8931b29e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296624907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41d5c7490a1b1f0c2395aa100b32d431ed52a0c11b293644ac2270f727b6063`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d79ab55df243721787bae594a1869e32111c3fceaedf29d6c4916281b829e3`  
		Last Modified: Mon, 11 May 2026 19:13:12 GMT  
		Size: 110.7 MB (110661006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefa18366212cb7871cc063fe2189897ae3ede04c35065e1041761e727a04552`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 414.0 KB (414006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437c42b38e5dd4ff52978453169e4760ca982ed52358da77cf1428e1d0a35dc`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626295b76a9867451fd495dd438f1ca2575ab6ec87675aebb1b6e00ab43fa94`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 28.1 MB (28068784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d915bd300681c6e58f23127c8cc0ab1491860713c1ca865459ba1917cb50f7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24807454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2697aaa028236a6efbe85f1f380bcc63263008ca7f97d22eba6ea829b8a3f1`

```dockerfile
```

-	Layers:
	-	`sha256:66765b0ae9a51a477b76dbb9ebf1cbafb71d4eea908797708288df58da1d3eb1`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 24.8 MB (24790833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929ab4c70f88b50c8a6a4c73812d6e5917e8e1fe47d308a0c6635f4f1c80554`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c22b11ae86c58ddc90ce067c7641f3eb501f18d7808be1afb030f3cbcbbcd94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285097578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbc602fd948b667d652b3b27cd93c4d7895631148083dae39e2fbf77960f5e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:10:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:10:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:10:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ef13a8256deb85c6ab6c779a50cae10e54bde2a7710d853fbc47767a135020`  
		Last Modified: Mon, 11 May 2026 19:11:38 GMT  
		Size: 106.1 MB (106088503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e204c60f127cbe48970ee27259bf80d1c1ad40e5b4f1f7833f50fa8468c99`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 414.0 KB (414004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f824c1438b2e0ad2054bdea0f885c631c4527adf75a317d1de5d764fb90bb3`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fdcf0407801b47e4bd3f232539f37ff6b13700e812eafeb81b0ff220bd8dc`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 27.2 MB (27178247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:47dc7b5b22b38978662411b3415c57faa57c97711f1aac5c7bd58b912e5f36a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24829870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6794c54b8ba603a582971278891bd3a70adb4ca46a7cf338bdc88657bb46b96a`

```dockerfile
```

-	Layers:
	-	`sha256:536e5e23b46b254ea67818466ec32d5d9e0e63d1c8d85b502fb5d5164c5347f3`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 24.8 MB (24813100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1dacd6cdc2beafe25edc8cb9a256766663e91f4b13f94979e74972f7f090598`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:eac11a5285beeb1e1884e71f7091c610e08452e823bfb3f43afaa334375325f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:1c3e6fcf78d686d404a825f32902359fd898c01596b17c3354c91b8931b29e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296624907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41d5c7490a1b1f0c2395aa100b32d431ed52a0c11b293644ac2270f727b6063`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d79ab55df243721787bae594a1869e32111c3fceaedf29d6c4916281b829e3`  
		Last Modified: Mon, 11 May 2026 19:13:12 GMT  
		Size: 110.7 MB (110661006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefa18366212cb7871cc063fe2189897ae3ede04c35065e1041761e727a04552`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 414.0 KB (414006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437c42b38e5dd4ff52978453169e4760ca982ed52358da77cf1428e1d0a35dc`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626295b76a9867451fd495dd438f1ca2575ab6ec87675aebb1b6e00ab43fa94`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 28.1 MB (28068784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d915bd300681c6e58f23127c8cc0ab1491860713c1ca865459ba1917cb50f7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24807454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2697aaa028236a6efbe85f1f380bcc63263008ca7f97d22eba6ea829b8a3f1`

```dockerfile
```

-	Layers:
	-	`sha256:66765b0ae9a51a477b76dbb9ebf1cbafb71d4eea908797708288df58da1d3eb1`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 24.8 MB (24790833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929ab4c70f88b50c8a6a4c73812d6e5917e8e1fe47d308a0c6635f4f1c80554`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c22b11ae86c58ddc90ce067c7641f3eb501f18d7808be1afb030f3cbcbbcd94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285097578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbc602fd948b667d652b3b27cd93c4d7895631148083dae39e2fbf77960f5e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:10:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:10:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:10:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ef13a8256deb85c6ab6c779a50cae10e54bde2a7710d853fbc47767a135020`  
		Last Modified: Mon, 11 May 2026 19:11:38 GMT  
		Size: 106.1 MB (106088503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e204c60f127cbe48970ee27259bf80d1c1ad40e5b4f1f7833f50fa8468c99`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 414.0 KB (414004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f824c1438b2e0ad2054bdea0f885c631c4527adf75a317d1de5d764fb90bb3`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fdcf0407801b47e4bd3f232539f37ff6b13700e812eafeb81b0ff220bd8dc`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 27.2 MB (27178247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:47dc7b5b22b38978662411b3415c57faa57c97711f1aac5c7bd58b912e5f36a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24829870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6794c54b8ba603a582971278891bd3a70adb4ca46a7cf338bdc88657bb46b96a`

```dockerfile
```

-	Layers:
	-	`sha256:536e5e23b46b254ea67818466ec32d5d9e0e63d1c8d85b502fb5d5164c5347f3`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 24.8 MB (24813100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1dacd6cdc2beafe25edc8cb9a256766663e91f4b13f94979e74972f7f090598`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:bcb227cb080b774ea58dab3d0af23168fb227d5f35104e3664c52bc1c8240051
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:0fc162ea3afb430ec3d19d5fa286b45f1f2846b5f57ff8880735e07fcec542f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157478623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d68c353f6974f34f875d2fc4bfba8ebcbefa6f8499ecb44ebed59c439d01fb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:158a72148c5a5b6f4f91aefc943c89083cc627b5a90f4184a22783246bd71f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18499978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7584a3829d92e76706b3458fa6f34d2bc24ed261c4511f312f5c2976aad92fb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a93c8abe0b8a8ba5fae670aa9d9282e23241784e183c11ae748c0e74b7a4202`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 18.5 MB (18485370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19dd046c746389d89df4cf5773cd71cc8b65051205d8eadd466cbdc5a82113a2`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b15262cd19f96863eef62ee766c93da52cc5e663e437acd14ce6fb4488a6c01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151414314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000971ca2196011fe2a8adba160fbbddba9c4d11b3b6ad4297931dffadb3c24`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:25b5e6cb76c9e746b94b69b41867ac88d0b58c3e0a753e2b52841e92f2b7dad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397d24e9dcd3d1ee6300541c483b1c17c7ccd458e9fb3cae45205719dfafc90b`

```dockerfile
```

-	Layers:
	-	`sha256:11b39afcf284a5e2ea25ed5501a44793025334f2fac0c09e493166154a1a33e1`  
		Last Modified: Mon, 11 May 2026 19:01:11 GMT  
		Size: 18.5 MB (18459376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06fe756ffee58f8ec8abc21d42291dda96fe283efbbf3cf8b89cc338827cf462`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 14.7 KB (14733 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:bcb227cb080b774ea58dab3d0af23168fb227d5f35104e3664c52bc1c8240051
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:0fc162ea3afb430ec3d19d5fa286b45f1f2846b5f57ff8880735e07fcec542f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157478623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d68c353f6974f34f875d2fc4bfba8ebcbefa6f8499ecb44ebed59c439d01fb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:158a72148c5a5b6f4f91aefc943c89083cc627b5a90f4184a22783246bd71f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18499978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7584a3829d92e76706b3458fa6f34d2bc24ed261c4511f312f5c2976aad92fb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a93c8abe0b8a8ba5fae670aa9d9282e23241784e183c11ae748c0e74b7a4202`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 18.5 MB (18485370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19dd046c746389d89df4cf5773cd71cc8b65051205d8eadd466cbdc5a82113a2`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b15262cd19f96863eef62ee766c93da52cc5e663e437acd14ce6fb4488a6c01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151414314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000971ca2196011fe2a8adba160fbbddba9c4d11b3b6ad4297931dffadb3c24`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:25b5e6cb76c9e746b94b69b41867ac88d0b58c3e0a753e2b52841e92f2b7dad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397d24e9dcd3d1ee6300541c483b1c17c7ccd458e9fb3cae45205719dfafc90b`

```dockerfile
```

-	Layers:
	-	`sha256:11b39afcf284a5e2ea25ed5501a44793025334f2fac0c09e493166154a1a33e1`  
		Last Modified: Mon, 11 May 2026 19:01:11 GMT  
		Size: 18.5 MB (18459376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06fe756ffee58f8ec8abc21d42291dda96fe283efbbf3cf8b89cc338827cf462`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 14.7 KB (14733 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:cf281fc739d5193a882ad7324e6dd03f9042de5d4c9d3d0148db7503e65c5a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:cb3d4998744a506d3f8bbaa64738ea7bfd43673112c7066a8f07f16023a1205a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297136544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f528e859b71dcab36a6045daff8d4a2e5e7ff45efb5eca098638bb666e82b27`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:13:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:14:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:14:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:14:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd392dbff6d7b6d67519ea916b13cc6925d0f92d2307dbd82948acdad262e`  
		Last Modified: Mon, 11 May 2026 19:14:56 GMT  
		Size: 110.7 MB (110663798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1181bd112c159be737e19d577fcc94d397c7a43df3b628032eba0cd6d04aaf1`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 382.2 KB (382206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b2253a336265af7d54719c96a7b7657acd02bdb998b134763b3d84a72ba52`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324873c74ee6b185565d669a1ea23f5580faf99788e41da860250d9c7599abb`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 27.9 MB (27889131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:907d5440f833628c2cd66d046da612d05b6dbaf613a36e923972b0d7ba1fca96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24756713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379d065e31e555ccd272014fd0ea8e326f2d896092d01d2f5d431390650b1185`

```dockerfile
```

-	Layers:
	-	`sha256:64dc42aa8bbf1cbd88565dee2e3b9217c3ae8ca0caa83f2eb80c839cc669fcd0`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 24.7 MB (24740366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4319d6fc7f46b8b6139c6311d8b3164aec04fae2546399cfddd86513aeb93ac3`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4b3054abbdebccaa00bebe2f1f0e6fa32055f0d7d9a5e20e5838855891011948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285553651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88425e0b22fabe9ef0564ee7133f7546f7a5f0114637c9eaf9e8e92271a91567`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27109cc6f2f4ce1d42bfbc092c0beee92d9717649e91b7bd9673e2fcbd075cbd`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 106.1 MB (106090308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522455a5a2e6e8a9311ac13057aa690b6d1ebf53c75b456e1cafc24bf8f9f27`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 382.2 KB (382192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d76cc9a9d526bd2365c7b6dc88a52aaf996f604271a069a01abc4cc2f0141`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bbcab63cba92ef478797b62881851c9f78d63434813a411a979a749f7fac07`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 27.0 MB (26997534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:345cd072abe5b9ed568306eefb47f8f69e38d46832e23a51c4ed460d74a25171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24779110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6b1efb3fdba4476ac69a6724610b446c83a91d09a3360c5d7a1b83fd0c57c2`

```dockerfile
```

-	Layers:
	-	`sha256:7b7f4139b31da0ae7c2cc84a845d28549bb57e698fe46299e796e62a398cff72`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 24.8 MB (24762626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c099573f70788522e5453ceabb26cbc497203ca0f5d27a91d955f634b003d85f`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:f10f0ca39f932a1a3a0d9320b5a553af3ba499fd9e6b316ac20ea4709a7629ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:ec16d6322313300194810b4f79bf9a7171907e45afc78a2f3b6eec96d245375d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082003503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235dfd1749dc7a25b40c277ca5b8553a9e9326a49ecef19aa5f4d0b87d03f198`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:13:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:14:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:14:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:14:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd392dbff6d7b6d67519ea916b13cc6925d0f92d2307dbd82948acdad262e`  
		Last Modified: Mon, 11 May 2026 19:14:56 GMT  
		Size: 110.7 MB (110663798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1181bd112c159be737e19d577fcc94d397c7a43df3b628032eba0cd6d04aaf1`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 382.2 KB (382206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b2253a336265af7d54719c96a7b7657acd02bdb998b134763b3d84a72ba52`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324873c74ee6b185565d669a1ea23f5580faf99788e41da860250d9c7599abb`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 27.9 MB (27889131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a8710847f07c6cec235443e0164daabd110ed01aeb7b20f3e3d93ff7904f8`  
		Last Modified: Mon, 11 May 2026 20:18:23 GMT  
		Size: 784.9 MB (784866959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:dd76c06623afe43413fcc8540211d56baa06acd2a94d6565c7728926a89b0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60933291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde38d31ed2fb10170c58e325e7c6a20ee4069de1e7ce7755c4927c022fcc950`

```dockerfile
```

-	Layers:
	-	`sha256:8a6d00c1b4470dce7c2f7e688520b0d8a2f526fa39e2ab8fb83d0545d0992f05`  
		Last Modified: Mon, 11 May 2026 20:18:08 GMT  
		Size: 60.9 MB (60923940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b7d7b496637da95284a2b0eab577946a256a2bcbe9b6f9d34074aa7e7e1239`  
		Last Modified: Mon, 11 May 2026 20:18:04 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d434861071c4ad6eda1f362305ad288a40c10577d68704cb2989068639c4639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 MB (984517104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212429b520a084e1922ecb666e3cfd89b325e308d00a7552d238b50752020703`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:16:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27109cc6f2f4ce1d42bfbc092c0beee92d9717649e91b7bd9673e2fcbd075cbd`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 106.1 MB (106090308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522455a5a2e6e8a9311ac13057aa690b6d1ebf53c75b456e1cafc24bf8f9f27`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 382.2 KB (382192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d76cc9a9d526bd2365c7b6dc88a52aaf996f604271a069a01abc4cc2f0141`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bbcab63cba92ef478797b62881851c9f78d63434813a411a979a749f7fac07`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 27.0 MB (26997534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e42a24d7148ad851d01b0f14a34e0adbe6ce1a671ebfe649f5fc69e3a4e61cc`  
		Last Modified: Mon, 11 May 2026 20:19:04 GMT  
		Size: 699.0 MB (698963453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9fff4e271c674c4ba2f760ac32dac6b529720bbe9a5e890d1e3a77fa75688b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60863892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1feaadbb76f92ca542e7a4d7100d9123dfe44f49e5f45915fd5cafb3ece86b3`

```dockerfile
```

-	Layers:
	-	`sha256:03db9e2d0a4f6ebb2b9e15398f95d336bb273e9764942dfa87fbb79ce163e996`  
		Last Modified: Mon, 11 May 2026 20:18:52 GMT  
		Size: 60.9 MB (60854460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccafddf35aeedcd1b9de7a4099e1ca2829418353116ab4243d0d9df91797e22d`  
		Last Modified: Mon, 11 May 2026 20:18:50 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:f10f0ca39f932a1a3a0d9320b5a553af3ba499fd9e6b316ac20ea4709a7629ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:ec16d6322313300194810b4f79bf9a7171907e45afc78a2f3b6eec96d245375d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082003503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235dfd1749dc7a25b40c277ca5b8553a9e9326a49ecef19aa5f4d0b87d03f198`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:13:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:14:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:14:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:14:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:15:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd392dbff6d7b6d67519ea916b13cc6925d0f92d2307dbd82948acdad262e`  
		Last Modified: Mon, 11 May 2026 19:14:56 GMT  
		Size: 110.7 MB (110663798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1181bd112c159be737e19d577fcc94d397c7a43df3b628032eba0cd6d04aaf1`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 382.2 KB (382206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b2253a336265af7d54719c96a7b7657acd02bdb998b134763b3d84a72ba52`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324873c74ee6b185565d669a1ea23f5580faf99788e41da860250d9c7599abb`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 27.9 MB (27889131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a8710847f07c6cec235443e0164daabd110ed01aeb7b20f3e3d93ff7904f8`  
		Last Modified: Mon, 11 May 2026 20:18:23 GMT  
		Size: 784.9 MB (784866959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:dd76c06623afe43413fcc8540211d56baa06acd2a94d6565c7728926a89b0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60933291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde38d31ed2fb10170c58e325e7c6a20ee4069de1e7ce7755c4927c022fcc950`

```dockerfile
```

-	Layers:
	-	`sha256:8a6d00c1b4470dce7c2f7e688520b0d8a2f526fa39e2ab8fb83d0545d0992f05`  
		Last Modified: Mon, 11 May 2026 20:18:08 GMT  
		Size: 60.9 MB (60923940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b7d7b496637da95284a2b0eab577946a256a2bcbe9b6f9d34074aa7e7e1239`  
		Last Modified: Mon, 11 May 2026 20:18:04 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d434861071c4ad6eda1f362305ad288a40c10577d68704cb2989068639c4639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 MB (984517104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212429b520a084e1922ecb666e3cfd89b325e308d00a7552d238b50752020703`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:16:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27109cc6f2f4ce1d42bfbc092c0beee92d9717649e91b7bd9673e2fcbd075cbd`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 106.1 MB (106090308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522455a5a2e6e8a9311ac13057aa690b6d1ebf53c75b456e1cafc24bf8f9f27`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 382.2 KB (382192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d76cc9a9d526bd2365c7b6dc88a52aaf996f604271a069a01abc4cc2f0141`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bbcab63cba92ef478797b62881851c9f78d63434813a411a979a749f7fac07`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 27.0 MB (26997534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e42a24d7148ad851d01b0f14a34e0adbe6ce1a671ebfe649f5fc69e3a4e61cc`  
		Last Modified: Mon, 11 May 2026 20:19:04 GMT  
		Size: 699.0 MB (698963453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9fff4e271c674c4ba2f760ac32dac6b529720bbe9a5e890d1e3a77fa75688b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60863892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1feaadbb76f92ca542e7a4d7100d9123dfe44f49e5f45915fd5cafb3ece86b3`

```dockerfile
```

-	Layers:
	-	`sha256:03db9e2d0a4f6ebb2b9e15398f95d336bb273e9764942dfa87fbb79ce163e996`  
		Last Modified: Mon, 11 May 2026 20:18:52 GMT  
		Size: 60.9 MB (60854460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccafddf35aeedcd1b9de7a4099e1ca2829418353116ab4243d0d9df91797e22d`  
		Last Modified: Mon, 11 May 2026 20:18:50 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:cf281fc739d5193a882ad7324e6dd03f9042de5d4c9d3d0148db7503e65c5a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:cb3d4998744a506d3f8bbaa64738ea7bfd43673112c7066a8f07f16023a1205a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297136544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f528e859b71dcab36a6045daff8d4a2e5e7ff45efb5eca098638bb666e82b27`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:13:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:14:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:14:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:14:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd392dbff6d7b6d67519ea916b13cc6925d0f92d2307dbd82948acdad262e`  
		Last Modified: Mon, 11 May 2026 19:14:56 GMT  
		Size: 110.7 MB (110663798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1181bd112c159be737e19d577fcc94d397c7a43df3b628032eba0cd6d04aaf1`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 382.2 KB (382206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b2253a336265af7d54719c96a7b7657acd02bdb998b134763b3d84a72ba52`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324873c74ee6b185565d669a1ea23f5580faf99788e41da860250d9c7599abb`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 27.9 MB (27889131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:907d5440f833628c2cd66d046da612d05b6dbaf613a36e923972b0d7ba1fca96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24756713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379d065e31e555ccd272014fd0ea8e326f2d896092d01d2f5d431390650b1185`

```dockerfile
```

-	Layers:
	-	`sha256:64dc42aa8bbf1cbd88565dee2e3b9217c3ae8ca0caa83f2eb80c839cc669fcd0`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 24.7 MB (24740366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4319d6fc7f46b8b6139c6311d8b3164aec04fae2546399cfddd86513aeb93ac3`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4b3054abbdebccaa00bebe2f1f0e6fa32055f0d7d9a5e20e5838855891011948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285553651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88425e0b22fabe9ef0564ee7133f7546f7a5f0114637c9eaf9e8e92271a91567`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27109cc6f2f4ce1d42bfbc092c0beee92d9717649e91b7bd9673e2fcbd075cbd`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 106.1 MB (106090308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522455a5a2e6e8a9311ac13057aa690b6d1ebf53c75b456e1cafc24bf8f9f27`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 382.2 KB (382192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d76cc9a9d526bd2365c7b6dc88a52aaf996f604271a069a01abc4cc2f0141`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bbcab63cba92ef478797b62881851c9f78d63434813a411a979a749f7fac07`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 27.0 MB (26997534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:345cd072abe5b9ed568306eefb47f8f69e38d46832e23a51c4ed460d74a25171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24779110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6b1efb3fdba4476ac69a6724610b446c83a91d09a3360c5d7a1b83fd0c57c2`

```dockerfile
```

-	Layers:
	-	`sha256:7b7f4139b31da0ae7c2cc84a845d28549bb57e698fe46299e796e62a398cff72`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 24.8 MB (24762626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c099573f70788522e5453ceabb26cbc497203ca0f5d27a91d955f634b003d85f`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:cf281fc739d5193a882ad7324e6dd03f9042de5d4c9d3d0148db7503e65c5a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:cb3d4998744a506d3f8bbaa64738ea7bfd43673112c7066a8f07f16023a1205a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297136544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f528e859b71dcab36a6045daff8d4a2e5e7ff45efb5eca098638bb666e82b27`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:13:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:14:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:14:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:14:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6dd392dbff6d7b6d67519ea916b13cc6925d0f92d2307dbd82948acdad262e`  
		Last Modified: Mon, 11 May 2026 19:14:56 GMT  
		Size: 110.7 MB (110663798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1181bd112c159be737e19d577fcc94d397c7a43df3b628032eba0cd6d04aaf1`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 382.2 KB (382206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b2253a336265af7d54719c96a7b7657acd02bdb998b134763b3d84a72ba52`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3324873c74ee6b185565d669a1ea23f5580faf99788e41da860250d9c7599abb`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 27.9 MB (27889131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:907d5440f833628c2cd66d046da612d05b6dbaf613a36e923972b0d7ba1fca96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24756713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379d065e31e555ccd272014fd0ea8e326f2d896092d01d2f5d431390650b1185`

```dockerfile
```

-	Layers:
	-	`sha256:64dc42aa8bbf1cbd88565dee2e3b9217c3ae8ca0caa83f2eb80c839cc669fcd0`  
		Last Modified: Mon, 11 May 2026 19:14:54 GMT  
		Size: 24.7 MB (24740366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4319d6fc7f46b8b6139c6311d8b3164aec04fae2546399cfddd86513aeb93ac3`  
		Last Modified: Mon, 11 May 2026 19:14:53 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4b3054abbdebccaa00bebe2f1f0e6fa32055f0d7d9a5e20e5838855891011948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285553651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88425e0b22fabe9ef0564ee7133f7546f7a5f0114637c9eaf9e8e92271a91567`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27109cc6f2f4ce1d42bfbc092c0beee92d9717649e91b7bd9673e2fcbd075cbd`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 106.1 MB (106090308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522455a5a2e6e8a9311ac13057aa690b6d1ebf53c75b456e1cafc24bf8f9f27`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 382.2 KB (382192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d76cc9a9d526bd2365c7b6dc88a52aaf996f604271a069a01abc4cc2f0141`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bbcab63cba92ef478797b62881851c9f78d63434813a411a979a749f7fac07`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 27.0 MB (26997534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:345cd072abe5b9ed568306eefb47f8f69e38d46832e23a51c4ed460d74a25171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24779110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6b1efb3fdba4476ac69a6724610b446c83a91d09a3360c5d7a1b83fd0c57c2`

```dockerfile
```

-	Layers:
	-	`sha256:7b7f4139b31da0ae7c2cc84a845d28549bb57e698fe46299e796e62a398cff72`  
		Last Modified: Mon, 11 May 2026 19:13:08 GMT  
		Size: 24.8 MB (24762626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c099573f70788522e5453ceabb26cbc497203ca0f5d27a91d955f634b003d85f`  
		Last Modified: Mon, 11 May 2026 19:13:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:62a7ba27a48159e00d0e94661e216820810b5b15adb5d8e757f8ed79d96f1d05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e50eee05e9060c826384bbdd9a82cc75bcd61ee8e5e77e1eaff72f25b08e507c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158198892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb045e003cdd6c6eb80a9052069c7c04b15e78a027a3b45541d54f292d73b4e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:174363aec632d507841cef9828cf98206efafe204f4159bf746f12f84520093c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18504606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50022f477cd3c8403c62e076f0821ab59e625d81980883f360abd050a76a2028`

```dockerfile
```

-	Layers:
	-	`sha256:24492611cd6397b462ea33a8224e6905f480fda5050ef5488fdef33e2ecdf50d`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 18.5 MB (18489985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc1721156701d2e894171b230c9ca05a79ff6274a7725616a309679149026e5`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8eea9a303d9e1ca63b81ab1b2e7ae8bf38f4589ca648230485599410ef614f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152081101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f802896a33854f12df469b46459247fef5e52ba9086aca664d48344f12abcc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:e3154051f38f23e86adad4d93bb0643e30818ad1502e96cf25f13ed2e323e546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2570de1c3e52fb0cfb6ad1223ea7cc5be34529ce7a973c7e1ff50f7199a982d5`

```dockerfile
```

-	Layers:
	-	`sha256:a67ef78cc77fe23e1b505b3ca3c07ceef240ac57ce65e8363a2a9abd297e34ff`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 18.5 MB (18463996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513690a7783078c92f117ad75129d56de5f064b0a925f8319c613f72c6c031cf`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:62a7ba27a48159e00d0e94661e216820810b5b15adb5d8e757f8ed79d96f1d05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:e50eee05e9060c826384bbdd9a82cc75bcd61ee8e5e77e1eaff72f25b08e507c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158198892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb045e003cdd6c6eb80a9052069c7c04b15e78a027a3b45541d54f292d73b4e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:35 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:13 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203aa6346a00710093073ecb851e68546fe7d5c7a63cadd967ed2e0aa14710a3`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 684.0 KB (683966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8297d1086b1f98cc9287380fd3692f52255afda0cdc36d3f71de8384e801f5c6`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 6.8 MB (6752218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4ff6313d42e457ed69085fdbdc948df6fb09eda1bce0ed0adc882aca17571`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 94.2 KB (94167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83cec8ec35503c52817d061b1414b615de2561b55cb85f2e547c2a4f2498d16`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 120.9 MB (120935367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbfd4d642fd8b6e0afa60c8511d6c0bc8eb8471fac315e352391383debe6f0`  
		Last Modified: Mon, 11 May 2026 19:01:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:174363aec632d507841cef9828cf98206efafe204f4159bf746f12f84520093c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18504606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50022f477cd3c8403c62e076f0821ab59e625d81980883f360abd050a76a2028`

```dockerfile
```

-	Layers:
	-	`sha256:24492611cd6397b462ea33a8224e6905f480fda5050ef5488fdef33e2ecdf50d`  
		Last Modified: Mon, 11 May 2026 19:01:40 GMT  
		Size: 18.5 MB (18489985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acc1721156701d2e894171b230c9ca05a79ff6274a7725616a309679149026e5`  
		Last Modified: Mon, 11 May 2026 19:01:39 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8eea9a303d9e1ca63b81ab1b2e7ae8bf38f4589ca648230485599410ef614f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152081101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f802896a33854f12df469b46459247fef5e52ba9086aca664d48344f12abcc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:08 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:53 GMT
ENV ROS_DISTRO=kilted
# Mon, 11 May 2026 19:01:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc10796365a045f536d89d2fac057e52b1f2ac4ded2cd70e983c8d188e980099`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cc3dfbf9593cf69afba801c78df1d39513c204943247037d87b6ffc686f2bd`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 6.8 MB (6765719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325aca0beeecd063d5b36f9d2b79c49f8b5285d68089393904bb78725a415c6`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 94.4 KB (94387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03683ac42ce0d6085689c7560dccd52e485e8811e595a23298003750fed62592`  
		Last Modified: Mon, 11 May 2026 19:02:25 GMT  
		Size: 115.7 MB (115660823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310fb8d7ab59c87909b9450d1df5d071d4e1796dd9aff7a3039b45a8807780b`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e3154051f38f23e86adad4d93bb0643e30818ad1502e96cf25f13ed2e323e546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2570de1c3e52fb0cfb6ad1223ea7cc5be34529ce7a973c7e1ff50f7199a982d5`

```dockerfile
```

-	Layers:
	-	`sha256:a67ef78cc77fe23e1b505b3ca3c07ceef240ac57ce65e8363a2a9abd297e34ff`  
		Last Modified: Mon, 11 May 2026 19:02:22 GMT  
		Size: 18.5 MB (18463996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513690a7783078c92f117ad75129d56de5f064b0a925f8319c613f72c6c031cf`  
		Last Modified: Mon, 11 May 2026 19:02:21 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:eac11a5285beeb1e1884e71f7091c610e08452e823bfb3f43afaa334375325f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:1c3e6fcf78d686d404a825f32902359fd898c01596b17c3354c91b8931b29e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296624907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41d5c7490a1b1f0c2395aa100b32d431ed52a0c11b293644ac2270f727b6063`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d79ab55df243721787bae594a1869e32111c3fceaedf29d6c4916281b829e3`  
		Last Modified: Mon, 11 May 2026 19:13:12 GMT  
		Size: 110.7 MB (110661006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefa18366212cb7871cc063fe2189897ae3ede04c35065e1041761e727a04552`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 414.0 KB (414006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437c42b38e5dd4ff52978453169e4760ca982ed52358da77cf1428e1d0a35dc`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626295b76a9867451fd495dd438f1ca2575ab6ec87675aebb1b6e00ab43fa94`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 28.1 MB (28068784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:d915bd300681c6e58f23127c8cc0ab1491860713c1ca865459ba1917cb50f7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24807454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2697aaa028236a6efbe85f1f380bcc63263008ca7f97d22eba6ea829b8a3f1`

```dockerfile
```

-	Layers:
	-	`sha256:66765b0ae9a51a477b76dbb9ebf1cbafb71d4eea908797708288df58da1d3eb1`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 24.8 MB (24790833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929ab4c70f88b50c8a6a4c73812d6e5917e8e1fe47d308a0c6635f4f1c80554`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c22b11ae86c58ddc90ce067c7641f3eb501f18d7808be1afb030f3cbcbbcd94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285097578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbc602fd948b667d652b3b27cd93c4d7895631148083dae39e2fbf77960f5e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
# Mon, 11 May 2026 19:10:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:10:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:10:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ef13a8256deb85c6ab6c779a50cae10e54bde2a7710d853fbc47767a135020`  
		Last Modified: Mon, 11 May 2026 19:11:38 GMT  
		Size: 106.1 MB (106088503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e204c60f127cbe48970ee27259bf80d1c1ad40e5b4f1f7833f50fa8468c99`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 414.0 KB (414004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f824c1438b2e0ad2054bdea0f885c631c4527adf75a317d1de5d764fb90bb3`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fdcf0407801b47e4bd3f232539f37ff6b13700e812eafeb81b0ff220bd8dc`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 27.2 MB (27178247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:47dc7b5b22b38978662411b3415c57faa57c97711f1aac5c7bd58b912e5f36a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24829870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6794c54b8ba603a582971278891bd3a70adb4ca46a7cf338bdc88657bb46b96a`

```dockerfile
```

-	Layers:
	-	`sha256:536e5e23b46b254ea67818466ec32d5d9e0e63d1c8d85b502fb5d5164c5347f3`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 24.8 MB (24813100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1dacd6cdc2beafe25edc8cb9a256766663e91f4b13f94979e74972f7f090598`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical`

```console
$ docker pull ros@sha256:2cdd3902d630fedfb33e7b2895034ce33d754f680f731df54e0009368a7a7db2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical` - linux; amd64

```console
$ docker pull ros@sha256:ada79a1ecc3953db0685f65be8b3d1424ee4a54e36f38a63279745791461c580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339416490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b600ff5deebe2ec7fb32713eb68df3de542d12985c39b444d6388febd0582f`
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
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:19:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:19:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:19:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:20:11 GMT
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
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d78e0bbfc54960c1d9050e06e1fbb6b8e71dacf2cdb4d66cb6e015a8f7312`  
		Last Modified: Sat, 09 May 2026 00:21:04 GMT  
		Size: 124.7 MB (124737949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a44bf4030e5e86c84762608c8c70592d177e681192adfc99cbc6ee911d5546`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 372.9 KB (372895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d20c0e84974b12eec6d14b04e2a6e9ad88f979d562e6fefa8af049ae36cfc5`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 130.8 KB (130820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93e4853a5be4476dc8afdd04e48a0d4cf8913d7431b2850bb30bf7ac89ecbf`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 25.7 MB (25708500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical` - unknown; unknown

```console
$ docker pull ros@sha256:2e4f4a88aa22149b8f7902e32bcfc19b8ea3d8b3ead54c3a6054cb1a89281bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29031296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9d20c7af3df94a5babd40059a96bfe98295fabe87e3c4d432176d5e9ead06a`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ddced94e7b81222993cbf35ca699f7960ffd4373aa0c92dd78b4dda4e6baa`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 29.0 MB (29014138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8910a6bd8c9e6bbe5049c8ca9bd33484850a549cdfcbcdfe3da9a4c6f5f5ac32`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 17.2 KB (17158 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8548467e419ef69ecdf02a25c0f25d76173d9208e9597e98e6d43f57eb6a61a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324190553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2297e725c268af41131d851a5917cc5e187a2f99d46938128d4fc3a12c081d1d`
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
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:17:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:17:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:17:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:17:54 GMT
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
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d616b9ddec74bbcb20aecbdb8529a143f8c7b16913e11f94e32199829327a93`  
		Last Modified: Sat, 09 May 2026 00:18:46 GMT  
		Size: 118.2 MB (118153470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c328c3b8daee7f1f707be08e1192ee6c9041f48302d1cd581895c3f543506`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 372.9 KB (372898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de351669d7d636b1fd95a81cd027b607bff48ac52729b84869644be0ee14ae`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 130.8 KB (130807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbf379aec8d97e3ab9091ff59091eb41363b0363c5bfec3929457e27e54b98`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 24.7 MB (24650366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical` - unknown; unknown

```console
$ docker pull ros@sha256:f3c9a13721bacb6b7d2236c2dd09ea5996f72f5ae9e50455ee034990d847a38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29094709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9030b2c11574415c78ab1905860db0c0796842c898ba7e09080735c4f739b12`

```dockerfile
```

-	Layers:
	-	`sha256:146db6f4e3ff1627ee09ede1d352f2fa38126c9d603435e2d45398e2fc7b36b4`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 29.1 MB (29077414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15c3d48e1916829dbecd4399e73a22884f3c1d69d4a19510db0d94495c1db47`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 17.3 KB (17295 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-perception`

```console
$ docker pull ros@sha256:1b035a4b15df2f5ae8902a6f571a20cea6cdb995517f4c506caa02198439835a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-perception` - linux; amd64

```console
$ docker pull ros@sha256:0df051ffc6db021225ab6cdfc1573644fcfdb71a9559e5908e378ef1e85f16d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1527925597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbd9262bbb81ab395e475af1e51a0cd04832bb5cdfc2545e854b0346ad6668c`
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
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:19:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:19:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:19:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:20:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 01:25:13 GMT
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
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d78e0bbfc54960c1d9050e06e1fbb6b8e71dacf2cdb4d66cb6e015a8f7312`  
		Last Modified: Sat, 09 May 2026 00:21:04 GMT  
		Size: 124.7 MB (124737949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a44bf4030e5e86c84762608c8c70592d177e681192adfc99cbc6ee911d5546`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 372.9 KB (372895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d20c0e84974b12eec6d14b04e2a6e9ad88f979d562e6fefa8af049ae36cfc5`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 130.8 KB (130820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93e4853a5be4476dc8afdd04e48a0d4cf8913d7431b2850bb30bf7ac89ecbf`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 25.7 MB (25708500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0254259b128c08f6d961eb93d3279b0ec3134a4b28614a3a0242b52cc3e13`  
		Last Modified: Sat, 09 May 2026 01:29:59 GMT  
		Size: 1.2 GB (1188509107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c69d500c876a8e34dffdc0d0a51ee25a3324ab145ca8939332139721a18d3dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64231304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607bb1a30d5695a5a32290346ac16bc559fa69efbbfb19f90fa2b88770340a78`

```dockerfile
```

-	Layers:
	-	`sha256:4a65cf1cd9b1b860976aedc21ae3544e9ecdcbae05b60261c1bd00c99e4b4d7d`  
		Last Modified: Sat, 09 May 2026 01:29:40 GMT  
		Size: 64.2 MB (64221611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8aaeed60b800c7c8b9d770bb01f29c65fe5e0620871633c2b8504e36da21cf`  
		Last Modified: Sat, 09 May 2026 01:29:36 GMT  
		Size: 9.7 KB (9693 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b461e81cec962c6a412b0449e2296fdaefcad6b355d6a810107d5d3c103d1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1471311395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72aed78914ac1c73bc1d081aeca5fa90a3ff4ec619a079517c3fd5f1fe1a5b8`
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
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:17:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:17:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:17:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:17:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 01:50:02 GMT
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
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d616b9ddec74bbcb20aecbdb8529a143f8c7b16913e11f94e32199829327a93`  
		Last Modified: Sat, 09 May 2026 00:18:46 GMT  
		Size: 118.2 MB (118153470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c328c3b8daee7f1f707be08e1192ee6c9041f48302d1cd581895c3f543506`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 372.9 KB (372898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de351669d7d636b1fd95a81cd027b607bff48ac52729b84869644be0ee14ae`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 130.8 KB (130807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbf379aec8d97e3ab9091ff59091eb41363b0363c5bfec3929457e27e54b98`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 24.7 MB (24650366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef19030f64476b24e550414112b2f4ba4b3756f7760cefe4362bd7b09d7ba83`  
		Last Modified: Sat, 09 May 2026 01:54:42 GMT  
		Size: 1.1 GB (1147120842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-perception` - unknown; unknown

```console
$ docker pull ros@sha256:ce5fac704a40f55b5936e3554179dec2d46d07c5e632b909bbe0d3345d8ba890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64144258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510b098a24683debacc996103d592f74b0c79aa37602aee697c0e67b15167f97`

```dockerfile
```

-	Layers:
	-	`sha256:46b2affd8b7b64d9ac7fbb7f054be33a2bf5b780d967b12423095898f329e279`  
		Last Modified: Sat, 09 May 2026 01:54:25 GMT  
		Size: 64.1 MB (64134485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e5d27dcfe393e7567d97dc877084339bcb8643bb894e21eaa5c4771be76323`  
		Last Modified: Sat, 09 May 2026 01:54:22 GMT  
		Size: 9.8 KB (9773 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-perception-resolute`

```console
$ docker pull ros@sha256:1b035a4b15df2f5ae8902a6f571a20cea6cdb995517f4c506caa02198439835a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-perception-resolute` - linux; amd64

```console
$ docker pull ros@sha256:0df051ffc6db021225ab6cdfc1573644fcfdb71a9559e5908e378ef1e85f16d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1527925597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbd9262bbb81ab395e475af1e51a0cd04832bb5cdfc2545e854b0346ad6668c`
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
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:19:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:19:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:19:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:20:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 01:25:13 GMT
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
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d78e0bbfc54960c1d9050e06e1fbb6b8e71dacf2cdb4d66cb6e015a8f7312`  
		Last Modified: Sat, 09 May 2026 00:21:04 GMT  
		Size: 124.7 MB (124737949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a44bf4030e5e86c84762608c8c70592d177e681192adfc99cbc6ee911d5546`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 372.9 KB (372895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d20c0e84974b12eec6d14b04e2a6e9ad88f979d562e6fefa8af049ae36cfc5`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 130.8 KB (130820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93e4853a5be4476dc8afdd04e48a0d4cf8913d7431b2850bb30bf7ac89ecbf`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 25.7 MB (25708500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d0254259b128c08f6d961eb93d3279b0ec3134a4b28614a3a0242b52cc3e13`  
		Last Modified: Sat, 09 May 2026 01:29:59 GMT  
		Size: 1.2 GB (1188509107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-perception-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:c69d500c876a8e34dffdc0d0a51ee25a3324ab145ca8939332139721a18d3dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64231304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607bb1a30d5695a5a32290346ac16bc559fa69efbbfb19f90fa2b88770340a78`

```dockerfile
```

-	Layers:
	-	`sha256:4a65cf1cd9b1b860976aedc21ae3544e9ecdcbae05b60261c1bd00c99e4b4d7d`  
		Last Modified: Sat, 09 May 2026 01:29:40 GMT  
		Size: 64.2 MB (64221611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8aaeed60b800c7c8b9d770bb01f29c65fe5e0620871633c2b8504e36da21cf`  
		Last Modified: Sat, 09 May 2026 01:29:36 GMT  
		Size: 9.7 KB (9693 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-perception-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b461e81cec962c6a412b0449e2296fdaefcad6b355d6a810107d5d3c103d1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1471311395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72aed78914ac1c73bc1d081aeca5fa90a3ff4ec619a079517c3fd5f1fe1a5b8`
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
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:17:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:17:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:17:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:17:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-base=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 01:50:02 GMT
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
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d616b9ddec74bbcb20aecbdb8529a143f8c7b16913e11f94e32199829327a93`  
		Last Modified: Sat, 09 May 2026 00:18:46 GMT  
		Size: 118.2 MB (118153470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c328c3b8daee7f1f707be08e1192ee6c9041f48302d1cd581895c3f543506`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 372.9 KB (372898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de351669d7d636b1fd95a81cd027b607bff48ac52729b84869644be0ee14ae`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 130.8 KB (130807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbf379aec8d97e3ab9091ff59091eb41363b0363c5bfec3929457e27e54b98`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 24.7 MB (24650366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef19030f64476b24e550414112b2f4ba4b3756f7760cefe4362bd7b09d7ba83`  
		Last Modified: Sat, 09 May 2026 01:54:42 GMT  
		Size: 1.1 GB (1147120842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-perception-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:ce5fac704a40f55b5936e3554179dec2d46d07c5e632b909bbe0d3345d8ba890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64144258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510b098a24683debacc996103d592f74b0c79aa37602aee697c0e67b15167f97`

```dockerfile
```

-	Layers:
	-	`sha256:46b2affd8b7b64d9ac7fbb7f054be33a2bf5b780d967b12423095898f329e279`  
		Last Modified: Sat, 09 May 2026 01:54:25 GMT  
		Size: 64.1 MB (64134485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e5d27dcfe393e7567d97dc877084339bcb8643bb894e21eaa5c4771be76323`  
		Last Modified: Sat, 09 May 2026 01:54:22 GMT  
		Size: 9.8 KB (9773 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-ros-base`

```console
$ docker pull ros@sha256:2cdd3902d630fedfb33e7b2895034ce33d754f680f731df54e0009368a7a7db2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:ada79a1ecc3953db0685f65be8b3d1424ee4a54e36f38a63279745791461c580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339416490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b600ff5deebe2ec7fb32713eb68df3de542d12985c39b444d6388febd0582f`
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
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:19:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:19:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:19:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:20:11 GMT
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
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d78e0bbfc54960c1d9050e06e1fbb6b8e71dacf2cdb4d66cb6e015a8f7312`  
		Last Modified: Sat, 09 May 2026 00:21:04 GMT  
		Size: 124.7 MB (124737949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a44bf4030e5e86c84762608c8c70592d177e681192adfc99cbc6ee911d5546`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 372.9 KB (372895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d20c0e84974b12eec6d14b04e2a6e9ad88f979d562e6fefa8af049ae36cfc5`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 130.8 KB (130820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93e4853a5be4476dc8afdd04e48a0d4cf8913d7431b2850bb30bf7ac89ecbf`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 25.7 MB (25708500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:2e4f4a88aa22149b8f7902e32bcfc19b8ea3d8b3ead54c3a6054cb1a89281bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29031296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9d20c7af3df94a5babd40059a96bfe98295fabe87e3c4d432176d5e9ead06a`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ddced94e7b81222993cbf35ca699f7960ffd4373aa0c92dd78b4dda4e6baa`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 29.0 MB (29014138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8910a6bd8c9e6bbe5049c8ca9bd33484850a549cdfcbcdfe3da9a4c6f5f5ac32`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 17.2 KB (17158 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8548467e419ef69ecdf02a25c0f25d76173d9208e9597e98e6d43f57eb6a61a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324190553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2297e725c268af41131d851a5917cc5e187a2f99d46938128d4fc3a12c081d1d`
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
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:17:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:17:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:17:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:17:54 GMT
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
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d616b9ddec74bbcb20aecbdb8529a143f8c7b16913e11f94e32199829327a93`  
		Last Modified: Sat, 09 May 2026 00:18:46 GMT  
		Size: 118.2 MB (118153470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c328c3b8daee7f1f707be08e1192ee6c9041f48302d1cd581895c3f543506`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 372.9 KB (372898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de351669d7d636b1fd95a81cd027b607bff48ac52729b84869644be0ee14ae`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 130.8 KB (130807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbf379aec8d97e3ab9091ff59091eb41363b0363c5bfec3929457e27e54b98`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 24.7 MB (24650366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:f3c9a13721bacb6b7d2236c2dd09ea5996f72f5ae9e50455ee034990d847a38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29094709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9030b2c11574415c78ab1905860db0c0796842c898ba7e09080735c4f739b12`

```dockerfile
```

-	Layers:
	-	`sha256:146db6f4e3ff1627ee09ede1d352f2fa38126c9d603435e2d45398e2fc7b36b4`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 29.1 MB (29077414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15c3d48e1916829dbecd4399e73a22884f3c1d69d4a19510db0d94495c1db47`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 17.3 KB (17295 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-ros-base-resolute`

```console
$ docker pull ros@sha256:2cdd3902d630fedfb33e7b2895034ce33d754f680f731df54e0009368a7a7db2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-base-resolute` - linux; amd64

```console
$ docker pull ros@sha256:ada79a1ecc3953db0685f65be8b3d1424ee4a54e36f38a63279745791461c580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339416490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b600ff5deebe2ec7fb32713eb68df3de542d12985c39b444d6388febd0582f`
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
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:19:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:19:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:19:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:20:11 GMT
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
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d78e0bbfc54960c1d9050e06e1fbb6b8e71dacf2cdb4d66cb6e015a8f7312`  
		Last Modified: Sat, 09 May 2026 00:21:04 GMT  
		Size: 124.7 MB (124737949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a44bf4030e5e86c84762608c8c70592d177e681192adfc99cbc6ee911d5546`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 372.9 KB (372895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d20c0e84974b12eec6d14b04e2a6e9ad88f979d562e6fefa8af049ae36cfc5`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 130.8 KB (130820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93e4853a5be4476dc8afdd04e48a0d4cf8913d7431b2850bb30bf7ac89ecbf`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 25.7 MB (25708500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:2e4f4a88aa22149b8f7902e32bcfc19b8ea3d8b3ead54c3a6054cb1a89281bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29031296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9d20c7af3df94a5babd40059a96bfe98295fabe87e3c4d432176d5e9ead06a`

```dockerfile
```

-	Layers:
	-	`sha256:3d8ddced94e7b81222993cbf35ca699f7960ffd4373aa0c92dd78b4dda4e6baa`  
		Last Modified: Sat, 09 May 2026 00:21:02 GMT  
		Size: 29.0 MB (29014138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8910a6bd8c9e6bbe5049c8ca9bd33484850a549cdfcbcdfe3da9a4c6f5f5ac32`  
		Last Modified: Sat, 09 May 2026 00:21:01 GMT  
		Size: 17.2 KB (17158 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-base-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8548467e419ef69ecdf02a25c0f25d76173d9208e9597e98e6d43f57eb6a61a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324190553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2297e725c268af41131d851a5917cc5e187a2f99d46938128d4fc3a12c081d1d`
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
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
# Sat, 09 May 2026 00:17:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:17:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Sat, 09 May 2026 00:17:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 09 May 2026 00:17:54 GMT
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
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d616b9ddec74bbcb20aecbdb8529a143f8c7b16913e11f94e32199829327a93`  
		Last Modified: Sat, 09 May 2026 00:18:46 GMT  
		Size: 118.2 MB (118153470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c328c3b8daee7f1f707be08e1192ee6c9041f48302d1cd581895c3f543506`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 372.9 KB (372898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17de351669d7d636b1fd95a81cd027b607bff48ac52729b84869644be0ee14ae`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 130.8 KB (130807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbbf379aec8d97e3ab9091ff59091eb41363b0363c5bfec3929457e27e54b98`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 24.7 MB (24650366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-base-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:f3c9a13721bacb6b7d2236c2dd09ea5996f72f5ae9e50455ee034990d847a38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29094709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9030b2c11574415c78ab1905860db0c0796842c898ba7e09080735c4f739b12`

```dockerfile
```

-	Layers:
	-	`sha256:146db6f4e3ff1627ee09ede1d352f2fa38126c9d603435e2d45398e2fc7b36b4`  
		Last Modified: Sat, 09 May 2026 00:18:44 GMT  
		Size: 29.1 MB (29077414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15c3d48e1916829dbecd4399e73a22884f3c1d69d4a19510db0d94495c1db47`  
		Last Modified: Sat, 09 May 2026 00:18:43 GMT  
		Size: 17.3 KB (17295 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-ros-core`

```console
$ docker pull ros@sha256:c56ac343fa97862e38b58a098c606573bea79b7922add04090676d1a08f85edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:82aa0cda98eab0df52ef080f8387daa8e406eb0e0a9546a15a69f6377733d029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188466326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac5db437362b6daab8a68ebe5a455bdab6fccfb73ba453b7332fb3977934e4`
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
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
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
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:eb46362455c4113d7895b0d1e6f0456499f1371be26e115ce317b93337eccf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22640304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6230aa06d1c826e706389a1870ed6c999bda4f9928e779de7143eddfcacafb0`

```dockerfile
```

-	Layers:
	-	`sha256:25fac0a70e1f25b7ce71e4c5cee97e5aca2b8212309e34ee96fc331b2d384a22`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 22.6 MB (22624638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e3389d5c21f95719680f1f7aee20a78bc1f0b1894867d1187d62ad83f9e702`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 15.7 KB (15666 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b7ada19442522356c41068b118d09779c23b6378fa0c62a1eda69e1778432a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180883012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43557dd5db2663de83be96d768e175ca14caf53c167390b08106a510738ba0ac`
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
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
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
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:b6100031a7e8e5dd64fc8906212a49b5eb3faa34f85d0a886449f01d8649ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22613122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273948cc2e96b5ce4e6eb43e0311b063a8142b0b5edd61c6f6f2093cdb1ee085`

```dockerfile
```

-	Layers:
	-	`sha256:346f29057dc412460266bcc5190b7124bacade959410d25bd2e7e4a07998c1bc`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 22.6 MB (22597330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a7cc396851c248c045d334cb5a5bb84f21c0f07c6c2a1b8808232ab344328a`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical-ros-core-resolute`

```console
$ docker pull ros@sha256:c56ac343fa97862e38b58a098c606573bea79b7922add04090676d1a08f85edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:lyrical-ros-core-resolute` - linux; amd64

```console
$ docker pull ros@sha256:82aa0cda98eab0df52ef080f8387daa8e406eb0e0a9546a15a69f6377733d029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188466326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddac5db437362b6daab8a68ebe5a455bdab6fccfb73ba453b7332fb3977934e4`
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
# Fri, 08 May 2026 22:59:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:59:39 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 23:00:27 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 23:00:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:00:28 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 23:00:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 23:00:28 GMT
CMD ["bash"]
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
	-	`sha256:b58fc8dd5a66dc7fa8b8c570fa7912cd1c0d64d137d2aa56def7154e90cf727b`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 740.5 KB (740458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feca8694738697c1567a29afc471a4b7ea676c3eddc5759f9263533970f2f16`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 9.8 MB (9823544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922240d09f956ad29b9fa276615b85985d409423150635bb69c069cd5b23557`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 89.6 KB (89556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0b6b69c6e422a26e80d97a17324c51f973ec6ef420d6aba5e4f7d584849c2`  
		Last Modified: Fri, 08 May 2026 23:01:10 GMT  
		Size: 136.3 MB (136257322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b86f409736327ea3469de3310b97135181291004f0273e763aea3cb96f6b794`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:eb46362455c4113d7895b0d1e6f0456499f1371be26e115ce317b93337eccf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22640304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6230aa06d1c826e706389a1870ed6c999bda4f9928e779de7143eddfcacafb0`

```dockerfile
```

-	Layers:
	-	`sha256:25fac0a70e1f25b7ce71e4c5cee97e5aca2b8212309e34ee96fc331b2d384a22`  
		Last Modified: Fri, 08 May 2026 23:01:08 GMT  
		Size: 22.6 MB (22624638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e3389d5c21f95719680f1f7aee20a78bc1f0b1894867d1187d62ad83f9e702`  
		Last Modified: Fri, 08 May 2026 23:01:07 GMT  
		Size: 15.7 KB (15666 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:lyrical-ros-core-resolute` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b7ada19442522356c41068b118d09779c23b6378fa0c62a1eda69e1778432a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180883012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43557dd5db2663de83be96d768e175ca14caf53c167390b08106a510738ba0ac`
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
# Fri, 08 May 2026 22:48:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:00 GMT
RUN curl -L -s -o /tmp/ros2-testing-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-testing-apt-source_1.2.0.resolute_all.deb     && echo "da9261ca7c06244da1528e0ede44018f7bb2e24a8a077eb0202f70706b578546 /tmp/ros2-testing-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-testing-apt-source.deb     && rm -f /tmp/ros2-testing-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV LC_ALL=C.UTF-8
# Fri, 08 May 2026 22:49:49 GMT
ENV ROS_DISTRO=lyrical
# Fri, 08 May 2026 22:49:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-lyrical-ros-core=0.13.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:49:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 08 May 2026 22:49:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 08 May 2026 22:49:49 GMT
CMD ["bash"]
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
	-	`sha256:f3e85634d1fbebf47d4daecf57083015fec4d5e485c1672a194d0ea711fa89a2`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 741.1 KB (741149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8354d4deb457ddf1c54c92b584b50e1d8c4f6fc494cbf5fad0095d18627edc58`  
		Last Modified: Fri, 08 May 2026 22:50:28 GMT  
		Size: 9.6 MB (9647454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e37e3b34a50099f4c08800cbd5d3901ef914cbcf05d8d305b5404f0f833461`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 90.3 KB (90294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8803f3bbdab9cc7b7ea61c314b1d91a491f614fceb1bdb9620b41d8f27fcf`  
		Last Modified: Fri, 08 May 2026 22:50:31 GMT  
		Size: 129.7 MB (129674576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd39f44e283c4ea1d22ea3fdf9f08689d73bf11fd40ca5a59259aa3648f8063`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:lyrical-ros-core-resolute` - unknown; unknown

```console
$ docker pull ros@sha256:b6100031a7e8e5dd64fc8906212a49b5eb3faa34f85d0a886449f01d8649ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22613122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273948cc2e96b5ce4e6eb43e0311b063a8142b0b5edd61c6f6f2093cdb1ee085`

```dockerfile
```

-	Layers:
	-	`sha256:346f29057dc412460266bcc5190b7124bacade959410d25bd2e7e4a07998c1bc`  
		Last Modified: Fri, 08 May 2026 22:50:29 GMT  
		Size: 22.6 MB (22597330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a7cc396851c248c045d334cb5a5bb84f21c0f07c6c2a1b8808232ab344328a`  
		Last Modified: Fri, 08 May 2026 22:50:27 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:723ba4fdcc232b43d7ee1effbee2414b3990321c22d3c9dfd8592ff17b2cd45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:31f9c6d5d29916f8453fbaedc90d04f6d90fd06e2fc6fde63df35b3922735981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310247490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92a3aabc48636ffb5e64ca286f5b824fb72230a55d9bd87334ba91245559fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:54:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:48 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 20:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:55:31 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:46:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:46:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0644559dc6b5362253940942368861ced9f603361da89c3adf2fa73b1f1d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 683.9 KB (683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5df3be57e9c4cb62447529fecd13a1ab07bdf59d8fa4cec97baabb95b4e82`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 6.8 MB (6751676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d348f5598561bd0e3f1088e2421dece24aa7886408f40050256c411670460`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 94.1 KB (94084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12fc106e828bf5ff0f53383298b088f62734575daaaa2895be3f66ba1cfb54`  
		Last Modified: Wed, 15 Apr 2026 20:56:03 GMT  
		Size: 134.6 MB (134574573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d7c739ca6a59209f2846d72bacf015f1dc13907916eed58de4d11acfffc88`  
		Last Modified: Wed, 15 Apr 2026 20:56:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0edaa250e70bbaa53abcbfe389b5fad0aa0ccf8a31288ff0f3bd56be0d828`  
		Last Modified: Wed, 15 Apr 2026 21:46:59 GMT  
		Size: 110.2 MB (110194688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd2230b661e86bd8f07be3fe552d014a6bb42e6c6f0e1fa2c4045df56aa97e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 372.6 KB (372604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbeb19838a72445d6331034c51685f40f29e6a1cea29183fb67841f42bdec46`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07594a85311817fb2971d58169042e384d9f2ba674661056a4843248d2b2d860`  
		Last Modified: Wed, 15 Apr 2026 21:46:58 GMT  
		Size: 27.8 MB (27840246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:9160eddb240a8b6961ea8dc2c209dcb4c78f3dd03b67fa0c9b41de246c4de7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25639305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1f06e701fb5bcf7ebbc0a8470d328c46b637279504b0a9e0b7acce0becfd60`

```dockerfile
```

-	Layers:
	-	`sha256:192b7fc04e9c190dba258987f37d3d622af18600b9a71749a77788e157eff235`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 25.6 MB (25622940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623bf7cc954c5cdb4b884a89eea6984e6c94c84632a1521d2ac915668d4fb7e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:79a9427039f9d78409f0f3e75b84b687d5de6b9788bcb35547b6089d47ca022a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298241998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3b9fad20ccb1f4ce82914ca570ae8b1dd8074079d45d2b0280d81c0b5d5f47`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:00 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 21:03:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:47 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0639bafbbdc971f48d3d9341ef1217810bc7f8a0f7b5f550a4de4f1eda3ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780148fe500efb9da4f54261b9798bc3826e7511b420c2f83053c80259562034`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 6.8 MB (6764969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cb309ea157ac41c9f5f3b289d2fc115949b136e8f5bc5ba4a4c5472ce2827`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 94.3 KB (94302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf0b996774010d3f153bedf3c3543d44d56ca9dacbabda918ae7803e211d095`  
		Last Modified: Wed, 15 Apr 2026 21:04:23 GMT  
		Size: 128.9 MB (128910385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19150fbc2aa4d400a4aabdcb600258de379ad9fcb5fedb3ecf7c4f62e66c76fd`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55fb6656c0bd58f1f4e8f0082f6663f39c311b9e6bb373a00bec4264bdd869`  
		Last Modified: Wed, 15 Apr 2026 21:59:36 GMT  
		Size: 105.6 MB (105607446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28d8aac2ee7081150c03cbcde7a4f24f212f4a35be4adca847877b6cb15dba3`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 372.6 KB (372606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b52b0368a0fe4002a81bfb4617077089e404ab39883aa6980f55d70d88ba180`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f2e0aca8d3cc0cdc8879d700e1fc2075dd7294a0ed1274b4b4e44ec8a2ef97`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 26.9 MB (26929600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:fafa44698ef68ded85039cfafe9fe2a0847c86f8165de5054a6e0996559258ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25661901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614e5195e08b2e642b8976aa479a328f39863a2a3874f9a1e2d005906fb4b533`

```dockerfile
```

-	Layers:
	-	`sha256:c86e42fa626316bf8f2341121584ad9fddf0a8b36b07cd48ec6d1b0653e358d9`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 25.6 MB (25645399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c16c7eb0a5f1ba24de37772385b79c70f92668a6e4939faa8f133719d79429`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:069adba4dc097602ecbadd22c372153c3b25938affe64e5e0a495fe665ef581c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:cb8a41af2ed2a76f76db40b01b92358356951281370e57f08ec55de3c5df8774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094485564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b7bcb8bad11923bc42d7f98bb7f5c88f7ff8e60932063c60e0070441fab202`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:54:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:48 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 20:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:55:31 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:46:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:46:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0644559dc6b5362253940942368861ced9f603361da89c3adf2fa73b1f1d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 683.9 KB (683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5df3be57e9c4cb62447529fecd13a1ab07bdf59d8fa4cec97baabb95b4e82`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 6.8 MB (6751676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d348f5598561bd0e3f1088e2421dece24aa7886408f40050256c411670460`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 94.1 KB (94084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12fc106e828bf5ff0f53383298b088f62734575daaaa2895be3f66ba1cfb54`  
		Last Modified: Wed, 15 Apr 2026 20:56:03 GMT  
		Size: 134.6 MB (134574573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d7c739ca6a59209f2846d72bacf015f1dc13907916eed58de4d11acfffc88`  
		Last Modified: Wed, 15 Apr 2026 20:56:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0edaa250e70bbaa53abcbfe389b5fad0aa0ccf8a31288ff0f3bd56be0d828`  
		Last Modified: Wed, 15 Apr 2026 21:46:59 GMT  
		Size: 110.2 MB (110194688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd2230b661e86bd8f07be3fe552d014a6bb42e6c6f0e1fa2c4045df56aa97e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 372.6 KB (372604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbeb19838a72445d6331034c51685f40f29e6a1cea29183fb67841f42bdec46`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07594a85311817fb2971d58169042e384d9f2ba674661056a4843248d2b2d860`  
		Last Modified: Wed, 15 Apr 2026 21:46:58 GMT  
		Size: 27.8 MB (27840246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ed1f57e9059a485b1e5e71e8465babde60dc3f7de0ecd9752523c2a077f6f`  
		Last Modified: Wed, 15 Apr 2026 22:33:19 GMT  
		Size: 784.2 MB (784238074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c7abfdaf5df307a548f5ad3e9c39e47ab0bae75feac9d8c34d9edde224780076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61807644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebe8e3a36e4932437f1afb456461c7b1884cf9524471ab087cf5aff90e40447`

```dockerfile
```

-	Layers:
	-	`sha256:35f28e8bd7242a5609b07d0a83c762d533f4baa63bf75d3daf7bf76dc0d173bb`  
		Last Modified: Wed, 15 Apr 2026 22:32:50 GMT  
		Size: 61.8 MB (61798283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9438d7fcb19ce4438bcf5a051ea9db28fdd034190be530781a480e7f5d5513d6`  
		Last Modified: Wed, 15 Apr 2026 22:32:47 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cb8c5ba66998e50f88675c26c4c0bc9198d5314ae14dba1d7f53ec47daa9211d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.6 MB (996620857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1bde9626d7edbea5f3a8d592c937df90f4ea49d3945e7ca4a57dff0288e3e2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:00 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 21:03:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:47 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0639bafbbdc971f48d3d9341ef1217810bc7f8a0f7b5f550a4de4f1eda3ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780148fe500efb9da4f54261b9798bc3826e7511b420c2f83053c80259562034`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 6.8 MB (6764969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cb309ea157ac41c9f5f3b289d2fc115949b136e8f5bc5ba4a4c5472ce2827`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 94.3 KB (94302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf0b996774010d3f153bedf3c3543d44d56ca9dacbabda918ae7803e211d095`  
		Last Modified: Wed, 15 Apr 2026 21:04:23 GMT  
		Size: 128.9 MB (128910385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19150fbc2aa4d400a4aabdcb600258de379ad9fcb5fedb3ecf7c4f62e66c76fd`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55fb6656c0bd58f1f4e8f0082f6663f39c311b9e6bb373a00bec4264bdd869`  
		Last Modified: Wed, 15 Apr 2026 21:59:36 GMT  
		Size: 105.6 MB (105607446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28d8aac2ee7081150c03cbcde7a4f24f212f4a35be4adca847877b6cb15dba3`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 372.6 KB (372606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b52b0368a0fe4002a81bfb4617077089e404ab39883aa6980f55d70d88ba180`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f2e0aca8d3cc0cdc8879d700e1fc2075dd7294a0ed1274b4b4e44ec8a2ef97`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 26.9 MB (26929600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1621f00909d53a407129792f8b61f3cd8ea2c0a6e80a4be628ffdbdfb7f05b`  
		Last Modified: Wed, 15 Apr 2026 22:40:59 GMT  
		Size: 698.4 MB (698378859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:d633aec837734ca70fe5ea65cfb24d9fa0a09d6f3699d7cedc89d0847a871cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61738442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f099555b3cce13a09b3e40c5556635f4897e91d2d510b94a3ede0775865e3b12`

```dockerfile
```

-	Layers:
	-	`sha256:2e8e4aff2748f38bb6aad8ee0a043395d67f4407b58c1295e7a9b780c6349d69`  
		Last Modified: Wed, 15 Apr 2026 22:40:46 GMT  
		Size: 61.7 MB (61729001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f931e8676b7db51c740efc2a54787d2e7b476619cf13fa19075fccdd6e727089`  
		Last Modified: Wed, 15 Apr 2026 22:40:43 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:069adba4dc097602ecbadd22c372153c3b25938affe64e5e0a495fe665ef581c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:cb8a41af2ed2a76f76db40b01b92358356951281370e57f08ec55de3c5df8774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094485564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b7bcb8bad11923bc42d7f98bb7f5c88f7ff8e60932063c60e0070441fab202`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:54:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:48 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 20:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:55:31 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:46:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:46:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0644559dc6b5362253940942368861ced9f603361da89c3adf2fa73b1f1d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 683.9 KB (683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5df3be57e9c4cb62447529fecd13a1ab07bdf59d8fa4cec97baabb95b4e82`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 6.8 MB (6751676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d348f5598561bd0e3f1088e2421dece24aa7886408f40050256c411670460`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 94.1 KB (94084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12fc106e828bf5ff0f53383298b088f62734575daaaa2895be3f66ba1cfb54`  
		Last Modified: Wed, 15 Apr 2026 20:56:03 GMT  
		Size: 134.6 MB (134574573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d7c739ca6a59209f2846d72bacf015f1dc13907916eed58de4d11acfffc88`  
		Last Modified: Wed, 15 Apr 2026 20:56:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0edaa250e70bbaa53abcbfe389b5fad0aa0ccf8a31288ff0f3bd56be0d828`  
		Last Modified: Wed, 15 Apr 2026 21:46:59 GMT  
		Size: 110.2 MB (110194688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd2230b661e86bd8f07be3fe552d014a6bb42e6c6f0e1fa2c4045df56aa97e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 372.6 KB (372604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbeb19838a72445d6331034c51685f40f29e6a1cea29183fb67841f42bdec46`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07594a85311817fb2971d58169042e384d9f2ba674661056a4843248d2b2d860`  
		Last Modified: Wed, 15 Apr 2026 21:46:58 GMT  
		Size: 27.8 MB (27840246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ed1f57e9059a485b1e5e71e8465babde60dc3f7de0ecd9752523c2a077f6f`  
		Last Modified: Wed, 15 Apr 2026 22:33:19 GMT  
		Size: 784.2 MB (784238074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c7abfdaf5df307a548f5ad3e9c39e47ab0bae75feac9d8c34d9edde224780076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61807644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebe8e3a36e4932437f1afb456461c7b1884cf9524471ab087cf5aff90e40447`

```dockerfile
```

-	Layers:
	-	`sha256:35f28e8bd7242a5609b07d0a83c762d533f4baa63bf75d3daf7bf76dc0d173bb`  
		Last Modified: Wed, 15 Apr 2026 22:32:50 GMT  
		Size: 61.8 MB (61798283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9438d7fcb19ce4438bcf5a051ea9db28fdd034190be530781a480e7f5d5513d6`  
		Last Modified: Wed, 15 Apr 2026 22:32:47 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cb8c5ba66998e50f88675c26c4c0bc9198d5314ae14dba1d7f53ec47daa9211d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.6 MB (996620857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1bde9626d7edbea5f3a8d592c937df90f4ea49d3945e7ca4a57dff0288e3e2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:00 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 21:03:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:47 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0639bafbbdc971f48d3d9341ef1217810bc7f8a0f7b5f550a4de4f1eda3ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780148fe500efb9da4f54261b9798bc3826e7511b420c2f83053c80259562034`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 6.8 MB (6764969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cb309ea157ac41c9f5f3b289d2fc115949b136e8f5bc5ba4a4c5472ce2827`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 94.3 KB (94302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf0b996774010d3f153bedf3c3543d44d56ca9dacbabda918ae7803e211d095`  
		Last Modified: Wed, 15 Apr 2026 21:04:23 GMT  
		Size: 128.9 MB (128910385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19150fbc2aa4d400a4aabdcb600258de379ad9fcb5fedb3ecf7c4f62e66c76fd`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55fb6656c0bd58f1f4e8f0082f6663f39c311b9e6bb373a00bec4264bdd869`  
		Last Modified: Wed, 15 Apr 2026 21:59:36 GMT  
		Size: 105.6 MB (105607446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28d8aac2ee7081150c03cbcde7a4f24f212f4a35be4adca847877b6cb15dba3`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 372.6 KB (372606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b52b0368a0fe4002a81bfb4617077089e404ab39883aa6980f55d70d88ba180`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f2e0aca8d3cc0cdc8879d700e1fc2075dd7294a0ed1274b4b4e44ec8a2ef97`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 26.9 MB (26929600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1621f00909d53a407129792f8b61f3cd8ea2c0a6e80a4be628ffdbdfb7f05b`  
		Last Modified: Wed, 15 Apr 2026 22:40:59 GMT  
		Size: 698.4 MB (698378859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d633aec837734ca70fe5ea65cfb24d9fa0a09d6f3699d7cedc89d0847a871cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61738442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f099555b3cce13a09b3e40c5556635f4897e91d2d510b94a3ede0775865e3b12`

```dockerfile
```

-	Layers:
	-	`sha256:2e8e4aff2748f38bb6aad8ee0a043395d67f4407b58c1295e7a9b780c6349d69`  
		Last Modified: Wed, 15 Apr 2026 22:40:46 GMT  
		Size: 61.7 MB (61729001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f931e8676b7db51c740efc2a54787d2e7b476619cf13fa19075fccdd6e727089`  
		Last Modified: Wed, 15 Apr 2026 22:40:43 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:723ba4fdcc232b43d7ee1effbee2414b3990321c22d3c9dfd8592ff17b2cd45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:31f9c6d5d29916f8453fbaedc90d04f6d90fd06e2fc6fde63df35b3922735981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310247490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92a3aabc48636ffb5e64ca286f5b824fb72230a55d9bd87334ba91245559fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:54:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:48 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 20:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:55:31 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:46:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:46:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0644559dc6b5362253940942368861ced9f603361da89c3adf2fa73b1f1d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 683.9 KB (683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5df3be57e9c4cb62447529fecd13a1ab07bdf59d8fa4cec97baabb95b4e82`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 6.8 MB (6751676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d348f5598561bd0e3f1088e2421dece24aa7886408f40050256c411670460`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 94.1 KB (94084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12fc106e828bf5ff0f53383298b088f62734575daaaa2895be3f66ba1cfb54`  
		Last Modified: Wed, 15 Apr 2026 20:56:03 GMT  
		Size: 134.6 MB (134574573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d7c739ca6a59209f2846d72bacf015f1dc13907916eed58de4d11acfffc88`  
		Last Modified: Wed, 15 Apr 2026 20:56:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0edaa250e70bbaa53abcbfe389b5fad0aa0ccf8a31288ff0f3bd56be0d828`  
		Last Modified: Wed, 15 Apr 2026 21:46:59 GMT  
		Size: 110.2 MB (110194688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd2230b661e86bd8f07be3fe552d014a6bb42e6c6f0e1fa2c4045df56aa97e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 372.6 KB (372604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbeb19838a72445d6331034c51685f40f29e6a1cea29183fb67841f42bdec46`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07594a85311817fb2971d58169042e384d9f2ba674661056a4843248d2b2d860`  
		Last Modified: Wed, 15 Apr 2026 21:46:58 GMT  
		Size: 27.8 MB (27840246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:9160eddb240a8b6961ea8dc2c209dcb4c78f3dd03b67fa0c9b41de246c4de7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25639305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1f06e701fb5bcf7ebbc0a8470d328c46b637279504b0a9e0b7acce0becfd60`

```dockerfile
```

-	Layers:
	-	`sha256:192b7fc04e9c190dba258987f37d3d622af18600b9a71749a77788e157eff235`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 25.6 MB (25622940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623bf7cc954c5cdb4b884a89eea6984e6c94c84632a1521d2ac915668d4fb7e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:79a9427039f9d78409f0f3e75b84b687d5de6b9788bcb35547b6089d47ca022a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298241998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3b9fad20ccb1f4ce82914ca570ae8b1dd8074079d45d2b0280d81c0b5d5f47`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:00 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 21:03:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:47 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0639bafbbdc971f48d3d9341ef1217810bc7f8a0f7b5f550a4de4f1eda3ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780148fe500efb9da4f54261b9798bc3826e7511b420c2f83053c80259562034`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 6.8 MB (6764969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cb309ea157ac41c9f5f3b289d2fc115949b136e8f5bc5ba4a4c5472ce2827`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 94.3 KB (94302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf0b996774010d3f153bedf3c3543d44d56ca9dacbabda918ae7803e211d095`  
		Last Modified: Wed, 15 Apr 2026 21:04:23 GMT  
		Size: 128.9 MB (128910385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19150fbc2aa4d400a4aabdcb600258de379ad9fcb5fedb3ecf7c4f62e66c76fd`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55fb6656c0bd58f1f4e8f0082f6663f39c311b9e6bb373a00bec4264bdd869`  
		Last Modified: Wed, 15 Apr 2026 21:59:36 GMT  
		Size: 105.6 MB (105607446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28d8aac2ee7081150c03cbcde7a4f24f212f4a35be4adca847877b6cb15dba3`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 372.6 KB (372606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b52b0368a0fe4002a81bfb4617077089e404ab39883aa6980f55d70d88ba180`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f2e0aca8d3cc0cdc8879d700e1fc2075dd7294a0ed1274b4b4e44ec8a2ef97`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 26.9 MB (26929600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fafa44698ef68ded85039cfafe9fe2a0847c86f8165de5054a6e0996559258ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25661901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614e5195e08b2e642b8976aa479a328f39863a2a3874f9a1e2d005906fb4b533`

```dockerfile
```

-	Layers:
	-	`sha256:c86e42fa626316bf8f2341121584ad9fddf0a8b36b07cd48ec6d1b0653e358d9`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 25.6 MB (25645399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c16c7eb0a5f1ba24de37772385b79c70f92668a6e4939faa8f133719d79429`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:723ba4fdcc232b43d7ee1effbee2414b3990321c22d3c9dfd8592ff17b2cd45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:31f9c6d5d29916f8453fbaedc90d04f6d90fd06e2fc6fde63df35b3922735981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310247490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a92a3aabc48636ffb5e64ca286f5b824fb72230a55d9bd87334ba91245559fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:54:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:48 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 20:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:55:31 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:46:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:46:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0644559dc6b5362253940942368861ced9f603361da89c3adf2fa73b1f1d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 683.9 KB (683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5df3be57e9c4cb62447529fecd13a1ab07bdf59d8fa4cec97baabb95b4e82`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 6.8 MB (6751676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d348f5598561bd0e3f1088e2421dece24aa7886408f40050256c411670460`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 94.1 KB (94084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12fc106e828bf5ff0f53383298b088f62734575daaaa2895be3f66ba1cfb54`  
		Last Modified: Wed, 15 Apr 2026 20:56:03 GMT  
		Size: 134.6 MB (134574573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d7c739ca6a59209f2846d72bacf015f1dc13907916eed58de4d11acfffc88`  
		Last Modified: Wed, 15 Apr 2026 20:56:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0edaa250e70bbaa53abcbfe389b5fad0aa0ccf8a31288ff0f3bd56be0d828`  
		Last Modified: Wed, 15 Apr 2026 21:46:59 GMT  
		Size: 110.2 MB (110194688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd2230b661e86bd8f07be3fe552d014a6bb42e6c6f0e1fa2c4045df56aa97e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 372.6 KB (372604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbeb19838a72445d6331034c51685f40f29e6a1cea29183fb67841f42bdec46`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07594a85311817fb2971d58169042e384d9f2ba674661056a4843248d2b2d860`  
		Last Modified: Wed, 15 Apr 2026 21:46:58 GMT  
		Size: 27.8 MB (27840246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9160eddb240a8b6961ea8dc2c209dcb4c78f3dd03b67fa0c9b41de246c4de7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25639305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1f06e701fb5bcf7ebbc0a8470d328c46b637279504b0a9e0b7acce0becfd60`

```dockerfile
```

-	Layers:
	-	`sha256:192b7fc04e9c190dba258987f37d3d622af18600b9a71749a77788e157eff235`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 25.6 MB (25622940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623bf7cc954c5cdb4b884a89eea6984e6c94c84632a1521d2ac915668d4fb7e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:79a9427039f9d78409f0f3e75b84b687d5de6b9788bcb35547b6089d47ca022a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298241998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3b9fad20ccb1f4ce82914ca570ae8b1dd8074079d45d2b0280d81c0b5d5f47`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:00 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 21:03:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:47 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0639bafbbdc971f48d3d9341ef1217810bc7f8a0f7b5f550a4de4f1eda3ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780148fe500efb9da4f54261b9798bc3826e7511b420c2f83053c80259562034`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 6.8 MB (6764969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cb309ea157ac41c9f5f3b289d2fc115949b136e8f5bc5ba4a4c5472ce2827`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 94.3 KB (94302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf0b996774010d3f153bedf3c3543d44d56ca9dacbabda918ae7803e211d095`  
		Last Modified: Wed, 15 Apr 2026 21:04:23 GMT  
		Size: 128.9 MB (128910385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19150fbc2aa4d400a4aabdcb600258de379ad9fcb5fedb3ecf7c4f62e66c76fd`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55fb6656c0bd58f1f4e8f0082f6663f39c311b9e6bb373a00bec4264bdd869`  
		Last Modified: Wed, 15 Apr 2026 21:59:36 GMT  
		Size: 105.6 MB (105607446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28d8aac2ee7081150c03cbcde7a4f24f212f4a35be4adca847877b6cb15dba3`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 372.6 KB (372606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b52b0368a0fe4002a81bfb4617077089e404ab39883aa6980f55d70d88ba180`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f2e0aca8d3cc0cdc8879d700e1fc2075dd7294a0ed1274b4b4e44ec8a2ef97`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 26.9 MB (26929600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fafa44698ef68ded85039cfafe9fe2a0847c86f8165de5054a6e0996559258ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25661901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614e5195e08b2e642b8976aa479a328f39863a2a3874f9a1e2d005906fb4b533`

```dockerfile
```

-	Layers:
	-	`sha256:c86e42fa626316bf8f2341121584ad9fddf0a8b36b07cd48ec6d1b0653e358d9`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 25.6 MB (25645399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c16c7eb0a5f1ba24de37772385b79c70f92668a6e4939faa8f133719d79429`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:c94add9c25ae32e9f6860d2351eb74a341030915279cff505d4c810324fd0561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:6831b1e9bbc4ebbac71511a3bb95bba347ce916b5cb90fb083ffd36d0296fc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171837446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01212f2377f15a1c1eba6cd117cc8c2e336b8618928d36cb864f291353eeaef`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:54:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:48 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 20:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:55:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0644559dc6b5362253940942368861ced9f603361da89c3adf2fa73b1f1d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 683.9 KB (683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5df3be57e9c4cb62447529fecd13a1ab07bdf59d8fa4cec97baabb95b4e82`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 6.8 MB (6751676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d348f5598561bd0e3f1088e2421dece24aa7886408f40050256c411670460`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 94.1 KB (94084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12fc106e828bf5ff0f53383298b088f62734575daaaa2895be3f66ba1cfb54`  
		Last Modified: Wed, 15 Apr 2026 20:56:03 GMT  
		Size: 134.6 MB (134574573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d7c739ca6a59209f2846d72bacf015f1dc13907916eed58de4d11acfffc88`  
		Last Modified: Wed, 15 Apr 2026 20:56:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:77c07fbc7e1a1d7de335637fbac2c962cf5c618356f59a251464aa3c694d868e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19431994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b396ea28e823dc7b135e760e6e7df53cb3f15fcdc707fb64dbfa0f1951911d24`

```dockerfile
```

-	Layers:
	-	`sha256:4376d7e862ced143af0d704becc1baf9304a68485756d6a355863efd406c745c`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 19.4 MB (19417372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e065256cd7b480ab5186e3a0349b9720d058a5ac5c2d1fd2941eddb248eacf5`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fe35b82c60de5e4bebc51d5fd0c09fa393d47b40ec3868cea9fa7404f559b791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165329830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da7b10fc14d76599309dc12df4e1a3bca15715370d2a21207226ac3e4279b92`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:00 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 21:03:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0639bafbbdc971f48d3d9341ef1217810bc7f8a0f7b5f550a4de4f1eda3ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780148fe500efb9da4f54261b9798bc3826e7511b420c2f83053c80259562034`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 6.8 MB (6764969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cb309ea157ac41c9f5f3b289d2fc115949b136e8f5bc5ba4a4c5472ce2827`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 94.3 KB (94302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf0b996774010d3f153bedf3c3543d44d56ca9dacbabda918ae7803e211d095`  
		Last Modified: Wed, 15 Apr 2026 21:04:23 GMT  
		Size: 128.9 MB (128910385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19150fbc2aa4d400a4aabdcb600258de379ad9fcb5fedb3ecf7c4f62e66c76fd`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1ad1a2944a22938562bea37162eabfb98beb36768d928fd955531d45c07fe14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19406327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f272f9b35173d606b8a8a61c25c95f8b7b755c5c77582b6dc75e5de456b5bd`

```dockerfile
```

-	Layers:
	-	`sha256:310632c34a4fa1242e8505db4fca4c49193e4f3379603f36740789ad99310db5`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 19.4 MB (19391581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67e0b2637e75e5a226356dcdb3854c0275f101aa7da68f12ae67696bdafb6ff`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:c94add9c25ae32e9f6860d2351eb74a341030915279cff505d4c810324fd0561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:6831b1e9bbc4ebbac71511a3bb95bba347ce916b5cb90fb083ffd36d0296fc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171837446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01212f2377f15a1c1eba6cd117cc8c2e336b8618928d36cb864f291353eeaef`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:54:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:48 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 20:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:55:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0644559dc6b5362253940942368861ced9f603361da89c3adf2fa73b1f1d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 683.9 KB (683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5df3be57e9c4cb62447529fecd13a1ab07bdf59d8fa4cec97baabb95b4e82`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 6.8 MB (6751676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d348f5598561bd0e3f1088e2421dece24aa7886408f40050256c411670460`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 94.1 KB (94084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12fc106e828bf5ff0f53383298b088f62734575daaaa2895be3f66ba1cfb54`  
		Last Modified: Wed, 15 Apr 2026 20:56:03 GMT  
		Size: 134.6 MB (134574573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d7c739ca6a59209f2846d72bacf015f1dc13907916eed58de4d11acfffc88`  
		Last Modified: Wed, 15 Apr 2026 20:56:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:77c07fbc7e1a1d7de335637fbac2c962cf5c618356f59a251464aa3c694d868e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19431994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b396ea28e823dc7b135e760e6e7df53cb3f15fcdc707fb64dbfa0f1951911d24`

```dockerfile
```

-	Layers:
	-	`sha256:4376d7e862ced143af0d704becc1baf9304a68485756d6a355863efd406c745c`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 19.4 MB (19417372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e065256cd7b480ab5186e3a0349b9720d058a5ac5c2d1fd2941eddb248eacf5`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fe35b82c60de5e4bebc51d5fd0c09fa393d47b40ec3868cea9fa7404f559b791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165329830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da7b10fc14d76599309dc12df4e1a3bca15715370d2a21207226ac3e4279b92`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:00 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 21:03:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0639bafbbdc971f48d3d9341ef1217810bc7f8a0f7b5f550a4de4f1eda3ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780148fe500efb9da4f54261b9798bc3826e7511b420c2f83053c80259562034`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 6.8 MB (6764969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cb309ea157ac41c9f5f3b289d2fc115949b136e8f5bc5ba4a4c5472ce2827`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 94.3 KB (94302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf0b996774010d3f153bedf3c3543d44d56ca9dacbabda918ae7803e211d095`  
		Last Modified: Wed, 15 Apr 2026 21:04:23 GMT  
		Size: 128.9 MB (128910385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19150fbc2aa4d400a4aabdcb600258de379ad9fcb5fedb3ecf7c4f62e66c76fd`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1ad1a2944a22938562bea37162eabfb98beb36768d928fd955531d45c07fe14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19406327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f272f9b35173d606b8a8a61c25c95f8b7b755c5c77582b6dc75e5de456b5bd`

```dockerfile
```

-	Layers:
	-	`sha256:310632c34a4fa1242e8505db4fca4c49193e4f3379603f36740789ad99310db5`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 19.4 MB (19391581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67e0b2637e75e5a226356dcdb3854c0275f101aa7da68f12ae67696bdafb6ff`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json
