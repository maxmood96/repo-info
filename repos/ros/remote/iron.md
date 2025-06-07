## `ros:iron`

```console
$ docker pull ros@sha256:923014f62b315ec219bbb2eb36642743bf2e90472cdb7ecf230b91f3a3d66200
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:4431362f4fdad4b0a5cb2437b91bfbd786c615c9c3c7a30679483993d0fa8329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267781074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc90dd951c183cd8de48e40f38228016e0c87acb13c92d38f28bad4ec4957fb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb9b3cb725d901af48e802f77ce73047c3689a12baf83905c56bd207982caf5`  
		Last Modified: Fri, 06 Jun 2025 22:49:19 GMT  
		Size: 1.2 MB (1214032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f141b6dc13f270c4f52ae21bfdb4af90e188ce8b57cd7ca5cbcb4308ea5180d5`  
		Last Modified: Fri, 06 Jun 2025 22:49:19 GMT  
		Size: 3.6 MB (3625827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7471adfa037bc44bef892286aab80c5af5331c2dee7b03f68c41a2b7dd95517c`  
		Last Modified: Fri, 06 Jun 2025 22:49:19 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a016a720aca2677cd85c28ae7e62ff9f9cb4864e2917d84c89ecfafd14c65b4`  
		Last Modified: Fri, 06 Jun 2025 22:49:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f14b329843fd765c3130965a174e03696f308b064db2c5aed6b4e45bd1aa2`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 124.4 MB (124356749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026118e86113f0f5c37c1d19ef1dd9ef5197c1ef2c62dc7dd8baf86a497be232`  
		Last Modified: Fri, 06 Jun 2025 22:49:20 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b53d37ed5500a235844cce8c59eef26c09e6c6d3fcdbf06e9a4deda8b98fb3e`  
		Last Modified: Fri, 06 Jun 2025 23:09:14 GMT  
		Size: 85.0 MB (84979032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35e67328b168297627618c8d3ea48cafa10b062280414d60c951ef8280105b9`  
		Last Modified: Fri, 06 Jun 2025 23:09:10 GMT  
		Size: 330.2 KB (330190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facab70c82f5bcc5c39f5cd43289497ad735cbb1b4f6860429582c18b1c400ca`  
		Last Modified: Fri, 06 Jun 2025 23:26:13 GMT  
		Size: 2.5 KB (2466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76283d507f7ec386e1442325e4c1328ea3f840e88a09e92e4bbeeed21c3d9639`  
		Last Modified: Sat, 07 Jun 2025 00:07:54 GMT  
		Size: 23.7 MB (23735265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:37da59ce377a09ca7bc16a9475531be8997206c67c196c2652e81c7e6581300e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24429402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10031ca80f5b7624771ebc28f39d28e73c661f85a80cc176b04967dd09906317`

```dockerfile
```

-	Layers:
	-	`sha256:36128da55ad62fa772cfb7726ac1533680a74c4b71f9382acc9061c3141ed638`  
		Last Modified: Sat, 07 Jun 2025 01:20:43 GMT  
		Size: 24.4 MB (24412278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098652041d9b1c18f505491eb90b8c8a7d45a8a275133ab61bedce1950d08156`  
		Last Modified: Sat, 07 Jun 2025 01:20:44 GMT  
		Size: 17.1 KB (17124 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e8ca5280de31dfc50a3ae12e2d33849c9ebe3bb5a49898881b3999a45c5284b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260101691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee6a09af01bd83f645c08b081ba17d34580e9e9b9ec3143faed81ce0bd47241`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7825d6a3f468116a5beb6ccde15d08c8df7fc2b9f4a7050d39cb6c58954659bd`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 3.6 MB (3597269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073bbc4a8060e2f431ffbf70e895ad6479cc9bc9e6e271caf597fc13a1f30048`  
		Last Modified: Fri, 06 Jun 2025 23:16:54 GMT  
		Size: 4.0 KB (4044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d329fc5b6ba2fdfdd0d4fcf4fca5fea50534f6d4e9cb4821de839e1e74b29287`  
		Last Modified: Fri, 06 Jun 2025 23:16:55 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e030c6bfe0f32b883f70ce9e56cfa239d4feee88bf45f9a74e8d193aaa7f4c`  
		Last Modified: Fri, 06 Jun 2025 23:17:01 GMT  
		Size: 121.8 MB (121816321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577601e3b1bcd6f4054acb2af03dad2078b1ccd23428d6ae0a262f08b4ebf1f6`  
		Last Modified: Fri, 06 Jun 2025 23:16:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b6673922d2ccdf14c63da73eddaac83cb8f5a98d13a5b5d3741697f5ef8d8a`  
		Last Modified: Sat, 07 Jun 2025 00:49:13 GMT  
		Size: 82.7 MB (82653152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e3c63811aa5833b3b88eb4b2527254bd0d6cc0d19d5d9a8b24d168e05580eb`  
		Last Modified: Sat, 07 Jun 2025 01:06:31 GMT  
		Size: 330.2 KB (330187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef485294f7a8192538b1eab0182c94e103d77e3706dc2d030d572bcabf297dd3`  
		Last Modified: Sat, 07 Jun 2025 01:06:34 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2f795302fbc34b8f4bf9a0cd098a15003ad6cec21ee93c7cd298c38022d38`  
		Last Modified: Sat, 07 Jun 2025 00:49:12 GMT  
		Size: 23.1 MB (23128008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:d002fe40ad348d6dbcd4f5442c53822352bb4ddf2c34888fcbdd13b14c5d5dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24442739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2402be6ef59a08ce1f77877dcc90758122f98ff3a3a6d2502a1410a74fb783b3`

```dockerfile
```

-	Layers:
	-	`sha256:a5e5629dfde755cb1874fc5715e9bf939f9fd2e127d2c1d624afc9668d0995bf`  
		Last Modified: Sat, 07 Jun 2025 01:21:02 GMT  
		Size: 24.4 MB (24425478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ecd10b7ad5c24e35fe7e41bcaef67a95f6c1e93c944323597f3e846dee97ba5`  
		Last Modified: Sat, 07 Jun 2025 01:21:03 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json
