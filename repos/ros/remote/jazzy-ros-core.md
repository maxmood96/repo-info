## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:994adbd9d087a08d4472b97d6fa8c8d1f43d7be311a001edb28c6af074ab13d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:7a07bdf8b1f3b2a2d1a791197b5d371553eda417a25725a7d939dd0566dbd023
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163523823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855cd85836a135337dcb0e1b11df58d6663bd74da5fc0a6d44b44de186fa375`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Apr 2024 00:02:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:02:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 21:29:48 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-testing-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 30 Apr 2024 21:29:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-testing-archive-keyring.gpg ] http://packages.ros.org/ros2-testing/ubuntu noble main" > /etc/apt/sources.list.d/ros2-testing.list
# Tue, 30 Apr 2024 21:29:49 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:29:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:29:49 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 23:22:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 23:22:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 30 Apr 2024 23:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 23:22:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8f5159575f7bbbce11277d1532c12d73076587ebb492562917370449a8c5e7fa`  
		Last Modified: Wed, 24 Apr 2024 17:16:59 GMT  
		Size: 29.7 MB (29702068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d685d4b1835697d792719b9d32a49e6f2ff490bf4864a1e921e19bdcf9b574`  
		Last Modified: Fri, 26 Apr 2024 00:16:06 GMT  
		Size: 680.6 KB (680624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4876135551aef0e8eb1671e4e34d581297f7255ba571e4bd11321bc6ebbb4ca0`  
		Last Modified: Fri, 26 Apr 2024 00:16:05 GMT  
		Size: 4.6 MB (4615573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89fe2ec06dadb4203f1134cd0a4db95d383b2e3b74ceea6eaf13f446ba3a192`  
		Last Modified: Tue, 30 Apr 2024 23:28:19 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e0049a6452236b3d343a2c4ef39d5d4f3a10cf8c9cd905f102b537099ae33c`  
		Last Modified: Tue, 30 Apr 2024 23:28:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde9645b516e92c3c078f25655fb83a2e7ef751c8ea0232a2380ca19a26b5a48`  
		Last Modified: Tue, 30 Apr 2024 23:28:38 GMT  
		Size: 128.5 MB (128523063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58aabe751358c1e8c5d6c30492977cdbe557ac66da8b9c123ba6bfd2d49c5e3`  
		Last Modified: Tue, 30 Apr 2024 23:28:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
