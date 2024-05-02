## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:c00b3b07efee3e56755b1864033bf26959dc63c026d40593bde4b72636b19e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:800debf9ceb3e118aed6d8aba3801cbef9d8dabcc365626ced58208059d23111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157418551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb66abbea53e0c4818814c10912c24d3f2904f1640ca21b18a31d7b7a4381019`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:58 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-testing-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:08:59 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-testing-archive-keyring.gpg ] http://packages.ros.org/ros2-testing/ubuntu noble main" > /etc/apt/sources.list.d/ros2-testing.list
# Thu, 02 May 2024 04:08:59 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:08:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:08:59 GMT
ENV ROS_DISTRO=jazzy
# Thu, 02 May 2024 04:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:10:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:10:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:10:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f222a4f0f0d169710bf5be1624344cef1bc1c8b5d4e9ba80a78da2f7d7512e3`  
		Last Modified: Thu, 02 May 2024 04:27:56 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892340976301cbeedb196f219d6d5d61e94afd0cedef6b4ac759a17a79cc2cbf`  
		Last Modified: Thu, 02 May 2024 04:27:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df8a6e27e79b2f137d619d477df5cc91bbfd654469743995198ed0a7e601164`  
		Last Modified: Thu, 02 May 2024 04:28:14 GMT  
		Size: 122.4 MB (122412498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0a77993a63310ae001b3fc1bff701bbc23f008a2925d9d275cf18fb4521dab`  
		Last Modified: Thu, 02 May 2024 04:27:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:95eb8627f16d2149a4525b8bc4b911dc89f744237aaab52e7b762eecded7d760
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151561394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6386b0fe348479ebb979313bc045e77679071e62253acf0ff17d5ef0e9879f8a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:43 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-testing-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:11:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-testing-archive-keyring.gpg ] http://packages.ros.org/ros2-testing/ubuntu noble main" > /etc/apt/sources.list.d/ros2-testing.list
# Thu, 02 May 2024 02:11:44 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:11:44 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:11:44 GMT
ENV ROS_DISTRO=jazzy
# Thu, 02 May 2024 02:13:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:13:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:13:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:13:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1530a98afb6ca6b735ba21a703b8ab482443c6984b4b5dd57136c4a1245e8f`  
		Last Modified: Thu, 02 May 2024 02:33:08 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b38a3ce2b2fd6079fcf853bc1533d0de85fbcf48949e9b3ee31f9b40f03e59`  
		Last Modified: Thu, 02 May 2024 02:33:08 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82b0c960739bc7a727ac975dffda488d4ba93e271c18d3600c4be19c237167`  
		Last Modified: Thu, 02 May 2024 02:33:32 GMT  
		Size: 117.2 MB (117224625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cff6639496fa69ef9e6bfd477bcec2737b680972d8f76ea9d277e11eb8f1b48`  
		Last Modified: Thu, 02 May 2024 02:33:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
