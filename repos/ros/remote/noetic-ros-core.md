## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:ba9c7efeba9d068ae4f32d4d10b463ee4e1d889482739c3ad1bef5ce87c3a360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:3d8309bcbc1866b9f648261f1083b315dc7e027be665caacf4dba5deba8981c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212337312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4433647c87593add14b75b17c1df6952cf57ede1b3fc1a1d62927c5c3300e88e`
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

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:9c805f96e59bfa706f4dc457766221f5eb8362657f06475e0fbb0c3a5698a206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187953328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c4484900c4fbaac43927ec35f52e49452c8cae4c23adf28ab78460f898e8f5`
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

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e595a95536e614013da0eefaf9312c846e14db0448831c3673bfaf716fef40f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205338655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dc6cbf2be3a541bcb3be985de27cb7e28e1ed71388f9cbc3b8228e96c83c92`
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
