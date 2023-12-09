## `ros:crystal`

```console
$ docker pull ros@sha256:cfb8a246d80eeb635e1f09157422f83d2152b1f61d92a35178fc878d4dac0433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:crystal` - linux; amd64

```console
$ docker pull ros@sha256:ba8f6d25693921717e86439cfe9343e683a5f00615de1bf9bb45f48130e24b5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270578690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a84e7e5d33ac42efcadd736a866731efbf8a55f30a7ef7b795a2d4054b9476`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 03:40:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:42:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:44:49 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:44:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:45:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:45:15 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:45:15 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:45:36 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 03:45:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:45:41 GMT
RUN pip3 install -U     argcomplete
# Sat, 09 Dec 2023 03:45:41 GMT
ENV ROS_DISTRO=crystal
# Sat, 09 Dec 2023 03:46:13 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:46:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:46:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:46:15 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:46:37 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a87e4a919bbb35ba9d44fc4cfc4ad95f0e50f0b9f7781c55d60a93226fbadaa`  
		Last Modified: Sat, 09 Dec 2023 04:45:49 GMT  
		Size: 818.9 KB (818901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75db07ca811323aee4149a004b7840679984582866b7ae0c8d6c342da3faecac`  
		Last Modified: Sat, 09 Dec 2023 04:46:08 GMT  
		Size: 159.1 MB (159073267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4c63d3fed9e72f3389c3de3b866a40b32fa0737bce4cb547229e26765b7a81`  
		Last Modified: Sat, 09 Dec 2023 04:46:31 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70c914b7322c913ebcaa18aa0383cde1bd4b1811feb3702947c7305b77426cb`  
		Last Modified: Sat, 09 Dec 2023 04:46:31 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cd5f540c98922e16797a51f4239113025b4ff16a3eae35cebe83c797ceaf42`  
		Last Modified: Sat, 09 Dec 2023 04:46:37 GMT  
		Size: 28.6 MB (28642967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93beedd85dbea0184c5302a1f9437968045a636e7617ad881ab255551cd6b8fa`  
		Last Modified: Sat, 09 Dec 2023 04:46:29 GMT  
		Size: 1.6 MB (1552712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b945318f10c75b1e72f6ad6c50b445bf6ee3a3e15ec85d2cec1849632436bbac`  
		Last Modified: Sat, 09 Dec 2023 04:46:29 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827bb356f902bb66817e80933dca89f034e1ae4757d307c5e7b073159b35dbad`  
		Last Modified: Sat, 09 Dec 2023 04:46:29 GMT  
		Size: 321.6 KB (321565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d23eaa878e51a8cacbfab705d420f9de313c51a629e7a90f721840f8060629`  
		Last Modified: Sat, 09 Dec 2023 04:46:43 GMT  
		Size: 50.3 MB (50263371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374ab8d1d81d7187c9ebe1d13008cf1987f76c78e593729c0ae00025d0fcedc3`  
		Last Modified: Sat, 09 Dec 2023 04:46:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6c61531f8a389a2230f512e7f966cbbedf86afa6b1cf4d1e465cf5a6ff012e`  
		Last Modified: Sat, 09 Dec 2023 04:46:52 GMT  
		Size: 3.2 MB (3183229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:crystal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:398061a6dbc0f2139b768bd821c3d581e6dcca3b043d16c32438d9c9d14438c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247115596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deccc795a3c68dab8fb9496e0f11446260f64ad0f116be009104ba93b3255a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 03:05:03 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:07:06 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:09:47 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:09:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:10:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:10:08 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:10:08 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:10:33 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 03:10:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:10:43 GMT
RUN pip3 install -U     argcomplete
# Sat, 09 Dec 2023 03:10:43 GMT
ENV ROS_DISTRO=crystal
# Sat, 09 Dec 2023 03:11:16 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:11:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:11:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:11:17 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:11:31 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0cc86ec3df331c06cddc9c328d020ffb34c14bab428cb58722dc03f6982888`  
		Last Modified: Sat, 09 Dec 2023 04:01:36 GMT  
		Size: 819.0 KB (818954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eb46c25f1edfc37ec8bac2e81e8f79c91edbb61d3c83828b49c8429b82eccd`  
		Last Modified: Sat, 09 Dec 2023 04:01:51 GMT  
		Size: 150.7 MB (150702502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174fd6cf04a3761997b180c19a52bfbfce1121d88de14bcb0aa81addbda36a48`  
		Last Modified: Sat, 09 Dec 2023 04:02:14 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ad7d3554926828fffa3f83836a967264e04b7c73832e8730292544da6b1801`  
		Last Modified: Sat, 09 Dec 2023 04:02:14 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e84493e3164ce25d73748b1f1a2bac49813e97fe32e84f805f32e756fd974e`  
		Last Modified: Sat, 09 Dec 2023 04:02:19 GMT  
		Size: 27.3 MB (27303072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f54549319d040aaa780ca63006bb5529d640f7358fbc73f518b6a889200c06e`  
		Last Modified: Sat, 09 Dec 2023 04:02:12 GMT  
		Size: 1.6 MB (1552709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d6fe886d03ef5781ada69445f63d3483482db9cc77cec17f2c084b0469d503`  
		Last Modified: Sat, 09 Dec 2023 04:02:12 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5febae93f70de05337d0c5d4edc4dc8eab5e88d4c7c0c22a4ad41e698171b376`  
		Last Modified: Sat, 09 Dec 2023 04:02:12 GMT  
		Size: 321.5 KB (321549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160145cabcbe2f1cf47c6aaca64ca78eff1708d24cf3d0bd189f53da8857d4ec`  
		Last Modified: Sat, 09 Dec 2023 04:02:24 GMT  
		Size: 39.7 MB (39727545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311df1112317d862a1e8ece09f10598fae4188b09e0eca01f0b6d6966958b4a3`  
		Last Modified: Sat, 09 Dec 2023 04:02:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abf8bc13881dbd9151b784dd6a9c6d96a90fbe1ebcb38848db428b3dc4ce0f8`  
		Last Modified: Sat, 09 Dec 2023 04:02:33 GMT  
		Size: 2.9 MB (2943045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
