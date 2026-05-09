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
$ docker pull ros@sha256:1b4a547378bca1b3072a06602cbeca5443e092df305f6005f3b9ddcb372edd06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:ec4ea4a624a8ea2aa3e304695731570cd47e4424980d7f00da4d172dc08a8625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263805187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc22507e1d9fb4156c141d0eab84bda63cdf2630ba2dae795bc0f03b599a526e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45ba2ee710139051388eae90cb6e670a31c05af43e98627a2d1711d2fd9c70`  
		Last Modified: Wed, 15 Apr 2026 21:46:44 GMT  
		Size: 98.2 MB (98158243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef8df8e2fe30a40fa7b72a18e14cf9ef6e7f658cfe5e0f1077ab38bf60d5318`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 393.0 KB (393032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8764faa03981d66386f3a858722bc29141e0f26d47a8445e9c9c18510df4a`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97534683f7c4591bc92e7a96a484cee7d3fc51d096d9773c164c69a4e145aa93`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.3 MB (23334771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:3a1d4de184f756d4875cf5c17f8bfff73f945992300722685ea610b5a9a03e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23851650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898ff72519f997af288d3e762d9d971a8bfaff8184b42b1877eed7fa1e58a32`

```dockerfile
```

-	Layers:
	-	`sha256:5ef4dcaba3d0d178484d71c909615ab39b4d7e81e178e2d9bd6adf27db4c44f1`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.8 MB (23835302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b674efee2131d03fd04042bd8a81991576395c935fe34d68acf0a4273a9b677`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3eea50f848d785edb3bf85720e55f0bf0ee2aa3a37c6a1eaff02c72b714cdab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256412103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8eb2286c3d648edb2de90a40affe4f8767756f6bb0b73f43410a62e344f24`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c7e9eb84bd5c3985eff3fd8415c04a41b5a94fb1a49ea566696e134c79b55`  
		Last Modified: Wed, 15 Apr 2026 21:59:18 GMT  
		Size: 95.8 MB (95795267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea249effcab0d693d068bc41ee0aed2d26a367ba55d8f7112b5371d5f6f017`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 393.0 KB (393024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f80a79325a2dd8eb06c0a86ef1bba3a0becb31cc638213b88be7d8fd8fecb3d`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d1e226215be958de1e435f8c6682297aedd0a218347bf5e08a083fb501ada`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 22.7 MB (22728119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:dc98a1629481afecf1b9ed37fbdd14ec5c419326ff8f7c00e404e38483d437c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23864804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03d64e1fe32da957e175df1bc86c273d8be2db6ee3da1c5ec223b32bfd345c9`

```dockerfile
```

-	Layers:
	-	`sha256:6446b737d0ec2d4bb1ea7ce136444d5713ef8e79dd2c20ceee3bbf4129624ed3`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 23.8 MB (23848319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e087b5b3c3d1257aba840d59f60b29e3aa5b3602397a157e08037894b9bc08`  
		Last Modified: Wed, 15 Apr 2026 21:59:14 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:70d8ab67ea4cac670db524f9e7095536aeead79f578c8142ff2b6a48e065e31a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:2d0b52aa815d3342863d3cd24e7f8065b6dfb5a0d78ac99fd7918409ce6f628a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.9 MB (955926195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2941a4d3d5c0362dc16ccabd8e7e40d6bb09bb1721107eafa1c9a75c724028d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45ba2ee710139051388eae90cb6e670a31c05af43e98627a2d1711d2fd9c70`  
		Last Modified: Wed, 15 Apr 2026 21:46:44 GMT  
		Size: 98.2 MB (98158243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef8df8e2fe30a40fa7b72a18e14cf9ef6e7f658cfe5e0f1077ab38bf60d5318`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 393.0 KB (393032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8764faa03981d66386f3a858722bc29141e0f26d47a8445e9c9c18510df4a`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97534683f7c4591bc92e7a96a484cee7d3fc51d096d9773c164c69a4e145aa93`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.3 MB (23334771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9a3a9bf9e52c568b7b527c7c37de029b686dea10aa1177245f2dac8041b415`  
		Last Modified: Wed, 15 Apr 2026 22:33:41 GMT  
		Size: 692.1 MB (692121008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c55a462df92ed03b3502ef70822be1ddd0482be24a99ead1c91371123b5c3fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58945086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24739044944ee8fc2adfd1de8571780d5f7304aa579c81c5d2f114e00b497acc`

```dockerfile
```

-	Layers:
	-	`sha256:32e0d7cc1de5ae6c59dfb166c690d781216933defd58a96686adda921631938a`  
		Last Modified: Wed, 15 Apr 2026 22:33:28 GMT  
		Size: 58.9 MB (58935734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ebace2d36cca824ead71102fbda04a247c86cbdb4d757f452630502ba49d25`  
		Last Modified: Wed, 15 Apr 2026 22:33:25 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:058beaf47da4acbe6da25a933cae828ee72f74667f6c284bf4fa3c18c0c57843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.5 MB (916499048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9f9d0fd19386a385411843e69deeea21c4eb63f303bf669dff3ecc185be1c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c7e9eb84bd5c3985eff3fd8415c04a41b5a94fb1a49ea566696e134c79b55`  
		Last Modified: Wed, 15 Apr 2026 21:59:18 GMT  
		Size: 95.8 MB (95795267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea249effcab0d693d068bc41ee0aed2d26a367ba55d8f7112b5371d5f6f017`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 393.0 KB (393024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f80a79325a2dd8eb06c0a86ef1bba3a0becb31cc638213b88be7d8fd8fecb3d`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d1e226215be958de1e435f8c6682297aedd0a218347bf5e08a083fb501ada`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 22.7 MB (22728119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9170d494e27e9dece2e37208438457682c8cfe1848dabf5889ebe7c823eb9fe`  
		Last Modified: Wed, 15 Apr 2026 22:40:14 GMT  
		Size: 660.1 MB (660086945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:64d98835332be1f2b865ebb376fe2f156c0844103afa355ccc022a17ae975784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b69be88306a1c32932f464a84f47e89ddf33777cf6c4e126887934c291b157e`

```dockerfile
```

-	Layers:
	-	`sha256:2379763680d837a98e95b5046cd024689ef1fbf0c3af75cfa42b32717172cccf`  
		Last Modified: Wed, 15 Apr 2026 22:40:03 GMT  
		Size: 58.9 MB (58920055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfe58f9b93c7484fbb92e2fd1d7cf5c0ae250ce4919bf20136c43d2b26eadc3`  
		Last Modified: Wed, 15 Apr 2026 22:40:00 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:70d8ab67ea4cac670db524f9e7095536aeead79f578c8142ff2b6a48e065e31a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:2d0b52aa815d3342863d3cd24e7f8065b6dfb5a0d78ac99fd7918409ce6f628a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.9 MB (955926195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2941a4d3d5c0362dc16ccabd8e7e40d6bb09bb1721107eafa1c9a75c724028d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45ba2ee710139051388eae90cb6e670a31c05af43e98627a2d1711d2fd9c70`  
		Last Modified: Wed, 15 Apr 2026 21:46:44 GMT  
		Size: 98.2 MB (98158243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef8df8e2fe30a40fa7b72a18e14cf9ef6e7f658cfe5e0f1077ab38bf60d5318`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 393.0 KB (393032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8764faa03981d66386f3a858722bc29141e0f26d47a8445e9c9c18510df4a`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97534683f7c4591bc92e7a96a484cee7d3fc51d096d9773c164c69a4e145aa93`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.3 MB (23334771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9a3a9bf9e52c568b7b527c7c37de029b686dea10aa1177245f2dac8041b415`  
		Last Modified: Wed, 15 Apr 2026 22:33:41 GMT  
		Size: 692.1 MB (692121008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:c55a462df92ed03b3502ef70822be1ddd0482be24a99ead1c91371123b5c3fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58945086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24739044944ee8fc2adfd1de8571780d5f7304aa579c81c5d2f114e00b497acc`

```dockerfile
```

-	Layers:
	-	`sha256:32e0d7cc1de5ae6c59dfb166c690d781216933defd58a96686adda921631938a`  
		Last Modified: Wed, 15 Apr 2026 22:33:28 GMT  
		Size: 58.9 MB (58935734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ebace2d36cca824ead71102fbda04a247c86cbdb4d757f452630502ba49d25`  
		Last Modified: Wed, 15 Apr 2026 22:33:25 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:058beaf47da4acbe6da25a933cae828ee72f74667f6c284bf4fa3c18c0c57843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.5 MB (916499048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9f9d0fd19386a385411843e69deeea21c4eb63f303bf669dff3ecc185be1c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c7e9eb84bd5c3985eff3fd8415c04a41b5a94fb1a49ea566696e134c79b55`  
		Last Modified: Wed, 15 Apr 2026 21:59:18 GMT  
		Size: 95.8 MB (95795267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea249effcab0d693d068bc41ee0aed2d26a367ba55d8f7112b5371d5f6f017`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 393.0 KB (393024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f80a79325a2dd8eb06c0a86ef1bba3a0becb31cc638213b88be7d8fd8fecb3d`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d1e226215be958de1e435f8c6682297aedd0a218347bf5e08a083fb501ada`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 22.7 MB (22728119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9170d494e27e9dece2e37208438457682c8cfe1848dabf5889ebe7c823eb9fe`  
		Last Modified: Wed, 15 Apr 2026 22:40:14 GMT  
		Size: 660.1 MB (660086945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:64d98835332be1f2b865ebb376fe2f156c0844103afa355ccc022a17ae975784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b69be88306a1c32932f464a84f47e89ddf33777cf6c4e126887934c291b157e`

```dockerfile
```

-	Layers:
	-	`sha256:2379763680d837a98e95b5046cd024689ef1fbf0c3af75cfa42b32717172cccf`  
		Last Modified: Wed, 15 Apr 2026 22:40:03 GMT  
		Size: 58.9 MB (58920055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfe58f9b93c7484fbb92e2fd1d7cf5c0ae250ce4919bf20136c43d2b26eadc3`  
		Last Modified: Wed, 15 Apr 2026 22:40:00 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:1b4a547378bca1b3072a06602cbeca5443e092df305f6005f3b9ddcb372edd06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:ec4ea4a624a8ea2aa3e304695731570cd47e4424980d7f00da4d172dc08a8625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263805187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc22507e1d9fb4156c141d0eab84bda63cdf2630ba2dae795bc0f03b599a526e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45ba2ee710139051388eae90cb6e670a31c05af43e98627a2d1711d2fd9c70`  
		Last Modified: Wed, 15 Apr 2026 21:46:44 GMT  
		Size: 98.2 MB (98158243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef8df8e2fe30a40fa7b72a18e14cf9ef6e7f658cfe5e0f1077ab38bf60d5318`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 393.0 KB (393032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8764faa03981d66386f3a858722bc29141e0f26d47a8445e9c9c18510df4a`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97534683f7c4591bc92e7a96a484cee7d3fc51d096d9773c164c69a4e145aa93`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.3 MB (23334771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:3a1d4de184f756d4875cf5c17f8bfff73f945992300722685ea610b5a9a03e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23851650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898ff72519f997af288d3e762d9d971a8bfaff8184b42b1877eed7fa1e58a32`

```dockerfile
```

-	Layers:
	-	`sha256:5ef4dcaba3d0d178484d71c909615ab39b4d7e81e178e2d9bd6adf27db4c44f1`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.8 MB (23835302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b674efee2131d03fd04042bd8a81991576395c935fe34d68acf0a4273a9b677`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3eea50f848d785edb3bf85720e55f0bf0ee2aa3a37c6a1eaff02c72b714cdab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256412103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8eb2286c3d648edb2de90a40affe4f8767756f6bb0b73f43410a62e344f24`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c7e9eb84bd5c3985eff3fd8415c04a41b5a94fb1a49ea566696e134c79b55`  
		Last Modified: Wed, 15 Apr 2026 21:59:18 GMT  
		Size: 95.8 MB (95795267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea249effcab0d693d068bc41ee0aed2d26a367ba55d8f7112b5371d5f6f017`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 393.0 KB (393024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f80a79325a2dd8eb06c0a86ef1bba3a0becb31cc638213b88be7d8fd8fecb3d`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d1e226215be958de1e435f8c6682297aedd0a218347bf5e08a083fb501ada`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 22.7 MB (22728119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:dc98a1629481afecf1b9ed37fbdd14ec5c419326ff8f7c00e404e38483d437c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23864804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03d64e1fe32da957e175df1bc86c273d8be2db6ee3da1c5ec223b32bfd345c9`

```dockerfile
```

-	Layers:
	-	`sha256:6446b737d0ec2d4bb1ea7ce136444d5713ef8e79dd2c20ceee3bbf4129624ed3`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 23.8 MB (23848319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e087b5b3c3d1257aba840d59f60b29e3aa5b3602397a157e08037894b9bc08`  
		Last Modified: Wed, 15 Apr 2026 21:59:14 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:1b4a547378bca1b3072a06602cbeca5443e092df305f6005f3b9ddcb372edd06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:ec4ea4a624a8ea2aa3e304695731570cd47e4424980d7f00da4d172dc08a8625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263805187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc22507e1d9fb4156c141d0eab84bda63cdf2630ba2dae795bc0f03b599a526e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45ba2ee710139051388eae90cb6e670a31c05af43e98627a2d1711d2fd9c70`  
		Last Modified: Wed, 15 Apr 2026 21:46:44 GMT  
		Size: 98.2 MB (98158243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef8df8e2fe30a40fa7b72a18e14cf9ef6e7f658cfe5e0f1077ab38bf60d5318`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 393.0 KB (393032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8764faa03981d66386f3a858722bc29141e0f26d47a8445e9c9c18510df4a`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97534683f7c4591bc92e7a96a484cee7d3fc51d096d9773c164c69a4e145aa93`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.3 MB (23334771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:3a1d4de184f756d4875cf5c17f8bfff73f945992300722685ea610b5a9a03e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23851650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1898ff72519f997af288d3e762d9d971a8bfaff8184b42b1877eed7fa1e58a32`

```dockerfile
```

-	Layers:
	-	`sha256:5ef4dcaba3d0d178484d71c909615ab39b4d7e81e178e2d9bd6adf27db4c44f1`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.8 MB (23835302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b674efee2131d03fd04042bd8a81991576395c935fe34d68acf0a4273a9b677`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3eea50f848d785edb3bf85720e55f0bf0ee2aa3a37c6a1eaff02c72b714cdab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256412103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a8eb2286c3d648edb2de90a40affe4f8767756f6bb0b73f43410a62e344f24`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c7e9eb84bd5c3985eff3fd8415c04a41b5a94fb1a49ea566696e134c79b55`  
		Last Modified: Wed, 15 Apr 2026 21:59:18 GMT  
		Size: 95.8 MB (95795267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea249effcab0d693d068bc41ee0aed2d26a367ba55d8f7112b5371d5f6f017`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 393.0 KB (393024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f80a79325a2dd8eb06c0a86ef1bba3a0becb31cc638213b88be7d8fd8fecb3d`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d1e226215be958de1e435f8c6682297aedd0a218347bf5e08a083fb501ada`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 22.7 MB (22728119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:dc98a1629481afecf1b9ed37fbdd14ec5c419326ff8f7c00e404e38483d437c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23864804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03d64e1fe32da957e175df1bc86c273d8be2db6ee3da1c5ec223b32bfd345c9`

```dockerfile
```

-	Layers:
	-	`sha256:6446b737d0ec2d4bb1ea7ce136444d5713ef8e79dd2c20ceee3bbf4129624ed3`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 23.8 MB (23848319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e087b5b3c3d1257aba840d59f60b29e3aa5b3602397a157e08037894b9bc08`  
		Last Modified: Wed, 15 Apr 2026 21:59:14 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:6692e2470f6f2ff0b35190b695ca6129345f6981bb53da62d91fafb3e982ceac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:a115d56b8bbbfd9f7f95e3b8c40da8a677403521a514386ceb7bdc48e18a76aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141916625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe11fb97e089bf8e581566803823aa40d2d1b629dbb84d89579009b61aba8d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6629137527899e2d686ca245175881accb128d96bea80b6e4819ffee14ed6767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e55a0caf0d52b742cace530a80d8332ba22b3066adb296aec162298bbed4f4`

```dockerfile
```

-	Layers:
	-	`sha256:79794308a686f8f07a4cf67445e845e0688932249c15cd56d1dae88115b25ee5`  
		Last Modified: Wed, 15 Apr 2026 20:55:12 GMT  
		Size: 17.8 MB (17802889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f87e84b20dd3533c31e8c940cdcfe1155a139d26860bdb4d1dee7c1ccfe11e`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 14.6 KB (14612 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:55d9908102dd6ff2d2184aa9b0c4e8a51e91117b42304f781a0f44ef0236e1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137493180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe4e59fd18c89523d45efb0bfac536f00b854d6abb82ddb802113c34bd79878`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:311ea494555619bde2709c2f93d4965b663c4176fabc2849697d12b365222d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58206d88fcbae8b27c8a7dbbedf203c85d091d7a2d48717eb15bfcc130a47feb`

```dockerfile
```

-	Layers:
	-	`sha256:afb861e8bd8684f76b4fa477b37bc36fd2c4766e39a917d8bfa8e9b3dc916718`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 17.8 MB (17789234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647ff0c8d1a703bc44c581bbf630b1ea86e9bd916a7adb386b722a0210413120`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:6692e2470f6f2ff0b35190b695ca6129345f6981bb53da62d91fafb3e982ceac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:a115d56b8bbbfd9f7f95e3b8c40da8a677403521a514386ceb7bdc48e18a76aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141916625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe11fb97e089bf8e581566803823aa40d2d1b629dbb84d89579009b61aba8d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:6629137527899e2d686ca245175881accb128d96bea80b6e4819ffee14ed6767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e55a0caf0d52b742cace530a80d8332ba22b3066adb296aec162298bbed4f4`

```dockerfile
```

-	Layers:
	-	`sha256:79794308a686f8f07a4cf67445e845e0688932249c15cd56d1dae88115b25ee5`  
		Last Modified: Wed, 15 Apr 2026 20:55:12 GMT  
		Size: 17.8 MB (17802889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f87e84b20dd3533c31e8c940cdcfe1155a139d26860bdb4d1dee7c1ccfe11e`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 14.6 KB (14612 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:55d9908102dd6ff2d2184aa9b0c4e8a51e91117b42304f781a0f44ef0236e1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137493180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe4e59fd18c89523d45efb0bfac536f00b854d6abb82ddb802113c34bd79878`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:311ea494555619bde2709c2f93d4965b663c4176fabc2849697d12b365222d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58206d88fcbae8b27c8a7dbbedf203c85d091d7a2d48717eb15bfcc130a47feb`

```dockerfile
```

-	Layers:
	-	`sha256:afb861e8bd8684f76b4fa477b37bc36fd2c4766e39a917d8bfa8e9b3dc916718`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 17.8 MB (17789234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647ff0c8d1a703bc44c581bbf630b1ea86e9bd916a7adb386b722a0210413120`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:e9b9b98c1a867673789dfa1cb622b780e1ae6e5a0c235b0340d83c2b46f6171c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:d1488d3b99ecd0edaec8349682bc1eadf11bc5b4dc266b3eaaeda8787a724cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296302721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f4249e792af1be98e76d5e3b71faa7086aaeb9f5a90e902c9461a6ac3e673`
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
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb934869c0062075d3924ee67ff17ece2c114ca0ce2144abe6c484a11464706b`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 110.2 MB (110191800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41de78adfb4b31cd70fec97b302a53039d85ae134cb88b28504b1a8f234d3f6a`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 406.0 KB (406035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56562b7711ce2dc52c7a11d2b429e85a9c969d469ef5eaf0530876ced6355d92`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238e0cbb8a4936a6230dd0b4e08a4fb91563787eabed4ed52c321cb254083f5`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 28.3 MB (28253633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:1dccc7efac09ea940614476c7a5b547d0ef600abe39ff4f2836923babfcd25ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24817696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0d92dd7d19f29c32c1ea2755842da2a2ab1183a28da09c0b6be052ca7097b7`

```dockerfile
```

-	Layers:
	-	`sha256:d6e28e9d8dc85665aed292205faba4faf500071be01e8d54146d31de77320601`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 24.8 MB (24801075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161d4f87e7b6311a1d2e9ab5aec66c322fd54084eb76940be809f7203137a561`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:75f904e512850c074a09b2fcad02f42496358ddedb14b0fb2844b2d063b67f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284743559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed588b014ed59b43c6e00b7ee5394c98c3119afdba85eff2e4e21702aa9ba296`
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
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b1652e06603234b577f2609a4675b0d8db5ae2bc8e9a76c212aa8372ec83b`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 105.6 MB (105603863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b1a61548270d1f294994d9d5c6b7ef600aa93cf0406dd697efd56a47fcaeef`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 406.0 KB (406033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab229f387e85cf75d9d2c2b9a816695857692067ddf66c147963519b872f6edd`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9fea2d7bdf03859ee3389c8beb5c8fa13ae0d91f3d7eb8ea185f0dcb5cbda`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 27.3 MB (27343654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:2842848376e0b5ae10b35caa0c4bd0f000c55c92fa8ad83d98caa6e544e4ee02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24840114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bed213097eed21c0c47f4129b1dccd0b3629c656c299a11fbb8324b0ccba2`

```dockerfile
```

-	Layers:
	-	`sha256:27fbf0cacc0c47420fa070f1a46d1c49be69a3b5d6cbba50e355ee22c06e4031`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 24.8 MB (24823344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7348e7326134d81c2a173b26a0de6babefbb17960b8fedb1bf5b857964d25364`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:29a62aed6ef63bdaddf44cfc1b7450c46019c5115b143b6a43ef60e0bbadcbf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:785e3523795c0adcd9589c3ec81ffdb5633748c103699c9a7378e1c5554bdb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080858776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4010bcc04ec130643e20154991f087f2f8c339e1055086f971ea5b59ec137ab6`
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
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb934869c0062075d3924ee67ff17ece2c114ca0ce2144abe6c484a11464706b`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 110.2 MB (110191800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41de78adfb4b31cd70fec97b302a53039d85ae134cb88b28504b1a8f234d3f6a`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 406.0 KB (406035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56562b7711ce2dc52c7a11d2b429e85a9c969d469ef5eaf0530876ced6355d92`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238e0cbb8a4936a6230dd0b4e08a4fb91563787eabed4ed52c321cb254083f5`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 28.3 MB (28253633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3d5793cf19f8d8069608d8e87dae2c4eae72e0c890187a944c2510d753d95f`  
		Last Modified: Wed, 15 Apr 2026 22:32:23 GMT  
		Size: 784.6 MB (784556055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:a14355e57eed7747efa4f7048777789883e9893fca6321961d3b9521411e1bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60978187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eeaf2eb2d7a04518afbc17d34f110e4d13c0b6b246d83236b2638001ac67be`

```dockerfile
```

-	Layers:
	-	`sha256:70b10207c8104daa621e4757e764b3f8db982ed8c5d169aedbfee21fb5d8a296`  
		Last Modified: Wed, 15 Apr 2026 22:32:04 GMT  
		Size: 61.0 MB (60968849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be47fcbe8309e1f93ff259c93f02e67d6828ade5651dcc478961db45df8c258e`  
		Last Modified: Wed, 15 Apr 2026 22:32:01 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4b857ae12a8171bcfd6a9edb975fe5c9cec9b2b052cceb3847d376b03c514b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.5 MB (983486943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a122d53d86c230c37fc5f21fdafe09fef6c6c994591a2e322ad29f7407c935c8`
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
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b1652e06603234b577f2609a4675b0d8db5ae2bc8e9a76c212aa8372ec83b`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 105.6 MB (105603863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b1a61548270d1f294994d9d5c6b7ef600aa93cf0406dd697efd56a47fcaeef`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 406.0 KB (406033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab229f387e85cf75d9d2c2b9a816695857692067ddf66c147963519b872f6edd`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9fea2d7bdf03859ee3389c8beb5c8fa13ae0d91f3d7eb8ea185f0dcb5cbda`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 27.3 MB (27343654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66526070dc88a16887fa155319e571a0bd7f8c249066944c0ec2e53646e2ff5e`  
		Last Modified: Wed, 15 Apr 2026 22:40:53 GMT  
		Size: 698.7 MB (698743384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e764d6b3e596e57a32f2910bd5cbe3e4e850138462742ff450f4889ab34e782b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60908783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9904456d1e64c4c85290a928980388d58140c41fa568c08a6f04ad7d4830d5dd`

```dockerfile
```

-	Layers:
	-	`sha256:047888e96168e6a93962e56186aa92edaea683addd34711e5d87b0d8a6abf88f`  
		Last Modified: Wed, 15 Apr 2026 22:40:39 GMT  
		Size: 60.9 MB (60899365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f564481ff937fbb44528eb5f3e2847c8f77ebbb3b7bfcc2814a8465e25883310`  
		Last Modified: Wed, 15 Apr 2026 22:40:36 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:29a62aed6ef63bdaddf44cfc1b7450c46019c5115b143b6a43ef60e0bbadcbf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:785e3523795c0adcd9589c3ec81ffdb5633748c103699c9a7378e1c5554bdb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080858776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4010bcc04ec130643e20154991f087f2f8c339e1055086f971ea5b59ec137ab6`
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
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb934869c0062075d3924ee67ff17ece2c114ca0ce2144abe6c484a11464706b`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 110.2 MB (110191800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41de78adfb4b31cd70fec97b302a53039d85ae134cb88b28504b1a8f234d3f6a`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 406.0 KB (406035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56562b7711ce2dc52c7a11d2b429e85a9c969d469ef5eaf0530876ced6355d92`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238e0cbb8a4936a6230dd0b4e08a4fb91563787eabed4ed52c321cb254083f5`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 28.3 MB (28253633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3d5793cf19f8d8069608d8e87dae2c4eae72e0c890187a944c2510d753d95f`  
		Last Modified: Wed, 15 Apr 2026 22:32:23 GMT  
		Size: 784.6 MB (784556055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a14355e57eed7747efa4f7048777789883e9893fca6321961d3b9521411e1bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60978187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eeaf2eb2d7a04518afbc17d34f110e4d13c0b6b246d83236b2638001ac67be`

```dockerfile
```

-	Layers:
	-	`sha256:70b10207c8104daa621e4757e764b3f8db982ed8c5d169aedbfee21fb5d8a296`  
		Last Modified: Wed, 15 Apr 2026 22:32:04 GMT  
		Size: 61.0 MB (60968849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be47fcbe8309e1f93ff259c93f02e67d6828ade5651dcc478961db45df8c258e`  
		Last Modified: Wed, 15 Apr 2026 22:32:01 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4b857ae12a8171bcfd6a9edb975fe5c9cec9b2b052cceb3847d376b03c514b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.5 MB (983486943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a122d53d86c230c37fc5f21fdafe09fef6c6c994591a2e322ad29f7407c935c8`
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
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b1652e06603234b577f2609a4675b0d8db5ae2bc8e9a76c212aa8372ec83b`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 105.6 MB (105603863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b1a61548270d1f294994d9d5c6b7ef600aa93cf0406dd697efd56a47fcaeef`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 406.0 KB (406033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab229f387e85cf75d9d2c2b9a816695857692067ddf66c147963519b872f6edd`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9fea2d7bdf03859ee3389c8beb5c8fa13ae0d91f3d7eb8ea185f0dcb5cbda`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 27.3 MB (27343654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66526070dc88a16887fa155319e571a0bd7f8c249066944c0ec2e53646e2ff5e`  
		Last Modified: Wed, 15 Apr 2026 22:40:53 GMT  
		Size: 698.7 MB (698743384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e764d6b3e596e57a32f2910bd5cbe3e4e850138462742ff450f4889ab34e782b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60908783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9904456d1e64c4c85290a928980388d58140c41fa568c08a6f04ad7d4830d5dd`

```dockerfile
```

-	Layers:
	-	`sha256:047888e96168e6a93962e56186aa92edaea683addd34711e5d87b0d8a6abf88f`  
		Last Modified: Wed, 15 Apr 2026 22:40:39 GMT  
		Size: 60.9 MB (60899365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f564481ff937fbb44528eb5f3e2847c8f77ebbb3b7bfcc2814a8465e25883310`  
		Last Modified: Wed, 15 Apr 2026 22:40:36 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:e9b9b98c1a867673789dfa1cb622b780e1ae6e5a0c235b0340d83c2b46f6171c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d1488d3b99ecd0edaec8349682bc1eadf11bc5b4dc266b3eaaeda8787a724cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296302721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f4249e792af1be98e76d5e3b71faa7086aaeb9f5a90e902c9461a6ac3e673`
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
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb934869c0062075d3924ee67ff17ece2c114ca0ce2144abe6c484a11464706b`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 110.2 MB (110191800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41de78adfb4b31cd70fec97b302a53039d85ae134cb88b28504b1a8f234d3f6a`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 406.0 KB (406035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56562b7711ce2dc52c7a11d2b429e85a9c969d469ef5eaf0530876ced6355d92`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238e0cbb8a4936a6230dd0b4e08a4fb91563787eabed4ed52c321cb254083f5`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 28.3 MB (28253633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:1dccc7efac09ea940614476c7a5b547d0ef600abe39ff4f2836923babfcd25ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24817696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0d92dd7d19f29c32c1ea2755842da2a2ab1183a28da09c0b6be052ca7097b7`

```dockerfile
```

-	Layers:
	-	`sha256:d6e28e9d8dc85665aed292205faba4faf500071be01e8d54146d31de77320601`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 24.8 MB (24801075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161d4f87e7b6311a1d2e9ab5aec66c322fd54084eb76940be809f7203137a561`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:75f904e512850c074a09b2fcad02f42496358ddedb14b0fb2844b2d063b67f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284743559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed588b014ed59b43c6e00b7ee5394c98c3119afdba85eff2e4e21702aa9ba296`
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
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b1652e06603234b577f2609a4675b0d8db5ae2bc8e9a76c212aa8372ec83b`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 105.6 MB (105603863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b1a61548270d1f294994d9d5c6b7ef600aa93cf0406dd697efd56a47fcaeef`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 406.0 KB (406033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab229f387e85cf75d9d2c2b9a816695857692067ddf66c147963519b872f6edd`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9fea2d7bdf03859ee3389c8beb5c8fa13ae0d91f3d7eb8ea185f0dcb5cbda`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 27.3 MB (27343654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:2842848376e0b5ae10b35caa0c4bd0f000c55c92fa8ad83d98caa6e544e4ee02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24840114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bed213097eed21c0c47f4129b1dccd0b3629c656c299a11fbb8324b0ccba2`

```dockerfile
```

-	Layers:
	-	`sha256:27fbf0cacc0c47420fa070f1a46d1c49be69a3b5d6cbba50e355ee22c06e4031`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 24.8 MB (24823344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7348e7326134d81c2a173b26a0de6babefbb17960b8fedb1bf5b857964d25364`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:e9b9b98c1a867673789dfa1cb622b780e1ae6e5a0c235b0340d83c2b46f6171c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:d1488d3b99ecd0edaec8349682bc1eadf11bc5b4dc266b3eaaeda8787a724cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296302721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f4249e792af1be98e76d5e3b71faa7086aaeb9f5a90e902c9461a6ac3e673`
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
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb934869c0062075d3924ee67ff17ece2c114ca0ce2144abe6c484a11464706b`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 110.2 MB (110191800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41de78adfb4b31cd70fec97b302a53039d85ae134cb88b28504b1a8f234d3f6a`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 406.0 KB (406035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56562b7711ce2dc52c7a11d2b429e85a9c969d469ef5eaf0530876ced6355d92`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238e0cbb8a4936a6230dd0b4e08a4fb91563787eabed4ed52c321cb254083f5`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 28.3 MB (28253633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1dccc7efac09ea940614476c7a5b547d0ef600abe39ff4f2836923babfcd25ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24817696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0d92dd7d19f29c32c1ea2755842da2a2ab1183a28da09c0b6be052ca7097b7`

```dockerfile
```

-	Layers:
	-	`sha256:d6e28e9d8dc85665aed292205faba4faf500071be01e8d54146d31de77320601`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 24.8 MB (24801075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161d4f87e7b6311a1d2e9ab5aec66c322fd54084eb76940be809f7203137a561`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:75f904e512850c074a09b2fcad02f42496358ddedb14b0fb2844b2d063b67f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284743559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed588b014ed59b43c6e00b7ee5394c98c3119afdba85eff2e4e21702aa9ba296`
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
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b1652e06603234b577f2609a4675b0d8db5ae2bc8e9a76c212aa8372ec83b`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 105.6 MB (105603863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b1a61548270d1f294994d9d5c6b7ef600aa93cf0406dd697efd56a47fcaeef`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 406.0 KB (406033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab229f387e85cf75d9d2c2b9a816695857692067ddf66c147963519b872f6edd`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9fea2d7bdf03859ee3389c8beb5c8fa13ae0d91f3d7eb8ea185f0dcb5cbda`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 27.3 MB (27343654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:2842848376e0b5ae10b35caa0c4bd0f000c55c92fa8ad83d98caa6e544e4ee02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24840114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bed213097eed21c0c47f4129b1dccd0b3629c656c299a11fbb8324b0ccba2`

```dockerfile
```

-	Layers:
	-	`sha256:27fbf0cacc0c47420fa070f1a46d1c49be69a3b5d6cbba50e355ee22c06e4031`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 24.8 MB (24823344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7348e7326134d81c2a173b26a0de6babefbb17960b8fedb1bf5b857964d25364`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:096dd6d816e697d0019c5cb359b37dae356937e4fd1ebcb27731a4997eff6973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:25ecd0066934e6385aef56ee218dc994fcc1f9ff9b45b4ab64a0f0fad50aa10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157448749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26241c9bcab8ee0d629bd9279ed24e4fd0fafc381bbd07a620966a6761ae0a0c`
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
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:132ccfee487ce76a1e79ab32fa9725a32fc9a0a015f1750a543fa5c13c2e3874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18498532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f607aed76ab4844e22e466f8a170291b8867979666edc49ebd78f1997069a6df`

```dockerfile
```

-	Layers:
	-	`sha256:7eee6ca82fd9a65f91eb19bc884dfb004ca9665fd3121ce4082a08244db23b8c`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 18.5 MB (18483934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789ea6ed1a0e01d9a9ab602effa6e351200a1d147cbf9d423d0dd6b6ab3f1ce8`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 14.6 KB (14598 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c80d117901cff9715cbee9b285e314d327632ef44805c7ffe4213fda7bc386e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151387522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94f6cd7a79da8082a6e3ec37299cc5ce99b5ff913b1ca6766d644e4f5706bfb`
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
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f03d27308a75556d0e50919fc87a82d6039591164c629953b7c74777a1c1d46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18472665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83656f21c4b1b74f39333035358b405b25ef25047378a831895f6737cfd038`

```dockerfile
```

-	Layers:
	-	`sha256:ce62b64a061062955d40fa45ead6428baa6f9b304c59c72fcb21c77992a6ca68`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 18.5 MB (18457940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06119fdc43365ceec6d77dfaecffd6bd8ebe35eb78d15b94345784b30481cee`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:096dd6d816e697d0019c5cb359b37dae356937e4fd1ebcb27731a4997eff6973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:25ecd0066934e6385aef56ee218dc994fcc1f9ff9b45b4ab64a0f0fad50aa10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157448749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26241c9bcab8ee0d629bd9279ed24e4fd0fafc381bbd07a620966a6761ae0a0c`
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
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:132ccfee487ce76a1e79ab32fa9725a32fc9a0a015f1750a543fa5c13c2e3874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18498532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f607aed76ab4844e22e466f8a170291b8867979666edc49ebd78f1997069a6df`

```dockerfile
```

-	Layers:
	-	`sha256:7eee6ca82fd9a65f91eb19bc884dfb004ca9665fd3121ce4082a08244db23b8c`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 18.5 MB (18483934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789ea6ed1a0e01d9a9ab602effa6e351200a1d147cbf9d423d0dd6b6ab3f1ce8`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 14.6 KB (14598 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c80d117901cff9715cbee9b285e314d327632ef44805c7ffe4213fda7bc386e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151387522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94f6cd7a79da8082a6e3ec37299cc5ce99b5ff913b1ca6766d644e4f5706bfb`
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
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f03d27308a75556d0e50919fc87a82d6039591164c629953b7c74777a1c1d46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18472665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83656f21c4b1b74f39333035358b405b25ef25047378a831895f6737cfd038`

```dockerfile
```

-	Layers:
	-	`sha256:ce62b64a061062955d40fa45ead6428baa6f9b304c59c72fcb21c77992a6ca68`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 18.5 MB (18457940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06119fdc43365ceec6d77dfaecffd6bd8ebe35eb78d15b94345784b30481cee`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:09fc4eafc58d55baba80fa2179761af87a1a24586c88049e5a2f2a76215b2071
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:711c35fa022e029585c6bd0445cd4e90a64d147945e93f0d17e8658dada9edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296822799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f3e53ea06654ca18393a63c24bf43ef1f2273575e6b31000eac328d06b568`
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
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b585e3d82ffce0664bce0c8a5cd547fab5ca89e846fcded5bfdea2945c92b0e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 110.2 MB (110194522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d9e768ed960260076e36fb5349f0f2bf428da3dd7ca881955f651442db85d`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 379.8 KB (379842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42645bfe1400d71c15649094acea6a941875adfdfbfdcdf5da5a0cf7329e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740609d32d16cf76c7d87805eff7096e854a1b987b669162d4caf38ef205d04`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 28.1 MB (28074461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:d5936346f135b582a261511d5983f9753ba160d0e43bb40ab9f5197266174b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd670b4353b1ad937dc8af910e89de70ce1a49678f9e5b3e4dce0f1951471a64`

```dockerfile
```

-	Layers:
	-	`sha256:420c0d5f20dafba09120bcbd505d4a20dd050524f990d868e4ef6c8fae194468`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 24.8 MB (24750608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d4c3744b9b9428d48825b5d40907bd738a9f30e5032264b201a51cf55221a6`  
		Last Modified: Wed, 15 Apr 2026 21:46:51 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cf195d400ea1b9522336650a09081c2b9bbd58c4567abaf065ae033d6c461831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285201575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e0b5a1092889590aeb2db6c88a896e4c0ec19dea93f92f768959ffdc096016`
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
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005d2616fb0134c4e667bf18779a12515e093b7032480fa955cae8082b1ed00`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 105.6 MB (105606696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c761530a5f45bde84b650345ffc0508fcb42841ff5090e705b63da0fe1389fdc`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 379.8 KB (379849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf27eb0b81b347de06b64c5b5e76195336cec112119695b36d7718b2e4e07b3c`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 2.5 KB (2545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00b01c95a9e75af81929c29b402746eb47e5ae30c7836299919af679dc2fe7`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 27.2 MB (27159941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:a574bc9e18529c423a7eed4fc7c73966ca33d7573d7547e9c5fcd2d59ffdc36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37c1c3d7e653759b7faf430a8ef65f87120f742604c33691af856b141fe6b90`

```dockerfile
```

-	Layers:
	-	`sha256:a70c674dcb660d44b806bb08907a34c2fb46f5a40eab10a7b9b0b205bb907724`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 24.8 MB (24772870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655d938644d51b7909a0fc104ddd54b1fd9b8353f9a4d630fcfb58e3840172eb`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:2055c0120e6fd8d6662c450fd8c9746c349a0d9c6e1cce3030f852d06618bf27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:dd682ae4e08bb96dcfc6dff6e2bca25ea3915154586f7ab6aab30058e6315fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081432609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7348d9cf4178bc7c9ce2dcaa5d5fb7a497c176f829241f6462de5f9a8bb79cb2`
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
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b585e3d82ffce0664bce0c8a5cd547fab5ca89e846fcded5bfdea2945c92b0e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 110.2 MB (110194522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d9e768ed960260076e36fb5349f0f2bf428da3dd7ca881955f651442db85d`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 379.8 KB (379842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42645bfe1400d71c15649094acea6a941875adfdfbfdcdf5da5a0cf7329e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740609d32d16cf76c7d87805eff7096e854a1b987b669162d4caf38ef205d04`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 28.1 MB (28074461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e1a4f7ac439011b9742367eb967d6d84afb4296b45e3baf0177fe657416ca4`  
		Last Modified: Wed, 15 Apr 2026 22:32:59 GMT  
		Size: 784.6 MB (784609810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9bb1691b6c8bda914acbde13ac6e67853cf23b1094802c42378bcb5e1e0c463e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60936687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d1b39c7bc48d12c18024b0a74e66445fcda50e21c5a68c36fa019a866f21f9`

```dockerfile
```

-	Layers:
	-	`sha256:1e278c0f0f182591f8ab3e55bc03fd20721793f3459a8420f332cb17ff93fbbf`  
		Last Modified: Wed, 15 Apr 2026 22:32:42 GMT  
		Size: 60.9 MB (60927336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed143f06f6ccc96627a9fdae7240f16c6ceae5e0e1b251818da1e86386b44b88`  
		Last Modified: Wed, 15 Apr 2026 22:32:39 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:37c7a50cb69db09a48cdef703cf232250801a6a3f84754f6d5ae51ff0e9c8460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 MB (983992526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1fb1c2968fdba99837795ed9505a8e58e91e78fa4fbac541f06a69032bab14`
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
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005d2616fb0134c4e667bf18779a12515e093b7032480fa955cae8082b1ed00`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 105.6 MB (105606696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c761530a5f45bde84b650345ffc0508fcb42841ff5090e705b63da0fe1389fdc`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 379.8 KB (379849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf27eb0b81b347de06b64c5b5e76195336cec112119695b36d7718b2e4e07b3c`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 2.5 KB (2545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00b01c95a9e75af81929c29b402746eb47e5ae30c7836299919af679dc2fe7`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 27.2 MB (27159941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb2d57d9b6531470bcaa5ec13f20c40e645ddb5ed8bf5f6ed3d0d0fc1e9e16`  
		Last Modified: Wed, 15 Apr 2026 22:40:48 GMT  
		Size: 698.8 MB (698790951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:164b7cebbfd5cbb0aebbe7662898de3b590171fa7a6c8ddaeb6abf9d0a7fe993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60867289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0613531574d30ce6d022b0641b1d53dc85eae0100a098dcac0962b8386960`

```dockerfile
```

-	Layers:
	-	`sha256:e0346651bfe269c2ae312325647afa7b3680071fb67669c8c98a3aa8961a8603`  
		Last Modified: Wed, 15 Apr 2026 22:40:29 GMT  
		Size: 60.9 MB (60857857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ca0d0c0395f7fddc186c9cf92000b993cb743201673e179aca9ebc46f2b612`  
		Last Modified: Wed, 15 Apr 2026 22:40:27 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:2055c0120e6fd8d6662c450fd8c9746c349a0d9c6e1cce3030f852d06618bf27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:dd682ae4e08bb96dcfc6dff6e2bca25ea3915154586f7ab6aab30058e6315fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081432609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7348d9cf4178bc7c9ce2dcaa5d5fb7a497c176f829241f6462de5f9a8bb79cb2`
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
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b585e3d82ffce0664bce0c8a5cd547fab5ca89e846fcded5bfdea2945c92b0e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 110.2 MB (110194522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d9e768ed960260076e36fb5349f0f2bf428da3dd7ca881955f651442db85d`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 379.8 KB (379842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42645bfe1400d71c15649094acea6a941875adfdfbfdcdf5da5a0cf7329e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740609d32d16cf76c7d87805eff7096e854a1b987b669162d4caf38ef205d04`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 28.1 MB (28074461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e1a4f7ac439011b9742367eb967d6d84afb4296b45e3baf0177fe657416ca4`  
		Last Modified: Wed, 15 Apr 2026 22:32:59 GMT  
		Size: 784.6 MB (784609810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9bb1691b6c8bda914acbde13ac6e67853cf23b1094802c42378bcb5e1e0c463e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60936687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d1b39c7bc48d12c18024b0a74e66445fcda50e21c5a68c36fa019a866f21f9`

```dockerfile
```

-	Layers:
	-	`sha256:1e278c0f0f182591f8ab3e55bc03fd20721793f3459a8420f332cb17ff93fbbf`  
		Last Modified: Wed, 15 Apr 2026 22:32:42 GMT  
		Size: 60.9 MB (60927336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed143f06f6ccc96627a9fdae7240f16c6ceae5e0e1b251818da1e86386b44b88`  
		Last Modified: Wed, 15 Apr 2026 22:32:39 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:37c7a50cb69db09a48cdef703cf232250801a6a3f84754f6d5ae51ff0e9c8460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 MB (983992526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1fb1c2968fdba99837795ed9505a8e58e91e78fa4fbac541f06a69032bab14`
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
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005d2616fb0134c4e667bf18779a12515e093b7032480fa955cae8082b1ed00`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 105.6 MB (105606696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c761530a5f45bde84b650345ffc0508fcb42841ff5090e705b63da0fe1389fdc`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 379.8 KB (379849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf27eb0b81b347de06b64c5b5e76195336cec112119695b36d7718b2e4e07b3c`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 2.5 KB (2545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00b01c95a9e75af81929c29b402746eb47e5ae30c7836299919af679dc2fe7`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 27.2 MB (27159941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb2d57d9b6531470bcaa5ec13f20c40e645ddb5ed8bf5f6ed3d0d0fc1e9e16`  
		Last Modified: Wed, 15 Apr 2026 22:40:48 GMT  
		Size: 698.8 MB (698790951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:164b7cebbfd5cbb0aebbe7662898de3b590171fa7a6c8ddaeb6abf9d0a7fe993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60867289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0613531574d30ce6d022b0641b1d53dc85eae0100a098dcac0962b8386960`

```dockerfile
```

-	Layers:
	-	`sha256:e0346651bfe269c2ae312325647afa7b3680071fb67669c8c98a3aa8961a8603`  
		Last Modified: Wed, 15 Apr 2026 22:40:29 GMT  
		Size: 60.9 MB (60857857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ca0d0c0395f7fddc186c9cf92000b993cb743201673e179aca9ebc46f2b612`  
		Last Modified: Wed, 15 Apr 2026 22:40:27 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:09fc4eafc58d55baba80fa2179761af87a1a24586c88049e5a2f2a76215b2071
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:711c35fa022e029585c6bd0445cd4e90a64d147945e93f0d17e8658dada9edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296822799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f3e53ea06654ca18393a63c24bf43ef1f2273575e6b31000eac328d06b568`
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
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b585e3d82ffce0664bce0c8a5cd547fab5ca89e846fcded5bfdea2945c92b0e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 110.2 MB (110194522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d9e768ed960260076e36fb5349f0f2bf428da3dd7ca881955f651442db85d`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 379.8 KB (379842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42645bfe1400d71c15649094acea6a941875adfdfbfdcdf5da5a0cf7329e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740609d32d16cf76c7d87805eff7096e854a1b987b669162d4caf38ef205d04`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 28.1 MB (28074461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d5936346f135b582a261511d5983f9753ba160d0e43bb40ab9f5197266174b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd670b4353b1ad937dc8af910e89de70ce1a49678f9e5b3e4dce0f1951471a64`

```dockerfile
```

-	Layers:
	-	`sha256:420c0d5f20dafba09120bcbd505d4a20dd050524f990d868e4ef6c8fae194468`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 24.8 MB (24750608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d4c3744b9b9428d48825b5d40907bd738a9f30e5032264b201a51cf55221a6`  
		Last Modified: Wed, 15 Apr 2026 21:46:51 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cf195d400ea1b9522336650a09081c2b9bbd58c4567abaf065ae033d6c461831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285201575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e0b5a1092889590aeb2db6c88a896e4c0ec19dea93f92f768959ffdc096016`
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
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005d2616fb0134c4e667bf18779a12515e093b7032480fa955cae8082b1ed00`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 105.6 MB (105606696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c761530a5f45bde84b650345ffc0508fcb42841ff5090e705b63da0fe1389fdc`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 379.8 KB (379849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf27eb0b81b347de06b64c5b5e76195336cec112119695b36d7718b2e4e07b3c`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 2.5 KB (2545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00b01c95a9e75af81929c29b402746eb47e5ae30c7836299919af679dc2fe7`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 27.2 MB (27159941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:a574bc9e18529c423a7eed4fc7c73966ca33d7573d7547e9c5fcd2d59ffdc36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37c1c3d7e653759b7faf430a8ef65f87120f742604c33691af856b141fe6b90`

```dockerfile
```

-	Layers:
	-	`sha256:a70c674dcb660d44b806bb08907a34c2fb46f5a40eab10a7b9b0b205bb907724`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 24.8 MB (24772870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655d938644d51b7909a0fc104ddd54b1fd9b8353f9a4d630fcfb58e3840172eb`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:09fc4eafc58d55baba80fa2179761af87a1a24586c88049e5a2f2a76215b2071
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:711c35fa022e029585c6bd0445cd4e90a64d147945e93f0d17e8658dada9edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296822799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f3e53ea06654ca18393a63c24bf43ef1f2273575e6b31000eac328d06b568`
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
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:56 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b585e3d82ffce0664bce0c8a5cd547fab5ca89e846fcded5bfdea2945c92b0e3`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 110.2 MB (110194522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d9e768ed960260076e36fb5349f0f2bf428da3dd7ca881955f651442db85d`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 379.8 KB (379842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42645bfe1400d71c15649094acea6a941875adfdfbfdcdf5da5a0cf7329e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:52 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740609d32d16cf76c7d87805eff7096e854a1b987b669162d4caf38ef205d04`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 28.1 MB (28074461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d5936346f135b582a261511d5983f9753ba160d0e43bb40ab9f5197266174b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd670b4353b1ad937dc8af910e89de70ce1a49678f9e5b3e4dce0f1951471a64`

```dockerfile
```

-	Layers:
	-	`sha256:420c0d5f20dafba09120bcbd505d4a20dd050524f990d868e4ef6c8fae194468`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 24.8 MB (24750608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d4c3744b9b9428d48825b5d40907bd738a9f30e5032264b201a51cf55221a6`  
		Last Modified: Wed, 15 Apr 2026 21:46:51 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cf195d400ea1b9522336650a09081c2b9bbd58c4567abaf065ae033d6c461831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285201575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e0b5a1092889590aeb2db6c88a896e4c0ec19dea93f92f768959ffdc096016`
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
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005d2616fb0134c4e667bf18779a12515e093b7032480fa955cae8082b1ed00`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 105.6 MB (105606696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c761530a5f45bde84b650345ffc0508fcb42841ff5090e705b63da0fe1389fdc`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 379.8 KB (379849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf27eb0b81b347de06b64c5b5e76195336cec112119695b36d7718b2e4e07b3c`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 2.5 KB (2545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00b01c95a9e75af81929c29b402746eb47e5ae30c7836299919af679dc2fe7`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 27.2 MB (27159941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a574bc9e18529c423a7eed4fc7c73966ca33d7573d7547e9c5fcd2d59ffdc36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37c1c3d7e653759b7faf430a8ef65f87120f742604c33691af856b141fe6b90`

```dockerfile
```

-	Layers:
	-	`sha256:a70c674dcb660d44b806bb08907a34c2fb46f5a40eab10a7b9b0b205bb907724`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 24.8 MB (24772870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655d938644d51b7909a0fc104ddd54b1fd9b8353f9a4d630fcfb58e3840172eb`  
		Last Modified: Wed, 15 Apr 2026 21:59:31 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:e98696af83cfd45f97ba9207bca4c7c126a98214411e7bde6d266bfccdc50f42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:3488a7a80106d067cc6c32ee8d1026c267fcd56fdbf0ab172d80216bb9b5e6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158171462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89b6088cc84722ffea57a901a9ad98f7384133340e7141f0700aed1782af5c6`
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
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f8b2359edb08a063032526bdfe786a4b14885a4736c5947bd785e66d6856a706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea32e6c73c6c625ec0ddf0c75ad0147650b36f36c3ce72f0e78610bdf5229c1`

```dockerfile
```

-	Layers:
	-	`sha256:48ae88e34d7373a715f5f5053b1f4bba51d637a5c47f8625146f6bd6d614fff0`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 18.5 MB (18488549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822a402c9fa80c9122edc35b5db34c5754fe7ae0a2aed1d55f79422af9416da1`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e40ce479b9adc7185209dc8a2420185a27265eca9b4a507d5c657fc7f3c8bb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152052544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e613dfc912c54bd59ee4814483271f481ba23ab404e246f45a16e70fd066c079`
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
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:86e282b8f99fdc46ffbe5f8b6cb5f24b751be8cd5686ee2d5a4e439afafcc13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984ef693910bb0c21a914da8fa91e9808e838876e44fb082c3b7218e3ea6a709`

```dockerfile
```

-	Layers:
	-	`sha256:515c5647c5cc991e648b72b6fefa9f61b11b8df09a72b214b9a664bc3069b568`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 18.5 MB (18462560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f7042ad15560f90c32f39765cec73a3180aa68d8fd559c7b84da22b33cd37c`  
		Last Modified: Wed, 15 Apr 2026 21:03:21 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:e98696af83cfd45f97ba9207bca4c7c126a98214411e7bde6d266bfccdc50f42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:3488a7a80106d067cc6c32ee8d1026c267fcd56fdbf0ab172d80216bb9b5e6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158171462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89b6088cc84722ffea57a901a9ad98f7384133340e7141f0700aed1782af5c6`
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
# Wed, 15 Apr 2026 20:53:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:12 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:54 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 20:54:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b1e8c88b55de7bb95fc86629c092b8ee1185957ce194ca3e8c032521218d23`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe78e730b0bc01704683bee8ea5c7144c34bc29d7f64e8f86e0fd3581c744d`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 6.8 MB (6751659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05bcb8e9e38af2e16e36258cd57336a7d9f443d029737a994e0cbcde39dc7d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 94.1 KB (94108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8e25e7760a7f86e056446fe983fc96739a4cbc9010d4e8c16779f7f1ebb51`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 120.9 MB (120908551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66fff459f77a979cc988155538d6cd842c44afec85e542f5659cee33be6ed7a`  
		Last Modified: Wed, 15 Apr 2026 20:55:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f8b2359edb08a063032526bdfe786a4b14885a4736c5947bd785e66d6856a706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea32e6c73c6c625ec0ddf0c75ad0147650b36f36c3ce72f0e78610bdf5229c1`

```dockerfile
```

-	Layers:
	-	`sha256:48ae88e34d7373a715f5f5053b1f4bba51d637a5c47f8625146f6bd6d614fff0`  
		Last Modified: Wed, 15 Apr 2026 20:55:20 GMT  
		Size: 18.5 MB (18488549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822a402c9fa80c9122edc35b5db34c5754fe7ae0a2aed1d55f79422af9416da1`  
		Last Modified: Wed, 15 Apr 2026 20:55:19 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e40ce479b9adc7185209dc8a2420185a27265eca9b4a507d5c657fc7f3c8bb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152052544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e613dfc912c54bd59ee4814483271f481ba23ab404e246f45a16e70fd066c079`
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
# Wed, 15 Apr 2026 21:01:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:03 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:53 GMT
ENV ROS_DISTRO=kilted
# Wed, 15 Apr 2026 21:02:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f0a2684d9babfb3177690b0c4a2b1ff0db4cf333b9a4f77b7eb9e6f53a0b5b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff337ea7733134af43106880ebb5e900603a2b5e4bd370721d73a7a25a8a3b86`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 6.8 MB (6765008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c6d8e1bd0a4b9a42f8763d22cd8574e5086ed2804ba50f19de93f76d72e0b`  
		Last Modified: Wed, 15 Apr 2026 21:03:22 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca663cb32814a19e937ea07bd86b12869cbb41a47cc848ddf0559c75b785cfa3`  
		Last Modified: Wed, 15 Apr 2026 21:03:25 GMT  
		Size: 115.6 MB (115633032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb611bb0edd49e965a3a9b4f6c4c6dc8471d483595597dd92e232531e2c6d27`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:86e282b8f99fdc46ffbe5f8b6cb5f24b751be8cd5686ee2d5a4e439afafcc13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984ef693910bb0c21a914da8fa91e9808e838876e44fb082c3b7218e3ea6a709`

```dockerfile
```

-	Layers:
	-	`sha256:515c5647c5cc991e648b72b6fefa9f61b11b8df09a72b214b9a664bc3069b568`  
		Last Modified: Wed, 15 Apr 2026 21:03:23 GMT  
		Size: 18.5 MB (18462560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f7042ad15560f90c32f39765cec73a3180aa68d8fd559c7b84da22b33cd37c`  
		Last Modified: Wed, 15 Apr 2026 21:03:21 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:e9b9b98c1a867673789dfa1cb622b780e1ae6e5a0c235b0340d83c2b46f6171c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:d1488d3b99ecd0edaec8349682bc1eadf11bc5b4dc266b3eaaeda8787a724cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296302721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f4249e792af1be98e76d5e3b71faa7086aaeb9f5a90e902c9461a6ac3e673`
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
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb934869c0062075d3924ee67ff17ece2c114ca0ce2144abe6c484a11464706b`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 110.2 MB (110191800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41de78adfb4b31cd70fec97b302a53039d85ae134cb88b28504b1a8f234d3f6a`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 406.0 KB (406035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56562b7711ce2dc52c7a11d2b429e85a9c969d469ef5eaf0530876ced6355d92`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238e0cbb8a4936a6230dd0b4e08a4fb91563787eabed4ed52c321cb254083f5`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 28.3 MB (28253633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:1dccc7efac09ea940614476c7a5b547d0ef600abe39ff4f2836923babfcd25ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24817696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0d92dd7d19f29c32c1ea2755842da2a2ab1183a28da09c0b6be052ca7097b7`

```dockerfile
```

-	Layers:
	-	`sha256:d6e28e9d8dc85665aed292205faba4faf500071be01e8d54146d31de77320601`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 24.8 MB (24801075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161d4f87e7b6311a1d2e9ab5aec66c322fd54084eb76940be809f7203137a561`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:75f904e512850c074a09b2fcad02f42496358ddedb14b0fb2844b2d063b67f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284743559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed588b014ed59b43c6e00b7ee5394c98c3119afdba85eff2e4e21702aa9ba296`
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
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b1652e06603234b577f2609a4675b0d8db5ae2bc8e9a76c212aa8372ec83b`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 105.6 MB (105603863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b1a61548270d1f294994d9d5c6b7ef600aa93cf0406dd697efd56a47fcaeef`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 406.0 KB (406033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab229f387e85cf75d9d2c2b9a816695857692067ddf66c147963519b872f6edd`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9fea2d7bdf03859ee3389c8beb5c8fa13ae0d91f3d7eb8ea185f0dcb5cbda`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 27.3 MB (27343654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:2842848376e0b5ae10b35caa0c4bd0f000c55c92fa8ad83d98caa6e544e4ee02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24840114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bed213097eed21c0c47f4129b1dccd0b3629c656c299a11fbb8324b0ccba2`

```dockerfile
```

-	Layers:
	-	`sha256:27fbf0cacc0c47420fa070f1a46d1c49be69a3b5d6cbba50e355ee22c06e4031`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 24.8 MB (24823344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7348e7326134d81c2a173b26a0de6babefbb17960b8fedb1bf5b857964d25364`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:lyrical`

**does not exist** (yet?)

## `ros:lyrical-perception`

**does not exist** (yet?)

## `ros:lyrical-perception-resolute`

**does not exist** (yet?)

## `ros:lyrical-ros-base`

**does not exist** (yet?)

## `ros:lyrical-ros-base-resolute`

**does not exist** (yet?)

## `ros:lyrical-ros-core`

**does not exist** (yet?)

## `ros:lyrical-ros-core-resolute`

**does not exist** (yet?)

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
