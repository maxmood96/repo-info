## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:5a625fb6e0fc52fa035bad3c7440b9343b1b16a3584e1806d598ff3be732d092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:e4955227787fd2b5f3b929bcab486d9eeb9a4d22e8efbd970d7741691ceb97ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157460105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53081cfdd3e9eb8edfe207684980b6a0dc468158d027969eda62a320559d8490`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:560290b12a23bee21f016f412c7d2d38e17958b21b24d4d0f24dd2886e6b11ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151610491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2d8d0bb52bd82301c1646050a8510ff088205d61cfc118059492d325f973f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
