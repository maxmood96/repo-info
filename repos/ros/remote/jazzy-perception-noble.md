## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:0a86cf2d29ff8b2d02d0b4878f14ee53f44ed5d884499679aaa13d2734e1cda9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:9a7fb15d6ca96cd3e95971740210d189874bf881bc782e80cbf17cbbe6adb6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622535782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88633ff5b437c437813d8123b940a66ebc64be14b4d88a9033b37c78eed37dd3`
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
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
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
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d98e5d832889da78d091b7b861c09171158c062c96ed2f4cc057acfec4fea82`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 683.2 KB (683205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c1f85e99a383d2060f5d0b7141691f023435e8a18e77dfd0f5e0318c822b3c`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 3.6 MB (3559586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3522cde17d79df8e8d1346725f69262e57ee7565b36cac340fb2d1605f806b`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91574f15f3561877a9a4eb13022ac04fedea9164ba97e025a7bdffbdcbd3d1b2`  
		Last Modified: Wed, 02 Oct 2024 01:59:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2845596bdf819e253ca9ae268548c57c7d67a92182690baa3189ce6803fc74`  
		Last Modified: Wed, 02 Oct 2024 01:59:17 GMT  
		Size: 122.6 MB (122645974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabf54d65021ba841e554915353f0eab36fe9e3dc62cd759a0a8f8221053badd`  
		Last Modified: Wed, 02 Oct 2024 01:59:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb757b36fdcc786b47eed6ba34c48eda7e9214119e26ff175c13e8a4c615dfec`  
		Last Modified: Wed, 02 Oct 2024 03:00:05 GMT  
		Size: 114.1 MB (114130038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f48b5fa6486947fb0f5f755c039b1e6e9adad5efeff41c3deb0847889130a62`  
		Last Modified: Wed, 02 Oct 2024 03:00:02 GMT  
		Size: 332.4 KB (332364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54f2cda517a1eac2d6d85a7041c56129c1b293231654e7ac708b6930c1edee8`  
		Last Modified: Wed, 02 Oct 2024 03:00:03 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728f1a6f4fa7898dd0da5a35f9b60124b8cb4162621ac1b93ca7d825c1859746`  
		Last Modified: Wed, 02 Oct 2024 03:00:03 GMT  
		Size: 27.5 MB (27530292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071d20ebd8942cf16acca76204cb81776100822d1a35ba4ab5615609acb6310c`  
		Last Modified: Wed, 02 Oct 2024 03:59:42 GMT  
		Size: 323.9 MB (323899560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:82092e5e6ec936a31c78f8f47a046bb9cd92211d829ab1782a14448ccb4bf8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42094115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa9521b450ca7b33b0db8bc09c6b5990b62304d217561cdeb8f054295f0e3f6`

```dockerfile
```

-	Layers:
	-	`sha256:7df8efed2e71a8b44909580820f79e58f969e8f3942ba4a98402d39860c88f85`  
		Last Modified: Wed, 02 Oct 2024 03:59:39 GMT  
		Size: 42.1 MB (42084456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b199ba27f5fb4b1e40b39091e1d2b3ff21a0c02fd745a5d262e46cf7b3c896a`  
		Last Modified: Wed, 02 Oct 2024 03:59:38 GMT  
		Size: 9.7 KB (9659 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

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

### `ros:jazzy-perception-noble` - unknown; unknown

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
