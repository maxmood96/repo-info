## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:33eea89feba24ddd6acc8a0f26a228fd51eaa04c5d613bce6484fecc5b9672d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:37f516c975da9fffccad5722f6e283091076d27f63010437e6f0cbb8eee17200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160228052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30612372da30bb99f75b419609fe802646aa0c6b3c25a9f1d2b26fcb589edb06`
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
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=foxy
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:e8b6b4a7ecb05df2f70ab245fb4765a692ab3b761124a164ce42de55eb13f37a`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 1.2 MB (1194822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59f0b1081586aa99c6e582b439fdfb45aeb6d84953aaf308502434be8c6447`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 10.0 MB (9982524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee8b17bb34ee6c86ac4cc65d1afcdaca935dc6a6384c82b6e9270fc80796b`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4503d1eb268818ccfcfa60cce616bf269d09462dcce6bc97cddb4fc6c4093cc`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac69b7953e35acff2c57bb856e9e8c7f5484f28093eedf764a04885357ec213`  
		Last Modified: Mon, 09 Jun 2025 21:16:54 GMT  
		Size: 121.5 MB (121535795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b370323b637277176e00ff105bfa5621b1c7d4e3364010bf52eed1af5165`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:44100099fc13cc41f70b6ff2c828c155e3bb89d383b4341abff110f0181eab49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18632545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7517231377f3fbbb87f63c190dfc900be4ae92534943f10764982f70f76b55c3`

```dockerfile
```

-	Layers:
	-	`sha256:8032981490f8386c19b5abcc208184607fb91b79b2389697077d2cec528884c9`  
		Last Modified: Mon, 09 Jun 2025 22:17:33 GMT  
		Size: 18.6 MB (18616208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df57fb4951aab045f23edddbb9744b4397d1e67401002cf31d4728ade173eac4`  
		Last Modified: Mon, 09 Jun 2025 22:17:34 GMT  
		Size: 16.3 KB (16337 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a2d2fce43c36a00a3294cf1b978359bb214dbab51c22ecfe80f5c9675373d4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141963914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3d1846b4748bca3a7b564a9a658dfd7f327e5bc3786e64d5fcadeabfd05998`
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
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=foxy
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b2e5e017a927cc328a3bf6d46e7f5f8e4b6f03e2b8db2154f657bec065e0cb14`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e065b47e25afcc4719d7aa531dcb8d893610e9d8ad388e835a367718fb4897`  
		Last Modified: Mon, 09 Jun 2025 21:22:04 GMT  
		Size: 104.9 MB (104947330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bdbb3b522ee491f0b6571d32bf6183362277741d82a1edc73e3f7da2b246bd`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ee25430c3aae4129e4938cce0430fa409ac2865c5338012f8d5f7e2351ee9d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17551000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4758539f92d20dd7c92558e8ef489f1cbc6396b9668115e3205b26b553931bdf`

```dockerfile
```

-	Layers:
	-	`sha256:48d93cb3474a3e8cf25c65db57daa9ebefb7c3bf0478e21a3b9f11b96811979c`  
		Last Modified: Mon, 09 Jun 2025 22:17:50 GMT  
		Size: 17.5 MB (17534530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c40244fc71a0636c56d3030197efb6142bee9053c6a4c4a5d57132ab7c06aff`  
		Last Modified: Mon, 09 Jun 2025 22:17:50 GMT  
		Size: 16.5 KB (16470 bytes)  
		MIME: application/vnd.in-toto+json
