## `ros:rolling-perception`

```console
$ docker pull ros@sha256:4e75644f381fca4b6edcd727735fd05b7ba11bc76593ca86303fba81ce0ab7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:afcaba5fc6bbc0b70cbbf010d1ad402b3e1c8f47c3c0f95025800325cea2c330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961072350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9105f3bbb81b1d6bd844917d73239dffc41a2f909ef9ea291925faaa26a163`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:45:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:46:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:46:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:46:36 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:47:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:47:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:47:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:49:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e816e1b53b0a2cfbc020786fc9237866c475b7a1577a3434f22757184feae43a`  
		Last Modified: Fri, 16 Feb 2024 02:55:23 GMT  
		Size: 124.0 MB (124022764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a59c2ece161c660ab1f9845fa7a104a86e1c1ce4c693528dbb9a209ebd5064`  
		Last Modified: Fri, 16 Feb 2024 02:55:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb70b401ad3cdd5e5312f608fac50c4d08235c46b4bb7d5b96a4fa3d4adffaa`  
		Last Modified: Fri, 16 Feb 2024 02:55:42 GMT  
		Size: 85.2 MB (85172455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e59a5e57117836224d8592f79069f4396990f938472fd8908c99647acc8bed4`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 288.3 KB (288267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84db4ed4691b1b8a17e3f51101a41d420677093770a40c6ab13bcc7d8962b6bb`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90e53c82be9bb64a07e8642c11539216cae554aeb5583f73c05deb0adbeaec2`  
		Last Modified: Fri, 16 Feb 2024 02:55:35 GMT  
		Size: 23.7 MB (23733355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3714e19d249980578d5b43bb699436b994ae29b3fcb161b137fcb8912ce5cfd`  
		Last Modified: Fri, 16 Feb 2024 02:57:26 GMT  
		Size: 692.4 MB (692355164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3425cb2bd3781e71a4f11b345f519e86e88485cc80bc438b28edfc7c177271fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920205442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d5e51eabc47c950d24ff10f9720ccbb84abe6fc0715fd8965b86034ff9cc93`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:52:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:52:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:52:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:52:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Feb 2024 02:52:17 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:52:17 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 03:08:05 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Feb 2024 03:08:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 03:08:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Feb 2024 03:08:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 03:08:49 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 03:09:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 03:09:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 03:09:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Feb 2024 03:09:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 03:11:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5992f730822fa824cbf7d3f44bbe42d9e0a430ee802ff3b881740b95fe753e`  
		Last Modified: Fri, 02 Feb 2024 03:14:29 GMT  
		Size: 1.2 MB (1216340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa8ec77518d8d3ea5f4a848375f3a742074922bc1107a763144500d58322d2`  
		Last Modified: Fri, 02 Feb 2024 03:14:27 GMT  
		Size: 3.8 MB (3800535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1be5561e0e858afd3baefdb8b8ae673b68af4125f6bf3c705d953f6e46b12ac`  
		Last Modified: Fri, 02 Feb 2024 03:14:26 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f99a3fc10280d08753ebc4cf1abcaa38717a8225d899c28c136c8b0cce61e`  
		Last Modified: Fri, 02 Feb 2024 03:14:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99847aefa4407a67549b8e7ff113bfbd347e5cba557f52434fff0529caf26db9`  
		Last Modified: Fri, 02 Feb 2024 03:19:52 GMT  
		Size: 121.7 MB (121735353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7673a747a43ef9159955abaa2116daa70aa1034ec4ef0ab13e76f85e79d94263`  
		Last Modified: Fri, 02 Feb 2024 03:19:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9001ecab27e78e4a22ac9b45a5962dbd573dc5071d9bc4a36c47f8831dc9b6fc`  
		Last Modified: Fri, 02 Feb 2024 03:20:11 GMT  
		Size: 82.8 MB (82846700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9eff8a4b0d50f2269e62c69a836c34450821bc259b91686f8b7e13ad9ac3d0b`  
		Last Modified: Fri, 02 Feb 2024 03:20:02 GMT  
		Size: 304.7 KB (304696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743ab94f429be6af3a7ab5adb21859b67b11d37783c61e311b12192fe6c06062`  
		Last Modified: Fri, 02 Feb 2024 03:20:01 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d18c9c234a29d7794604a93fb0b5ccb926871b633c7ddac5c05f98a53fc634`  
		Last Modified: Fri, 02 Feb 2024 03:20:06 GMT  
		Size: 23.2 MB (23164433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139bb74ec8cbe58894692e488856b7bc3102dcfc3462631e78bc850dab28e2a2`  
		Last Modified: Fri, 02 Feb 2024 03:21:45 GMT  
		Size: 658.7 MB (658732310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
