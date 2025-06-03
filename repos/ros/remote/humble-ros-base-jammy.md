## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:d66b8a36f8c6cad03526188c8dcd2cb17096aff73a1af628990ab118794479ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:6ae2d4d3bf17eb8b13eff00824be6abf90f337eba12ebbe319f984c1d9f26792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262981180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168e1f658ab579833f7ff97e00c52f1637240d742daae16ce3246bf6dfd2f209`
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
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b611258b9e589c289c2fb50570b97c455ad6e5e6e9de251b753fab9c5618c`  
		Last Modified: Tue, 03 Jun 2025 17:07:39 GMT  
		Size: 1.2 MB (1214039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf6d82836139f37c4872db40ac59c01b82bfce2b74e5ba795b14ee21f7bc4e`  
		Last Modified: Tue, 03 Jun 2025 17:07:38 GMT  
		Size: 6.0 MB (5991843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ee3eb0604e23957531406bba2fdaa67f77da515ebbafa7e8f318d462c40be`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 97.2 KB (97179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67910d3d301a88382773a066be8c81a350d18c243ade54d61ec50923c5e7583`  
		Last Modified: Tue, 03 Jun 2025 17:07:47 GMT  
		Size: 104.5 MB (104532630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1c867fd17fe66471be29077931fd8ec1699a13818eb93034e99868ecd7bd3`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c35195e7507c24005520a8c45874a499a1bf080555373c57a5d59b1a2df30b6`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 98.0 MB (97954050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c64fea9ecf8685a15c2e72575fde6075df9337d0daff01a2707185e92209ef`  
		Last Modified: Tue, 03 Jun 2025 17:09:31 GMT  
		Size: 362.1 KB (362150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba527436b8c305a48ac0cc16f3a7e43f9ea5f827c368c8b90c0fffeed8273e03`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5237a367af95b4bc5cef912321b337fe2e5d66f06a23ad973680596da45b35`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 23.3 MB (23293629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:3f9a1f71a07eeee1d89c2ad93a5a3d2ac24ae2e416db0045d901b25dc26b98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23029026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bcd344793f2c51eb8da1c190bf0ed7340dd88a97cf388d91a9ab5cfb3641ed`

```dockerfile
```

-	Layers:
	-	`sha256:dec6754de12c5c273127119636a801198a3de05c2e6aa7911fda9b935583a54b`  
		Last Modified: Tue, 03 Jun 2025 19:17:27 GMT  
		Size: 23.0 MB (23012635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51171abc4c4a0cde6313f059dc67861e4ac2e78c764b0af0a0857e4d5b1bd3fc`  
		Last Modified: Tue, 03 Jun 2025 19:17:28 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:19292be2584cd845db9b5542b76546a7e5da661bcac15f1804d2c1cbb68467d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255409086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6a8d0d8d582d4cfdd0c7b9e2b03f3befcc80db56d8e63074ecb9105ec73b8a`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371b330eabe98b4c2f7a23612c6b1e42a4956672754821ddf5872050a558eb4`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 95.5 MB (95506704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaf8eb4130d56998aaeb0e2ba32f8c3a358eae317fcc40d60886b6021008de`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 362.2 KB (362154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014dcb0d353b6d71d8ee54ea5ea2da373e2d203f95d5aa144a904474030c8f6e`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa21615c56eef2e3c96f602ed9e098526eebb513ac0e2d5ba41b462cea49278`  
		Last Modified: Tue, 03 Jun 2025 17:09:41 GMT  
		Size: 22.7 MB (22681600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:ec37020439d18152fd259a5d6f242dc62d3856e1ccecc11f77aabd1ff5c5c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23042179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f0cd94ca0f26a5bd27e47c2292056ae159e15f778b2d7e6ecb6d7ec7ca8414`

```dockerfile
```

-	Layers:
	-	`sha256:3fd7739ab610e44cd8a172462b5d39eb9be018c2619daa3c23e80de27f82e039`  
		Last Modified: Tue, 03 Jun 2025 19:17:45 GMT  
		Size: 23.0 MB (23025651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6aff5c76f0803b84b6c1353d30ff26b3426ace202704137c99555c427643e9e`  
		Last Modified: Tue, 03 Jun 2025 19:17:46 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json
