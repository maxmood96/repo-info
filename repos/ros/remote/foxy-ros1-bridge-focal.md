## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:b22bd431548c7f329c3c1f3c5417e40985b53f22e9857e22ff3e71d757967d18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:de1c8aaa89130f05dbd4975f80e27528a84f884063255e7644cecec05379eea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.7 MB (543656670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4ca8a63bf5f732fb7b394814b4cce3056f177c61a1804ef6bc342b530c23e`
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
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=foxy
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
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
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e64fda5bae5a61863a5e59d0a5ef77d7c2bbf4a438b47eab0aa40199f15b43`  
		Last Modified: Mon, 09 Jun 2025 21:45:20 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab802a4ff0e43df0a701f10b18cfda3603f618895a434c033d25e5075f46e78a`  
		Last Modified: Mon, 09 Jun 2025 21:45:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aae94330fcaff2780466afe5e118dab6e5e18206c0d3618361192644d1eb668`  
		Last Modified: Tue, 10 Jun 2025 04:38:50 GMT  
		Size: 266.6 MB (266595963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160682a67416d67f284ec74e1a471cb7b449f0dbef147bfe1ed59bd825fd0253`  
		Last Modified: Mon, 09 Jun 2025 21:45:23 GMT  
		Size: 21.5 MB (21527366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975b003866e73673e5446f5c6bca1a95bc533887b921162cb5ff7c860af12a6a`  
		Last Modified: Mon, 09 Jun 2025 21:45:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros1-bridge-focal` - unknown; unknown

```console
$ docker pull ros@sha256:20636e794adce8327f41e9d59d1fc6d898bd37113d984aa5d782aea6aaf10269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43488904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7eab8b0dbde855009ec783110e3fd6fabda983dc73bb2720dc7af75ba509aa`

```dockerfile
```

-	Layers:
	-	`sha256:dff2c0e077e3576987993bc5faefbf6fc717a8265849d6497af5ab6402556a79`  
		Last Modified: Mon, 09 Jun 2025 22:17:45 GMT  
		Size: 43.5 MB (43461018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30f2c7c41fffdee2dd1ab8ba1456386dcba889f8063953f2066b9e334e30e96`  
		Last Modified: Mon, 09 Jun 2025 22:17:46 GMT  
		Size: 27.9 KB (27886 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2a45cf74cfdf4f6968094b656f3af4a8f99dc8d5ea370bac948328de2663a84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.4 MB (508401122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728409448ce4ecc91e60a5f48c4d0d0800a1295a2d6e139316002fb37fc56923`
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
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=foxy
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
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
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68c10a7a245451454382c443b8762047c631763657f710726dd777a900cd03`  
		Last Modified: Mon, 09 Jun 2025 21:52:37 GMT  
		Size: 4.0 KB (4050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e03ce9014ab5e7ffb8c26d05d8a659767ce8534d5563a2d9fd0d876beec5cc`  
		Last Modified: Mon, 09 Jun 2025 21:52:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e954e2c82942236430969db994323bfbc2ea0235c053530747d99e6b03f779`  
		Last Modified: Tue, 10 Jun 2025 08:49:44 GMT  
		Size: 263.9 MB (263888200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f29a713482afc94946a4e6d95c626b06d87973e1fbf3bc2a998ba36611e75e`  
		Last Modified: Mon, 09 Jun 2025 21:52:39 GMT  
		Size: 14.2 MB (14166541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd5c3d11ef8ac05a7fda6f247518cc62232c4198e6e21ea18d7c61e7fede0e5`  
		Last Modified: Mon, 09 Jun 2025 21:52:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros1-bridge-focal` - unknown; unknown

```console
$ docker pull ros@sha256:88f3a3a1f798961f3f54082051b6374403eabf5f48acbf3b3206069974a604b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41830004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1be3b8bdf918c686b1fb0647c07de2f0a23a22285084a9acc058bcf98bfb19`

```dockerfile
```

-	Layers:
	-	`sha256:783aa4088a7e20c04b34201cdb39b15ade9dad13f08fd5067d44f3f2c2621418`  
		Last Modified: Mon, 09 Jun 2025 22:18:39 GMT  
		Size: 41.8 MB (41801979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723cdf002feaf93d7ec74e6c316c2bb9c31e999ee209d088ff4e275d19956d18`  
		Last Modified: Mon, 09 Jun 2025 22:18:40 GMT  
		Size: 28.0 KB (28025 bytes)  
		MIME: application/vnd.in-toto+json
