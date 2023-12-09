## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:b7312519d1f0ca9e486a6f6f876a9de30c017b0f21d52811142e0ab1c33cba5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:6f2ac2bf4d1ff188f41d6b90db0c8a0b5b3b6b893dedfd2eb559b03ee5ae6e06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144510480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a83b300640653c29ba26e95f49868f32e1e07e062a45be0a49726eb42250797`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 02:08:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:04:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:55:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 04:01:42 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 04:01:42 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 04:01:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 04:01:42 GMT
ENV ROS_DISTRO=galactic
# Sat, 09 Dec 2023 04:02:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:02:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 04:02:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 04:02:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1327734170da8c4ae4171fb4248189d0691d6b4a3f01b09239c3e34688651`  
		Last Modified: Sat, 02 Dec 2023 02:20:57 GMT  
		Size: 1.2 MB (1198788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77125e61032dbbcd43c015fe756de97b5661bdbbf4f5219588148f651ae900c1`  
		Last Modified: Sat, 02 Dec 2023 05:59:34 GMT  
		Size: 5.6 MB (5553989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cfdb297cb2e56f5144d6a03d94e416f7101347779b1dac8d072ddb965d0b5`  
		Last Modified: Sat, 09 Dec 2023 04:49:40 GMT  
		Size: 3.6 KB (3622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ae93d7330b04913f411e004ee6e95c6f115a405deced6159ed0ae4c9987099`  
		Last Modified: Sat, 09 Dec 2023 04:51:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadbc41c419150c402c40f1d1eed2da57691737b48cfabb2a85a677c999bdb79`  
		Last Modified: Sat, 09 Dec 2023 04:51:27 GMT  
		Size: 109.2 MB (109169623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f16c937df28690cec98c60ae445a5ad2e4d5c2868816a30a5d8859297cd824c`  
		Last Modified: Sat, 09 Dec 2023 04:51:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:55b406840f898479b7a0328c20606d0e89db0d7395a55fbd410620b61a016357
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138623496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1518b44884a961e24c6b7102e8b5d9472a443ee4feda98c8adf5b233ec964267`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:21:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:18:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:24:08 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:24:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:24:09 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:24:09 GMT
ENV ROS_DISTRO=galactic
# Sat, 09 Dec 2023 03:24:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:25:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:25:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:25:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5d2acf9ee7cfde47b6ce997317767b8fa9bf8d93b8297016db9e093d06aa913d`  
		Last Modified: Wed, 29 Nov 2023 17:47:09 GMT  
		Size: 27.2 MB (27203865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2aa78ed8ad18394d7ae521e83b2810fec9fbb7d95aa074d794bb43e6e2bbfb`  
		Last Modified: Sat, 02 Dec 2023 06:56:12 GMT  
		Size: 1.2 MB (1198781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f106a95fef578814e019c4ac69f1cf32b15d5f85da2729a7ab2487c5d3505d`  
		Last Modified: Sat, 02 Dec 2023 06:56:11 GMT  
		Size: 5.5 MB (5532202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2293949a62535f558d267574d694fe0b0e9498fce13b94a8a2e83b00a4d86669`  
		Last Modified: Sat, 09 Dec 2023 04:05:04 GMT  
		Size: 3.6 KB (3625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e6106ec9b9e87d61a209dae736d5a55521179a1e971b3e19fbf6e6cf862b0`  
		Last Modified: Sat, 09 Dec 2023 04:06:23 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd4c4d79e02de926140a561865bc9b24c63a07e419305ab0a1deae10efadf8`  
		Last Modified: Sat, 09 Dec 2023 04:06:44 GMT  
		Size: 104.7 MB (104684595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b236153245646eabf2f747172467aceaec88d3f377325803397c5ea67e5fd6e4`  
		Last Modified: Sat, 09 Dec 2023 04:06:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
