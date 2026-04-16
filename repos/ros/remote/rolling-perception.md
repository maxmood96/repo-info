## `ros:rolling-perception`

```console
$ docker pull ros@sha256:069adba4dc097602ecbadd22c372153c3b25938affe64e5e0a495fe665ef581c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:cb8a41af2ed2a76f76db40b01b92358356951281370e57f08ec55de3c5df8774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094485564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b7bcb8bad11923bc42d7f98bb7f5c88f7ff8e60932063c60e0070441fab202`
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
# Wed, 15 Apr 2026 20:54:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:48 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:55:31 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 20:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:55:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:55:31 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:46:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:46:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0644559dc6b5362253940942368861ced9f603361da89c3adf2fa73b1f1d8`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 683.9 KB (683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5df3be57e9c4cb62447529fecd13a1ab07bdf59d8fa4cec97baabb95b4e82`  
		Last Modified: Wed, 15 Apr 2026 20:56:00 GMT  
		Size: 6.8 MB (6751676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d348f5598561bd0e3f1088e2421dece24aa7886408f40050256c411670460`  
		Last Modified: Wed, 15 Apr 2026 20:55:59 GMT  
		Size: 94.1 KB (94084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12fc106e828bf5ff0f53383298b088f62734575daaaa2895be3f66ba1cfb54`  
		Last Modified: Wed, 15 Apr 2026 20:56:03 GMT  
		Size: 134.6 MB (134574573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d7c739ca6a59209f2846d72bacf015f1dc13907916eed58de4d11acfffc88`  
		Last Modified: Wed, 15 Apr 2026 20:56:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d0edaa250e70bbaa53abcbfe389b5fad0aa0ccf8a31288ff0f3bd56be0d828`  
		Last Modified: Wed, 15 Apr 2026 21:46:59 GMT  
		Size: 110.2 MB (110194688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd2230b661e86bd8f07be3fe552d014a6bb42e6c6f0e1fa2c4045df56aa97e5`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 372.6 KB (372604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbeb19838a72445d6331034c51685f40f29e6a1cea29183fb67841f42bdec46`  
		Last Modified: Wed, 15 Apr 2026 21:46:56 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07594a85311817fb2971d58169042e384d9f2ba674661056a4843248d2b2d860`  
		Last Modified: Wed, 15 Apr 2026 21:46:58 GMT  
		Size: 27.8 MB (27840246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ed1f57e9059a485b1e5e71e8465babde60dc3f7de0ecd9752523c2a077f6f`  
		Last Modified: Wed, 15 Apr 2026 22:33:19 GMT  
		Size: 784.2 MB (784238074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c7abfdaf5df307a548f5ad3e9c39e47ab0bae75feac9d8c34d9edde224780076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61807644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebe8e3a36e4932437f1afb456461c7b1884cf9524471ab087cf5aff90e40447`

```dockerfile
```

-	Layers:
	-	`sha256:35f28e8bd7242a5609b07d0a83c762d533f4baa63bf75d3daf7bf76dc0d173bb`  
		Last Modified: Wed, 15 Apr 2026 22:32:50 GMT  
		Size: 61.8 MB (61798283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9438d7fcb19ce4438bcf5a051ea9db28fdd034190be530781a480e7f5d5513d6`  
		Last Modified: Wed, 15 Apr 2026 22:32:47 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cb8c5ba66998e50f88675c26c4c0bc9198d5314ae14dba1d7f53ec47daa9211d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **996.6 MB (996620857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1bde9626d7edbea5f3a8d592c937df90f4ea49d3945e7ca4a57dff0288e3e2`
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
# Wed, 15 Apr 2026 21:02:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:00 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:03:47 GMT
ENV ROS_DISTRO=rolling
# Wed, 15 Apr 2026 21:03:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:03:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:03:47 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0639bafbbdc971f48d3d9341ef1217810bc7f8a0f7b5f550a4de4f1eda3ed`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780148fe500efb9da4f54261b9798bc3826e7511b420c2f83053c80259562034`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 6.8 MB (6764969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972cb309ea157ac41c9f5f3b289d2fc115949b136e8f5bc5ba4a4c5472ce2827`  
		Last Modified: Wed, 15 Apr 2026 21:04:20 GMT  
		Size: 94.3 KB (94302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf0b996774010d3f153bedf3c3543d44d56ca9dacbabda918ae7803e211d095`  
		Last Modified: Wed, 15 Apr 2026 21:04:23 GMT  
		Size: 128.9 MB (128910385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19150fbc2aa4d400a4aabdcb600258de379ad9fcb5fedb3ecf7c4f62e66c76fd`  
		Last Modified: Wed, 15 Apr 2026 21:04:21 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55fb6656c0bd58f1f4e8f0082f6663f39c311b9e6bb373a00bec4264bdd869`  
		Last Modified: Wed, 15 Apr 2026 21:59:36 GMT  
		Size: 105.6 MB (105607446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28d8aac2ee7081150c03cbcde7a4f24f212f4a35be4adca847877b6cb15dba3`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 372.6 KB (372606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b52b0368a0fe4002a81bfb4617077089e404ab39883aa6980f55d70d88ba180`  
		Last Modified: Wed, 15 Apr 2026 21:59:33 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f2e0aca8d3cc0cdc8879d700e1fc2075dd7294a0ed1274b4b4e44ec8a2ef97`  
		Last Modified: Wed, 15 Apr 2026 21:59:34 GMT  
		Size: 26.9 MB (26929600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1621f00909d53a407129792f8b61f3cd8ea2c0a6e80a4be628ffdbdfb7f05b`  
		Last Modified: Wed, 15 Apr 2026 22:40:59 GMT  
		Size: 698.4 MB (698378859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:d633aec837734ca70fe5ea65cfb24d9fa0a09d6f3699d7cedc89d0847a871cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61738442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f099555b3cce13a09b3e40c5556635f4897e91d2d510b94a3ede0775865e3b12`

```dockerfile
```

-	Layers:
	-	`sha256:2e8e4aff2748f38bb6aad8ee0a043395d67f4407b58c1295e7a9b780c6349d69`  
		Last Modified: Wed, 15 Apr 2026 22:40:46 GMT  
		Size: 61.7 MB (61729001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f931e8676b7db51c740efc2a54787d2e7b476619cf13fa19075fccdd6e727089`  
		Last Modified: Wed, 15 Apr 2026 22:40:43 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
