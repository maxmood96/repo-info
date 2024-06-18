## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:bd8204a95f1d46b9ee7c78f77ba5d34d6921b50c02bae31f374468d74f097f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:f6721cc9d725c0e77ce6bcbed204c83f50febe75c524a926e83b4582fd6b74b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623670793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522872f7ab271415a58b3cc68eb554b3f58b0a58b619883bf4d5675fe1c6777c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 22:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:53:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:53:04 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 22:53:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 22:53:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 22:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:58:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb560ba80e4159bbd7ecd0b2b087742543cda4c6a38d6e11962899cf93f2a99`  
		Last Modified: Mon, 17 Jun 2024 23:03:06 GMT  
		Size: 122.4 MB (122449281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f73baf8579b4bee759b3d8255736d35aaea708c7807937e9fa93672b74912`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fffed5895f069623e78dd312f447401d9427c7955cbf44a7a5d6e9d1f793b`  
		Last Modified: Mon, 17 Jun 2024 23:03:30 GMT  
		Size: 114.3 MB (114314047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff86107534e43b482d4ed6f953a16a76dea0fd2355e45153fc52cd185d78ce7`  
		Last Modified: Mon, 17 Jun 2024 23:03:16 GMT  
		Size: 314.5 KB (314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c28d23077d3ae521447fc0ce44530ee13e13395ef0de730f3ee6263b7df0be`  
		Last Modified: Mon, 17 Jun 2024 23:03:15 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e7b1ff4609540214de8a236a1a608ef17ca2d2913bb57f6ee161c6355f305`  
		Last Modified: Mon, 17 Jun 2024 23:03:20 GMT  
		Size: 27.7 MB (27666753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf7e67c8b7c76d5cad0865b1d9b6f8c530dbaf74aebba9d2663f114a691c579`  
		Last Modified: Mon, 17 Jun 2024 23:04:26 GMT  
		Size: 323.9 MB (323917543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e8c78bc53cc58bb80ff9524a2c18a1724020b7c63852fa3a916c1630865c3b6a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.0 MB (566971316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf7db3d282f096ee145c24ad99ccc3b4a681782e3b8f94b025abaafabfb3533`
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
# Mon, 17 Jun 2024 23:46:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:46:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:46:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c227546804467a35149673a9940ef7ba3bec2ca50b237ac3a8dbfbe65a346f93`  
		Last Modified: Mon, 17 Jun 2024 23:57:07 GMT  
		Size: 111.2 MB (111158516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a75a7a4fb720def18c709bff7759e8ec90103efc11974be93b35b4d8bb60e09`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 314.5 KB (314458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeb39b65c9c71daa91633b54cbad6d09c4e4e2a88323868569c0ccd15ceacc3`  
		Last Modified: Mon, 17 Jun 2024 23:56:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f222721a53e6bd52638b546ab83ac3dfe065f3d27213fa0b81c0dcc98ad81`  
		Last Modified: Mon, 17 Jun 2024 23:56:58 GMT  
		Size: 26.8 MB (26813598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff20b0ef4daf156e82f37126f5a0d485f125ea3d17d4a0201496e97d8132224b`  
		Last Modified: Mon, 17 Jun 2024 23:57:48 GMT  
		Size: 277.1 MB (277068389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
