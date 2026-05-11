## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:bcb227cb080b774ea58dab3d0af23168fb227d5f35104e3664c52bc1c8240051
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:0fc162ea3afb430ec3d19d5fa286b45f1f2846b5f57ff8880735e07fcec542f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157478623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d68c353f6974f34f875d2fc4bfba8ebcbefa6f8499ecb44ebed59c439d01fb`
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
# Mon, 11 May 2026 19:00:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:40 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:01:15 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:01:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:01:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:01:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c94fd66e3352f9890bde8c12bcb1e4bac0432bf78a320f9c2c1e7015228ce`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 684.0 KB (683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6649a1dc8968bdcb81e364d602ec1bbfaeddf0f4b1ee8d8eaf3ba966062d0be`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 6.8 MB (6752204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872cad1997f18f1c0b65839c92ddddf1b5f9d577c27bb7b55a8e51918db2957`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 94.2 KB (94169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecf1e25d032fbc5d95d2c3934f5cabb82c1f0db841b476c12c9c41d226988b8`  
		Last Modified: Mon, 11 May 2026 19:01:46 GMT  
		Size: 120.2 MB (120215105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4e5a95f9df9ef93e72e3a576cd5f8f1d3ace13cc9b7296cece241e22f44fde`  
		Last Modified: Mon, 11 May 2026 19:01:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:158a72148c5a5b6f4f91aefc943c89083cc627b5a90f4184a22783246bd71f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18499978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7584a3829d92e76706b3458fa6f34d2bc24ed261c4511f312f5c2976aad92fb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a93c8abe0b8a8ba5fae670aa9d9282e23241784e183c11ae748c0e74b7a4202`  
		Last Modified: Mon, 11 May 2026 19:01:43 GMT  
		Size: 18.5 MB (18485370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19dd046c746389d89df4cf5773cd71cc8b65051205d8eadd466cbdc5a82113a2`  
		Last Modified: Mon, 11 May 2026 19:01:42 GMT  
		Size: 14.6 KB (14608 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b15262cd19f96863eef62ee766c93da52cc5e663e437acd14ce6fb4488a6c01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151414314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000971ca2196011fe2a8adba160fbbddba9c4d11b3b6ad4297931dffadb3c24`
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
# Mon, 11 May 2026 18:59:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 18:59:55 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV LC_ALL=C.UTF-8
# Mon, 11 May 2026 19:00:41 GMT
ENV ROS_DISTRO=jazzy
# Mon, 11 May 2026 19:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:00:42 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 11 May 2026 19:00:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 May 2026 19:00:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3e3b1dc60385babc924df082077517a52656ad26a6fd66982bfa8b6f73174d`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 684.2 KB (684199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571c28708c004fd152b4d4056b7e7ef6a8f80c148f3f1afaf999193d3ee7db`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 6.8 MB (6765755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031bedc2c9882a0946a305a494b2135bcd8b3956588da28af565171bf0164a8`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 94.4 KB (94373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f195799a078fccb27e645dde1908bb43f496d7e0d9306145833a25563ef976`  
		Last Modified: Mon, 11 May 2026 19:01:13 GMT  
		Size: 115.0 MB (114994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f91dd065b35bf9372598a188657b8a4f99ee09bd7563ff78e57537802f98a`  
		Last Modified: Mon, 11 May 2026 19:01:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:25b5e6cb76c9e746b94b69b41867ac88d0b58c3e0a753e2b52841e92f2b7dad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397d24e9dcd3d1ee6300541c483b1c17c7ccd458e9fb3cae45205719dfafc90b`

```dockerfile
```

-	Layers:
	-	`sha256:11b39afcf284a5e2ea25ed5501a44793025334f2fac0c09e493166154a1a33e1`  
		Last Modified: Mon, 11 May 2026 19:01:11 GMT  
		Size: 18.5 MB (18459376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06fe756ffee58f8ec8abc21d42291dda96fe283efbbf3cf8b89cc338827cf462`  
		Last Modified: Mon, 11 May 2026 19:01:10 GMT  
		Size: 14.7 KB (14733 bytes)  
		MIME: application/vnd.in-toto+json
