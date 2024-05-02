## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:56959310b6983c5aaacb3e9c1d94b7f5edf9665ea0baf805e1af47e38cf4a1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:8d012e1794d7019802be9cb462448788898509e1f98ee46ad7a23bbb2f8513f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835402970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be917fe752a096a8264db442912bd583c805319b0f7bd93941978ff4cf6bb88`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:45:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:52:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c3ee459bf535e354c3ae5772e5dc01acfc7c39896912f2cb3d0e028f483594`  
		Last Modified: Thu, 02 May 2024 04:21:05 GMT  
		Size: 50.9 MB (50942130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880207582f574785e219e4fe9c0ed76d6a71bdb7737257f3e1e5eebbb9512`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 321.3 KB (321273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2631648f5934240033e56e0e8675f135439fcb185b941b63b2ad7b837cf7e`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 1.1 MB (1130667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6c72841ac154ae796f224a0247b3ca6fb15ac539e54561cc2b9b23443bacf8`  
		Last Modified: Thu, 02 May 2024 04:22:46 GMT  
		Size: 570.7 MB (570673669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:d7a744035fb1321aa63c110f2c92d9282753de91a105f25d0bbc411247b0e2f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.4 MB (726371761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1c652fa83108c130d327c496b370a1674f486873ff25d3b9d9dd54cb441f8d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:50 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:50 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:43:02 GMT
ADD file:5789980ed37544805bfc38f68255149cf4ceac7689ffcbcf606720b1b7170733 in / 
# Sat, 27 Apr 2024 14:43:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:31:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:32:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:32:02 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:32:02 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:32:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:32:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:32:02 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:34:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:34:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:34:42 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:35:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:35:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:46:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8bc6554297d271d6d4b2d1b92b5a4a9fc067e28e04c1d749f5fa99295fe0b1d9`  
		Last Modified: Thu, 02 May 2024 01:27:40 GMT  
		Size: 24.6 MB (24604686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd985310cba8086f206a6048f4b3bd5199f44a1743dcc51ac515633e75e0fa8`  
		Last Modified: Thu, 02 May 2024 01:46:28 GMT  
		Size: 1.2 MB (1200360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f43ecdec7e1ebaf0cf9c242f95cb61d8d03620d3d621149960dd3642aa9b909`  
		Last Modified: Thu, 02 May 2024 01:46:25 GMT  
		Size: 4.7 MB (4681121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0a2622b6713e97ea241960da874c2e0b71ac5537e012ca46663651b3e5deb`  
		Last Modified: Thu, 02 May 2024 01:46:25 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88348572b90bf6ba5d1efce66d3087d8a543a775b2e4ac869db130202bf51a89`  
		Last Modified: Thu, 02 May 2024 01:46:25 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a2206d0f480c67f115ee930ab37de12ab92e63ed0968a45feddb0c9e16e155`  
		Last Modified: Thu, 02 May 2024 01:47:01 GMT  
		Size: 157.5 MB (157470938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e78c2525822682e02fa368fabde02c7587ece63b62ad0ef06a43370a3dbe03`  
		Last Modified: Thu, 02 May 2024 01:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bb47acf423da109d525fc838aa26cc06637ef40cb60bb44ed949bd7c4796c4`  
		Last Modified: Thu, 02 May 2024 01:47:15 GMT  
		Size: 40.5 MB (40506863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e711dabd14809f4cbeba4ae62e253c057066cf9b8ae8a7a4ba7fa02d491f38c6`  
		Last Modified: Thu, 02 May 2024 01:47:10 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9460635641239b9750422c4e7b50b61c4a5eeb2bff01dd8736711846d63309d4`  
		Last Modified: Thu, 02 May 2024 01:47:10 GMT  
		Size: 1.1 MB (1062991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8a37cb60c6dbc5909e142e0b51f0ca9c82916cfe84a7f6a2b5b2fecbae554b`  
		Last Modified: Thu, 02 May 2024 01:48:44 GMT  
		Size: 496.5 MB (496521044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4fbbe768e3d8f62c74b207d8066be5d19e60603f02c3f412bdc8705040443c06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785607788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eac203a831c8bc83122c4c2c5719138c5a2ad7da6e1756e3d543cea245781c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04978fbd01f4ac1f8deb48a3af3b6ae2156a3391bae378b5b70c6034c28bc86b`  
		Last Modified: Thu, 02 May 2024 02:26:39 GMT  
		Size: 45.2 MB (45207993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a3b7368effc67cf6c5233658704ca94e11ba21d4cb3f96dc5dbd5c4c22152`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 321.3 KB (321274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d39198ddd342125de1b67017e7b7cd521133b18a37e4d153b8c10f01f7c0`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 1.1 MB (1115420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901273720d18672c8e8b0a89f41fa95c3c247baa7502a07c5a44170b616d9ddc`  
		Last Modified: Thu, 02 May 2024 02:28:11 GMT  
		Size: 533.6 MB (533639400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
