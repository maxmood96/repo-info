## `ros:rolling`

```console
$ docker pull ros@sha256:bdb7718f2185d3d9cf54712c617e0ad82d2f02ae15ccb90f56d0598c242cd9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:ca7ada2bcd35ac04deb8cdda8b2f971321533b3f9e2bbd0b9f8d33005b8f625d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299704572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccfc1148c7c9ae20e4e5a5292c3a1e63673b55903ecd6b8af28ea6a9472466f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV ROS_DISTRO=rolling
# Thu, 02 May 2024 04:17:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:18:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:18:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:18:00 GMT
CMD ["bash"]
# Thu, 02 May 2024 04:18:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:18:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 04:18:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 04:18:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e484ef4424e4b62b917fb7a6d4980f231d1685459e628d5080f9091c5b2456`  
		Last Modified: Thu, 02 May 2024 04:30:00 GMT  
		Size: 122.4 MB (122415848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79989973bd9f0a6fde631f5c045521fd10a6645a57328a68993f0ed4cc2e375`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11bf6acf43f7c5e6841d0732bd150769a2d936ce4044ae9775dba0e155ef6bf`  
		Last Modified: Thu, 02 May 2024 04:30:25 GMT  
		Size: 114.3 MB (114305622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40758d223f42f271f3eb830670bf4c2b9cc898dcd5aa35864500eb72eb98f145`  
		Last Modified: Thu, 02 May 2024 04:30:09 GMT  
		Size: 308.7 KB (308746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace9d99d6167521400d39dda9c24528cd8e174cab8b7f2e0cbba82f5dec2bd6c`  
		Last Modified: Thu, 02 May 2024 04:30:09 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a01497548475d2118d2fcb5a002afea5fd119e767be8c1a5dcf178d08253a7`  
		Last Modified: Thu, 02 May 2024 04:30:13 GMT  
		Size: 27.7 MB (27665794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28918bebd9a511129af137e7ff3d6c14c68c720e24289a08789fd1e3a7dc7980
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289846314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05834fd869cba3632b8eb6eb73a152e5c15da85b0993832bb70fc64c443db503`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Thu, 02 May 2024 02:23:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:23:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:23:49 GMT
CMD ["bash"]
# Thu, 02 May 2024 02:24:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:24:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:24:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:24:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9c27e6b07ed6f6642218c3b8a1eeec6661cffc8a02391bed51154498ab163d`  
		Last Modified: Thu, 02 May 2024 02:35:13 GMT  
		Size: 117.2 MB (117225103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6e9fc856033a2d60a00f8b9c0f2d6cf1af09f0eff1aaaf65b33a4e142a52b`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeee49f272384ea98c1409e784ee434d221d14fc91b442c7ce9a63bf9fe09af`  
		Last Modified: Thu, 02 May 2024 02:35:35 GMT  
		Size: 111.2 MB (111162003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae90260d02fe631fea4319a71d06ce90edb8fb039c93bc235b988ecbb4e6ee1`  
		Last Modified: Thu, 02 May 2024 02:35:22 GMT  
		Size: 308.7 KB (308742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884c3f02d72ee39446f6d04fdebc2167c27296b6b140301f990f00d27f22f20b`  
		Last Modified: Thu, 02 May 2024 02:35:21 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b339374ab1ff5470fd91de8a2ca0ea42e7bb7fffea3c5156c63022eebbaad60d`  
		Last Modified: Thu, 02 May 2024 02:35:26 GMT  
		Size: 26.8 MB (26811230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
