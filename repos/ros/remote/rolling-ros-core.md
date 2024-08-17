## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:cd4d0bf9a5b81e2e69d111f74def72d5e557f9d39f3ce4b81cffefbc763dde24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:2bab17738a780636dcb86f1433549864332d860c4f0987d59fff48adaf42ca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156457664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debe6fc5c9f6cb22d262dcd9f4da2986e3b8be704562927dc3c67ea158b80338`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f73b267ee4afb2b78b98679d1b7855756112b475c822b5e650f21727d11e560d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17820095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d324cc0cabf32bab15d66468aa5b08b299a01ec3dec2d640552a06cc5a18efa`

```dockerfile
```

-	Layers:
	-	`sha256:e52a2fb7d8cfd575bf794db55a89040a81338f6a08eb02b8ef90888d3edf5907`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 17.8 MB (17803955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71dbb7d25636a8a0ff323ffe399e9bfef01fd3e939d2e8e82d5786e761f24ca5`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0503c3cb0cefff6bb65d10f79eb038b1b787536f9cba635c8f53b893e3b7ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150417831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129853cf267bd1d1d0acb529081fe3dcaa0790b1fe8c3e6d3e8ffc048621ea08`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a631a99905201093a192b96d6b9344a759bab04da8001fa7f2bd7df0eb20f436`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 682.9 KB (682877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2beccfb7f73210b53f07f3b786019cbd7b54faebe00e559e8511b67575df29`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 3.6 MB (3557897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fdcea445bfe641533a4e4eb218d30dd044e1fb979c59c9ffb8d6d41c654c4`  
		Last Modified: Sat, 17 Aug 2024 04:01:16 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a42c4dd663c96d6c786e46499dedfb50ea24fb2702a2108d9a94cb3aa990a`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9c04e2bffc1ed794fb172146ff902e16b2168278b07cf37fa39ebba8e09d`  
		Last Modified: Sat, 17 Aug 2024 04:02:49 GMT  
		Size: 117.3 MB (117330906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97270cb5d2135d6378730d2c10ca4fa7c82d05d3108eaef2bfec60d3b45662d`  
		Last Modified: Sat, 17 Aug 2024 04:02:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:91843b20dfe3b63d355b75840cd693f789183104021cf7378c6a03f9c7c93d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17794343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a913b197ad39612d1fcbf729c123a28b5124825a603684bb2137c57a6f628538`

```dockerfile
```

-	Layers:
	-	`sha256:bd093f7c86abf07bf98fa36b887986c9a16008d2bfec0c6c66c8338abb22cd40`  
		Last Modified: Sat, 17 Aug 2024 04:02:46 GMT  
		Size: 17.8 MB (17777926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2fce5d47d4778c24df9f1d404353d5418bc601672d94807d624899ae0f5ccbc`  
		Last Modified: Sat, 17 Aug 2024 04:02:45 GMT  
		Size: 16.4 KB (16417 bytes)  
		MIME: application/vnd.in-toto+json
