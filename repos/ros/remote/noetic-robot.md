## `ros:noetic-robot`

```console
$ docker pull ros@sha256:9aeaf1883e7f99ad6991f9d6d32a064d9a6ebd2eff53af117879df4efb4f514b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:c4b623c55d4f0efd4d55a6f4a04a86951ee6a76dfd3777d8b92767d18f7f277b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285180705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e21974628d32eb1929c77293e3abc72912dc98a640d0117b8c58f030dd5407`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7281aa604e720b5eaf7e72404849690d72fa5effb15608d2a303b3882f13c9dc`  
		Last Modified: Mon, 10 Mar 2025 18:14:14 GMT  
		Size: 1.2 MB (1191587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a18ba426e6ea26c8fd790e38fecd6025373c25669dd4315eeb94f7ed6599d`  
		Last Modified: Mon, 10 Mar 2025 18:14:14 GMT  
		Size: 5.4 MB (5361910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e537c3c3ddc4adb3cc0de8338089b7d98cf338a1a97a138514e61d335c0a0ddf`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493688bad29a80f481679ba66e7b0d6fcb8fd23852d6436d0d44395070278bf5`  
		Last Modified: Mon, 10 Mar 2025 18:14:13 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23863567396658bbea590c4eba5622c43ca5757b6235b1c39638f702d1783627`  
		Last Modified: Mon, 10 Mar 2025 18:14:20 GMT  
		Size: 182.2 MB (182208805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab278496cd9deb6d829558f60bad9417912d96a69106575b781f28c587248b6`  
		Last Modified: Mon, 10 Mar 2025 18:14:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f10566245ae7b1dbe985b768beababeb0c24425b84d360a75b42e134f7b427`  
		Last Modified: Mon, 10 Mar 2025 19:11:35 GMT  
		Size: 50.7 MB (50721416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b45450f27b6388c692d3dd88c1971fc7d928fb1972d4e0d1aa834957d9292c7`  
		Last Modified: Mon, 10 Mar 2025 19:11:35 GMT  
		Size: 341.9 KB (341901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8e3869e8a5095ddf47b56543b341986d86d402ed4888a9d2eb5b295c824b9`  
		Last Modified: Mon, 10 Mar 2025 19:11:35 GMT  
		Size: 916.6 KB (916582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab5e31af9c937f6f6f5083892882506d24bac6e9ad058e672039d362857b139`  
		Last Modified: Mon, 10 Mar 2025 20:10:56 GMT  
		Size: 16.9 MB (16924975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:f98e82bf6dae8c6ae0ae1642606626ba03b0ab63630b0d085f4b72d8be51c473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29511325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08291978f9f82b05621dfc28c3bf28dcc17bdba813b2e36da2e0607ddda977b`

```dockerfile
```

-	Layers:
	-	`sha256:fa6da71bc07efc74f0a9358fb0cc4870ed8f76f516466c3fb993ad63558c993e`  
		Last Modified: Mon, 10 Mar 2025 20:10:56 GMT  
		Size: 29.5 MB (29502000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb660e767ac21018451e7dbcd8730f4d72cf4314e16271717f5a60b32fb12bfa`  
		Last Modified: Mon, 10 Mar 2025 20:10:56 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:1740817aacc1db15c662e7365c979b72e4891f0454a33a54f4ede401178404fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247723226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcd0ffa140eb5e40c9da400e591912a76aefab3ac8943c959ded8a3abb864dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63403fc54a5c95851d7b7b8c40144a5f9a318cee65813dfc14eefc11288ef1ac`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 1.2 MB (1191602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7a32017f42f62156bbd13034c1e560d3c291b3c7d26b31a2a57871131c347`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 4.5 MB (4487460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eb69a80d32b5cdb468886f797acdf344eee06f2f9f6510e9d48a41316f3fd0`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d74eccd6b688697b2abb8ed4135c32d6faf5a9c10eeb053f449ad68fa905c`  
		Last Modified: Mon, 10 Mar 2025 18:21:58 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254f2e42a794615ac4855d623b55a398152062f1f9e286f1c15fe9c7042b870`  
		Last Modified: Mon, 10 Mar 2025 18:22:03 GMT  
		Size: 161.9 MB (161923934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac45b8cd6234ec64252da29a03ffda622d8cb517602f6f5af6d4956033de55d`  
		Last Modified: Mon, 10 Mar 2025 18:21:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc45151179805bc1c6d38dd6bb2cb5013007598ec757330781e297e568940d0`  
		Last Modified: Mon, 10 Mar 2025 19:11:54 GMT  
		Size: 40.3 MB (40284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42feb571b0049ebb27436266b1f2965944073dfd9821fa77503ea4d2cf50ee5`  
		Last Modified: Mon, 10 Mar 2025 19:11:53 GMT  
		Size: 341.9 KB (341900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f529e153073749b539502ea1187426235b2812ecbaadba764ba886e0739ab`  
		Last Modified: Mon, 10 Mar 2025 19:11:53 GMT  
		Size: 847.3 KB (847307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9295e76c3b79970caf0e40d20cef1fe95e921b317975f8266ac2f4bb78bde14e`  
		Last Modified: Mon, 10 Mar 2025 20:11:20 GMT  
		Size: 15.0 MB (15023517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:4f7a20f11630eb225ad10289b3f18372190775db8f65bb6325bb911c84feac2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29265642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86af39bb90371301145ea289eaaa4e120043c0f6083172d1232251ddc46c427d`

```dockerfile
```

-	Layers:
	-	`sha256:485ae8dedc2b2774097e4ad36bac35411daf8f0820c41f8b2e7cb6b1c0b96881`  
		Last Modified: Mon, 10 Mar 2025 20:11:20 GMT  
		Size: 29.3 MB (29256256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc5e280f4fc6c1a3182e312a20a213e74cc1d14432139115c891e9094a3e7f8`  
		Last Modified: Mon, 10 Mar 2025 20:11:19 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fefa2d22e18f900ca6763ebb865b5c032120b264bdbcce46ebc4a37abef89e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.0 MB (270975954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964e5ea962af99798fd5cf4b4eb32904d7e04612892705cd4d1987c7d7fea71b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2121f1f68d1125f94e05d5d5f8eb016a4d81ece6993d4e7c57bfe5ad26044844`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 1.2 MB (1191456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88b5cd2df85b5bf6fb6fb1ce3368e75445a74bb65bca8e0b7c862ee326d6a7`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 5.3 MB (5342153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc415fb12ec5c88f126a927064c087cfe92feb936886efa41626024d640a7ce1`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c2b989b81c9cede611618c4b68d5118f857fe6d7eb371449bfe5467122384a`  
		Last Modified: Mon, 10 Mar 2025 18:29:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4605f7e1eea47d341d92031419819b83d0405500f6bf1c118e732be197d7e9a`  
		Last Modified: Mon, 10 Mar 2025 18:29:24 GMT  
		Size: 175.7 MB (175710430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca092e0891945ffc24a56747a902585fab1a46bf29aa20e37747360dead81d5`  
		Last Modified: Mon, 10 Mar 2025 18:29:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42202f9e855ace69a460b084edae9cb26837b64d9824340a8cda3a2813d6ccd`  
		Last Modified: Mon, 10 Mar 2025 19:11:36 GMT  
		Size: 45.0 MB (44991183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621b8e717c780838641725b18127ce953c68f9d50772c01111fa3e0f41868b59`  
		Last Modified: Mon, 10 Mar 2025 19:11:34 GMT  
		Size: 341.9 KB (341908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0e24dd49ee6f9d9cfc01ab3096ea6c86179549b984d28649dc14d6d71e137d`  
		Last Modified: Mon, 10 Mar 2025 19:11:34 GMT  
		Size: 897.8 KB (897829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ab89a1a3a34aa65fa864b7535024430b9a9fac23aff0fc58fffd88ba82fbf9`  
		Last Modified: Mon, 10 Mar 2025 20:11:46 GMT  
		Size: 16.5 MB (16524695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:d4bf2f7845360043ba647a71b4fa952f321b30e04bb883b1e2c153e88d2a4841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29460165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7479993eb901a811da38c15602a648ad8e2588135353a2cdc394696ab07a6f78`

```dockerfile
```

-	Layers:
	-	`sha256:d180f6dbeee7c77edc0e5e6a6def90755efea384d43a04e1b2547d135f6c7700`  
		Last Modified: Mon, 10 Mar 2025 20:11:46 GMT  
		Size: 29.5 MB (29450759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2cf439658c812fad1d7ac4459b8041e69b85d31f50003a6a9faec74a9c7633`  
		Last Modified: Mon, 10 Mar 2025 20:11:45 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json
