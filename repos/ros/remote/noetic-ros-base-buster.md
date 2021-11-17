## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:bf10472962fc48f37970677f551a97902b4bec515b3d5ff0fb308ff451b8b737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:530299c145dfcbdcd00313984b1012be0f853042a76ac4764491a7d7cc2d7eab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463281671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b203009a4dab52db70f4b3c1a23b49128db68c46b988529e375f69ae2173b8a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:51 GMT
ADD file:cb5ed7070880d4c0177fbe6dd278adb7926e38cd73e6abd582fd8d67e4bbf06c in / 
# Wed, 17 Nov 2021 02:20:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 22:36:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:36:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 17 Nov 2021 22:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 17 Nov 2021 22:36:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 22:36:28 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Nov 2021 22:36:29 GMT
ENV ROS_DISTRO=noetic
# Wed, 17 Nov 2021 22:37:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:37:37 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 17 Nov 2021 22:37:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Nov 2021 22:37:37 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 22:38:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:38:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Nov 2021 22:38:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1230f17f526cb07307d41462355b10488b994e8bdafe0d8f275a405fa3b33831`  
		Last Modified: Wed, 17 Nov 2021 02:26:06 GMT  
		Size: 50.4 MB (50437098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f64a2cee9a8973db7ffaff43c62f68f0db43144b718c8339856ff2d039b430`  
		Last Modified: Wed, 17 Nov 2021 22:43:20 GMT  
		Size: 10.9 MB (10891910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d367fa9b39ce393432a2a974cff50cc6c0a295b0c00a6a71152b947621dfd2`  
		Last Modified: Wed, 17 Nov 2021 22:43:18 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54972089aecf2d558033d5c01eb20f1a2fc64c872aca23ad9ab78f45f335f6e4`  
		Last Modified: Wed, 17 Nov 2021 22:43:18 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d68c1a3d9a31ff02e5ed0caf544e9e047643eeaa48073c11c2aff158e93739`  
		Last Modified: Wed, 17 Nov 2021 22:43:56 GMT  
		Size: 239.1 MB (239087074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb488c1f6198579f8b779a8d04bba2ad192ec739f12e0996b08295f67e238be`  
		Last Modified: Wed, 17 Nov 2021 22:43:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95ec5664844d6b0b37d4f1fb00c8c3471f9ed1c9279b982e28e0bc5187c5d32`  
		Last Modified: Wed, 17 Nov 2021 22:44:18 GMT  
		Size: 86.6 MB (86566518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f591fef24508ee575fa1a04719eedace93ecc69747c634ee129ab56e7afaf`  
		Last Modified: Wed, 17 Nov 2021 22:44:04 GMT  
		Size: 319.7 KB (319667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bfb467cccf362fae16d482dedbaa84f68b710a3551e876a27d306cf8487b62`  
		Last Modified: Wed, 17 Nov 2021 22:44:16 GMT  
		Size: 76.0 MB (75976988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2ead67f2f4e708b83ba09ee7e4b274882ddd397f9574aaa8f26af03199977b28
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402750993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dde0ba9a1344c26edaeacb4e64fe2315ac51bb119bbc9b9fbfcfee9a5464e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:55:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 17 Nov 2021 09:55:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 17 Nov 2021 09:55:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:55:40 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Nov 2021 09:55:41 GMT
ENV ROS_DISTRO=noetic
# Wed, 17 Nov 2021 09:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:57:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 17 Nov 2021 09:57:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Nov 2021 09:57:09 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:57:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:57:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Nov 2021 09:58:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e1e6c972c4d10ef0b28be7441b9faba756aef9d8502c13834239097e49`  
		Last Modified: Wed, 17 Nov 2021 10:05:24 GMT  
		Size: 10.7 MB (10688089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1a10d650dd3ccec5c33cb88fd591b4d3377d74b6bc192bfc5703c3377d2490`  
		Last Modified: Wed, 17 Nov 2021 10:05:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5555e0dff8030a1664f72dbd55c2ccb0f9643856a0543a792754ce07a9a295`  
		Last Modified: Wed, 17 Nov 2021 10:05:22 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aba732adf84216832ef6ac06de2d7a0f183d75a35f86164d76ad6c20b84e81d`  
		Last Modified: Wed, 17 Nov 2021 10:05:54 GMT  
		Size: 184.3 MB (184302665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77ffa64df86146e7a47c4de87957d94a0df3a134a9c3b631ac299b4ac79f716`  
		Last Modified: Wed, 17 Nov 2021 10:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8cbbefff3909b904d5a6b9278f2706cb037366625e701143f47f2d9171ac36`  
		Last Modified: Wed, 17 Nov 2021 10:06:13 GMT  
		Size: 84.4 MB (84350861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8330a922777eecbb2b62936269690eff07ec9f74763739d6c64c216921bcb1`  
		Last Modified: Wed, 17 Nov 2021 10:06:02 GMT  
		Size: 319.6 KB (319619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a208bf616b1d8d934b041d89a2c229baac87ab27ba204fa7abc72d8d152427f`  
		Last Modified: Wed, 17 Nov 2021 10:06:12 GMT  
		Size: 73.9 MB (73864399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
