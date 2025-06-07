## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:313fa668db1b4ae5906dc7cbd8fe0dfa91a2d9dca3f79a08ee598b5ffa48648f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:abecde4d2da59d71741c97f381c4123cea5ed425192bcd91dba6a2b4b44ae279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.3 MB (960272361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c597b31155bc87299d34ed59833847b7d36d0ee2505c79f6f1157d483104c8`
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
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a8bda2abedb143efe345b7c1bb7d6b69f326352dd46aa347e5dc1660459df4ac`  
		Last Modified: Sat, 07 Jun 2025 00:12:13 GMT  
		Size: 692.5 MB (692491287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e2a9eb751658e8b69cd254fb6e1040e71886f2c4edbb12b6802bfbf8367fc57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59443422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f97f15c92182655e13cfa0efabc9465177bcc532c55630e96932ee547cfe415`

```dockerfile
```

-	Layers:
	-	`sha256:ab306db0eab49a8eaeaf3d5752cc52138bb84bc1703a2550c97b158db59f821c`  
		Last Modified: Sat, 07 Jun 2025 01:20:46 GMT  
		Size: 59.4 MB (59433748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0426d5a3f1093fc4236ac4c719735072e3e678568cdd46bbc8b81eff4698770a`  
		Last Modified: Sat, 07 Jun 2025 01:20:48 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:49a3e947dfa00660963b18f7aeef475f295136f6ec41f443c70e78cbc571c5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.5 MB (920460630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cce0c253ecc115d111945882d5ef97703310e19f0babdbd46b1a6bd857432c7`
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
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
		Last Modified: Sat, 07 Jun 2025 04:39:01 GMT  
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
		Last Modified: Sat, 07 Jun 2025 04:38:58 GMT  
		Size: 23.1 MB (23128008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c7500a406594913bb71a73415f0e07cbe518725fa29d0b9ae0d2d66e58847`  
		Last Modified: Sat, 07 Jun 2025 11:58:09 GMT  
		Size: 660.4 MB (660358939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:79ef688afbee1037eabc30e666c5905ab7169024eeeb025bb5452733483f65a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59428003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77653b4fb4db777b7b589a1eef07368a371bd1c9077c98f39ac5aecb1b8aa9ab`

```dockerfile
```

-	Layers:
	-	`sha256:316f9f499312723f0c87505cc22349fb17271f421f1bb9a2bfb942a3ccb620fa`  
		Last Modified: Sat, 07 Jun 2025 04:19:28 GMT  
		Size: 59.4 MB (59418248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee977eeaee84f3bd93eacdf121c4629a716a6da6076f25d0f5ca3ab0b3f7dcab`  
		Last Modified: Sat, 07 Jun 2025 04:19:30 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json
