## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:05078e88013819c6d8a04415dc55cd630d5d481f093324cbbe8fa2b788950f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:3b69ec5144484dc74b25bc85236543e9e1fedc8491558a7fc283a27eed29e256
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170808009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302f159e7d317d553b7fd59e932a25a8fd7853acc7cd59a7c61c897546edcc82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 01:10:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 01:10:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 01:10:58 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 09 Apr 2024 01:10:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 09 Apr 2024 01:10:58 GMT
ENV LANG=C.UTF-8
# Tue, 09 Apr 2024 01:10:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 09 Apr 2024 01:10:58 GMT
ENV ROS_DISTRO=rolling
# Tue, 09 Apr 2024 01:12:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 01:13:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 09 Apr 2024 01:13:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 09 Apr 2024 01:13:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ae7a4b8533ed02de25c6db9cadf9d6185ec0c1449006f72c8c102f88d9c366`  
		Last Modified: Tue, 09 Apr 2024 01:16:20 GMT  
		Size: 678.8 KB (678804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f996e40de6f8f6916bb8e6980652668cc0d05d02c25eadb51093298574fcb`  
		Last Modified: Tue, 09 Apr 2024 01:16:19 GMT  
		Size: 8.6 MB (8592662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56c22f3aa219c5138ff1bbc82374315aa1922757308b29877c35a3cb8b5e6ea`  
		Last Modified: Tue, 09 Apr 2024 01:16:18 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eec9388bb59844a59497d2429ee5f3f2015200df4fa2c240bb17af7f0f71468`  
		Last Modified: Tue, 09 Apr 2024 01:16:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d655d21d1312116546a5f98c784090af77df702fe99fdfc6a1c9a35eba60e5de`  
		Last Modified: Tue, 09 Apr 2024 01:16:37 GMT  
		Size: 131.0 MB (130982386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78161d0fd69b73de8cf9ceaa94a41d12f84426830950ed264cb4c2f7305e2d29`  
		Last Modified: Tue, 09 Apr 2024 01:16:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
