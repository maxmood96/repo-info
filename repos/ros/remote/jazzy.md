## `ros:jazzy`

```console
$ docker pull ros@sha256:41f18a8f86588e379e42f2a6a1f35b9b9173e474699c5cfc5ff76737b10a60da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:7a86535d35141d9c670e3ac22d61820941f668df69c11e74c43108c8ae4d1b7d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299753250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2978d0177f10c303c210a050f03e7067a92a2ea2c7ec247934be9296398871fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV ROS_DISTRO=jazzy
# Mon, 17 Jun 2024 22:53:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:53:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:53:04 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 22:53:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:53:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 22:53:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 22:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb560ba80e4159bbd7ecd0b2b087742543cda4c6a38d6e11962899cf93f2a99`  
		Last Modified: Mon, 17 Jun 2024 23:03:06 GMT  
		Size: 122.4 MB (122449281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1f73baf8579b4bee759b3d8255736d35aaea708c7807937e9fa93672b74912`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663fffed5895f069623e78dd312f447401d9427c7955cbf44a7a5d6e9d1f793b`  
		Last Modified: Mon, 17 Jun 2024 23:03:30 GMT  
		Size: 114.3 MB (114314047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff86107534e43b482d4ed6f953a16a76dea0fd2355e45153fc52cd185d78ce7`  
		Last Modified: Mon, 17 Jun 2024 23:03:16 GMT  
		Size: 314.5 KB (314451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c28d23077d3ae521447fc0ce44530ee13e13395ef0de730f3ee6263b7df0be`  
		Last Modified: Mon, 17 Jun 2024 23:03:15 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e7b1ff4609540214de8a236a1a608ef17ca2d2913bb57f6ee161c6355f305`  
		Last Modified: Mon, 17 Jun 2024 23:03:20 GMT  
		Size: 27.7 MB (27666753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1badf5a00191973b50801c72965fed62d9cd394e275ba8f85a1d51ece2d1146e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289901220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1abcda7e1004e215f1dda94b2e26e0821a85324f8ddfa60827afa098187ac23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:37:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:37:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:37:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:38:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6d52f206ff0a29a3eb7519bdc04d32db2c40e16c511e7ccf45eeb792f1944`  
		Last Modified: Wed, 05 Jun 2024 05:55:58 GMT  
		Size: 111.2 MB (111160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2c06fb4721bb4f54fc284881cc94751c3671444b26cb306c223c1d33004789`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 312.8 KB (312756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73532281aed74c405fee3b771131841982e81415f390ec4db8c64be0e55810f`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cda6cf897fb0f813d993a3a9006e251e903cb04b3386865697fb70974cd143c`  
		Last Modified: Wed, 05 Jun 2024 05:55:49 GMT  
		Size: 26.8 MB (26813698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
