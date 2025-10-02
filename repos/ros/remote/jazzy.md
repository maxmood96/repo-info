## `ros:jazzy`

```console
$ docker pull ros@sha256:84c6d227cfb7362a43f5520d50b3c71d9dd876b0eb14a6cbf57642302d4052f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:2bd04827f4462cdf8098c71a265f12cff4aea22a9d4e3c5acdd9aa75b30e0355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295899157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9754767980152367adc12157d3406a2d9080e9994bfc54baccf249a3c2cc2bf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1090f035fbb3dc8bff3a56b524d81b9bff6d998a0a78d6e678503894be117f`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 683.8 KB (683822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb53581a15804c55072740da9f13b016d0777a3634e94bab7a8a4df208f2b99`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 6.7 MB (6746858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e479f0117c61cf443355a1be70fb06e043d70a323af3a3542f6940e3ac348b`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 94.1 KB (94065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3827cbce68e708ff8fefb47ed721c708e9b631f8adc64c2474b51d4f31647ecb`  
		Last Modified: Mon, 15 Sep 2025 22:25:46 GMT  
		Size: 120.1 MB (120092087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200725f5cdae6e8eab61a6a056105dd4adf3b52c0299b2f6fe3b53066de58cd4`  
		Last Modified: Mon, 15 Sep 2025 22:25:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0523a66e924be7abe6f7b9d4ce7c5cadaa9233be337776ae14f92491ccbdc71f`  
		Last Modified: Mon, 15 Sep 2025 23:21:06 GMT  
		Size: 110.2 MB (110181982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ced83196a2edff71faef07a7a0cc8ffd99d3434634b0fdda47e1d195fe8cef0`  
		Last Modified: Mon, 15 Sep 2025 23:21:03 GMT  
		Size: 376.5 KB (376498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c281d4b675e614a6b07c1c78576063a9fa9168cf623ee86c3f6339822ddabd`  
		Last Modified: Mon, 15 Sep 2025 23:21:02 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6863cb938247e1b255f5eb5b18b9eb0187b1f7e4fa687f1153af70cbe295b17b`  
		Last Modified: Mon, 15 Sep 2025 23:21:04 GMT  
		Size: 28.0 MB (27997745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:371d4d64014e521c396df2d39dd38addfb977ded9dda0455ec9075c503006756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a439d2080156f4dead34dea48971cd9c2a46f0ea569974e34a29bc2445b96ad6`

```dockerfile
```

-	Layers:
	-	`sha256:b3c7968144705c68ea78ef6cf9b429fd4a6f2cfd79494ec085a732850a0e2bcb`  
		Last Modified: Tue, 16 Sep 2025 01:17:27 GMT  
		Size: 24.5 MB (24543454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad5772f2fe31332b047e2891c3e8ce432551a9e4a7247e74147da03ae7b471dc`  
		Last Modified: Tue, 16 Sep 2025 01:17:29 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3d0e5b652b7bc395b79e6bff9e10e35e862a5adfc7ebd756d0a198faa2c0eabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286576562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b913ca6da461594facd10ff82b6ea5e40e574b18ceec831c3b7ad5673dc06f52`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c230c754b06fb1abaa171cbe1b52c8a718141367beba210225ebb9d34dd9d027`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 684.0 KB (683992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d38513ca49b6b0834c47cf6b18e52e2642520ec4454634c02f8da0d420d270`  
		Last Modified: Thu, 02 Oct 2025 02:25:10 GMT  
		Size: 9.0 MB (8974004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d914f9184b30f554f13bc5d41e195dfab61a67de52741a2f3198f89b17d10a`  
		Last Modified: Thu, 02 Oct 2025 02:20:41 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d788dad654f531b2f7d5ad87a14b113aba8498aa7be02cc4dff8a39eeba0c41`  
		Last Modified: Thu, 02 Oct 2025 02:25:25 GMT  
		Size: 114.9 MB (114893855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee96a6e101843cdd99aefa321431376ce8e031fa4892c4b90281e38e99e3814e`  
		Last Modified: Thu, 02 Oct 2025 02:20:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a8952246885893e275a8e591e2b0b2655986ed266dd7d095c1612787fb5772`  
		Last Modified: Thu, 02 Oct 2025 02:29:07 GMT  
		Size: 105.6 MB (105591038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb9b3bfb92d462971d8c1fa71a749beb3ff42f30f64cae6e43939a837a3feee`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 378.3 KB (378300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de80e031b87f9b8e4cacb07195ef625d7d807a160cdb8fee8cacfb1a7b528b`  
		Last Modified: Thu, 02 Oct 2025 02:28:55 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a4441c07ec5481a13edab2cd51d04b856a326c4c48c05b6eec13c65e492433`  
		Last Modified: Thu, 02 Oct 2025 02:28:58 GMT  
		Size: 27.1 MB (27096846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:c2f7c6c797eea4625f53276251170cff19433ffb3f5e9e3c53284d3f2efb08c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24582540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff22f022cce7b94679cd1f691bf2f478261c95ef41fc1f7b39d4905082e987e`

```dockerfile
```

-	Layers:
	-	`sha256:36155c38a5edb438516abb1f20660b99bbc32576ac6b765d7e5c63706c578e5c`  
		Last Modified: Thu, 02 Oct 2025 04:18:05 GMT  
		Size: 24.6 MB (24565727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3f26318a42f5ecbcc048c1478bffee73eb09c82fdf00ce4c1242b859c846482`  
		Last Modified: Thu, 02 Oct 2025 04:18:06 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json
