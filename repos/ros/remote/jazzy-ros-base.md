## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:07eeb96e0a7f7ec15ac1babcda01c6fffce99b35225afdfc58495338d0aaa49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:4dfc55090b9b10743aedc99e7c93cc09d9b51f722c8af38e914e62a1f7c9b820
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299700105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73f3fe05768e2e7402741f3a26d528e4fdc1cdfb902de92fdb4ce85a11d9c5c`
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
# Thu, 02 May 2024 04:08:58 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-testing-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:08:59 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-testing-archive-keyring.gpg ] http://packages.ros.org/ros2-testing/ubuntu noble main" > /etc/apt/sources.list.d/ros2-testing.list
# Thu, 02 May 2024 04:08:59 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:08:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:08:59 GMT
ENV ROS_DISTRO=jazzy
# Thu, 02 May 2024 04:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:10:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:10:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:10:47 GMT
CMD ["bash"]
# Thu, 02 May 2024 04:11:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:11:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 04:11:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 04:12:48 GMT
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
	-	`sha256:0f222a4f0f0d169710bf5be1624344cef1bc1c8b5d4e9ba80a78da2f7d7512e3`  
		Last Modified: Thu, 02 May 2024 04:27:56 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892340976301cbeedb196f219d6d5d61e94afd0cedef6b4ac759a17a79cc2cbf`  
		Last Modified: Thu, 02 May 2024 04:27:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df8a6e27e79b2f137d619d477df5cc91bbfd654469743995198ed0a7e601164`  
		Last Modified: Thu, 02 May 2024 04:28:14 GMT  
		Size: 122.4 MB (122412498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0a77993a63310ae001b3fc1bff701bbc23f008a2925d9d275cf18fb4521dab`  
		Last Modified: Thu, 02 May 2024 04:27:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4477c6640986cfaa1a287078d0f5a7bc75b6291651c336087ec82f1167e528fa`  
		Last Modified: Thu, 02 May 2024 04:28:38 GMT  
		Size: 114.3 MB (114305581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22f083021ef1e6ccdea519172a6bb151efe9b2f75bee41afe37c51e5b0bf2ce`  
		Last Modified: Thu, 02 May 2024 04:28:23 GMT  
		Size: 308.4 KB (308375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669d67df7ebffba7b4c408bf2fc48f3d379f9835111248f24c22758dccf31912`  
		Last Modified: Thu, 02 May 2024 04:28:23 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f211ecd56560eb5ab01355befd15402b85d5ddef7e46e364706796b55fff1454`  
		Last Modified: Thu, 02 May 2024 04:28:27 GMT  
		Size: 27.7 MB (27665105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f652c502c971653afc2ed9b9e5929643df644e6125b6ee68349408b6cc2f64cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289845264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89fc1483cf5c6eeff236d365b7d26c5ad583eff3fa6060b304b366a50c588ab`
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
# Thu, 02 May 2024 02:11:43 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-testing-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:11:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-testing-archive-keyring.gpg ] http://packages.ros.org/ros2-testing/ubuntu noble main" > /etc/apt/sources.list.d/ros2-testing.list
# Thu, 02 May 2024 02:11:44 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:11:44 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:11:44 GMT
ENV ROS_DISTRO=jazzy
# Thu, 02 May 2024 02:13:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:13:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:13:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:13:53 GMT
CMD ["bash"]
# Thu, 02 May 2024 02:16:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:16:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:16:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:17:25 GMT
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
	-	`sha256:eb1530a98afb6ca6b735ba21a703b8ab482443c6984b4b5dd57136c4a1245e8f`  
		Last Modified: Thu, 02 May 2024 02:33:08 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b38a3ce2b2fd6079fcf853bc1533d0de85fbcf48949e9b3ee31f9b40f03e59`  
		Last Modified: Thu, 02 May 2024 02:33:08 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82b0c960739bc7a727ac975dffda488d4ba93e271c18d3600c4be19c237167`  
		Last Modified: Thu, 02 May 2024 02:33:32 GMT  
		Size: 117.2 MB (117224625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cff6639496fa69ef9e6bfd477bcec2737b680972d8f76ea9d277e11eb8f1b48`  
		Last Modified: Thu, 02 May 2024 02:33:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd60f30b99627b5549ca5e7bff2775c2b644e0cd30c8b45fc5138151253ebfbb`  
		Last Modified: Thu, 02 May 2024 02:33:53 GMT  
		Size: 111.2 MB (111162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b969bb4bf67906361ad61576a20a059d9585983685fa4627816b5d372617d9`  
		Last Modified: Thu, 02 May 2024 02:33:41 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a916c4b0f1c4cf0a44b3d8f1b0163250de4a881d0f8e26cad5d4f1ec05ba7f`  
		Last Modified: Thu, 02 May 2024 02:33:41 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4b118cd961c3a016019eb79dcaffa47df6bc91d3ee0bbe45774d48d3249d91`  
		Last Modified: Thu, 02 May 2024 02:33:45 GMT  
		Size: 26.8 MB (26810944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
