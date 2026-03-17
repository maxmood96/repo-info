## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:f790a9b8147bb016aa1e6e4cb4e2113b24941414f99346ed2c66227e13548c1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:ae89c6f49ef4d1d87268fc1e6336dca87f6306492cf144a906fadb156146df7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312195599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b93c37d9b7bce6fd8bf17cd9bd94df675cf02a711b5c5f07d1ef2b23294e36e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:21:02 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:21:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Mar 2026 02:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:21:02 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:21:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:21:02 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:22:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:22:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:22:42 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:23:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15463b82d632a1bc8cf0fa79f69d770edd9fcf2c7dc6fd90ff2bd17e055841a`  
		Last Modified: Tue, 17 Mar 2026 02:21:31 GMT  
		Size: 683.9 KB (683904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f8b81a23f03cb1f80996b1b31fd2dba3346f972b473e53a0e3698bbc5b0d03`  
		Last Modified: Tue, 17 Mar 2026 02:21:31 GMT  
		Size: 6.8 MB (6751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe925611e40b8d95c593caef9f6ece9b81c61828373e4ac5694187a041abdb94`  
		Last Modified: Tue, 17 Mar 2026 02:21:30 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09240c2cd96a025739e67f40f2364f9385438562acbbdac5739bde6fe42e309a`  
		Last Modified: Tue, 17 Mar 2026 02:21:34 GMT  
		Size: 136.5 MB (136530193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f17b80019f4c578c4719a33fed7d89543c542dc0af18e9dbd35bd0f12926540`  
		Last Modified: Tue, 17 Mar 2026 02:21:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eeb04a53f4529b057fc6d3942d716b817129085c16cc5a6e942305c7c2482b`  
		Last Modified: Tue, 17 Mar 2026 03:23:39 GMT  
		Size: 110.2 MB (110190736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e500b20efdf6169284b695142a33f05378c6d39b9c60dadbe578d5a3b3f425`  
		Last Modified: Tue, 17 Mar 2026 03:23:34 GMT  
		Size: 369.7 KB (369697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5de0c53b7b9b2ce70983fe631cf677fcb1f9011efbefe4e70ef8a357dd1e8e8`  
		Last Modified: Tue, 17 Mar 2026 03:23:34 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f828c4342aa4485401ff029b3e3f9cfaced5d3b65d7aa6a59160b976575dd0`  
		Last Modified: Tue, 17 Mar 2026 03:23:36 GMT  
		Size: 27.8 MB (27840528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:1e01c29192310e8fbc41527ef16ea568faa5bcd876b561e2ef4936fbbee2a0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25639099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d585a280a8ad168cbd92bbc914498c8cea9ed2df69856995445a008c39da619`

```dockerfile
```

-	Layers:
	-	`sha256:497d5a57bbf633f3f75eb0715af50f9a51cdaff8e0faab70103d6e3b813e2991`  
		Last Modified: Tue, 17 Mar 2026 03:23:36 GMT  
		Size: 25.6 MB (25622736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825bda0d55a3daf8aaebdd66ea64d81f1cddaf4b0123814455c98fdb4be7f27f`  
		Last Modified: Tue, 17 Mar 2026 03:23:34 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:53ede76106c773efafb139f1e029e17fa81727fe35f073e3c05afe2526a40fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300281521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865a37fca5c523b2189089044adc89928cb7180d81fc4f221782da7b20d078dc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:48 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:26:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:26:48 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Mar 2026 02:26:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:48 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:26:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:26:48 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ce31aeaa29ac4e6452e3da1b22f70b50bef7b8fb4360d957c378666e3a1ea`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 684.0 KB (684045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240ec1232177be2455f9a0dc247b5543e0b1a1197eeb970ad1ad08a3ceca3419`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 6.8 MB (6764923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517ea7c6da9dda5a9d9bd7a79a74e38c3a3db8ed248109a7be2337d8aa0e0300`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 94.2 KB (94239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465c0a6393d917b703e9eaadd7cecb66acc38ea8629230531e47694ef6af4f37`  
		Last Modified: Tue, 17 Mar 2026 02:27:25 GMT  
		Size: 131.0 MB (130963424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed02cf0331f23f1c9a6b54ba39118f8e8d77a71a77e5e9b735f5d44bd01e28b`  
		Last Modified: Tue, 17 Mar 2026 02:27:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a0d7af6e6451dfb3d085ed4ab78846bdf5f619c2f05256888faa6dc061f54c`  
		Last Modified: Tue, 17 Mar 2026 03:25:21 GMT  
		Size: 105.6 MB (105602778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784aadb7347c148d8ba2df723ec2812676f056f276012ae570b1271b4ee7fbe8`  
		Last Modified: Tue, 17 Mar 2026 03:25:18 GMT  
		Size: 369.7 KB (369714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ce190425448cb309f63600b4bae8a5e0b0dcc87c16858009cf4055d7d61ed0`  
		Last Modified: Tue, 17 Mar 2026 03:25:18 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fab84afb5be776288df4f031f072a03f78bec0701683256e7cd04f8deef1a9`  
		Last Modified: Tue, 17 Mar 2026 03:25:19 GMT  
		Size: 26.9 MB (26929991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:bb9fa03b96dc7569ac03c08446680c4bbb6c7fa5e3e398ab9a56fa711f9e1e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25661697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0521c4983ee69beb3055fc35f4c0944856f06c56864561cfa3d8b8e6130b4`

```dockerfile
```

-	Layers:
	-	`sha256:32743d3c73fbbacf4b7297f374a8ca17e66b6c19af517d63aa5518b2586aafc8`  
		Last Modified: Tue, 17 Mar 2026 03:25:19 GMT  
		Size: 25.6 MB (25645195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebb42fb05224f2ca79cae24013c4cee8d831b3278f0f5eca0aebf0513d51d0d`  
		Last Modified: Tue, 17 Mar 2026 03:25:18 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
