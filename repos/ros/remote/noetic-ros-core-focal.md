## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:2bc9c192df893b1cbef7320aa74e68aa63a85d7e5e450a0a2f5650d82ea27c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:d1e196ff69ec963adbb02205932140ad2bfa60648356c457ea3a5f9ad4ae4bc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212334162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713ee668ee8724c7d1e6c9005232dd20b3c0c64ff3548c66ca0afde66ee2ebc5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:30:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:30:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:45:17 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 05:45:18 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 05:45:18 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 05:47:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:20 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 05:47:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 05:47:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350577e5266945e4416d80fce245cb0971317163751d1b7260af54a9cb3b480c`  
		Last Modified: Tue, 16 Apr 2024 04:38:09 GMT  
		Size: 1.2 MB (1198508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e04936935ba44d82940f64f9eeb303923248c298ecd92e7b48155f112ff5d88`  
		Last Modified: Tue, 16 Apr 2024 04:38:08 GMT  
		Size: 5.6 MB (5553810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3b1d4dad59ddee8371a3ab046f6e0095e3388d04874c3d21fb804587f8af3`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f17d290a6474befa7b597f62f015eeed1d045bf1acc47e9d480bc70cfd781b`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29812559af96e682cd9256d59fe34acb684a5c6ba045fbb0274ee9bfee60132e`  
		Last Modified: Tue, 16 Apr 2024 06:24:08 GMT  
		Size: 177.0 MB (176994850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b02b11705da1fb18f6a5cff32609e59818c31c4a8b9ad68f476aebbad11eb97`  
		Last Modified: Tue, 16 Apr 2024 06:23:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:5be4bd88b4dd0f8435cc575a96faac5ec52d9735e31fada395d357100e1a5065
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192329576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7273443bffe70cbded19b90d9298804a0e57327d4f5859bab0bdb34c6d94f58`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e681636c6d110834bb7020010a7d8c300f8e8604c6f3553babf82a0e6f70e339
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205323503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81412ffff8171740fe1719a5b808d20715becbfc29f663ab4e7c8e11a559dbf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:57:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:57:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 03:57:12 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 03:57:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 03:59:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 03:59:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 03:59:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 03:59:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eec760d2952771275204853cbd79b7875ae7ec13ad8ef032b897e7bb82dcfd`  
		Last Modified: Tue, 16 Apr 2024 04:27:16 GMT  
		Size: 1.2 MB (1198928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6491bfc88f7a9e85b4547d77cd1c05719f020a30cc47cb43fe40efdfa6337f`  
		Last Modified: Tue, 16 Apr 2024 04:27:14 GMT  
		Size: 5.5 MB (5532407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59218009560d754bbbbc21b59012c039ea115eecb469087ede52a4707084eb0`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 2.0 KB (2019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f235077395f573c8116982ca2322a5489128ec6824f3d3e2f7df1a2b9db682`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90233dc2d11e0229857f05179bf2e1c6b02f09c31c064ba2681e4fcf0cf2bcef`  
		Last Modified: Tue, 16 Apr 2024 04:27:48 GMT  
		Size: 171.4 MB (171384701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dc3285e50ca5cadc420875addbac6a709f14fc4a0287a79fc6a71d541483a2`  
		Last Modified: Tue, 16 Apr 2024 04:27:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
