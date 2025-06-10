## `ros:foxy`

```console
$ docker pull ros@sha256:34fbe32f5b1cd3eb25f6becaaa1d293bad754d64c31d96e638e4b30ed82f9f8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:078ac8eaffc953e97d4abf72f57da1fc33080b720b94bb1dc8c05ef4f7690367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255528741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d94b936914c0c299582ee509d62abd1fb86d1d181f68906a78efb53ed11289b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:641f030e7bffcccfe0747baba44f7af6dd25fe525476bc3dfec496f0ca25231b`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 73.3 MB (73324260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7992bd907c286578d31f6fa5849a571b36b7b96773c294e10ebd77f103066676`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 301.2 KB (301155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e5ea1274e6719ae30e2c531a96fc11563836e1b355051cc6fee6456b1298b`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05613765d2b16f984507a7bceb0e742e814e822c16413dfe5a9d3eb3d6964980`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 21.7 MB (21672813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy` - unknown; unknown

```console
$ docker pull ros@sha256:dff4a59ddac240692c3eb13999ffe63bf59de0633253cf39d524deba938f75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b062eff39362fc854810dd58ba695860b169d46056706f2335964691c40672af`

```dockerfile
```

-	Layers:
	-	`sha256:50b901735eac590f22326e84eeedcf570de2072b887afbb5b9f93c6356262111`  
		Last Modified: Mon, 09 Jun 2025 22:17:24 GMT  
		Size: 22.6 MB (22629617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6034fb143f7b17057c17af8739e99744162c20aa8da37a32f62337390f670e`  
		Last Modified: Mon, 09 Jun 2025 22:17:25 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7bc031f0f6603d9ee6a21ccc0d8f6b9204d7f2a9e1dcbf9181cc0926c0e30a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230341771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26bc4823a8f6a75600077ee19c659000952bef4c488a5b6db7101e7b6323a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:469ae630fae53c7ab2055ea3d53f0ca27a77a1a70f2d43f7b604ade498ac199e`  
		Last Modified: Mon, 09 Jun 2025 21:40:53 GMT  
		Size: 67.7 MB (67675196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3e71a66a3a86dc10acf882350a2523b1e91f63a713da6920a1adf47c46459`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 301.2 KB (301152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e371813eea9c4f185fb2f53a18e98ccd8a84e1d9b06ef38727a07f34059570`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34406e2c7125d268c606619fec209daac599aed8ff794912378c2ace9488cb29`  
		Last Modified: Mon, 09 Jun 2025 21:40:51 GMT  
		Size: 20.4 MB (20399031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy` - unknown; unknown

```console
$ docker pull ros@sha256:d05593fbff060b58c59d1df728ea63a1b03e7729c4d21b1a8c3e7fbc23d92ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21566581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d2f7828474d6746cda7d49b0902cc26f931dc40d6127bcda25228b1650ac9d`

```dockerfile
```

-	Layers:
	-	`sha256:ee199d34c0becab0fc7f739e2f62b133a62f4fb33480343a0375dc2a107cd353`  
		Last Modified: Mon, 09 Jun 2025 22:17:39 GMT  
		Size: 21.5 MB (21549325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5e0f353473f29a09dcf7cd9dda7d29044db2d358680183088ad9c6bef9fc31`  
		Last Modified: Mon, 09 Jun 2025 22:17:40 GMT  
		Size: 17.3 KB (17256 bytes)  
		MIME: application/vnd.in-toto+json
