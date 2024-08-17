## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:748d74758a37dce3dcc358fcb028b22a064813e0a8126933a97fa12b62797d4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:273279b99b53fa62526f367def6c25b5c7206ab2e337ceea2fb5132980f385cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140907965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea466fb89f40dfce2ed6aeb308749108a15dc6e631de20851f4557d7073c024`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:15b39854f1b5bec9ba3674052584294e8f3e56a0c0030eb53c18f3eaa8020088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16971353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b0796a1b5b7ac78a492f5feed9c5df97eb3a67431999e5c9aea8de44eba569`

```dockerfile
```

-	Layers:
	-	`sha256:0400f298396fd054345c54aa82f03ad8ed574daf5f8550407d3a6817eb1f69f8`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 17.0 MB (16955216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddf2898e14d341110cf49b9c77015ec91699f87226db7a03aaea7ead097ec7c`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bb304aa559114f8d6ef3bb3ef5fe8f4bc7821f33aa35a0cafe13599b732add44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136438911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a208dd7ba1f41e681f280585eb5612d8760911591cb2a24bf9249930e3ed75`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c92e67449590912b6c7755a150613269346b5015b668c99f2db49450f6a8e8`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 1.2 MB (1215007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2693553852f919b16b21546e1d8543a7ad744597e5f6749446017c3790d7277`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 3.6 MB (3595960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9fe7ebd0a06ee011e10d604fd769d9ff4552a42b94b0887d4e53098983bf75`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074b02edbde483a99adecce394a1c8fe6ec4582c39bad3ac5050bd5c6a5466b`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52f3878065eb3ee88c776c4daebe7310fe219adc004d71d843d7ae13921f44b`  
		Last Modified: Sat, 17 Aug 2024 03:57:12 GMT  
		Size: 104.3 MB (104266794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd9444ec78d82b8472db5e98823f37ae6d6f2c2f73640f40d3764e0b2813ae`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:d1223f4ddf4451faa4c5c5462dff7604c1d37c2d30970e35e3f025d94d9dcc8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16958359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3077d0cf67afb7c0b8a112876cc626c8af516835c2867a2761d69a76d60e2c7`

```dockerfile
```

-	Layers:
	-	`sha256:b776e091b066de05a97da896ef568e455fe9d644cc7e98ca0ce17129c1698d27`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 16.9 MB (16941945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c395d30d3b958b8c96887624c748be7b794a266815d6661b27a28169a321a6`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
