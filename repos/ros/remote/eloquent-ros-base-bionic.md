## `ros:eloquent-ros-base-bionic`

```console
$ docker pull ros@sha256:f1b31418a9ac6d9af49983856cd54778f0d552b6c8140b3570d4d437b09f8c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:7e9a4cb04479daa45528bc64eb8443c9addddec4bc11bd5bd10f855b475bd38b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284223084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b386cab965997cb59ed84f43815e5796c5c146a9d8fe530fb2f4e9e3c9476f19`
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
# Sat, 09 Dec 2023 03:48:45 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:48:45 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:48:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:48:46 GMT
ENV ROS_DISTRO=eloquent
# Sat, 09 Dec 2023 03:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:49:45 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:49:46 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:50:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:50:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:50:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:50:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:acde76eba4d4e8498aad6d875227f7c9099d9aeda9dddd94a20809595b92e947`  
		Last Modified: Sat, 09 Dec 2023 04:48:06 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c37c08ac634e6d38933df0c02ee3cb5667ae6a9821a9bd52009fe3caefecb39`  
		Last Modified: Sat, 09 Dec 2023 04:48:38 GMT  
		Size: 183.2 MB (183220587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c633bda9b91acd880ec76f0b0b123de783a543408c34f6b8ec48d3b5f946cf`  
		Last Modified: Sat, 09 Dec 2023 04:48:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7f621c1fb796c55fc7c77eee0ab2565af571f3c4e3c688da6a63d15ed43d69`  
		Last Modified: Sat, 09 Dec 2023 04:48:55 GMT  
		Size: 63.8 MB (63753882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e3b2a42b24a56076cfaa4bd5caadfe6ccb6b1081274f265579a20ee225434f`  
		Last Modified: Sat, 09 Dec 2023 04:48:46 GMT  
		Size: 240.4 KB (240442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0970ba80184e0e910fdc903565c677be89682c5c3809f9c6a5300e7806b63d`  
		Last Modified: Sat, 09 Dec 2023 04:48:46 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2266c2b93777a3775f1698aa59fcaeb5bbc4bfcc75b97daed2a1a3ac7bf83a3d`  
		Last Modified: Sat, 09 Dec 2023 04:48:47 GMT  
		Size: 4.6 MB (4588224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:d379c6127c2c4be808e0ce7ffa52c776b75abf8a33092258ac758b794518c2af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235997462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbbf5465f23910343abf2aea085b59f4fee05735485e4c0fed180a1bddb31ba`
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
# Sat, 09 Dec 2023 03:25:43 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:25:43 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:25:43 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:25:43 GMT
ENV ROS_DISTRO=eloquent
# Sat, 09 Dec 2023 03:28:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:28:03 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:28:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:28:03 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:28:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:28:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:28:55 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:57c793c7f3a118ae9e4d4f53d0d093faf1a193e9dfcac1baa25b75fff7bb3b7c`  
		Last Modified: Sat, 09 Dec 2023 03:44:15 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f28e9b8e963c120ae7664d793862196ab199b8a4c3fe049ea8303de3171c1fe`  
		Last Modified: Sat, 09 Dec 2023 03:44:46 GMT  
		Size: 156.8 MB (156783586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814cc6e54cdd4a8a81f9cd0db77aa1dba3eb85dab1f2358922cf657297c3c6f5`  
		Last Modified: Sat, 09 Dec 2023 03:44:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d1710ff3194f3ea295be983db6380e4af615d684dd80b48a6de0494c4499e`  
		Last Modified: Sat, 09 Dec 2023 03:45:02 GMT  
		Size: 48.2 MB (48247944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075812fe1368dc08489c5d65ddccaedc9714e7b28dc30fbb0e8ce195b772af23`  
		Last Modified: Sat, 09 Dec 2023 03:44:55 GMT  
		Size: 240.4 KB (240450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1099efa64d064578f3ef5a707705084237109fe9596f2f87904905fee91497`  
		Last Modified: Sat, 09 Dec 2023 03:44:55 GMT  
		Size: 2.4 KB (2427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3717687124f3d9c5791e09e569d8def54c9bd0159f6e5776ce2413fe6f0fe8e`  
		Last Modified: Sat, 09 Dec 2023 03:44:56 GMT  
		Size: 3.5 MB (3496971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1864181798821d3235c7831ff19f2f642e8f57bb176f4061160758a65107d939
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258254233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadaa480922ff5b45e4b8b410c06cfdd2d56c9d7a874079fd774ed0cb043b3e3`
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
# Sat, 09 Dec 2023 03:16:14 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:16:14 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:16:14 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:16:14 GMT
ENV ROS_DISTRO=eloquent
# Sat, 09 Dec 2023 03:17:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:17:14 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:17:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:17:15 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:17:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:17:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:17:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:18:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8a151493b6c9d8425d7a9e6a9993ba4d731ad95e12a87256be858d78684d1286`  
		Last Modified: Sat, 09 Dec 2023 04:04:12 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275752ffee34d72b25cef8a220d83716491d1d0bd45b8c1aa4fae36ba907a345`  
		Last Modified: Sat, 09 Dec 2023 04:04:39 GMT  
		Size: 168.6 MB (168606855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9479152d19f2aa17356df5322c932e234af902cfd11b793012f23329c8c79c`  
		Last Modified: Sat, 09 Dec 2023 04:04:12 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060b6e6ec91a69696d3a30e570566858a8c81d35a90b1563198d9c5a12acdc45`  
		Last Modified: Sat, 09 Dec 2023 04:04:53 GMT  
		Size: 56.4 MB (56446168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb3122a7276f53e87b38348885606ff107df1dbf3eaaf3747680d75b627982`  
		Last Modified: Sat, 09 Dec 2023 04:04:47 GMT  
		Size: 240.5 KB (240451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3254779e9290c20ec877ee69e363c350743f4de49b96453d2c882bd5a1d5eb`  
		Last Modified: Sat, 09 Dec 2023 04:04:47 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6ee3ef7fa3685810aa57edf4c9c1e9b933ad324de2e6d4870d903a842e4807`  
		Last Modified: Sat, 09 Dec 2023 04:04:48 GMT  
		Size: 3.9 MB (3933942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
