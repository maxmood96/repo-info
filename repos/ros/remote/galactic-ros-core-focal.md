## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:8f5a6326be760da91c01175d40bd70ee1aa4a159c0c50f03eebd42fc7bc814e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:548cb7cbc1f0f1bddf6119aaafd9c0f58d4c4d49979385f3506f508dcbc86f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143257724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b098d76410ec3458136c1083779e1b7d9632e00d5c54bb73bab856fda3b05240`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=galactic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945134a43cf5436bcd4c4fabbe5f8689d89a7e3813c2be30f673ddd81f849543`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 1.2 MB (1194815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddc9e11a6f24d45a0fd6c2fd537bb5c96fcfe7ad0f2a5534cc8f35938605463`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 5.4 MB (5363955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49802bd0654544e040c6c148afac52b1bc2758819ccf7844589f6ea1f8d42935`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4547639f65f5b71b189c02bc2917e674ef90e9b6aac3744e8961e9ae71488bc0`  
		Last Modified: Fri, 06 Jun 2025 22:49:32 GMT  
		Size: 109.2 MB (109184147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:3d840b0b1e25ec3dfdd1e6aa095609a71c48c653e3bc5ead24e0af09555d6d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17529458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617872342dc41f43ce15777a293a32bf0c10e480474dd48736cce76463dab31d`

```dockerfile
```

-	Layers:
	-	`sha256:f9556e6b5d67234ddbb1027d5eafebb92f48afedc0ad3ab84d357cc5826a3e7f`  
		Last Modified: Sat, 07 Jun 2025 01:19:51 GMT  
		Size: 17.5 MB (17514286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab891ec9bb5414a34308ecf2465716cafa4bc4982d8944350155dff3a264317`  
		Last Modified: Sat, 07 Jun 2025 01:19:52 GMT  
		Size: 15.2 KB (15172 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6f5cd9da10e0131cae5062e66a561ed67c3085e7d9e70fb4d907e1ba97b2d915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137195647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59688edd96d9a55b6d48b8331191b191d9ead03102fdbe5c542840e57213422`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=galactic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c8192db141ffbb5140fe411c5eced3897890db3b1fcea32de47823cb1e9f5`  
		Last Modified: Fri, 06 Jun 2025 23:24:52 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d05758778f2814758f8af46ee68fc371f4c70c37e44d6667bd998a6a401889`  
		Last Modified: Sat, 07 Jun 2025 23:59:04 GMT  
		Size: 104.7 MB (104674775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d724ca4312a3680a73d9b733e052cdc81fc0456386fb1c596c2520fc09de111`  
		Last Modified: Fri, 06 Jun 2025 23:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:ef5b00499c028f1c7e984c287ebdb0d972cb9f3219437caa066c276246817e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17521884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9ee7cfcbef04246e6b926052620d528750616ee431dc2c06308131090ee7d8`

```dockerfile
```

-	Layers:
	-	`sha256:b473b35e03df4ffd11151436147454b8ad88a0f1f1628f50dda41f95889d37f4`  
		Last Modified: Sat, 07 Jun 2025 01:20:06 GMT  
		Size: 17.5 MB (17506578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873ee2c735e58d05673811da84537673af3746b02f8c667a92f71831778f6d56`  
		Last Modified: Sat, 07 Jun 2025 01:20:07 GMT  
		Size: 15.3 KB (15306 bytes)  
		MIME: application/vnd.in-toto+json
