## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:f420cfcaa46dee6af211a90dd9de1f27c4eab44e71397f5796493371d9e6b5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:b4b7ea311b3c467b5c061080d29de4dc120488522eb96d47786065b31aa95ab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.7 MB (629738420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddd7d19427343547671b6edbe6eb3d299d9d37daa4da5117f17348eab16e40c`
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
# Tue, 30 Apr 2024 23:24:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 23:24:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 30 Apr 2024 23:24:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 30 Apr 2024 23:25:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 23:27:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:98d6d1825be4f9c2f6efbc21aafbeb2d4f371b90e7b4fc3f7c70f0a8ba10b3b9`  
		Last Modified: Tue, 30 Apr 2024 23:29:03 GMT  
		Size: 114.3 MB (114306774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18fad7a3c3dec2031224eab9e284458528c0ea2ec75427eafbbb609fa72f00b`  
		Last Modified: Tue, 30 Apr 2024 23:28:48 GMT  
		Size: 308.4 KB (308381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5f61a028e7a15b34862fb805f21aa50571356d49c3898a88b66fa365baa7ea`  
		Last Modified: Tue, 30 Apr 2024 23:28:48 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0289aedc3217b314a6be9a7fc66e70170b6b8f08cf665143bfa215d6c52e8561`  
		Last Modified: Tue, 30 Apr 2024 23:28:52 GMT  
		Size: 27.7 MB (27666018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e43ecfc13baaa991b635bc0a4ca1afdf490dfc57ebdd7af014c11034a77842`  
		Last Modified: Tue, 30 Apr 2024 23:30:01 GMT  
		Size: 323.9 MB (323930911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7f7621614566411595bed8838de61451f4b680c5a4d17ec3a7fced6fa6e49d9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.9 MB (566935035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2139ef6d4d3e76ab33a34c51a979f91f82cf98c86855c4ccfea9335170a1f39b`
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
# Thu, 02 May 2024 02:16:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:16:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:16:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:17:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:22:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:bd60f30b99627b5549ca5e7bff2775c2b644e0cd30c8b45fc5138151253ebfbb`  
		Last Modified: Thu, 02 May 2024 02:33:53 GMT  
		Size: 111.2 MB (111162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b969bb4bf67906361ad61576a20a059d9585983685fa4627816b5d372617d9`  
		Last Modified: Thu, 02 May 2024 02:33:41 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a916c4b0f1c4cf0a44b3d8f1b0163250de4a881d0f8e26cad5d4f1ec05ba7f`  
		Last Modified: Thu, 02 May 2024 02:33:41 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4b118cd961c3a016019eb79dcaffa47df6bc91d3ee0bbe45774d48d3249d91`  
		Last Modified: Thu, 02 May 2024 02:33:45 GMT  
		Size: 26.8 MB (26810944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5cce51b59ba63cc66bff3d556595871666e7bce14ac3ef756e26e8ab28e4f9`  
		Last Modified: Thu, 02 May 2024 02:34:42 GMT  
		Size: 277.1 MB (277089771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
