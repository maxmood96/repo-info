## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:4e654b1839d79e613d0a393fc49c5bdb01a0a7aa8dac5517804ee57a4815ebb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:7d6ca3817633bb47b79586aa8e706ddb7f042871e5942b2704b701eaa42c1e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216275831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eba44f69107ee478fe9cdcdcf61af311b30cd2e2238cd7bcfdd450f467d08cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7281aa604e720b5eaf7e72404849690d72fa5effb15608d2a303b3882f13c9dc`  
		Last Modified: Mon, 10 Mar 2025 18:14:14 GMT  
		Size: 1.2 MB (1191587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a18ba426e6ea26c8fd790e38fecd6025373c25669dd4315eeb94f7ed6599d`  
		Last Modified: Mon, 10 Mar 2025 18:14:14 GMT  
		Size: 5.4 MB (5361910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e537c3c3ddc4adb3cc0de8338089b7d98cf338a1a97a138514e61d335c0a0ddf`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493688bad29a80f481679ba66e7b0d6fcb8fd23852d6436d0d44395070278bf5`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23863567396658bbea590c4eba5622c43ca5757b6235b1c39638f702d1783627`  
		Last Modified: Mon, 10 Mar 2025 18:14:20 GMT  
		Size: 182.2 MB (182208805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab278496cd9deb6d829558f60bad9417912d96a69106575b781f28c587248b6`  
		Last Modified: Mon, 10 Mar 2025 18:14:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1cee193e3cf55a547b51bf7b9cd93b5cda6cc68af4c78689dfe8dcfff3d3007e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6679ee1502c9df3be8dad2bdc9989cc8c76d1c92ef7058373ad233d522ff006d`

```dockerfile
```

-	Layers:
	-	`sha256:ed70aa069ce6da22da1f2b5c384617667bb87a6ecf8b9a3a9f328507e25c6114`  
		Last Modified: Mon, 10 Mar 2025 18:14:15 GMT  
		Size: 26.1 MB (26125935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fbde5065217803f7c41c39a3e63e07859f8027fb2b78dd749b165ccee46493`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 16.4 KB (16376 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:67dd1583c8a38e517b3953bab5bd4ae4a131d8a7b759eecb1d0019627e97e3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191225876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dfeb0e7c29ad80d58da20b821ad53923a89344a32967371c19e30c4be88f4d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63403fc54a5c95851d7b7b8c40144a5f9a318cee65813dfc14eefc11288ef1ac`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 1.2 MB (1191602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7a32017f42f62156bbd13034c1e560d3c291b3c7d26b31a2a57871131c347`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 4.5 MB (4487460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eb69a80d32b5cdb468886f797acdf344eee06f2f9f6510e9d48a41316f3fd0`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d74eccd6b688697b2abb8ed4135c32d6faf5a9c10eeb053f449ad68fa905c`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254f2e42a794615ac4855d623b55a398152062f1f9e286f1c15fe9c7042b870`  
		Last Modified: Mon, 10 Mar 2025 18:22:03 GMT  
		Size: 161.9 MB (161923934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac45b8cd6234ec64252da29a03ffda622d8cb517602f6f5af6d4956033de55d`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:063537f27200090830b26f444de82ce21f42d3ff7e4f8c1b8a1f318ed3682923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26055405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362c61cfa73d7232b534164bb603ae5fb41313922a61b5f964885d6ce69638e0`

```dockerfile
```

-	Layers:
	-	`sha256:05e6a6902d0f9a30c5f7c9fa2748ffa839bbe323e1f074da0349f1e8c8df08d5`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 26.0 MB (26038916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62411d0dbf00af3dd535c69dcba9dd0eded57daff34b54aa9a6e95e6cc0125ab`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 16.5 KB (16489 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8f4841dced005577d18cd81b26f1fcc8a02132b497876e3aa89e53e21cc34ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208220339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d426ded96d38709672df6adcda90679455d55634253e5d4fb53da2054cb59c4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2121f1f68d1125f94e05d5d5f8eb016a4d81ece6993d4e7c57bfe5ad26044844`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 1.2 MB (1191456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88b5cd2df85b5bf6fb6fb1ce3368e75445a74bb65bca8e0b7c862ee326d6a7`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 5.3 MB (5342153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc415fb12ec5c88f126a927064c087cfe92feb936886efa41626024d640a7ce1`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c2b989b81c9cede611618c4b68d5118f857fe6d7eb371449bfe5467122384a`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4605f7e1eea47d341d92031419819b83d0405500f6bf1c118e732be197d7e9a`  
		Last Modified: Mon, 10 Mar 2025 18:29:24 GMT  
		Size: 175.7 MB (175710430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca092e0891945ffc24a56747a902585fab1a46bf29aa20e37747360dead81d5`  
		Last Modified: Mon, 10 Mar 2025 18:29:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:75cde1ea8a736c0b29eb43e3e31d960a4963e35585d045a23a34443b06706b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d9076878575223ebd5faad124520b2761a94459fb98822734c28f591827f7d`

```dockerfile
```

-	Layers:
	-	`sha256:f6f7ebe863d8066db648f08ba919f1c3db871a36b1a5608ec0a7cb2a902095ae`  
		Last Modified: Mon, 10 Mar 2025 18:29:18 GMT  
		Size: 26.0 MB (26047668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23866d8db4dff5fe835c471621039286a99ed5f4bb75312ec0d70bf47b0a7b92`  
		Last Modified: Mon, 10 Mar 2025 18:29:16 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json
