## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:37a589d8b29165533eb9b365a22f7cc6a02048dfbf6e5bbf943f6db35a3889d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b89df97dd9e57f60e44c3ed8e0555afbf2764d3323051784cb31c2535743c3f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.0 MB (961034771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34638ebbb65a9ff4294af75873c0076a46a3e6c0ab4defe346df6de3495ae411`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:43:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:43:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:45:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e592df8efe0984926f743e834f7746effd90d514f3d3851abe3044c8a61c0`  
		Last Modified: Fri, 16 Feb 2024 02:53:07 GMT  
		Size: 85.2 MB (85170370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82907e5ee200d3fc665288fc89fc9cf64841db34917726251c720cd2178de28`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62501b0855f8ce6c24c8e4011b811b0a788aa94b6bf9a2a64c672fb2dee59828`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6846f1670ef3d1bc2c2f4ac35db04c584f6230744c631aac1531732b9eb6b3`  
		Last Modified: Fri, 16 Feb 2024 02:53:01 GMT  
		Size: 23.7 MB (23731179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b87fc794a6250d680bd9b7b58667af4784b595b7ff1a5911281ff89f9d5bad`  
		Last Modified: Fri, 16 Feb 2024 02:54:51 GMT  
		Size: 692.1 MB (692072545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d3f78400a14896ff5a2805afc40472c40ba3d882a6fca7d99982a6fb2bcce0b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 MB (921354929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0f5150263e592dc4d373e2693757906e86844edd536f4deb50785e7d67bfdc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:32:32 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 05:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:33:26 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:33:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:33:58 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:34:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207bf6d488de8bf4729e007d8eb9410b4b3a38a7c721829786658d178204f07`  
		Last Modified: Fri, 16 Feb 2024 05:42:41 GMT  
		Size: 121.7 MB (121717451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb71cb6cd71fe8fa2e2596589682998757cfdec8fc8da02644abb2d765f0252`  
		Last Modified: Fri, 16 Feb 2024 05:42:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bc779048061a71f1468d53a6c163fdfe916bb3394178b935cd72b13b5cfbf0`  
		Last Modified: Fri, 16 Feb 2024 05:42:58 GMT  
		Size: 82.8 MB (82844209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25527e451a1fe313ae426757e1658152f1cff6a3d0d8099e5b419bd5c9771452`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efc4c25e34e2e5a67ab27e06262274ba4466c2f0f2c5e79436943fe6cfa0e0`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234f1eff56417c7838f77bc1df18e31fe55a3588ebdef5395b13f3fcdeb61300`  
		Last Modified: Fri, 16 Feb 2024 05:42:53 GMT  
		Size: 23.1 MB (23119281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca27c0b368e44e2e47a4108ec308ac6773c88e26d409d337ba04f823d38759c7`  
		Last Modified: Fri, 16 Feb 2024 05:44:26 GMT  
		Size: 660.0 MB (659956328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
