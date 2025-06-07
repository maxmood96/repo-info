## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:2e327ff9f721f0706009a659f3f6e686e0997243a991ef21d402e02d784fdd9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1fadc26291840a5231ddb8c2577c956354131cd3886b57c6da37ca270bff209d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158734121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e77d82cf7839837ba1c6f8205f87da2120124fd5645c409fa327708690dc0e2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
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

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:a82311107581382e388364acdc953b16f6fc942589472f6c1c1370d75e471407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19749573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28db133c5efea4f0eec1c51efdd2ad36d1eeed9692d0595874784bc298e24336`

```dockerfile
```

-	Layers:
	-	`sha256:090e7d756d7b819b1052b5434e64f19d699083029e3a11ee6169e9c9990ae04e`  
		Last Modified: Sat, 07 Jun 2025 01:20:54 GMT  
		Size: 19.7 MB (19733170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d753b77767c5e9aefe7661c163663be1899ecff5d4a70bfbeb2ec14d66ffb7e`  
		Last Modified: Sat, 07 Jun 2025 01:20:55 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:380bec6888479c8ee3c53307faf55241e79f5f3f1d39797d78d63e7e0885cf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153987892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4258755f4fb94c2ca26e81dac9d4224c588152e138782867328175bf709bf486`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
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

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:0146b6e5b480425858823b49da25fa04642a538aadfdcf47672d5b7b16ac0692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19742300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da72ace61bbd9085495bc0286722633d3c2b52f792b71ad92fa88f2abac8260`

```dockerfile
```

-	Layers:
	-	`sha256:8d8f6a5a903008f980184a57863d01d908486d49eb24f7360991e788d160993e`  
		Last Modified: Sat, 07 Jun 2025 01:21:09 GMT  
		Size: 19.7 MB (19725755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb111978e35d306c2c7508736322d1876dceec47861a84ac29dde2043c6ab37`  
		Last Modified: Sat, 07 Jun 2025 01:21:10 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json
