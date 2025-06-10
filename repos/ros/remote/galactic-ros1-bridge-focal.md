## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:12819852beb1dc8a77c7b97acc359121bd3dd392b0c28228b63ae23eef58ebbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:ecca8a5fd119a1f0a64f72d211c87797dbf463a3066d272e2761d1fb4a4a4853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.7 MB (524740442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb1fe4ae95e6b8ea4caa2f02f0a5940d623846a7db98d27f3bee14d55a4f020`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=galactic
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253e2d090968ae89743bbc0954bbaff92e4d1cf5edb29f37fb2280091749d623`  
		Last Modified: Mon, 09 Jun 2025 21:39:31 GMT  
		Size: 73.3 MB (73268914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc26cf621e6a72aaa5d3eb0f5a09aee8538a839398139f320377d2a72f53c5d`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 308.6 KB (308610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf544bbac493b95c4a165fc116cd06e7f0b5a0d5f4d33c5badb04d06c596dbf`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d465cf5a0978d969e83313b858f2bf01cb90f173f91ad5a034d3de674974931`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 22.1 MB (22138329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b954ef683d62fc2852ffb3b371c3a5309c6c4eceb36f18fc83970e3ee0dd260e`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 4.0 KB (4044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed0b7dba42feec029c3b9857de60d1cae93757e4a625b55c9209b67245fd602`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5452b5c26559d932e2261ae0c995ca3dfff21bf6b2d3bc658b0e48f06dfd84`  
		Last Modified: Tue, 10 Jun 2025 05:27:52 GMT  
		Size: 268.9 MB (268866483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a63ec30fab27e3e0e2cb88adfcf44b2217c9b701d6dc71bdaead55823c3be3d`  
		Last Modified: Mon, 09 Jun 2025 21:46:06 GMT  
		Size: 16.3 MB (16327804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a309ba382fb3dfbf713287041481766354e04b25ca4130fd3245f7f3b49ee5b`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros1-bridge-focal` - unknown; unknown

```console
$ docker pull ros@sha256:3327e7e1f8e07589ce6bbc2c36ac122e0caf05301cc5d9dab5cc54f0315446ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42214401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e119bc78c96b691212dc4ae01dfd355ab9267962ad5fb817be375764ef2c4a`

```dockerfile
```

-	Layers:
	-	`sha256:f62b0bf5b9d055031e1730803d37329f3f4e0d34cbb9863e659b79b91c910764`  
		Last Modified: Mon, 09 Jun 2025 22:18:14 GMT  
		Size: 42.2 MB (42186408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26dccc8caab279b52f11d6667419651f69b0e8e60e18d8022844d116891c8361`  
		Last Modified: Mon, 09 Jun 2025 22:18:15 GMT  
		Size: 28.0 KB (27993 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34eabc2c6e2c8426a5ee96cd3ed5ad12c3a811276089e013384fdcb09337ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.1 MB (509116232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef4607a6ff1348f28869194675d40447af6ada82df0dbafb155e5c2fd63163b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=galactic
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5acbcd197ca2dd8f85a827ba1ed6820e86c136f1ab4985faaf3bf8cbfa5a739`  
		Last Modified: Mon, 09 Jun 2025 21:42:36 GMT  
		Size: 67.6 MB (67617373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208649ea3be9f05fa2e17c11294e68dc52f05a0923235b10ca3df0213eec0efa`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 308.6 KB (308607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d142d51b07449e8ce86f0d2de6671d5b67a4d18fc5fc90600f4e3e432b3ae4`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e400c2e79021db0693711a8489954b121a4d0785902a1f433ed75e65ffefa`  
		Last Modified: Mon, 09 Jun 2025 21:42:35 GMT  
		Size: 21.5 MB (21481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fba43c0e277a98c13c0ecea35c9eedaa63f8a2f263e674cdf2a6d22f24e506`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 4.0 KB (4049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a7e0e2dfb57d918aa4bfedaf0abc94868d9b34bc669b577cf2f0ff6cd7f98`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01256842ea5c742a75d0e3e54d342c3864a54dd084f70815aef4e91c423da4c`  
		Last Modified: Tue, 10 Jun 2025 11:55:42 GMT  
		Size: 266.1 MB (266089651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc8f12c340362f1e3bf27d871896d0b2b603ddf1365a5c2fa4df695e1ac6c7d`  
		Last Modified: Mon, 09 Jun 2025 21:55:26 GMT  
		Size: 15.8 MB (15846612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7180df42ee70eb2a1d4aaa73a06cc909ee5be98932ba27865712ff396f5991f`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros1-bridge-focal` - unknown; unknown

```console
$ docker pull ros@sha256:ce3a5df97bd35ed5e3c71064e07f0e65fbb601e03f13d6d8082b47e8838eab75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42109690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71f45fd34ed072a79d0e1f99957aba4b5cf133204971195936510556af7020a`

```dockerfile
```

-	Layers:
	-	`sha256:127524945f7611120269313c5bd8ff9092024b269137dad0533ab9d9f6ca9773`  
		Last Modified: Mon, 09 Jun 2025 22:18:57 GMT  
		Size: 42.1 MB (42081557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14df5383ee125710147bc37871b35a2aef6dcb54368898d466bfa52561e709f`  
		Last Modified: Mon, 09 Jun 2025 22:18:58 GMT  
		Size: 28.1 KB (28133 bytes)  
		MIME: application/vnd.in-toto+json
