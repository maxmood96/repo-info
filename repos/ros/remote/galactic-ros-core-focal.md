## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:a3717e650d2c1ebdc85166a3f64b49c2cf8338679babff36cae622c93c8a0d81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:f433ebe87c80db8d001b366688da325536a5603c1be2a766ef4284096bf1d78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143823215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c549bf02d5f5c532d835fb1b85a744a23e7c9521a9e773e2c84dcee30463e9e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=galactic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:ec5efeb461ee54afd417411274bbb1c6d2cbea7bc9c320292ede300b4a7f239e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17533939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42a6fa891c8a5d787a6d7e3a1036b59a5ab0424990380fcbac5a30381e76373`

```dockerfile
```

-	Layers:
	-	`sha256:43e8dbd1f7ca4668035f3b1a23afc26c35fd078140a0059545b779198d0362de`  
		Last Modified: Mon, 09 Jun 2025 22:18:01 GMT  
		Size: 17.5 MB (17517546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b651d5f72059331b9033f24be143c321b1d4c6802cca239bd5e27ea8ea7fab`  
		Last Modified: Mon, 09 Jun 2025 22:18:02 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:885ea35a786ad8da5e0b08b90a6f53e2c16f9a80efc98b1ed20ebfe03f20c3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137765884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02efb2bb05c593a26f2bc99066834cd024a1cee8d76363e5e2819173f907954`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=galactic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1b8ff4f1c4d1a398f009fcc9e62f2828af9312e7262ff309ea5e85a4df27bd1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17526365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa252d53c24c1b75b58763b52888a8995267f98cf7edfbaa5a981cc70a562dc1`

```dockerfile
```

-	Layers:
	-	`sha256:b1378a615dd898c97194716bf04077290c94cdf87e57caf705d7d03bba6fc6e8`  
		Last Modified: Mon, 09 Jun 2025 22:18:15 GMT  
		Size: 17.5 MB (17509838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8584669a13ff3781bbf6ad0f824ce8a47bc69402095019e601e69a12f347c89d`  
		Last Modified: Mon, 09 Jun 2025 22:18:16 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json
