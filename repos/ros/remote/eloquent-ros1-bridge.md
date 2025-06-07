## `ros:eloquent-ros1-bridge`

```console
$ docker pull ros@sha256:fce5131d66ef3ca6aa66a23b693c786c1b24a85e83fecec4152a216a21f1644c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:eloquent-ros1-bridge` - linux; amd64

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

### `ros:eloquent-ros1-bridge` - unknown; unknown

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

### `ros:eloquent-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:79a1194b42df1e7f57c72788f773c678dbbad3ba43a772398dff3df9f22077ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.9 MB (427898637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b111cd623b06553a01217a406e9d4eae3dcbaaa33fbb081677b743d8f75ec1dc`
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
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
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
	-	`sha256:33728956a279755bb5e348de30626ffff0023b589d4fae264c2722ad7c06e207`  
		Last Modified: Fri, 13 Dec 2024 23:12:36 GMT  
		Size: 21.4 MB (21399001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49dc90beb658024e96db38e10eb9d3d5e95151611e5a8b1e4aac7ea6e45313`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 820.1 KB (820137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd276fdf8bc17a3ae89b76a87869626c84e29eb535dbb5b183ac80bae85c02c`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 3.9 MB (3900545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b029d64f9143b80260f4b5b994450da65eef021667391fbce44a5f2aa0f4398`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30d7b9793ce6e39fe204512d45290f47261186305bb67b812db91174e635176`  
		Last Modified: Fri, 06 Jun 2025 23:25:13 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733d36e0267ac31385145d2451947c564af6e00b7c40a2b0609fe6a7b1221f3d`  
		Last Modified: Fri, 06 Jun 2025 23:12:04 GMT  
		Size: 156.8 MB (156771762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60f6ce791c835a931f96cd4ecb40b4c458df0e59a8f7474a54fb368ed4a9453`  
		Last Modified: Fri, 06 Jun 2025 23:25:16 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8d49e612f90dbec0d4f6098780f2774bb5dbe5c337a08c12dfc9c9c91772f`  
		Last Modified: Sat, 07 Jun 2025 00:42:15 GMT  
		Size: 48.0 MB (48033459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a708b6f1ffe3041048665490416c1fc43edde90b804472bd3cbf061690275a`  
		Last Modified: Sat, 07 Jun 2025 00:50:07 GMT  
		Size: 270.6 KB (270583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88fd6411454093f479c8f57eb421bcad3db00e85ea1c237cd4b373dc61bb1ec`  
		Last Modified: Sat, 07 Jun 2025 00:50:09 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed43a02e09f372e640782153786f049698f1e2ca6d284a807f278882be9591cc`  
		Last Modified: Sat, 07 Jun 2025 00:50:13 GMT  
		Size: 3.3 MB (3282567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04da869cf7bd0f10518153d75029102af54a914f5f6764cee3865b93c3dde96`  
		Last Modified: Sat, 07 Jun 2025 02:07:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33cce1e21fbb6c236b39f42de9efafc20f6d5ed8db189fafac037b3e9fc5b4f`  
		Last Modified: Sat, 07 Jun 2025 02:07:30 GMT  
		Size: 110.7 MB (110682142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03f4fca64311d044bf96b8f13630f9631a0175e18f10d9b029dffacf6d9f8a3`  
		Last Modified: Sat, 07 Jun 2025 02:07:29 GMT  
		Size: 82.2 MB (82217683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31241b52ad9ae6f545a0885233c20c2145deb7c13ff32984e2373521f95072b7`  
		Last Modified: Sat, 07 Jun 2025 02:07:26 GMT  
		Size: 515.0 KB (515008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3cb65336936df92949c630906851def792e20cc5f807d106cb2179ef102b1`  
		Last Modified: Sat, 07 Jun 2025 02:07:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros1-bridge` - unknown; unknown

```console
$ docker pull ros@sha256:24c1a4e9e60e2bb3efef769827178d49e52d402f34ef035b39d720216d592d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44303620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d277786aa94f9490c11804de4add9946aa96ceb2a4a5fc0beba0d2cbcbeb182`

```dockerfile
```

-	Layers:
	-	`sha256:ab96718739b18e1e9eb55c871844cbf464c55983868de1e249ed6ccb5c4997f3`  
		Last Modified: Sat, 07 Jun 2025 04:18:44 GMT  
		Size: 44.3 MB (44276581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2b501b769ad791dd8329d61243890b54622ce7aa7058ee93a898f430c53d1f`  
		Last Modified: Sat, 07 Jun 2025 04:18:46 GMT  
		Size: 27.0 KB (27039 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:eloquent-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6fcb68d23104a472bfbfe3d3405d66ebade27efb24433f35726cad8fbd24b36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.7 MB (462708402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877f587ef3bf4a2c8a870b073dac6bd7b8e559b36844b7e9675d41b9811e7352`
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
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
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
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Fri, 13 Dec 2024 14:46:44 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6559b6c0a95271b577d553166080f5d9965d9e2d2b1732c96a566175205af31f`  
		Last Modified: Fri, 06 Jun 2025 22:59:17 GMT  
		Size: 818.8 KB (818832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99d6787c1aa8369d0f0e3a1051c56c004c0b42816139b09e85d5fed6e44a27`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 4.3 MB (4270397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5c6de79efb0ec1e3e319f9a58fd5e398fcb65ffb3eff75ff9ff1cff87f158`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f53cf949d0a3b8bf9cdb088732c432b8d3952789160aacd1caddd73b9c02c`  
		Last Modified: Fri, 06 Jun 2025 23:22:54 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a1bc71fd481d7d8718010e4e6b76a3efdbf1727fff82166ddec47c8dc073c`  
		Last Modified: Fri, 06 Jun 2025 23:08:55 GMT  
		Size: 168.6 MB (168591100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092ab5015c6f828f787cad76d98dd4c33d3eb5fe8ad9d21e52f9d05925893a56`  
		Last Modified: Fri, 06 Jun 2025 23:22:59 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f983474caee00ea13129800634333ba0c7f0086baafc12988656531e1fca45`  
		Last Modified: Sat, 07 Jun 2025 00:41:45 GMT  
		Size: 56.2 MB (56229815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4e6d8c04cfc3c6b1ff35f4e5584b2cb24c50af48e5264ab0783a942ad48275`  
		Last Modified: Sat, 07 Jun 2025 00:56:51 GMT  
		Size: 270.6 KB (270588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887a1ed262af20f43df18c98781b3a61f2854cd42b378eee06d320f34b919727`  
		Last Modified: Sat, 07 Jun 2025 00:56:54 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e3b715715fcc3753494a91bf3d0bfbe61ba651b34c917fce18a016ff1e47c`  
		Last Modified: Sat, 07 Jun 2025 00:56:57 GMT  
		Size: 3.7 MB (3717264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25429ff2d4a6638fad0e9a9194c90aa777e26e9575a72f3c1474250906aec93`  
		Last Modified: Sat, 07 Jun 2025 02:08:19 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cea359f9389baa6151a80dd6f931f448c41f3dc57a5bc32a1cb4022b730094`  
		Last Modified: Sat, 07 Jun 2025 01:54:16 GMT  
		Size: 116.7 MB (116696843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525a26f70ff791d5c91a1e1b12a9e42b2477291bb2929aad0f5daa38a59b124f`  
		Last Modified: Sat, 07 Jun 2025 01:54:16 GMT  
		Size: 88.9 MB (88878823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a95e2dfdab304caec9a18d434ffc97ce74ccd595646e7405c00bcc66bfb20d`  
		Last Modified: Sat, 07 Jun 2025 02:08:22 GMT  
		Size: 515.4 KB (515446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b94b3278152a7555adfd1533a7c1518fc1e25ac8f29121a967dcc43051a249`  
		Last Modified: Sat, 07 Jun 2025 02:08:30 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros1-bridge` - unknown; unknown

```console
$ docker pull ros@sha256:29fc6af74a8a3d0fed3e42d873baff8832714b548de1b75b3284e9f9dff8a464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44494332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bac1f1ebcf5349b65fccb12605269a529d09c59bdb8b5b426b1adc6a414e73`

```dockerfile
```

-	Layers:
	-	`sha256:be94908fe849d270373934ee671e659de31418a8a241a141433eda3583957607`  
		Last Modified: Sat, 07 Jun 2025 04:19:44 GMT  
		Size: 44.5 MB (44467265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeebf923a4e3c55a88fa3a4cc723ea0c9d45f4e912b1629239618732e6785dcf`  
		Last Modified: Sat, 07 Jun 2025 04:19:46 GMT  
		Size: 27.1 KB (27067 bytes)  
		MIME: application/vnd.in-toto+json
