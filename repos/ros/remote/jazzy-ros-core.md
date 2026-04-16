## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:096dd6d816e697d0019c5cb359b37dae356937e4fd1ebcb27731a4997eff6973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:25ecd0066934e6385aef56ee218dc994fcc1f9ff9b45b4ab64a0f0fad50aa10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157448749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26241c9bcab8ee0d629bd9279ed24e4fd0fafc381bbd07a620966a6761ae0a0c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:132ccfee487ce76a1e79ab32fa9725a32fc9a0a015f1750a543fa5c13c2e3874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18498532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f607aed76ab4844e22e466f8a170291b8867979666edc49ebd78f1997069a6df`

```dockerfile
```

-	Layers:
	-	`sha256:7eee6ca82fd9a65f91eb19bc884dfb004ca9665fd3121ce4082a08244db23b8c`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 18.5 MB (18483934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789ea6ed1a0e01d9a9ab602effa6e351200a1d147cbf9d423d0dd6b6ab3f1ce8`  
		Last Modified: Wed, 15 Apr 2026 20:55:23 GMT  
		Size: 14.6 KB (14598 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c80d117901cff9715cbee9b285e314d327632ef44805c7ffe4213fda7bc386e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151387522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94f6cd7a79da8082a6e3ec37299cc5ce99b5ff913b1ca6766d644e4f5706bfb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f03d27308a75556d0e50919fc87a82d6039591164c629953b7c74777a1c1d46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18472665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83656f21c4b1b74f39333035358b405b25ef25047378a831895f6737cfd038`

```dockerfile
```

-	Layers:
	-	`sha256:ce62b64a061062955d40fa45ead6428baa6f9b304c59c72fcb21c77992a6ca68`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 18.5 MB (18457940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06119fdc43365ceec6d77dfaecffd6bd8ebe35eb78d15b94345784b30481cee`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json
