## `ros:kilted-perception`

```console
$ docker pull ros@sha256:9ecd5ea1dd0e9429d13f794c016bcffb0e92c4ce7127807df5b2451c925ca9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:ff71f2194c043f247fad9ab7ff360caa47e1f0f80d21a83908dd1c640859659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1095789877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7882bd433024cf1971d7b0b580111ebb50683d8599ddbdf8a487b1aefdcabe`
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
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df8e2597bb5081a304f28b13049febe272f2c6d03097adb5bf569346c6a5f5`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 683.9 KB (683859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1827b068556f57886cad395350cded398b71c780dad810d9cb5f48aeb1bd5`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 6.7 MB (6746894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ab4ea82f37711412e2ce34dff17f73d11caef6a5cb3c8f4a23bb24242ff66`  
		Last Modified: Mon, 15 Sep 2025 22:26:52 GMT  
		Size: 94.1 KB (94080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c92407c0c99f8ce4496a5f8ab4a6883930dd204426676dc03f36394b96ef20c`  
		Last Modified: Mon, 15 Sep 2025 23:19:20 GMT  
		Size: 135.0 MB (134968079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb84c0ca29118539fdb1987693ba26bbb7fef03bad6c1349885f8189f99491`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ad4e0967c4f2fc54b1fc8c9371361914af0419279ef3a09f8f9ecbc3e17f3f`  
		Last Modified: Mon, 15 Sep 2025 23:21:05 GMT  
		Size: 110.2 MB (110185503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c3dabe47646cba938ba7076a97e47b843b10a81d035548e0c5ae09767aa456`  
		Last Modified: Mon, 15 Sep 2025 23:21:00 GMT  
		Size: 362.0 KB (361999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f256a20a09d470c8e0eb81166c3ecc100e308702d21403458d3e9acb78178d`  
		Last Modified: Mon, 15 Sep 2025 23:21:00 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428752ea94da6d6c5f53cfad376970875b81973b8f3c9bc747f9a9e63e679329`  
		Last Modified: Mon, 15 Sep 2025 23:21:05 GMT  
		Size: 28.1 MB (28050584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75dac3dfc4bfcbc5878189378dacb7de7b810e63674511c1f112016a35af24c`  
		Last Modified: Tue, 16 Sep 2025 05:41:59 GMT  
		Size: 785.0 MB (784972764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:4b915a495a15cc28f3e5731900bc645a2a9b05295f324413366c2bafe3925a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fb9e4489bad5a3dc9902d83ae8f02d197dffbb0b36a85bf2442f1536e4f63d`

```dockerfile
```

-	Layers:
	-	`sha256:d6c5a5ec63104f75c3c1cb9b79c5ee1f05b9bc7071f47ed4550ac5b7c1b5cea3`  
		Last Modified: Tue, 16 Sep 2025 01:18:09 GMT  
		Size: 60.8 MB (60822353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d034e593f848a66c145deb5c0acf1b08a6dfb279d7f20d20727a457c10129b4a`  
		Last Modified: Tue, 16 Sep 2025 01:18:11 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

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
		Last Modified: Thu, 02 Oct 2025 03:19:41 GMT  
		Size: 695.0 MB (694963382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

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
