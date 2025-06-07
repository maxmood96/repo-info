## `ros:eloquent-ros1-bridge-bionic`

```console
$ docker pull ros@sha256:18816203a36dcb226fa6ec871cdd0d160c534584b62d0d04c63ef370b02bd584
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros1-bridge-bionic` - linux; amd64

```console
$ docker pull ros@sha256:407c160f925e9fdec79e6bc3d8bf804c39c873a086b4669d41b66af35c3dbadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 MB (502857716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbd76016ef89199ab1e69d1ca429676a34d88f9a9dbd71ada3dee4d4208ce2d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 14 Dec 2020 01:00:59 GMT
ARG RELEASE
# Mon, 14 Dec 2020 01:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Dec 2020 01:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Dec 2020 01:00:59 GMT
LABEL org.opencontainers.image.version=18.04
# Mon, 14 Dec 2020 01:00:59 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Mon, 14 Dec 2020 01:00:59 GMT
CMD ["/bin/bash"]
# Mon, 14 Dec 2020 01:00:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
ENV LANG=C.UTF-8
# Mon, 14 Dec 2020 01:00:59 GMT
ENV LC_ALL=C.UTF-8
# Mon, 14 Dec 2020 01:00:59 GMT
ENV ROS_DISTRO=eloquent
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 14 Dec 2020 01:00:59 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS1_DISTRO=melodic
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS2_DISTRO=eloquent
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.13-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Fri, 13 Dec 2024 13:10:33 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479d6516b5b71644b6cc96d844b23830cbf0d1ab4f7c4a9180dbb003352974a`  
		Last Modified: Fri, 06 Jun 2025 22:49:22 GMT  
		Size: 818.8 KB (818769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b06a714936526a1264026982671e2fd973aabc5e3a06382de9a5ff2039dbaf0`  
		Last Modified: Fri, 06 Jun 2025 22:49:23 GMT  
		Size: 4.7 MB (4688743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9a5f477bff1dc9a46e96f21b664baa2c61c24f38a784517fa45c4440fa48d9`  
		Last Modified: Fri, 06 Jun 2025 22:49:23 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2ad959edfc7117efd0d3c75f21de5fc71c696f3c566f6d4f963abc4178886d`  
		Last Modified: Fri, 06 Jun 2025 22:49:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88090f0cf723f1c40ededf8978a6634972fec544dbcef35613d7a6f975f5fd`  
		Last Modified: Fri, 06 Jun 2025 23:07:34 GMT  
		Size: 183.2 MB (183210181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef0a1c07f2aa35a613d990a378483fc39698ed4ec70214f61088c71c59b47d8`  
		Last Modified: Fri, 06 Jun 2025 22:49:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd763c4f102fe26075ed12bdf3a53ae0335b10b75246e333d1729551946783b`  
		Last Modified: Sat, 07 Jun 2025 00:07:52 GMT  
		Size: 63.5 MB (63538581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fff6ed272ffd78a1c88497de95987c8fce161eadab2a2aa622ff9f73754035c`  
		Last Modified: Sat, 07 Jun 2025 00:07:49 GMT  
		Size: 270.6 KB (270593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa858cf34fe14ce5c1c0fa29d97687cca30e5a655f7e9695cf7d56123c83fc9`  
		Last Modified: Sat, 07 Jun 2025 00:07:49 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a644f5d92179411288e51b40f3dc04ae03506a62ed4fc7520de3825e253791a`  
		Last Modified: Sat, 07 Jun 2025 00:07:49 GMT  
		Size: 4.4 MB (4371111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a13105f155096b8d57efe008da65a5d3c991dec9758c25b34be027218afc90`  
		Last Modified: Sat, 07 Jun 2025 00:10:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09cb5bb42aee6add2d12aebd11c62265e7cbe5dc1985fd49bb3b1d4f8c2ee9c`  
		Last Modified: Sat, 07 Jun 2025 00:10:51 GMT  
		Size: 117.8 MB (117762065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf9f92997f565951c39edc79efa872bab835cc0adb2602aa998f203bd0ff6b2`  
		Last Modified: Sat, 07 Jun 2025 00:10:51 GMT  
		Size: 102.0 MB (101981476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf83d24832adde23887df03cd99655660cd8db39c6be92a55ebd9fd54e7dbf09`  
		Last Modified: Sat, 07 Jun 2025 00:10:48 GMT  
		Size: 519.1 KB (519146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cae05b262fbdfff0f3bca4f70fc1cee352203cfd2ddb0ab1896aca5e42953b7`  
		Last Modified: Sat, 07 Jun 2025 00:10:51 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros1-bridge-bionic` - unknown; unknown

```console
$ docker pull ros@sha256:03cc1899e2c71a5525c2b46f444f383f4ce046bd3524ee287c9a422160207e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45867445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c941de56a07d01aea1ef2af30a79551b0556dcdd75afa329a6e52fa8e3d781ae`

```dockerfile
```

-	Layers:
	-	`sha256:bfcdca458012ea8b896186edd2310f37b39cbc16f04352d0b0d08527ca7fcbd7`  
		Last Modified: Sat, 07 Jun 2025 01:19:19 GMT  
		Size: 45.8 MB (45840515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65db3e11eb191150fe39d2a53114f1009a2d79de19c5bc9f5d9292c3b5341ff8`  
		Last Modified: Sat, 07 Jun 2025 01:19:20 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:eloquent-ros1-bridge-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:0040f128fdbdee7f904ec9db6f5ae93a4ca9ec1e756c5dabb33c7766fa4e6a2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.8 MB (429848896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aaeb9fbaeb366dba0f5c1b67cc2cab61d2f190f0546146f72707e55863089f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:56:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:57:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:57:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:25:43 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:25:43 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:25:43 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:25:43 GMT
ENV ROS_DISTRO=eloquent
# Sat, 09 Dec 2023 03:28:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:28:03 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:28:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:28:03 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:28:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:28:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:28:55 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:29:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:38:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 04:38:19 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 04:38:19 GMT
ENV ROS1_DISTRO=melodic
# Sat, 09 Dec 2023 04:38:20 GMT
ENV ROS2_DISTRO=eloquent
# Sat, 09 Dec 2023 04:40:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.13-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:42:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:42:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:42:31 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:76bc0c6b06fc92c1f911be6147b55b6430301b80e4062178329c4fa8a0f79f51`  
		Last Modified: Sun, 05 Jan 2025 20:38:31 GMT  
		Size: 22.3 MB (22312178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e61f2f0ecdbc00c1478913acffbebaebcb6c199462717018cc5c71eed71d93`  
		Last Modified: Wed, 15 Jan 2025 00:47:30 GMT  
		Size: 820.3 KB (820323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13552f8532802decc8d718ee39a8826c22eb2f08a55ec54be8349c2ec390066d`  
		Last Modified: Tue, 24 Dec 2024 13:34:26 GMT  
		Size: 4.1 MB (4090743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73031d8d6723d2c344f35a55a3313e78b28caf1442735033da25f0e991699c8b`  
		Last Modified: Tue, 24 Dec 2024 13:34:27 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c793c7f3a118ae9e4d4f53d0d093faf1a193e9dfcac1baa25b75fff7bb3b7c`  
		Last Modified: Thu, 05 Jun 2025 08:27:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f28e9b8e963c120ae7664d793862196ab199b8a4c3fe049ea8303de3171c1fe`  
		Last Modified: Sat, 09 Dec 2023 03:44:46 GMT  
		Size: 156.8 MB (156783586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814cc6e54cdd4a8a81f9cd0db77aa1dba3eb85dab1f2358922cf657297c3c6f5`  
		Last Modified: Thu, 05 Jun 2025 08:27:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8d1710ff3194f3ea295be983db6380e4af615d684dd80b48a6de0494c4499e`  
		Last Modified: Thu, 05 Jun 2025 08:27:46 GMT  
		Size: 48.2 MB (48247944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075812fe1368dc08489c5d65ddccaedc9714e7b28dc30fbb0e8ce195b772af23`  
		Last Modified: Thu, 05 Jun 2025 08:27:28 GMT  
		Size: 240.4 KB (240450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1099efa64d064578f3ef5a707705084237109fe9596f2f87904905fee91497`  
		Last Modified: Thu, 05 Jun 2025 08:27:30 GMT  
		Size: 2.4 KB (2427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3717687124f3d9c5791e09e569d8def54c9bd0159f6e5776ce2413fe6f0fe8e`  
		Last Modified: Thu, 05 Jun 2025 08:27:37 GMT  
		Size: 3.5 MB (3496971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19514cec248d3a18298a17fbbfa50e3390ab11bb4efc6d330492f50ac80c417`  
		Last Modified: Sun, 18 May 2025 14:37:31 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcbf5e91d07cfd48228354cbeccbdadda38e084a9106349ca3e20457e8e57e4`  
		Last Modified: Thu, 05 Jun 2025 08:28:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c5badcb7c4fe5f4266a244b74bd200244782a2b20e5dc162a79b76371088fa`  
		Last Modified: Sat, 09 Dec 2023 04:43:54 GMT  
		Size: 110.9 MB (110896855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c5ee7142993efd7f84ba2c2d5df0a13c981d760e79ba5088ec9fe858b3e6c1`  
		Last Modified: Sat, 09 Dec 2023 04:43:49 GMT  
		Size: 82.2 MB (82219152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a070e67476f9b30e2d9e68b33043f47a1b9923cdab4bb552f6919d481f9cf0`  
		Last Modified: Thu, 05 Jun 2025 08:28:18 GMT  
		Size: 734.8 KB (734796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920cdf7b3614b41a09d9152b0e69f5bfbf0fd7211546c1ef9c1ad17740f01c98`  
		Last Modified: Thu, 05 Jun 2025 08:28:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eca560d9a7826925abd2ab009368843dbcddfac73ab5ec0ce33ff2d03cec6c58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.8 MB (464793197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a3a880b3686d13076093df5b6e4ff5f085e5e11f3932dea18897b6047d9e62`
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
# Sat, 09 Dec 2023 02:23:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:24:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:24:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:16:14 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:16:14 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:16:14 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:16:14 GMT
ENV ROS_DISTRO=eloquent
# Sat, 09 Dec 2023 03:17:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:17:14 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:17:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:17:15 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:17:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:17:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:17:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:18:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:47:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 04:47:32 GMT
RUN echo "deb http://snapshots.ros.org/melodic/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 04:47:33 GMT
ENV ROS1_DISTRO=melodic
# Sat, 09 Dec 2023 04:47:33 GMT
ENV ROS2_DISTRO=eloquent
# Sat, 09 Dec 2023 04:50:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.13-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:51:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:51:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:51:50 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Fri, 13 Dec 2024 16:03:06 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92311637e9983a187857b246a6417188e5a1de48e9d03e831eb2cb63a811cf67`  
		Last Modified: Sat, 14 Dec 2024 04:09:58 GMT  
		Size: 819.0 KB (818985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b4394df3604b47aaa3d36d1ad63c563ac4d8b172081757c048ee6bf10cdd08`  
		Last Modified: Sat, 14 Dec 2024 19:23:14 GMT  
		Size: 4.5 MB (4461631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1d3a8f1076e5ddb09c78ae7493c813f46853e1e63d7cfe42ba1c50cf6bcf28`  
		Last Modified: Tue, 17 Dec 2024 21:52:48 GMT  
		Size: 2.4 KB (2409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a151493b6c9d8425d7a9e6a9993ba4d731ad95e12a87256be858d78684d1286`  
		Last Modified: Fri, 14 Feb 2025 20:58:35 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275752ffee34d72b25cef8a220d83716491d1d0bd45b8c1aa4fae36ba907a345`  
		Last Modified: Fri, 14 Feb 2025 21:09:07 GMT  
		Size: 168.6 MB (168606855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9479152d19f2aa17356df5322c932e234af902cfd11b793012f23329c8c79c`  
		Last Modified: Tue, 14 Jan 2025 23:28:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060b6e6ec91a69696d3a30e570566858a8c81d35a90b1563198d9c5a12acdc45`  
		Last Modified: Fri, 14 Feb 2025 20:58:45 GMT  
		Size: 56.4 MB (56446168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafb3122a7276f53e87b38348885606ff107df1dbf3eaaf3747680d75b627982`  
		Last Modified: Fri, 14 Feb 2025 20:58:47 GMT  
		Size: 240.5 KB (240451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3254779e9290c20ec877ee69e363c350743f4de49b96453d2c882bd5a1d5eb`  
		Last Modified: Tue, 14 Jan 2025 23:28:09 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6ee3ef7fa3685810aa57edf4c9c1e9b933ad324de2e6d4870d903a842e4807`  
		Last Modified: Fri, 20 Dec 2024 15:53:00 GMT  
		Size: 3.9 MB (3933942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40874f31e6c9a8eb1ab503dbc5719f1d4ce909e9635c069085a360b470caf873`  
		Last Modified: Tue, 14 Jan 2025 23:28:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab206a732c2d4713d53818052135eb49b2228e547c0467970643505fc8253d19`  
		Last Modified: Sat, 09 Dec 2023 04:53:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929ed5bc47f6f4712f5cef0afd9eeff293dca9719a2cedf4e8c075c654f773df`  
		Last Modified: Tue, 14 Jan 2025 23:28:15 GMT  
		Size: 116.9 MB (116916260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da37e77d136d0cc98a6c59de32cfaacc2cc96e217a5a8705e76ff6b1a8aa4eaf`  
		Last Modified: Sat, 21 Dec 2024 13:24:37 GMT  
		Size: 88.9 MB (88886837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4b056a8f2f7c32fb4794e6c3d9390f8aa7a9468cc9b022079e34275d43d4e4`  
		Last Modified: Sat, 21 Dec 2024 13:24:47 GMT  
		Size: 735.2 KB (735243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeb5b6b3d341bfee6af13bf1bcf30331f916d3ecf8d13ef12260e60dbc4e3ea`  
		Last Modified: Sat, 09 Dec 2023 04:53:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
