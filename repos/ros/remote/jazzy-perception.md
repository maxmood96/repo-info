## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:a624559a50641165c65d8f1fae9890232381f51fa7f40365cca0d1a0d4daf612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:dd9aa8a30580ae18bc7fe5130c112d7f14a396c267f94f4e63067759a9fe743e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1036859926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684a77547bf02d57dfb990db1eb50bf05a8ec8dff7cb0b40456184813ab319f1`
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
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb9b5148ae557dba975bb84acfb09e3d5ecb3b30a6664c1b158038437ff864`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 684.0 KB (684039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec79256506a8ed2c76d26fb5263d09a717a558dbad31f97bc79a412b71bc3d5`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 3.6 MB (3560620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa924df05280940cb19b9e74ac5885a2f67622eab697a7433b583a120694239`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f3e08353bf8f53937fa7168cbad7d39df3214474bc9b07557880d6ff63b08`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01218c18dd3d57f0fd398836513b6b50fbe554ff4b460941357ebfb7289972`  
		Last Modified: Tue, 03 Dec 2024 02:17:25 GMT  
		Size: 122.7 MB (122691998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a4d000285c3d2a81b20a96c50372bd1cde9b88f7611ccaa417fea7a3c85459`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17292e7638873b8383a8077c14d0b55cd66f74bc5428ac9cbfb5d353da8c8423`  
		Last Modified: Tue, 03 Dec 2024 03:25:07 GMT  
		Size: 114.1 MB (114147298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d15681af803fdb5522376544c8684b41f96b7302f381c439f144544ecee9777`  
		Last Modified: Tue, 03 Dec 2024 03:25:06 GMT  
		Size: 342.4 KB (342357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28e771bfd74e3604730bf79016216276d7f5a0ffa622e23f687b33b7f0baacc`  
		Last Modified: Tue, 03 Dec 2024 03:25:06 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401ff9aff2459f1c5d9ec5957ad0af8f8e54696b7d93bda3cdae79703db2adc5`  
		Last Modified: Tue, 03 Dec 2024 03:25:06 GMT  
		Size: 27.5 MB (27530745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3afa5dbc2b085fe55b153f9297601b3ed264ab949e6ea652a2ccdc92bf548`  
		Last Modified: Tue, 03 Dec 2024 04:35:36 GMT  
		Size: 738.1 MB (738146016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:2c6b6e47d90a19f47ac25ef635505c01992e8d334e82f6ebe0c8fb096b72b827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59646540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8014053ddfcadb0cdf53481241b72c66edcf62eac12f7e8945fc7464c7c1da`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e4c78f159b0468bcec82e8c3034a485a0b90e77cd6b7690bd86f79265dfb0`  
		Last Modified: Tue, 03 Dec 2024 04:35:26 GMT  
		Size: 59.6 MB (59636853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3930749044ec8d702df96329c2e5639642de11118e33736b69fba4b12655a2fc`  
		Last Modified: Tue, 03 Dec 2024 04:35:25 GMT  
		Size: 9.7 KB (9687 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:95cf72b87eb1cf2c85644e737a7b17eacb0e6490e2af7d75deabfcb13e1c3fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565693556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54084f47ee5d450322d2546e195cd60b778be0818340b601335c7de0c2c1258`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81328307e6050d58a3786b0d8d4e0e280336fcbe5e12ed33eafac0e62f39b3c6`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 684.0 KB (683965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dc71d0f9b404e0afdeede800f6310ebab3be587e6a707bfd42f238d09438d`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88656ab2aa8b4c276fa4728d3578e2aa637b914c7cc65e1016f5861ad78de29a`  
		Last Modified: Sat, 16 Nov 2024 03:40:47 GMT  
		Size: 117.5 MB (117510931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c462529133b7263830c6dade28a2ef5fae040e0cc3fe2b0b11853d1315966b0a`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809581c77d8ab1705a59d94b7dc3d6c54d9fc4137b95a2bd2695ccb27fcbecd5`  
		Last Modified: Sat, 16 Nov 2024 04:48:22 GMT  
		Size: 111.0 MB (111007658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe2d40317b9ee7167e469c991fa79073edc979b155fc50bb204591d0428c5d5`  
		Last Modified: Sat, 16 Nov 2024 04:48:19 GMT  
		Size: 339.0 KB (339046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e216209922a2f6097e8083ac22f18f748b0871b80e539e44486bd980356dd0`  
		Last Modified: Sat, 16 Nov 2024 04:48:19 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d6c35ae1809282e464658df766e60ae5a16dee49516437d9e2bcfbbc95f258`  
		Last Modified: Sat, 16 Nov 2024 04:48:20 GMT  
		Size: 26.7 MB (26681372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42405ae036edd9517d17125181fdbbf9a37447ffec2dbf38e74684d90a26cb1f`  
		Last Modified: Sat, 16 Nov 2024 06:06:23 GMT  
		Size: 277.0 MB (277013865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e52f737d7e2deefa20fbdf4747ea81fb35ffd2b47e689e70755eadc972c08aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42202181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57c8c01aa898179db9af8f00c4f3f543fca55397287bf10d2a340b9ff84b5e0`

```dockerfile
```

-	Layers:
	-	`sha256:fa7fb890fde628ef935e133b1756361e60608f51ee2032b7014116e4aea47c63`  
		Last Modified: Sat, 16 Nov 2024 06:06:17 GMT  
		Size: 42.2 MB (42192413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5bc9ab197ca4a4c0f351283de8c56950b3ea4fa6a98fce9f28b740af548972c`  
		Last Modified: Sat, 16 Nov 2024 06:06:16 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.in-toto+json
