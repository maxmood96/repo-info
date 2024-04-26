## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:5e1f1789c2d963246cb93020672ae57dbfc3a3dbaac57f1319d8cd4b1de59bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:2dbb0a1f7d21ce9b7235242cf7fc85d1bd7e598b293f5bba856523981144a8ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147157534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c8118ed8bd24ca40db916cc29649031004c8a1c63e4ee70dc712023733cd6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eddc3c5f7180b6bf9ab2128cf3231c74367a99f019f8e8b42e09941e79b56cbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141721375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70735918669b34ff60aa8774f233b61761fc3ab444ee21fdc83e61b84be2fee6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
