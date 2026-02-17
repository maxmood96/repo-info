## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:8da7f7fa59bd12358e5747d01f27cc72b170087d9385b518c409d78a708d054f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:142107517dbd635a465b087c93bd5baaa95ea674edb98971ddfc419b6dd2a710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298136760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1541b452cc1ef1bf23289369e927a6ef6c363a43cf079034898b62b3fa6e9f82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7664201107a73be69a1fcc67abe7b8dfba9f08f8ac21cd6e6653ff31c72386`  
		Last Modified: Tue, 17 Feb 2026 21:30:45 GMT  
		Size: 110.2 MB (110187964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ca4d412f7ba8e088e340e41db78e3af76477eef4de912442cad60baafe980`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 374.4 KB (374406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b84c226681e00ba22043272c1fd02b401bd4ef90eeb5d75340c924016701c0b`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f44533e62581038678d3c036cd8b357f29ecca65c9e45adeafa646d32244d7`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 28.1 MB (28064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:76bd4a9406e75fb1ce91a7ec01a8d57548e73b3fa3ae7e49f06ee73512c442ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24601050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61448b0d6517ebf743ef3cfa18d2cf8db4e3fa89627cf81f55d956619b218ee4`

```dockerfile
```

-	Layers:
	-	`sha256:e96a8d5c8c28953c60992748f592a29c89a24846347219530366abeb2cd963dc`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 24.6 MB (24584703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043e5fa61b540d977a745f78b99a2c7a43cd3f0684aca7f9ca74ad7057c3b7e1`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f485861c48c691bdd94fb5b278fae25bb65e23405ddc307c390ed1125b39b270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286462906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aec7a60265cff1010022fe066e76ac3ccdcd9cd58e296905e9df6d0d5ea935`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:30:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e37013cf9183e38cc9955d643924c43a7498cfc246fcbca68d2cd37ff696`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 105.6 MB (105600489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767953e8490b993e411a343f8bcff3b560c0ca2cbfe5175afe92ff040558a79`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 374.4 KB (374408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ebc39380b97a2003e0ec3a56e4d2013953c1ad0bf4c68d2bc22d7c2a61e80`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c245d1be384cea3eebb42dfd710b8a80c899f2db13badd8d32df1fd718dc4d7a`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 27.1 MB (27146333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:94e9b065f18eabbb67b64926525574cd16faadb1d19518951137e4e3a855c0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24623444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814b86870d96f8d262f86c272889f9c5b9ffcdda5498ee527a6480f2d4b4502d`

```dockerfile
```

-	Layers:
	-	`sha256:46e79985533ff02e1d666e674ccb4d3da616b812b93b3e30d83cfdac9410e698`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 24.6 MB (24606960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a441fb19ad061cae8b01e2aa0398c0b2e5842c36e59b060a46bbb6bcac5092`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json
