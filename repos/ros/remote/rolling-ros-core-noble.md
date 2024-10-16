## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:62b3e980c657f4b2667a3e0ca705b13b8ff9d93b3b5b21558777d6578d5194ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:158b80d4592b191a9650f3784c3ad8358ddfdcaf5bd9d7e256713a44142687f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157781076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a3750c536c0d3e85a4a3fa5b1e596fbf0d6c95d75f6f034f2f63d19f0bb532`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683ce39351d82fd950e092e88b264489382ee7a8011bb25a91ae065931834d76`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 683.7 KB (683724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3b9772f3202bbb08e9a737743bfada3868c76ea9cc44b353bf9b1deb0ac13`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 3.6 MB (3560038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9ce07c40bfee960a575dea3c30d31c04682b9fb99b7fa7238d0d2ddf23eb4`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca4c8456ef5db1377c36a0880dd7a288494a5cac776ca008c8f481539e99eb`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032b417bf94d18d3f038ffdda1575d627239628cc4d017bebeea601ce15e2178`  
		Last Modified: Wed, 16 Oct 2024 16:18:30 GMT  
		Size: 123.8 MB (123784480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f9730083900838d53743e27311546041b1c9515db812aad84ceda8a05b1609`  
		Last Modified: Wed, 16 Oct 2024 16:18:28 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:eb9338721e3ab85e974e2b9aab3cad6fcd1644a6252328e181f2fdf421c789e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17830382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fd36dba62e7ee96ba020704abb7c04ea4bd12dd19fef6bf10037b49d4d58c6`

```dockerfile
```

-	Layers:
	-	`sha256:06ff670d3a2659b9262c328e943527b497b5e5808c30b252e592bcbdc4996b10`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 17.8 MB (17814204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba6c527f12365b08feecf5130084fa9039e0f8507863fc9b58f3837aa6fbada`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 16.2 KB (16178 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2d1fd1d7abda6d3afb77d372d1e415b66b72b3c21cdec17f90d6e6409bec8b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151699929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6d8c00dfa58cc3c885db54d9d90929b24fa4082311860532c87e77280731c8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75906b0dbbabb024c7f890638530898ee5c0c44e20c5f9b2843574dc92ee4e4e`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 683.8 KB (683843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f509c8e504eee35bdf2f7a4cbcc4941d472d9a497b7f511c549dc7c5b8a4e`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 3.6 MB (3559114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed51f7b48cfd97dfccaca6e9172453c23a61383c3cbd8b7db4643cef6c1bc5b`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969caf6e5719f51692ea48756b21810e0471a7e3f778cd747e55d3becbd5e265`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ebdd9e47436c4391ff4f96f57db9ce3f74dadcba2a10820af55318e09901a5`  
		Last Modified: Wed, 16 Oct 2024 04:17:15 GMT  
		Size: 118.6 MB (118568656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6cc5189b8f5cfc989c33a8d416b71f388bda6054059e70948ed2ee8f2d8eab`  
		Last Modified: Wed, 16 Oct 2024 04:17:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ad8557dfce44bd7c02679a605d8cc07533642b3034268aae74f346433236ca6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17804487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae58938cff17919a68f8085d038d0413c9f5c247d2c13c2c5f812b1a7d5145d1`

```dockerfile
```

-	Layers:
	-	`sha256:8f267011f317d3d91d3e59e068c093132b637e41017c77035f4785565983eac9`  
		Last Modified: Wed, 16 Oct 2024 04:17:13 GMT  
		Size: 17.8 MB (17788175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3124b4341f0f34fae057f1d0eac8112454874bfc73238b3fe842a47305816f89`  
		Last Modified: Wed, 16 Oct 2024 04:17:12 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
