## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:02245a7ff6e40181fc132a1dc2dcafc7d104851c2de4b1c4e5fbcc9a1a6f0734
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:86ee978085ad3d1521ed99a29e2b5b50a8099b6a773efac726229a84bddc55bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080367749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc49cca7ce2ae5c6fd4265bc54c8d8c8fbca7c185af56bdac4780b2561d0729`
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:bd9849a67d447e38d5327e338d8d044b287306fef1db1a27d42e4333b6ada930`  
		Last Modified: Tue, 16 Sep 2025 01:18:19 GMT  
		Size: 784.5 MB (784468592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e6bbb783012fc38bcce9ac706d29cca93a3c6db494037daf9a9cab42616991fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60714690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925eb7cc995eb60657091e2e7bcceab883fa64eed5c740d008caaa24e277715b`

```dockerfile
```

-	Layers:
	-	`sha256:2284225dae7197ae61ef7f95038613d7421efe4d3eb5a87055bd7b9984738bb2`  
		Last Modified: Tue, 16 Sep 2025 01:17:37 GMT  
		Size: 60.7 MB (60705309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3632f1dd3840c377f6242d97a42bcdcdedc8e42741c7a66df2f7754a6fd0140b`  
		Last Modified: Tue, 16 Sep 2025 01:17:39 GMT  
		Size: 9.4 KB (9381 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e3d12876a44c5c13223e60ff755d5d2114f5b1f8f6d23077cb304c9257bc710b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.8 MB (978825934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21757d92d688ec5dd4f10c3e07d4fc05c4f7abcefccacab8e66fb3efc8e96d87`
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
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afe45326b33b72902c4bd68b7c8798bac7037433a4b4f545af4fec05dffe990`  
		Last Modified: Mon, 15 Sep 2025 22:23:33 GMT  
		Size: 684.0 KB (684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d740f914ce1ffd99f507c92fa25971ff588ee996167913e4394c9957e5ce275`  
		Last Modified: Mon, 15 Sep 2025 22:23:32 GMT  
		Size: 6.8 MB (6759958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce5412b91a44dc2aaa0777c15f80990638ae282683241432dfff3677ca16cb`  
		Last Modified: Mon, 15 Sep 2025 22:23:32 GMT  
		Size: 94.3 KB (94274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f3d89bd8e41e0665381ccc6f343cfcd152211f034fc11d6312e1f378ddf328`  
		Last Modified: Mon, 15 Sep 2025 22:23:46 GMT  
		Size: 114.9 MB (114876898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19abcdb5bc0973e97ec396544e74248ac1e4fdad4761edcffc72198609bac108`  
		Last Modified: Mon, 15 Sep 2025 22:23:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659050775b8c0fcd8f319ffb401551dc2f92291ff5f2a0b0a4d9481e39dd7090`  
		Last Modified: Mon, 15 Sep 2025 23:20:59 GMT  
		Size: 105.6 MB (105590834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c342d9fcd518f7daf5ca429d8f93c14f9486753addd699dc0c069227b01e20`  
		Last Modified: Mon, 15 Sep 2025 23:20:53 GMT  
		Size: 376.5 KB (376493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a4e76cb15008337901249e3f844ccf54b154b5129058cd7ad0424c5e1243e5`  
		Last Modified: Mon, 15 Sep 2025 23:20:53 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8dc2308420a34a89470534a991650fd2b5625b8be7e74321216a56e57cb355`  
		Last Modified: Mon, 15 Sep 2025 23:20:55 GMT  
		Size: 27.1 MB (27096015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edaaffc46558418948de110a6ef7ec4876b6d605ce1664cf1c6f84d37263b00`  
		Last Modified: Tue, 16 Sep 2025 06:41:04 GMT  
		Size: 694.5 MB (694483435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:8376c2d21b173f5719530d9f8b3a9d424632067253cc4403107af596d974dc47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7274710f70e756155f408adabb4af8278c92c588bb444c94e4c7922a33f319e9`

```dockerfile
```

-	Layers:
	-	`sha256:54f6aeced5ef1dd159662436f18f292fb23630fde0039d36749d1bb3681bc239`  
		Last Modified: Tue, 16 Sep 2025 01:20:13 GMT  
		Size: 60.6 MB (60635834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa84f735e59d6c035a6cf40724f9116c710aacc80e72e10745b4efa1be8ee317`  
		Last Modified: Tue, 16 Sep 2025 01:20:14 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
