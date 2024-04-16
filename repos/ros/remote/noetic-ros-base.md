## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:1d56b31da48f8c65d13af7b1fd452ba8427b44989060f113dbfdedbaa649f6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0079c89a0b83b2a9bc8df635ba6e417cc70341fdc28b58b6107b8ee115aff90b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264727097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d27c296d320dd5e72294985860d6b8aee0e24e7e447e49c53b5b6d1a336f285`
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

### `ros:noetic-ros-base` - linux; arm variant v7

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

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b6ef817d5656642cbe1ee562a8a8375855b2e88c231f5ad95dcfb5d1e8837fc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251978011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bea440a091d3e9b7efec94ad5662096ef0a1363dcb32ff70504dddfb04738a`
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
