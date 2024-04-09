## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:a33b5a2d4f0e06889af9104c6d2081a263e9fcb5f3ddd3539fa3813c79a39d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:9c6b1fd4cabc26028f9811becf9f7b86b28d7931e608255c641924c03c437c38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312928587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5199814c9885888b1775a73f195eba82bef47b7614e259ac984a51aec689b66f`
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
# Tue, 09 Apr 2024 01:14:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 01:14:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 09 Apr 2024 01:14:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 09 Apr 2024 01:15:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:16c8b87d727c91d29d462f1d74e4e23730ed1e3872ca84233a3ec6efd65828c3`  
		Last Modified: Tue, 09 Apr 2024 01:17:02 GMT  
		Size: 117.4 MB (117367025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2426d5cb0ec58cdd1563cc31ae0384c0193eb0441fd191af5a8cf5d926ef5525`  
		Last Modified: Tue, 09 Apr 2024 01:16:46 GMT  
		Size: 307.1 KB (307129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bb9995b3dd22894ce26995fe8c90d1fa9543fdf86f52f5e3615cf75aa9c1df`  
		Last Modified: Tue, 09 Apr 2024 01:16:46 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4ce9e86e8153669fcc14faa5b354a9c87f54c0272ea9d3421125a09ba7581b`  
		Last Modified: Tue, 09 Apr 2024 01:16:50 GMT  
		Size: 24.4 MB (24443916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
