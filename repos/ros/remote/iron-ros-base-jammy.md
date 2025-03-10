## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:670790c14b741d613262d4829bd7afd84b327198cfff742e9fc44c8f36f52cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:9f88e27bd63620ea343fc50d57eda91b8585425a9959a8c6ac95a9c982c802a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275222161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de6265c8ca8d0158f95ba058d3c564d89ec26ebf1b2c2ae4edb05f364b250db`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3462f71d2a0e18954d5184197e3d81efd3f0f9532354e4efe8a9c00e89b52f9d`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 1.2 MB (1208107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613b3bdd3f675c9e6f115690c98f70841a8d5409c2abca2142578b657f0fdafe`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 3.6 MB (3625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c84f42f76f81695686241b905d92e4291c9c1f2e464b66234a989764d3ff2f6`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f679410b03e667d0a75866f5f27e525633bfd06e12beab159454064db254c8b2`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9ddb9e9f15efe8ba457c6acec0d3f45b8e95c55dd3ce4eb51a949a9d1c1ea2`  
		Last Modified: Mon, 10 Mar 2025 18:13:41 GMT  
		Size: 131.8 MB (131807751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65600ace7adaf01c69182fded1b02b1ddb5154b6e699eca14753a650c912b5`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60391d4a0a6e2a93edbb62bac36e015bea0682e45fca645e4f591ca9957cef4e`  
		Last Modified: Mon, 10 Mar 2025 19:12:09 GMT  
		Size: 85.0 MB (84977124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569c5e1d9be8c2cd97f0730c37bad04cf50abf80d3775d9ef9805050600a5cd`  
		Last Modified: Mon, 10 Mar 2025 19:12:07 GMT  
		Size: 325.7 KB (325735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36c4817e53bdbebd33189fe48a8bc6cad63f5659a0c32f87370e186df06ccea`  
		Last Modified: Mon, 10 Mar 2025 19:12:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171da437077181109566035cc20b251d499221e473ad73e504373419a4fbd81`  
		Last Modified: Mon, 10 Mar 2025 19:12:08 GMT  
		Size: 23.7 MB (23735840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4c9736a424effc8717786aea9b88633fc856ced43c1dd29bb182c576f0f8db3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23736916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c3791a0c2465cd07f521867c4ba39bb7edd0a3f6ba6072240c93d3bd142a8b`

```dockerfile
```

-	Layers:
	-	`sha256:24e862e78b232cc5f9feee9dc6545f91189517d64f3e1711a17114f889090e59`  
		Last Modified: Mon, 10 Mar 2025 19:12:08 GMT  
		Size: 23.7 MB (23719792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:085bfc6698640ad6fc36d06a8609b90e9d756c58a6ea501920e09e3ed345e0e6`  
		Last Modified: Mon, 10 Mar 2025 19:12:07 GMT  
		Size: 17.1 KB (17124 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b21790c30dc2b3df2df35ecab30ccfda0feb3db0568d3b4fe277c760797b595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266285834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58a57dd9976f37e2cb35e44d1245dc96e18677e856bc9f99ce6069445e29b55`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1926f36c9b7b151d496c801225ee7599eb5a8b9b724136c3f5e16b117476669d`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 1.2 MB (1208081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6a4a0853d9c07e7a7b7e748902799150df963c6d6c838f9689a1221332395`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 3.6 MB (3596329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d7b8158f3e4d0bc00f0b83b4f7652632ca53aa97593b50614e361a8057b00`  
		Last Modified: Mon, 10 Mar 2025 18:23:23 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95bfa72cbcd78f679175ba71dd1855fc3b7d01686c288428c1ad9a99e928d5`  
		Last Modified: Mon, 10 Mar 2025 18:23:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad630b2a2b3a1b904d5d02d598bffc5bf6b3a0f69e400bc074b2aab1de0843`  
		Last Modified: Mon, 10 Mar 2025 18:23:28 GMT  
		Size: 128.0 MB (128007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18262b00390f040cf294eaa509d4f779a9ffbf41db0b492fe510f0f29a3f3e4c`  
		Last Modified: Mon, 10 Mar 2025 18:23:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5c7877c93243b37cf8b45f86ec8b6290502659cbe29af959c30149f5c60a06`  
		Last Modified: Mon, 10 Mar 2025 19:16:04 GMT  
		Size: 82.7 MB (82654646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a812bd506442907c24e01b27b154cd30e8a55e68af94b0fc14284e66b5e308`  
		Last Modified: Mon, 10 Mar 2025 19:15:49 GMT  
		Size: 325.7 KB (325737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68ac77cafd0228867e12f7999aa66b727821f31bae2a8832b99adfddc8294e`  
		Last Modified: Mon, 10 Mar 2025 19:15:49 GMT  
		Size: 2.4 KB (2422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a279769da580b8f51b38b6159e86548d6be6d076b0f43cfd7b70e9f4984c2`  
		Last Modified: Mon, 10 Mar 2025 19:15:51 GMT  
		Size: 23.1 MB (23128942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4844fe67030386da7e868f3af41b046a452fdef2a2948cb4d2334f3201f8dc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23750252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f74b938aa8327c87b8fd96993da47ce66ba73a5732612c40e8868e6002d809`

```dockerfile
```

-	Layers:
	-	`sha256:c3b99d29648e2ca021802fe5bb7bc99c95bcedaadc60b1c82387aed0b5287c14`  
		Last Modified: Mon, 10 Mar 2025 19:15:50 GMT  
		Size: 23.7 MB (23732991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec515de742c44810bd4a2c36a4ee971bbe29d5633e9dd89568135c9bc604229`  
		Last Modified: Mon, 10 Mar 2025 19:15:49 GMT  
		Size: 17.3 KB (17261 bytes)  
		MIME: application/vnd.in-toto+json
