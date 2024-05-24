## `ros:jazzy`

```console
$ docker pull ros@sha256:792f28ddc091984c1b2fcd9f780d0cbb4094accdead971724f4762512dc5c5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:94903a2e6311026989fbe35c31cacd5e509d5a860bc374467d4ed161d39f70b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302117951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de2625d3b31b7c6871791708581b2df681f6937ae7006b2cb3feeab1b0de1d`
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
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
# Fri, 24 May 2024 00:53:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 00:53:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 00:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72deef87e0bd3e2b9fb1b1332ebb772e7570201e69d13a80a786526c9cc825`  
		Last Modified: Fri, 24 May 2024 00:59:36 GMT  
		Size: 114.3 MB (114312618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c3e4cc06ea4818223f482308fe858138535f4b16b60e6ea752908b0c818b13`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 310.6 KB (310567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed492ab0db3f83a748a510c07a2f30f503a9e2a1ef38bf73806def6cc0aca245`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14706106e0f4a9775057016e557106aa7abafdf3f95290bf62f5d740cd66c60`  
		Last Modified: Fri, 24 May 2024 00:59:25 GMT  
		Size: 27.7 MB (27668097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:291f4c0bebacd781250a880a256d8834646030bb6066ec99ec088af1a845df0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292073626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb57bb1324bca2415c246a1b26b2b2ccb527b81e52135e310a9b102acb8c4c4c`
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
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
# Fri, 24 May 2024 01:08:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:08:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 01:08:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 01:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2b8c0b62382bad46d18ffa279fb2e701a853dbc8f1457806b0140841a622a`  
		Last Modified: Fri, 24 May 2024 01:16:08 GMT  
		Size: 111.2 MB (111153710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ace28299c354a7a02a6f44bd73e5385aca4a3b0eb87a26f9fe3eb9c2c322d`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 310.6 KB (310587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dab07297abace30add756a2eac059cf770c1ed9122df19c8d1e4a9ee2a1300`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac06ef535dced021e53c6859dea1ba0d8d0042a2a6ba8ca087d724f3477f397`  
		Last Modified: Fri, 24 May 2024 01:15:59 GMT  
		Size: 26.8 MB (26813058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
