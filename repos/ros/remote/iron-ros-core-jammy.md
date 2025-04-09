## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:e6f605d0f86aaf1e3da8d7a8d618a38cb65ba6ff8183e6d2d63f24a78afa9b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:70d5036081281c33d01b7a397d706c4b22c46ec7359659271ecb59469f24dc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158741608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cfc4cc1935f650cf5db05be31aeb394e8b0d15f829755db45adc5e293bf52a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
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

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:2f7300f6a28bfafc568dc6d4f92e704241cf6bb3dc9f8ef14f7cd7a8d839c8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19242256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccb440c2f41b957fb6f869ec764c58c788fca64854ff84da0fdc34e232a3932`

```dockerfile
```

-	Layers:
	-	`sha256:8512acde24b888671239fd31dbe59d9654128f22ea970edf0167c2be6b521c29`  
		Last Modified: Wed, 09 Apr 2025 01:20:50 GMT  
		Size: 19.2 MB (19225851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e671102472b9cf10097bf426a18c9c5771e38544b7bd98f02c5a6b98c2c0c9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dafb1235408b5776b1cc23ef27fa1d676d03741f826f5e21ef29bcffe52b6185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153997147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997dd26dc1ed64ff82b82216ff9cae31700501be14627e9524440e98f0fbba1d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 09 Mar 2025 12:07:58 GMT
ARG RELEASE
# Sun, 09 Mar 2025 12:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 09 Mar 2025 12:07:58 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 09 Mar 2025 12:07:58 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["/bin/bash"]
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV LC_ALL=C.UTF-8
# Sun, 09 Mar 2025 12:07:58 GMT
ENV ROS_DISTRO=iron
# Sun, 09 Mar 2025 12:07:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sun, 09 Mar 2025 12:07:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sun, 09 Mar 2025 12:07:58 GMT
CMD ["bash"]
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

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:acba8ba5fa9515cf7c16a12e7160010b05ec5be283ad0525aa62426a65656066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19235271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1dc8fbb8858531f0d2a0483c32537ed045f6e5d95e121080f1bc70185e98b8`

```dockerfile
```

-	Layers:
	-	`sha256:90c3859bcd49f030bbcf395f359a1361341c71772e4b253fdd1527231652eefa`  
		Last Modified: Wed, 09 Apr 2025 09:13:00 GMT  
		Size: 19.2 MB (19218726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f523d0f5febf0105d402cb773e5ecbf75c4420ef23aa7e0891bab9aca3ecbf6`  
		Last Modified: Wed, 09 Apr 2025 09:12:59 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json
