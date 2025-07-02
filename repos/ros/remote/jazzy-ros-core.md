## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:9d2c6cf976c3819b1423d646d71b3571c1ae79b10480bd7b00c73e1e57d19748
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:87a6bec8689eb8299ca5bf7065b994df4345a312cc91333d36afbbf4ae5521fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157171438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c34c30ae19587c16e48deb0e2c79f66ca42a3bd518ff1f9cb128bf4fbac1bbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:57f546e00a2e9a2b998ec6f62f13c7434a948e8bcfca880bacaae5a3a1b525d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18309089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e8b3ebd1c3fd8f991467aaadc8d910478d6de8cbc6e0c485a0d88ebbce2d2f`

```dockerfile
```

-	Layers:
	-	`sha256:ca5040fc8da57ac37a2566346523cd9e4e3d425aff40f2ac565a65c5908bdb25`  
		Last Modified: Wed, 02 Jul 2025 07:17:54 GMT  
		Size: 18.3 MB (18294446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83896e6358063c249e8ce7d16eda8adcd9cd65189a300d3a39a78585b908a25`  
		Last Modified: Wed, 02 Jul 2025 07:17:55 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f732493fe5877da6b04b02156795aa6da912a8e6b6d4649294ec4230b517a550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151101359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce1228054e42dc12e90dd096c6b317e868eef394d4b95d10cb36f71a28dcd86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:768b49f1f18def116d7ac6f02c7f327b839957f935f9ef3ac4e71abc9995edc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18283220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a339e9d643a2a09474de8315d5d2f502d3081f51c1344044b993fe702d7407a`

```dockerfile
```

-	Layers:
	-	`sha256:f26f2c06d2835cc809f9a71ca9f1d7d072e6ca9ea76e7a7d1b2692c80b36be81`  
		Last Modified: Wed, 02 Jul 2025 07:18:07 GMT  
		Size: 18.3 MB (18268452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfef5223b7b48f5fbd8268ff766a086e20b2fc7c9e93e040509cf4fec9f4b716`  
		Last Modified: Wed, 02 Jul 2025 07:18:08 GMT  
		Size: 14.8 KB (14768 bytes)  
		MIME: application/vnd.in-toto+json
