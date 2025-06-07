## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:233f8425f29a42bfbd95de9acf216921191cbc3d5421ee41139ec4946b80d258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:bde7c8b6d345de454b5dac6f5249c55bc7a5cc7a2c2986cbe4b87faff74fff67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad133bd4ef06f61336eaf87844a7d4d40482b853caa2f74682322914076a9e1e`
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
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=foxy
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:905dfb1bab3312147382cf593a88dfd91dcde255426f42b174c0a00cbfee3d49`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 1.2 MB (1194819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf200ef89210ac612db81e54c264d517b910910145ae871d765696f0b2599d`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 5.4 MB (5363903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09efa67422b34d4c77e03962a93fb1c22f91239484ef3e692b04953247ee3d`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc4be6b715533df3810ad59eb7a493b1ad5a0fcd129ace37d611a85328e0d7`  
		Last Modified: Fri, 06 Jun 2025 22:49:35 GMT  
		Size: 125.6 MB (125595150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ea74b1607fc4dd1a8f37902c6ebe4faef897ca6c038ccbba0f66427232b7844f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18628064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea580783e9d8620d49f8daa117bd8ddcb2a6ea4178f22c318539d1acf6f53579`

```dockerfile
```

-	Layers:
	-	`sha256:06018cbdae5b90c89e6bee62965594d9d4aa5bf5746638138d8dd2476b3d5d38`  
		Last Modified: Sat, 07 Jun 2025 01:19:32 GMT  
		Size: 18.6 MB (18612948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f39e5d5101c1bb0ec4c1b76d33068788647bddbc3a45cfd2a02db9440f53ea7`  
		Last Modified: Sat, 07 Jun 2025 01:19:33 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bd8104dd64efbcc029bdd091ff0f48d2ae1534af3a078aa1ebf0884052daf4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141399846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc117f8978792a3b3742858bfdaa5357fa37bac5abdce2de50bbfbcd4c2d431`
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
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=foxy
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:fd563e74b9280d17b11bae86038561c7184eda5ae05a08570ac236ede7caab26`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f376c0b3101d22149ca2d878d920aa16f69ba90b157b102210f0b0216b96c6`  
		Last Modified: Fri, 06 Jun 2025 23:12:25 GMT  
		Size: 108.9 MB (108878978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8bbf8c8a1cae034a096fd542d615567aabad879961709c67a9d412fa9cb10c`  
		Last Modified: Fri, 06 Jun 2025 23:12:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:814dd8552cf538bd3e2b4136a218e10b7e798a9fff5fc58a999f66419ece5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17546520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d19296288acc8269f4632218eab94f56376679f69743854981d09361034737`

```dockerfile
```

-	Layers:
	-	`sha256:fbe35413fbf6cd78b976514fb78fc21327f4c016ab9c7e0cb68df7a9ffd89c58`  
		Last Modified: Sat, 07 Jun 2025 01:19:46 GMT  
		Size: 17.5 MB (17531270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7a234ca656e538fc6a75900ffb7883e26bbed0b16d27b333ee8dccdbab3177`  
		Last Modified: Sat, 07 Jun 2025 01:19:47 GMT  
		Size: 15.2 KB (15250 bytes)  
		MIME: application/vnd.in-toto+json
