## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:f338af006d456dd4b9919504252eefb8ca4f1eff57b5ed5cbdbc47e177bf3463
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:53d3ccddb6e2b31d36bc45df90af638212f621afa1fb24acbb99406c95582122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1098205741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ace56c9751862d4973a146424025f4039ad7c8676e156feee8346da6b2634e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb11ad22aa215c08ab1ddd8afcf87b3fa553117dd34ee4667c1b976a3cba5c61`  
		Last Modified: Thu, 02 Oct 2025 06:28:42 GMT  
		Size: 683.9 KB (683888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e123d6ddecce0d115e4e5410f78a0f72324f8a035468137b9ee1364c334df2`  
		Last Modified: Thu, 02 Oct 2025 07:41:05 GMT  
		Size: 9.1 MB (9147619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5567e6c6a0bca7204e8091a90278f279084d427cf99bcacb4c36bb80b4860ba9`  
		Last Modified: Thu, 02 Oct 2025 07:02:32 GMT  
		Size: 94.2 KB (94205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf308a9b4ee769ffe671af02237428bbea707579aa9053eec48de01d5691165`  
		Last Modified: Thu, 02 Oct 2025 08:40:38 GMT  
		Size: 135.0 MB (134982262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f34280af7632305bf440a28b5c441aa18ec0b5b665cb07eb7c5650b7e2267`  
		Last Modified: Thu, 02 Oct 2025 06:30:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66d21c8232d8783a7e2705dcddc210613500a4b975935094f13e8082d289c9a`  
		Last Modified: Thu, 02 Oct 2025 08:43:14 GMT  
		Size: 110.2 MB (110185711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e760c71521ea26184b0599cdcba9130630299976a0ed74d9afcf9d6a379736d2`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 362.5 KB (362511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5588a5d3ef0a80619aef78ff285dde481841fa73fafc364a7128c81f2ef933a`  
		Last Modified: Thu, 02 Oct 2025 08:43:03 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffb14e2f9ab03b3ce4945152457991029f211759a81f65e4a067268860e47c1`  
		Last Modified: Thu, 02 Oct 2025 08:43:06 GMT  
		Size: 28.1 MB (28051331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c3127fbcff76719a7f13056727bbb20c5828a27e14688ff7ec623538200256`  
		Last Modified: Thu, 02 Oct 2025 12:10:35 GMT  
		Size: 785.0 MB (784972547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:33af5c77568c8981fe0a074c3dfd26cc9a8ff16a901c3ffe4e562992d3e2fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf8173db8583e3d6dae29d67deb6982b1edda12448ec94acae74083288f4915`

```dockerfile
```

-	Layers:
	-	`sha256:168067b7930ec0bffd26d93e056c06a7b840f6524b192dc866d126776c60bf21`  
		Last Modified: Thu, 02 Oct 2025 13:18:06 GMT  
		Size: 60.8 MB (60822377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6db91243f3a26f5304aea14b6fcd8d4cc510ac5606b84c294bd942ad8217355a`  
		Last Modified: Thu, 02 Oct 2025 13:18:09 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b299f5123149caf8c27b4738218ddfad816b06629f06f8b23981b0f702127dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.4 MB (996376178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899ac3d335fcfb30f59981d69869304c7dcf53f08053d27dd420aa699f6dae9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86736f5c635c3f5b8beef3efae36f38495b548069192ed89cac1cf4d6f934d`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 684.0 KB (683979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfbb087113ae53a3e90cb85b5963ad48e6ec8532d44321eefe684834cfc497a`  
		Last Modified: Thu, 02 Oct 2025 01:33:57 GMT  
		Size: 9.0 MB (8973926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd17857154a30cddea03ad031105494a674f1db252bb895b5c4a81ca05fb03`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 94.3 KB (94284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968f8f03edaf427d0a41dcda7f3a9a8b145be55f1ea067ed842bf92d5e2744a`  
		Last Modified: Thu, 02 Oct 2025 02:27:13 GMT  
		Size: 129.7 MB (129702693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5dc83680276732c62d2982905f12cebedd44317e978e6d78085b929089fdf0`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 105.6 MB (105593985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70058fa606338201849e6038a5e65ed4a30257067d38892931c54bcc0f06761`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 362.5 KB (362513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029c1a9952b890d778e8ebee58be510e51bbbe5a70553e39094c3566884feaa0`  
		Last Modified: Thu, 02 Oct 2025 02:28:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac005d2fde08e254e758d6d7e2564b3a75cf637e9d90df6894fef093d88310f`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27137188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e10717649fb04c0c45c9989ca7cbb84576448290e0f3d1a703166ec01d39ce`  
		Last Modified: Thu, 02 Oct 2025 06:35:22 GMT  
		Size: 695.0 MB (694963382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:3cb719f408a19b8961f7a8a5329e20d4e07c0db664928ae14b9ccb01a88385fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4f626ac4227909bc7adfff7d3e289c9b2ebcfdfa5425cdf374c694be2f8dd6`

```dockerfile
```

-	Layers:
	-	`sha256:d312e4430c740b516eec05d3643f0b9f1e58bad9e0bb37af1c9a7798ac98e519`  
		Last Modified: Thu, 02 Oct 2025 04:20:45 GMT  
		Size: 60.8 MB (60752902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a181c206ec07fdd0171e29a034af3ebf0d0614262b6562e8f08edeac22dea00`  
		Last Modified: Thu, 02 Oct 2025 04:20:46 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
