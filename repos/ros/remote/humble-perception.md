## `ros:humble-perception`

```console
$ docker pull ros@sha256:5c409a9653bd8c21deeb348c078ece929ca4a15853eaf1501b58dfd8d714bbfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:c75bfbe908127a1381094caa671ee565dba6aa73c0a0fcaccd7a098cac26de6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.1 MB (955136015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2693a138e81af6fc56d06abbe0dea32832ef50a9c03c59567dcf886c1d7ad75`
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
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b660084749371d069f921040a4fd644dd612af0b6c49a62da486ab5570ab3`  
		Last Modified: Tue, 12 Aug 2025 17:56:33 GMT  
		Size: 1.2 MB (1214020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146caa6e438614ec1a4691e35f239ffdf79e5484472d13d5371f8435eb40c00`  
		Last Modified: Tue, 12 Aug 2025 17:56:31 GMT  
		Size: 6.0 MB (5995314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f16346373fec485486a8a417c01db653ab08c41a8a584599a1dee0a7e97f3c`  
		Last Modified: Tue, 12 Aug 2025 17:56:31 GMT  
		Size: 97.1 KB (97149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ca3259567d61027fb2a9a419ca64c71255a0ae49f3dc2fdd46d1b387ed7950`  
		Last Modified: Tue, 12 Aug 2025 17:56:44 GMT  
		Size: 104.6 MB (104581293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff17287297b63ed8841e34c2306fc84dd688a1f6e692bd2bb16c052e30c24ab1`  
		Last Modified: Tue, 12 Aug 2025 17:56:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c400a0b3bc0026beaf12a2b8d0e1d99e6a942ac84652eeb32e2ca74fc210c485`  
		Last Modified: Tue, 12 Aug 2025 17:58:49 GMT  
		Size: 98.0 MB (97962839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1e8d0461b937fa2d7389357b77b36161c10f39d0840829ad0158e26c469ff8`  
		Last Modified: Tue, 12 Aug 2025 17:58:41 GMT  
		Size: 371.3 KB (371347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4866170ebdac2669aaa72728f70829004897726b562502b81cbdea1eae1b5df9`  
		Last Modified: Tue, 12 Aug 2025 17:58:40 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7600c7d62fade9c3aae1e5c633b9c75a24d0899364d1c727c6549653aa435135`  
		Last Modified: Tue, 12 Aug 2025 17:58:42 GMT  
		Size: 23.3 MB (23314796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14011341c8814f87ff63ab3ff784e46940140935ed3429028a495d6206368a3`  
		Last Modified: Tue, 12 Aug 2025 19:43:31 GMT  
		Size: 692.1 MB (692059606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:941d1cb3cd82ae91a93f3e17fd21c4c11a02d8961c65a97ef4c6596c9e9bc202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58767241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4c9012409f9ae677c5e9c58d929bca08cd8c63fc0d6eac43dbb3c35f65bf27`

```dockerfile
```

-	Layers:
	-	`sha256:86cd68029468d65b2bfcf9e74035589e1a47e7e1d9679af036ef3b214ef30b87`  
		Last Modified: Tue, 12 Aug 2025 19:17:28 GMT  
		Size: 58.8 MB (58757846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4fc8dbd27e53359de2c46ea4853cce27cf3d891c1c72f292390bab7a4539d99`  
		Last Modified: Tue, 12 Aug 2025 19:17:30 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5f0c6f72b615c656ad908d84339ca67252ec07ed4456b5ac9bb0c4df7c6c8106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.5 MB (915455742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dc9e67acb9605c21fa8dd623b86f0fcb15e98233ad700dc6d8e17050053c15`
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
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3413538d349f34643db7890061af65431ab5eed6cefd879692cd3c858f9ca2`  
		Last Modified: Tue, 12 Aug 2025 21:04:44 GMT  
		Size: 1.2 MB (1214253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d2273514f7012f909f7c1472d8f5340ed9119a3f46752cad7705f39ca84e31`  
		Last Modified: Tue, 12 Aug 2025 21:04:44 GMT  
		Size: 5.9 MB (5939779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bbe0bfd7eadceb47a12ac0d96fa7b9e08244b0375ff7dba570c85625a176f5`  
		Last Modified: Tue, 12 Aug 2025 21:04:43 GMT  
		Size: 97.3 KB (97300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de148676c2b7a41926a9dd1197c85f396169405dacf02baa600ce8a4ad4a87c3`  
		Last Modified: Tue, 12 Aug 2025 21:04:54 GMT  
		Size: 102.3 MB (102283556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bc3d3b69ae746ff83fe854c8253b45aa7248f9ee7cf73ee8fcd57fe9868871`  
		Last Modified: Tue, 12 Aug 2025 21:04:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729e29f63aebc5c34da996f392c69cb6cdc511d6208213920557deb9dc36798a`  
		Last Modified: Wed, 13 Aug 2025 00:09:03 GMT  
		Size: 95.5 MB (95513202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118e719215c9fdaeb84c18034f93724715e8f901d8ae9401ca92fe08cfa5388`  
		Last Modified: Wed, 13 Aug 2025 00:08:53 GMT  
		Size: 371.3 KB (371345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452885f0d0914a003157299a7d137eed5cfe7fb035eea968f21553812d1d2e7`  
		Last Modified: Wed, 13 Aug 2025 00:08:54 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bba396e51e1a07ba0cd679fe9a65f85ecc3290d3ca38b8fe50b0e06a703de1`  
		Last Modified: Wed, 13 Aug 2025 00:08:57 GMT  
		Size: 22.7 MB (22702878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66d6df2d8c8470b7993b067d0f09c3dac20b0fe882f2db70ce742428f8d364c`  
		Last Modified: Wed, 13 Aug 2025 13:07:16 GMT  
		Size: 660.0 MB (659971494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:23098c714f143545e2c69762d088888ba61764da80c674667b3bfc6045aefd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58751642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef5e49cd102f754e2270b559aa4defcf3e07b24e094ca78b58ed8cc2c9f7302`

```dockerfile
```

-	Layers:
	-	`sha256:1ce9ebeb07c94d5352819019609df914e8295c47e07701f42877c41da2e7d91d`  
		Last Modified: Wed, 13 Aug 2025 13:18:59 GMT  
		Size: 58.7 MB (58742167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8094b1710f430f031fecf31240d31bc5e60fa06af61862a1404a90e6adb10236`  
		Last Modified: Wed, 13 Aug 2025 13:19:01 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
