## `ros:iron-perception`

```console
$ docker pull ros@sha256:e8830f1ea20b4ae6554ed2b0b407c1cf62b145622c077bc6d24148fa331dc2a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:527d413b7a38527c8ede72afda05120c09a53da68cb9878bb29caab384d170ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.2 MB (960245890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e703c5b2ab8d143a5edaac7528296e4c39d5fe28fda627b61f2db47effff0cf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7846943e3d9298fdd9fe26a42e42bf98bc05af7261e8bd2b1733e389edfe59e`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 1.2 MB (1213915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aa8586cf11825d7e10ae4444ca3b83648ae7dad28324ce38ae538e6180acb5`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 MB (3625561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f1565c7e7e6ff4f87e7d2b009d611e56267bddf3c32d322fe724e0916272e9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad7354d3b595af2bed14f27f06908e2caf0eac957613e4b27ef1509f3ee10`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e718750b0e9b02bd3475720412d93698bee5511db8ddae1cd3d9bf39339b3`  
		Last Modified: Wed, 09 Apr 2025 01:20:53 GMT  
		Size: 124.4 MB (124365656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36620f46180918624c7173c874dcab6859508f3d0078919cf838dfe86210069f`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925f3794b44a9c41a9dca97fc337e0c078057b6b8c8e08cb8589fda8c1aa1c8c`  
		Last Modified: Wed, 09 Apr 2025 02:16:08 GMT  
		Size: 85.0 MB (84978995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacefee13185173d4ff01dd7548b15ef2db6729cb16fd3a87143b1971b05eef7`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 326.3 KB (326342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40fa4dc66e5a94bf73c46024d39ad45c210cd3922fe6551205e89fdff9f6b83`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bdc7458748f6ca3dfa37fda6f04b5681ee7af8822f522ebad0672c98b74a6e`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23734603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb51f26a8b26812a2523ac94a4b24d2f93d58f1ecfe70f1cb6e42c3e58b8d276`  
		Last Modified: Wed, 09 Apr 2025 03:14:44 GMT  
		Size: 692.5 MB (692461909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:bc1a5e055290e92dcea49441cb61b69c60ff5ec03ca6b26789031932eb4bd66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58344159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d43f1af5c5bc3fa785f0b17ecbf0d8afdcca3c08f5ff93827ec6162204923e`

```dockerfile
```

-	Layers:
	-	`sha256:08f818f83b45126a611bbbb8fb31de67529ea2897ffae0963ba1640e52d972c1`  
		Last Modified: Wed, 09 Apr 2025 03:14:31 GMT  
		Size: 58.3 MB (58334484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200ec83f06dd4d7a37297f6efb7392a536e05a259aaa21801256cb8575acbd8d`  
		Last Modified: Wed, 09 Apr 2025 03:14:31 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:79f21b2e19d79e736d7594242f97b9b761dc9c1aff762e3f0b72cb087fda2be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.4 MB (920441425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2945b901f4ddad8be0349da17b52fbeff48d10b6537c9da4637ba67780c6a945`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203623a863f43e1e4b881948129cab8d7bea8980b186a2d5f73e12abefec75d1`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc3526ae0181f5bb51d08158c52a09b96e0f34319c8364f538ceb688698cf50`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec78c40c286de9039f4431dff10337f00059c57c3081b33d466230bb34c6168`  
		Last Modified: Wed, 09 Apr 2025 09:13:03 GMT  
		Size: 121.8 MB (121827814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5e3f6f19fdee885ac03b2133333e7dd66ccf52adc2d22fdc1c85140516d6f8`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf78a7404654cefd6c73cdea6c92c9504507fb337d1b192c319f5ebe576a1d6b`  
		Last Modified: Wed, 09 Apr 2025 15:50:16 GMT  
		Size: 82.7 MB (82653174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc443957dc455b1a1b37a2ee16ee89f84b943588123e09669f383265d60ad47`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 326.3 KB (326346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f136d44d7462d06b25723dc55af10787ae5eee9327affd0edfe09ac6ecf6488`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b176733e755d05394cf45d34f8bad771ac2328c723da26437741a03c84b041`  
		Last Modified: Wed, 09 Apr 2025 15:50:14 GMT  
		Size: 23.1 MB (23127398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81382454172fc2eb54c32396b994d770add9d8b7967324b1a7aadb2eb9e2c8`  
		Last Modified: Wed, 09 Apr 2025 19:11:31 GMT  
		Size: 660.3 MB (660334931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:5dc3a43919d7389199c7b68f49942f2e715fb761761f421eea8da97320c49d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58340254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a29c574cd7bac583d4377c6ee6d29139ccf3f84bbeac3c4c6f8f3464117d015`

```dockerfile
```

-	Layers:
	-	`sha256:502e50242b22194f416d3794b44c770607d18111d1fb368387a5d9b4af8dd062`  
		Last Modified: Wed, 09 Apr 2025 19:11:21 GMT  
		Size: 58.3 MB (58330499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df3f02146bede93f0eff3b34aa2113b2ea6f55736529d089d5ef4f498c776af5`  
		Last Modified: Wed, 09 Apr 2025 19:11:19 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json
