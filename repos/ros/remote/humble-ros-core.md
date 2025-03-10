## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:a2612da764af45e1fb38fc028f3113b779e8507f5e556b0a143372923f3aa6bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:8dbe3a67254c3073c19943c5049e72be6db9154e56d322a97818020b2f4dd488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148433552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f616bd18c3e5d9a943349a67f47bf70317850a5a9dc38c9d4177109ba3523e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6a79aeb6571349bd0ed39d022974bd75ce6cd8a8fb16abc081979f49eb047c`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 1.2 MB (1208095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad511e33582dd506cff877292e878fa641e74fc75c6b05d646f02a8591ff6375`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 3.6 MB (3625056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cae3cbe2ca7852f81be5faded91257ec73279265656d13ab374d2b575abf05`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea7840eaa99bd262f11e2fa84632a1f7ba2a6fba94652d5e4272e9a11794793`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad57cd4eadaac8aeec4e7509e5fd14d30569d2e25cdba0bb834a763bf11cb3`  
		Last Modified: Mon, 10 Mar 2025 18:13:47 GMT  
		Size: 114.1 MB (114061990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82474f94165ca84f75e2d760c63690d4ca308855187afbce52058b83f50ffa2`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:db7bc0a5d05320fbb4906b521b8d9da6e26e8eb6aa864fc48cf860f1a6258994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17133639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4098d7e3151baba9cdb29a6965d49a3f9d8f3caf7fb650fea5cae0f12c6be86f`

```dockerfile
```

-	Layers:
	-	`sha256:b0ed53ba8e4cb459558b31ead673e25933ad751cfc63ad29fa9236fda2c50e81`  
		Last Modified: Mon, 10 Mar 2025 18:13:44 GMT  
		Size: 17.1 MB (17117248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591723d676a96e3281e418b6f1804f8f194570ae0bf29867c2cf93f4ab2fac91`  
		Last Modified: Mon, 10 Mar 2025 18:13:43 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3521cba9eba15ea916dee2f02c692e5af52c10d84769e3f2bb09b1dfc919393f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142687189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726e828639952a77e9eeb490bbea44ded50b44ab8515b7dd1c9eee7e7fbe5663`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926f36c9b7b151d496c801225ee7599eb5a8b9b724136c3f5e16b117476669d`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 1.2 MB (1208081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6a4a0853d9c07e7a7b7e748902799150df963c6d6c838f9689a1221332395`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 3.6 MB (3596329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeeed08a57b27403fa9fe9538ce4160740d4ec04e65be4ed90fbb9ac2bb25df`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf01b92f5fca1f33ea542127260bc8758f57c788ac4d6d9346acea13a47675`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8e209955f92010bb513e324647114f2359e3b4f0c03936550a6734d9f53e4`  
		Last Modified: Mon, 10 Mar 2025 18:24:56 GMT  
		Size: 110.5 MB (110522121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804f4e59511abf9df55102f7c8e0af1ed796adc901b8d302319e1239f269c737`  
		Last Modified: Mon, 10 Mar 2025 18:24:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:75dab6f34142165c2a7014caff86c9e91268128f1a8cff14670df263d25d5009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17120417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18837126796282060c11cff971e9b55d4ab1752e170a9094309e9e1625b30cfc`

```dockerfile
```

-	Layers:
	-	`sha256:ad99b5798d1abcb03974d78123cc03c460035f9e49766fb20e37edbd521f91e1`  
		Last Modified: Mon, 10 Mar 2025 18:24:53 GMT  
		Size: 17.1 MB (17103887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cbdadda0486228f4ed192372863450ac40e7982f64e3c33baf07d2ef3053737`  
		Last Modified: Mon, 10 Mar 2025 18:24:52 GMT  
		Size: 16.5 KB (16530 bytes)  
		MIME: application/vnd.in-toto+json
