## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:8a006d4d89be304403bbc7dd6c5c9b16403b8cde50964225e3d3f5a37ee79908
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:99262b7183a0267139ee026c57a20e05004bfe4c9d063638b94f4a13b35d0d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156678973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734f1eecb8b1d8a7bc6b91f3843369db390efaa4284882b4ca30b8585ae8dc68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3b2484efd73305009117d35bdc14769dac7cc55a59591b622561a50646fbc`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 683.9 KB (683912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9ee196cfb19dc0d61a08117b1827bc75c1072281719ccd336f9acb1b3c93cd`  
		Last Modified: Wed, 08 Jan 2025 00:00:33 GMT  
		Size: 3.6 MB (3560517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d977c02a44f1802debe1eee8710a41198847b4c0d9e6ea5c4a9e893d37a19c8`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2dc8ecf92fab78948452397647f0e17ff6de87b314612dd9030f699ce17b85`  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a665f5b789f6618a5b5333bfaeced39dfa1da05d2fc4bcbe994b40c0050630`  
		Last Modified: Sat, 16 Nov 2024 02:57:59 GMT  
		Size: 122.7 MB (122680298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f731aa396c65b6542509fea891d58ddab177bae76da2dbcb1dbeecf8be19de`  
		Last Modified: Sat, 16 Nov 2024 02:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:dfd3b5fd109a806bf23fa27a79aa8347acd69827d577bdf1c36ba34d0884c897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17875855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58aef9d2d258d9652a1a3d912af9139021e27b8a685034f83c7f49cc4c6f2169`

```dockerfile
```

-	Layers:
	-	`sha256:1f68cc4f22e45263bb78acc27e97b6ccc6d50b74d74bde040811bc2ac24f4d7f`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 17.9 MB (17859461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6a9cadf7b6646045c8109a867f9c4a5162ab9d59dd1e6fc3215d9c02a6931e`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:56a6663275e5466757d04c3e5e6881aab83e4532dfbacfa6cdd9c7cecfb8f6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150653909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240db244be99789efe89ef52a573948c9a60a4b05050c3e5b443f15258ebb83`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81328307e6050d58a3786b0d8d4e0e280336fcbe5e12ed33eafac0e62f39b3c6`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 684.0 KB (683965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dc71d0f9b404e0afdeede800f6310ebab3be587e6a707bfd42f238d09438d`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336756432be3b9f7f44dd7afbc515faeb978872819b168b6908d418b86736edb`  
		Last Modified: Sat, 16 Nov 2024 03:42:13 GMT  
		Size: 117.5 MB (117515664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870e1f30b2d734ef09cf0ddbc60a50570d5c677f7f244597cd0092ccc28a9734`  
		Last Modified: Sat, 16 Nov 2024 03:42:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:2277d4ea94561d842f9958d3e158a46915f2401b15c4546d8a43c62ee6a76c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17849966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4745e4e2ac8b6e86c5cd306d312975d36ad5b932d44425315ce1b16b038a53a`

```dockerfile
```

-	Layers:
	-	`sha256:b257b561c9b6a4474bf9536cf9ad42046609a37eb4cc7431138f1bc0bfcb27bc`  
		Last Modified: Sat, 16 Nov 2024 03:42:10 GMT  
		Size: 17.8 MB (17833432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a759b056535121e42fb5d64202aabe126f153b6e6e08618bbd8fd3ad42ad8f4c`  
		Last Modified: Sat, 16 Nov 2024 03:42:09 GMT  
		Size: 16.5 KB (16534 bytes)  
		MIME: application/vnd.in-toto+json
