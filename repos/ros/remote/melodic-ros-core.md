## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:82baf144538428a67cebe7819b1edecf91d687fa38e4bfba646c9ad19359b326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:42d6936ea543d58f2327869e9f62b2840cfbb3978dc242fdd221551fa55b68aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292031610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e543bb90abe83e46045fa726422d3ee94dae38a2d13b49f6a5156d5976c47ff6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:55:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:55:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:55:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:55:29 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:55:29 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:55:29 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:55:29 GMT
ENV ROS_DISTRO=melodic
# Sat, 09 Dec 2023 02:59:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:59:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 09 Dec 2023 02:59:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:59:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384ee9769243a721793f2bfc136371fa17319fb6c6b6477a2e03a17d545616c`  
		Last Modified: Sat, 09 Dec 2023 04:36:31 GMT  
		Size: 818.9 KB (818932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc85c6d8f29e7702b5251b205f55245dc5eb2973909564ad084046a1f6c9324a`  
		Last Modified: Sat, 09 Dec 2023 04:36:29 GMT  
		Size: 4.9 MB (4878334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9964396126f3f0fdee6bb57ba39280b6966c6879a933be850490cea1c00bc65f`  
		Last Modified: Sat, 09 Dec 2023 04:36:28 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c28351996c6c7bb200787f2ae30700632287e339957c50cb872ee1c5ed42a2`  
		Last Modified: Sat, 09 Dec 2023 04:36:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd55250710281eb618886b4fe6cef44a1ca9e053ef131934d46b782e9b734add`  
		Last Modified: Sat, 09 Dec 2023 04:37:12 GMT  
		Size: 259.6 MB (259614154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c210fd778b46dcd44d92baee49b532e8ee1587f7d81be6dcea176e8acfb8d3cb`  
		Last Modified: Sat, 09 Dec 2023 04:36:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:0f75eeac3da8cca60a327f85e2d8f6a73fea798086828590c067a5d5e340e780
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266300288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89c28efde3e34d67c88abfe176b3b10ef3413be4b3923bd65ff91dcfb641276`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:56:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:57:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:57:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:57:08 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:57:08 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:57:08 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:57:09 GMT
ENV ROS_DISTRO=melodic
# Sat, 09 Dec 2023 03:01:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:01:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 09 Dec 2023 03:01:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:01:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76bc0c6b06fc92c1f911be6147b55b6430301b80e4062178329c4fa8a0f79f51`  
		Last Modified: Thu, 01 Jun 2023 23:54:31 GMT  
		Size: 22.3 MB (22312178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e61f2f0ecdbc00c1478913acffbebaebcb6c199462717018cc5c71eed71d93`  
		Last Modified: Sat, 09 Dec 2023 03:39:09 GMT  
		Size: 820.3 KB (820323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13552f8532802decc8d718ee39a8826c22eb2f08a55ec54be8349c2ec390066d`  
		Last Modified: Sat, 09 Dec 2023 03:39:07 GMT  
		Size: 4.1 MB (4090743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73031d8d6723d2c344f35a55a3313e78b28caf1442735033da25f0e991699c8b`  
		Last Modified: Sat, 09 Dec 2023 03:39:06 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea471d10f31c21943b5fb3a94221ddd6ecaed5355c282e8c3fff7319bd09f4`  
		Last Modified: Sat, 09 Dec 2023 03:39:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d630a7a6dcaf92636c94de605851c8e3899e235c3100028c236a501a228ce6`  
		Last Modified: Sat, 09 Dec 2023 03:39:53 GMT  
		Size: 239.1 MB (239074210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c6d49c19da38a18503f705b389fca4852bb3be7aa962e68997fb87f17685eb`  
		Last Modified: Sat, 09 Dec 2023 03:39:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:253d2bcc35a57a71fd77d68dcfd6e2b2542e57cf40adc5dd148b4eef424adf4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281549133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28abffbe21f85ec3ac71e5bde9558b558c6d59f46155c5d90d20b52a53dc19dc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:23:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:24:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:24:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:24:04 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:24:04 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:24:04 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:24:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 09 Dec 2023 02:28:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:28:17 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 09 Dec 2023 02:28:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:28:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92311637e9983a187857b246a6417188e5a1de48e9d03e831eb2cb63a811cf67`  
		Last Modified: Sat, 09 Dec 2023 03:53:39 GMT  
		Size: 819.0 KB (818985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4394df3604b47aaa3d36d1ad63c563ac4d8b172081757c048ee6bf10cdd08`  
		Last Modified: Sat, 09 Dec 2023 03:53:38 GMT  
		Size: 4.5 MB (4461631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1d3a8f1076e5ddb09c78ae7493c813f46853e1e63d7cfe42ba1c50cf6bcf28`  
		Last Modified: Sat, 09 Dec 2023 03:53:37 GMT  
		Size: 2.4 KB (2409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036e7f64f73112ea8e18288826f4488b6c199f9eb6b52b365c9394cd9985aff8`  
		Last Modified: Sat, 09 Dec 2023 03:53:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64713228c51d8c1f734ca8e4d8d35b5df0f68afa2b011d2ad527c7f817d315f5`  
		Last Modified: Sat, 09 Dec 2023 03:54:18 GMT  
		Size: 252.5 MB (252524786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e6f76be465d778be816e36f006d438bc9c9a13cf3ddf69d36bbe6421643429`  
		Last Modified: Sat, 09 Dec 2023 03:53:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
