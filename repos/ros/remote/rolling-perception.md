## `ros:rolling-perception`

```console
$ docker pull ros@sha256:6b25e0d5bab4ee8f5b06298d85174847c6fc138173e53807a4f4298c76500081
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:336028e965cc5cffc49fcb29935bf7214d24bea6dc6af7a58a5a7269a9072b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1109584877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f388206aa11918dbcf5e96e766253e477d73da5198a2e09662b638734d2829a`
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
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1090f035fbb3dc8bff3a56b524d81b9bff6d998a0a78d6e678503894be117f`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 683.8 KB (683822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb53581a15804c55072740da9f13b016d0777a3634e94bab7a8a4df208f2b99`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 6.7 MB (6746858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e479f0117c61cf443355a1be70fb06e043d70a323af3a3542f6940e3ac348b`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 94.1 KB (94065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee7384dbecd35a0eab61a37ccb1544fe43b6e12df8bb82664f36d7f3c8f17c8`  
		Last Modified: Tue, 16 Sep 2025 01:47:21 GMT  
		Size: 148.7 MB (148690069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e689d29ebbdfe99b51ce27372da98ec09baee25a0bf94f58e7d77b7bb8dda948`  
		Last Modified: Mon, 15 Sep 2025 22:27:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f8275dc3e79a5471bc6930acf91b55bf641c31f510e3e4111799e1528e93f0`  
		Last Modified: Mon, 15 Sep 2025 23:21:52 GMT  
		Size: 110.2 MB (110186282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba1f9e46ab66e2fe3834378d7d0631f4f5daf2532cf4a35550a7a75a0791a55`  
		Last Modified: Mon, 15 Sep 2025 23:21:41 GMT  
		Size: 354.3 KB (354333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09202b43a35018fd231e82741e9e253dd231b83e4aaf92f347c41d7cfc993fc6`  
		Last Modified: Mon, 15 Sep 2025 23:21:41 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7959145ae6737a50e62cb4b31a80f50e846de3e313d52b5579f70aefce64d3`  
		Last Modified: Mon, 15 Sep 2025 23:21:44 GMT  
		Size: 28.1 MB (28063365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4856980e5850baaeba536be8edc4cb48a57df294c05eb292cde29f46615e0a92`  
		Last Modified: Tue, 16 Sep 2025 06:38:17 GMT  
		Size: 785.0 MB (785039987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e0657732086d89a175949ee9383ad949efda269eaedbce613c95a9a92eb675d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61763018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5026f8731e26c7552522d50a2e46b850fe3b09aff6b3220b3c98fe19e20800`

```dockerfile
```

-	Layers:
	-	`sha256:719171c2da1f4c5829446008ca84915c858ffd036e630d960f18a48981f7461b`  
		Last Modified: Tue, 16 Sep 2025 01:18:44 GMT  
		Size: 61.8 MB (61753614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf381cc393391db3032555d09cfb9d5ea9e5f14003163080e49b5ac7b82e9484`  
		Last Modified: Tue, 16 Sep 2025 01:18:46 GMT  
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
