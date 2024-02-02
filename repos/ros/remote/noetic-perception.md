## `ros:noetic-perception`

```console
$ docker pull ros@sha256:2c148353584102ee7991e9e5b00480c64549b3861704569466e89505cce4fe02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:bd001e6c1caade1e9e6c9b113b27c8cf357ef9521e4f07c03bc3193768f70f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835191775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3094361c2b747dfde1632ee2f4628bfad5c2998162e6900fa9598c48993a50`
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
# Fri, 02 Feb 2024 02:58:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a0d296db1c4147b052044e176bc981e70533ef30f7d4fb898c04660e4c4b70c8`  
		Last Modified: Fri, 02 Feb 2024 03:19:42 GMT  
		Size: 570.5 MB (570488541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:8116a2ec3393b0b10dca954cedda9f8365cc5fb9337a2e99ddb9b4039c06325a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726198513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b01c33a81a2eb5710e8e3b8733ca3f43835f6c7860dc7cb64ffd4a99051b65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:16:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 00:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f14aa3c10e2086f72ed556eda8d19460fc5d82b83b1907928a09f36a4164d5`  
		Last Modified: Fri, 02 Feb 2024 00:26:41 GMT  
		Size: 40.5 MB (40504147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb38a6164e77c6851bc201aaeccf8c3fb2232a434cc5c76191bdc9d9220925c`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 313.9 KB (313921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1f3a607ddd355114411ed00b9b5d84628f9b5d9983316fdd11cf697833b61`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 1.1 MB (1061142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1055a8b31ee9456fbc9755c48f94ce23fc267bf488bc15ea829546c767aa0281`  
		Last Modified: Fri, 02 Feb 2024 00:28:12 GMT  
		Size: 496.4 MB (496372955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:592dc254833f8aca88a2637371bf3761c4803aa4a293694c9645ae7c78d9ce47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785478217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e8a46d9370a9f5bbe88a2218ed403e1b81b69516011699c34e2fe8df54191b`
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
# Fri, 02 Feb 2024 02:51:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:367843c93cc0c093c415056cd200d5951983cdf6a6f6b157323718a00d486498`  
		Last Modified: Fri, 02 Feb 2024 03:14:17 GMT  
		Size: 533.5 MB (533489527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
