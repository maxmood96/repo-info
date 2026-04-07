<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
-	[`ros:kilted`](#roskilted)
-	[`ros:kilted-perception`](#roskilted-perception)
-	[`ros:kilted-perception-noble`](#roskilted-perception-noble)
-	[`ros:kilted-ros-base`](#roskilted-ros-base)
-	[`ros:kilted-ros-base-noble`](#roskilted-ros-base-noble)
-	[`ros:kilted-ros-core`](#roskilted-ros-core)
-	[`ros:kilted-ros-core-noble`](#roskilted-ros-core-noble)
-	[`ros:latest`](#roslatest)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:1660822550ab8bcbe0145acf4ff0fee33b0fae4f5d4b101d7d11cd5d42876d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:6f2b851ee039c447ad27437efa96459396bc433aabaafdb6fb424513cda93be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263801349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c08ba95445517fba6074f26f19f6d1086c8fe9c760675c8f96139fe41c82cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:15 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:11:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:11:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:11:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed72e15eea09997a888cfd394babf47cd5d3ee9a2c1856f4c7f38000a28cd39`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6bae53520479265b0edca56a5a3c05822e791ced08e5c7231de5c0d547ae28`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 6.0 MB (5994357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bfebc4f1259f371e9045d574e48ccd4cafc66527ceff0773160f92e5eed2b`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890b14f7743317dbac8424f43f421d35c3760e3e790feec63d58f7f8660dace`  
		Last Modified: Wed, 01 Apr 2026 20:16:41 GMT  
		Size: 104.9 MB (104872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6941913bec3545a993c44a7e163faed16e361b4d7a736437dde612fd9509bbd`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c896a95beb5d795345bb3b17a68fb6ddf384eba91010e5ae0fab2b6ffaa4b50`  
		Last Modified: Wed, 01 Apr 2026 21:12:52 GMT  
		Size: 98.2 MB (98158288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9755a7b2bcd6ac84cdbfb843118ad74105566968c5fed29fe9a119f252f7512d`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 390.9 KB (390880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1387f1b937a6d9c6946869d2d0bb31a19208ce67c354b99e273fac62837f5c39`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e682bb1d7aab2c53fa42ed55165efef896598e4c59d1ea32413e718579cdd7`  
		Last Modified: Wed, 01 Apr 2026 21:12:50 GMT  
		Size: 23.3 MB (23334801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:0c2b895c5b596bf231168aa1a98145146cc9cd6d27338138c072ee74be0644fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23851650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39316ec407a80e44290c68c9fd160e7ca4175cc667f13bd2b2bcb628b9fa0eb8`

```dockerfile
```

-	Layers:
	-	`sha256:369d1fc2b74f9116ecbfe60f6dcc623be9a114f4fe7ef20e6b8cee81a86b3b30`  
		Last Modified: Wed, 01 Apr 2026 21:12:50 GMT  
		Size: 23.8 MB (23835302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304ac9b7f10316cc2584dfffb2d209fba00360241c42350b636d2148009af445`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:815bf0ffa4615ce6e1e970af3cd142083cf22ef17745bec2b4c4446b80fcde3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256418157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725c9064b4bf32192dce3a9b8c85feac00588df68f91b0d11026d3d4a0f866a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:09 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:15:52 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:12:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:12:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc0bc42613cab0a58d13ec77015563460d9740f7e9867c8256f65bf194cf98`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 1.2 MB (1214285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66fd6281dcdd3b1a9b6441c2607d70ef8e296483e894ed72f4e8d0cc94c907`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 5.9 MB (5948732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31af296322d1075bf72e1cc3420c7980512f421e9541f4b9fa43f9c2600f7999`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 97.3 KB (97306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d43e320d8992650cb03a0b71eb19d216643b7b26f2161f0a6e3eaf47edf968`  
		Last Modified: Wed, 01 Apr 2026 20:16:22 GMT  
		Size: 102.6 MB (102634213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818371cd205c99f6e214ae759d622585e624ffd84553b1b95e78eeefec55d9d3`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fccb60a4efb53f0b5a957f477b0472d72cf154bacdb5c7400d39996128d22`  
		Last Modified: Wed, 01 Apr 2026 21:13:10 GMT  
		Size: 95.8 MB (95795135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3925511d5109b8abc9487080e46a5482d78169e2622ce61b144bbf4d695a8079`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 390.9 KB (390881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3950ae4bb7a9331ecc9ef96b3c30cbc259e56f2fe92924c9e09e9531e508d330`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e75da22aaf38edd96540827c1ff07111fd2057047f1f4bbb90a5ffc383d83a`  
		Last Modified: Wed, 01 Apr 2026 21:13:09 GMT  
		Size: 22.7 MB (22727961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:b418547700361565d5a6f3ec53a212af039246a963c835416f2b38ad6392203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23864803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ab69dd5891a9fb6e81a9c4fd30d3121a7de1092dd7202e9dfdf6ba612e0dc`

```dockerfile
```

-	Layers:
	-	`sha256:dd5b956eb4161fe3111d0d1c96084bb839a7f164088df3054008c5ec2bd122ff`  
		Last Modified: Wed, 01 Apr 2026 21:13:09 GMT  
		Size: 23.8 MB (23848319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51b7b6018fc927eaa27435452ec893b024616dd5c51ee47a4aa6e2884f1f92d`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:ca58dcbc4db306c2c569509261675600fc21efee113c0960b7579b847006a541
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:db8d50ca3d9cc41bbaa81052b069fdb41d8e4df0a3a67767b13efefe867e4890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **956.3 MB (956263604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0fb98e0a2bb8731c705dd0055989e242dceefb73a9bcc741a0f819ead2822b2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:15 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:11:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:11:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:11:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 22:14:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed72e15eea09997a888cfd394babf47cd5d3ee9a2c1856f4c7f38000a28cd39`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6bae53520479265b0edca56a5a3c05822e791ced08e5c7231de5c0d547ae28`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 6.0 MB (5994357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bfebc4f1259f371e9045d574e48ccd4cafc66527ceff0773160f92e5eed2b`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890b14f7743317dbac8424f43f421d35c3760e3e790feec63d58f7f8660dace`  
		Last Modified: Wed, 01 Apr 2026 20:16:41 GMT  
		Size: 104.9 MB (104872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6941913bec3545a993c44a7e163faed16e361b4d7a736437dde612fd9509bbd`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c896a95beb5d795345bb3b17a68fb6ddf384eba91010e5ae0fab2b6ffaa4b50`  
		Last Modified: Wed, 01 Apr 2026 21:12:52 GMT  
		Size: 98.2 MB (98158288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9755a7b2bcd6ac84cdbfb843118ad74105566968c5fed29fe9a119f252f7512d`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 390.9 KB (390880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1387f1b937a6d9c6946869d2d0bb31a19208ce67c354b99e273fac62837f5c39`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e682bb1d7aab2c53fa42ed55165efef896598e4c59d1ea32413e718579cdd7`  
		Last Modified: Wed, 01 Apr 2026 21:12:50 GMT  
		Size: 23.3 MB (23334801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9ba8039051fc9645c2bdb77a90ae97c820ba269ac4323930620092f4ce263`  
		Last Modified: Wed, 01 Apr 2026 22:16:43 GMT  
		Size: 692.5 MB (692462255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:a2c26fc482767ec282e39ded61975a51f4daa034a72ca416f6ffb638d474dbee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58946266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302850cd45778c249b318dd1685ffff4d2a2f31dbf56dfb8cb827a13ce6c9c01`

```dockerfile
```

-	Layers:
	-	`sha256:0ae63e3fa5e30117af54d32549bacc1cc20cbc7dd169a7132052db8d8cb1a538`  
		Last Modified: Wed, 01 Apr 2026 22:16:29 GMT  
		Size: 58.9 MB (58936915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64bfeaaf162eeca610b8626745f51a1de007d8fdfa4559459cb10a38910de840`  
		Last Modified: Wed, 01 Apr 2026 22:16:26 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:df5d4e791ea19c44862328132b9c218f58efa299603f872fc707c015a440b013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.9 MB (916876945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a6a56ae7ed8d978b655b235981e7d48fb6a50091dace1c7f820a427deba9fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:09 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:15:52 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:12:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:12:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 22:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc0bc42613cab0a58d13ec77015563460d9740f7e9867c8256f65bf194cf98`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 1.2 MB (1214285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66fd6281dcdd3b1a9b6441c2607d70ef8e296483e894ed72f4e8d0cc94c907`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 5.9 MB (5948732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31af296322d1075bf72e1cc3420c7980512f421e9541f4b9fa43f9c2600f7999`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 97.3 KB (97306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d43e320d8992650cb03a0b71eb19d216643b7b26f2161f0a6e3eaf47edf968`  
		Last Modified: Wed, 01 Apr 2026 20:16:22 GMT  
		Size: 102.6 MB (102634213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818371cd205c99f6e214ae759d622585e624ffd84553b1b95e78eeefec55d9d3`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fccb60a4efb53f0b5a957f477b0472d72cf154bacdb5c7400d39996128d22`  
		Last Modified: Wed, 01 Apr 2026 21:13:10 GMT  
		Size: 95.8 MB (95795135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3925511d5109b8abc9487080e46a5482d78169e2622ce61b144bbf4d695a8079`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 390.9 KB (390881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3950ae4bb7a9331ecc9ef96b3c30cbc259e56f2fe92924c9e09e9531e508d330`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e75da22aaf38edd96540827c1ff07111fd2057047f1f4bbb90a5ffc383d83a`  
		Last Modified: Wed, 01 Apr 2026 21:13:09 GMT  
		Size: 22.7 MB (22727961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274220491018732e1e9d907da140974b080c59e189876870d5558c187bf42def`  
		Last Modified: Wed, 01 Apr 2026 22:16:56 GMT  
		Size: 660.5 MB (660458788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1fbbe2852ca7a6c38af98259b82264d1fc50d0b484e2acad03e95587ea971850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58930668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577fbe9760a1e7c9213d1b62fceddbb2fdd7c431cd28108c457bb81eca9df29a`

```dockerfile
```

-	Layers:
	-	`sha256:873c027741c06c4275fcb261fe2f3036520d58928076bbeb3910a175c9344e9e`  
		Last Modified: Wed, 01 Apr 2026 22:16:43 GMT  
		Size: 58.9 MB (58921236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2351b1f88b65099fc611865cc000e71635805542ed4b67d97d77a37c5090239`  
		Last Modified: Wed, 01 Apr 2026 22:16:40 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:ca58dcbc4db306c2c569509261675600fc21efee113c0960b7579b847006a541
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:db8d50ca3d9cc41bbaa81052b069fdb41d8e4df0a3a67767b13efefe867e4890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **956.3 MB (956263604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0fb98e0a2bb8731c705dd0055989e242dceefb73a9bcc741a0f819ead2822b2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:15 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:11:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:11:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:11:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 22:14:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed72e15eea09997a888cfd394babf47cd5d3ee9a2c1856f4c7f38000a28cd39`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6bae53520479265b0edca56a5a3c05822e791ced08e5c7231de5c0d547ae28`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 6.0 MB (5994357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bfebc4f1259f371e9045d574e48ccd4cafc66527ceff0773160f92e5eed2b`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890b14f7743317dbac8424f43f421d35c3760e3e790feec63d58f7f8660dace`  
		Last Modified: Wed, 01 Apr 2026 20:16:41 GMT  
		Size: 104.9 MB (104872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6941913bec3545a993c44a7e163faed16e361b4d7a736437dde612fd9509bbd`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c896a95beb5d795345bb3b17a68fb6ddf384eba91010e5ae0fab2b6ffaa4b50`  
		Last Modified: Wed, 01 Apr 2026 21:12:52 GMT  
		Size: 98.2 MB (98158288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9755a7b2bcd6ac84cdbfb843118ad74105566968c5fed29fe9a119f252f7512d`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 390.9 KB (390880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1387f1b937a6d9c6946869d2d0bb31a19208ce67c354b99e273fac62837f5c39`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e682bb1d7aab2c53fa42ed55165efef896598e4c59d1ea32413e718579cdd7`  
		Last Modified: Wed, 01 Apr 2026 21:12:50 GMT  
		Size: 23.3 MB (23334801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa9ba8039051fc9645c2bdb77a90ae97c820ba269ac4323930620092f4ce263`  
		Last Modified: Wed, 01 Apr 2026 22:16:43 GMT  
		Size: 692.5 MB (692462255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:a2c26fc482767ec282e39ded61975a51f4daa034a72ca416f6ffb638d474dbee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58946266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302850cd45778c249b318dd1685ffff4d2a2f31dbf56dfb8cb827a13ce6c9c01`

```dockerfile
```

-	Layers:
	-	`sha256:0ae63e3fa5e30117af54d32549bacc1cc20cbc7dd169a7132052db8d8cb1a538`  
		Last Modified: Wed, 01 Apr 2026 22:16:29 GMT  
		Size: 58.9 MB (58936915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64bfeaaf162eeca610b8626745f51a1de007d8fdfa4559459cb10a38910de840`  
		Last Modified: Wed, 01 Apr 2026 22:16:26 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:df5d4e791ea19c44862328132b9c218f58efa299603f872fc707c015a440b013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.9 MB (916876945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a6a56ae7ed8d978b655b235981e7d48fb6a50091dace1c7f820a427deba9fd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:09 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:15:52 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:12:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:12:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 22:13:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc0bc42613cab0a58d13ec77015563460d9740f7e9867c8256f65bf194cf98`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 1.2 MB (1214285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66fd6281dcdd3b1a9b6441c2607d70ef8e296483e894ed72f4e8d0cc94c907`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 5.9 MB (5948732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31af296322d1075bf72e1cc3420c7980512f421e9541f4b9fa43f9c2600f7999`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 97.3 KB (97306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d43e320d8992650cb03a0b71eb19d216643b7b26f2161f0a6e3eaf47edf968`  
		Last Modified: Wed, 01 Apr 2026 20:16:22 GMT  
		Size: 102.6 MB (102634213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818371cd205c99f6e214ae759d622585e624ffd84553b1b95e78eeefec55d9d3`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fccb60a4efb53f0b5a957f477b0472d72cf154bacdb5c7400d39996128d22`  
		Last Modified: Wed, 01 Apr 2026 21:13:10 GMT  
		Size: 95.8 MB (95795135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3925511d5109b8abc9487080e46a5482d78169e2622ce61b144bbf4d695a8079`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 390.9 KB (390881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3950ae4bb7a9331ecc9ef96b3c30cbc259e56f2fe92924c9e09e9531e508d330`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e75da22aaf38edd96540827c1ff07111fd2057047f1f4bbb90a5ffc383d83a`  
		Last Modified: Wed, 01 Apr 2026 21:13:09 GMT  
		Size: 22.7 MB (22727961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274220491018732e1e9d907da140974b080c59e189876870d5558c187bf42def`  
		Last Modified: Wed, 01 Apr 2026 22:16:56 GMT  
		Size: 660.5 MB (660458788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:1fbbe2852ca7a6c38af98259b82264d1fc50d0b484e2acad03e95587ea971850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58930668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577fbe9760a1e7c9213d1b62fceddbb2fdd7c431cd28108c457bb81eca9df29a`

```dockerfile
```

-	Layers:
	-	`sha256:873c027741c06c4275fcb261fe2f3036520d58928076bbeb3910a175c9344e9e`  
		Last Modified: Wed, 01 Apr 2026 22:16:43 GMT  
		Size: 58.9 MB (58921236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2351b1f88b65099fc611865cc000e71635805542ed4b67d97d77a37c5090239`  
		Last Modified: Wed, 01 Apr 2026 22:16:40 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:1660822550ab8bcbe0145acf4ff0fee33b0fae4f5d4b101d7d11cd5d42876d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:6f2b851ee039c447ad27437efa96459396bc433aabaafdb6fb424513cda93be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263801349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c08ba95445517fba6074f26f19f6d1086c8fe9c760675c8f96139fe41c82cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:15 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:11:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:11:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:11:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed72e15eea09997a888cfd394babf47cd5d3ee9a2c1856f4c7f38000a28cd39`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6bae53520479265b0edca56a5a3c05822e791ced08e5c7231de5c0d547ae28`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 6.0 MB (5994357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bfebc4f1259f371e9045d574e48ccd4cafc66527ceff0773160f92e5eed2b`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890b14f7743317dbac8424f43f421d35c3760e3e790feec63d58f7f8660dace`  
		Last Modified: Wed, 01 Apr 2026 20:16:41 GMT  
		Size: 104.9 MB (104872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6941913bec3545a993c44a7e163faed16e361b4d7a736437dde612fd9509bbd`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c896a95beb5d795345bb3b17a68fb6ddf384eba91010e5ae0fab2b6ffaa4b50`  
		Last Modified: Wed, 01 Apr 2026 21:12:52 GMT  
		Size: 98.2 MB (98158288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9755a7b2bcd6ac84cdbfb843118ad74105566968c5fed29fe9a119f252f7512d`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 390.9 KB (390880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1387f1b937a6d9c6946869d2d0bb31a19208ce67c354b99e273fac62837f5c39`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e682bb1d7aab2c53fa42ed55165efef896598e4c59d1ea32413e718579cdd7`  
		Last Modified: Wed, 01 Apr 2026 21:12:50 GMT  
		Size: 23.3 MB (23334801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0c2b895c5b596bf231168aa1a98145146cc9cd6d27338138c072ee74be0644fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23851650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39316ec407a80e44290c68c9fd160e7ca4175cc667f13bd2b2bcb628b9fa0eb8`

```dockerfile
```

-	Layers:
	-	`sha256:369d1fc2b74f9116ecbfe60f6dcc623be9a114f4fe7ef20e6b8cee81a86b3b30`  
		Last Modified: Wed, 01 Apr 2026 21:12:50 GMT  
		Size: 23.8 MB (23835302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304ac9b7f10316cc2584dfffb2d209fba00360241c42350b636d2148009af445`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:815bf0ffa4615ce6e1e970af3cd142083cf22ef17745bec2b4c4446b80fcde3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256418157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725c9064b4bf32192dce3a9b8c85feac00588df68f91b0d11026d3d4a0f866a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:09 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:15:52 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:12:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:12:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc0bc42613cab0a58d13ec77015563460d9740f7e9867c8256f65bf194cf98`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 1.2 MB (1214285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66fd6281dcdd3b1a9b6441c2607d70ef8e296483e894ed72f4e8d0cc94c907`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 5.9 MB (5948732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31af296322d1075bf72e1cc3420c7980512f421e9541f4b9fa43f9c2600f7999`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 97.3 KB (97306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d43e320d8992650cb03a0b71eb19d216643b7b26f2161f0a6e3eaf47edf968`  
		Last Modified: Wed, 01 Apr 2026 20:16:22 GMT  
		Size: 102.6 MB (102634213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818371cd205c99f6e214ae759d622585e624ffd84553b1b95e78eeefec55d9d3`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fccb60a4efb53f0b5a957f477b0472d72cf154bacdb5c7400d39996128d22`  
		Last Modified: Wed, 01 Apr 2026 21:13:10 GMT  
		Size: 95.8 MB (95795135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3925511d5109b8abc9487080e46a5482d78169e2622ce61b144bbf4d695a8079`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 390.9 KB (390881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3950ae4bb7a9331ecc9ef96b3c30cbc259e56f2fe92924c9e09e9531e508d330`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e75da22aaf38edd96540827c1ff07111fd2057047f1f4bbb90a5ffc383d83a`  
		Last Modified: Wed, 01 Apr 2026 21:13:09 GMT  
		Size: 22.7 MB (22727961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b418547700361565d5a6f3ec53a212af039246a963c835416f2b38ad6392203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23864803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ab69dd5891a9fb6e81a9c4fd30d3121a7de1092dd7202e9dfdf6ba612e0dc`

```dockerfile
```

-	Layers:
	-	`sha256:dd5b956eb4161fe3111d0d1c96084bb839a7f164088df3054008c5ec2bd122ff`  
		Last Modified: Wed, 01 Apr 2026 21:13:09 GMT  
		Size: 23.8 MB (23848319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51b7b6018fc927eaa27435452ec893b024616dd5c51ee47a4aa6e2884f1f92d`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:1660822550ab8bcbe0145acf4ff0fee33b0fae4f5d4b101d7d11cd5d42876d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:6f2b851ee039c447ad27437efa96459396bc433aabaafdb6fb424513cda93be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263801349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c08ba95445517fba6074f26f19f6d1086c8fe9c760675c8f96139fe41c82cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:15 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:11:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:11:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:11:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed72e15eea09997a888cfd394babf47cd5d3ee9a2c1856f4c7f38000a28cd39`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6bae53520479265b0edca56a5a3c05822e791ced08e5c7231de5c0d547ae28`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 6.0 MB (5994357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bfebc4f1259f371e9045d574e48ccd4cafc66527ceff0773160f92e5eed2b`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890b14f7743317dbac8424f43f421d35c3760e3e790feec63d58f7f8660dace`  
		Last Modified: Wed, 01 Apr 2026 20:16:41 GMT  
		Size: 104.9 MB (104872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6941913bec3545a993c44a7e163faed16e361b4d7a736437dde612fd9509bbd`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c896a95beb5d795345bb3b17a68fb6ddf384eba91010e5ae0fab2b6ffaa4b50`  
		Last Modified: Wed, 01 Apr 2026 21:12:52 GMT  
		Size: 98.2 MB (98158288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9755a7b2bcd6ac84cdbfb843118ad74105566968c5fed29fe9a119f252f7512d`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 390.9 KB (390880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1387f1b937a6d9c6946869d2d0bb31a19208ce67c354b99e273fac62837f5c39`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e682bb1d7aab2c53fa42ed55165efef896598e4c59d1ea32413e718579cdd7`  
		Last Modified: Wed, 01 Apr 2026 21:12:50 GMT  
		Size: 23.3 MB (23334801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:0c2b895c5b596bf231168aa1a98145146cc9cd6d27338138c072ee74be0644fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23851650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39316ec407a80e44290c68c9fd160e7ca4175cc667f13bd2b2bcb628b9fa0eb8`

```dockerfile
```

-	Layers:
	-	`sha256:369d1fc2b74f9116ecbfe60f6dcc623be9a114f4fe7ef20e6b8cee81a86b3b30`  
		Last Modified: Wed, 01 Apr 2026 21:12:50 GMT  
		Size: 23.8 MB (23835302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304ac9b7f10316cc2584dfffb2d209fba00360241c42350b636d2148009af445`  
		Last Modified: Wed, 01 Apr 2026 21:12:49 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:815bf0ffa4615ce6e1e970af3cd142083cf22ef17745bec2b4c4446b80fcde3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256418157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2725c9064b4bf32192dce3a9b8c85feac00588df68f91b0d11026d3d4a0f866a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:09 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:15:52 GMT
CMD ["bash"]
# Wed, 01 Apr 2026 21:12:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 01 Apr 2026 21:12:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 01 Apr 2026 21:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc0bc42613cab0a58d13ec77015563460d9740f7e9867c8256f65bf194cf98`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 1.2 MB (1214285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66fd6281dcdd3b1a9b6441c2607d70ef8e296483e894ed72f4e8d0cc94c907`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 5.9 MB (5948732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31af296322d1075bf72e1cc3420c7980512f421e9541f4b9fa43f9c2600f7999`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 97.3 KB (97306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d43e320d8992650cb03a0b71eb19d216643b7b26f2161f0a6e3eaf47edf968`  
		Last Modified: Wed, 01 Apr 2026 20:16:22 GMT  
		Size: 102.6 MB (102634213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818371cd205c99f6e214ae759d622585e624ffd84553b1b95e78eeefec55d9d3`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082fccb60a4efb53f0b5a957f477b0472d72cf154bacdb5c7400d39996128d22`  
		Last Modified: Wed, 01 Apr 2026 21:13:10 GMT  
		Size: 95.8 MB (95795135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3925511d5109b8abc9487080e46a5482d78169e2622ce61b144bbf4d695a8079`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 390.9 KB (390881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3950ae4bb7a9331ecc9ef96b3c30cbc259e56f2fe92924c9e09e9531e508d330`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e75da22aaf38edd96540827c1ff07111fd2057047f1f4bbb90a5ffc383d83a`  
		Last Modified: Wed, 01 Apr 2026 21:13:09 GMT  
		Size: 22.7 MB (22727961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:b418547700361565d5a6f3ec53a212af039246a963c835416f2b38ad6392203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23864803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3ab69dd5891a9fb6e81a9c4fd30d3121a7de1092dd7202e9dfdf6ba612e0dc`

```dockerfile
```

-	Layers:
	-	`sha256:dd5b956eb4161fe3111d0d1c96084bb839a7f164088df3054008c5ec2bd122ff`  
		Last Modified: Wed, 01 Apr 2026 21:13:09 GMT  
		Size: 23.8 MB (23848319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51b7b6018fc927eaa27435452ec893b024616dd5c51ee47a4aa6e2884f1f92d`  
		Last Modified: Wed, 01 Apr 2026 21:13:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:e0409a258a7a1275fe8b9afc6ce7ff1e75e9b5ba73b51b6d06fb16b2726f95e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:52450ec51729dbb32012aa5416f02277bd17497f8bd8e6abaeb38ee4e30bf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141914860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972a5ae48203a9e8269be6f9f75b411734bdfc00d08301328cc8b329166a99cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed72e15eea09997a888cfd394babf47cd5d3ee9a2c1856f4c7f38000a28cd39`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6bae53520479265b0edca56a5a3c05822e791ced08e5c7231de5c0d547ae28`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 6.0 MB (5994357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bfebc4f1259f371e9045d574e48ccd4cafc66527ceff0773160f92e5eed2b`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890b14f7743317dbac8424f43f421d35c3760e3e790feec63d58f7f8660dace`  
		Last Modified: Wed, 01 Apr 2026 20:16:41 GMT  
		Size: 104.9 MB (104872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6941913bec3545a993c44a7e163faed16e361b4d7a736437dde612fd9509bbd`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:43755a3f7613f1dd2826cf2555152ecd9669362b914656aa6d508fef634b5ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59fd4b3d33fe457241fb3ab4265e7d134e26b079568df6790e64b02ebe16d7b`

```dockerfile
```

-	Layers:
	-	`sha256:aa3ed7fc9309ecaf57b690158ba089f0da6a87bcdc8fcad974a8e3f163238b91`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 17.8 MB (17802889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f0a3522c54ad82092531300e1d1010fab759007c61a1d0be9191dc0c08b193`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:355363572714aec6f643157394eae0954e3cd0fd88303b883c044750d377819d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137501676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddd3ac82c5f9104d261ff1b80e8b7fb63467950c4653e59f8b6b3bf734acc25`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:09 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:15:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc0bc42613cab0a58d13ec77015563460d9740f7e9867c8256f65bf194cf98`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 1.2 MB (1214285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66fd6281dcdd3b1a9b6441c2607d70ef8e296483e894ed72f4e8d0cc94c907`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 5.9 MB (5948732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31af296322d1075bf72e1cc3420c7980512f421e9541f4b9fa43f9c2600f7999`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 97.3 KB (97306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d43e320d8992650cb03a0b71eb19d216643b7b26f2161f0a6e3eaf47edf968`  
		Last Modified: Wed, 01 Apr 2026 20:16:22 GMT  
		Size: 102.6 MB (102634213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818371cd205c99f6e214ae759d622585e624ffd84553b1b95e78eeefec55d9d3`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:be14b6c326c2ed1a1f2ce9c96f681e3e4ff994ab18a03f3f419d29ab1b354f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492b33062b62aed6651ba319549de0bd23625a663ae60dc88ebc754b21f0bb77`

```dockerfile
```

-	Layers:
	-	`sha256:b380490051e96c35fdc82298d61bd40ac282fbfc3e5fc7cee15ace54ce092420`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 17.8 MB (17789234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55108833cb7db6e4704823226f9ac12fc9a3cdf39c01abbc4c2423fa8d588bd2`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:e0409a258a7a1275fe8b9afc6ce7ff1e75e9b5ba73b51b6d06fb16b2726f95e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:52450ec51729dbb32012aa5416f02277bd17497f8bd8e6abaeb38ee4e30bf811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141914860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972a5ae48203a9e8269be6f9f75b411734bdfc00d08301328cc8b329166a99cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:16:15 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed72e15eea09997a888cfd394babf47cd5d3ee9a2c1856f4c7f38000a28cd39`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6bae53520479265b0edca56a5a3c05822e791ced08e5c7231de5c0d547ae28`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 6.0 MB (5994357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18bfebc4f1259f371e9045d574e48ccd4cafc66527ceff0773160f92e5eed2b`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6890b14f7743317dbac8424f43f421d35c3760e3e790feec63d58f7f8660dace`  
		Last Modified: Wed, 01 Apr 2026 20:16:41 GMT  
		Size: 104.9 MB (104872609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6941913bec3545a993c44a7e163faed16e361b4d7a736437dde612fd9509bbd`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:43755a3f7613f1dd2826cf2555152ecd9669362b914656aa6d508fef634b5ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59fd4b3d33fe457241fb3ab4265e7d134e26b079568df6790e64b02ebe16d7b`

```dockerfile
```

-	Layers:
	-	`sha256:aa3ed7fc9309ecaf57b690158ba089f0da6a87bcdc8fcad974a8e3f163238b91`  
		Last Modified: Wed, 01 Apr 2026 20:16:40 GMT  
		Size: 17.8 MB (17802889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f0a3522c54ad82092531300e1d1010fab759007c61a1d0be9191dc0c08b193`  
		Last Modified: Wed, 01 Apr 2026 20:16:39 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:355363572714aec6f643157394eae0954e3cd0fd88303b883c044750d377819d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137501676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddd3ac82c5f9104d261ff1b80e8b7fb63467950c4653e59f8b6b3bf734acc25`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:09 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LANG=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Apr 2026 20:15:52 GMT
ENV ROS_DISTRO=humble
# Wed, 01 Apr 2026 20:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:15:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Apr 2026 20:15:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc0bc42613cab0a58d13ec77015563460d9740f7e9867c8256f65bf194cf98`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 1.2 MB (1214285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac66fd6281dcdd3b1a9b6441c2607d70ef8e296483e894ed72f4e8d0cc94c907`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 5.9 MB (5948732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31af296322d1075bf72e1cc3420c7980512f421e9541f4b9fa43f9c2600f7999`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 97.3 KB (97306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d43e320d8992650cb03a0b71eb19d216643b7b26f2161f0a6e3eaf47edf968`  
		Last Modified: Wed, 01 Apr 2026 20:16:22 GMT  
		Size: 102.6 MB (102634213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818371cd205c99f6e214ae759d622585e624ffd84553b1b95e78eeefec55d9d3`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:be14b6c326c2ed1a1f2ce9c96f681e3e4ff994ab18a03f3f419d29ab1b354f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492b33062b62aed6651ba319549de0bd23625a663ae60dc88ebc754b21f0bb77`

```dockerfile
```

-	Layers:
	-	`sha256:b380490051e96c35fdc82298d61bd40ac282fbfc3e5fc7cee15ace54ce092420`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 17.8 MB (17789234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55108833cb7db6e4704823226f9ac12fc9a3cdf39c01abbc4c2423fa8d588bd2`  
		Last Modified: Wed, 01 Apr 2026 20:16:18 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:d1eca5bd28aef56ea7370e8d35796a0804ed297f8f245283817c85475e2c73e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:db27fc6125927590ee131d5f4bffbffca9dea368424684f707103afad34614c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296283805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba05340ef60bdf2b4273658986b4c71b7ca689bde04f1182f1e3d04629ef36b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8dd6647a3c1e7d18001a45a8789638361caf8dfef0f307b190a1384f0a2413`  
		Last Modified: Tue, 07 Apr 2026 03:31:11 GMT  
		Size: 110.2 MB (110188982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6af0b3531a3918b50c613a65fd716cbff3bb7b3243c89bb4312d5e60cdf14e`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 405.7 KB (405659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf926922fb8b2b3271f1be2185badc4d52812efb69c4186e57f4bb5b97e60cb`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e9897748f310d88fd17993769228e2f42207223ca0c90914f25c4d40da3c7`  
		Last Modified: Tue, 07 Apr 2026 03:31:09 GMT  
		Size: 28.0 MB (28010350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:bbfb05f0c551c51da32aa0f57e6d43f9847587d2479e338e58ae37c231e20929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07e0628f14767a277bce48ac54ab97d98056d618026bd9d82d6d6fd6caa43ea`

```dockerfile
```

-	Layers:
	-	`sha256:6f2d7574bb1fb6b1621a352e11874c092e186023e5d2523fe4c6f3975845a7c6`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 24.6 MB (24571750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a641ee42aa231b2615a8ac734ab358d1e6fb5f00fb0a707adc56abebc2384ae4`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:637d8247407ec5a2efb5afdfed8e56c31cc3227f23dc6e6b92d7d409566546c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284739621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4b7e222c910549863d8b92dddc2274f61d2beef948949587de641333bf328e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161909dfa0ad7f5997c40a973a116ed80646d74843f0a597dc20ed3e125a8e7`  
		Last Modified: Tue, 07 Apr 2026 03:43:19 GMT  
		Size: 105.6 MB (105602757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acde01ab9a2e4a57c5d4f65c24cb93972ea90a24913b0a6fe47933637d93d94`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 405.7 KB (405655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e592252c9ae49ff56f1b4f86b18208ba2ccc2fd338f6501a7ce53ed3d869dd`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 2.5 KB (2519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b8c78e8323633d8f1b0a4cbde5ac8aca13922c7dc16e99313d98fb1d9169c`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 27.1 MB (27103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:3119a143d3c64ab3b53d92ce1e6251635f38bb2cc3692a6f7e5a83e0333e4ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b76c6bbed17c5df5c2ef77a2c1f8cea7dc86ed393c664e4fda16b4eecd189`

```dockerfile
```

-	Layers:
	-	`sha256:5805811070e70ffaf29a1282e772de909cc339923d7675d64b3c7466d666a2d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 24.6 MB (24594011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225da648b529e7e6431b0259d1bf4d5069c749064d2377239124819c4a4cb058`  
		Last Modified: Tue, 07 Apr 2026 03:43:15 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:b4cb947f343cb7aae84f2c568fb08c98ea48923f8e3015a7be3a72e011c7d6a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:c20aff77ba56b7be673f61e98c1137439a74ee4e572ef48b905af2f44c2ce278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080579520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7305a62a09a778c80206513c1dcd51ca8f1bfe31bfbb2a9608b00eaa50ecf82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8dd6647a3c1e7d18001a45a8789638361caf8dfef0f307b190a1384f0a2413`  
		Last Modified: Tue, 07 Apr 2026 03:31:11 GMT  
		Size: 110.2 MB (110188982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6af0b3531a3918b50c613a65fd716cbff3bb7b3243c89bb4312d5e60cdf14e`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 405.7 KB (405659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf926922fb8b2b3271f1be2185badc4d52812efb69c4186e57f4bb5b97e60cb`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e9897748f310d88fd17993769228e2f42207223ca0c90914f25c4d40da3c7`  
		Last Modified: Tue, 07 Apr 2026 03:31:09 GMT  
		Size: 28.0 MB (28010350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbbb9f561c02a517af508d90c638f9dd5ca527ecb662bef78029d81a4d998b0`  
		Last Modified: Tue, 07 Apr 2026 05:01:23 GMT  
		Size: 784.3 MB (784295715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9857cc23020ae6f264eef773a1a0d3a6941eab6cef0f6d4d3e49366da3da17a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60738111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d7c7b6e6c7e49675baf9db45b607a422716c651fb221ee97ae8fde4f1efc8a`

```dockerfile
```

-	Layers:
	-	`sha256:f1988328b5c59e064ec2867182b834eafdbf7ebc3c62d1def734792f095c61d0`  
		Last Modified: Tue, 07 Apr 2026 05:00:44 GMT  
		Size: 60.7 MB (60728772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a903f7162cbe7e88b054e9415f3bd534f5a37ac61466fc5cc12526a5d645ffc`  
		Last Modified: Tue, 07 Apr 2026 05:00:42 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c5520caba868b61968962c494030ffc68c3b41b4f75933e4d7facc94836de030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.2 MB (983187921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9ad98273a04e2c42a7f3063705bff5f522e1b2f4330b8e3b23386b9eaa608f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:02:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161909dfa0ad7f5997c40a973a116ed80646d74843f0a597dc20ed3e125a8e7`  
		Last Modified: Tue, 07 Apr 2026 03:43:19 GMT  
		Size: 105.6 MB (105602757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acde01ab9a2e4a57c5d4f65c24cb93972ea90a24913b0a6fe47933637d93d94`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 405.7 KB (405655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e592252c9ae49ff56f1b4f86b18208ba2ccc2fd338f6501a7ce53ed3d869dd`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 2.5 KB (2519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b8c78e8323633d8f1b0a4cbde5ac8aca13922c7dc16e99313d98fb1d9169c`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 27.1 MB (27103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48105a07856f73b4deb14484aa74c7d18c537b920940151130b841e1754d08f9`  
		Last Modified: Tue, 07 Apr 2026 05:05:35 GMT  
		Size: 698.4 MB (698448300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:6d826aedb138c604e66e75465414efb0e2d605a0c902bf195df5367c48cdf4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60668699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337aa2b208f38b5c7f9a943462907748a37fa3cbf9c8939d5f9e7e3fca787065`

```dockerfile
```

-	Layers:
	-	`sha256:365572da5e6b035d1a8c167bb682d0d4c6e4bf3cdefad6223e93cf9c947e6fc4`  
		Last Modified: Tue, 07 Apr 2026 05:05:21 GMT  
		Size: 60.7 MB (60659280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513be45092d456f84f1fd7fba9da7d6900f60e315f6862d10258d34ac5e28785`  
		Last Modified: Tue, 07 Apr 2026 05:05:18 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:b4cb947f343cb7aae84f2c568fb08c98ea48923f8e3015a7be3a72e011c7d6a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:c20aff77ba56b7be673f61e98c1137439a74ee4e572ef48b905af2f44c2ce278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080579520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7305a62a09a778c80206513c1dcd51ca8f1bfe31bfbb2a9608b00eaa50ecf82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8dd6647a3c1e7d18001a45a8789638361caf8dfef0f307b190a1384f0a2413`  
		Last Modified: Tue, 07 Apr 2026 03:31:11 GMT  
		Size: 110.2 MB (110188982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6af0b3531a3918b50c613a65fd716cbff3bb7b3243c89bb4312d5e60cdf14e`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 405.7 KB (405659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf926922fb8b2b3271f1be2185badc4d52812efb69c4186e57f4bb5b97e60cb`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e9897748f310d88fd17993769228e2f42207223ca0c90914f25c4d40da3c7`  
		Last Modified: Tue, 07 Apr 2026 03:31:09 GMT  
		Size: 28.0 MB (28010350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbbb9f561c02a517af508d90c638f9dd5ca527ecb662bef78029d81a4d998b0`  
		Last Modified: Tue, 07 Apr 2026 05:01:23 GMT  
		Size: 784.3 MB (784295715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9857cc23020ae6f264eef773a1a0d3a6941eab6cef0f6d4d3e49366da3da17a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60738111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d7c7b6e6c7e49675baf9db45b607a422716c651fb221ee97ae8fde4f1efc8a`

```dockerfile
```

-	Layers:
	-	`sha256:f1988328b5c59e064ec2867182b834eafdbf7ebc3c62d1def734792f095c61d0`  
		Last Modified: Tue, 07 Apr 2026 05:00:44 GMT  
		Size: 60.7 MB (60728772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a903f7162cbe7e88b054e9415f3bd534f5a37ac61466fc5cc12526a5d645ffc`  
		Last Modified: Tue, 07 Apr 2026 05:00:42 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c5520caba868b61968962c494030ffc68c3b41b4f75933e4d7facc94836de030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.2 MB (983187921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9ad98273a04e2c42a7f3063705bff5f522e1b2f4330b8e3b23386b9eaa608f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:02:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161909dfa0ad7f5997c40a973a116ed80646d74843f0a597dc20ed3e125a8e7`  
		Last Modified: Tue, 07 Apr 2026 03:43:19 GMT  
		Size: 105.6 MB (105602757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acde01ab9a2e4a57c5d4f65c24cb93972ea90a24913b0a6fe47933637d93d94`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 405.7 KB (405655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e592252c9ae49ff56f1b4f86b18208ba2ccc2fd338f6501a7ce53ed3d869dd`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 2.5 KB (2519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b8c78e8323633d8f1b0a4cbde5ac8aca13922c7dc16e99313d98fb1d9169c`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 27.1 MB (27103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48105a07856f73b4deb14484aa74c7d18c537b920940151130b841e1754d08f9`  
		Last Modified: Tue, 07 Apr 2026 05:05:35 GMT  
		Size: 698.4 MB (698448300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6d826aedb138c604e66e75465414efb0e2d605a0c902bf195df5367c48cdf4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60668699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337aa2b208f38b5c7f9a943462907748a37fa3cbf9c8939d5f9e7e3fca787065`

```dockerfile
```

-	Layers:
	-	`sha256:365572da5e6b035d1a8c167bb682d0d4c6e4bf3cdefad6223e93cf9c947e6fc4`  
		Last Modified: Tue, 07 Apr 2026 05:05:21 GMT  
		Size: 60.7 MB (60659280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513be45092d456f84f1fd7fba9da7d6900f60e315f6862d10258d34ac5e28785`  
		Last Modified: Tue, 07 Apr 2026 05:05:18 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:d1eca5bd28aef56ea7370e8d35796a0804ed297f8f245283817c85475e2c73e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:db27fc6125927590ee131d5f4bffbffca9dea368424684f707103afad34614c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296283805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba05340ef60bdf2b4273658986b4c71b7ca689bde04f1182f1e3d04629ef36b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8dd6647a3c1e7d18001a45a8789638361caf8dfef0f307b190a1384f0a2413`  
		Last Modified: Tue, 07 Apr 2026 03:31:11 GMT  
		Size: 110.2 MB (110188982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6af0b3531a3918b50c613a65fd716cbff3bb7b3243c89bb4312d5e60cdf14e`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 405.7 KB (405659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf926922fb8b2b3271f1be2185badc4d52812efb69c4186e57f4bb5b97e60cb`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e9897748f310d88fd17993769228e2f42207223ca0c90914f25c4d40da3c7`  
		Last Modified: Tue, 07 Apr 2026 03:31:09 GMT  
		Size: 28.0 MB (28010350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:bbfb05f0c551c51da32aa0f57e6d43f9847587d2479e338e58ae37c231e20929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07e0628f14767a277bce48ac54ab97d98056d618026bd9d82d6d6fd6caa43ea`

```dockerfile
```

-	Layers:
	-	`sha256:6f2d7574bb1fb6b1621a352e11874c092e186023e5d2523fe4c6f3975845a7c6`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 24.6 MB (24571750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a641ee42aa231b2615a8ac734ab358d1e6fb5f00fb0a707adc56abebc2384ae4`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:637d8247407ec5a2efb5afdfed8e56c31cc3227f23dc6e6b92d7d409566546c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284739621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4b7e222c910549863d8b92dddc2274f61d2beef948949587de641333bf328e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161909dfa0ad7f5997c40a973a116ed80646d74843f0a597dc20ed3e125a8e7`  
		Last Modified: Tue, 07 Apr 2026 03:43:19 GMT  
		Size: 105.6 MB (105602757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acde01ab9a2e4a57c5d4f65c24cb93972ea90a24913b0a6fe47933637d93d94`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 405.7 KB (405655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e592252c9ae49ff56f1b4f86b18208ba2ccc2fd338f6501a7ce53ed3d869dd`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 2.5 KB (2519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b8c78e8323633d8f1b0a4cbde5ac8aca13922c7dc16e99313d98fb1d9169c`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 27.1 MB (27103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:3119a143d3c64ab3b53d92ce1e6251635f38bb2cc3692a6f7e5a83e0333e4ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b76c6bbed17c5df5c2ef77a2c1f8cea7dc86ed393c664e4fda16b4eecd189`

```dockerfile
```

-	Layers:
	-	`sha256:5805811070e70ffaf29a1282e772de909cc339923d7675d64b3c7466d666a2d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 24.6 MB (24594011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225da648b529e7e6431b0259d1bf4d5069c749064d2377239124819c4a4cb058`  
		Last Modified: Tue, 07 Apr 2026 03:43:15 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:d1eca5bd28aef56ea7370e8d35796a0804ed297f8f245283817c85475e2c73e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:db27fc6125927590ee131d5f4bffbffca9dea368424684f707103afad34614c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296283805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba05340ef60bdf2b4273658986b4c71b7ca689bde04f1182f1e3d04629ef36b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8dd6647a3c1e7d18001a45a8789638361caf8dfef0f307b190a1384f0a2413`  
		Last Modified: Tue, 07 Apr 2026 03:31:11 GMT  
		Size: 110.2 MB (110188982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6af0b3531a3918b50c613a65fd716cbff3bb7b3243c89bb4312d5e60cdf14e`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 405.7 KB (405659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf926922fb8b2b3271f1be2185badc4d52812efb69c4186e57f4bb5b97e60cb`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e9897748f310d88fd17993769228e2f42207223ca0c90914f25c4d40da3c7`  
		Last Modified: Tue, 07 Apr 2026 03:31:09 GMT  
		Size: 28.0 MB (28010350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:bbfb05f0c551c51da32aa0f57e6d43f9847587d2479e338e58ae37c231e20929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07e0628f14767a277bce48ac54ab97d98056d618026bd9d82d6d6fd6caa43ea`

```dockerfile
```

-	Layers:
	-	`sha256:6f2d7574bb1fb6b1621a352e11874c092e186023e5d2523fe4c6f3975845a7c6`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 24.6 MB (24571750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a641ee42aa231b2615a8ac734ab358d1e6fb5f00fb0a707adc56abebc2384ae4`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:637d8247407ec5a2efb5afdfed8e56c31cc3227f23dc6e6b92d7d409566546c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284739621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4b7e222c910549863d8b92dddc2274f61d2beef948949587de641333bf328e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161909dfa0ad7f5997c40a973a116ed80646d74843f0a597dc20ed3e125a8e7`  
		Last Modified: Tue, 07 Apr 2026 03:43:19 GMT  
		Size: 105.6 MB (105602757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acde01ab9a2e4a57c5d4f65c24cb93972ea90a24913b0a6fe47933637d93d94`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 405.7 KB (405655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e592252c9ae49ff56f1b4f86b18208ba2ccc2fd338f6501a7ce53ed3d869dd`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 2.5 KB (2519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b8c78e8323633d8f1b0a4cbde5ac8aca13922c7dc16e99313d98fb1d9169c`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 27.1 MB (27103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:3119a143d3c64ab3b53d92ce1e6251635f38bb2cc3692a6f7e5a83e0333e4ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b76c6bbed17c5df5c2ef77a2c1f8cea7dc86ed393c664e4fda16b4eecd189`

```dockerfile
```

-	Layers:
	-	`sha256:5805811070e70ffaf29a1282e772de909cc339923d7675d64b3c7466d666a2d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 24.6 MB (24594011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225da648b529e7e6431b0259d1bf4d5069c749064d2377239124819c4a4cb058`  
		Last Modified: Tue, 07 Apr 2026 03:43:15 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:83ffbe8efc6b37f20e7cb4a4af0c9ec556f5222eb3eff0adc687ac2552b85589
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:abaf0d5b1c4272b021f9c12f23e267d1d7740c9a0716f74b6fd1c0b53ebaaabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157676277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b20c925c68bf455766410e82359ba652d4ffdec1b1abd553cbe062f8776a838`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:934253c51a14ba5879aa9f8c7795d888aaf31af4894ea8f93dd889dac2c49181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdbd951b91babbb3678eb3ab6a84b8b41d96cc5ee7cc4851291ea3c1e661fce`

```dockerfile
```

-	Layers:
	-	`sha256:f4e38c3dec79902d1841ee4dc073b27d46479d2a4da84d721a9c6ed34219418f`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830ea8df1cff2451c7a44f9a286358a89eb9cb9bd0208dfe0b6487f22798c59`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0a1cc042e1611d8f2b9ecb7be39ba51715d33a1e9aa29d7dc38f8e9cd75ae9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151625197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf163ac9fa79261e25774d31c542e875759bcc789f9d7438c5e5e7e2174d3c9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6e1ea3944a0b3fb1c5be59ca8085fa1f155ff7014b89ae7a954efb8cf23635d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cbb6a86aba99e6b013dac98bd091c904a230f8a73457fe47dd863bef88179`

```dockerfile
```

-	Layers:
	-	`sha256:4debb5b556b74709b6e1a5210eaab7b97136b7f646b396cb17422ec68be84f33`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a88731848c1ea876f483f7a4111728ed24ba7df599cce5e60df0cb2aeba403`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:83ffbe8efc6b37f20e7cb4a4af0c9ec556f5222eb3eff0adc687ac2552b85589
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:abaf0d5b1c4272b021f9c12f23e267d1d7740c9a0716f74b6fd1c0b53ebaaabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157676277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b20c925c68bf455766410e82359ba652d4ffdec1b1abd553cbe062f8776a838`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:934253c51a14ba5879aa9f8c7795d888aaf31af4894ea8f93dd889dac2c49181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdbd951b91babbb3678eb3ab6a84b8b41d96cc5ee7cc4851291ea3c1e661fce`

```dockerfile
```

-	Layers:
	-	`sha256:f4e38c3dec79902d1841ee4dc073b27d46479d2a4da84d721a9c6ed34219418f`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c830ea8df1cff2451c7a44f9a286358a89eb9cb9bd0208dfe0b6487f22798c59`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0a1cc042e1611d8f2b9ecb7be39ba51715d33a1e9aa29d7dc38f8e9cd75ae9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151625197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf163ac9fa79261e25774d31c542e875759bcc789f9d7438c5e5e7e2174d3c9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6e1ea3944a0b3fb1c5be59ca8085fa1f155ff7014b89ae7a954efb8cf23635d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068cbb6a86aba99e6b013dac98bd091c904a230f8a73457fe47dd863bef88179`

```dockerfile
```

-	Layers:
	-	`sha256:4debb5b556b74709b6e1a5210eaab7b97136b7f646b396cb17422ec68be84f33`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a88731848c1ea876f483f7a4111728ed24ba7df599cce5e60df0cb2aeba403`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:6c62fad7aa64c94223fa6c327b55684b71e029a63152d183c44330be3327fe6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:5e2dd30c17d2f21f56da6ca00e05aef04512153b20690e45c89e0b517b275f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297328572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72d1a6b3b1871318ebd8c0fd16e79c2bad75fba76c35fc484cb8b9533f12d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71c8b2b7800651b1ebed77c93e9e88181449a81ce4d83668d196953b74930f`  
		Last Modified: Tue, 07 Apr 2026 03:31:14 GMT  
		Size: 110.2 MB (110192712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e990202056cce74a97a1d88af992471957a5ca3246b73c8e843be09fcf51b3`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279757b2e3bf73fe38bd373df54844e8f12e865e560d46c2fb972600fbff380`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d27fadbaedf7924960dc53c887f8ab5fe2cd773a64e3f50c5ba1ef3cb1899b`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 28.1 MB (28074526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:b54e568135f0f8ff148878e05d890d5294bba7c82bf4ecf2fd4af5e60d28a32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d7cc0e91d71baf8abcf9f29fce2de72cbf6704a489563997c366ec576a9fec`

```dockerfile
```

-	Layers:
	-	`sha256:d0790a7ba44e8ae54961ffb4a40a44a692558e0d680b9933e723623eddf955b4`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 24.8 MB (24750608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1185ed4241993de2b3d22f0692b34be58eea1cbd2c4ee7082ea277948e809f61`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d28094b2d31ea8e3ae26e89f2e5e8712bbf6d1296435f0b90146ae0941b45401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285705599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb790354d7fe39725c4875c4b7048ed4ba848ce6e11bd7d1e276c931e9e6b80`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c52e72a98ff18024c49e42ee5a244f148f67c229f893f253bb98739e4601b2`  
		Last Modified: Tue, 07 Apr 2026 03:43:37 GMT  
		Size: 105.6 MB (105605517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47880aad4a35736cef7a2c581e364e499a17cda990ef9faf212e5f8dc5dc498`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776f56cf9e1966633dc9669e8a06f723d88958d885f0bafeca03338fe3f06d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fb55a370964daa8364587fcd75a1c5697db6be6c7a368cc372ca913dd6424`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 27.2 MB (27159980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:021db3c29d874aeaf4a52e6476f55134d6179b1fdc34bb35049b5653866cb55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987c999ccbbafc31ba85d411659003345fae235c66d28d57d3b667e6c996733f`

```dockerfile
```

-	Layers:
	-	`sha256:d479adab56c856db5a5921e5d2a65dbd9864671d45016bb31549949bde04fb26`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 24.8 MB (24772870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f21380ebe03c6ff83ee024b4347dca4cfcab0119ce6e0bcbecfac6c3a04eb04`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:d2e4e3adeb8c04596265b1c47ca324e6d9f356241c82ed651d9fcdfd3d4d04b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:3498c793c85f64a55cc8f05d700dcf94f93bf4d66ad6078896e05caa90cdf018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081946320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340705fdf7e84594d321cbc3a5ddc7801b30516286b0333cb8d6afd9a4cb20f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:58:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71c8b2b7800651b1ebed77c93e9e88181449a81ce4d83668d196953b74930f`  
		Last Modified: Tue, 07 Apr 2026 03:31:14 GMT  
		Size: 110.2 MB (110192712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e990202056cce74a97a1d88af992471957a5ca3246b73c8e843be09fcf51b3`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279757b2e3bf73fe38bd373df54844e8f12e865e560d46c2fb972600fbff380`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d27fadbaedf7924960dc53c887f8ab5fe2cd773a64e3f50c5ba1ef3cb1899b`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 28.1 MB (28074526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d468e65492340372f5a757aaa386b1461ba9890a065702f50f680694f9dd07`  
		Last Modified: Tue, 07 Apr 2026 05:01:26 GMT  
		Size: 784.6 MB (784617748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:7f752636ed1fbce072cb76ca5d40e3a36ba12d0904f3ab28891534a4b2a5b9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60936688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c951f7355b085115499dfdf706f9c2829695a3d391fdd05e75e2b0261b2301`

```dockerfile
```

-	Layers:
	-	`sha256:001d4cda1a401c26de87a620397bc0db0f16f7848df1f02687f298bc62f264d1`  
		Last Modified: Tue, 07 Apr 2026 05:01:09 GMT  
		Size: 60.9 MB (60927336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fde1c67c4c20d82d0f51689a37f86e8461cf653045f464fb7cba9fa8051c84`  
		Last Modified: Tue, 07 Apr 2026 05:01:08 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a677d9d345f1b09ed86dd1b168a5c6387cb24ca35a1740992b10ac90ac0e7069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 MB (984494737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1397af9b711850ae30d67d72aa8cb0b7518ef1fc979d6533a4cb3ddc65f252`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:05:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c52e72a98ff18024c49e42ee5a244f148f67c229f893f253bb98739e4601b2`  
		Last Modified: Tue, 07 Apr 2026 03:43:37 GMT  
		Size: 105.6 MB (105605517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47880aad4a35736cef7a2c581e364e499a17cda990ef9faf212e5f8dc5dc498`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776f56cf9e1966633dc9669e8a06f723d88958d885f0bafeca03338fe3f06d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fb55a370964daa8364587fcd75a1c5697db6be6c7a368cc372ca913dd6424`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 27.2 MB (27159980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb19de17725a4e4df59958e8f258266cfe3b9cd0f7e2e313bece27ac39c98a7e`  
		Last Modified: Tue, 07 Apr 2026 05:08:06 GMT  
		Size: 698.8 MB (698789138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:d349fdaaf5e45caeb9c71f7c0941d9d6e4a9284c8dff1eed7d149ac426dec344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60867289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f6a048b1b0295fda9496a03a3e37613079446c10250a7a11bb2abb4fb6703d`

```dockerfile
```

-	Layers:
	-	`sha256:75a72935f0722f2b1cb2d46fe44a96628293b1ffef7d81de372b41fcb7438010`  
		Last Modified: Tue, 07 Apr 2026 05:07:53 GMT  
		Size: 60.9 MB (60857857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58699756c434346ae0a53510a1936d1cb511dfef56773fc99fd5403c5b28b2bc`  
		Last Modified: Tue, 07 Apr 2026 05:07:50 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:d2e4e3adeb8c04596265b1c47ca324e6d9f356241c82ed651d9fcdfd3d4d04b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:3498c793c85f64a55cc8f05d700dcf94f93bf4d66ad6078896e05caa90cdf018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081946320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3340705fdf7e84594d321cbc3a5ddc7801b30516286b0333cb8d6afd9a4cb20f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:58:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71c8b2b7800651b1ebed77c93e9e88181449a81ce4d83668d196953b74930f`  
		Last Modified: Tue, 07 Apr 2026 03:31:14 GMT  
		Size: 110.2 MB (110192712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e990202056cce74a97a1d88af992471957a5ca3246b73c8e843be09fcf51b3`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279757b2e3bf73fe38bd373df54844e8f12e865e560d46c2fb972600fbff380`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d27fadbaedf7924960dc53c887f8ab5fe2cd773a64e3f50c5ba1ef3cb1899b`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 28.1 MB (28074526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d468e65492340372f5a757aaa386b1461ba9890a065702f50f680694f9dd07`  
		Last Modified: Tue, 07 Apr 2026 05:01:26 GMT  
		Size: 784.6 MB (784617748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7f752636ed1fbce072cb76ca5d40e3a36ba12d0904f3ab28891534a4b2a5b9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60936688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c951f7355b085115499dfdf706f9c2829695a3d391fdd05e75e2b0261b2301`

```dockerfile
```

-	Layers:
	-	`sha256:001d4cda1a401c26de87a620397bc0db0f16f7848df1f02687f298bc62f264d1`  
		Last Modified: Tue, 07 Apr 2026 05:01:09 GMT  
		Size: 60.9 MB (60927336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fde1c67c4c20d82d0f51689a37f86e8461cf653045f464fb7cba9fa8051c84`  
		Last Modified: Tue, 07 Apr 2026 05:01:08 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a677d9d345f1b09ed86dd1b168a5c6387cb24ca35a1740992b10ac90ac0e7069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.5 MB (984494737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1397af9b711850ae30d67d72aa8cb0b7518ef1fc979d6533a4cb3ddc65f252`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:05:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c52e72a98ff18024c49e42ee5a244f148f67c229f893f253bb98739e4601b2`  
		Last Modified: Tue, 07 Apr 2026 03:43:37 GMT  
		Size: 105.6 MB (105605517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47880aad4a35736cef7a2c581e364e499a17cda990ef9faf212e5f8dc5dc498`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776f56cf9e1966633dc9669e8a06f723d88958d885f0bafeca03338fe3f06d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fb55a370964daa8364587fcd75a1c5697db6be6c7a368cc372ca913dd6424`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 27.2 MB (27159980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb19de17725a4e4df59958e8f258266cfe3b9cd0f7e2e313bece27ac39c98a7e`  
		Last Modified: Tue, 07 Apr 2026 05:08:06 GMT  
		Size: 698.8 MB (698789138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d349fdaaf5e45caeb9c71f7c0941d9d6e4a9284c8dff1eed7d149ac426dec344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60867289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f6a048b1b0295fda9496a03a3e37613079446c10250a7a11bb2abb4fb6703d`

```dockerfile
```

-	Layers:
	-	`sha256:75a72935f0722f2b1cb2d46fe44a96628293b1ffef7d81de372b41fcb7438010`  
		Last Modified: Tue, 07 Apr 2026 05:07:53 GMT  
		Size: 60.9 MB (60857857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58699756c434346ae0a53510a1936d1cb511dfef56773fc99fd5403c5b28b2bc`  
		Last Modified: Tue, 07 Apr 2026 05:07:50 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:6c62fad7aa64c94223fa6c327b55684b71e029a63152d183c44330be3327fe6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:5e2dd30c17d2f21f56da6ca00e05aef04512153b20690e45c89e0b517b275f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297328572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72d1a6b3b1871318ebd8c0fd16e79c2bad75fba76c35fc484cb8b9533f12d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71c8b2b7800651b1ebed77c93e9e88181449a81ce4d83668d196953b74930f`  
		Last Modified: Tue, 07 Apr 2026 03:31:14 GMT  
		Size: 110.2 MB (110192712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e990202056cce74a97a1d88af992471957a5ca3246b73c8e843be09fcf51b3`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279757b2e3bf73fe38bd373df54844e8f12e865e560d46c2fb972600fbff380`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d27fadbaedf7924960dc53c887f8ab5fe2cd773a64e3f50c5ba1ef3cb1899b`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 28.1 MB (28074526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b54e568135f0f8ff148878e05d890d5294bba7c82bf4ecf2fd4af5e60d28a32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d7cc0e91d71baf8abcf9f29fce2de72cbf6704a489563997c366ec576a9fec`

```dockerfile
```

-	Layers:
	-	`sha256:d0790a7ba44e8ae54961ffb4a40a44a692558e0d680b9933e723623eddf955b4`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 24.8 MB (24750608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1185ed4241993de2b3d22f0692b34be58eea1cbd2c4ee7082ea277948e809f61`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d28094b2d31ea8e3ae26e89f2e5e8712bbf6d1296435f0b90146ae0941b45401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285705599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb790354d7fe39725c4875c4b7048ed4ba848ce6e11bd7d1e276c931e9e6b80`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c52e72a98ff18024c49e42ee5a244f148f67c229f893f253bb98739e4601b2`  
		Last Modified: Tue, 07 Apr 2026 03:43:37 GMT  
		Size: 105.6 MB (105605517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47880aad4a35736cef7a2c581e364e499a17cda990ef9faf212e5f8dc5dc498`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776f56cf9e1966633dc9669e8a06f723d88958d885f0bafeca03338fe3f06d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fb55a370964daa8364587fcd75a1c5697db6be6c7a368cc372ca913dd6424`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 27.2 MB (27159980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:021db3c29d874aeaf4a52e6476f55134d6179b1fdc34bb35049b5653866cb55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987c999ccbbafc31ba85d411659003345fae235c66d28d57d3b667e6c996733f`

```dockerfile
```

-	Layers:
	-	`sha256:d479adab56c856db5a5921e5d2a65dbd9864671d45016bb31549949bde04fb26`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 24.8 MB (24772870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f21380ebe03c6ff83ee024b4347dca4cfcab0119ce6e0bcbecfac6c3a04eb04`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:6c62fad7aa64c94223fa6c327b55684b71e029a63152d183c44330be3327fe6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:5e2dd30c17d2f21f56da6ca00e05aef04512153b20690e45c89e0b517b275f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297328572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72d1a6b3b1871318ebd8c0fd16e79c2bad75fba76c35fc484cb8b9533f12d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71c8b2b7800651b1ebed77c93e9e88181449a81ce4d83668d196953b74930f`  
		Last Modified: Tue, 07 Apr 2026 03:31:14 GMT  
		Size: 110.2 MB (110192712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e990202056cce74a97a1d88af992471957a5ca3246b73c8e843be09fcf51b3`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279757b2e3bf73fe38bd373df54844e8f12e865e560d46c2fb972600fbff380`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d27fadbaedf7924960dc53c887f8ab5fe2cd773a64e3f50c5ba1ef3cb1899b`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 28.1 MB (28074526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b54e568135f0f8ff148878e05d890d5294bba7c82bf4ecf2fd4af5e60d28a32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d7cc0e91d71baf8abcf9f29fce2de72cbf6704a489563997c366ec576a9fec`

```dockerfile
```

-	Layers:
	-	`sha256:d0790a7ba44e8ae54961ffb4a40a44a692558e0d680b9933e723623eddf955b4`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 24.8 MB (24750608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1185ed4241993de2b3d22f0692b34be58eea1cbd2c4ee7082ea277948e809f61`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d28094b2d31ea8e3ae26e89f2e5e8712bbf6d1296435f0b90146ae0941b45401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285705599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb790354d7fe39725c4875c4b7048ed4ba848ce6e11bd7d1e276c931e9e6b80`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c52e72a98ff18024c49e42ee5a244f148f67c229f893f253bb98739e4601b2`  
		Last Modified: Tue, 07 Apr 2026 03:43:37 GMT  
		Size: 105.6 MB (105605517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47880aad4a35736cef7a2c581e364e499a17cda990ef9faf212e5f8dc5dc498`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776f56cf9e1966633dc9669e8a06f723d88958d885f0bafeca03338fe3f06d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fb55a370964daa8364587fcd75a1c5697db6be6c7a368cc372ca913dd6424`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 27.2 MB (27159980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:021db3c29d874aeaf4a52e6476f55134d6179b1fdc34bb35049b5653866cb55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987c999ccbbafc31ba85d411659003345fae235c66d28d57d3b667e6c996733f`

```dockerfile
```

-	Layers:
	-	`sha256:d479adab56c856db5a5921e5d2a65dbd9864671d45016bb31549949bde04fb26`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 24.8 MB (24772870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f21380ebe03c6ff83ee024b4347dca4cfcab0119ce6e0bcbecfac6c3a04eb04`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:5b77f83a3a50b3777ad50b3d2a97a97fdbae7e3ce359bad5b0964de2cb176049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:a32c9f3fcad0ab56e8f3bc92e5a25aff4439a0183d1e59c4781c11050d4ea432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158679332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d4f90e1c47c06896d89a1cdf97f43000560814205cb9517f1c4fda3cdb773e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:8f0efb67ea2edd66de78221a30e607f3f8d1c338a88c7a674c9e9b7707ff924c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18503158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c67a49064f25ecfaf222bcaa307a5092662e58314140207de5b6b7ed9183f18`

```dockerfile
```

-	Layers:
	-	`sha256:ff7e426cf73653a4e56ae783c79b048160e2112e8b26356771add17146207731`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 18.5 MB (18488549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a1d769ed1985fea97dbb7fd3d1b64aa25dc9072b313b39b07af0628d92d1faf`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93815e796e1040bbdc6ff4ffea61189953ec155e2f71f9eda5c583d0d861fb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152558107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a40a844595baaa50f4f3684d35af6296ca04faa282c9c81ba0aacda90c3c74c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6381b1a882f2a22df58957277d01c30cede21d11f7f1b79529a546ed88c89083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff06bc1d858b3d8b4d48c6fedea1768f5a4859e402aa2587039d69043f4b626`

```dockerfile
```

-	Layers:
	-	`sha256:5825211cc812652427cca4a9a7955e1f75f6bf2e85fc8c3b8c380644e016f0f5`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 18.5 MB (18462560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e75081f1b7fb421b0a6c9049c5fcfa971a0a11c272cd348e1c28d823cb0b383`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:5b77f83a3a50b3777ad50b3d2a97a97fdbae7e3ce359bad5b0964de2cb176049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:a32c9f3fcad0ab56e8f3bc92e5a25aff4439a0183d1e59c4781c11050d4ea432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158679332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d4f90e1c47c06896d89a1cdf97f43000560814205cb9517f1c4fda3cdb773e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8f0efb67ea2edd66de78221a30e607f3f8d1c338a88c7a674c9e9b7707ff924c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18503158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c67a49064f25ecfaf222bcaa307a5092662e58314140207de5b6b7ed9183f18`

```dockerfile
```

-	Layers:
	-	`sha256:ff7e426cf73653a4e56ae783c79b048160e2112e8b26356771add17146207731`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 18.5 MB (18488549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a1d769ed1985fea97dbb7fd3d1b64aa25dc9072b313b39b07af0628d92d1faf`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93815e796e1040bbdc6ff4ffea61189953ec155e2f71f9eda5c583d0d861fb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152558107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a40a844595baaa50f4f3684d35af6296ca04faa282c9c81ba0aacda90c3c74c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6381b1a882f2a22df58957277d01c30cede21d11f7f1b79529a546ed88c89083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff06bc1d858b3d8b4d48c6fedea1768f5a4859e402aa2587039d69043f4b626`

```dockerfile
```

-	Layers:
	-	`sha256:5825211cc812652427cca4a9a7955e1f75f6bf2e85fc8c3b8c380644e016f0f5`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 18.5 MB (18462560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e75081f1b7fb421b0a6c9049c5fcfa971a0a11c272cd348e1c28d823cb0b383`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:d1eca5bd28aef56ea7370e8d35796a0804ed297f8f245283817c85475e2c73e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:db27fc6125927590ee131d5f4bffbffca9dea368424684f707103afad34614c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296283805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba05340ef60bdf2b4273658986b4c71b7ca689bde04f1182f1e3d04629ef36b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8dd6647a3c1e7d18001a45a8789638361caf8dfef0f307b190a1384f0a2413`  
		Last Modified: Tue, 07 Apr 2026 03:31:11 GMT  
		Size: 110.2 MB (110188982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6af0b3531a3918b50c613a65fd716cbff3bb7b3243c89bb4312d5e60cdf14e`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 405.7 KB (405659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf926922fb8b2b3271f1be2185badc4d52812efb69c4186e57f4bb5b97e60cb`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e9897748f310d88fd17993769228e2f42207223ca0c90914f25c4d40da3c7`  
		Last Modified: Tue, 07 Apr 2026 03:31:09 GMT  
		Size: 28.0 MB (28010350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:bbfb05f0c551c51da32aa0f57e6d43f9847587d2479e338e58ae37c231e20929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07e0628f14767a277bce48ac54ab97d98056d618026bd9d82d6d6fd6caa43ea`

```dockerfile
```

-	Layers:
	-	`sha256:6f2d7574bb1fb6b1621a352e11874c092e186023e5d2523fe4c6f3975845a7c6`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 24.6 MB (24571750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a641ee42aa231b2615a8ac734ab358d1e6fb5f00fb0a707adc56abebc2384ae4`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:637d8247407ec5a2efb5afdfed8e56c31cc3227f23dc6e6b92d7d409566546c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284739621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4b7e222c910549863d8b92dddc2274f61d2beef948949587de641333bf328e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161909dfa0ad7f5997c40a973a116ed80646d74843f0a597dc20ed3e125a8e7`  
		Last Modified: Tue, 07 Apr 2026 03:43:19 GMT  
		Size: 105.6 MB (105602757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acde01ab9a2e4a57c5d4f65c24cb93972ea90a24913b0a6fe47933637d93d94`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 405.7 KB (405655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e592252c9ae49ff56f1b4f86b18208ba2ccc2fd338f6501a7ce53ed3d869dd`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 2.5 KB (2519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b8c78e8323633d8f1b0a4cbde5ac8aca13922c7dc16e99313d98fb1d9169c`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 27.1 MB (27103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:3119a143d3c64ab3b53d92ce1e6251635f38bb2cc3692a6f7e5a83e0333e4ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b76c6bbed17c5df5c2ef77a2c1f8cea7dc86ed393c664e4fda16b4eecd189`

```dockerfile
```

-	Layers:
	-	`sha256:5805811070e70ffaf29a1282e772de909cc339923d7675d64b3c7466d666a2d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 24.6 MB (24594011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225da648b529e7e6431b0259d1bf4d5069c749064d2377239124819c4a4cb058`  
		Last Modified: Tue, 07 Apr 2026 03:43:15 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:fb8469ba130be60dde6561fb194a1bf43063a2a492ee01db9866d851ece0cad6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:227685994dd9af94297314531a6eec57c2beae45783aeb0513f87347e9a7431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310754513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4f878140c5dcf5e025d008095ddb1a17be09d579890f5212fa70cc0dda4608`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ab68a8765d2a0bb4fbd79e885d30475c96d517d9f388fd717df7df6a58cb6`  
		Last Modified: Tue, 07 Apr 2026 03:31:33 GMT  
		Size: 110.2 MB (110193398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61184d2a7dd89b65d8ea9c22edbcc83d7777c1852fb9503e9f765c0904cebabb`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 371.8 KB (371819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78675698bbbb43c8f40b4c835d17cb575878395b5d95384101aa6d449081b144`  
		Last Modified: Tue, 07 Apr 2026 03:31:30 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed39434b1f48964c8be41d16116e0f3d41c2cf9522aa1be7797100f8d83d55`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 27.8 MB (27840327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:b28f4e5eadbd9958b2fb725dee34a934ac997947c20620926b41959a10f786d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25639305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad5f183537ff8ae32b55058805b53b9ac5f22876ab814f7c1c207015fbc5242`

```dockerfile
```

-	Layers:
	-	`sha256:a784a44876f3a4e6ebfbddf3da7c5204a8ebfc98e08c14e94f99e6763c10b674`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 25.6 MB (25622940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f955b6a175e9f1b32f75f062020cfa51940be83f01a0712bdfc15f620707106b`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2290f9ce4119ad35aa8d9410d24fb024c55a3d643f9fec182b38a1a6039b60a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298748151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae0e79d66de4591e06de411d978d41d9bd7555012e5256162e0cc730513c1d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc58942ba23c0013ff4f043dc403940a128b600496526dd7a6c1ff107a363a28`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 105.6 MB (105606215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1a89472c625e25828173ec6e90ca03edabd608f21ec8d06eea1f387c4fc9`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 371.8 KB (371817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f32cbbfee1b751cf080817885147f380443df091a1789a6f76b47b867472e3`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e52d4e6ad307b275501259d4ff705bb40b6264b227536a5d46c28979dc6e86`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 26.9 MB (26929634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:6ad5a91a7d31e93d70e10ce0b7ffdfb99d4622bb211c8e69f3c9b83b1c810db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25661901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922b5409df6b325d49757e417f32c7297c3ea8a5245fee0f85fd94e87ebd2a99`

```dockerfile
```

-	Layers:
	-	`sha256:00dd01ad060c7d2429e809f7a912ef817c5a6773359db44fa38f821f50096b8c`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 25.6 MB (25645399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f7c607c8a6b27cf5fb23bfe6beba2f52ebf3a10cd83b22c661753718b5534d`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:f525a863a90c9bea6ec08e2b48fe8c68c22c5eca04253817e96866a956b9e9c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:6ade9cb543892dc2005c85fc1b4a74210da8cbc633ba29ea0e7a363486faa8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094996610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3883164fd22f97ba3567f3aca9b079ed2c261f9116fce02bb4cb38c402b291`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:59:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ab68a8765d2a0bb4fbd79e885d30475c96d517d9f388fd717df7df6a58cb6`  
		Last Modified: Tue, 07 Apr 2026 03:31:33 GMT  
		Size: 110.2 MB (110193398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61184d2a7dd89b65d8ea9c22edbcc83d7777c1852fb9503e9f765c0904cebabb`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 371.8 KB (371819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78675698bbbb43c8f40b4c835d17cb575878395b5d95384101aa6d449081b144`  
		Last Modified: Tue, 07 Apr 2026 03:31:30 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed39434b1f48964c8be41d16116e0f3d41c2cf9522aa1be7797100f8d83d55`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 27.8 MB (27840327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d771503b03b06f0248677850cab72eb9be0c6d88887cf877358d7401735bfe71`  
		Last Modified: Tue, 07 Apr 2026 05:02:33 GMT  
		Size: 784.2 MB (784242097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:8f1a997fa44bc12440d608de9b9632e1f26040123ce46fd5a9ff948fcc198841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61807644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f43ac78852ee853c63f0082a7dea027a57c1d10ae9e77effe1544a450396e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f598ca81494bfb9404de345610bb5028b947fb79b08928c4970aa0fefb718fd`  
		Last Modified: Tue, 07 Apr 2026 05:02:21 GMT  
		Size: 61.8 MB (61798283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3742ccaf8533ab5b1bf1cd0ca8c83ee95bbc8e7625c5386d8452e8d7309bf485`  
		Last Modified: Tue, 07 Apr 2026 05:02:18 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:daca987a1a2f76631abce62ce4be783354562949a8a97c4f4ef7b2563dc838ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.1 MB (997126498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c3341541c83a08ec2a6c930ae0df00e6b4d01ca97e8c7f458607f587abbfb7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:05:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc58942ba23c0013ff4f043dc403940a128b600496526dd7a6c1ff107a363a28`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 105.6 MB (105606215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1a89472c625e25828173ec6e90ca03edabd608f21ec8d06eea1f387c4fc9`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 371.8 KB (371817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f32cbbfee1b751cf080817885147f380443df091a1789a6f76b47b867472e3`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e52d4e6ad307b275501259d4ff705bb40b6264b227536a5d46c28979dc6e86`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 26.9 MB (26929634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8668c2db6917b395bf1929e634c15c0002acf8e95b856ad02795bddb2905389e`  
		Last Modified: Tue, 07 Apr 2026 05:09:01 GMT  
		Size: 698.4 MB (698378347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:307ddec5f3bd8bb84a01c0734dc1f8465f934a3c922a401018a57acc8049b172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61738442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f880383f6626972e0645b88ee16804e21e6f7f22144cbb80cc60c75b53755fcd`

```dockerfile
```

-	Layers:
	-	`sha256:18241b55135ee1be315b190a49552380e0ff95862dc021c33c9f3f773fc3d8ff`  
		Last Modified: Tue, 07 Apr 2026 05:08:49 GMT  
		Size: 61.7 MB (61729001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9c6324a26829a8542921331ed09d41738ab6a83f08321f4154e5f8c500dadf`  
		Last Modified: Tue, 07 Apr 2026 05:08:47 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:f525a863a90c9bea6ec08e2b48fe8c68c22c5eca04253817e96866a956b9e9c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:6ade9cb543892dc2005c85fc1b4a74210da8cbc633ba29ea0e7a363486faa8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094996610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3883164fd22f97ba3567f3aca9b079ed2c261f9116fce02bb4cb38c402b291`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:59:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ab68a8765d2a0bb4fbd79e885d30475c96d517d9f388fd717df7df6a58cb6`  
		Last Modified: Tue, 07 Apr 2026 03:31:33 GMT  
		Size: 110.2 MB (110193398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61184d2a7dd89b65d8ea9c22edbcc83d7777c1852fb9503e9f765c0904cebabb`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 371.8 KB (371819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78675698bbbb43c8f40b4c835d17cb575878395b5d95384101aa6d449081b144`  
		Last Modified: Tue, 07 Apr 2026 03:31:30 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed39434b1f48964c8be41d16116e0f3d41c2cf9522aa1be7797100f8d83d55`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 27.8 MB (27840327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d771503b03b06f0248677850cab72eb9be0c6d88887cf877358d7401735bfe71`  
		Last Modified: Tue, 07 Apr 2026 05:02:33 GMT  
		Size: 784.2 MB (784242097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:8f1a997fa44bc12440d608de9b9632e1f26040123ce46fd5a9ff948fcc198841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61807644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f43ac78852ee853c63f0082a7dea027a57c1d10ae9e77effe1544a450396e37`

```dockerfile
```

-	Layers:
	-	`sha256:1f598ca81494bfb9404de345610bb5028b947fb79b08928c4970aa0fefb718fd`  
		Last Modified: Tue, 07 Apr 2026 05:02:21 GMT  
		Size: 61.8 MB (61798283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3742ccaf8533ab5b1bf1cd0ca8c83ee95bbc8e7625c5386d8452e8d7309bf485`  
		Last Modified: Tue, 07 Apr 2026 05:02:18 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:daca987a1a2f76631abce62ce4be783354562949a8a97c4f4ef7b2563dc838ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.1 MB (997126498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c3341541c83a08ec2a6c930ae0df00e6b4d01ca97e8c7f458607f587abbfb7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:05:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc58942ba23c0013ff4f043dc403940a128b600496526dd7a6c1ff107a363a28`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 105.6 MB (105606215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1a89472c625e25828173ec6e90ca03edabd608f21ec8d06eea1f387c4fc9`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 371.8 KB (371817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f32cbbfee1b751cf080817885147f380443df091a1789a6f76b47b867472e3`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e52d4e6ad307b275501259d4ff705bb40b6264b227536a5d46c28979dc6e86`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 26.9 MB (26929634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8668c2db6917b395bf1929e634c15c0002acf8e95b856ad02795bddb2905389e`  
		Last Modified: Tue, 07 Apr 2026 05:09:01 GMT  
		Size: 698.4 MB (698378347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:307ddec5f3bd8bb84a01c0734dc1f8465f934a3c922a401018a57acc8049b172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61738442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f880383f6626972e0645b88ee16804e21e6f7f22144cbb80cc60c75b53755fcd`

```dockerfile
```

-	Layers:
	-	`sha256:18241b55135ee1be315b190a49552380e0ff95862dc021c33c9f3f773fc3d8ff`  
		Last Modified: Tue, 07 Apr 2026 05:08:49 GMT  
		Size: 61.7 MB (61729001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9c6324a26829a8542921331ed09d41738ab6a83f08321f4154e5f8c500dadf`  
		Last Modified: Tue, 07 Apr 2026 05:08:47 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:fb8469ba130be60dde6561fb194a1bf43063a2a492ee01db9866d851ece0cad6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:227685994dd9af94297314531a6eec57c2beae45783aeb0513f87347e9a7431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310754513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4f878140c5dcf5e025d008095ddb1a17be09d579890f5212fa70cc0dda4608`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ab68a8765d2a0bb4fbd79e885d30475c96d517d9f388fd717df7df6a58cb6`  
		Last Modified: Tue, 07 Apr 2026 03:31:33 GMT  
		Size: 110.2 MB (110193398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61184d2a7dd89b65d8ea9c22edbcc83d7777c1852fb9503e9f765c0904cebabb`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 371.8 KB (371819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78675698bbbb43c8f40b4c835d17cb575878395b5d95384101aa6d449081b144`  
		Last Modified: Tue, 07 Apr 2026 03:31:30 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed39434b1f48964c8be41d16116e0f3d41c2cf9522aa1be7797100f8d83d55`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 27.8 MB (27840327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b28f4e5eadbd9958b2fb725dee34a934ac997947c20620926b41959a10f786d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25639305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad5f183537ff8ae32b55058805b53b9ac5f22876ab814f7c1c207015fbc5242`

```dockerfile
```

-	Layers:
	-	`sha256:a784a44876f3a4e6ebfbddf3da7c5204a8ebfc98e08c14e94f99e6763c10b674`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 25.6 MB (25622940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f955b6a175e9f1b32f75f062020cfa51940be83f01a0712bdfc15f620707106b`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2290f9ce4119ad35aa8d9410d24fb024c55a3d643f9fec182b38a1a6039b60a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298748151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae0e79d66de4591e06de411d978d41d9bd7555012e5256162e0cc730513c1d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc58942ba23c0013ff4f043dc403940a128b600496526dd7a6c1ff107a363a28`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 105.6 MB (105606215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1a89472c625e25828173ec6e90ca03edabd608f21ec8d06eea1f387c4fc9`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 371.8 KB (371817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f32cbbfee1b751cf080817885147f380443df091a1789a6f76b47b867472e3`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e52d4e6ad307b275501259d4ff705bb40b6264b227536a5d46c28979dc6e86`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 26.9 MB (26929634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6ad5a91a7d31e93d70e10ce0b7ffdfb99d4622bb211c8e69f3c9b83b1c810db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25661901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922b5409df6b325d49757e417f32c7297c3ea8a5245fee0f85fd94e87ebd2a99`

```dockerfile
```

-	Layers:
	-	`sha256:00dd01ad060c7d2429e809f7a912ef817c5a6773359db44fa38f821f50096b8c`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 25.6 MB (25645399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f7c607c8a6b27cf5fb23bfe6beba2f52ebf3a10cd83b22c661753718b5534d`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:fb8469ba130be60dde6561fb194a1bf43063a2a492ee01db9866d851ece0cad6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:227685994dd9af94297314531a6eec57c2beae45783aeb0513f87347e9a7431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310754513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4f878140c5dcf5e025d008095ddb1a17be09d579890f5212fa70cc0dda4608`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ab68a8765d2a0bb4fbd79e885d30475c96d517d9f388fd717df7df6a58cb6`  
		Last Modified: Tue, 07 Apr 2026 03:31:33 GMT  
		Size: 110.2 MB (110193398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61184d2a7dd89b65d8ea9c22edbcc83d7777c1852fb9503e9f765c0904cebabb`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 371.8 KB (371819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78675698bbbb43c8f40b4c835d17cb575878395b5d95384101aa6d449081b144`  
		Last Modified: Tue, 07 Apr 2026 03:31:30 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed39434b1f48964c8be41d16116e0f3d41c2cf9522aa1be7797100f8d83d55`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 27.8 MB (27840327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b28f4e5eadbd9958b2fb725dee34a934ac997947c20620926b41959a10f786d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25639305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad5f183537ff8ae32b55058805b53b9ac5f22876ab814f7c1c207015fbc5242`

```dockerfile
```

-	Layers:
	-	`sha256:a784a44876f3a4e6ebfbddf3da7c5204a8ebfc98e08c14e94f99e6763c10b674`  
		Last Modified: Tue, 07 Apr 2026 03:31:31 GMT  
		Size: 25.6 MB (25622940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f955b6a175e9f1b32f75f062020cfa51940be83f01a0712bdfc15f620707106b`  
		Last Modified: Tue, 07 Apr 2026 03:31:29 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2290f9ce4119ad35aa8d9410d24fb024c55a3d643f9fec182b38a1a6039b60a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298748151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae0e79d66de4591e06de411d978d41d9bd7555012e5256162e0cc730513c1d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc58942ba23c0013ff4f043dc403940a128b600496526dd7a6c1ff107a363a28`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 105.6 MB (105606215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1a89472c625e25828173ec6e90ca03edabd608f21ec8d06eea1f387c4fc9`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 371.8 KB (371817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f32cbbfee1b751cf080817885147f380443df091a1789a6f76b47b867472e3`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e52d4e6ad307b275501259d4ff705bb40b6264b227536a5d46c28979dc6e86`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 26.9 MB (26929634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6ad5a91a7d31e93d70e10ce0b7ffdfb99d4622bb211c8e69f3c9b83b1c810db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25661901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922b5409df6b325d49757e417f32c7297c3ea8a5245fee0f85fd94e87ebd2a99`

```dockerfile
```

-	Layers:
	-	`sha256:00dd01ad060c7d2429e809f7a912ef817c5a6773359db44fa38f821f50096b8c`  
		Last Modified: Tue, 07 Apr 2026 03:43:33 GMT  
		Size: 25.6 MB (25645399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f7c607c8a6b27cf5fb23bfe6beba2f52ebf3a10cd83b22c661753718b5534d`  
		Last Modified: Tue, 07 Apr 2026 03:43:32 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:22c43c0ae043ef89c72f6f3228924221f6cd356e08c196fa14264abda6a49137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f3c6f5c0b3b2d6aef9b44d6c4334847dcb014aa578b05012476220a5bca0def2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172346463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1d6dd5376df1f7b6389f6b351972d34efc4a74efbb3de675b21dfebd846a65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1b96ecb8416ed40d535d13a6eebe2dee3176928cd83be7c8e726ee0d6f912d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19431994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db31f2f92304481c917c1cc4669c2d3141ff051858ad5b3f3ad671475dacbd9c`

```dockerfile
```

-	Layers:
	-	`sha256:38d8b4a091c49852cccc107d94726f979393da8891bb832abf819ce795a917e3`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 19.4 MB (19417372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20512c1e7bd56f1a4f6342e576938573513f237f45904fc85ec4c06943f0ffca`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2d381eddfb4f845059f26be1f39ff84a8efda8a7ffd1e6f8ff56984eeada6af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165837981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa54c30092cbba01cad3de9b74a2e50b9054e6b8fb6ad1c00a26ed1022dcfdd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ba5eff58741065d750dd1412e6dc1a5340831452f7bfeb84929235d77114ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19406327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d14d57199743b390b3db2691756e04d3b7a2a22bbefceabce203abe2eae7d0`

```dockerfile
```

-	Layers:
	-	`sha256:182afa8fa2196e632f5e179bee4ea8b72c9d44ccbdb7f40c9e3bb9427e1427a3`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 19.4 MB (19391581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19de5763163292cba089dd297d9bdf02c1b42b41bc6ac90511347a58e564b8c`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:22c43c0ae043ef89c72f6f3228924221f6cd356e08c196fa14264abda6a49137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:f3c6f5c0b3b2d6aef9b44d6c4334847dcb014aa578b05012476220a5bca0def2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172346463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1d6dd5376df1f7b6389f6b351972d34efc4a74efbb3de675b21dfebd846a65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1b96ecb8416ed40d535d13a6eebe2dee3176928cd83be7c8e726ee0d6f912d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19431994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db31f2f92304481c917c1cc4669c2d3141ff051858ad5b3f3ad671475dacbd9c`

```dockerfile
```

-	Layers:
	-	`sha256:38d8b4a091c49852cccc107d94726f979393da8891bb832abf819ce795a917e3`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 19.4 MB (19417372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20512c1e7bd56f1a4f6342e576938573513f237f45904fc85ec4c06943f0ffca`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2d381eddfb4f845059f26be1f39ff84a8efda8a7ffd1e6f8ff56984eeada6af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165837981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa54c30092cbba01cad3de9b74a2e50b9054e6b8fb6ad1c00a26ed1022dcfdd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ba5eff58741065d750dd1412e6dc1a5340831452f7bfeb84929235d77114ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19406327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d14d57199743b390b3db2691756e04d3b7a2a22bbefceabce203abe2eae7d0`

```dockerfile
```

-	Layers:
	-	`sha256:182afa8fa2196e632f5e179bee4ea8b72c9d44ccbdb7f40c9e3bb9427e1427a3`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 19.4 MB (19391581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19de5763163292cba089dd297d9bdf02c1b42b41bc6ac90511347a58e564b8c`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json
