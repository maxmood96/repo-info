## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:20b337f10f4275a6d589388cf8f72a7216de2ba3632b10d9d05c205c65446b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:a98aba6bd66e748c00ac8e3f49301a705098d21895e3b8083810128b4970de85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264727228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff1104ff05bfbfd2cae96418b8bf424f39900b1ac3078547614b0578cb6783`
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

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:635eb1391a3b8bb1fc42b87569f1f2dffdaf3c80c160a640d94f308330021e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229839090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc577849b266aeb15413942ea0a869d4b9dedab59d86a27b31202dd1302abaf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:57:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 01:57:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 01:57:41 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 01:57:41 GMT
ENV ROS_DISTRO=noetic
# Tue, 16 Apr 2024 02:00:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 Apr 2024 02:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 02:00:33 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 02:01:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:01:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e3d993727e234d20d5ebe7b239f39bc376ccb0319dcb3d36ec01bb0abf6cec`  
		Last Modified: Tue, 16 Apr 2024 02:11:47 GMT  
		Size: 1.2 MB (1199168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff23c5d52e0ed7e2717999a401b023666d3f8f2ed49b1dacd29c0257606f50e3`  
		Last Modified: Tue, 16 Apr 2024 02:11:45 GMT  
		Size: 4.7 MB (4679896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd81682e9f89213ce83d83567ce465b5c40f8be53987501409c534146433f1d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74dd2adac4f62063623de475b3c08f2b52337d70ae5daeceb7cb2a40cf6cf2d`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d1e8521edc35f0e0391b0eabd7c5021c85ae02cabf14e2b3c8d1611b86553f`  
		Last Modified: Tue, 16 Apr 2024 02:12:21 GMT  
		Size: 157.5 MB (157467075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059939f2cf750e2392ffd5141665f6db37220524b0b85a6da0164bf46002341`  
		Last Modified: Tue, 16 Apr 2024 02:11:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7425da53f3c1d55c83d3a606a99acd8eef02039870d76d98ebede0619d0b2122`  
		Last Modified: Tue, 16 Apr 2024 02:12:36 GMT  
		Size: 40.5 MB (40505672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafaaf4238382826bc4dfb255028df6bc9ddc8bc776e38844ae4d49eb012aa8`  
		Last Modified: Tue, 16 Apr 2024 02:12:30 GMT  
		Size: 320.4 KB (320353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5043f2ccdd491f51c214414dedd2bcfa681447f1a87169fc8c9be6ad8ce99d5`  
		Last Modified: Tue, 16 Apr 2024 02:12:31 GMT  
		Size: 1.1 MB (1061815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:10c849400e59d70fd0382b5451aff7f989e32640d4abb0afbc11e4cd93f120ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251966661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5231a09af0bed0887118754f7797c9ed15471a9b98876bae2afd0f72656b6ca2`
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
