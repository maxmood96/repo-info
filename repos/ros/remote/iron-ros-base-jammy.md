## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:dad3689190929a744c752e22afc537941281589319cf8ddc53dace56e4e77c08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:cbc62dcad96543658418e453f653564b1d2de9f7e07c1c364677d30c875d93e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267783981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8667f453785555730325cc280970ff18ff8faf60032d2162ff1e20fd14bf175a`
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

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:512f1d9c9af4c68806f7ae6dbe8005fe8c8cc6d82b482631f8212ac27a61df8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23738300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fd46e65de82e8225ea0ea59699f2c7cdae83bff91ef51ff473607bd60408b1`

```dockerfile
```

-	Layers:
	-	`sha256:0558e1beb895c5631840e7f9cdc870aece52f165285a0db85baab88ffb3578d9`  
		Last Modified: Wed, 09 Apr 2025 02:16:07 GMT  
		Size: 23.7 MB (23721176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c955dfa67de3fc24d7d948c5a54362876c9f6d9b3317cf3a6160053b424a4d`  
		Last Modified: Wed, 09 Apr 2025 02:16:06 GMT  
		Size: 17.1 KB (17124 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2c9bc845b2e32ac28aea3c87a434a0e0a003d3121df0a3c7a292d9f6a3a36a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260106494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1eb46fb86bc04f694d3c32d991a6d78eb43d4cf3101280616e02762cc4bf353`
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

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:d3cd64e42592e0e7ce725ceccc8192b25dcfc56eb1b5cdb1d00f334849b6ffac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23751636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7b91c77dae12c4d830848562854e2221d6363f130b7995b6321dcb6d9fb6c`

```dockerfile
```

-	Layers:
	-	`sha256:62d7fe04ef80474d978763c35f0eec010b16a3db7a78fef0930391e2b0b62cf6`  
		Last Modified: Wed, 09 Apr 2025 15:50:13 GMT  
		Size: 23.7 MB (23734375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22c8cddd75c64cc105847d3fae0700a846c44599589251903698b241e95db28`  
		Last Modified: Wed, 09 Apr 2025 15:50:12 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json
