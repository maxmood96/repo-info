## `ros:rolling-perception`

```console
$ docker pull ros@sha256:6b87d905fe62638a4377f75c1aae143931cc5d73572fff684c148153a0304065
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:4a08b6d0f8273db4db83b4b58d10f55849b1c295e7f21c70d38fd574d9383107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1096432674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa27eb5477d823ecf51734c534a2cb51dc36f6d5173fc4745990a3a3251f6387`
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
# Tue, 17 Mar 2026 04:17:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:512849ab37cc4e781e883bfe671fb4e8a695c0575669ee4fd17a6a42759be846`  
		Last Modified: Tue, 17 Mar 2026 04:20:17 GMT  
		Size: 784.2 MB (784237075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e58807700fe229cda27a429072c95eca08d81e70eae0aeabbcae5a937a258670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61806644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc1467c44dab6a14857bc1750d2f19eaaec8cdb0f4ffc2465f133757ea6b93d`

```dockerfile
```

-	Layers:
	-	`sha256:62a1748d17b4e51b1fd651630cd1e4b15cf7f21b32eb7021c0092be280e3f42a`  
		Last Modified: Tue, 17 Mar 2026 04:20:04 GMT  
		Size: 61.8 MB (61797283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983433934561b55e55d96826c1f2036a64ada95b48de3d99b0c2de8f557a8ec5`  
		Last Modified: Tue, 17 Mar 2026 04:20:02 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6a3ae17571947089ed0c91352a5d24ef6688bfbf5b98477af5967e9083290059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **998.7 MB (998661487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd1ab0ebcdcfb635908d1448b5c74bfaf4a7b749d379046035bd81fba0b2700`
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
# Tue, 17 Mar 2026 04:15:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:54577cdd61e488522aa56a91cd89c5414ed668415eb5a87cb790032c1b985092`  
		Last Modified: Tue, 17 Mar 2026 04:18:39 GMT  
		Size: 698.4 MB (698379966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:105f5ec9c11fe1ccb4d0515b4ce1f513f0d3e8a6786e67aa05d62e283b3896c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61737442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30a0293e7c3e0bfb93bbcfa9477e4c054577ffab62fab5886a7263fa451f3e7`

```dockerfile
```

-	Layers:
	-	`sha256:bce44bac1e2689ea7d5f0dc2487885a78191bf7eea747e4875ce18b4420b520a`  
		Last Modified: Tue, 17 Mar 2026 04:18:28 GMT  
		Size: 61.7 MB (61728001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc0a3992aeff2e72d6993fc969785700a8e50959129c3c96a4e86da8955acdf`  
		Last Modified: Tue, 17 Mar 2026 04:18:25 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
