## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:655cf34e42f94aa0111f1d872decf5582d91a9ae2dda90b73b7454bbffa55e2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:c7631b6323509f943142bd494abf268127a6807d81bd75e5f1fec2e0cd2caf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263061226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408a67701899f969b3e60f4a0eb58d35defafadadb7f564aadcd939bac6d28d`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fc58b4b5b47a9daf00a015010b9c405b2bee15fbcedb748dc03ec81728c088fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27594860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4332305b98df7ac49ef214202dd987420519c390e070c0a75a3ae2192efc6d46`

```dockerfile
```

-	Layers:
	-	`sha256:89609352396b765399d331c17b049a4903d13cc7b7165511bde21d8a061ce2e3`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 27.6 MB (27581208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783f1ac79ac7347d7269a070e63dd8d785bba5a1bf91955cdf05d7a0faac1760`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:16f26c7d44fbd3cf3d9e035ff76de360e992cf6fc7e4254290980286774ed4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0057b00ee435f96c6f5be12c690f3189f8a289111f5b5915f940befb9a00f0fd`
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
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
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
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:2df235d55b1f2af746ffc7217df4e45535de5e5073e1f5827e6105ab6b528b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c37f348b239028298251d0b86d1db02d5b50229cf5448fcdec29b57d7514c3`

```dockerfile
```

-	Layers:
	-	`sha256:e2a7dbfd0c788d3bf5679e89cf1b8f0005ab4953a8d6db188b14521177558656`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 27.3 MB (27344563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df22184734123eb54b635454f9e7340cea27496039962e972936a206f75ac5`  
		Last Modified: Sat, 17 Aug 2024 04:37:55 GMT  
		Size: 13.7 KB (13746 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d77f21b335488076a87d9a8f8c28b1ebfddca8c05ce0eaa2c6f87f735200f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250130142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0506c22d8fd8347c0efb1e962f146e28d52cf08b67c437661d6fc00d43acfed1`
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
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
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
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:507079eb803a28edee0a748fc0f2a7e01baddd285b3911753794c3afb3ae1dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27461621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafbfbddf500b2700b9b02cc29de87c89b1895a7fb99719ecc8bdd4d2f6c4afb`

```dockerfile
```

-	Layers:
	-	`sha256:ac5c0e52276d8f8cd8be47db7acc0f0710cd263c766060f69001cadb7b50512b`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 27.4 MB (27447597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cd9fffa9b07636cc8d1c1fe41f4200966f27178c82192a8f2946f6e2c636155`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 14.0 KB (14024 bytes)  
		MIME: application/vnd.in-toto+json
