## `ros:rolling-perception`

```console
$ docker pull ros@sha256:e9939de0fd4fb6065494f12830a1fa1d030ec6fabf398b8fb87331e980e759b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:cf3e74c985260a0fcf4a1f5f0e121c74d0248a05217992f3e005b355542b0361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1111936049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8881edbed91c5eed923c596356ec3b576ec21f4e736f5063c71b19ec293afc8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b61cd581a56f484742941f9fecb044c9b59058d2fa4beedf24f7e7885f01d23`  
		Last Modified: Thu, 02 Oct 2025 06:28:54 GMT  
		Size: 683.9 KB (683878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171251c304424eb6f36b5385f9d7d05b22608afe36a4d7218e9d8cb3ca31479`  
		Last Modified: Thu, 02 Oct 2025 07:40:58 GMT  
		Size: 9.1 MB (9147633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067ffa5de5de694e11dd8fab9a66b88aee908fd14c9f86af59376c5b570314a9`  
		Last Modified: Thu, 02 Oct 2025 06:29:01 GMT  
		Size: 94.2 KB (94202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2155f8d6d58365d02cbb1abdf9be88b90b2885ab7b839682ddf8c5af3e0c9fc2`  
		Last Modified: Thu, 02 Oct 2025 07:41:07 GMT  
		Size: 148.8 MB (148816264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce003c37d3b958571a9c710e8a9dc81cf1125c8483b6386a97293006bd747b`  
		Last Modified: Thu, 02 Oct 2025 06:29:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3311874e56d0a6824364bbac059cc43e6badf6eea3008cbee875737dcb636cb`  
		Last Modified: Thu, 02 Oct 2025 08:47:14 GMT  
		Size: 110.2 MB (110186692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2031436755676a305b3188c60bfddba85f5867de88dd480160afdd2928efb9a6`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 355.7 KB (355733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78d23d85055afcc3c0e9479a1518fbca2c51ce686a5df837f9157160634b088`  
		Last Modified: Thu, 02 Oct 2025 08:47:09 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200b3bdbe806fe52a8d0b156e38d69f34e2f262e9b309eb651e23165677498e`  
		Last Modified: Thu, 02 Oct 2025 08:47:11 GMT  
		Size: 28.0 MB (28041672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd1961ff94a232dfb0517663c2b3dcc652a33abf5d877df9ef159927270cbd2`  
		Last Modified: Thu, 02 Oct 2025 13:20:56 GMT  
		Size: 784.9 MB (784884306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:0fbef80c39af9322714f74e36ae0b54f8f917a7f4db57c2b90fb45286bd306b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61765051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601af995edf12475577c2ab453eb06cf1155dd7e5648025a811d2d057b51b516`

```dockerfile
```

-	Layers:
	-	`sha256:9ca78e5544cdce49384bef0c4a4378f313044c7bd53f660def4677fabfcb2149`  
		Last Modified: Thu, 02 Oct 2025 13:18:16 GMT  
		Size: 61.8 MB (61755647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de263ef8dab896ad23482dc683da862b7ca4e2c3d8d3466008188a67d21a4d6d`  
		Last Modified: Thu, 02 Oct 2025 13:18:17 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5d2f4d14a46ae5c7f5285d3b6dbdc70f9177b985dd6559f9da694fdaea229faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1009713604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be8d477d600961ba7b8225e29aecc15f0ab4f43b32b09815d25faa25aa87d90`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405d746b2e8e7ce7738b1e9aed7c013430edd37997e3df63cc1fcd07921b25d`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 684.0 KB (683980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da54c7c4310afa97400aea2c20195b24269208ada7d53fe377f2ae01f75d193`  
		Last Modified: Thu, 02 Oct 2025 01:33:59 GMT  
		Size: 9.0 MB (8973936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675b7f405bed0152d1b27d7c72a2312d179c5ea0e0a8f0868682929ad1b0e1cd`  
		Last Modified: Thu, 02 Oct 2025 01:33:58 GMT  
		Size: 94.3 KB (94286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9267757f1f7c27d4e5765e789787f1c7ada31d6efab6d32714301347766dd9e`  
		Last Modified: Thu, 02 Oct 2025 02:27:18 GMT  
		Size: 143.1 MB (143142374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327223fa4a35fd1f26458825de95cb7d529d4954db71112bfb124d0d7dcf04ae`  
		Last Modified: Thu, 02 Oct 2025 01:33:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4867bbf27802ebcec126da4f4f575520a706c2de1b5cab1b07f4d8c8ce60ae4`  
		Last Modified: Thu, 02 Oct 2025 02:29:11 GMT  
		Size: 105.6 MB (105594631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad6a6d41bbeb02aaf40e3187214c2c70bea0c74ed6f768294ae35e88c75ba48`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 355.7 KB (355734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebae24cd02da0cf854a5ee1e08308bf6d2b3ad5b2375052e084657c981d1aa7`  
		Last Modified: Thu, 02 Oct 2025 02:29:03 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829949e7504fb2923c21b6dba15e172d82d6a35d1f358470c866a163ff2b91a`  
		Last Modified: Thu, 02 Oct 2025 02:29:06 GMT  
		Size: 27.1 MB (27123180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d527e4874e96a4508731ef6d33d6fafffdc92793ff47bdd173a276e7d4f968`  
		Last Modified: Thu, 02 Oct 2025 03:20:16 GMT  
		Size: 694.9 MB (694881259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:0f760fdfcf698bc756fd491e90702d8e2c3570b37539de6ab2d0c480a6c1cae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61695853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666953a248101e452327a88733d4ed470158fcf8cbb113a80758faf807ecebdc`

```dockerfile
```

-	Layers:
	-	`sha256:af33cad7aac03a4d98b941153dd8842bf065c713d192ab9eff4ee87989a1dd8a`  
		Last Modified: Thu, 02 Oct 2025 04:20:38 GMT  
		Size: 61.7 MB (61686369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2aa219138327d20373bf98932a1cf501f8a72a44ea1de84f77b5dd81dbf670`  
		Last Modified: Thu, 02 Oct 2025 04:20:39 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json
