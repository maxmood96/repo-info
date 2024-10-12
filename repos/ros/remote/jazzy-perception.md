## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:d3b0c6a7288c6cad566f1e4292a0cb2716b7a144c764ba0fa60236f6f1ab9857
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:f4345909853d5ee92b9885ee3785ae3f79f451acb11f8fb6e1af3099aea47493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.6 MB (622553753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57faa2a134be7f82ab1b1bf8ec11e70eb0f1804de730a53bd534ba2194a50d3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8482975072cd0a0d630920c4c872f2d5e88cc212cff096177260ff1006f883b`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 683.7 KB (683706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c40938900c81ecdae1d6f62b49e2175c396aa4f3255e9c6c32b634364e57cc6`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 3.6 MB (3560128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a37febe7812efd5687665ec7fe420688d4464e02b2f3376e442cc1e50f9014`  
		Last Modified: Sat, 12 Oct 2024 00:01:33 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cf892f7e024165b3c3b94213d3c171e01212fbfb113a13574bf1609dba11b0`  
		Last Modified: Sat, 12 Oct 2024 00:01:33 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d112f720c4670f7c99793a7838a37ee1515ab0394ddf57e49becd1c4204f560`  
		Last Modified: Sat, 12 Oct 2024 00:01:36 GMT  
		Size: 122.7 MB (122664569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b8a934f13c77b28bc4fd03f6150d43bf257620c525384558ccf1ea3b14f08e`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cea74593c90939ba3b8c0a137933189d8684ceb415da4003de0dff394cf310a`  
		Last Modified: Sat, 12 Oct 2024 00:57:11 GMT  
		Size: 114.1 MB (114131892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e41d6636b6aef9f25d96f0c090992a11bbe05acde5a71259f58da412deda7f`  
		Last Modified: Sat, 12 Oct 2024 00:57:09 GMT  
		Size: 335.4 KB (335382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2133898faf909aa255ccc404d9ec95e8697f9d5d5b86f9b5812c62e6b5e9e36`  
		Last Modified: Sat, 12 Oct 2024 00:57:09 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a0f69de29ef4eb4db6bc4ecd98e621b3b4c24120a6137747651d2dabb7146b`  
		Last Modified: Sat, 12 Oct 2024 00:57:10 GMT  
		Size: 27.5 MB (27530386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ecc83c8d616e37933dd6692418e2a59d71814b64223b43c5fa953c6cb22272`  
		Last Modified: Sat, 12 Oct 2024 01:57:22 GMT  
		Size: 323.9 MB (323892328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:451ba7eb92f7702b802b68f5158eaea193a71218230ea5c7ab57885e9e0915d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42100563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b4ad18a2460c1b2ecc1053d8d454ab07fdfc5c50cf7289787fcb28c8082da0`

```dockerfile
```

-	Layers:
	-	`sha256:ab187003d42812c20cca1d7044b7aaa610d39bcaa983d37ac6230e4e59c9ea08`  
		Last Modified: Sat, 12 Oct 2024 01:57:16 GMT  
		Size: 42.1 MB (42090871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3253fab938194db90261b311aa9ca75152407048d762839f0b44c99cd3b414`  
		Last Modified: Sat, 12 Oct 2024 01:57:14 GMT  
		Size: 9.7 KB (9692 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8e1543425cf3dd9bfb168bd5f45efb5175090ac517984103a4de3975b2634ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.6 MB (565594042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ce680d9d1d81e144b2ec1d303aeb683a27df1d7b02f3b4c34417a624c32791`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:dec397e53698aeaaac6929ffd3e7a4c83430d729be6d0dabc2154a31ba33c4d0`  
		Last Modified: Wed, 02 Oct 2024 03:39:15 GMT  
		Size: 117.5 MB (117467950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab30a000a8aeb4fa03a68aafc5862185a9eafb5975c9b61fd1efbe4bedf6806`  
		Last Modified: Wed, 02 Oct 2024 03:39:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5aa0a132c4003f4ae2b3d4324d3f7acfbd85536a298ece06ce28db7d00fb4b`  
		Last Modified: Wed, 02 Oct 2024 06:08:30 GMT  
		Size: 111.0 MB (110969729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041b3a94a7169dfe19b36fa80bb80f975ca63b83594e3ab50324156d2b091488`  
		Last Modified: Wed, 02 Oct 2024 06:08:27 GMT  
		Size: 332.4 KB (332363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4382ecf474c72e5b06d68f1b040c39db4d0c63a38adeb1ffe67b52eccf66a7ab`  
		Last Modified: Wed, 02 Oct 2024 06:08:27 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f6c3c877cf872c2044c21ea4936d71066c2afb3dfeb89791e03a96b97e72e3`  
		Last Modified: Wed, 02 Oct 2024 06:08:28 GMT  
		Size: 26.7 MB (26681092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109cff0d6224896696cc017c7a585e10751301339a20704b44ce215eb9dce379`  
		Last Modified: Wed, 02 Oct 2024 07:43:01 GMT  
		Size: 277.0 MB (277010361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:0b0edecf6396a495703de8549501b920835539373ab057239afec516a310e174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42092288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21245f15364a5b4d6828dad6b0d775967670a59153b1221aae88ca7913a77f87`

```dockerfile
```

-	Layers:
	-	`sha256:f42a2af2ce8c56086ae724410340957951197cd208f8070e2654e9dd908b2c14`  
		Last Modified: Wed, 02 Oct 2024 07:42:54 GMT  
		Size: 42.1 MB (42082549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81541b233b9d830e0d64edf11df3a736d35274ed31b3ed122d8adb8259083891`  
		Last Modified: Wed, 02 Oct 2024 07:42:53 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json
