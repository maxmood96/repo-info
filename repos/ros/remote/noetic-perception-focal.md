## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:9a176c12bf224ec83705f50b871c82afb5586a550fe332c5d6a603249eb5c2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:52461efe4708b02006dd49cd166a62531e5c577ae371925b98208f8117cd1de4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835400194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c35d716844b824480907e9c138bbba6ac87639d51b452b59ecab78c12eb8df`
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
# Tue, 16 Apr 2024 05:47:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:47:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 05:48:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7fc7127f4302b5d7690e9128f8a7051575604639251e3a4fb770aecf12f4eb09`  
		Last Modified: Tue, 16 Apr 2024 06:24:25 GMT  
		Size: 50.9 MB (50942064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100c0401b1d83939b2f027a6560c4dc65fd7a4a4b6cc4ab6b73986a90c70a3df`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 320.3 KB (320347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5a527f20b46de848ab8d7d47519a866273776636a5ed05c0b5ad9776327ef4`  
		Last Modified: Tue, 16 Apr 2024 06:24:17 GMT  
		Size: 1.1 MB (1130655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531aa000bd3c3c147ba8e3f84106e3c508cbc4b17a3ade6e46fa307b41acd091`  
		Last Modified: Tue, 16 Apr 2024 06:26:09 GMT  
		Size: 570.7 MB (570672966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:24b363b3f0afa0594079f769e4a2f9ad595b7699fb12386f79ea76f1d6061139
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.7 MB (730741016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71259b9d424129594b2dbd6199c1548e4cda8523248e56d985160e77cda88d50`
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
# Thu, 25 Apr 2024 21:48:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a890070a65f31ffd4461eeb161999179f8006289a9d3d8b6d5f88fe4eb520727`  
		Last Modified: Thu, 25 Apr 2024 21:51:28 GMT  
		Size: 496.5 MB (496521121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d98bbfd83b227a42b3355642681f4c99bf3bdb7df1bc55c790af943cb1f8e65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785606448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224e629bb73af675852edeb4cae73685fbb15e18846e2593ab5556aed4c013e7`
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
# Tue, 16 Apr 2024 03:59:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:00:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 04:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 04:09:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e68cf2dcea72a76f4194585b5fe94ebc6ceed16911250d44186a9f060b3e832d`  
		Last Modified: Tue, 16 Apr 2024 04:28:03 GMT  
		Size: 45.2 MB (45207668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5333b432eed5e9067399472b766459ecaab72e2d23c9d5fd42d70f4275594`  
		Last Modified: Tue, 16 Apr 2024 04:27:57 GMT  
		Size: 320.4 KB (320355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a05f6a82e2dc62e74bac15cfaa0678c5f0076676fd02435d94d9e26f7a92bca`  
		Last Modified: Tue, 16 Apr 2024 04:27:58 GMT  
		Size: 1.1 MB (1115135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7702a3540858594d7cb89a451c6531d55f33384d21aa12c1df41981f9b1541ae`  
		Last Modified: Tue, 16 Apr 2024 04:29:34 GMT  
		Size: 533.6 MB (533639787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
