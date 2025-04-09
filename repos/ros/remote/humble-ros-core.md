## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:5ce697976d4fd5e209e3825f259c0739200806a2ae7b121d9987906b904e09cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c70abc7df27d282a393c3223f9f73a69fa8b5621aca238d7c53e9cbff0d203bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141020131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369ad11ee949de80e1372e3cffe6af698d8f3389145bc60aa8e912d4c76d5c55`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=humble
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e736ce0baf9d51b44d5ead6000c34fa440489dcf492ead6c6cb55b64a4fe1`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 1.2 MB (1213930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc958827a8b499b348349b560b1c2798dda767c94207d3a94a10a8b5842ea0e8`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 3.6 MB (3625591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0be3271a91fea9ec7a9ed9e2e17342524d3c263ee0e7c90f47539f41c2366eb`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127f0b2aa5a5573254ec6d3bfe78b8827d5fb8a246fbaa9c14eeb580e1706398`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59678e0c4abad5e5af5b3f2ee45704cd2fe32b25cc9397c4755eabd9a3ab70ff`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 106.6 MB (106645773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb2caa05f4f7b95a7e3ad2eed0de31749b03afe8f5d79634db56ae3941f8c6`  
		Last Modified: Wed, 09 Apr 2025 01:20:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:89173ee0f9c4d3581784ecab2746e1ca759e449535ddcf4d16224c571df6c954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17148109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec3eee04982c4e1ebeea2c756bd1ac846999547715b38008b7d40e2bb5d1a02`

```dockerfile
```

-	Layers:
	-	`sha256:8c9b2c9c0e5f161d016dae18c3e2b5cbf659b6f7b0b07b84f42c8b43a04c0d85`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 17.1 MB (17131718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc16592db763361b1548111e815c0274d7aed3c96b32c63b53b42b1ca6238a9`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3feb7c459f5991a1568c6a6d82cb336d0b9b25e5ec371f8da8fdabc3045aa579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136525481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773cd12d5e31f9469bc697d60320acd00efc798ddd0e9cd8441d0f02b6c1a7f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=humble
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dc6ed59947c90b653cb852244d8678f5c628a0287a08d61ac58f91cd15623e`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f378741874b2ef719a549823a1ad8ac08f65e893d7e78e8c44dd32aa56ac2`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163ae49ef6d582016a4496c4ac205ec01fba6474497e21655b3690b6264a05f`  
		Last Modified: Wed, 09 Apr 2025 09:11:19 GMT  
		Size: 104.4 MB (104357788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec322fe64af860101529ee59c11078c6c4bf13e33bb86cce625573f864fbaaa4`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:61b74c7be27d67ab3b5688f60aea9889d9d424d8892d91f49a6d1eb60311117f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17134888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78b68f5ef47a2e513977f761abfaf4f6f43460603d897607cbd5231ad869374`

```dockerfile
```

-	Layers:
	-	`sha256:87e9a14e64adc2dc579476cf17fe7f89ac718d8ec98a7154540d934aa334ec31`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 17.1 MB (17118357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75677f13111d09237b2b388d308f30590a4454c7792c27aeca0593645090a27c`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json
