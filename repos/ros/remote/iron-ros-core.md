## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:6de152a55ca314c3034e01f09a04152aba96728a7d885db4a73782ddc4f460f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:96ff941af5536d048e6bb17d70343dadd7c204cdfe78dc570f7381d5b207718a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159817781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea178dee662c9dd27ccd769a3565efe6f4cc411af5c6fa971a3d09072bd2b700`
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

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0aa49e1e3d9a8b41e0ccbd37a2e7b456fdea6fc86b498bbf18a7d914d3e157cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155207877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3ead61c5a6d83b4898b61bcfde734853af26f40352246084e8e861be74cb07`
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
