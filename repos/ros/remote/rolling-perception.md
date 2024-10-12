## `ros:rolling-perception`

```console
$ docker pull ros@sha256:b46a9a4f11514fb9bd36e189f941e1755be80d898fd190d1120f6f715b3dc9c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:ff46c54ac4812f80e88478c5eb71a895020620a5356e61768400df35249c2d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622464466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e9c9f0671e81fb9f1be9015a80e96ca64e335fe18a06081d630cd2518dda09`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450d3cec92d952ac282860d51dd456a0a7f8291e239c707abe0e1be191ca1`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 683.7 KB (683703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6fda2b3a1f9bc93f10e32c59c206e893f4171f3f780376252b1d015e775e7f`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 3.6 MB (3560091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a811bdfc164a2919f11f77a0d3956e6eaa0616b3872a5281a02f3aa2c2582575`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d525325ea8e09d24717475bc7ebba7d15803e4cbb329b673a6a9305f7d542e`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd192ce0803868a565ccd85257480e827e75a1250defbfed757fb9fa479b2d33`  
		Last Modified: Sat, 12 Oct 2024 00:02:10 GMT  
		Size: 122.7 MB (122667784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ff71b488639f9ffe665466acdbe25b20fb1a21143ebd4c9a99eb42953bbe7b`  
		Last Modified: Sat, 12 Oct 2024 00:02:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0105f2effcfe2e7fb58999ca849b96403c60b0340db438bb40e91166bf5ea502`  
		Last Modified: Sat, 12 Oct 2024 00:57:07 GMT  
		Size: 114.1 MB (114131978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5863e4a247597a9d4c398752759faf63356ab025ac291afe06f464535a0c101`  
		Last Modified: Sat, 12 Oct 2024 00:57:04 GMT  
		Size: 324.0 KB (323959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d0ecfb5a5283ee58e13dbecf4f18f432bbb51c2e6a8202c3fa21e3d3166b3c`  
		Last Modified: Sat, 12 Oct 2024 00:57:04 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6029ca4b9ca247c94112615ff3f887a5ce5625f93981b6d9eeb768f605bee6b`  
		Last Modified: Sat, 12 Oct 2024 00:57:05 GMT  
		Size: 27.5 MB (27533112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21ab92f1f0452511d58ffe8fe3474aba86e35a8bdce2822d70279442274bc68`  
		Last Modified: Sat, 12 Oct 2024 01:57:10 GMT  
		Size: 323.8 MB (323808477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:59874938500f64e574e36aa6d1da753b09418172af0386dd2a09f8ec79cf3c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42145301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808f5d7d75d99c6ca81b50166f5f773b97f81d12543d7c15077f0fe8ed84b443`

```dockerfile
```

-	Layers:
	-	`sha256:e7823cafbe87184cce52828429677e70881b4cb902197fe6d242a059541edf13`  
		Last Modified: Sat, 12 Oct 2024 01:57:07 GMT  
		Size: 42.1 MB (42135587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4763899af6b8b6656b0d4fe67a94771857cfddb02d58620bd38448d67173277`  
		Last Modified: Sat, 12 Oct 2024 01:57:06 GMT  
		Size: 9.7 KB (9714 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:20e76a220322715517981080fee65cdd490b29b208ff7a85f212827a27407e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.6 MB (565575616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94b936d82cac70d4de6b25a5c409f7a9d15df891b7a45b7a0d7243db6955f3a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729a8513c4ec86780d3d7e8c0d22c4343de25f46d9491c10e38b667b193a52a`  
		Last Modified: Wed, 02 Oct 2024 03:39:11 GMT  
		Size: 683.4 KB (683440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c31f126aab317c208659fa46d07187c05e1d5b12a65a384ba2874f4712c91d6`  
		Last Modified: Wed, 02 Oct 2024 03:39:11 GMT  
		Size: 3.6 MB (3558765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eee2d177bb84dcf907f22436e3fa6e2627496b478315a511ae8595076b8573b`  
		Last Modified: Wed, 02 Oct 2024 03:39:10 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a29dab60a180dac66fb5e855684cdc85b3ed77b9504812b2ec597b9c623242`  
		Last Modified: Wed, 02 Oct 2024 03:39:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0420697c0d4d459eed826f21a285af2cdab39729a3af20e586ae6ec93e3a5e`  
		Last Modified: Wed, 02 Oct 2024 03:40:40 GMT  
		Size: 117.5 MB (117475104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcc451f806caf001c7370e241898a5b972e98108fdb21e0b5a727f0f38643db`  
		Last Modified: Wed, 02 Oct 2024 03:40:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f8a4f55897eea800d38351218d0e2e6c664b30b0d25991c5a2e330420cbec6`  
		Last Modified: Wed, 02 Oct 2024 06:10:19 GMT  
		Size: 111.0 MB (110969214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a60ff2cdd3f422d1dcc99ca25637a97954cbe329c4da1950d9512111c7e4d2`  
		Last Modified: Wed, 02 Oct 2024 06:10:16 GMT  
		Size: 322.6 KB (322636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3e98785aec8b4135098102e2b9595b11343d0073f8b9cb17eb11a401dda4ec`  
		Last Modified: Wed, 02 Oct 2024 06:10:16 GMT  
		Size: 2.4 KB (2427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174862ae8973943e788bdcc435acfd8ba1165c034cb680f161493958deaa9e52`  
		Last Modified: Wed, 02 Oct 2024 06:10:17 GMT  
		Size: 26.7 MB (26684154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2749aab14d8cbace1558fbf0a64fe903adae38a90050b21e7a013982b75424ad`  
		Last Modified: Wed, 02 Oct 2024 07:46:09 GMT  
		Size: 277.0 MB (276991979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:d1432e8c5691a14ce840a03eefaf40c3b29030958f1ca77f537ae7778b3c8f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42137026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10040e8897922e38996bdc29a86290ee0ece7051208755ce46a89924bff67ace`

```dockerfile
```

-	Layers:
	-	`sha256:5966705d6f4932db58ee0927f4e50c5d186fd0451bdb1abe8444b011f688aa90`  
		Last Modified: Wed, 02 Oct 2024 07:46:03 GMT  
		Size: 42.1 MB (42127265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89bceebb7a8f48c438f09afa38527b295c619ac7d9899fa5d2bdc94fe434ca9`  
		Last Modified: Wed, 02 Oct 2024 07:46:01 GMT  
		Size: 9.8 KB (9761 bytes)  
		MIME: application/vnd.in-toto+json
