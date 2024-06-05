## `ros:noetic-robot`

```console
$ docker pull ros@sha256:32f09dabf219dc56dd8353f1c9d08d0f4d9d5158d2f47050e8de9dc96334f529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:3a6f7d904d7206bdd94bfd40c22b2f1026dd2a3a1be8df17d4b8cb018b5b417f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281658097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22055ee262111566fa4b4d36987ba4a4a675c5466f12198185335dae6769b1c`
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
# Thu, 02 May 2024 03:46:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:148e744f802628ef1fda93f6cb2ec95d7f4aadb4525b14f70393b4a6961b27a3`  
		Last Modified: Thu, 02 May 2024 04:21:18 GMT  
		Size: 16.9 MB (16928796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9524686e4eec342bcccf61e5f3cf478e5fc8ca325426c4e682bbed1f9e8f0613
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244891054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2912a93b958d3c6f8c6738c11a9eaf1509be89540af84906adeaba05830ea2cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 03:17:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 03:17:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:18:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cfdc59b78354ae32bcf5b55594f95d7055d41a7dc855a9b8839be3e74546b9`  
		Last Modified: Wed, 05 Jun 2024 03:31:38 GMT  
		Size: 40.5 MB (40506614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538f808a96d47124193d51356dff2e3ccceb60b634042d2154110232c7ea4f7`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b11dbf16d842b6f56ac3b8ece22e46a6e2358c415d73f99eb0487951c1742f`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d73dceec9fb4fcaad37b56a30558433c3f7ea50e56f1fbab4ce3a345dca0f`  
		Last Modified: Wed, 05 Jun 2024 03:31:50 GMT  
		Size: 15.0 MB (15030156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2bbcfd1f11e78cd501eb506b9114a869f65c71a7f06adbf1380c0f31e3f7604f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268498987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8bb70ca791bae66bf01a804f85d049232180028269cb2330fd0a95b0732514`
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
# Thu, 02 May 2024 01:40:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a8c6f686cb916978707587c24919108b59142326731a176c99d6adf9a4740e89`  
		Last Modified: Thu, 02 May 2024 02:26:55 GMT  
		Size: 16.5 MB (16530599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
