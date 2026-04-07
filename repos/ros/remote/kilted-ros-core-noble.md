## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:5b77f83a3a50b3777ad50b3d2a97a97fdbae7e3ce359bad5b0964de2cb176049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:a32c9f3fcad0ab56e8f3bc92e5a25aff4439a0183d1e59c4781c11050d4ea432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158679332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d4f90e1c47c06896d89a1cdf97f43000560814205cb9517f1c4fda3cdb773e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8f0efb67ea2edd66de78221a30e607f3f8d1c338a88c7a674c9e9b7707ff924c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18503158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c67a49064f25ecfaf222bcaa307a5092662e58314140207de5b6b7ed9183f18`

```dockerfile
```

-	Layers:
	-	`sha256:ff7e426cf73653a4e56ae783c79b048160e2112e8b26356771add17146207731`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 18.5 MB (18488549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a1d769ed1985fea97dbb7fd3d1b64aa25dc9072b313b39b07af0628d92d1faf`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93815e796e1040bbdc6ff4ffea61189953ec155e2f71f9eda5c583d0d861fb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152558107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a40a844595baaa50f4f3684d35af6296ca04faa282c9c81ba0aacda90c3c74c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6381b1a882f2a22df58957277d01c30cede21d11f7f1b79529a546ed88c89083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff06bc1d858b3d8b4d48c6fedea1768f5a4859e402aa2587039d69043f4b626`

```dockerfile
```

-	Layers:
	-	`sha256:5825211cc812652427cca4a9a7955e1f75f6bf2e85fc8c3b8c380644e016f0f5`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 18.5 MB (18462560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e75081f1b7fb421b0a6c9049c5fcfa971a0a11c272cd348e1c28d823cb0b383`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json
