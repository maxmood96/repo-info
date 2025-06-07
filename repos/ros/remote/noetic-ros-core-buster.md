## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:556ed9b5e8a8afba4ffc7f84a6e12025ecf8139578f96d42fca7d0cd0dfe2aff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:38f1c060223b2e6c6b47560fd21620817609a7570fa909707b52d7ec5f3a276c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306073777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3798c3c90d1daae3ef8867e0322059db0530bceff4645af5f0022d3a2e9ece2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/noetic/final/debian buster main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=noetic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Fri, 13 Dec 2024 15:13:43 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592cee934a9adff7342cbbc6a887ade3408c48439779f6324665510a2b3eee1a`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 10.7 MB (10700658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53725fd6a1efa565e80ffec22dfec1aec196082d80e59ddfb11f79d86d6aa39a`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7027ac027521944b4d527509c9e64408524f714db5f3eb7db24b36c3947c519`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b8fa11775b938ce704d7a0e85f3a5a1c670d8a5505742c10c987346deb2055`  
		Last Modified: Fri, 06 Jun 2025 23:07:41 GMT  
		Size: 244.7 MB (244711338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208bc360693340c0084653cad3e347704144ab9bb29bf9a0d8ab2952fcc7e6a0`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-buster` - unknown; unknown

```console
$ docker pull ros@sha256:2a58580286c6e32569eee2aa8ebb07f07b2e95585254946aea08ae2cb3fa03f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29958213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cb197ec70fb6255a643a165d6de13116035b3d7c3cee9dec5280f4afea4937`

```dockerfile
```

-	Layers:
	-	`sha256:f5429655f60cc9f1e5c82ac5cc5f56e00c15be88c01ff597cd5f6e8becc0ab7a`  
		Last Modified: Sat, 07 Jun 2025 01:24:51 GMT  
		Size: 29.9 MB (29945658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305005445e99eec301b707d04b7b923cc072e6a8a0cd325b3395a52485d08539`  
		Last Modified: Sat, 07 Jun 2025 01:24:52 GMT  
		Size: 12.6 KB (12555 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c9c74d7ed436263349bc0ea51d16f63231dfd20cce2bd4c5ccd138ad4fec7798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249206991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef46bdfa4793d30db2337293242a0c47003907c62eb35fafc11b7d82d29eb4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/noetic/final/debian buster main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=noetic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Fri, 13 Dec 2024 16:38:19 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f35ccbf79a842b1dc8f347bdf3cd4c9e8ff3d04fedab80030644cc1c81fd2b`  
		Last Modified: Fri, 06 Jun 2025 23:01:09 GMT  
		Size: 10.7 MB (10706443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0feb157d1ea993f3e44f6dc61b202f82dd11284dd48665846def3c4bee2a5a4`  
		Last Modified: Fri, 06 Jun 2025 23:08:38 GMT  
		Size: 4.0 KB (3987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1160b9b3c836ab8493c6ea91b3af6c6d942ca85290dc7c9b7f8fad0f0f8bea`  
		Last Modified: Fri, 06 Jun 2025 23:08:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daed68793c5fc7a0ae25e2497c554fcaa1cd4391a8020ec7c70ed8ea909d86a`  
		Last Modified: Fri, 06 Jun 2025 23:01:13 GMT  
		Size: 189.0 MB (189042883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37659a0e86f6f971277bd12fd260edde892e084b66f66a075189c47c74edbca6`  
		Last Modified: Fri, 06 Jun 2025 23:08:48 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-buster` - unknown; unknown

```console
$ docker pull ros@sha256:1ed13ac181c15cd29993bed8b077bbc171e5050b1ff6ceed5627d4216381027e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29852049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c22880cc3094322c5181d3992a24f8fc2ac4246fc2e037581119e1d0003aff`

```dockerfile
```

-	Layers:
	-	`sha256:a1f3f95c72c02ae85d386d530b79c7a6f01375428aaa8f6234acfb5ca5ba0367`  
		Last Modified: Sat, 07 Jun 2025 01:25:21 GMT  
		Size: 29.8 MB (29839386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9a536b02583696085cb574465cd4a85ee6bd97118ea6af3411a34dc3177649`  
		Last Modified: Sat, 07 Jun 2025 01:25:22 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json
