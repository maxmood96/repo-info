## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:b1b54754a3b0ab5c5fcb2bab22af22a76cec3a610669db310b90522d64437197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:19da7f9b9cdd8f1c74e7e85bd1c489c5cf44d5a07a9103fa6e03ed22e19d7452
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269855614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2655d647e16dab430a4ab3e0fd88a0ff4d48d749c9fc095b92ced2cf84cfa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:38:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:38:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2042a043f80758c28a5085cc32b1b95a7ca2b058c0cafd51cab3a38f6c90abd9`  
		Last Modified: Fri, 26 Apr 2024 00:08:20 GMT  
		Size: 50.9 MB (50942523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89c27bd2976f63a3b389c2abca113a81e69f65764d0cd0b29bf8d6c15e2048`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 321.3 KB (321272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739fa1e6ce1a27dcd30dbe9247ecd6e46e3ab63e942aed8b10426f25b5ca4617`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 1.1 MB (1130946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:bb6a6d98c3c87304529ba58c0bd3552bedb2d340eb7f25a9a01645271b667e8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234219895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ab54c0bf134242e1fb27512203ae482be46b731ee02315d6e2eeb41632079`
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
# Thu, 25 Apr 2024 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 21:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:bd2816939926a122bd358038de82d4cfab0e8f0c93b2314bd6255b3714e16ce3`  
		Last Modified: Thu, 25 Apr 2024 21:49:58 GMT  
		Size: 40.5 MB (40506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc2d4fd3276529e1d6a7750cfeed0babd5a9715ad7f05f84265931aa73ed916`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41cf2f29b6ef786b1f9bb11f48d1a06b36d458954f8e8e7fea76e3417bd029`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 1.1 MB (1062732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5865307a4a1cc6f0107c987374732bb7439d634829c17d52b2e4e2f485b4a099
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256234064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee4042e70495fb72a82455992f83cb31483c7ba66e016ad7e28347669434a9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 22:57:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 22:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8e1dda62c86776ddde10c811ef285d3c93bb5e555a2bc77c86d47b7a8eae2`  
		Last Modified: Thu, 25 Apr 2024 23:47:13 GMT  
		Size: 45.2 MB (45208883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe611b97ee16439882986c4db27e03bd4a744413b106139077698f89e94f066c`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 321.3 KB (321275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e83a2db4356c8df2eba1a0d044a5b944d95996fcad3f50882dd8ecb50b9d`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 1.1 MB (1116233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
