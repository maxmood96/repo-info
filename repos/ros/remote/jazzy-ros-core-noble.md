## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:4f2536852c6771406708e351858c2b3d0b1f9ad628278c33ecb179f9dcf4ad5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:b562f956fc138f4741ef99a7ec7da6cb207f968ad78431481e76ae3827572568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157358498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27aa14f9b6c9b89befea3bcdc02299c8458b975d6c04dcfd0d4a3f59ab815f0f`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d108b0455d26874467bb535ac1b0fb32de8c484d3ffd3710dbea124ffc245adb`  
		Last Modified: Thu, 09 Oct 2025 21:24:11 GMT  
		Size: 120.1 MB (120110076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d51c9d4c4e7ee2f490765efc765899f07ad09fdba245ea055344af0b2e9f2d`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5b70d0eb9d9656cd82057b9c5c9b3aaa73d7df9716c946e4221433c9c0d6df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18314538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e518a419ab6d84ad80b001b66f7eca9181a9e0554d3c132a959c8c3b980d6`

```dockerfile
```

-	Layers:
	-	`sha256:745c761d3615d3a2597c85d87c43733490c1102be429cfabbe2bfc96f682f38d`  
		Last Modified: Fri, 10 Oct 2025 01:17:52 GMT  
		Size: 18.3 MB (18299895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0abe9db77d50e2e696d7fd5d096dc5018e2dac7548662f4bd8f3cf65ec5b4b7`  
		Last Modified: Fri, 10 Oct 2025 01:17:54 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b5102a569630d1391222b5aa6ef6e0ccdca9a4775291abbf4f422de5954103ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151294155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8210fa0488361c2267050d8d5e72d5051ab64916ddf394571840c765afa3794`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb091d265588996d309a696050b8d873efa1a977c33604e5241d0745dae157`  
		Last Modified: Thu, 09 Oct 2025 21:26:15 GMT  
		Size: 114.9 MB (114893499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1fd8e39aed1e99b329b904170291216c4df87e9a05ceb6e27c4e277cef7e6e`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4495fd35e1ec208fee280e5d5ce58c24feafb4f655f933c5e54e57f6df389bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18288669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82891b0d2625a4b9962d02deb7490ce3e320cf12a30b7161d0e966c3f2ee21f1`

```dockerfile
```

-	Layers:
	-	`sha256:cf09b7b71608b18f11fcf31d98f8974a7d9498198841cc56c43e1fc39e77a2ec`  
		Last Modified: Thu, 09 Oct 2025 21:24:10 GMT  
		Size: 18.3 MB (18273901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989bbd24ee2de74d927a6538ae8f557fcde6bfafcf6ec9ca08f5fc05379233be`  
		Last Modified: Thu, 09 Oct 2025 22:18:41 GMT  
		Size: 14.8 KB (14768 bytes)  
		MIME: application/vnd.in-toto+json
