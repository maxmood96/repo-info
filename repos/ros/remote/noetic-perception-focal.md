## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:c09aae48b785da56d7344f06895b02d6fedf506f1e571bd56aa786bc0d6df0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:11f498f513e2534e44d09ce467abfdf35309186dea2dddf1d6525e05c0a81a1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835442875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b304e402828779989a0808fece12cb1467eb41b9f1150fbccaef5ee777ca15ee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:47:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:52:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309495ac492939fdfde58cf1da120fd01dea776ac0a3e45571a05ea16397fbf`  
		Last Modified: Wed, 05 Jun 2024 06:24:03 GMT  
		Size: 50.9 MB (50942120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d1f7dd7d6fa4c340c75f515ba00dd63ee35abe4412137c64f5eb2798199`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034066f6b071e6963ba4d9a67225826faeb2a36f7ab0cf1b22c3eb9ce5b50d4c`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 1.1 MB (1130676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f8bbb2feda4a64a67d52e553f651c44b46c596aafc2576d96f5a013c213f81`  
		Last Modified: Wed, 05 Jun 2024 06:25:49 GMT  
		Size: 570.7 MB (570696392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:36c5d63c3e3503fd964b11d74458e53c2b2e48a679d495e0440e9a6d550d9266
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.4 MB (726381143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6960f2606800f20438876589aa153a9c53debd190b2030efe33b97c115e82736`
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
# Wed, 05 Jun 2024 03:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:f571459483a794c9e8e8f534a0c2b226bbebc228e2ab5af766c7a27c79c84442`  
		Last Modified: Wed, 05 Jun 2024 03:33:05 GMT  
		Size: 496.5 MB (496520245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3936901dcc1fe259133babc1c556f049c38cbc96577dec5975cbb0e01d4d8454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785645182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974cf60bc830169980e9b095faecb33cc29aa519d93ca6f14529311cde4dec8e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:02:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055caabb25cb3f56fdf7f72c7c835b3b1a31b20b9bbd24ae2fee4ab2a32811`  
		Last Modified: Wed, 05 Jun 2024 05:48:51 GMT  
		Size: 45.2 MB (45207269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c79a6839de6fd95d123e3a7422ff707f103d1ce1a76a5eb533428e9406735e`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 323.2 KB (323165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c477a284d1c9c16d5e3f1580b6ccf4b4667a94ec48b60aa971e29021b82fa`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 1.1 MB (1114835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac49e590bb5479f0b16356093f73e0f90c036c4db368b00ba0dbb8975dc79ec`  
		Last Modified: Wed, 05 Jun 2024 05:50:20 GMT  
		Size: 533.7 MB (533656966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
