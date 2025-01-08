## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:14d99306d540fa6ad8f6669fd9faac1ed927bf0d640381f64271724c3f226f80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:66cb86aaf7310984367fead817aea9bddf2321bce45315192f1f73334b529904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298713910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bb61428e300e7291067a2020bdf9abf336e35ae91748786c87612ab4eb19d1`
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
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Wed, 08 Jan 2025 01:47:07 GMT  
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

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0c39f966b631c97b04ed5352f01a766290df845b742174648646d2d29f9e95f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23880764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63a020862acd213f2413889262df93f7a25f8449cf4037f5ffd1e003704b906`

```dockerfile
```

-	Layers:
	-	`sha256:a0fc534526efa5c13efdf4825b0d4a3ae017c79f940aa3516ef9c57bc545802c`  
		Last Modified: Tue, 03 Dec 2024 03:25:06 GMT  
		Size: 23.9 MB (23863335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acb4873f2e65e2c410ef9a36b8ed4768ce64c79e577dc9c6b837992534d8fc7`  
		Last Modified: Tue, 03 Dec 2024 03:25:06 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:50d69360783044a3c19d980a2586135f963261a2bd2e3da311024bb95b946d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288678258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf5c5ee507fa1678da8f1cad3209e8eeb7177bcd7b0dbd62dd83ff13cfe1039`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Wed, 08 Jan 2025 03:22:49 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828cafb5606bfc377030b11684ade4e9ef094c5c8866214772783aeefc65dd3e`  
		Size: 684.2 KB (684168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c673bfa5b508b4c5473b5d450e971cdb23a088fdd04c3bc04bc7016a57396a`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 3.6 MB (3559491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75b4ec669cbefd2d68a727cdba4a382b80cd85f1930c4c17ea0f72808c33af2`  
		Last Modified: Tue, 03 Dec 2024 10:21:25 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb025d30ba4de809090f9a665f12e338cb143fc5b85c065932d10e06f6d155a`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b494426cf0020c43838c91deb89a9ce6da60bcac380a766a5a3103053fc4a0de`  
		Last Modified: Tue, 03 Dec 2024 10:21:30 GMT  
		Size: 117.5 MB (117505391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c8974010aba9f0fb6ac664cee0cae14553b8820fc0de89028fb2488ebf0691`  
		Last Modified: Tue, 03 Dec 2024 10:21:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2b101ee11fe97dea9fb6db087d7e03417e50d6c827fa3b0081c59a7bfa4f9e`  
		Last Modified: Tue, 03 Dec 2024 14:37:53 GMT  
		Size: 111.0 MB (111007739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3cf1612d9d1fb2cd20d97d63dbb42923046c3bb1f7696caaff67cbcf8fc278`  
		Last Modified: Tue, 03 Dec 2024 14:37:50 GMT  
		Size: 342.4 KB (342353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6222ec72157e7abcd4ed22919ea0768fce7e1a2eacd878c2be5ba94c39cbc4`  
		Last Modified: Tue, 03 Dec 2024 14:37:50 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4564659199e87c69ffefaf3d047ec489aa6c03024ac1c21c3af3d9d92978bb1`  
		Last Modified: Tue, 03 Dec 2024 14:37:51 GMT  
		Size: 26.7 MB (26681514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b8472536f3ad366ed0de26b4a07718010d0c531a2a9314fa2e5e87416209c288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23903489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878b2bf9dc7405a1ca457c4a0cebaf1f6347da5b95f4d0481f64604fe8ce3f2d`

```dockerfile
```

-	Layers:
	-	`sha256:d143fc48534527d4b52d19d90b1eb2e299e6bd26d3cccf5253d1a9f86cd11661`  
		Last Modified: Tue, 03 Dec 2024 14:37:51 GMT  
		Size: 23.9 MB (23885912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6352b919778348e72928b0aaf7853e1ed552213db004c5e67a2be60d5514f75`  
		Last Modified: Tue, 03 Dec 2024 14:37:49 GMT  
		Size: 17.6 KB (17577 bytes)  
		MIME: application/vnd.in-toto+json
