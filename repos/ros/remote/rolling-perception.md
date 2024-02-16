## `ros:rolling-perception`

```console
$ docker pull ros@sha256:7f27d949206140004b0f3499027d13b9b9f61047aecab07bcfeba8fe8131597c
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
$ docker pull ros@sha256:cf9a5e2843e818d94b386fe0925982ad02a7120b9fd6bb44c8f80b2a40de4aff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 MB (921371813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acc19911fa655ae7768fddfc42b3aac88a27487f2c3604a395eac365ee3792`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:36:11 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 05:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:36:51 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:37:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:37:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:37:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f5ba27e09156f2abd707c31ae4b3c30fba1cb7cc093834e02213c76a491920`  
		Last Modified: Fri, 16 Feb 2024 05:44:56 GMT  
		Size: 121.5 MB (121514724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c354b27f981f31060a6bc28d16882869ff3cea5aa8f51e2f01aeb59d51cb2d4b`  
		Last Modified: Fri, 16 Feb 2024 05:44:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073be48ee18b888bdb5c24da37b988d2b052da8cf145531ab73fa0445128685a`  
		Last Modified: Fri, 16 Feb 2024 05:45:14 GMT  
		Size: 82.8 MB (82846557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5ba1697514e19d58532dd5504508d8b7064c817df9cc114872b71f2c7f090d`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 288.3 KB (288272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fe0b2c75f5a9d76b0e16f87ee5742545c5d13f47f45fd005ec0e3cf3523b1`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3820ab663dcc8467f214e63948aabc8674a0c40002cee43566e0d8a524aa92`  
		Last Modified: Fri, 16 Feb 2024 05:45:09 GMT  
		Size: 23.1 MB (23101747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ea8db1138bc712cf216edfa2f027f2de7b389cf5495fa5df7606b2ad1f630e`  
		Last Modified: Fri, 16 Feb 2024 05:46:31 GMT  
		Size: 660.2 MB (660198287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
