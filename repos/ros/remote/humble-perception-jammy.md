## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:3aacd66a9c7b1789495997f92ec9d8da8334e6e8bca25732e86fbc07c67d930e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:191aaa65c6f079e29c1b009402cd53ec4151134bf1be5b8d00be9ea8af8f0e00
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.9 MB (954893842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb3d9147c655081d54ba105d7321de64c7ff681bbfee1d0a49dbf86347bb2f9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 06:12:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 06:12:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 06:12:38 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 06:13:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:13:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 06:13:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 06:13:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 06:14:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:14:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 06:14:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 06:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:21:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834851e18e2213f7ab1b3eac471f9a2bf1ac851276e6545c235b867752295a65`  
		Last Modified: Tue, 02 Jul 2024 06:27:09 GMT  
		Size: 1.2 MB (1214779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812ffac3f486cd0025be751ffe1ff4a529eca49221b59aadc9a9326d31152963`  
		Last Modified: Tue, 02 Jul 2024 06:27:08 GMT  
		Size: 3.8 MB (3829612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3c8e489256d2e519404d75afc9d6ba3cd49ea01162174909b9849e44f1724`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef01b32b1eec952e6afc5e7acbbe08bac17caa0ecab0353a36437c0ce10c58`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a6ad111ea9e627c5ddd919cccc3f44a8ffe7ba3b24068fae2b35143321f834`  
		Last Modified: Tue, 02 Jul 2024 06:27:23 GMT  
		Size: 106.5 MB (106534706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1089c45a27fa6775af871e4c2a4fe847d10f55db1aeddfc745406207518119`  
		Last Modified: Tue, 02 Jul 2024 06:27:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc28a3d8ba8d4113899198db9fd697dcd7c545f49b1063b676a5198b5fcf9f3`  
		Last Modified: Tue, 02 Jul 2024 06:27:43 GMT  
		Size: 98.1 MB (98145979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe07c304cdbbeac013841c1866ea8f65b3cc60b250758c177aa7225cda40021a`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 329.5 KB (329506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e75bb1bfb3eb97b0e2abdaa51660f203f2fc4bd967f467f977b4bf5ad86e5e6`  
		Last Modified: Tue, 02 Jul 2024 06:27:31 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2055f9c9cc67e0e78e21d16d3cf2c9ba4a63fbc9dcf4427fc942f8f189df4`  
		Last Modified: Tue, 02 Jul 2024 06:27:34 GMT  
		Size: 22.8 MB (22824049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e2d84f2e1bd771c94e90f8efccd97606d4d11741b815cc758a8b2b88452575`  
		Last Modified: Tue, 02 Jul 2024 06:29:20 GMT  
		Size: 691.6 MB (691570413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ee40053af58c37010977f74761ffda66d2cf680293a48656aff8e49c2fe66bf2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.4 MB (915449931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4effc3cabe26473746f30726a09937b3506fd116ee347f4494221776a65377`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:38:42 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 02 Jul 2024 04:38:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jul 2024 04:38:43 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Jul 2024 04:40:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Jul 2024 04:40:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jul 2024 04:40:10 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:40:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:40:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Jul 2024 04:40:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Jul 2024 04:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:50:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7b10f47a370e5fedf6c9a77acbc3dc2ae925b72b160c153a2ae6a1a0154744`  
		Last Modified: Tue, 02 Jul 2024 04:55:03 GMT  
		Size: 1.2 MB (1215126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b864962a37b4d333a12d023d9ad1aff4dd315de89d37cd91a319e46eddbdd19`  
		Last Modified: Tue, 02 Jul 2024 04:55:01 GMT  
		Size: 3.8 MB (3801499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3d99d993ce83190c87890f568916bac423c7d37ea17e40fe0e6fb59bd14d2a`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4e4922ae0a702fad33cb6bc1b8062016c4dd4106ad86f9cb22046aef012a59`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31d95c6effa23866939e90b650996f401ea05eaf75999b406ee415479b71bb`  
		Last Modified: Tue, 02 Jul 2024 04:55:21 GMT  
		Size: 104.3 MB (104259492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3cfca808ce5a3e85fef69e383034dbf3d4c4420da1763be2c07f0fb1cc5cd8`  
		Last Modified: Tue, 02 Jul 2024 04:55:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9a0fb56b7f1e4b815ae336e390970c0f24f893dd71218daf35b302a34dd4a9`  
		Last Modified: Tue, 02 Jul 2024 04:55:41 GMT  
		Size: 95.7 MB (95715416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bed3eca41259a671dec69d55ff9184d01d25d1655ec828ec45204579b6df29`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 329.5 KB (329499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3ca19b14268fc7aed9d9edab3b959ea7a2551523997a1250b2b297528dd662`  
		Last Modified: Tue, 02 Jul 2024 04:55:29 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ca8ad62e3384aca8bf996f68146f47006029f9094904a72f297d5021c9a7b`  
		Last Modified: Tue, 02 Jul 2024 04:55:32 GMT  
		Size: 22.2 MB (22236600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55de3ffa3a7b727436f175ee25b99e280bffa6b8e2e07484f4f0f83837f60b57`  
		Last Modified: Tue, 02 Jul 2024 04:56:53 GMT  
		Size: 659.5 MB (659486243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
