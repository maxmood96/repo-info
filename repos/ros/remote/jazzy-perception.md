## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:f412f8df4962e6dc579614aca091ede18fa00fb2c6059876282844fe8af07151
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:1c35184faff5565838285a9db9c6baa33a61fb91106f2f2454f6981ab334c849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081434248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b72117bb7b4047614b58ca55a535c6201414f69543bc9aa5e85b2c61e3321a7`
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
# Mon, 11 May 2026 19:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:12:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:12:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:12:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f2d79ab55df243721787bae594a1869e32111c3fceaedf29d6c4916281b829e3`  
		Last Modified: Mon, 11 May 2026 19:13:12 GMT  
		Size: 110.7 MB (110661006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefa18366212cb7871cc063fe2189897ae3ede04c35065e1041761e727a04552`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 414.0 KB (414006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437c42b38e5dd4ff52978453169e4760ca982ed52358da77cf1428e1d0a35dc`  
		Last Modified: Mon, 11 May 2026 19:13:09 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626295b76a9867451fd495dd438f1ca2575ab6ec87675aebb1b6e00ab43fa94`  
		Last Modified: Mon, 11 May 2026 19:13:10 GMT  
		Size: 28.1 MB (28068784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4640b83eb291263d8fda37113525b335f47bb0162699941f39387d29872231f`  
		Last Modified: Mon, 11 May 2026 20:15:43 GMT  
		Size: 784.8 MB (784809341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c14163a6e81b9eddee217bbb6ce1c594e914f27b550d8d0c245c6da4edd71b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60974792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3256715cc88463d3817dc1e373c747df39026a6d5aa798a014720e36717d459`

```dockerfile
```

-	Layers:
	-	`sha256:4ce51c8c5351d0d442998b7f5d0be890947450514524ed06ca47b31add780740`  
		Last Modified: Mon, 11 May 2026 20:15:27 GMT  
		Size: 61.0 MB (60965453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a2afc85dff5086683306a95832eb05bc442b8576ceb3d5001738ae0da1d008`  
		Last Modified: Mon, 11 May 2026 20:15:24 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3e802f089163d4e95e49acb9faa4305dfc514e71e6f38cb3b36ca144b2eb6994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.0 MB (984011579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28797e96fee39d4fe724e8459af2043c8c1843dd50295fd5765be5984a1519e6`
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
# Mon, 11 May 2026 19:10:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 19:10:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 11 May 2026 19:10:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 11 May 2026 19:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 20:13:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:53ef13a8256deb85c6ab6c779a50cae10e54bde2a7710d853fbc47767a135020`  
		Last Modified: Mon, 11 May 2026 19:11:38 GMT  
		Size: 106.1 MB (106088503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764e204c60f127cbe48970ee27259bf80d1c1ad40e5b4f1f7833f50fa8468c99`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 414.0 KB (414004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f824c1438b2e0ad2054bdea0f885c631c4527adf75a317d1de5d764fb90bb3`  
		Last Modified: Mon, 11 May 2026 19:11:34 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fdcf0407801b47e4bd3f232539f37ff6b13700e812eafeb81b0ff220bd8dc`  
		Last Modified: Mon, 11 May 2026 19:11:36 GMT  
		Size: 27.2 MB (27178247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755f8136493ff290781635874e2968eeeef4de3189dc6d5cac9f7a92ee0e034d`  
		Last Modified: Mon, 11 May 2026 20:16:47 GMT  
		Size: 698.9 MB (698914001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:b02f59c72098e60762aa33da5a2422e0e55bd8b146f105ec1365b821223c0e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60905387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c537faebae8884066db5476f9c9bb5c099c14d30fe8e1224d90c3ba3fc40092a`

```dockerfile
```

-	Layers:
	-	`sha256:87156aef9397e47eeff8049980d0816f33f14a8b252978de1592b020c9e6d988`  
		Last Modified: Mon, 11 May 2026 20:16:34 GMT  
		Size: 60.9 MB (60895968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45385e82a599ca93889539a95c402fa1ef8ea8f8be54b282ada5cda17a2f60be`  
		Last Modified: Mon, 11 May 2026 20:16:31 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json
