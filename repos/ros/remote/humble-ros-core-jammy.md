## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:22cd499dba0929c34121be8cc1ad1a5dd882dec6a73c789563c7e057d696fb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:04b7706431613a9f96f52722afea5ddb5b8cc7cfca21f7788ea2f64113106c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141989176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9e9ea97bbfd2afb0ef16979f5e610bbe87d9bcbf6a4e336a1665bf9020f079`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:55:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:55:32 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:55:32 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:55:32 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 05:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:57:09 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 05:57:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:57:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41440ed90fd838dddf218e12140cca3a662a2a72c9f6a447e1f538b087ee8699`  
		Last Modified: Tue, 16 Apr 2024 06:26:21 GMT  
		Size: 1.2 MB (1214634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c4c92ddfbf72bb3dd101dc3923584896fbcc7474879653b5221be859ce36d1`  
		Last Modified: Tue, 16 Apr 2024 06:26:20 GMT  
		Size: 3.8 MB (3829620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995bbbd01b94164626977be8da9c7b01cd25f4b0d1395714d6522a8f36ee1437`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0f8febe71fce8d47d4275e7a529033851f9d558df32723ea0c10693217279f`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6de90dedd39cf0b1730535cdf7031e84e6565036b333da15a71191096357c5`  
		Last Modified: Tue, 16 Apr 2024 06:26:35 GMT  
		Size: 106.5 MB (106502657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0594dc2886ddcc3b3c9798bb0f9ab9c9edd30fffa4356e49afeefe2bedfd112b`  
		Last Modified: Tue, 16 Apr 2024 06:26:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:94ee9c8f3470277b6263b9a1e92b7f77687362e1088dbc96a9cfa8671ce6c85a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137642939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04fcf1a72be6f817692bdb3deafea66dc10f0ad09fcb5f8b7dbe6833a66289b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:10:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:10:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 04:10:13 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 04:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 04:10:14 GMT
ENV ROS_DISTRO=humble
# Tue, 16 Apr 2024 04:11:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:11:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 04:11:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 04:11:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82788a1d68c5d56e22bb25bfde08263036f5ff28a5320a18f097be730a23d02b`  
		Last Modified: Tue, 16 Apr 2024 04:29:45 GMT  
		Size: 1.2 MB (1215385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8dbd081fd82bf72d7d4ae2163ce5e86ea0da721667ed7466a5a0718b0e1c0f8`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 3.8 MB (3801728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6dc8444bb1c99b3ea457dd564610b65f5175770f4687a59d8ce95549ac2ce3`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafe31a9057527718d465144dcca2f57344d738a184a59b7ab93bf0fc740fec0`  
		Last Modified: Tue, 16 Apr 2024 04:29:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a46a8cbf231b891ffb86a4c10d0d5f72574c257f9bca66ce7b3a2e082025058`  
		Last Modified: Tue, 16 Apr 2024 04:29:57 GMT  
		Size: 104.2 MB (104223043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd8f310b2ac7d9e59f07486977e7918635f2a4182a4334fe6f9268b9cb43853`  
		Last Modified: Tue, 16 Apr 2024 04:29:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
