<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:iron`](#rosiron)
-	[`ros:iron-perception`](#rosiron-perception)
-	[`ros:iron-perception-jammy`](#rosiron-perception-jammy)
-	[`ros:iron-ros-base`](#rosiron-ros-base)
-	[`ros:iron-ros-base-jammy`](#rosiron-ros-base-jammy)
-	[`ros:iron-ros-core`](#rosiron-ros-core)
-	[`ros:iron-ros-core-jammy`](#rosiron-ros-core-jammy)
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
-	[`ros:latest`](#roslatest)
-	[`ros:noetic`](#rosnoetic)
-	[`ros:noetic-perception`](#rosnoetic-perception)
-	[`ros:noetic-perception-focal`](#rosnoetic-perception-focal)
-	[`ros:noetic-robot`](#rosnoetic-robot)
-	[`ros:noetic-robot-focal`](#rosnoetic-robot-focal)
-	[`ros:noetic-ros-base`](#rosnoetic-ros-base)
-	[`ros:noetic-ros-base-focal`](#rosnoetic-ros-base-focal)
-	[`ros:noetic-ros-core`](#rosnoetic-ros-core)
-	[`ros:noetic-ros-core-focal`](#rosnoetic-ros-core-focal)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:482ae18aa5d4813dd5c59aee9e4cd830eac94c60587f494e9ff343e6aaf3aba3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:e2bf5d73089ecafac2f14de05e7cbc1b20ab7568185e2011cec508286dcc6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262007961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6987833c468f25c50e4802a0a8fe13182025fd5be69f3fc7f4550d5a5afa89b0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e134650a58527f750ae8240053485a2f137352ecf756235b1e1e6fdb2e58bd5`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 1.2 MB (1214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1e367d2c4dd5ee27bf7de101f8a5375cd32e0c78aaf62c8575c0e6b6b6d85`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 3.6 MB (3624633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f588ed24bdf5fad71de96bbb5b7fc275fda37756cef0ed01956e6f35ebb4a`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6852c2b80f647da68213c7078cdb71485445219e260e3465e6f38a0bb1ad627`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d91075c9ed31da02a9b4c33814db9286e4b1b259d48c139ab0c58bb41ea233`  
		Last Modified: Tue, 17 Sep 2024 01:01:11 GMT  
		Size: 106.5 MB (106531769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a8272a83deb81f823b1cb3bf041f95c7d711601610c50de02837a1fab738`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a0131e0c73a7071017bbc743e74591d78261e5fb886e39f5f89da54721d7a`  
		Last Modified: Tue, 17 Sep 2024 01:58:30 GMT  
		Size: 97.9 MB (97933888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319799ae1afd30876970d7bb2b3200269a4a1d49c448e6183e6ad42d0439b017`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92d07b72e749b4d1f35a36946f6470904304c610e8208688ab5bd132580e74e`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82b3fc9b8259a2df8418e0bd1c22651c30c4d5d33aefdb144429af07a39515`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.8 MB (22824416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:10163c349a13ba6ae506742ac20d9c43d56817b576158f89a814bb63fadaa8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22690706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c55608b8e01eddea7d327e54582b480f389f8fe8d0b0af572aa4c2ee5d1635`

```dockerfile
```

-	Layers:
	-	`sha256:d587c79cc328a77c3ac363aebc882987b88d872d5daeb13bc9b430dfa5416131`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.7 MB (22673585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6fc7ed6f0445f1c7823fa43bc6979f8f17efd432b5c51f659d218c913a4ead`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 17.1 KB (17121 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b0b9bb05b0dceb08acc0e640c5b1c8a205da350369881d61b4ef42715ee42a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254508441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c385226566a1052d32479d7a991b16d1279890a907e34927be70ced44195517a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f820de24ad6ec8445c6b22cb0048286de3789be116cb819f1632d833f980fe`  
		Last Modified: Tue, 17 Sep 2024 03:02:08 GMT  
		Size: 104.2 MB (104248768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45581323c34fb26086d975e1aad2476e027d2d6dbc7fbc43a7ba8a057463d6`  
		Last Modified: Tue, 17 Sep 2024 03:02:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d7fb3f2145a764dae68a91d33961df7d08270335a1149b4c8ec231a7c68ef`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 95.5 MB (95501362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2056cdee121a8f7aba7d544f9dbc2098f1068d24b38c5c380143b5c965aaec9`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaafba2dac67131d8abb8cc1c154deefa1f261c8a6ea45890c38a327ab8ecba`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc16a1d1ac077be73e099a09b28bd4a72f6e448919e903104f9f40a9ccdd13d`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 22.2 MB (22246214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:c33b48de1db8cedf6d472fbd730a05797f1f794fc4e03a6aa5d6e7a43b3adf7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22704104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac92bd6d86e4e2af8b97ae24fc3892fead167be1e92f9193e81e38097fa7866`

```dockerfile
```

-	Layers:
	-	`sha256:b3039f0dbc51e996d27a48ccefcdda069c93560250042546ebf27af7c1a2a6f5`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 22.7 MB (22686610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ec6bbd359a8df0209b028fbf4ea1f665527ca946dd3d7c29d5ae4a41d9e6e9`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:0d171f4423f09921c036a82a13c686a03f71d0ee772bda1c86f362b46465b98e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:48cd640829bc18559948dacac8f63f481acd4ba2b165e66dbce62d3edf733d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.7 MB (953666303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212e16b4ae00372c7148be9c220dc2bde2b53f7b44b9f68aca4297b6886e22bf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e134650a58527f750ae8240053485a2f137352ecf756235b1e1e6fdb2e58bd5`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 1.2 MB (1214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1e367d2c4dd5ee27bf7de101f8a5375cd32e0c78aaf62c8575c0e6b6b6d85`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 3.6 MB (3624633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f588ed24bdf5fad71de96bbb5b7fc275fda37756cef0ed01956e6f35ebb4a`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6852c2b80f647da68213c7078cdb71485445219e260e3465e6f38a0bb1ad627`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d91075c9ed31da02a9b4c33814db9286e4b1b259d48c139ab0c58bb41ea233`  
		Last Modified: Tue, 17 Sep 2024 01:01:11 GMT  
		Size: 106.5 MB (106531769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a8272a83deb81f823b1cb3bf041f95c7d711601610c50de02837a1fab738`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a0131e0c73a7071017bbc743e74591d78261e5fb886e39f5f89da54721d7a`  
		Last Modified: Tue, 17 Sep 2024 01:58:30 GMT  
		Size: 97.9 MB (97933888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319799ae1afd30876970d7bb2b3200269a4a1d49c448e6183e6ad42d0439b017`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92d07b72e749b4d1f35a36946f6470904304c610e8208688ab5bd132580e74e`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82b3fc9b8259a2df8418e0bd1c22651c30c4d5d33aefdb144429af07a39515`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.8 MB (22824416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c540f25eb30966e2453afcf2ec3b9f8d52bbeba0d0c0ce24f2aed05ae32217`  
		Last Modified: Tue, 17 Sep 2024 03:05:08 GMT  
		Size: 691.7 MB (691658342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:70742ceda40e028dd9da998d6d748044bfbd9af39ab2ce403354fbe2b8b5f62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a919e24298a17a44951cf234e173f101bbde9f435e1d30b172dc643241128f`

```dockerfile
```

-	Layers:
	-	`sha256:90179f67e11fda3948a1715b288acc46f431c16f8a3213a17ef880567c4a5c90`  
		Last Modified: Tue, 17 Sep 2024 03:05:00 GMT  
		Size: 57.3 MB (57271103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a8cb8eace79c6f17720bced02d7218d596c83fa9303db4094a4b4e1258d28f`  
		Last Modified: Tue, 17 Sep 2024 03:04:58 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0c889a4cf75531a6c768b58bb77fbd8456601357eb2bac7660a2c489df25c662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914089948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441542988372f2c0b97a3cdd453bb1d905e01d3d9afbe8a8a2566da93226a6c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f820de24ad6ec8445c6b22cb0048286de3789be116cb819f1632d833f980fe`  
		Last Modified: Tue, 17 Sep 2024 03:02:08 GMT  
		Size: 104.2 MB (104248768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45581323c34fb26086d975e1aad2476e027d2d6dbc7fbc43a7ba8a057463d6`  
		Last Modified: Tue, 17 Sep 2024 03:02:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d7fb3f2145a764dae68a91d33961df7d08270335a1149b4c8ec231a7c68ef`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 95.5 MB (95501362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2056cdee121a8f7aba7d544f9dbc2098f1068d24b38c5c380143b5c965aaec9`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaafba2dac67131d8abb8cc1c154deefa1f261c8a6ea45890c38a327ab8ecba`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc16a1d1ac077be73e099a09b28bd4a72f6e448919e903104f9f40a9ccdd13d`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 22.2 MB (22246214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8345062cb5a1abbd168f691c276ca112ca7cbb0cd616074b75569f75fbf22fc`  
		Last Modified: Tue, 17 Sep 2024 07:55:21 GMT  
		Size: 659.6 MB (659581507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:fca4eab27a353e516af1c9bdff8eaa806c8f246c4ff94179c82a219cdc552087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57277343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946504180fcd7de189dc50ba066d98b3027685bea9af3a111d27e3ed35849f2b`

```dockerfile
```

-	Layers:
	-	`sha256:7aee9a0de81444b73a032acb30eeb9cd7e05587924310ed6e8c8e202abd64f78`  
		Last Modified: Tue, 17 Sep 2024 07:55:10 GMT  
		Size: 57.3 MB (57267315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27253494f59cfdec38ca070f76f3af12d4efeb3f6f852f31fd9a0404fc97a911`  
		Last Modified: Tue, 17 Sep 2024 07:55:07 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:0d171f4423f09921c036a82a13c686a03f71d0ee772bda1c86f362b46465b98e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:48cd640829bc18559948dacac8f63f481acd4ba2b165e66dbce62d3edf733d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.7 MB (953666303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212e16b4ae00372c7148be9c220dc2bde2b53f7b44b9f68aca4297b6886e22bf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e134650a58527f750ae8240053485a2f137352ecf756235b1e1e6fdb2e58bd5`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 1.2 MB (1214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1e367d2c4dd5ee27bf7de101f8a5375cd32e0c78aaf62c8575c0e6b6b6d85`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 3.6 MB (3624633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f588ed24bdf5fad71de96bbb5b7fc275fda37756cef0ed01956e6f35ebb4a`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6852c2b80f647da68213c7078cdb71485445219e260e3465e6f38a0bb1ad627`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d91075c9ed31da02a9b4c33814db9286e4b1b259d48c139ab0c58bb41ea233`  
		Last Modified: Tue, 17 Sep 2024 01:01:11 GMT  
		Size: 106.5 MB (106531769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a8272a83deb81f823b1cb3bf041f95c7d711601610c50de02837a1fab738`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a0131e0c73a7071017bbc743e74591d78261e5fb886e39f5f89da54721d7a`  
		Last Modified: Tue, 17 Sep 2024 01:58:30 GMT  
		Size: 97.9 MB (97933888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319799ae1afd30876970d7bb2b3200269a4a1d49c448e6183e6ad42d0439b017`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92d07b72e749b4d1f35a36946f6470904304c610e8208688ab5bd132580e74e`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82b3fc9b8259a2df8418e0bd1c22651c30c4d5d33aefdb144429af07a39515`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.8 MB (22824416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c540f25eb30966e2453afcf2ec3b9f8d52bbeba0d0c0ce24f2aed05ae32217`  
		Last Modified: Tue, 17 Sep 2024 03:05:08 GMT  
		Size: 691.7 MB (691658342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:70742ceda40e028dd9da998d6d748044bfbd9af39ab2ce403354fbe2b8b5f62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a919e24298a17a44951cf234e173f101bbde9f435e1d30b172dc643241128f`

```dockerfile
```

-	Layers:
	-	`sha256:90179f67e11fda3948a1715b288acc46f431c16f8a3213a17ef880567c4a5c90`  
		Last Modified: Tue, 17 Sep 2024 03:05:00 GMT  
		Size: 57.3 MB (57271103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a8cb8eace79c6f17720bced02d7218d596c83fa9303db4094a4b4e1258d28f`  
		Last Modified: Tue, 17 Sep 2024 03:04:58 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0c889a4cf75531a6c768b58bb77fbd8456601357eb2bac7660a2c489df25c662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914089948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441542988372f2c0b97a3cdd453bb1d905e01d3d9afbe8a8a2566da93226a6c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f820de24ad6ec8445c6b22cb0048286de3789be116cb819f1632d833f980fe`  
		Last Modified: Tue, 17 Sep 2024 03:02:08 GMT  
		Size: 104.2 MB (104248768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45581323c34fb26086d975e1aad2476e027d2d6dbc7fbc43a7ba8a057463d6`  
		Last Modified: Tue, 17 Sep 2024 03:02:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d7fb3f2145a764dae68a91d33961df7d08270335a1149b4c8ec231a7c68ef`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 95.5 MB (95501362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2056cdee121a8f7aba7d544f9dbc2098f1068d24b38c5c380143b5c965aaec9`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaafba2dac67131d8abb8cc1c154deefa1f261c8a6ea45890c38a327ab8ecba`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc16a1d1ac077be73e099a09b28bd4a72f6e448919e903104f9f40a9ccdd13d`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 22.2 MB (22246214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8345062cb5a1abbd168f691c276ca112ca7cbb0cd616074b75569f75fbf22fc`  
		Last Modified: Tue, 17 Sep 2024 07:55:21 GMT  
		Size: 659.6 MB (659581507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:fca4eab27a353e516af1c9bdff8eaa806c8f246c4ff94179c82a219cdc552087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57277343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946504180fcd7de189dc50ba066d98b3027685bea9af3a111d27e3ed35849f2b`

```dockerfile
```

-	Layers:
	-	`sha256:7aee9a0de81444b73a032acb30eeb9cd7e05587924310ed6e8c8e202abd64f78`  
		Last Modified: Tue, 17 Sep 2024 07:55:10 GMT  
		Size: 57.3 MB (57267315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27253494f59cfdec38ca070f76f3af12d4efeb3f6f852f31fd9a0404fc97a911`  
		Last Modified: Tue, 17 Sep 2024 07:55:07 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:482ae18aa5d4813dd5c59aee9e4cd830eac94c60587f494e9ff343e6aaf3aba3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e2bf5d73089ecafac2f14de05e7cbc1b20ab7568185e2011cec508286dcc6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262007961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6987833c468f25c50e4802a0a8fe13182025fd5be69f3fc7f4550d5a5afa89b0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e134650a58527f750ae8240053485a2f137352ecf756235b1e1e6fdb2e58bd5`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 1.2 MB (1214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1e367d2c4dd5ee27bf7de101f8a5375cd32e0c78aaf62c8575c0e6b6b6d85`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 3.6 MB (3624633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f588ed24bdf5fad71de96bbb5b7fc275fda37756cef0ed01956e6f35ebb4a`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6852c2b80f647da68213c7078cdb71485445219e260e3465e6f38a0bb1ad627`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d91075c9ed31da02a9b4c33814db9286e4b1b259d48c139ab0c58bb41ea233`  
		Last Modified: Tue, 17 Sep 2024 01:01:11 GMT  
		Size: 106.5 MB (106531769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a8272a83deb81f823b1cb3bf041f95c7d711601610c50de02837a1fab738`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a0131e0c73a7071017bbc743e74591d78261e5fb886e39f5f89da54721d7a`  
		Last Modified: Tue, 17 Sep 2024 01:58:30 GMT  
		Size: 97.9 MB (97933888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319799ae1afd30876970d7bb2b3200269a4a1d49c448e6183e6ad42d0439b017`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92d07b72e749b4d1f35a36946f6470904304c610e8208688ab5bd132580e74e`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82b3fc9b8259a2df8418e0bd1c22651c30c4d5d33aefdb144429af07a39515`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.8 MB (22824416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:10163c349a13ba6ae506742ac20d9c43d56817b576158f89a814bb63fadaa8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22690706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c55608b8e01eddea7d327e54582b480f389f8fe8d0b0af572aa4c2ee5d1635`

```dockerfile
```

-	Layers:
	-	`sha256:d587c79cc328a77c3ac363aebc882987b88d872d5daeb13bc9b430dfa5416131`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.7 MB (22673585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6fc7ed6f0445f1c7823fa43bc6979f8f17efd432b5c51f659d218c913a4ead`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 17.1 KB (17121 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b0b9bb05b0dceb08acc0e640c5b1c8a205da350369881d61b4ef42715ee42a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254508441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c385226566a1052d32479d7a991b16d1279890a907e34927be70ced44195517a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f820de24ad6ec8445c6b22cb0048286de3789be116cb819f1632d833f980fe`  
		Last Modified: Tue, 17 Sep 2024 03:02:08 GMT  
		Size: 104.2 MB (104248768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45581323c34fb26086d975e1aad2476e027d2d6dbc7fbc43a7ba8a057463d6`  
		Last Modified: Tue, 17 Sep 2024 03:02:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d7fb3f2145a764dae68a91d33961df7d08270335a1149b4c8ec231a7c68ef`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 95.5 MB (95501362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2056cdee121a8f7aba7d544f9dbc2098f1068d24b38c5c380143b5c965aaec9`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaafba2dac67131d8abb8cc1c154deefa1f261c8a6ea45890c38a327ab8ecba`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc16a1d1ac077be73e099a09b28bd4a72f6e448919e903104f9f40a9ccdd13d`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 22.2 MB (22246214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:c33b48de1db8cedf6d472fbd730a05797f1f794fc4e03a6aa5d6e7a43b3adf7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22704104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac92bd6d86e4e2af8b97ae24fc3892fead167be1e92f9193e81e38097fa7866`

```dockerfile
```

-	Layers:
	-	`sha256:b3039f0dbc51e996d27a48ccefcdda069c93560250042546ebf27af7c1a2a6f5`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 22.7 MB (22686610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ec6bbd359a8df0209b028fbf4ea1f665527ca946dd3d7c29d5ae4a41d9e6e9`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:482ae18aa5d4813dd5c59aee9e4cd830eac94c60587f494e9ff343e6aaf3aba3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:e2bf5d73089ecafac2f14de05e7cbc1b20ab7568185e2011cec508286dcc6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262007961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6987833c468f25c50e4802a0a8fe13182025fd5be69f3fc7f4550d5a5afa89b0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e134650a58527f750ae8240053485a2f137352ecf756235b1e1e6fdb2e58bd5`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 1.2 MB (1214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1e367d2c4dd5ee27bf7de101f8a5375cd32e0c78aaf62c8575c0e6b6b6d85`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 3.6 MB (3624633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f588ed24bdf5fad71de96bbb5b7fc275fda37756cef0ed01956e6f35ebb4a`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6852c2b80f647da68213c7078cdb71485445219e260e3465e6f38a0bb1ad627`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d91075c9ed31da02a9b4c33814db9286e4b1b259d48c139ab0c58bb41ea233`  
		Last Modified: Tue, 17 Sep 2024 01:01:11 GMT  
		Size: 106.5 MB (106531769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a8272a83deb81f823b1cb3bf041f95c7d711601610c50de02837a1fab738`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a0131e0c73a7071017bbc743e74591d78261e5fb886e39f5f89da54721d7a`  
		Last Modified: Tue, 17 Sep 2024 01:58:30 GMT  
		Size: 97.9 MB (97933888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319799ae1afd30876970d7bb2b3200269a4a1d49c448e6183e6ad42d0439b017`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92d07b72e749b4d1f35a36946f6470904304c610e8208688ab5bd132580e74e`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82b3fc9b8259a2df8418e0bd1c22651c30c4d5d33aefdb144429af07a39515`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.8 MB (22824416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:10163c349a13ba6ae506742ac20d9c43d56817b576158f89a814bb63fadaa8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22690706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c55608b8e01eddea7d327e54582b480f389f8fe8d0b0af572aa4c2ee5d1635`

```dockerfile
```

-	Layers:
	-	`sha256:d587c79cc328a77c3ac363aebc882987b88d872d5daeb13bc9b430dfa5416131`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.7 MB (22673585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6fc7ed6f0445f1c7823fa43bc6979f8f17efd432b5c51f659d218c913a4ead`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 17.1 KB (17121 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b0b9bb05b0dceb08acc0e640c5b1c8a205da350369881d61b4ef42715ee42a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254508441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c385226566a1052d32479d7a991b16d1279890a907e34927be70ced44195517a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f820de24ad6ec8445c6b22cb0048286de3789be116cb819f1632d833f980fe`  
		Last Modified: Tue, 17 Sep 2024 03:02:08 GMT  
		Size: 104.2 MB (104248768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45581323c34fb26086d975e1aad2476e027d2d6dbc7fbc43a7ba8a057463d6`  
		Last Modified: Tue, 17 Sep 2024 03:02:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d7fb3f2145a764dae68a91d33961df7d08270335a1149b4c8ec231a7c68ef`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 95.5 MB (95501362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2056cdee121a8f7aba7d544f9dbc2098f1068d24b38c5c380143b5c965aaec9`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaafba2dac67131d8abb8cc1c154deefa1f261c8a6ea45890c38a327ab8ecba`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc16a1d1ac077be73e099a09b28bd4a72f6e448919e903104f9f40a9ccdd13d`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 22.2 MB (22246214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:c33b48de1db8cedf6d472fbd730a05797f1f794fc4e03a6aa5d6e7a43b3adf7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22704104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac92bd6d86e4e2af8b97ae24fc3892fead167be1e92f9193e81e38097fa7866`

```dockerfile
```

-	Layers:
	-	`sha256:b3039f0dbc51e996d27a48ccefcdda069c93560250042546ebf27af7c1a2a6f5`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 22.7 MB (22686610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ec6bbd359a8df0209b028fbf4ea1f665527ca946dd3d7c29d5ae4a41d9e6e9`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:854e48183c14881767553657ca73602fe7bb5d7f265f744c5ea66ef88bb59955
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:232964417e4e17f95e1820ab2d06091cbc5f5c6df9ca95852f27f448a739b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140909236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceeef97a669e465659805804b47d75e76594c18cd3766fc3697b8ab1b7440cb6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e134650a58527f750ae8240053485a2f137352ecf756235b1e1e6fdb2e58bd5`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 1.2 MB (1214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1e367d2c4dd5ee27bf7de101f8a5375cd32e0c78aaf62c8575c0e6b6b6d85`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 3.6 MB (3624633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f588ed24bdf5fad71de96bbb5b7fc275fda37756cef0ed01956e6f35ebb4a`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6852c2b80f647da68213c7078cdb71485445219e260e3465e6f38a0bb1ad627`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d91075c9ed31da02a9b4c33814db9286e4b1b259d48c139ab0c58bb41ea233`  
		Last Modified: Tue, 17 Sep 2024 01:01:11 GMT  
		Size: 106.5 MB (106531769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a8272a83deb81f823b1cb3bf041f95c7d711601610c50de02837a1fab738`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:97ce29530511890cb56999ab8dedf003a9f2162a83a3ed9df3fb0675fc62e7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16971377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ab7fb9bced199e71b1c15e3de78ac49ee0240ec9d6575286bdd81d9b6205a6`

```dockerfile
```

-	Layers:
	-	`sha256:21f635495a7eb0959a4276cffecb87f1442f0c2597fd9967eddc5fded2a34e68`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 17.0 MB (16955240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6f0d43405e27545633560a2900a5672b98009dd8c0f8b69e33cfceb24b3bac`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fcf959403db41f43241a04d6769904137ef782be53b37848989fbfe89a565378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136420401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0063d8bddd50101426945acc78596ac9b9111c3665c5dbf85573167cb9feda7d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f820de24ad6ec8445c6b22cb0048286de3789be116cb819f1632d833f980fe`  
		Last Modified: Tue, 17 Sep 2024 03:02:08 GMT  
		Size: 104.2 MB (104248768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45581323c34fb26086d975e1aad2476e027d2d6dbc7fbc43a7ba8a057463d6`  
		Last Modified: Tue, 17 Sep 2024 03:02:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ef75ab71240d0df770808cffcb83eded728d33e9d82aa2f3b678778ede3828c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16958382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf539d5577d01ea355e68feed2501941263d8969aa7a7e6db024ac2c5d9597a`

```dockerfile
```

-	Layers:
	-	`sha256:2fea7c4c4f6098cec2387bb94af165227157bb1daf44f578a4c975c2de13bc33`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 16.9 MB (16941969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c77a97039679f8a056f654dea8cd183928e929e140a2ad491ea0ba0028452f`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 16.4 KB (16413 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:854e48183c14881767553657ca73602fe7bb5d7f265f744c5ea66ef88bb59955
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:232964417e4e17f95e1820ab2d06091cbc5f5c6df9ca95852f27f448a739b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140909236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceeef97a669e465659805804b47d75e76594c18cd3766fc3697b8ab1b7440cb6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e134650a58527f750ae8240053485a2f137352ecf756235b1e1e6fdb2e58bd5`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 1.2 MB (1214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1e367d2c4dd5ee27bf7de101f8a5375cd32e0c78aaf62c8575c0e6b6b6d85`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 3.6 MB (3624633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f588ed24bdf5fad71de96bbb5b7fc275fda37756cef0ed01956e6f35ebb4a`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6852c2b80f647da68213c7078cdb71485445219e260e3465e6f38a0bb1ad627`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d91075c9ed31da02a9b4c33814db9286e4b1b259d48c139ab0c58bb41ea233`  
		Last Modified: Tue, 17 Sep 2024 01:01:11 GMT  
		Size: 106.5 MB (106531769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a8272a83deb81f823b1cb3bf041f95c7d711601610c50de02837a1fab738`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:97ce29530511890cb56999ab8dedf003a9f2162a83a3ed9df3fb0675fc62e7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16971377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ab7fb9bced199e71b1c15e3de78ac49ee0240ec9d6575286bdd81d9b6205a6`

```dockerfile
```

-	Layers:
	-	`sha256:21f635495a7eb0959a4276cffecb87f1442f0c2597fd9967eddc5fded2a34e68`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 17.0 MB (16955240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6f0d43405e27545633560a2900a5672b98009dd8c0f8b69e33cfceb24b3bac`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 16.1 KB (16137 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fcf959403db41f43241a04d6769904137ef782be53b37848989fbfe89a565378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136420401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0063d8bddd50101426945acc78596ac9b9111c3665c5dbf85573167cb9feda7d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f820de24ad6ec8445c6b22cb0048286de3789be116cb819f1632d833f980fe`  
		Last Modified: Tue, 17 Sep 2024 03:02:08 GMT  
		Size: 104.2 MB (104248768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45581323c34fb26086d975e1aad2476e027d2d6dbc7fbc43a7ba8a057463d6`  
		Last Modified: Tue, 17 Sep 2024 03:02:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:ef75ab71240d0df770808cffcb83eded728d33e9d82aa2f3b678778ede3828c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16958382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf539d5577d01ea355e68feed2501941263d8969aa7a7e6db024ac2c5d9597a`

```dockerfile
```

-	Layers:
	-	`sha256:2fea7c4c4f6098cec2387bb94af165227157bb1daf44f578a4c975c2de13bc33`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 16.9 MB (16941969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c77a97039679f8a056f654dea8cd183928e929e140a2ad491ea0ba0028452f`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 16.4 KB (16413 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron`

```console
$ docker pull ros@sha256:66bd659365bd1ef28f956ee829a1732234e1c217630a07269a8b1541b04cf9ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:76a2deab3da4dec0074b05cd55c4a13fb1b29d41a94bb8b9950dce20a3522264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267718567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297211dc40183d69dc480702730b40cbae9dfc493fb796b5fc04db545de658a4`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91675c8122bd5e5d099d638e3c2658258e550c65c38ff6a8a870788e49f4cbb`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f2086610af1e63647a355ac52c3e68978a86a959a8a7c6636dcd39e9d7480`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 3.6 MB (3624624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb353b4ff7460b69326f178db7028bef8949ed46ce7c9350cfda0c589be8c6`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8e7cb50e4a3269f4c49ce050ab8e86311ccdc3aff32892c3744297e921c5c`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15233d472285856d529c20d856a2397e1fc39287365860f4c074b2fc66aae374`  
		Last Modified: Tue, 17 Sep 2024 01:01:04 GMT  
		Size: 124.3 MB (124324901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96307cbb609eec848b4f63287642661d57946ba176b73d9672e7250ca7ebb588`  
		Last Modified: Tue, 17 Sep 2024 01:01:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d5fab837b49bba793141aff686b0c6f68bfec9cbf399e4fbe0b9f485a9a36`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 85.0 MB (84961563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0547d9968b62e61f578a202d34e1d8fa2ab3d1ea00374118b5155eb554a46`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 315.1 KB (315111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3d90fd3b189da91d9eb321cff21faafbad014dc98d94c03b50f6cf32d01bf4`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf9f1e81fe596d17c20e89ff3648760dba253d4a63cf4a6da095a95f2e530d`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 23.7 MB (23737116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:e8e45a5abd446d57fe0ee7b556059d0f9d3da94f8576448235e474cf1255c689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23694054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff63d91ae3b77ee75926057059d52174775ec10721689a963ce4c4664460d86`

```dockerfile
```

-	Layers:
	-	`sha256:70f29cef0a56c4c12d5e7bcb4cc4eeab4c92b55550e6b8ae53fc1d00be7f9023`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 23.7 MB (23676964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcb4bf154ffc745753b7138d756ea50c89610caaa2efba2edbe08880e66f5c5`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 17.1 KB (17090 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:923dee9792d1ac0772c83ea00bcea1fcecc3436f969148c817ac165a3b87088e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260030161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaae715bf4e1ac4053be3a3ce01be416bc689a2b6025438170dc8b4c6a2fba3`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7dd201263c103c809e1c44853e0636966888f2e37335ba2e026f35dafaafb2`  
		Last Modified: Tue, 17 Sep 2024 06:13:47 GMT  
		Size: 82.6 MB (82646665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f0f63fa981ec33dc63f4267e3f21c9f2816ea1bb26acc01a6ded62ef00af1`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 315.1 KB (315114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee4c039d165d6a20ea24e5ae06e4057f612ff7c5c6f87a657205ca0300213ce`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f4d1352e2286892bc738d595b438bc1147d080ee49a6c207153c9ccf4e35d`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.1 MB (23128446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron` - unknown; unknown

```console
$ docker pull ros@sha256:7d5af0baeabe69e767955d95397ab04bb27e2c12bb2326de62c29352ead7486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23707637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736281f35081f119a4156a7645a4a422ac8a26270e654aaf3e56656648b92e2`

```dockerfile
```

-	Layers:
	-	`sha256:508076939eabe19b1b849463536d01de387d086d08229596d83872bdffd9f0fb`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.7 MB (23690174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c567ff9e8346fd963c339e60aa4fe17485f2fee1d54ba9c9ef80828de6f959`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-perception`

```console
$ docker pull ros@sha256:71056fa056321590c7d980feb822afe94fa514ff69f0fb5f09bad41f7305abae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:b11908a6b870acbba473bafea86168a78fad5d7c22c8dd1913e06d109e6fb7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.0 MB (960027971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99de75e0f15325ce0e9a57b3b15aa176d59049f94ebadb25c927377b74d9d795`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91675c8122bd5e5d099d638e3c2658258e550c65c38ff6a8a870788e49f4cbb`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f2086610af1e63647a355ac52c3e68978a86a959a8a7c6636dcd39e9d7480`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 3.6 MB (3624624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb353b4ff7460b69326f178db7028bef8949ed46ce7c9350cfda0c589be8c6`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8e7cb50e4a3269f4c49ce050ab8e86311ccdc3aff32892c3744297e921c5c`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15233d472285856d529c20d856a2397e1fc39287365860f4c074b2fc66aae374`  
		Last Modified: Tue, 17 Sep 2024 01:01:04 GMT  
		Size: 124.3 MB (124324901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96307cbb609eec848b4f63287642661d57946ba176b73d9672e7250ca7ebb588`  
		Last Modified: Tue, 17 Sep 2024 01:01:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d5fab837b49bba793141aff686b0c6f68bfec9cbf399e4fbe0b9f485a9a36`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 85.0 MB (84961563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0547d9968b62e61f578a202d34e1d8fa2ab3d1ea00374118b5155eb554a46`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 315.1 KB (315111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3d90fd3b189da91d9eb321cff21faafbad014dc98d94c03b50f6cf32d01bf4`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf9f1e81fe596d17c20e89ff3648760dba253d4a63cf4a6da095a95f2e530d`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 23.7 MB (23737116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b516d5e0a7f715646eaf84f4372d78cbd699a5511c506141e9adbe309540977`  
		Last Modified: Tue, 17 Sep 2024 03:04:56 GMT  
		Size: 692.3 MB (692309404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:86a44a4ecde0aae3f295a0797bac0980b64f6878942e7689f1ed518bab05c6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58260122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f8a9a8a3193c12d124baad32de3c05777ddbdc1207edd7bf283e741b43813`

```dockerfile
```

-	Layers:
	-	`sha256:e1b18f0d90e3a70c3bc9800aa5d68150b338405083d7e383deb683b0684a1b86`  
		Last Modified: Tue, 17 Sep 2024 03:04:47 GMT  
		Size: 58.3 MB (58250482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020da288a7eb976b41ab3d4de13868dbe77dd6cd14cea558e0907367d3e26207`  
		Last Modified: Tue, 17 Sep 2024 03:04:46 GMT  
		Size: 9.6 KB (9640 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:114a133fffe1db7d3dfa05cd821a1741204968452ede0993fe2005f1e1ed6982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920236423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb9882929f140b730cc82c95e045d9fada684c65df8b860f7aca3c577478785`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7dd201263c103c809e1c44853e0636966888f2e37335ba2e026f35dafaafb2`  
		Last Modified: Tue, 17 Sep 2024 06:13:47 GMT  
		Size: 82.6 MB (82646665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f0f63fa981ec33dc63f4267e3f21c9f2816ea1bb26acc01a6ded62ef00af1`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 315.1 KB (315114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee4c039d165d6a20ea24e5ae06e4057f612ff7c5c6f87a657205ca0300213ce`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f4d1352e2286892bc738d595b438bc1147d080ee49a6c207153c9ccf4e35d`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.1 MB (23128446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d806dae4ec45dfdd497ba2fcf284d15f981bee138fa71fd78bcb0235e96fc20f`  
		Last Modified: Tue, 17 Sep 2024 08:00:22 GMT  
		Size: 660.2 MB (660206262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:a794980dc98b5c7b9fbf4043a6aa5c95f00f3ec596a162e7e245634f7b2d330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58256876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8648167f650d81f0084300670e41d614ab07760573efa8d7a1734d51d996f3b7`

```dockerfile
```

-	Layers:
	-	`sha256:de474500ff35deefa1abc0933752aa38cf597e1af65579be4580e9facb884dec`  
		Last Modified: Tue, 17 Sep 2024 08:00:11 GMT  
		Size: 58.2 MB (58246875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee3e6d30d8cb2253f5eb15b99dc024f7005f8b62dd78ee6c2f11a8a00c995c0`  
		Last Modified: Tue, 17 Sep 2024 08:00:08 GMT  
		Size: 10.0 KB (10001 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:71056fa056321590c7d980feb822afe94fa514ff69f0fb5f09bad41f7305abae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b11908a6b870acbba473bafea86168a78fad5d7c22c8dd1913e06d109e6fb7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.0 MB (960027971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99de75e0f15325ce0e9a57b3b15aa176d59049f94ebadb25c927377b74d9d795`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91675c8122bd5e5d099d638e3c2658258e550c65c38ff6a8a870788e49f4cbb`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f2086610af1e63647a355ac52c3e68978a86a959a8a7c6636dcd39e9d7480`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 3.6 MB (3624624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb353b4ff7460b69326f178db7028bef8949ed46ce7c9350cfda0c589be8c6`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8e7cb50e4a3269f4c49ce050ab8e86311ccdc3aff32892c3744297e921c5c`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15233d472285856d529c20d856a2397e1fc39287365860f4c074b2fc66aae374`  
		Last Modified: Tue, 17 Sep 2024 01:01:04 GMT  
		Size: 124.3 MB (124324901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96307cbb609eec848b4f63287642661d57946ba176b73d9672e7250ca7ebb588`  
		Last Modified: Tue, 17 Sep 2024 01:01:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d5fab837b49bba793141aff686b0c6f68bfec9cbf399e4fbe0b9f485a9a36`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 85.0 MB (84961563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0547d9968b62e61f578a202d34e1d8fa2ab3d1ea00374118b5155eb554a46`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 315.1 KB (315111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3d90fd3b189da91d9eb321cff21faafbad014dc98d94c03b50f6cf32d01bf4`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf9f1e81fe596d17c20e89ff3648760dba253d4a63cf4a6da095a95f2e530d`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 23.7 MB (23737116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b516d5e0a7f715646eaf84f4372d78cbd699a5511c506141e9adbe309540977`  
		Last Modified: Tue, 17 Sep 2024 03:04:56 GMT  
		Size: 692.3 MB (692309404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:86a44a4ecde0aae3f295a0797bac0980b64f6878942e7689f1ed518bab05c6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58260122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953f8a9a8a3193c12d124baad32de3c05777ddbdc1207edd7bf283e741b43813`

```dockerfile
```

-	Layers:
	-	`sha256:e1b18f0d90e3a70c3bc9800aa5d68150b338405083d7e383deb683b0684a1b86`  
		Last Modified: Tue, 17 Sep 2024 03:04:47 GMT  
		Size: 58.3 MB (58250482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020da288a7eb976b41ab3d4de13868dbe77dd6cd14cea558e0907367d3e26207`  
		Last Modified: Tue, 17 Sep 2024 03:04:46 GMT  
		Size: 9.6 KB (9640 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:114a133fffe1db7d3dfa05cd821a1741204968452ede0993fe2005f1e1ed6982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920236423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb9882929f140b730cc82c95e045d9fada684c65df8b860f7aca3c577478785`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7dd201263c103c809e1c44853e0636966888f2e37335ba2e026f35dafaafb2`  
		Last Modified: Tue, 17 Sep 2024 06:13:47 GMT  
		Size: 82.6 MB (82646665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f0f63fa981ec33dc63f4267e3f21c9f2816ea1bb26acc01a6ded62ef00af1`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 315.1 KB (315114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee4c039d165d6a20ea24e5ae06e4057f612ff7c5c6f87a657205ca0300213ce`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f4d1352e2286892bc738d595b438bc1147d080ee49a6c207153c9ccf4e35d`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.1 MB (23128446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d806dae4ec45dfdd497ba2fcf284d15f981bee138fa71fd78bcb0235e96fc20f`  
		Last Modified: Tue, 17 Sep 2024 08:00:22 GMT  
		Size: 660.2 MB (660206262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:a794980dc98b5c7b9fbf4043a6aa5c95f00f3ec596a162e7e245634f7b2d330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58256876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8648167f650d81f0084300670e41d614ab07760573efa8d7a1734d51d996f3b7`

```dockerfile
```

-	Layers:
	-	`sha256:de474500ff35deefa1abc0933752aa38cf597e1af65579be4580e9facb884dec`  
		Last Modified: Tue, 17 Sep 2024 08:00:11 GMT  
		Size: 58.2 MB (58246875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee3e6d30d8cb2253f5eb15b99dc024f7005f8b62dd78ee6c2f11a8a00c995c0`  
		Last Modified: Tue, 17 Sep 2024 08:00:08 GMT  
		Size: 10.0 KB (10001 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:66bd659365bd1ef28f956ee829a1732234e1c217630a07269a8b1541b04cf9ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:76a2deab3da4dec0074b05cd55c4a13fb1b29d41a94bb8b9950dce20a3522264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267718567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297211dc40183d69dc480702730b40cbae9dfc493fb796b5fc04db545de658a4`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91675c8122bd5e5d099d638e3c2658258e550c65c38ff6a8a870788e49f4cbb`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f2086610af1e63647a355ac52c3e68978a86a959a8a7c6636dcd39e9d7480`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 3.6 MB (3624624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb353b4ff7460b69326f178db7028bef8949ed46ce7c9350cfda0c589be8c6`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8e7cb50e4a3269f4c49ce050ab8e86311ccdc3aff32892c3744297e921c5c`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15233d472285856d529c20d856a2397e1fc39287365860f4c074b2fc66aae374`  
		Last Modified: Tue, 17 Sep 2024 01:01:04 GMT  
		Size: 124.3 MB (124324901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96307cbb609eec848b4f63287642661d57946ba176b73d9672e7250ca7ebb588`  
		Last Modified: Tue, 17 Sep 2024 01:01:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d5fab837b49bba793141aff686b0c6f68bfec9cbf399e4fbe0b9f485a9a36`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 85.0 MB (84961563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0547d9968b62e61f578a202d34e1d8fa2ab3d1ea00374118b5155eb554a46`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 315.1 KB (315111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3d90fd3b189da91d9eb321cff21faafbad014dc98d94c03b50f6cf32d01bf4`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf9f1e81fe596d17c20e89ff3648760dba253d4a63cf4a6da095a95f2e530d`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 23.7 MB (23737116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:e8e45a5abd446d57fe0ee7b556059d0f9d3da94f8576448235e474cf1255c689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23694054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff63d91ae3b77ee75926057059d52174775ec10721689a963ce4c4664460d86`

```dockerfile
```

-	Layers:
	-	`sha256:70f29cef0a56c4c12d5e7bcb4cc4eeab4c92b55550e6b8ae53fc1d00be7f9023`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 23.7 MB (23676964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcb4bf154ffc745753b7138d756ea50c89610caaa2efba2edbe08880e66f5c5`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 17.1 KB (17090 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:923dee9792d1ac0772c83ea00bcea1fcecc3436f969148c817ac165a3b87088e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260030161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaae715bf4e1ac4053be3a3ce01be416bc689a2b6025438170dc8b4c6a2fba3`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7dd201263c103c809e1c44853e0636966888f2e37335ba2e026f35dafaafb2`  
		Last Modified: Tue, 17 Sep 2024 06:13:47 GMT  
		Size: 82.6 MB (82646665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f0f63fa981ec33dc63f4267e3f21c9f2816ea1bb26acc01a6ded62ef00af1`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 315.1 KB (315114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee4c039d165d6a20ea24e5ae06e4057f612ff7c5c6f87a657205ca0300213ce`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f4d1352e2286892bc738d595b438bc1147d080ee49a6c207153c9ccf4e35d`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.1 MB (23128446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:7d5af0baeabe69e767955d95397ab04bb27e2c12bb2326de62c29352ead7486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23707637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736281f35081f119a4156a7645a4a422ac8a26270e654aaf3e56656648b92e2`

```dockerfile
```

-	Layers:
	-	`sha256:508076939eabe19b1b849463536d01de387d086d08229596d83872bdffd9f0fb`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.7 MB (23690174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c567ff9e8346fd963c339e60aa4fe17485f2fee1d54ba9c9ef80828de6f959`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:66bd659365bd1ef28f956ee829a1732234e1c217630a07269a8b1541b04cf9ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:76a2deab3da4dec0074b05cd55c4a13fb1b29d41a94bb8b9950dce20a3522264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267718567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297211dc40183d69dc480702730b40cbae9dfc493fb796b5fc04db545de658a4`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91675c8122bd5e5d099d638e3c2658258e550c65c38ff6a8a870788e49f4cbb`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f2086610af1e63647a355ac52c3e68978a86a959a8a7c6636dcd39e9d7480`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 3.6 MB (3624624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb353b4ff7460b69326f178db7028bef8949ed46ce7c9350cfda0c589be8c6`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8e7cb50e4a3269f4c49ce050ab8e86311ccdc3aff32892c3744297e921c5c`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15233d472285856d529c20d856a2397e1fc39287365860f4c074b2fc66aae374`  
		Last Modified: Tue, 17 Sep 2024 01:01:04 GMT  
		Size: 124.3 MB (124324901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96307cbb609eec848b4f63287642661d57946ba176b73d9672e7250ca7ebb588`  
		Last Modified: Tue, 17 Sep 2024 01:01:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d5fab837b49bba793141aff686b0c6f68bfec9cbf399e4fbe0b9f485a9a36`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 85.0 MB (84961563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0547d9968b62e61f578a202d34e1d8fa2ab3d1ea00374118b5155eb554a46`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 315.1 KB (315111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3d90fd3b189da91d9eb321cff21faafbad014dc98d94c03b50f6cf32d01bf4`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf9f1e81fe596d17c20e89ff3648760dba253d4a63cf4a6da095a95f2e530d`  
		Last Modified: Tue, 17 Sep 2024 01:58:32 GMT  
		Size: 23.7 MB (23737116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e8e45a5abd446d57fe0ee7b556059d0f9d3da94f8576448235e474cf1255c689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23694054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff63d91ae3b77ee75926057059d52174775ec10721689a963ce4c4664460d86`

```dockerfile
```

-	Layers:
	-	`sha256:70f29cef0a56c4c12d5e7bcb4cc4eeab4c92b55550e6b8ae53fc1d00be7f9023`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 23.7 MB (23676964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcb4bf154ffc745753b7138d756ea50c89610caaa2efba2edbe08880e66f5c5`  
		Last Modified: Tue, 17 Sep 2024 01:58:31 GMT  
		Size: 17.1 KB (17090 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:923dee9792d1ac0772c83ea00bcea1fcecc3436f969148c817ac165a3b87088e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260030161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaae715bf4e1ac4053be3a3ce01be416bc689a2b6025438170dc8b4c6a2fba3`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7dd201263c103c809e1c44853e0636966888f2e37335ba2e026f35dafaafb2`  
		Last Modified: Tue, 17 Sep 2024 06:13:47 GMT  
		Size: 82.6 MB (82646665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1f0f63fa981ec33dc63f4267e3f21c9f2816ea1bb26acc01a6ded62ef00af1`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 315.1 KB (315114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee4c039d165d6a20ea24e5ae06e4057f612ff7c5c6f87a657205ca0300213ce`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f4d1352e2286892bc738d595b438bc1147d080ee49a6c207153c9ccf4e35d`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.1 MB (23128446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:7d5af0baeabe69e767955d95397ab04bb27e2c12bb2326de62c29352ead7486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23707637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9736281f35081f119a4156a7645a4a422ac8a26270e654aaf3e56656648b92e2`

```dockerfile
```

-	Layers:
	-	`sha256:508076939eabe19b1b849463536d01de387d086d08229596d83872bdffd9f0fb`  
		Last Modified: Tue, 17 Sep 2024 06:13:45 GMT  
		Size: 23.7 MB (23690174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c567ff9e8346fd963c339e60aa4fe17485f2fee1d54ba9c9ef80828de6f959`  
		Last Modified: Tue, 17 Sep 2024 06:13:44 GMT  
		Size: 17.5 KB (17463 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:7f44e6479d6f23d91e78ba4a5239645b2c71daa989529daff72fd21eebf07619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:ed20bf25b726beb44bd94a33020c89f47224f21cd1880db9bf035a6363d598d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158702361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304159b9ff0f962f7bc5389e1816ed1e79c85d0d06747f460c60d9445793477c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91675c8122bd5e5d099d638e3c2658258e550c65c38ff6a8a870788e49f4cbb`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f2086610af1e63647a355ac52c3e68978a86a959a8a7c6636dcd39e9d7480`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 3.6 MB (3624624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb353b4ff7460b69326f178db7028bef8949ed46ce7c9350cfda0c589be8c6`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8e7cb50e4a3269f4c49ce050ab8e86311ccdc3aff32892c3744297e921c5c`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15233d472285856d529c20d856a2397e1fc39287365860f4c074b2fc66aae374`  
		Last Modified: Tue, 17 Sep 2024 01:01:04 GMT  
		Size: 124.3 MB (124324901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96307cbb609eec848b4f63287642661d57946ba176b73d9672e7250ca7ebb588`  
		Last Modified: Tue, 17 Sep 2024 01:01:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:0ac254df8229c0e300cbb28bb01b87b867dd98fbcfa46a3818d0243b32fc7a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea05015f68f5c04a0324f89b56da42f1d6536ace28df95acc62cf184662335f`

```dockerfile
```

-	Layers:
	-	`sha256:9c8387e869b30293121edcb0c5943e93e2fabd8b743519e6f1d3c7cafabf153a`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.7 KB (1667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f84522e1ab35d57eb4aea003c237e9b775d9a889d42a73de81161eaee60b96a`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 16.1 KB (16111 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:12f9b2170e11a52d7305a6abfc8bb645aab71b33f043ba22ebc6cc32b3734255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153937505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c722353942070e3f847ee536084d2325e447aaac0266310901b1e32861e4a027`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fe3e2587f80367fb6a901726f98e5e7cafbfed122e76959c37b4be19a0e682a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19205110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59933117d1d7e6494fac00353e9f7d062440e6c742e377e8b8ce5ffcff9d705`

```dockerfile
```

-	Layers:
	-	`sha256:c7e2c2cc282e969e8a2423aa026fabf25f64fea551c239037d8bb3f75816d5af`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 19.2 MB (19188722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9155a360922796df69257bca56a3ee38501648e2e96bccc1801d913175aa1ba3`  
		Last Modified: Tue, 17 Sep 2024 03:03:33 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:7f44e6479d6f23d91e78ba4a5239645b2c71daa989529daff72fd21eebf07619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:ed20bf25b726beb44bd94a33020c89f47224f21cd1880db9bf035a6363d598d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158702361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304159b9ff0f962f7bc5389e1816ed1e79c85d0d06747f460c60d9445793477c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91675c8122bd5e5d099d638e3c2658258e550c65c38ff6a8a870788e49f4cbb`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.2 MB (1214680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6f2086610af1e63647a355ac52c3e68978a86a959a8a7c6636dcd39e9d7480`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 3.6 MB (3624624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb353b4ff7460b69326f178db7028bef8949ed46ce7c9350cfda0c589be8c6`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac8e7cb50e4a3269f4c49ce050ab8e86311ccdc3aff32892c3744297e921c5c`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15233d472285856d529c20d856a2397e1fc39287365860f4c074b2fc66aae374`  
		Last Modified: Tue, 17 Sep 2024 01:01:04 GMT  
		Size: 124.3 MB (124324901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96307cbb609eec848b4f63287642661d57946ba176b73d9672e7250ca7ebb588`  
		Last Modified: Tue, 17 Sep 2024 01:01:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:0ac254df8229c0e300cbb28bb01b87b867dd98fbcfa46a3818d0243b32fc7a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea05015f68f5c04a0324f89b56da42f1d6536ace28df95acc62cf184662335f`

```dockerfile
```

-	Layers:
	-	`sha256:9c8387e869b30293121edcb0c5943e93e2fabd8b743519e6f1d3c7cafabf153a`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 1.7 KB (1667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f84522e1ab35d57eb4aea003c237e9b775d9a889d42a73de81161eaee60b96a`  
		Last Modified: Tue, 17 Sep 2024 01:01:01 GMT  
		Size: 16.1 KB (16111 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:12f9b2170e11a52d7305a6abfc8bb645aab71b33f043ba22ebc6cc32b3734255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153937505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c722353942070e3f847ee536084d2325e447aaac0266310901b1e32861e4a027`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:fe3e2587f80367fb6a901726f98e5e7cafbfed122e76959c37b4be19a0e682a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19205110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59933117d1d7e6494fac00353e9f7d062440e6c742e377e8b8ce5ffcff9d705`

```dockerfile
```

-	Layers:
	-	`sha256:c7e2c2cc282e969e8a2423aa026fabf25f64fea551c239037d8bb3f75816d5af`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 19.2 MB (19188722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9155a360922796df69257bca56a3ee38501648e2e96bccc1801d913175aa1ba3`  
		Last Modified: Tue, 17 Sep 2024 03:03:33 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:c98c19c3ac3d82f6ee1d1b7d4b303adcd26f53a73d108dfcca9dd79be705f01a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:297ac04d2482efc75290975efd571ab9140f5f08e7c9fd124a94e52dab67a058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301015992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73deb91779711bfc3ec22695e0f25ac2ca97d5567d482838d25afa8659b5efb1`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3245a54a6b1203c259d98711247694d539946e93b88b73476dbc5e7f10dfae7`  
		Last Modified: Tue, 17 Sep 2024 01:58:43 GMT  
		Size: 114.1 MB (114117439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ddecc69889e6bac66d7cd30bb100e9bf169f0d9f4d1e138f38b2c134a6d0c`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ee904ea3ce21019e7f33293925fb443fda37c9113a49c7d4150f96f44b4b4`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6791264fbf82a2caabb5d5294307d95b55bd7b69f0b34f91aa7e6bd8a59ed`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 27.5 MB (27528209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:2ddd3053d5e96e6c1edc85922062d0d6794f1866f3560e19305ec7542e3d6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23825095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2a8e02fbbe5ce71f86f8412887f48fe876f80323bebaad33342133fce46247`

```dockerfile
```

-	Layers:
	-	`sha256:f889b9d8d945886175060cbaca0d8171b1c30a45e16abb4fedf5f741d95d4794`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 23.8 MB (23807700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e71bded234afd21d6799e8c98b251a660f5b9eb733d55ef0db2589645d72a06`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aaba420e8b0d780d3ce019de3d7cc725c5c0cc01855a92a5267fad489fb3a6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290782313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f01b10ca815f5c8dacfa0b482df1614d585b6c4366551ba36b59ac1fa20de2b`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518a131b38ee95b961064f197710798a17648dc0631e5fb4433b8aa99952067`  
		Last Modified: Tue, 17 Sep 2024 06:16:29 GMT  
		Size: 111.0 MB (110959042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d9029a2747adaedc2d53f563fbf4187b643c280e2e5051a9ce8713d68eae7`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457da156fa4ef9f8c441d5b0b526955cbdbae966e50fda5954eaa2960486c83`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed8c21754ba7715f2563fbcffee96bd233879e2752df41ed13cb72933e17e6`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 26.7 MB (26673054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:28b66e4751fd4aa27e3c9ce79145258c745a724dfbaaf588e1533d59e3e910a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23848165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ada7bb4b81b4bfe508612c4c842acf1f766ae7957783622e4c009bd93aef0a1`

```dockerfile
```

-	Layers:
	-	`sha256:18c07dd4348274979bb3cf3ddf3b3f6f4f8f5f732e10208358c4127abe484f6e`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 23.8 MB (23830385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8e182c910c0f1961c930cf536ec28357f4f5f1ab8ec5803ebf69e2662f765ab`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:640ea78cd08cfc6b3fbb32ff8d0b7b410263c57ff5f2e9230cc1dd47c31b57e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:562ddcb7cdecf28139f141852b1590638f95cbf3550c2efeca33c9fac234bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624913772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1280adcbe207e351aa67df3fe1862fa1b73ae9341dff73ddcf69542f5976eb94`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3245a54a6b1203c259d98711247694d539946e93b88b73476dbc5e7f10dfae7`  
		Last Modified: Tue, 17 Sep 2024 01:58:43 GMT  
		Size: 114.1 MB (114117439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ddecc69889e6bac66d7cd30bb100e9bf169f0d9f4d1e138f38b2c134a6d0c`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ee904ea3ce21019e7f33293925fb443fda37c9113a49c7d4150f96f44b4b4`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6791264fbf82a2caabb5d5294307d95b55bd7b69f0b34f91aa7e6bd8a59ed`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 27.5 MB (27528209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f76a4ee6bd37d6f59d31f5c887311e5e357f57f4e71fc7509132768a58e399f`  
		Last Modified: Tue, 17 Sep 2024 03:03:15 GMT  
		Size: 323.9 MB (323897780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9396d083c18356d3d6907cae04f955abcc499e76c50c8cebf489d477c9e7cdf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42092885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea80db29aa0acd47a1e183b00143c3d83c923ea15a3533fa1e406b709378227`

```dockerfile
```

-	Layers:
	-	`sha256:f0afc267360d5976558e24e87bbbc9c914b64f50ddf337e97bdd4a38765e0d71`  
		Last Modified: Tue, 17 Sep 2024 03:03:11 GMT  
		Size: 42.1 MB (42083231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e640e9b7e8daa2964fce3ee3bf9a7e8515f24646591c13faa363d1f0f297812`  
		Last Modified: Tue, 17 Sep 2024 03:03:11 GMT  
		Size: 9.7 KB (9654 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8eebc6ffd92314b1833e06171223f52f9de798c40b8dcc1fc3559b47d81eabec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.8 MB (567794628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3286e660df0145c72c9652d4e0e40eeb9362e2099155ed7f76fb5d1e9f1c5109`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518a131b38ee95b961064f197710798a17648dc0631e5fb4433b8aa99952067`  
		Last Modified: Tue, 17 Sep 2024 06:16:29 GMT  
		Size: 111.0 MB (110959042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d9029a2747adaedc2d53f563fbf4187b643c280e2e5051a9ce8713d68eae7`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457da156fa4ef9f8c441d5b0b526955cbdbae966e50fda5954eaa2960486c83`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed8c21754ba7715f2563fbcffee96bd233879e2752df41ed13cb72933e17e6`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 26.7 MB (26673054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7125b2360b0a7e967429934d8a8682aaa8dfcff559778fe75399fc28565fb4`  
		Last Modified: Tue, 17 Sep 2024 08:07:13 GMT  
		Size: 277.0 MB (277012315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:288b279c7248e078d722abf741726efa283e0727c1d3c9e7ab35d9e78e4b11f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42091339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d51944033316ffd311477dea436701e7965ffefa3ff6daef68544ab3daeb67c`

```dockerfile
```

-	Layers:
	-	`sha256:0dd99915b79df3a9f0747acc4f24a11c6d74af0f77de58018e0c23f39acb918b`  
		Last Modified: Tue, 17 Sep 2024 08:07:07 GMT  
		Size: 42.1 MB (42081324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5508be16bf7e9178906fb10a9df1073eb447bc3e4d0240010ae06fd9fd1eff43`  
		Last Modified: Tue, 17 Sep 2024 08:07:06 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:640ea78cd08cfc6b3fbb32ff8d0b7b410263c57ff5f2e9230cc1dd47c31b57e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:562ddcb7cdecf28139f141852b1590638f95cbf3550c2efeca33c9fac234bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624913772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1280adcbe207e351aa67df3fe1862fa1b73ae9341dff73ddcf69542f5976eb94`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3245a54a6b1203c259d98711247694d539946e93b88b73476dbc5e7f10dfae7`  
		Last Modified: Tue, 17 Sep 2024 01:58:43 GMT  
		Size: 114.1 MB (114117439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ddecc69889e6bac66d7cd30bb100e9bf169f0d9f4d1e138f38b2c134a6d0c`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ee904ea3ce21019e7f33293925fb443fda37c9113a49c7d4150f96f44b4b4`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6791264fbf82a2caabb5d5294307d95b55bd7b69f0b34f91aa7e6bd8a59ed`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 27.5 MB (27528209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f76a4ee6bd37d6f59d31f5c887311e5e357f57f4e71fc7509132768a58e399f`  
		Last Modified: Tue, 17 Sep 2024 03:03:15 GMT  
		Size: 323.9 MB (323897780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9396d083c18356d3d6907cae04f955abcc499e76c50c8cebf489d477c9e7cdf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42092885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea80db29aa0acd47a1e183b00143c3d83c923ea15a3533fa1e406b709378227`

```dockerfile
```

-	Layers:
	-	`sha256:f0afc267360d5976558e24e87bbbc9c914b64f50ddf337e97bdd4a38765e0d71`  
		Last Modified: Tue, 17 Sep 2024 03:03:11 GMT  
		Size: 42.1 MB (42083231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e640e9b7e8daa2964fce3ee3bf9a7e8515f24646591c13faa363d1f0f297812`  
		Last Modified: Tue, 17 Sep 2024 03:03:11 GMT  
		Size: 9.7 KB (9654 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8eebc6ffd92314b1833e06171223f52f9de798c40b8dcc1fc3559b47d81eabec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.8 MB (567794628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3286e660df0145c72c9652d4e0e40eeb9362e2099155ed7f76fb5d1e9f1c5109`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518a131b38ee95b961064f197710798a17648dc0631e5fb4433b8aa99952067`  
		Last Modified: Tue, 17 Sep 2024 06:16:29 GMT  
		Size: 111.0 MB (110959042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d9029a2747adaedc2d53f563fbf4187b643c280e2e5051a9ce8713d68eae7`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457da156fa4ef9f8c441d5b0b526955cbdbae966e50fda5954eaa2960486c83`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed8c21754ba7715f2563fbcffee96bd233879e2752df41ed13cb72933e17e6`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 26.7 MB (26673054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7125b2360b0a7e967429934d8a8682aaa8dfcff559778fe75399fc28565fb4`  
		Last Modified: Tue, 17 Sep 2024 08:07:13 GMT  
		Size: 277.0 MB (277012315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:288b279c7248e078d722abf741726efa283e0727c1d3c9e7ab35d9e78e4b11f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42091339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d51944033316ffd311477dea436701e7965ffefa3ff6daef68544ab3daeb67c`

```dockerfile
```

-	Layers:
	-	`sha256:0dd99915b79df3a9f0747acc4f24a11c6d74af0f77de58018e0c23f39acb918b`  
		Last Modified: Tue, 17 Sep 2024 08:07:07 GMT  
		Size: 42.1 MB (42081324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5508be16bf7e9178906fb10a9df1073eb447bc3e4d0240010ae06fd9fd1eff43`  
		Last Modified: Tue, 17 Sep 2024 08:07:06 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:c98c19c3ac3d82f6ee1d1b7d4b303adcd26f53a73d108dfcca9dd79be705f01a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:297ac04d2482efc75290975efd571ab9140f5f08e7c9fd124a94e52dab67a058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301015992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73deb91779711bfc3ec22695e0f25ac2ca97d5567d482838d25afa8659b5efb1`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3245a54a6b1203c259d98711247694d539946e93b88b73476dbc5e7f10dfae7`  
		Last Modified: Tue, 17 Sep 2024 01:58:43 GMT  
		Size: 114.1 MB (114117439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ddecc69889e6bac66d7cd30bb100e9bf169f0d9f4d1e138f38b2c134a6d0c`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ee904ea3ce21019e7f33293925fb443fda37c9113a49c7d4150f96f44b4b4`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6791264fbf82a2caabb5d5294307d95b55bd7b69f0b34f91aa7e6bd8a59ed`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 27.5 MB (27528209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:2ddd3053d5e96e6c1edc85922062d0d6794f1866f3560e19305ec7542e3d6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23825095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2a8e02fbbe5ce71f86f8412887f48fe876f80323bebaad33342133fce46247`

```dockerfile
```

-	Layers:
	-	`sha256:f889b9d8d945886175060cbaca0d8171b1c30a45e16abb4fedf5f741d95d4794`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 23.8 MB (23807700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e71bded234afd21d6799e8c98b251a660f5b9eb733d55ef0db2589645d72a06`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aaba420e8b0d780d3ce019de3d7cc725c5c0cc01855a92a5267fad489fb3a6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290782313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f01b10ca815f5c8dacfa0b482df1614d585b6c4366551ba36b59ac1fa20de2b`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518a131b38ee95b961064f197710798a17648dc0631e5fb4433b8aa99952067`  
		Last Modified: Tue, 17 Sep 2024 06:16:29 GMT  
		Size: 111.0 MB (110959042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d9029a2747adaedc2d53f563fbf4187b643c280e2e5051a9ce8713d68eae7`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457da156fa4ef9f8c441d5b0b526955cbdbae966e50fda5954eaa2960486c83`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed8c21754ba7715f2563fbcffee96bd233879e2752df41ed13cb72933e17e6`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 26.7 MB (26673054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:28b66e4751fd4aa27e3c9ce79145258c745a724dfbaaf588e1533d59e3e910a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23848165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ada7bb4b81b4bfe508612c4c842acf1f766ae7957783622e4c009bd93aef0a1`

```dockerfile
```

-	Layers:
	-	`sha256:18c07dd4348274979bb3cf3ddf3b3f6f4f8f5f732e10208358c4127abe484f6e`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 23.8 MB (23830385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8e182c910c0f1961c930cf536ec28357f4f5f1ab8ec5803ebf69e2662f765ab`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:c98c19c3ac3d82f6ee1d1b7d4b303adcd26f53a73d108dfcca9dd79be705f01a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:297ac04d2482efc75290975efd571ab9140f5f08e7c9fd124a94e52dab67a058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301015992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73deb91779711bfc3ec22695e0f25ac2ca97d5567d482838d25afa8659b5efb1`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3245a54a6b1203c259d98711247694d539946e93b88b73476dbc5e7f10dfae7`  
		Last Modified: Tue, 17 Sep 2024 01:58:43 GMT  
		Size: 114.1 MB (114117439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ddecc69889e6bac66d7cd30bb100e9bf169f0d9f4d1e138f38b2c134a6d0c`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ee904ea3ce21019e7f33293925fb443fda37c9113a49c7d4150f96f44b4b4`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6791264fbf82a2caabb5d5294307d95b55bd7b69f0b34f91aa7e6bd8a59ed`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 27.5 MB (27528209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:2ddd3053d5e96e6c1edc85922062d0d6794f1866f3560e19305ec7542e3d6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23825095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2a8e02fbbe5ce71f86f8412887f48fe876f80323bebaad33342133fce46247`

```dockerfile
```

-	Layers:
	-	`sha256:f889b9d8d945886175060cbaca0d8171b1c30a45e16abb4fedf5f741d95d4794`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 23.8 MB (23807700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e71bded234afd21d6799e8c98b251a660f5b9eb733d55ef0db2589645d72a06`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aaba420e8b0d780d3ce019de3d7cc725c5c0cc01855a92a5267fad489fb3a6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290782313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f01b10ca815f5c8dacfa0b482df1614d585b6c4366551ba36b59ac1fa20de2b`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518a131b38ee95b961064f197710798a17648dc0631e5fb4433b8aa99952067`  
		Last Modified: Tue, 17 Sep 2024 06:16:29 GMT  
		Size: 111.0 MB (110959042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d9029a2747adaedc2d53f563fbf4187b643c280e2e5051a9ce8713d68eae7`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457da156fa4ef9f8c441d5b0b526955cbdbae966e50fda5954eaa2960486c83`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed8c21754ba7715f2563fbcffee96bd233879e2752df41ed13cb72933e17e6`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 26.7 MB (26673054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:28b66e4751fd4aa27e3c9ce79145258c745a724dfbaaf588e1533d59e3e910a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23848165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ada7bb4b81b4bfe508612c4c842acf1f766ae7957783622e4c009bd93aef0a1`

```dockerfile
```

-	Layers:
	-	`sha256:18c07dd4348274979bb3cf3ddf3b3f6f4f8f5f732e10208358c4127abe484f6e`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 23.8 MB (23830385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8e182c910c0f1961c930cf536ec28357f4f5f1ab8ec5803ebf69e2662f765ab`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:a0d1431020224c6c7ca122fa85297245067bfabc2ff988a0489d2fdc9d96e6f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:5d29bd09131a94bdc0f659d39215093d503808909f55eb45027d7957fb3a1357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159036689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4869fd5580b33ce9c332550445aaa3a94cf6ebef37eb6875223edfdee310f74`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6dd70e42372eb6e009b26d9e91425d417875917388bfe8eb6f55f14fe5d3d8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17802762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5461a25e5dc3022b2d3f3457b270cb83049e19df71ae80ec85430c882da99228`

```dockerfile
```

-	Layers:
	-	`sha256:d590caa6ee64bf31908299512cc784014df46c88a0616be8a61be17608c4fa47`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 17.8 MB (17786644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4656c91b4471fc9d534b1e2569e3ded51bea948b185eccf8f8e6cf9bf1e44fd9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cab851142807b422f7ede19f6eb07c220b320e832e3575eaf0c4029529b6ae8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152816580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8975a9812612d067bf362740b8042622c480d4e4de1d6df2b4b5555bc4682b4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:a567299747b5c103493ab1b8392adf9a8861c7d86369944cbb633f4356c5149b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17777010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d60b95fc9944cb121a5a008cef985156082b2ebb8b848f8cc680b88bfb419c`

```dockerfile
```

-	Layers:
	-	`sha256:12b6b943f5f987303a5745273e198cc72565ec512018cfcca8bdae94a72899c0`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 17.8 MB (17760615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3d9df6f5aea3ed218ec489eca8cfc2bcb8efc33d297c9924c5f30c4c34c15b`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:a0d1431020224c6c7ca122fa85297245067bfabc2ff988a0489d2fdc9d96e6f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:5d29bd09131a94bdc0f659d39215093d503808909f55eb45027d7957fb3a1357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159036689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4869fd5580b33ce9c332550445aaa3a94cf6ebef37eb6875223edfdee310f74`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6dd70e42372eb6e009b26d9e91425d417875917388bfe8eb6f55f14fe5d3d8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17802762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5461a25e5dc3022b2d3f3457b270cb83049e19df71ae80ec85430c882da99228`

```dockerfile
```

-	Layers:
	-	`sha256:d590caa6ee64bf31908299512cc784014df46c88a0616be8a61be17608c4fa47`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 17.8 MB (17786644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4656c91b4471fc9d534b1e2569e3ded51bea948b185eccf8f8e6cf9bf1e44fd9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cab851142807b422f7ede19f6eb07c220b320e832e3575eaf0c4029529b6ae8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152816580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8975a9812612d067bf362740b8042622c480d4e4de1d6df2b4b5555bc4682b4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a567299747b5c103493ab1b8392adf9a8861c7d86369944cbb633f4356c5149b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17777010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d60b95fc9944cb121a5a008cef985156082b2ebb8b848f8cc680b88bfb419c`

```dockerfile
```

-	Layers:
	-	`sha256:12b6b943f5f987303a5745273e198cc72565ec512018cfcca8bdae94a72899c0`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 17.8 MB (17760615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3d9df6f5aea3ed218ec489eca8cfc2bcb8efc33d297c9924c5f30c4c34c15b`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:c98c19c3ac3d82f6ee1d1b7d4b303adcd26f53a73d108dfcca9dd79be705f01a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:297ac04d2482efc75290975efd571ab9140f5f08e7c9fd124a94e52dab67a058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301015992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73deb91779711bfc3ec22695e0f25ac2ca97d5567d482838d25afa8659b5efb1`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96daa89ceb291c8f771d1ab72b9663f1805a33a5636f7b62f64c1863247b25`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 683.2 KB (683196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7df6a09a620587b969314ddcbc24a77fd041419f7e59b8ff3b3551cd3452d51`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 3.6 MB (3559558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a173d97c2a8ca8483bef9f3d972986ecb37a8aa7b3d1e8bc3845870c938a9`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cddd502d528310c0b48eac5d95ae5e804f83cdc8857e334167e8a48fa97bc4`  
		Last Modified: Tue, 17 Sep 2024 01:01:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080fff65da1b2a3f0eda92d84c470f05c5e4b255d89cb68ab7db5e5775ac6e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:09 GMT  
		Size: 125.0 MB (125041637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789740404e0b1f903f5e7cc001df2bfa8348d5057ab457a38814c91abb285941`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3245a54a6b1203c259d98711247694d539946e93b88b73476dbc5e7f10dfae7`  
		Last Modified: Tue, 17 Sep 2024 01:58:43 GMT  
		Size: 114.1 MB (114117439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ddecc69889e6bac66d7cd30bb100e9bf169f0d9f4d1e138f38b2c134a6d0c`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ee904ea3ce21019e7f33293925fb443fda37c9113a49c7d4150f96f44b4b4`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6791264fbf82a2caabb5d5294307d95b55bd7b69f0b34f91aa7e6bd8a59ed`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 27.5 MB (27528209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:2ddd3053d5e96e6c1edc85922062d0d6794f1866f3560e19305ec7542e3d6024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23825095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2a8e02fbbe5ce71f86f8412887f48fe876f80323bebaad33342133fce46247`

```dockerfile
```

-	Layers:
	-	`sha256:f889b9d8d945886175060cbaca0d8171b1c30a45e16abb4fedf5f741d95d4794`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 23.8 MB (23807700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e71bded234afd21d6799e8c98b251a660f5b9eb733d55ef0db2589645d72a06`  
		Last Modified: Tue, 17 Sep 2024 01:58:42 GMT  
		Size: 17.4 KB (17395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aaba420e8b0d780d3ce019de3d7cc725c5c0cc01855a92a5267fad489fb3a6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290782313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f01b10ca815f5c8dacfa0b482df1614d585b6c4366551ba36b59ac1fa20de2b`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712aa33a4663c4af5aba8f2b6a24ada39bb199c4545aa5da94a3428451eb30f7`  
		Last Modified: Tue, 17 Sep 2024 03:06:10 GMT  
		Size: 119.7 MB (119686286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aca6c76c980e62f820bd5219b507c3aadde101d91ce75faca3a64e38068c54`  
		Last Modified: Tue, 17 Sep 2024 03:06:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518a131b38ee95b961064f197710798a17648dc0631e5fb4433b8aa99952067`  
		Last Modified: Tue, 17 Sep 2024 06:16:29 GMT  
		Size: 111.0 MB (110959042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d9029a2747adaedc2d53f563fbf4187b643c280e2e5051a9ce8713d68eae7`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 331.2 KB (331200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5457da156fa4ef9f8c441d5b0b526955cbdbae966e50fda5954eaa2960486c83`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed8c21754ba7715f2563fbcffee96bd233879e2752df41ed13cb72933e17e6`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 26.7 MB (26673054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:28b66e4751fd4aa27e3c9ce79145258c745a724dfbaaf588e1533d59e3e910a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23848165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ada7bb4b81b4bfe508612c4c842acf1f766ae7957783622e4c009bd93aef0a1`

```dockerfile
```

-	Layers:
	-	`sha256:18c07dd4348274979bb3cf3ddf3b3f6f4f8f5f732e10208358c4127abe484f6e`  
		Last Modified: Tue, 17 Sep 2024 06:16:27 GMT  
		Size: 23.8 MB (23830385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8e182c910c0f1961c930cf536ec28357f4f5f1ab8ec5803ebf69e2662f765ab`  
		Last Modified: Tue, 17 Sep 2024 06:16:26 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic`

```console
$ docker pull ros@sha256:e3866df3b9798c4f3b49946d61b179745a22409ee8ce7037411ea550581b12b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:c7631b6323509f943142bd494abf268127a6807d81bd75e5f1fec2e0cd2caf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263061226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408a67701899f969b3e60f4a0eb58d35defafadadb7f564aadcd939bac6d28d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:fc58b4b5b47a9daf00a015010b9c405b2bee15fbcedb748dc03ec81728c088fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27594860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4332305b98df7ac49ef214202dd987420519c390e070c0a75a3ae2192efc6d46`

```dockerfile
```

-	Layers:
	-	`sha256:89609352396b765399d331c17b049a4903d13cc7b7165511bde21d8a061ce2e3`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 27.6 MB (27581208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783f1ac79ac7347d7269a070e63dd8d785bba5a1bf91955cdf05d7a0faac1760`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:16f26c7d44fbd3cf3d9e035ff76de360e992cf6fc7e4254290980286774ed4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0057b00ee435f96c6f5be12c690f3189f8a289111f5b5915f940befb9a00f0fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:2df235d55b1f2af746ffc7217df4e45535de5e5073e1f5827e6105ab6b528b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c37f348b239028298251d0b86d1db02d5b50229cf5448fcdec29b57d7514c3`

```dockerfile
```

-	Layers:
	-	`sha256:e2a7dbfd0c788d3bf5679e89cf1b8f0005ab4953a8d6db188b14521177558656`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 27.3 MB (27344563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df22184734123eb54b635454f9e7340cea27496039962e972936a206f75ac5`  
		Last Modified: Sat, 17 Aug 2024 04:37:55 GMT  
		Size: 13.7 KB (13746 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:52faca237a809534ad5a7ed7e690f03870c886d409b7f36a7f023fb2c78c8dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250137186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbafa4ad53ba861e563d273562d8bbd9284277009490126a216ac061454a7f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3fae8c58da741669e19764e401a7013912e589d9c6d92c5a2945d08fec39a0`  
		Last Modified: Sat, 17 Aug 2024 08:08:47 GMT  
		Size: 45.0 MB (44991185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4462df4c39bb00784ad189022804cc9152913e31a1728620b9825f5e37db6`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 328.3 KB (328336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63189b8e00968cd826a850018fd7d859a1f3fc70ddfb6d4516c68273f24bfc`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:a219de600f12d49f47f8089bc52b3165408aaa6070138f27f22a39ff303b087f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27545519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a116aa9d4e62e43f62651071e3f03b94f410287307399f9d5720fd6c2301ec1`

```dockerfile
```

-	Layers:
	-	`sha256:1a0b2c900c0ff7aad65d97a32d6e5662f1d7e4024119511fa37f056621ed90cb`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 27.5 MB (27531494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a73d809fe4276e42d11adc9d11be29140cfcd3d3a7f66d41a1a0d703466f9519`  
		Last Modified: Sat, 17 Aug 2024 08:08:45 GMT  
		Size: 14.0 KB (14025 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:296547d04032cebbf5b8e6e3865f90296f54d91991f340d1e171b42e5a7f1308
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:61702b8c76b4f7c24532bf40434dadfbefadacec0e40b3ebb7bdf7eb6da97eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.2 MB (834220729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2880310d2194c8b1b0e07527bfe69673b02d184809d18dc03fc970c36f1ab444`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fa10f85d04d0836d1a7c22d2ad13e46571f44a1f1dfaee1c674ca2f6095cc`  
		Last Modified: Sat, 17 Aug 2024 05:03:22 GMT  
		Size: 571.2 MB (571159503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:a5efc55a26a40f301d96620861c7499e45720b8b857b5ab5444205d5de54b75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51767830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98782f46dc4a047d83771b48af03e37df75da7fceed5ae0148ddb82875a139e1`

```dockerfile
```

-	Layers:
	-	`sha256:f1ef0f1b81e9d98b666a3e3555d994d0ea061ec9d4b8e8654fcfe0c4869c295b`  
		Last Modified: Sat, 17 Aug 2024 05:03:07 GMT  
		Size: 51.8 MB (51758491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b4f292f9ed120d34bc2ebe984fd67d9a0ae996a1d82d6fda4708e46ce631d0`  
		Last Modified: Sat, 17 Aug 2024 05:03:05 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:43c1a1a7aa88b2a90ca5d55361090ebd99bd55eeb6c1419bf629f840ccd48761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.1 MB (725142418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ce214f07aa17e207f4a073ee0cedfa0620db9f3394cf02b10a158c4ef69ef9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e16c522834ddb11992be720d1f536f974b3e32f7ab85bd13d7c1310ca3f38f`  
		Last Modified: Sat, 17 Aug 2024 05:13:55 GMT  
		Size: 496.9 MB (496869266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:0ec620ced06fd208b24ac804fef70a534967f54ef8402e2f2b44384c690afa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51401685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba7336350a27cca0d27f6574c74e2523ae2132c9e6e1f630cfc861cbdd36e8`

```dockerfile
```

-	Layers:
	-	`sha256:fd8662e1afe75503280ba88308b9b29d52a06f230a7f865238d04fbbb5ddff2c`  
		Last Modified: Sat, 17 Aug 2024 05:13:46 GMT  
		Size: 51.4 MB (51392285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81db02321b3ccf7bdcb5e82623c68586bc3639f3bea788e07ce7c0b49343c0a4`  
		Last Modified: Sat, 17 Aug 2024 05:13:44 GMT  
		Size: 9.4 KB (9400 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:52c269f692fe649a5e5aa49b82fe3c6305a724049dfaa20dc0ce2f000d9811fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.2 MB (784186089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1130ac47fccd7cf68959033a3c0c73ee51bc3a144e4748bc4394770160e1f5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3fae8c58da741669e19764e401a7013912e589d9c6d92c5a2945d08fec39a0`  
		Last Modified: Sat, 17 Aug 2024 08:08:47 GMT  
		Size: 45.0 MB (44991185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4462df4c39bb00784ad189022804cc9152913e31a1728620b9825f5e37db6`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 328.3 KB (328336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63189b8e00968cd826a850018fd7d859a1f3fc70ddfb6d4516c68273f24bfc`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af2d83f36bbb6cbe2362215312fb2257d98c0571fb07ca732e3670225b285ce`  
		Last Modified: Sat, 17 Aug 2024 10:18:58 GMT  
		Size: 534.0 MB (534048903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:5229bdb54011ccb83b75a605294105bf6ad307a54bd193aeb1f4d191bac1745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51635983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3553c175911fb7964234b524d8c8c80078eabe0b67efc04c89d26a213eaeddf`

```dockerfile
```

-	Layers:
	-	`sha256:aeacb402431bfa6ff55a78cd09d01abd4370771e4d08f62dea8ade8f17fc0c59`  
		Last Modified: Sat, 17 Aug 2024 10:18:48 GMT  
		Size: 51.6 MB (51626283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7fa283055b38f806101a483b9f8a0201ac9e2c2d009ed5c2d47015e44eed36`  
		Last Modified: Sat, 17 Aug 2024 10:18:46 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:296547d04032cebbf5b8e6e3865f90296f54d91991f340d1e171b42e5a7f1308
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:61702b8c76b4f7c24532bf40434dadfbefadacec0e40b3ebb7bdf7eb6da97eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.2 MB (834220729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2880310d2194c8b1b0e07527bfe69673b02d184809d18dc03fc970c36f1ab444`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fa10f85d04d0836d1a7c22d2ad13e46571f44a1f1dfaee1c674ca2f6095cc`  
		Last Modified: Sat, 17 Aug 2024 05:03:22 GMT  
		Size: 571.2 MB (571159503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:a5efc55a26a40f301d96620861c7499e45720b8b857b5ab5444205d5de54b75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51767830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98782f46dc4a047d83771b48af03e37df75da7fceed5ae0148ddb82875a139e1`

```dockerfile
```

-	Layers:
	-	`sha256:f1ef0f1b81e9d98b666a3e3555d994d0ea061ec9d4b8e8654fcfe0c4869c295b`  
		Last Modified: Sat, 17 Aug 2024 05:03:07 GMT  
		Size: 51.8 MB (51758491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b4f292f9ed120d34bc2ebe984fd67d9a0ae996a1d82d6fda4708e46ce631d0`  
		Last Modified: Sat, 17 Aug 2024 05:03:05 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:43c1a1a7aa88b2a90ca5d55361090ebd99bd55eeb6c1419bf629f840ccd48761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.1 MB (725142418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ce214f07aa17e207f4a073ee0cedfa0620db9f3394cf02b10a158c4ef69ef9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e16c522834ddb11992be720d1f536f974b3e32f7ab85bd13d7c1310ca3f38f`  
		Last Modified: Sat, 17 Aug 2024 05:13:55 GMT  
		Size: 496.9 MB (496869266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:0ec620ced06fd208b24ac804fef70a534967f54ef8402e2f2b44384c690afa17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51401685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba7336350a27cca0d27f6574c74e2523ae2132c9e6e1f630cfc861cbdd36e8`

```dockerfile
```

-	Layers:
	-	`sha256:fd8662e1afe75503280ba88308b9b29d52a06f230a7f865238d04fbbb5ddff2c`  
		Last Modified: Sat, 17 Aug 2024 05:13:46 GMT  
		Size: 51.4 MB (51392285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81db02321b3ccf7bdcb5e82623c68586bc3639f3bea788e07ce7c0b49343c0a4`  
		Last Modified: Sat, 17 Aug 2024 05:13:44 GMT  
		Size: 9.4 KB (9400 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:52c269f692fe649a5e5aa49b82fe3c6305a724049dfaa20dc0ce2f000d9811fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.2 MB (784186089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1130ac47fccd7cf68959033a3c0c73ee51bc3a144e4748bc4394770160e1f5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3fae8c58da741669e19764e401a7013912e589d9c6d92c5a2945d08fec39a0`  
		Last Modified: Sat, 17 Aug 2024 08:08:47 GMT  
		Size: 45.0 MB (44991185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4462df4c39bb00784ad189022804cc9152913e31a1728620b9825f5e37db6`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 328.3 KB (328336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63189b8e00968cd826a850018fd7d859a1f3fc70ddfb6d4516c68273f24bfc`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af2d83f36bbb6cbe2362215312fb2257d98c0571fb07ca732e3670225b285ce`  
		Last Modified: Sat, 17 Aug 2024 10:18:58 GMT  
		Size: 534.0 MB (534048903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:5229bdb54011ccb83b75a605294105bf6ad307a54bd193aeb1f4d191bac1745c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51635983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3553c175911fb7964234b524d8c8c80078eabe0b67efc04c89d26a213eaeddf`

```dockerfile
```

-	Layers:
	-	`sha256:aeacb402431bfa6ff55a78cd09d01abd4370771e4d08f62dea8ade8f17fc0c59`  
		Last Modified: Sat, 17 Aug 2024 10:18:48 GMT  
		Size: 51.6 MB (51626283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7fa283055b38f806101a483b9f8a0201ac9e2c2d009ed5c2d47015e44eed36`  
		Last Modified: Sat, 17 Aug 2024 10:18:46 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:7ee1c28f9dca82cccbf37e3649f9a4c1cb0425df0e5d3712d7d15f33b3a44add
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:782576ce68a671148560414243d698c554b71c0d5e5732ab0a67551891b9a2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279987122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120ea3b748974369b4b335f3a908cb17af118979f4f1ca981ed99f2b742aaf93`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfc686f3bacdc6d32f924080fa2c9086e4dca5aa5bc4df5e2a19a22eb0f047a`  
		Last Modified: Sat, 17 Aug 2024 04:59:58 GMT  
		Size: 16.9 MB (16925896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:51e691c6daa27ca0d8ba6418b61c889745b1d70efd2f3c50bad8f6ef083018ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29477831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6566fd87815ad05f4c558b343f712f9debaa99f7251fb048ec8c070c060f7065`

```dockerfile
```

-	Layers:
	-	`sha256:ea6c8db06c8395b285d065c892c95dc7a26b69195eff8fe9fab97f56545fbe5e`  
		Last Modified: Sat, 17 Aug 2024 04:59:58 GMT  
		Size: 29.5 MB (29468540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da35892a20fd08cba2fda679005f3aa7cdff252699fd45fe3042c3907a97129`  
		Last Modified: Sat, 17 Aug 2024 04:59:57 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:7d2352b6140d728f1e573022b42a0cb67f83b7a8bba3286c3625831baa01f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243300002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a83584ed1b81627427c8bdb844db2b2b658b29474bd71073e8b39f40e4b478`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6a18f856b355e0ec84a29e8e96a61a46a967df36166795808e267c55320ad`  
		Last Modified: Sat, 17 Aug 2024 05:00:52 GMT  
		Size: 15.0 MB (15026850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:271ff5877fec192e3772389613e043bae0a6f6e6c525abb56737c71f3646af1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29232681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5901a0ea2f264d312d555165dd539667f0a02236f32058bd527082a058f35c`

```dockerfile
```

-	Layers:
	-	`sha256:324a40922421be6b149c6b5fbb6fca3a145f735321a70d86d237d946952d6201`  
		Last Modified: Sat, 17 Aug 2024 05:00:53 GMT  
		Size: 29.2 MB (29223330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b2b57eec9e4954db17498f45f2c516ff4f112bf1a137edb439b84268a599fb`  
		Last Modified: Sat, 17 Aug 2024 05:00:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1a3c0d4e297f31360238260d9a859bc10d38ba3ff22ca9cb5969f8da575a4f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266662371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4506b056c3330abf2a0f07c4d6a2cc3874a1b08f7f4a0e6acbf7ef1aab15526d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3fae8c58da741669e19764e401a7013912e589d9c6d92c5a2945d08fec39a0`  
		Last Modified: Sat, 17 Aug 2024 08:08:47 GMT  
		Size: 45.0 MB (44991185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4462df4c39bb00784ad189022804cc9152913e31a1728620b9825f5e37db6`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 328.3 KB (328336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63189b8e00968cd826a850018fd7d859a1f3fc70ddfb6d4516c68273f24bfc`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad978fac46dd2ae03e61a4d06527676e590ee5fd92f680338b0ca24cb150d16`  
		Last Modified: Sat, 17 Aug 2024 10:07:34 GMT  
		Size: 16.5 MB (16525185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:0fab2a858dd27b6a8775b7c1ac0304440b858bfb805496137ed78c07e9b19627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29427325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e6ff6d8b16f79d758ac21b1852217263a9308b6db32c4a2d20e309f6f11dcd`

```dockerfile
```

-	Layers:
	-	`sha256:9478704946463e823a8c26500c0cb5c3909c1427c390791aa626c66927deb906`  
		Last Modified: Sat, 17 Aug 2024 10:07:34 GMT  
		Size: 29.4 MB (29417674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a43568ce067acc1dd8c1e06a70ac1787d8ecfea3ee93d3d87c7ddb59773695`  
		Last Modified: Sat, 17 Aug 2024 10:07:33 GMT  
		Size: 9.7 KB (9651 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:7ee1c28f9dca82cccbf37e3649f9a4c1cb0425df0e5d3712d7d15f33b3a44add
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:782576ce68a671148560414243d698c554b71c0d5e5732ab0a67551891b9a2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279987122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120ea3b748974369b4b335f3a908cb17af118979f4f1ca981ed99f2b742aaf93`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfc686f3bacdc6d32f924080fa2c9086e4dca5aa5bc4df5e2a19a22eb0f047a`  
		Last Modified: Sat, 17 Aug 2024 04:59:58 GMT  
		Size: 16.9 MB (16925896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:51e691c6daa27ca0d8ba6418b61c889745b1d70efd2f3c50bad8f6ef083018ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29477831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6566fd87815ad05f4c558b343f712f9debaa99f7251fb048ec8c070c060f7065`

```dockerfile
```

-	Layers:
	-	`sha256:ea6c8db06c8395b285d065c892c95dc7a26b69195eff8fe9fab97f56545fbe5e`  
		Last Modified: Sat, 17 Aug 2024 04:59:58 GMT  
		Size: 29.5 MB (29468540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da35892a20fd08cba2fda679005f3aa7cdff252699fd45fe3042c3907a97129`  
		Last Modified: Sat, 17 Aug 2024 04:59:57 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:7d2352b6140d728f1e573022b42a0cb67f83b7a8bba3286c3625831baa01f5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243300002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a83584ed1b81627427c8bdb844db2b2b658b29474bd71073e8b39f40e4b478`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6a18f856b355e0ec84a29e8e96a61a46a967df36166795808e267c55320ad`  
		Last Modified: Sat, 17 Aug 2024 05:00:52 GMT  
		Size: 15.0 MB (15026850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:271ff5877fec192e3772389613e043bae0a6f6e6c525abb56737c71f3646af1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29232681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5901a0ea2f264d312d555165dd539667f0a02236f32058bd527082a058f35c`

```dockerfile
```

-	Layers:
	-	`sha256:324a40922421be6b149c6b5fbb6fca3a145f735321a70d86d237d946952d6201`  
		Last Modified: Sat, 17 Aug 2024 05:00:53 GMT  
		Size: 29.2 MB (29223330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b2b57eec9e4954db17498f45f2c516ff4f112bf1a137edb439b84268a599fb`  
		Last Modified: Sat, 17 Aug 2024 05:00:51 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1a3c0d4e297f31360238260d9a859bc10d38ba3ff22ca9cb5969f8da575a4f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266662371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4506b056c3330abf2a0f07c4d6a2cc3874a1b08f7f4a0e6acbf7ef1aab15526d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3fae8c58da741669e19764e401a7013912e589d9c6d92c5a2945d08fec39a0`  
		Last Modified: Sat, 17 Aug 2024 08:08:47 GMT  
		Size: 45.0 MB (44991185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4462df4c39bb00784ad189022804cc9152913e31a1728620b9825f5e37db6`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 328.3 KB (328336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63189b8e00968cd826a850018fd7d859a1f3fc70ddfb6d4516c68273f24bfc`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad978fac46dd2ae03e61a4d06527676e590ee5fd92f680338b0ca24cb150d16`  
		Last Modified: Sat, 17 Aug 2024 10:07:34 GMT  
		Size: 16.5 MB (16525185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:0fab2a858dd27b6a8775b7c1ac0304440b858bfb805496137ed78c07e9b19627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29427325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e6ff6d8b16f79d758ac21b1852217263a9308b6db32c4a2d20e309f6f11dcd`

```dockerfile
```

-	Layers:
	-	`sha256:9478704946463e823a8c26500c0cb5c3909c1427c390791aa626c66927deb906`  
		Last Modified: Sat, 17 Aug 2024 10:07:34 GMT  
		Size: 29.4 MB (29417674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a43568ce067acc1dd8c1e06a70ac1787d8ecfea3ee93d3d87c7ddb59773695`  
		Last Modified: Sat, 17 Aug 2024 10:07:33 GMT  
		Size: 9.7 KB (9651 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:e3866df3b9798c4f3b49946d61b179745a22409ee8ce7037411ea550581b12b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:c7631b6323509f943142bd494abf268127a6807d81bd75e5f1fec2e0cd2caf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263061226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408a67701899f969b3e60f4a0eb58d35defafadadb7f564aadcd939bac6d28d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fc58b4b5b47a9daf00a015010b9c405b2bee15fbcedb748dc03ec81728c088fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27594860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4332305b98df7ac49ef214202dd987420519c390e070c0a75a3ae2192efc6d46`

```dockerfile
```

-	Layers:
	-	`sha256:89609352396b765399d331c17b049a4903d13cc7b7165511bde21d8a061ce2e3`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 27.6 MB (27581208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783f1ac79ac7347d7269a070e63dd8d785bba5a1bf91955cdf05d7a0faac1760`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:16f26c7d44fbd3cf3d9e035ff76de360e992cf6fc7e4254290980286774ed4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0057b00ee435f96c6f5be12c690f3189f8a289111f5b5915f940befb9a00f0fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:2df235d55b1f2af746ffc7217df4e45535de5e5073e1f5827e6105ab6b528b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c37f348b239028298251d0b86d1db02d5b50229cf5448fcdec29b57d7514c3`

```dockerfile
```

-	Layers:
	-	`sha256:e2a7dbfd0c788d3bf5679e89cf1b8f0005ab4953a8d6db188b14521177558656`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 27.3 MB (27344563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df22184734123eb54b635454f9e7340cea27496039962e972936a206f75ac5`  
		Last Modified: Sat, 17 Aug 2024 04:37:55 GMT  
		Size: 13.7 KB (13746 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:52faca237a809534ad5a7ed7e690f03870c886d409b7f36a7f023fb2c78c8dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250137186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbafa4ad53ba861e563d273562d8bbd9284277009490126a216ac061454a7f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3fae8c58da741669e19764e401a7013912e589d9c6d92c5a2945d08fec39a0`  
		Last Modified: Sat, 17 Aug 2024 08:08:47 GMT  
		Size: 45.0 MB (44991185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4462df4c39bb00784ad189022804cc9152913e31a1728620b9825f5e37db6`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 328.3 KB (328336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63189b8e00968cd826a850018fd7d859a1f3fc70ddfb6d4516c68273f24bfc`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:a219de600f12d49f47f8089bc52b3165408aaa6070138f27f22a39ff303b087f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27545519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a116aa9d4e62e43f62651071e3f03b94f410287307399f9d5720fd6c2301ec1`

```dockerfile
```

-	Layers:
	-	`sha256:1a0b2c900c0ff7aad65d97a32d6e5662f1d7e4024119511fa37f056621ed90cb`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 27.5 MB (27531494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a73d809fe4276e42d11adc9d11be29140cfcd3d3a7f66d41a1a0d703466f9519`  
		Last Modified: Sat, 17 Aug 2024 08:08:45 GMT  
		Size: 14.0 KB (14025 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:e3866df3b9798c4f3b49946d61b179745a22409ee8ce7037411ea550581b12b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:c7631b6323509f943142bd494abf268127a6807d81bd75e5f1fec2e0cd2caf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263061226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d408a67701899f969b3e60f4a0eb58d35defafadadb7f564aadcd939bac6d28d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0e1c2116ea193696e706d7e522e8734c145bde845b1e23757ae4a1e79f517`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 50.7 MB (50728255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e04836e938964031c6a92b804724699bc0fb9a19c80000b5eb8202c599b31`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 328.3 KB (328338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dedf7912386e5fff2200861dc2a661c674973a16adea60846d003e1d5df81e`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 915.8 KB (915827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:fc58b4b5b47a9daf00a015010b9c405b2bee15fbcedb748dc03ec81728c088fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27594860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4332305b98df7ac49ef214202dd987420519c390e070c0a75a3ae2192efc6d46`

```dockerfile
```

-	Layers:
	-	`sha256:89609352396b765399d331c17b049a4903d13cc7b7165511bde21d8a061ce2e3`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 27.6 MB (27581208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783f1ac79ac7347d7269a070e63dd8d785bba5a1bf91955cdf05d7a0faac1760`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 13.7 KB (13652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:16f26c7d44fbd3cf3d9e035ff76de360e992cf6fc7e4254290980286774ed4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0057b00ee435f96c6f5be12c690f3189f8a289111f5b5915f940befb9a00f0fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d6f061535974ce1582fd76c9910d7fd670edf53b55ac955db57c869f02f18`  
		Last Modified: Sat, 17 Aug 2024 04:37:57 GMT  
		Size: 40.3 MB (40292650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b427e244d36741bc4e25da9222a29d90c644a6e2b7eb302b1839c043257d2c`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 328.3 KB (328341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32177d81bb3648ab8f2b93d17bce9cca177ce79e644fa951d22f6906d1f2ed`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 848.2 KB (848180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:2df235d55b1f2af746ffc7217df4e45535de5e5073e1f5827e6105ab6b528b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c37f348b239028298251d0b86d1db02d5b50229cf5448fcdec29b57d7514c3`

```dockerfile
```

-	Layers:
	-	`sha256:e2a7dbfd0c788d3bf5679e89cf1b8f0005ab4953a8d6db188b14521177558656`  
		Last Modified: Sat, 17 Aug 2024 04:37:56 GMT  
		Size: 27.3 MB (27344563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df22184734123eb54b635454f9e7340cea27496039962e972936a206f75ac5`  
		Last Modified: Sat, 17 Aug 2024 04:37:55 GMT  
		Size: 13.7 KB (13746 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:52faca237a809534ad5a7ed7e690f03870c886d409b7f36a7f023fb2c78c8dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250137186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbafa4ad53ba861e563d273562d8bbd9284277009490126a216ac061454a7f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3fae8c58da741669e19764e401a7013912e589d9c6d92c5a2945d08fec39a0`  
		Last Modified: Sat, 17 Aug 2024 08:08:47 GMT  
		Size: 45.0 MB (44991185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4462df4c39bb00784ad189022804cc9152913e31a1728620b9825f5e37db6`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 328.3 KB (328336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b63189b8e00968cd826a850018fd7d859a1f3fc70ddfb6d4516c68273f24bfc`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:a219de600f12d49f47f8089bc52b3165408aaa6070138f27f22a39ff303b087f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27545519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a116aa9d4e62e43f62651071e3f03b94f410287307399f9d5720fd6c2301ec1`

```dockerfile
```

-	Layers:
	-	`sha256:1a0b2c900c0ff7aad65d97a32d6e5662f1d7e4024119511fa37f056621ed90cb`  
		Last Modified: Sat, 17 Aug 2024 08:08:46 GMT  
		Size: 27.5 MB (27531494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a73d809fe4276e42d11adc9d11be29140cfcd3d3a7f66d41a1a0d703466f9519`  
		Last Modified: Sat, 17 Aug 2024 08:08:45 GMT  
		Size: 14.0 KB (14025 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:862408ffdd836eb441b3726f158a32f6d4e26f49fbda5c822716d55f43412d5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e53f9fd13c91747c3515c3a85ec56075ca7a514c7363dd29953d77ac708f8dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211088806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe3ea8df787b305e82b2bd150ac62029c175de520cc4fca5d1490d13d0dfd8f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:a4e2fa817226360c08f935434f280eb5a49849f7f4dc958e22c7b7711f2f4210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26121031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbdbe4497382e951d563205769c7e00cdcae3e8f15d3e596005f0867842703e`

```dockerfile
```

-	Layers:
	-	`sha256:d2b59b2b3a4fd0107e0bd00551ec211c29f8bdfe60388c4dcdbc1ed618298383`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 26.1 MB (26104908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d146ee1d613fa1acb9052c4a59df7684f02365809983d3c50230410d30ea24f`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:118b7e318e80c9dd3db19659dff04d5107aeffae11996479a82e754068453b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186803981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7c5d9d36881fa46bfc4649c88bf8f8dee70baa13ba302d2691541912d50788`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:21a8376f977d52d40e9d2cffeabec7480b581e6ceb642a21b3021472d11d2456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26034665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a411540f87187a5e5e162dc7de95bf53077c7cab2c2f30da58dfe6fdd72ae7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e3adc4cfcbbd695b5327ec7f9d53d37d956a2c3b800c0a9b7ace83695460f42`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 26.0 MB (26018436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea628ace720a446206b95a7fa4e06b7e2993d45b4e449009ad3fb9862346a40`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 16.2 KB (16229 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:743c284f23157c9b9e31d8c0bc92b6d4904a4c7ddcbf41bd57a18d090b97e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203920434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7c68ab0f0ecb313bd8476adbbe7e0c0cfecf5121d5b77285634f1ed2c73aab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:5cef2541aa51813d10e953f0912d6c9ec4d28cb577d39ce2a429d0d4cae1e5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26043384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61bf9369c405e592cb2e925f090da05fab2f7a50ada788ede74c4467a12c5e1`

```dockerfile
```

-	Layers:
	-	`sha256:366c9d783c5112c0dd3d6cb62743e0899d4ebd6f826464098f3084ef8fd5a811`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 26.0 MB (26026984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea59315c8c8a4a4b588dce50f045ac53a273b4c0f28923941f667eae1dbf9f4`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:862408ffdd836eb441b3726f158a32f6d4e26f49fbda5c822716d55f43412d5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:e53f9fd13c91747c3515c3a85ec56075ca7a514c7363dd29953d77ac708f8dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211088806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe3ea8df787b305e82b2bd150ac62029c175de520cc4fca5d1490d13d0dfd8f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20df0a8340b8bcf1285d4a7c67eb16091bce74308aa3b8464b13312afa09ba0c`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 1.2 MB (1198607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e280bc16345f9fd184cb4d7324b5badbf008062aedbc346a5d3919fec60c857`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 5.4 MB (5361685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2c1a1a49864ec107fe318830613b909190e6cc3d10a8eeee02e7c85acdedd9`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7522651d5ed283e3b6d0ef85572ef9dea0fd4685ce2557987c0e421616c80dda`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3ddd46c8e3c22e9ca7bb92dda2933ea24f22e4120389d712e9295a1f78476`  
		Last Modified: Sat, 17 Aug 2024 02:03:03 GMT  
		Size: 177.0 MB (177014279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97dc3bb0e280c2ffbbff666ea4601abe3d6a7d3301bf4f008e55baaf4e83bf4`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:a4e2fa817226360c08f935434f280eb5a49849f7f4dc958e22c7b7711f2f4210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26121031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbdbe4497382e951d563205769c7e00cdcae3e8f15d3e596005f0867842703e`

```dockerfile
```

-	Layers:
	-	`sha256:d2b59b2b3a4fd0107e0bd00551ec211c29f8bdfe60388c4dcdbc1ed618298383`  
		Last Modified: Sat, 17 Aug 2024 02:03:00 GMT  
		Size: 26.1 MB (26104908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d146ee1d613fa1acb9052c4a59df7684f02365809983d3c50230410d30ea24f`  
		Last Modified: Sat, 17 Aug 2024 02:02:59 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:118b7e318e80c9dd3db19659dff04d5107aeffae11996479a82e754068453b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186803981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7c5d9d36881fa46bfc4649c88bf8f8dee70baa13ba302d2691541912d50788`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fb9c859c31b986dc92d2134d764c84842dec5c6f0e6c22ac27a6532417df5a7`  
		Last Modified: Tue, 13 Aug 2024 10:24:01 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d18a59233af0864a62e4be8c895f18f9b075e73d479e6a73b1f0aa91bbee3`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 1.2 MB (1200157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc03d008acfec2cade1208ac5a8e213e2752dad64bcf6d1376c65a9b8aad20`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 4.5 MB (4488691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d647f24348c227157165960f086547ede23fcd0e9e2475c61e3cb8b3061a551c`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a43be1539a269308263c4af916a154f7d6202f5972c14a1c72c5c60ced0410`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e044e4d7806c87ef08a5ecf0a644f636ad808f2954e204ddbc147ad6dfe0e6f`  
		Last Modified: Sat, 17 Aug 2024 02:24:21 GMT  
		Size: 157.5 MB (157489282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362a54d6d6c7970caae45140a289b8fd7e822bd73c79dcaf46e82c253347da08`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:21a8376f977d52d40e9d2cffeabec7480b581e6ceb642a21b3021472d11d2456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26034665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a411540f87187a5e5e162dc7de95bf53077c7cab2c2f30da58dfe6fdd72ae7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e3adc4cfcbbd695b5327ec7f9d53d37d956a2c3b800c0a9b7ace83695460f42`  
		Last Modified: Sat, 17 Aug 2024 02:24:17 GMT  
		Size: 26.0 MB (26018436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea628ace720a446206b95a7fa4e06b7e2993d45b4e449009ad3fb9862346a40`  
		Last Modified: Sat, 17 Aug 2024 02:24:16 GMT  
		Size: 16.2 KB (16229 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:743c284f23157c9b9e31d8c0bc92b6d4904a4c7ddcbf41bd57a18d090b97e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203920434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7c68ab0f0ecb313bd8476adbbe7e0c0cfecf5121d5b77285634f1ed2c73aab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37125b5cdd78f80b03aafa631ad5b64d38e81669533f23dc9a9b1906fabe382f`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 1.2 MB (1198578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58296f934ce0acc22125493bc6b7a6fd435583bd42b527cc56f35351b71320`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 5.3 MB (5341984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0f3f7eb5eb353fee01c58028cbf7e98f6b21140b10d1133ce5b48f24fabc5`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ffa9bc8f96fdc6dc62611efd48fb123e3abe52ad2d6c424fb376d820b07952`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6cee76faab3ae6cfb93fb6ca791567d23dfa316c19dc2b98870ab63d6103a0`  
		Last Modified: Sat, 17 Aug 2024 03:55:01 GMT  
		Size: 171.4 MB (171403185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a99af8cf44ec323f546f22351cb43591ad95d73eeb34264ec278b49f3e071ec`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:5cef2541aa51813d10e953f0912d6c9ec4d28cb577d39ce2a429d0d4cae1e5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26043384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61bf9369c405e592cb2e925f090da05fab2f7a50ada788ede74c4467a12c5e1`

```dockerfile
```

-	Layers:
	-	`sha256:366c9d783c5112c0dd3d6cb62743e0899d4ebd6f826464098f3084ef8fd5a811`  
		Last Modified: Sat, 17 Aug 2024 03:54:57 GMT  
		Size: 26.0 MB (26026984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea59315c8c8a4a4b588dce50f045ac53a273b4c0f28923941f667eae1dbf9f4`  
		Last Modified: Sat, 17 Aug 2024 03:54:56 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:b01cd7e9d50e94f7cc49c21f678c44eee57f33bfa65c08ec47aeaa3e6671c3cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:996f92c60bd09b8f53044c7fde439f7dd29198a00e636729def7e62b6d657701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301021444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a45f4801129516dcf117676228e2bd5cdb416b1380da6ad4412c17bee974d`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea468ce4d6726e6249b698710a216b6451300bb0b8f0db95a23bea1cc36c220`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 683.2 KB (683185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09db84bd7ce6f19fa188382e892629d263d9eb2765d06b83284b4c344420e7`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 3.6 MB (3559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553618b115e04a0e0ed5aba56a6122e8dd3d8802fb5701bb102ba439a047a18`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9492c5d1be31b86346623af378f7ccbea92f756729c322f1478d81949c34e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb268c89e7dd0a796ba37f4edfd170c91e8bd89378d62f7fe277481cd497600e`  
		Last Modified: Tue, 17 Sep 2024 01:01:18 GMT  
		Size: 125.1 MB (125056898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3886af81a66bd7e358cdb7a6928ea323ee4bde5dda9ef5048d45cae3327156`  
		Last Modified: Tue, 17 Sep 2024 01:01:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4b605a96dad984d6f6d44736e0781fb44f40a42494c61f4b592540d4d0533c`  
		Last Modified: Tue, 17 Sep 2024 01:58:56 GMT  
		Size: 114.1 MB (114118324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f77a16200a9735ad4fd69fa08adb5a87c0ceaed92fd225ffc2613ee2e0d57c1`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f95d60fb7276439314b252ed9be57377912f470fd4ae76fcfebabc4bd7826e`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f98cab3b6517823eae319e8222596dcfd4850d36c0cdbb808b8814a387f25`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 27.5 MB (27526899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:cdef78d2e495b1a5b1effe6edd88fb43dfddb84ec7c05d7c467fc2326f9bfe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23862654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c07a57643b1a96636f7735179c1021db273e77fcb0bbae2af07e6d01f03773`

```dockerfile
```

-	Layers:
	-	`sha256:3ab282fd77006fa12654f991c36ba36c81b332e2fe4dbc54e3dadf4bf73ef9e2`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 23.8 MB (23845515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87648a82909dfd121e60111879464d3f2a7babd73943151464defeed4f8395fb`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d71c39cb6b63156baffdb7a5b8d45912751d5f5ace4928d2b9a55363f23bba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290754161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b36aa65569365a24aa1f971f13125c60fa7b0dcd65486a6f8172de3a62fb4d4`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15327493c6dd53eeca04df48c98b782b1bfba24702812756c9b9924914b51dd`  
		Last Modified: Tue, 17 Sep 2024 03:07:38 GMT  
		Size: 119.7 MB (119673861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570423f4f1ba76651d92dfa91d35f99b190496f3284f7f78a84928c7e1d0a826`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3a3e4a34e633e0ae3ecc340c7da0f9f3e82dfd31ca88b883cb9f8981cee21`  
		Last Modified: Tue, 17 Sep 2024 06:18:16 GMT  
		Size: 111.0 MB (110959230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68216777387a38d479338b542d4ee354502e97cb5dc91de386b7484105b32d50`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639b477f8bac49ad74bd4d971d0df8e3b83a3fa71d5285c1549d2457d638a18`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689cc2dc2897eeb8b429ed9b70b4d02255aad2640d936450a544d1fa3849c714`  
		Last Modified: Tue, 17 Sep 2024 06:18:14 GMT  
		Size: 26.7 MB (26666417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:b20dfc6ab55d2f07f4abb3e397eb573a0325537044898cc11391e4ef1dabff5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23885700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbab634007531fbe64697dfbefda0e300b6baad6ad9a722e0da9b736ea1d2575`

```dockerfile
```

-	Layers:
	-	`sha256:a2f40ad0a51c075df1e190b5a9675cb8e8c642dc8518a986ff2c855efbd44c33`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 23.9 MB (23868188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25536249a626d79d47197e21de3ed252e6d219fdf5af607cbf73b1f158a92f1e`  
		Last Modified: Tue, 17 Sep 2024 06:18:12 GMT  
		Size: 17.5 KB (17512 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:783ff5fc337e6f74a6e0cb434568eb77176689e4f6fd84e9a790dbffa48a96e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:ad74a2a7dcb1815f9a1018f4ab30ee78f7e2aeb76dcf04d5519c3f8bdf2cc924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624867892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ebd3bb9e89b8c600cc6b7a5a6fbd07a3ce2cbaeb1c7117813d3fc24b8ca201`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea468ce4d6726e6249b698710a216b6451300bb0b8f0db95a23bea1cc36c220`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 683.2 KB (683185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09db84bd7ce6f19fa188382e892629d263d9eb2765d06b83284b4c344420e7`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 3.6 MB (3559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553618b115e04a0e0ed5aba56a6122e8dd3d8802fb5701bb102ba439a047a18`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9492c5d1be31b86346623af378f7ccbea92f756729c322f1478d81949c34e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb268c89e7dd0a796ba37f4edfd170c91e8bd89378d62f7fe277481cd497600e`  
		Last Modified: Tue, 17 Sep 2024 01:01:18 GMT  
		Size: 125.1 MB (125056898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3886af81a66bd7e358cdb7a6928ea323ee4bde5dda9ef5048d45cae3327156`  
		Last Modified: Tue, 17 Sep 2024 01:01:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4b605a96dad984d6f6d44736e0781fb44f40a42494c61f4b592540d4d0533c`  
		Last Modified: Tue, 17 Sep 2024 01:58:56 GMT  
		Size: 114.1 MB (114118324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f77a16200a9735ad4fd69fa08adb5a87c0ceaed92fd225ffc2613ee2e0d57c1`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f95d60fb7276439314b252ed9be57377912f470fd4ae76fcfebabc4bd7826e`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f98cab3b6517823eae319e8222596dcfd4850d36c0cdbb808b8814a387f25`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 27.5 MB (27526899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1ad02a528230401a48684b4a948613aeb393e6717ea6544cde85fc9f715aa1`  
		Last Modified: Tue, 17 Sep 2024 03:03:18 GMT  
		Size: 323.8 MB (323846448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e990cc82764b30f37fec9c1f5931330849ae62a65ec5546dfb91ccbeb1c20352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42136334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3a8e22f08fc690434d972d528a92853ba42227adabfe89720fc890aa0ac941`

```dockerfile
```

-	Layers:
	-	`sha256:c57118ff9c9d4471bacbc31ecbb9537c98a0f0a1b7fcf36e4761b4d6e1fa174a`  
		Last Modified: Tue, 17 Sep 2024 03:03:14 GMT  
		Size: 42.1 MB (42126658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9287123322f645739abc85bcb379154409782f1184901d9678934553c4107a6f`  
		Last Modified: Tue, 17 Sep 2024 03:03:13 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f851921a94ea1df27f4f7331ebd28c6514497cd697c08622f0a6036c750e0b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.7 MB (567746100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892beca8c7f9b20d171f2b8789d277f9b5c5c06af6708ee29dfeca965c049d7c`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15327493c6dd53eeca04df48c98b782b1bfba24702812756c9b9924914b51dd`  
		Last Modified: Tue, 17 Sep 2024 03:07:38 GMT  
		Size: 119.7 MB (119673861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570423f4f1ba76651d92dfa91d35f99b190496f3284f7f78a84928c7e1d0a826`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3a3e4a34e633e0ae3ecc340c7da0f9f3e82dfd31ca88b883cb9f8981cee21`  
		Last Modified: Tue, 17 Sep 2024 06:18:16 GMT  
		Size: 111.0 MB (110959230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68216777387a38d479338b542d4ee354502e97cb5dc91de386b7484105b32d50`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639b477f8bac49ad74bd4d971d0df8e3b83a3fa71d5285c1549d2457d638a18`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689cc2dc2897eeb8b429ed9b70b4d02255aad2640d936450a544d1fa3849c714`  
		Last Modified: Tue, 17 Sep 2024 06:18:14 GMT  
		Size: 26.7 MB (26666417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a2aaecfd712d989271a79d7d1ce0bd52def4138d984163622896c268187394`  
		Last Modified: Tue, 17 Sep 2024 08:10:19 GMT  
		Size: 277.0 MB (276991939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:d13f3dc3ac6d85040565d4b66d7551e34e0ed3b278f27bb26452e6b04d34ba92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42134788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57e84e899b8ef57488aee5812b1e1a86092db7b9ba25a77c7d5994147a96c98`

```dockerfile
```

-	Layers:
	-	`sha256:4342cffcfc95ef3c91f7ad6fb20397f0219a293598b438b0a6faefc0292ceafd`  
		Last Modified: Tue, 17 Sep 2024 08:10:14 GMT  
		Size: 42.1 MB (42124751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c9fa345bf7c5de14c5591e9dbecb063428ce648b7b5cedf5c90820aa43b67f`  
		Last Modified: Tue, 17 Sep 2024 08:10:13 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:783ff5fc337e6f74a6e0cb434568eb77176689e4f6fd84e9a790dbffa48a96e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:ad74a2a7dcb1815f9a1018f4ab30ee78f7e2aeb76dcf04d5519c3f8bdf2cc924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624867892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ebd3bb9e89b8c600cc6b7a5a6fbd07a3ce2cbaeb1c7117813d3fc24b8ca201`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea468ce4d6726e6249b698710a216b6451300bb0b8f0db95a23bea1cc36c220`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 683.2 KB (683185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09db84bd7ce6f19fa188382e892629d263d9eb2765d06b83284b4c344420e7`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 3.6 MB (3559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553618b115e04a0e0ed5aba56a6122e8dd3d8802fb5701bb102ba439a047a18`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9492c5d1be31b86346623af378f7ccbea92f756729c322f1478d81949c34e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb268c89e7dd0a796ba37f4edfd170c91e8bd89378d62f7fe277481cd497600e`  
		Last Modified: Tue, 17 Sep 2024 01:01:18 GMT  
		Size: 125.1 MB (125056898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3886af81a66bd7e358cdb7a6928ea323ee4bde5dda9ef5048d45cae3327156`  
		Last Modified: Tue, 17 Sep 2024 01:01:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4b605a96dad984d6f6d44736e0781fb44f40a42494c61f4b592540d4d0533c`  
		Last Modified: Tue, 17 Sep 2024 01:58:56 GMT  
		Size: 114.1 MB (114118324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f77a16200a9735ad4fd69fa08adb5a87c0ceaed92fd225ffc2613ee2e0d57c1`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f95d60fb7276439314b252ed9be57377912f470fd4ae76fcfebabc4bd7826e`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f98cab3b6517823eae319e8222596dcfd4850d36c0cdbb808b8814a387f25`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 27.5 MB (27526899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1ad02a528230401a48684b4a948613aeb393e6717ea6544cde85fc9f715aa1`  
		Last Modified: Tue, 17 Sep 2024 03:03:18 GMT  
		Size: 323.8 MB (323846448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e990cc82764b30f37fec9c1f5931330849ae62a65ec5546dfb91ccbeb1c20352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42136334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3a8e22f08fc690434d972d528a92853ba42227adabfe89720fc890aa0ac941`

```dockerfile
```

-	Layers:
	-	`sha256:c57118ff9c9d4471bacbc31ecbb9537c98a0f0a1b7fcf36e4761b4d6e1fa174a`  
		Last Modified: Tue, 17 Sep 2024 03:03:14 GMT  
		Size: 42.1 MB (42126658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9287123322f645739abc85bcb379154409782f1184901d9678934553c4107a6f`  
		Last Modified: Tue, 17 Sep 2024 03:03:13 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f851921a94ea1df27f4f7331ebd28c6514497cd697c08622f0a6036c750e0b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.7 MB (567746100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892beca8c7f9b20d171f2b8789d277f9b5c5c06af6708ee29dfeca965c049d7c`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15327493c6dd53eeca04df48c98b782b1bfba24702812756c9b9924914b51dd`  
		Last Modified: Tue, 17 Sep 2024 03:07:38 GMT  
		Size: 119.7 MB (119673861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570423f4f1ba76651d92dfa91d35f99b190496f3284f7f78a84928c7e1d0a826`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3a3e4a34e633e0ae3ecc340c7da0f9f3e82dfd31ca88b883cb9f8981cee21`  
		Last Modified: Tue, 17 Sep 2024 06:18:16 GMT  
		Size: 111.0 MB (110959230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68216777387a38d479338b542d4ee354502e97cb5dc91de386b7484105b32d50`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639b477f8bac49ad74bd4d971d0df8e3b83a3fa71d5285c1549d2457d638a18`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689cc2dc2897eeb8b429ed9b70b4d02255aad2640d936450a544d1fa3849c714`  
		Last Modified: Tue, 17 Sep 2024 06:18:14 GMT  
		Size: 26.7 MB (26666417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a2aaecfd712d989271a79d7d1ce0bd52def4138d984163622896c268187394`  
		Last Modified: Tue, 17 Sep 2024 08:10:19 GMT  
		Size: 277.0 MB (276991939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d13f3dc3ac6d85040565d4b66d7551e34e0ed3b278f27bb26452e6b04d34ba92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42134788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57e84e899b8ef57488aee5812b1e1a86092db7b9ba25a77c7d5994147a96c98`

```dockerfile
```

-	Layers:
	-	`sha256:4342cffcfc95ef3c91f7ad6fb20397f0219a293598b438b0a6faefc0292ceafd`  
		Last Modified: Tue, 17 Sep 2024 08:10:14 GMT  
		Size: 42.1 MB (42124751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c9fa345bf7c5de14c5591e9dbecb063428ce648b7b5cedf5c90820aa43b67f`  
		Last Modified: Tue, 17 Sep 2024 08:10:13 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:b01cd7e9d50e94f7cc49c21f678c44eee57f33bfa65c08ec47aeaa3e6671c3cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:996f92c60bd09b8f53044c7fde439f7dd29198a00e636729def7e62b6d657701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301021444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a45f4801129516dcf117676228e2bd5cdb416b1380da6ad4412c17bee974d`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea468ce4d6726e6249b698710a216b6451300bb0b8f0db95a23bea1cc36c220`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 683.2 KB (683185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09db84bd7ce6f19fa188382e892629d263d9eb2765d06b83284b4c344420e7`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 3.6 MB (3559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553618b115e04a0e0ed5aba56a6122e8dd3d8802fb5701bb102ba439a047a18`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9492c5d1be31b86346623af378f7ccbea92f756729c322f1478d81949c34e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb268c89e7dd0a796ba37f4edfd170c91e8bd89378d62f7fe277481cd497600e`  
		Last Modified: Tue, 17 Sep 2024 01:01:18 GMT  
		Size: 125.1 MB (125056898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3886af81a66bd7e358cdb7a6928ea323ee4bde5dda9ef5048d45cae3327156`  
		Last Modified: Tue, 17 Sep 2024 01:01:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4b605a96dad984d6f6d44736e0781fb44f40a42494c61f4b592540d4d0533c`  
		Last Modified: Tue, 17 Sep 2024 01:58:56 GMT  
		Size: 114.1 MB (114118324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f77a16200a9735ad4fd69fa08adb5a87c0ceaed92fd225ffc2613ee2e0d57c1`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f95d60fb7276439314b252ed9be57377912f470fd4ae76fcfebabc4bd7826e`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f98cab3b6517823eae319e8222596dcfd4850d36c0cdbb808b8814a387f25`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 27.5 MB (27526899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:cdef78d2e495b1a5b1effe6edd88fb43dfddb84ec7c05d7c467fc2326f9bfe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23862654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c07a57643b1a96636f7735179c1021db273e77fcb0bbae2af07e6d01f03773`

```dockerfile
```

-	Layers:
	-	`sha256:3ab282fd77006fa12654f991c36ba36c81b332e2fe4dbc54e3dadf4bf73ef9e2`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 23.8 MB (23845515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87648a82909dfd121e60111879464d3f2a7babd73943151464defeed4f8395fb`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d71c39cb6b63156baffdb7a5b8d45912751d5f5ace4928d2b9a55363f23bba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290754161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b36aa65569365a24aa1f971f13125c60fa7b0dcd65486a6f8172de3a62fb4d4`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15327493c6dd53eeca04df48c98b782b1bfba24702812756c9b9924914b51dd`  
		Last Modified: Tue, 17 Sep 2024 03:07:38 GMT  
		Size: 119.7 MB (119673861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570423f4f1ba76651d92dfa91d35f99b190496f3284f7f78a84928c7e1d0a826`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3a3e4a34e633e0ae3ecc340c7da0f9f3e82dfd31ca88b883cb9f8981cee21`  
		Last Modified: Tue, 17 Sep 2024 06:18:16 GMT  
		Size: 111.0 MB (110959230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68216777387a38d479338b542d4ee354502e97cb5dc91de386b7484105b32d50`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639b477f8bac49ad74bd4d971d0df8e3b83a3fa71d5285c1549d2457d638a18`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689cc2dc2897eeb8b429ed9b70b4d02255aad2640d936450a544d1fa3849c714`  
		Last Modified: Tue, 17 Sep 2024 06:18:14 GMT  
		Size: 26.7 MB (26666417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b20dfc6ab55d2f07f4abb3e397eb573a0325537044898cc11391e4ef1dabff5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23885700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbab634007531fbe64697dfbefda0e300b6baad6ad9a722e0da9b736ea1d2575`

```dockerfile
```

-	Layers:
	-	`sha256:a2f40ad0a51c075df1e190b5a9675cb8e8c642dc8518a986ff2c855efbd44c33`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 23.9 MB (23868188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25536249a626d79d47197e21de3ed252e6d219fdf5af607cbf73b1f158a92f1e`  
		Last Modified: Tue, 17 Sep 2024 06:18:12 GMT  
		Size: 17.5 KB (17512 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:b01cd7e9d50e94f7cc49c21f678c44eee57f33bfa65c08ec47aeaa3e6671c3cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:996f92c60bd09b8f53044c7fde439f7dd29198a00e636729def7e62b6d657701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301021444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a45f4801129516dcf117676228e2bd5cdb416b1380da6ad4412c17bee974d`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea468ce4d6726e6249b698710a216b6451300bb0b8f0db95a23bea1cc36c220`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 683.2 KB (683185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09db84bd7ce6f19fa188382e892629d263d9eb2765d06b83284b4c344420e7`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 3.6 MB (3559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553618b115e04a0e0ed5aba56a6122e8dd3d8802fb5701bb102ba439a047a18`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9492c5d1be31b86346623af378f7ccbea92f756729c322f1478d81949c34e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb268c89e7dd0a796ba37f4edfd170c91e8bd89378d62f7fe277481cd497600e`  
		Last Modified: Tue, 17 Sep 2024 01:01:18 GMT  
		Size: 125.1 MB (125056898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3886af81a66bd7e358cdb7a6928ea323ee4bde5dda9ef5048d45cae3327156`  
		Last Modified: Tue, 17 Sep 2024 01:01:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4b605a96dad984d6f6d44736e0781fb44f40a42494c61f4b592540d4d0533c`  
		Last Modified: Tue, 17 Sep 2024 01:58:56 GMT  
		Size: 114.1 MB (114118324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f77a16200a9735ad4fd69fa08adb5a87c0ceaed92fd225ffc2613ee2e0d57c1`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f95d60fb7276439314b252ed9be57377912f470fd4ae76fcfebabc4bd7826e`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f98cab3b6517823eae319e8222596dcfd4850d36c0cdbb808b8814a387f25`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 27.5 MB (27526899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:cdef78d2e495b1a5b1effe6edd88fb43dfddb84ec7c05d7c467fc2326f9bfe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23862654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c07a57643b1a96636f7735179c1021db273e77fcb0bbae2af07e6d01f03773`

```dockerfile
```

-	Layers:
	-	`sha256:3ab282fd77006fa12654f991c36ba36c81b332e2fe4dbc54e3dadf4bf73ef9e2`  
		Last Modified: Tue, 17 Sep 2024 01:58:54 GMT  
		Size: 23.8 MB (23845515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87648a82909dfd121e60111879464d3f2a7babd73943151464defeed4f8395fb`  
		Last Modified: Tue, 17 Sep 2024 01:58:53 GMT  
		Size: 17.1 KB (17139 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d71c39cb6b63156baffdb7a5b8d45912751d5f5ace4928d2b9a55363f23bba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290754161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b36aa65569365a24aa1f971f13125c60fa7b0dcd65486a6f8172de3a62fb4d4`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15327493c6dd53eeca04df48c98b782b1bfba24702812756c9b9924914b51dd`  
		Last Modified: Tue, 17 Sep 2024 03:07:38 GMT  
		Size: 119.7 MB (119673861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570423f4f1ba76651d92dfa91d35f99b190496f3284f7f78a84928c7e1d0a826`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3a3e4a34e633e0ae3ecc340c7da0f9f3e82dfd31ca88b883cb9f8981cee21`  
		Last Modified: Tue, 17 Sep 2024 06:18:16 GMT  
		Size: 111.0 MB (110959230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68216777387a38d479338b542d4ee354502e97cb5dc91de386b7484105b32d50`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 321.9 KB (321893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639b477f8bac49ad74bd4d971d0df8e3b83a3fa71d5285c1549d2457d638a18`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689cc2dc2897eeb8b429ed9b70b4d02255aad2640d936450a544d1fa3849c714`  
		Last Modified: Tue, 17 Sep 2024 06:18:14 GMT  
		Size: 26.7 MB (26666417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b20dfc6ab55d2f07f4abb3e397eb573a0325537044898cc11391e4ef1dabff5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23885700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbab634007531fbe64697dfbefda0e300b6baad6ad9a722e0da9b736ea1d2575`

```dockerfile
```

-	Layers:
	-	`sha256:a2f40ad0a51c075df1e190b5a9675cb8e8c642dc8518a986ff2c855efbd44c33`  
		Last Modified: Tue, 17 Sep 2024 06:18:13 GMT  
		Size: 23.9 MB (23868188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25536249a626d79d47197e21de3ed252e6d219fdf5af607cbf73b1f158a92f1e`  
		Last Modified: Tue, 17 Sep 2024 06:18:12 GMT  
		Size: 17.5 KB (17512 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:79667ca4f60b514836c8805ca16f7b4e1e8ad71e8deb12228e2903f4e11df20c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1a19644a107a2ff162b839830c69aef8424187f44c045fa4fc7de35ff1a16c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159051882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14f993f5655076c3edbab89e59804a041520797fe8fa644f0deb7f8386fe427`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea468ce4d6726e6249b698710a216b6451300bb0b8f0db95a23bea1cc36c220`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 683.2 KB (683185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09db84bd7ce6f19fa188382e892629d263d9eb2765d06b83284b4c344420e7`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 3.6 MB (3559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553618b115e04a0e0ed5aba56a6122e8dd3d8802fb5701bb102ba439a047a18`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9492c5d1be31b86346623af378f7ccbea92f756729c322f1478d81949c34e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb268c89e7dd0a796ba37f4edfd170c91e8bd89378d62f7fe277481cd497600e`  
		Last Modified: Tue, 17 Sep 2024 01:01:18 GMT  
		Size: 125.1 MB (125056898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3886af81a66bd7e358cdb7a6928ea323ee4bde5dda9ef5048d45cae3327156`  
		Last Modified: Tue, 17 Sep 2024 01:01:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f1a4fb4299c246c34bc1c96891d35baa8254ff029c23660e5871e4508fb3e6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17823904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70edd2b7ba4a6755cabb59eb092e27f7587a553f1f955770c07fe7e646741131`

```dockerfile
```

-	Layers:
	-	`sha256:b277e694d9f74d54fdcf2e02da50ea2bac803b75c156c40e90fe131cdf003f7e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 17.8 MB (17807764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371f61b9248390c8d7901033c938de517656df949653e3f374c53d0b3f5607ef`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:04f7eebf6fa2c71eb1a274b78ad75d7ceeed9116e8231dca04c170c8d83da20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152804154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b064c361cfbeaeb7110b9c1b5898e8c6a324308d40b19950d2bf611bb4e8f92`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15327493c6dd53eeca04df48c98b782b1bfba24702812756c9b9924914b51dd`  
		Last Modified: Tue, 17 Sep 2024 03:07:38 GMT  
		Size: 119.7 MB (119673861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570423f4f1ba76651d92dfa91d35f99b190496f3284f7f78a84928c7e1d0a826`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:cb3de657e8fc8276e60be28f57218b923387293dfb56f7ac409c04de0e53b6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17798152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec57b03dfef90517f9faf74f3eaf9b9563df5e95ce010005b60a0e58bd17db`

```dockerfile
```

-	Layers:
	-	`sha256:15b78604c7a083f80132f4ec1196c8346918d92b8d25c032a1d7d9ed4d38d985`  
		Last Modified: Tue, 17 Sep 2024 03:07:35 GMT  
		Size: 17.8 MB (17781735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8cdbee95322ce3ffe68a71f083501e0d5e3a0285d0dde05c0a78daecd30c22f`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 16.4 KB (16417 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:79667ca4f60b514836c8805ca16f7b4e1e8ad71e8deb12228e2903f4e11df20c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:1a19644a107a2ff162b839830c69aef8424187f44c045fa4fc7de35ff1a16c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159051882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14f993f5655076c3edbab89e59804a041520797fe8fa644f0deb7f8386fe427`
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
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
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
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea468ce4d6726e6249b698710a216b6451300bb0b8f0db95a23bea1cc36c220`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 683.2 KB (683185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc09db84bd7ce6f19fa188382e892629d263d9eb2765d06b83284b4c344420e7`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 3.6 MB (3559502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d553618b115e04a0e0ed5aba56a6122e8dd3d8802fb5701bb102ba439a047a18`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9492c5d1be31b86346623af378f7ccbea92f756729c322f1478d81949c34e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb268c89e7dd0a796ba37f4edfd170c91e8bd89378d62f7fe277481cd497600e`  
		Last Modified: Tue, 17 Sep 2024 01:01:18 GMT  
		Size: 125.1 MB (125056898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3886af81a66bd7e358cdb7a6928ea323ee4bde5dda9ef5048d45cae3327156`  
		Last Modified: Tue, 17 Sep 2024 01:01:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f1a4fb4299c246c34bc1c96891d35baa8254ff029c23660e5871e4508fb3e6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17823904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70edd2b7ba4a6755cabb59eb092e27f7587a553f1f955770c07fe7e646741131`

```dockerfile
```

-	Layers:
	-	`sha256:b277e694d9f74d54fdcf2e02da50ea2bac803b75c156c40e90fe131cdf003f7e`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 17.8 MB (17807764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371f61b9248390c8d7901033c938de517656df949653e3f374c53d0b3f5607ef`  
		Last Modified: Tue, 17 Sep 2024 01:01:16 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:04f7eebf6fa2c71eb1a274b78ad75d7ceeed9116e8231dca04c170c8d83da20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152804154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b064c361cfbeaeb7110b9c1b5898e8c6a324308d40b19950d2bf611bb4e8f92`
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
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
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
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ac9b8b68598ae2508c74970152ada13f7a19ce823f6077624e5dd8c1691d`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 683.5 KB (683470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187d8b60463e96958432ea26306d79b77a42e66cbde4fc5ab9c149b48e6a285c`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 3.6 MB (3558753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd43ebb5b559bf7ceaeb61380b377fa8a323f050c1c8d7cc4cfe55c95af5359`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca3bebc1c6b9c4b2be1a479da2d28557c5dadbf9ac1ba834363377acbe46b2`  
		Last Modified: Tue, 17 Sep 2024 03:06:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15327493c6dd53eeca04df48c98b782b1bfba24702812756c9b9924914b51dd`  
		Last Modified: Tue, 17 Sep 2024 03:07:38 GMT  
		Size: 119.7 MB (119673861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570423f4f1ba76651d92dfa91d35f99b190496f3284f7f78a84928c7e1d0a826`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:cb3de657e8fc8276e60be28f57218b923387293dfb56f7ac409c04de0e53b6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17798152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec57b03dfef90517f9faf74f3eaf9b9563df5e95ce010005b60a0e58bd17db`

```dockerfile
```

-	Layers:
	-	`sha256:15b78604c7a083f80132f4ec1196c8346918d92b8d25c032a1d7d9ed4d38d985`  
		Last Modified: Tue, 17 Sep 2024 03:07:35 GMT  
		Size: 17.8 MB (17781735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8cdbee95322ce3ffe68a71f083501e0d5e3a0285d0dde05c0a78daecd30c22f`  
		Last Modified: Tue, 17 Sep 2024 03:07:34 GMT  
		Size: 16.4 KB (16417 bytes)  
		MIME: application/vnd.in-toto+json
