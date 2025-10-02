## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:af26f0522e84b768763f0ceb2fc1551048292b9123a84b9f73f062f60e17451b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:88b4952a8c335d73d9486aca7673052c078d6f7a8378c342d8fc8c6489313be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324544890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84b090aee5625b8e198bf1a3d8f78bd776a0daac2129724b12b0a1ee21c1f39`
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

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ec504128040f18c6460baeef7b367cdfcfef7023bd8b2a14ebc3cf4d5a67d7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25597442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad1646624c232662ed53f73233151cb3b0539ac9eb5cb6874b1efea2490d915`

```dockerfile
```

-	Layers:
	-	`sha256:2af551f8c4f80f1aeb7348543c27a96ab622e4d9830ad070318fb9180f55bd67`  
		Last Modified: Tue, 16 Sep 2025 01:18:36 GMT  
		Size: 25.6 MB (25581035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c607989f19b796a86c906a8a8b6047f788a0a4f465d325c581e8c585571890e1`  
		Last Modified: Tue, 16 Sep 2025 01:18:38 GMT  
		Size: 16.4 KB (16407 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bf8df8af2693c9524125412c0513ca2f2aa7a3e8669f1f02ed9cd90cbbd0978e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314832345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2361206f4eb90de5ec0d3b984ec5ad5e7dc452683be75b3482b40cc1878089a`
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

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9134bb428ed8a7b2074c9f77a0ce409207d8b50a9ca7a3ffe0f5d65741eec4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25622047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07770cac81e9cd393b90faff9c8b722e0f4252f55ef6d58b4ec9c4c4ee639fa6`

```dockerfile
```

-	Layers:
	-	`sha256:f0c5ee712074116e305cd84771afb611bab3a06b89250697a16b5e70aabc0316`  
		Last Modified: Thu, 02 Oct 2025 04:19:04 GMT  
		Size: 25.6 MB (25605502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58639b7ff5de7f8336e25023e740ccecc53d3843a6521d65388a2052ac9c28d`  
		Last Modified: Thu, 02 Oct 2025 04:19:05 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json
