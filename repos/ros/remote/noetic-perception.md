## `ros:noetic-perception`

```console
$ docker pull ros@sha256:2ea2d2daf28a4be8cf8138792d50526a587e82da0d0a9950b1efdceda7a4fc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:24d68148eea081dd8b8ddabea91dbaeefbaa259433a585789dcaff46325f7114
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835219651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b83a16ebf4c9d7b2f2dc882e36fa18644f75fcc35d0d0fa5f09ebfbfb4f7ef3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:33:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:33:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54e59330e9a8f9d250b062121a852c8a375d755bca20b39794ea2bd92f3e78`  
		Last Modified: Wed, 06 Mar 2024 04:58:38 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ddf4fbb020496e4eaaf355a6cd2a24b481295beffeb19738591d417c3c51a9`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11354471cad5084e7d4a54163b6875984b80aae53f1b22226e60250b6f14b465`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 1.1 MB (1130634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5255159392436789f89a4054e639b6e1707c49e38e1f1a92f713cc3c07d774d6`  
		Last Modified: Wed, 06 Mar 2024 05:00:21 GMT  
		Size: 570.5 MB (570492554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:9ce23ca0160e6c8103116c5b8cb64e9675feecd931a6a5471d7aac119c6d3cb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726218440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db7e317d856dff1ba8cb75151e6ca692cd462fc1e64f572d0c748fa0666bee0`
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
# Wed, 06 Mar 2024 02:44:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1c8d30e0606ce27fd291d8167034e47a6d2aa920bbe64f21eae76d07174e76e0`  
		Last Modified: Wed, 06 Mar 2024 02:47:57 GMT  
		Size: 496.4 MB (496381248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a36bb43bec3718d7b6b9438fcb6383400204b811d7cee6c1f1bcae434d92f455
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785467683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f53d8d7f193ecf16fe38aaa4eb475165ff1697ea44b6b61a1347144149fc66`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:12:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:22:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c690c1ca3d85a61d8f3e87d84817be0932b2873f0785d6d61d64d3f54a7137`  
		Last Modified: Wed, 06 Mar 2024 04:44:55 GMT  
		Size: 45.2 MB (45207349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39e35aab238ae9a046045f0be90350874ce4e999a82a14fa6b1ae0e3616cab`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b89ab41d60352f77ccd8e2a2d80710850509070284e9dc6792a405b578dc1b`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 1.1 MB (1114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d2daa20df3657295834721a85f09970bfe42b9cd4f9c163963124f230597e`  
		Last Modified: Wed, 06 Mar 2024 04:46:29 GMT  
		Size: 533.5 MB (533489672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
