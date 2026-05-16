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
