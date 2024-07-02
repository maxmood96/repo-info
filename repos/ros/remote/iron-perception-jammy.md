## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:57d5330559ed0df42fb0b093fc1901b60282f77a3caaffd9a197e3ab83f086c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:47df8429d108a81cb9156e4cfe4076c71b3e5824948654ed104d59c0a8727191
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.4 MB (961381346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719c5ab476d3208dd75305ef2361f4071967a6156d7bf4e08deb610da88ba6a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:22:21 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 06:23:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:23:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:23:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:23:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:23:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:24:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:24:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:26:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6035e0c20aa9a6a0e72cf291215a36408ff518e0b9da966329c30f8c9580a36`  
		Last Modified: Tue, 02 Jul 2024 06:29:47 GMT  
		Size: 124.3 MB (124331033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c982681289ab5fec9bc8ad601404cf9b8cf253486448949dd554ae96b169dc53`  
		Last Modified: Tue, 02 Jul 2024 06:29:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3dd9ed9a2217783c07c06264630b1d38f0f53924faa3d7be94edee1f46a5d2`  
		Last Modified: Tue, 02 Jul 2024 06:30:05 GMT  
		Size: 85.2 MB (85177019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6602c7f18082b5d3dad3c904b267f744d9b5549b8f4d1b0e6a4ef7711953cd`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 309.1 KB (309061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03594b9a6a50634d9d79b7783fc18c923e0da60100953a1d7c9e7b430e7f86f4`  
		Last Modified: Tue, 02 Jul 2024 06:29:55 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4948e4b0173081d9719e580a03997444c2a559883e955f0fbb92d2d3c5c5f5cc`  
		Last Modified: Tue, 02 Jul 2024 06:29:58 GMT  
		Size: 23.7 MB (23735580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af257a623f983e2e8d42742126bbf11bc7bbf9f8dcde0becc5e67315d8c78f09`  
		Last Modified: Tue, 02 Jul 2024 06:31:43 GMT  
		Size: 692.3 MB (692339448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7164a41db893aecc6fc0bba88604f7a07666bad9a15b29d417277fc3bad39e79
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.7 MB (921691478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e44a58f57c90284a6043f5c00d27b64a9e0cbdb65dfc653f39648ac6d10bbbe`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:50:55 GMT
ENV ROS_DISTRO=iron
# Tue, 02 Jul 2024 04:51:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:51:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:51:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:51:42 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:52:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:52:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:52:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:52:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:54:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30cdc1a9ff2f9ebf8213a700af558357b58ae913c7e61edcb1d27a280e6ad96`  
		Last Modified: Tue, 02 Jul 2024 04:57:16 GMT  
		Size: 121.8 MB (121787632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08fbb2991af2e722c40559a15cb594a3c45661508bc2b7949ea31be77da61b5`  
		Last Modified: Tue, 02 Jul 2024 04:57:01 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318e763e20b58a15dcf9b1149f8fd8e451417b06f70ea72ed5efd37d9c81bb5`  
		Last Modified: Tue, 02 Jul 2024 04:57:31 GMT  
		Size: 82.9 MB (82864796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2b526fed218337f0520e3445d0429a8fa8bfe0ac52b6a4b3f33185b01d52a7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 309.1 KB (309054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c90e04e32de4d9cc1872a0e6b6145c9249699644d747bff9a66798f07053ec7`  
		Last Modified: Tue, 02 Jul 2024 04:57:23 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293d50e1335efefa8a6cdb594118dd02584b001e0ce1e50c126cadd5d805544`  
		Last Modified: Tue, 02 Jul 2024 04:57:26 GMT  
		Size: 23.1 MB (23125986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ae3db0abb1c48789d6032454829c6b30955dce1bab1fb652d74a4395dbf6df`  
		Last Modified: Tue, 02 Jul 2024 04:58:43 GMT  
		Size: 660.2 MB (660181333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
