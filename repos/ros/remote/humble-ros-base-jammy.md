## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:45dfc0b15c8315c2b808cfd3d9ccf3132e828f5eac2fa68f4aea50b1cb2fea7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:457f6c18a248fced2fa60b54d6968f7ab6c52e741893be40bc5cf81647f17bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263076409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a44deed6887ad48cd9f17f692849d415c5b8b4d3ef016e57de53ad3a3c9b58`
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

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:895e9cf92a296b37d4f291797b91e084f174229ede4477d78066e92d1afbcf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23682729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f7489f33f0374bf53a0ceadc25a82e7a641b85ca59a3ceffbaaceccd756ca7`

```dockerfile
```

-	Layers:
	-	`sha256:8947fcd2746eb939bcfefec3fb96296b2d716b163a2b50b55764a661f486f8fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:22 GMT  
		Size: 23.7 MB (23666338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4c0ad1e9703a56e766f57176823fc8ef6e327c1a3922af8e751c40fdaa6394`  
		Last Modified: Tue, 12 Aug 2025 19:17:23 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c011023f390a2e945608d095f2c9fa072fbe63fc8fbe166ac44d2d3cd35eb805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255484248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c78efb495871f50b26ca150b9ea28211418ffb348fc3cb4b7cfc7570d3c47a`
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

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:bfff264262e9001c84e057f2387cbfc98954eb32374ac154fae0c53e5cff4959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23695883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a64af86435ea59747cdff8481a9c6d0584083ee3dedd1e5a7d4db1ea4e4632`

```dockerfile
```

-	Layers:
	-	`sha256:49dc6c5233f2af2b3e54d53f15807b2952d689f8028c276e51d9707b22c4ff48`  
		Last Modified: Wed, 13 Aug 2025 01:17:40 GMT  
		Size: 23.7 MB (23679355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba10c372abf61dbec82e33e0e7ceb3a51525fc9ac8d199ea29c587976c97d852`  
		Last Modified: Wed, 13 Aug 2025 01:17:41 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json
