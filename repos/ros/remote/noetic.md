## `ros:noetic`

```console
$ docker pull ros@sha256:035f5945072e3c7f772276987057b176b81413ac20ecda380320201c9871227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:41a0aad743d47e08bec68cf48005706c27a3d7aad10632d204cada99ef3642b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264703234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ea3953302a6e2a2f91d97e3176d5d13cf3f90bee0b275851f6ac905a51480`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:50:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:50:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024be12c4ffd4a149d28e31d958bc58069c42db5afb0cd99622d76e3e567d07d`  
		Last Modified: Fri, 02 Feb 2024 03:18:01 GMT  
		Size: 50.9 MB (50942122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc791a8924c8665d0f658cbb906ef7da28971a46346f6e0506615abbbf4f10f5`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 313.9 KB (313919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e64ce06ce76c1990596e84ebbdb5bd709437b2d9d8bd557617c4b324a27b6`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 1.1 MB (1130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:962f66ef1fb5e89c2defb0d9292396bc824c07d73b993906c6dd3dcacbe4edee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229837192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aebcf2c59e23191c160390b401ff59cf5857e2eb0507ee07d0e010919d3d86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 02:32:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:32:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 02:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832bc149615378810f4a9fe40729770ad9dba7a7c228e62d356c50099736428`  
		Last Modified: Wed, 06 Mar 2024 02:46:09 GMT  
		Size: 40.5 MB (40505317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdce4a2b8116db5f3f6152d30787df0a9c52fded830a5320b2269895938171`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 317.1 KB (317110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e455f7807a21a05976ec00cb49130c7b2d93e058e90a6d16d04dbc3aa81696`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 1.1 MB (1061437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ea77a409e77dc685cc6f7afce25cc7d0c9d1b13dc4b7b34afaeb7867a15ee646
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251988690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d439934e28b7cd08d1dd54db338ce1cb0cf22971131b27801cf6440d8265a7c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:41:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c611c5a97cbf0cdf9e83341151f6e4e327d36f5f1ec0a3ffffca3ad32b90b6`  
		Last Modified: Fri, 02 Feb 2024 03:12:44 GMT  
		Size: 45.2 MB (45207021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9018935407b2aa0321010be3e88629c37577aca47c2cc6fa04fbcee72458f4`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 313.9 KB (313926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df260141e23ac900edc232c7425584d8b241f1d4a8e53d7db1c3ddbc57ab044`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 1.1 MB (1114853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
