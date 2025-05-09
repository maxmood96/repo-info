## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:4629fd3705b39eef374f61ad6a03a2e07f3a441dfa118190dd959ff7472a112e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:3680a8c37b6bd620e83cf381fffb6a3af37b71de07f8bc9c27f57e3520ec3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb58800db018755c21761630a3d30004494508fa53579e52b2d1bc6317666cb6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db6612a791b94a9bf8fabae0aa79d724aeeb933eee71621a8b97650e5c989b7`  
		Last Modified: Thu, 08 May 2025 17:06:19 GMT  
		Size: 683.7 KB (683654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3983963a90e8fa68690e05966e629ff5a9883d85bcc023046d90d9f68d636`  
		Last Modified: Thu, 08 May 2025 17:06:20 GMT  
		Size: 3.6 MB (3563319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5443d20d5093c36fbdb72dc61460392cbdb629c68c4519b2075ff007364a8d3a`  
		Last Modified: Thu, 08 May 2025 17:06:18 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c5e46a5a33f034e5d6b276d25aad71c24e71feea8742bb4a9fb4c07acd7c22`  
		Last Modified: Thu, 08 May 2025 17:06:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247a03c6dd3d195fd6087d50e6c4e22e336d3a02b38275631e3743c39976ec5e`  
		Last Modified: Thu, 08 May 2025 17:06:26 GMT  
		Size: 122.9 MB (122892142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941b252d0546e6b8fee519dd212cd7c65b9527f946aaa1d8fc88ee0a12559edf`  
		Last Modified: Thu, 08 May 2025 17:06:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b35756b3becb18b3d5e0922bc7eb94b64f201e22d590960a839e8627b12f69a`  
		Last Modified: Thu, 08 May 2025 17:06:30 GMT  
		Size: 110.2 MB (110177223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6b9c42df52260e9183d0c89206f299f225faff4ff1edbf8bd2136f389b2fab`  
		Last Modified: Thu, 08 May 2025 17:06:22 GMT  
		Size: 361.5 KB (361537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f63233f789f2324bf1fee9d3cfd0034a3c789c255907d458e1c414665a0c6e`  
		Last Modified: Thu, 08 May 2025 17:06:23 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5176cb754ce9815b27109d1731385a6e1aa0d57089bd464a1bbdb0d1eab40ea5`  
		Last Modified: Thu, 08 May 2025 17:06:27 GMT  
		Size: 28.0 MB (27965416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f797b9791de8aa22f549fa10385d2ef0545531fc257a87f773b58a52c635eba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23886818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b720475fb9d73e61503afe573b97a98fc7139fefb67a9de2096ac9bd499fe77`

```dockerfile
```

-	Layers:
	-	`sha256:3ad81d703b6312f4a5e620db5a6a8e0ddce7e731d5d0e0ae1af0f561f40e4960`  
		Last Modified: Fri, 09 May 2025 12:30:31 GMT  
		Size: 23.9 MB (23869389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a0a1c9be81f2607b25f3e8c7b5e143697ebd34f515e37c2f6b4b8bb4967be77`  
		Last Modified: Fri, 09 May 2025 12:30:21 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fea6b7990d42339628157a7dad7526fc33b6270a16c09f40b3e8cd8a2ccc3e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283791021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2dbf69df32cb8c5c8b58e6a5a564f0be08d57ae2c013632a48fd0373f6d82f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2e6d631663d69d931328844662622971edf603268f55d74da74b2f1832435b`  
		Last Modified: Thu, 08 May 2025 17:05:37 GMT  
		Size: 683.7 KB (683725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ec84cbb756b62af9e3d14e9f2de6ea3bab2ef3004d88f35527f5b06731e5de`  
		Last Modified: Thu, 08 May 2025 17:05:38 GMT  
		Size: 3.6 MB (3561582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3c6650198856d89ceb2205e3faf841383f08c4f761180ffb26aff4c61888cb`  
		Last Modified: Thu, 08 May 2025 17:05:39 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4f33a49a4d32aa02eb8d0ed177d6f1618ea6ed82efb0abb3c82978bf9b2487`  
		Last Modified: Thu, 08 May 2025 17:05:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617abecb85c9162d81ea2cbe7eaa782a047b0551dac5a24381cb2e1912668b3f`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 117.7 MB (117682404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ea95c5199fdd922b6236aaecfa05b1338a5a59763fa9e9010a537880b343fa`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84efb190ea734269f584722b4c3e925274a26fc4d994dfbf6a675c5d22b042f`  
		Last Modified: Thu, 08 May 2025 17:05:51 GMT  
		Size: 105.6 MB (105590547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b439b17ae91a0bc0b15f592db251970e2ed47183d073838ada4eb3a84b69d46`  
		Last Modified: Thu, 08 May 2025 17:05:44 GMT  
		Size: 362.6 KB (362627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ea01bc444e685647afde99a6b5113f6542d507ba8303a8eccc5fc8868addaf`  
		Last Modified: Thu, 08 May 2025 17:05:45 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280e9e947ac112eb5f4818eda534910a294d9a599b17a66242e9225b4af41f1`  
		Last Modified: Thu, 08 May 2025 17:05:50 GMT  
		Size: 27.1 MB (27058364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0b6ce68a791a7b2e5d255dc3008bc197bfc00444e32d8022e66608276f799657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23896342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de1f972a6de61e3acef2bf5e7585e308be1bde614f56394995ddefc24e1fb72`

```dockerfile
```

-	Layers:
	-	`sha256:ee1633b8c9b846059b4f44e4ad2ead726b65ef9d43bf19f8fb051ed5fed69b61`  
		Last Modified: Fri, 09 May 2025 12:30:30 GMT  
		Size: 23.9 MB (23878764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21968fc097dd3b43ff4aa8fa8ba4db324c865572590a93ab1125095a6c181090`  
		Last Modified: Fri, 09 May 2025 12:30:21 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json
