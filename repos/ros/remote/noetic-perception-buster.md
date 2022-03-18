## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:b7c3fa77d19c6feea864bb68205e0ba32489e44e828293683f02c96c1dc35e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:540b61c3d6c1a503aa1932987820a050e217eb5790d0ed9b8c76830e8b243133
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.3 MB (951259140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb695e29ce5ed8caaebe3e6225350cbae49f321f1293c695edfc9d62f4d98bb8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:37:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:37:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Mar 2022 10:37:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Mar 2022 10:38:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:38:59 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Mar 2022 10:38:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Mar 2022 10:38:59 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:39:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:39:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Mar 2022 10:39:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:42:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c133b370766b6f5552e000ccf033e32442276773c2cd08a21a0ac9f18259d3`  
		Last Modified: Wed, 02 Mar 2022 10:43:37 GMT  
		Size: 10.9 MB (10892098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ae26f65841562882d5b66361657c9e58e057d74f3ecdca875adcf248f594eb`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c03d38883523f98928ace45a667c9a6f9c1e357c09c22bc32e9f75e3ee391`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3c4ec48c4a1bce55afcd9bbda77e99d790164b04caa20748eb0bd7b2dd5ae`  
		Last Modified: Wed, 02 Mar 2022 10:44:10 GMT  
		Size: 239.1 MB (239095099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970c2b44800a0ec91c9c10e46c3e219d142dbbce8abf085f6c89e01de485a28a`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f52ffdc8600971c23fcc3470929f8e69fcf2f8140208f05977079961d4c9237`  
		Last Modified: Wed, 02 Mar 2022 10:44:29 GMT  
		Size: 86.6 MB (86566685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44425534870ef9a16bf44a1fe3fa688b25244bebc0c9fe2c9db6e3107d70aa`  
		Last Modified: Wed, 02 Mar 2022 10:44:17 GMT  
		Size: 303.9 KB (303871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c3bc0c0b6b4ceaa48e62a3d09745513fcedb49c063d68038f3b84cd2ef6909`  
		Last Modified: Wed, 02 Mar 2022 10:44:27 GMT  
		Size: 76.0 MB (75976673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936eb4d6ce9175f6ea5ceac81d0faf33295da1adfb9748fdd642e0628eeba00`  
		Last Modified: Wed, 02 Mar 2022 10:45:57 GMT  
		Size: 488.0 MB (487985253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1d6888e4199da19491c3d5c20ef785a22858b6516af1d9f5eaf2c538a9487071
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 MB (867455252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d95740cc37f873a3b971491d4e0fe8ba6078164c6584f922a76f50db5a8124`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:57:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:57:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Mar 2022 00:58:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Mar 2022 00:58:40 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 00:58:41 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Mar 2022 00:58:42 GMT
ENV ROS_DISTRO=noetic
# Fri, 18 Mar 2022 01:00:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:00:08 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Mar 2022 01:00:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Mar 2022 01:00:10 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 01:00:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:00:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 18 Mar 2022 01:01:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:06:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cb989cba7dc1d50cf620a207810dfda41194cf7c3488cada787f5828ee2090`  
		Last Modified: Fri, 18 Mar 2022 01:24:22 GMT  
		Size: 10.7 MB (10688147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dc0d7ec12bfae1925877797eaff4b9a4ba48083fd8920a4ccff5b5dd0bb07e`  
		Last Modified: Fri, 18 Mar 2022 01:24:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eae995b77a571bfa585e4b04eb18f60b0cec5688a13afb5be92ba9e38eefe23`  
		Last Modified: Fri, 18 Mar 2022 01:24:21 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fda29b26873c08cbc5f7efdb9b3a02f08b87dcfc7a69a0f8f684a88c92237`  
		Last Modified: Fri, 18 Mar 2022 01:24:53 GMT  
		Size: 184.3 MB (184325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d63919ef43f47b1ff0002843cb0ab133ab048f94d0241d53d989f63971f26a`  
		Last Modified: Fri, 18 Mar 2022 01:24:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5617ca4faf4158afbdca7a157ff503b9946d6c29f88eb4c4f3ffa169c50b23f`  
		Last Modified: Fri, 18 Mar 2022 01:25:13 GMT  
		Size: 84.4 MB (84350617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac233a43af2e3ccd2100b8d8bba599ab0599daf41d3991647e2ba9cb5abfb028`  
		Last Modified: Fri, 18 Mar 2022 01:25:02 GMT  
		Size: 304.3 KB (304262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acef00249fd85131df6b4130a40a2480a309cf90d004df97bfc77393581f601`  
		Last Modified: Fri, 18 Mar 2022 01:25:12 GMT  
		Size: 73.9 MB (73865119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e5ad5fac2a7cc667982fd81481ab2c26dc679844c7cb0de069ffe77a14d54b`  
		Last Modified: Fri, 18 Mar 2022 01:26:40 GMT  
		Size: 464.7 MB (464695805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
