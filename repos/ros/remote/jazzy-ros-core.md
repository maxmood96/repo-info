## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:fb6f39dd0a9dee031e7a41dab6c7e2acc72cce622d1270d931ff772fc9bf8943
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e2210a4a3331cf5ca965ba303ee6013ebd21dffed65d94d3d5850a1c6715ef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156406651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a20bffe6e20a2386465358485d7190ebbe0dd6c2bfd6239182da0249b396f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08803d401c081fc3d12416d99b187a634698db36a10df80f4cef29170ef83e5b`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 681.8 KB (681844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f68a5436d21a97e82cf7e242efe03dde4f5b729ed2dbaf097fa8087d993f1c`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 3.6 MB (3558040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36adc7815cbb0b60279e15f0898d1f5d3880e45c336e2d37b6e55f3c19a7d41`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd0181ad8621c2a9206894fa0ac8823b0e7b0c1e07f8700418d53b93a2fa76`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b76af7af5fdf91bcc77e8167917c7c9febf10158f328daafe713d29813881e`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 122.5 MB (122459142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ae2ca4e9abcb78cdac5210d4cbcc57bb261e4fd8cca1695e8606c8e4193be`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:9c8fd8442f082ce2292b4081373891e19bf177069044539319c52955b8c80b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17709145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478bc18e7fb696948cffd284c5a971c603debc121132e3845f43ac7aaa1ad6fc`

```dockerfile
```

-	Layers:
	-	`sha256:57de735ba8354022e87468ff71de5bed30883a305227c776817e4d0dda0885ac`  
		Last Modified: Fri, 05 Jul 2024 19:57:31 GMT  
		Size: 17.7 MB (17693028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5cb0a359f2ece50fa7fca665005192834964183e863a8a9506ffe63fe40e2f`  
		Last Modified: Fri, 05 Jul 2024 19:57:30 GMT  
		Size: 16.1 KB (16117 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c3168eacba547192d800351b9edc64604d881376b386bed03d0c134b099379a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151613896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345f08d42b19afe6542ccf950058268a4a8e3d1908ff5dd01d0bb2cbb4af86b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 23:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:45:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:45:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:45:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04cb07560bbb610920c0e1636256cc57e8b24b2f1ef7a43aa366679dbc9ec60`  
		Last Modified: Mon, 17 Jun 2024 23:56:47 GMT  
		Size: 117.3 MB (117265666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb97f6a7fef0b1a3c83e726667929f588cdbe927fd37bae919ef56e96e274b`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
