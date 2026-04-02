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
$ docker pull ros@sha256:86808dfea395039494b4ce75d666c10264c353435b19fa8aecf74014a4500dd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:3f3434e8c66b35b4362d43b3c68d4debb705121fc5f16e850b6174f3c304be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297737941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b861d78ba166e07b81f0322c6e47e9a5a15c07400fb36c636a290ede57179`
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
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38077e6cfcbd5baf66472415e8a5d780f3de0dafa51d29468a03ecf6f9f8135f`  
		Last Modified: Tue, 17 Mar 2026 03:22:34 GMT  
		Size: 110.2 MB (110185787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449b29ed7335849798c88a6d5e97ab5f026c70338148cae7dbd88769de9d7ac9`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 397.5 KB (397528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf5de7d8b8ef94434270e8f7f6907642bd8ff1a706fe5da83278f624ddcc679`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615ef4778d0e24a85c04be1043b9f2a4efcb7435745fb881f91c76c43230449`  
		Last Modified: Tue, 17 Mar 2026 03:22:32 GMT  
		Size: 28.0 MB (28010658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:bf3566f1f09c8118d736c936f8d9a1441accd489d516c4c0cc4ce205565840e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54591db849ffc7e9320f0f8b07f6aff008c44e2800052d8b4421c0fb50eca387`

```dockerfile
```

-	Layers:
	-	`sha256:4b44b6d9082678531c67b5b4669eb393bb2bde2e284208bf385d1745b965f939`  
		Last Modified: Tue, 17 Mar 2026 03:22:31 GMT  
		Size: 24.6 MB (24571546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ee0f1caabf1f9ddb69204af7f718f229e0be39a1a7af06bc7ed3ca02613880`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:39e0457ec2d2b4a983c3fbc10989608149c95801cd935d78b47acf315b092689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286253348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353be99d01e2ddf62f150321868a918f3e04cc033646c6096b9642752fce4c6f`
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
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b4a8ad856ea6339c44417d49ca205c68a95d17f01148a70b8e3f039f3e946`  
		Last Modified: Tue, 17 Mar 2026 03:25:12 GMT  
		Size: 105.6 MB (105598022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc6c0a18c005b79ece467126eef3247c61cb22d0a0033c8bbad8e7cd9e6d0f`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 397.5 KB (397525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9715a303f4f20401efab555ff525c6d6e5512fcf959ba0fef1577655a158`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73015f6cee846794d7d549c4f42139f5b316b765d8d90d686ff890466a6550c6`  
		Last Modified: Tue, 17 Mar 2026 03:25:10 GMT  
		Size: 27.1 MB (27103932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:1324a34d5164c61970d483eccc2194346ac044db00db0600f1517a13d155e78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6eef6b99bcd6aa01e5cf0fadd1f84f804417a2aa22cd3054b2c8722a340f74b`

```dockerfile
```

-	Layers:
	-	`sha256:12b8c77b02fb73641998a275cf6ac00bf2dbba608dcd95044d60b0559351145c`  
		Last Modified: Tue, 17 Mar 2026 03:25:09 GMT  
		Size: 24.6 MB (24593807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cf20a84f6f792840ed0856e3d11d4be39be3cb96b5ce98fcf507e953c59967`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:1ad47dc6fd722e08c5268f95796b9e9478491f831c33447751cadc058a3453c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:54d640ad3692f96a975b86f6e5420161b22da938b9dc95de384c477725dab7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082043008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d9827f6eae5901e23e8bfe702cc8694f7979ff64b77994628d3e2306b4dcd6`
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
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:16:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38077e6cfcbd5baf66472415e8a5d780f3de0dafa51d29468a03ecf6f9f8135f`  
		Last Modified: Tue, 17 Mar 2026 03:22:34 GMT  
		Size: 110.2 MB (110185787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449b29ed7335849798c88a6d5e97ab5f026c70338148cae7dbd88769de9d7ac9`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 397.5 KB (397528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf5de7d8b8ef94434270e8f7f6907642bd8ff1a706fe5da83278f624ddcc679`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615ef4778d0e24a85c04be1043b9f2a4efcb7435745fb881f91c76c43230449`  
		Last Modified: Tue, 17 Mar 2026 03:22:32 GMT  
		Size: 28.0 MB (28010658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5299b46a39e7b4ab4ed2e084669a311ad188e3fdb3968fb53ee5e074b64bf0ff`  
		Last Modified: Tue, 17 Mar 2026 04:20:00 GMT  
		Size: 784.3 MB (784305067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:020b8a7fc63cc04d5bb9064a2b42916472f7fca79c026c206f928b9e67af45b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60737111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93073a2eb9d488755717f088fa95f283d09e46c2ce87b070d5d047f39cc24e0c`

```dockerfile
```

-	Layers:
	-	`sha256:5fb64c9fe5264ca00e3ab89dc1959a13ac0fe67bd74622a0715ed27fcf7336f2`  
		Last Modified: Tue, 17 Mar 2026 04:19:48 GMT  
		Size: 60.7 MB (60727772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98e1791b9d513bd6bd97e8d8891300aafb511385f0475d5ba635f61c3a12118`  
		Last Modified: Tue, 17 Mar 2026 04:19:45 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cde737f692ba72693f4f5853a886c1d4e5d44a25d3379d82d35984ae0b0be87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.7 MB (984708218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825936dbcff8e6cf391ae63acf18f3f09a0b512b53abc0464b03d8eaa6432703`
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
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:15:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b4a8ad856ea6339c44417d49ca205c68a95d17f01148a70b8e3f039f3e946`  
		Last Modified: Tue, 17 Mar 2026 03:25:12 GMT  
		Size: 105.6 MB (105598022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc6c0a18c005b79ece467126eef3247c61cb22d0a0033c8bbad8e7cd9e6d0f`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 397.5 KB (397525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9715a303f4f20401efab555ff525c6d6e5512fcf959ba0fef1577655a158`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73015f6cee846794d7d549c4f42139f5b316b765d8d90d686ff890466a6550c6`  
		Last Modified: Tue, 17 Mar 2026 03:25:10 GMT  
		Size: 27.1 MB (27103932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312dbd512c95ff5845350c2ebb0ea02142abde88f5735ff1f1404ace81bdee14`  
		Last Modified: Tue, 17 Mar 2026 04:18:00 GMT  
		Size: 698.5 MB (698454870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:a3513a767ae00e18b2901020cca6227ffe591996b8d0ebbf8f7856b450054dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60667699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fa5c404a5a1de50925cd89f20f1de8ae748c608e1a4f148425b5c65b04aac`

```dockerfile
```

-	Layers:
	-	`sha256:e41b2e555c0ace0eccba9b13d88f60f0dd47291abd4e573a24fe13f5dce538d9`  
		Last Modified: Tue, 17 Mar 2026 04:17:48 GMT  
		Size: 60.7 MB (60658280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3d8b07409863bffdb1ec3a3c518386e0ca58a15b74ae50375884bfd5de61d5`  
		Last Modified: Tue, 17 Mar 2026 04:17:46 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:1ad47dc6fd722e08c5268f95796b9e9478491f831c33447751cadc058a3453c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:54d640ad3692f96a975b86f6e5420161b22da938b9dc95de384c477725dab7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082043008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d9827f6eae5901e23e8bfe702cc8694f7979ff64b77994628d3e2306b4dcd6`
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
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:16:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38077e6cfcbd5baf66472415e8a5d780f3de0dafa51d29468a03ecf6f9f8135f`  
		Last Modified: Tue, 17 Mar 2026 03:22:34 GMT  
		Size: 110.2 MB (110185787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449b29ed7335849798c88a6d5e97ab5f026c70338148cae7dbd88769de9d7ac9`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 397.5 KB (397528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf5de7d8b8ef94434270e8f7f6907642bd8ff1a706fe5da83278f624ddcc679`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615ef4778d0e24a85c04be1043b9f2a4efcb7435745fb881f91c76c43230449`  
		Last Modified: Tue, 17 Mar 2026 03:22:32 GMT  
		Size: 28.0 MB (28010658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5299b46a39e7b4ab4ed2e084669a311ad188e3fdb3968fb53ee5e074b64bf0ff`  
		Last Modified: Tue, 17 Mar 2026 04:20:00 GMT  
		Size: 784.3 MB (784305067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:020b8a7fc63cc04d5bb9064a2b42916472f7fca79c026c206f928b9e67af45b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60737111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93073a2eb9d488755717f088fa95f283d09e46c2ce87b070d5d047f39cc24e0c`

```dockerfile
```

-	Layers:
	-	`sha256:5fb64c9fe5264ca00e3ab89dc1959a13ac0fe67bd74622a0715ed27fcf7336f2`  
		Last Modified: Tue, 17 Mar 2026 04:19:48 GMT  
		Size: 60.7 MB (60727772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98e1791b9d513bd6bd97e8d8891300aafb511385f0475d5ba635f61c3a12118`  
		Last Modified: Tue, 17 Mar 2026 04:19:45 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cde737f692ba72693f4f5853a886c1d4e5d44a25d3379d82d35984ae0b0be87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.7 MB (984708218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825936dbcff8e6cf391ae63acf18f3f09a0b512b53abc0464b03d8eaa6432703`
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
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:15:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b4a8ad856ea6339c44417d49ca205c68a95d17f01148a70b8e3f039f3e946`  
		Last Modified: Tue, 17 Mar 2026 03:25:12 GMT  
		Size: 105.6 MB (105598022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc6c0a18c005b79ece467126eef3247c61cb22d0a0033c8bbad8e7cd9e6d0f`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 397.5 KB (397525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9715a303f4f20401efab555ff525c6d6e5512fcf959ba0fef1577655a158`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73015f6cee846794d7d549c4f42139f5b316b765d8d90d686ff890466a6550c6`  
		Last Modified: Tue, 17 Mar 2026 03:25:10 GMT  
		Size: 27.1 MB (27103932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312dbd512c95ff5845350c2ebb0ea02142abde88f5735ff1f1404ace81bdee14`  
		Last Modified: Tue, 17 Mar 2026 04:18:00 GMT  
		Size: 698.5 MB (698454870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a3513a767ae00e18b2901020cca6227ffe591996b8d0ebbf8f7856b450054dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60667699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fa5c404a5a1de50925cd89f20f1de8ae748c608e1a4f148425b5c65b04aac`

```dockerfile
```

-	Layers:
	-	`sha256:e41b2e555c0ace0eccba9b13d88f60f0dd47291abd4e573a24fe13f5dce538d9`  
		Last Modified: Tue, 17 Mar 2026 04:17:48 GMT  
		Size: 60.7 MB (60658280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3d8b07409863bffdb1ec3a3c518386e0ca58a15b74ae50375884bfd5de61d5`  
		Last Modified: Tue, 17 Mar 2026 04:17:46 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:86808dfea395039494b4ce75d666c10264c353435b19fa8aecf74014a4500dd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:3f3434e8c66b35b4362d43b3c68d4debb705121fc5f16e850b6174f3c304be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297737941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b861d78ba166e07b81f0322c6e47e9a5a15c07400fb36c636a290ede57179`
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
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38077e6cfcbd5baf66472415e8a5d780f3de0dafa51d29468a03ecf6f9f8135f`  
		Last Modified: Tue, 17 Mar 2026 03:22:34 GMT  
		Size: 110.2 MB (110185787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449b29ed7335849798c88a6d5e97ab5f026c70338148cae7dbd88769de9d7ac9`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 397.5 KB (397528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf5de7d8b8ef94434270e8f7f6907642bd8ff1a706fe5da83278f624ddcc679`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615ef4778d0e24a85c04be1043b9f2a4efcb7435745fb881f91c76c43230449`  
		Last Modified: Tue, 17 Mar 2026 03:22:32 GMT  
		Size: 28.0 MB (28010658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:bf3566f1f09c8118d736c936f8d9a1441accd489d516c4c0cc4ce205565840e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54591db849ffc7e9320f0f8b07f6aff008c44e2800052d8b4421c0fb50eca387`

```dockerfile
```

-	Layers:
	-	`sha256:4b44b6d9082678531c67b5b4669eb393bb2bde2e284208bf385d1745b965f939`  
		Last Modified: Tue, 17 Mar 2026 03:22:31 GMT  
		Size: 24.6 MB (24571546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ee0f1caabf1f9ddb69204af7f718f229e0be39a1a7af06bc7ed3ca02613880`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:39e0457ec2d2b4a983c3fbc10989608149c95801cd935d78b47acf315b092689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286253348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353be99d01e2ddf62f150321868a918f3e04cc033646c6096b9642752fce4c6f`
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
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b4a8ad856ea6339c44417d49ca205c68a95d17f01148a70b8e3f039f3e946`  
		Last Modified: Tue, 17 Mar 2026 03:25:12 GMT  
		Size: 105.6 MB (105598022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc6c0a18c005b79ece467126eef3247c61cb22d0a0033c8bbad8e7cd9e6d0f`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 397.5 KB (397525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9715a303f4f20401efab555ff525c6d6e5512fcf959ba0fef1577655a158`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73015f6cee846794d7d549c4f42139f5b316b765d8d90d686ff890466a6550c6`  
		Last Modified: Tue, 17 Mar 2026 03:25:10 GMT  
		Size: 27.1 MB (27103932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:1324a34d5164c61970d483eccc2194346ac044db00db0600f1517a13d155e78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6eef6b99bcd6aa01e5cf0fadd1f84f804417a2aa22cd3054b2c8722a340f74b`

```dockerfile
```

-	Layers:
	-	`sha256:12b8c77b02fb73641998a275cf6ac00bf2dbba608dcd95044d60b0559351145c`  
		Last Modified: Tue, 17 Mar 2026 03:25:09 GMT  
		Size: 24.6 MB (24593807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cf20a84f6f792840ed0856e3d11d4be39be3cb96b5ce98fcf507e953c59967`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:86808dfea395039494b4ce75d666c10264c353435b19fa8aecf74014a4500dd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:3f3434e8c66b35b4362d43b3c68d4debb705121fc5f16e850b6174f3c304be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297737941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b861d78ba166e07b81f0322c6e47e9a5a15c07400fb36c636a290ede57179`
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
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38077e6cfcbd5baf66472415e8a5d780f3de0dafa51d29468a03ecf6f9f8135f`  
		Last Modified: Tue, 17 Mar 2026 03:22:34 GMT  
		Size: 110.2 MB (110185787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449b29ed7335849798c88a6d5e97ab5f026c70338148cae7dbd88769de9d7ac9`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 397.5 KB (397528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf5de7d8b8ef94434270e8f7f6907642bd8ff1a706fe5da83278f624ddcc679`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615ef4778d0e24a85c04be1043b9f2a4efcb7435745fb881f91c76c43230449`  
		Last Modified: Tue, 17 Mar 2026 03:22:32 GMT  
		Size: 28.0 MB (28010658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:bf3566f1f09c8118d736c936f8d9a1441accd489d516c4c0cc4ce205565840e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54591db849ffc7e9320f0f8b07f6aff008c44e2800052d8b4421c0fb50eca387`

```dockerfile
```

-	Layers:
	-	`sha256:4b44b6d9082678531c67b5b4669eb393bb2bde2e284208bf385d1745b965f939`  
		Last Modified: Tue, 17 Mar 2026 03:22:31 GMT  
		Size: 24.6 MB (24571546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ee0f1caabf1f9ddb69204af7f718f229e0be39a1a7af06bc7ed3ca02613880`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:39e0457ec2d2b4a983c3fbc10989608149c95801cd935d78b47acf315b092689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286253348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353be99d01e2ddf62f150321868a918f3e04cc033646c6096b9642752fce4c6f`
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
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b4a8ad856ea6339c44417d49ca205c68a95d17f01148a70b8e3f039f3e946`  
		Last Modified: Tue, 17 Mar 2026 03:25:12 GMT  
		Size: 105.6 MB (105598022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc6c0a18c005b79ece467126eef3247c61cb22d0a0033c8bbad8e7cd9e6d0f`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 397.5 KB (397525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9715a303f4f20401efab555ff525c6d6e5512fcf959ba0fef1577655a158`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73015f6cee846794d7d549c4f42139f5b316b765d8d90d686ff890466a6550c6`  
		Last Modified: Tue, 17 Mar 2026 03:25:10 GMT  
		Size: 27.1 MB (27103932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1324a34d5164c61970d483eccc2194346ac044db00db0600f1517a13d155e78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6eef6b99bcd6aa01e5cf0fadd1f84f804417a2aa22cd3054b2c8722a340f74b`

```dockerfile
```

-	Layers:
	-	`sha256:12b8c77b02fb73641998a275cf6ac00bf2dbba608dcd95044d60b0559351145c`  
		Last Modified: Tue, 17 Mar 2026 03:25:09 GMT  
		Size: 24.6 MB (24593807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cf20a84f6f792840ed0856e3d11d4be39be3cb96b5ce98fcf507e953c59967`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:f166f8843c4e9d0daa6d3d46ddf94e2b9c24d4528ba23b670417c3612b21dcd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c67e76f473f78c8a586514f42ff90cede4983817642ec2833c0c09a1c8a4811e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159141469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986e2984e1a898f636dd2836fc3b1cd12099e47fde1abb8828b4dee22e5674ad`
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
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:532bc3aa23c4b1159c6e4496316f3f2cb6918232fc735cfcc523649ede27fe33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef83d24e317e67b9e2a9cf40e66e4e42d481994768ddf70314cf30f230b40e4`

```dockerfile
```

-	Layers:
	-	`sha256:e3d244e35056c2eac3feda388784e8e5707c4390dfdd6de4e16fc712fa71dfde`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dd1af4adf9c39ca81af616e2012014d0472bdd068360ffd8d5ab8ffcdec2d2`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ff3ca5af04319ebd01fdc0a8ca87bfc80e364bade419f540a5271ff61ab29b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153151364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5879234065016f688fe3de3e9ab8873ca0b8760662db642fcdf18825577b98`
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
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ce04a2ff107f3e2886980db837743ca52691801f340c3aaf198e409fa4402cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052cdf281590b7e26e9d670d3a4b71dac9d33509d3252d0111bebcaaa5957eb7`

```dockerfile
```

-	Layers:
	-	`sha256:f02552ffdff761db0d91c235be596e2696ffbd6365c9bf49cf84a684b6c132dd`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45c07c4ba308b8ae3a44ff25fdfd881349ad7298d112796b22c474555444508`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:f166f8843c4e9d0daa6d3d46ddf94e2b9c24d4528ba23b670417c3612b21dcd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c67e76f473f78c8a586514f42ff90cede4983817642ec2833c0c09a1c8a4811e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159141469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986e2984e1a898f636dd2836fc3b1cd12099e47fde1abb8828b4dee22e5674ad`
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
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:532bc3aa23c4b1159c6e4496316f3f2cb6918232fc735cfcc523649ede27fe33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef83d24e317e67b9e2a9cf40e66e4e42d481994768ddf70314cf30f230b40e4`

```dockerfile
```

-	Layers:
	-	`sha256:e3d244e35056c2eac3feda388784e8e5707c4390dfdd6de4e16fc712fa71dfde`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dd1af4adf9c39ca81af616e2012014d0472bdd068360ffd8d5ab8ffcdec2d2`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ff3ca5af04319ebd01fdc0a8ca87bfc80e364bade419f540a5271ff61ab29b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153151364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5879234065016f688fe3de3e9ab8873ca0b8760662db642fcdf18825577b98`
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
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ce04a2ff107f3e2886980db837743ca52691801f340c3aaf198e409fa4402cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052cdf281590b7e26e9d670d3a4b71dac9d33509d3252d0111bebcaaa5957eb7`

```dockerfile
```

-	Layers:
	-	`sha256:f02552ffdff761db0d91c235be596e2696ffbd6365c9bf49cf84a684b6c132dd`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45c07c4ba308b8ae3a44ff25fdfd881349ad7298d112796b22c474555444508`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:258d00503f89585c49d9c6e3d8b2d2118687c36eb970ac7531e5e8d908d9dc90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:7f8b2fa6ca5b5439b09c53c235658363e3dfac0325bf5402dd2d58c9020845c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298776460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72a7a4b4f0b36b161bbfc0c9fdbfac83c9d0525cf0ebfab1f69f3e17f059ea8`
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
# Tue, 17 Mar 2026 02:19:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:32 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:18 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733af0eb21948dafdba3174060d605a7a5ce37ef697e776ecdbcb5daa178b9d`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 683.9 KB (683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640a8010e6bda8de7f8d1c280d352ca1a547af8e23b3f7beb3840292846e9bd`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 6.8 MB (6751703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320dc2ec0b5cd3c55ef3f2e91e0549838485b3598dce50d390b3f4253f3c646`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 94.1 KB (94075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff09f05c982f53d0ecd47e2996c8fb168a31676c0c1f68841620f8ef113f0e8`  
		Last Modified: Tue, 17 Mar 2026 02:20:51 GMT  
		Size: 122.9 MB (122871643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f719d557608cd72ca6c0848ed9385a0a9a4c1d7b79e56b43afd124ab63727`  
		Last Modified: Tue, 17 Mar 2026 02:20:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d8b1d4752eaa500c6efc8db16cb8b457b543e0b16daa36cd38cd6b2b7b45e`  
		Last Modified: Tue, 17 Mar 2026 03:22:51 GMT  
		Size: 110.2 MB (110189194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a79975d2590faffad5964efa3ffcf70a8fdcdf4e4c793df399827287af1e83`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 376.3 KB (376275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01c121ff57367529a268f24be813245351e804f51e8e9dc6b4da3ac95b116fa`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 2.5 KB (2528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333f1ace39e22f1185f96b57b8f58282d8f0fae9cf0ccc9c5e5ce86615bf3eea`  
		Last Modified: Tue, 17 Mar 2026 03:22:49 GMT  
		Size: 28.1 MB (28074955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:34364ca6123378d9e09886b5a85e7af5d25e86eb055cede8c1d8d33d0e7950e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6461d8af0070b9cc224f352b3ca99290fda6b337272bf44c2b432fde63700c08`

```dockerfile
```

-	Layers:
	-	`sha256:3b460ea356b62d263160f53a0c5e7af91db668eeffc557e12c10c1c16ba6edbe`  
		Last Modified: Tue, 17 Mar 2026 03:22:49 GMT  
		Size: 24.8 MB (24750404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf536bcd2a322707b3913ce3c35fca9fff4822dd46b014b9a8efddb77bbc7dbf`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5edd16869ad274b3457437a50594e8d34fd121e9420cf30149231c112e4651fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287231128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b9ecccb229b0d7104a5c89db0dfdc55e8c11380430fade01f0f544fd67138c`
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
# Tue, 17 Mar 2026 02:24:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:52 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:44 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4032add1c3a62b531b452e08894f5b539c0ebfd5c41101aad071c963e7bc4118`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 684.1 KB (684058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085966617c2b05eb1bf8873d4280874b657172aa69a68c66409865ade8eec292`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 6.8 MB (6765000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a8e5be68a9bcecd8ad2b7c43f79072eca8f7dcc81717386af1707d76c3c4c7`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 94.2 KB (94245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f355398debccf560edf88d2aa155d7c6101b838903729fc38bf416cc8448374`  
		Last Modified: Tue, 17 Mar 2026 02:26:17 GMT  
		Size: 117.7 MB (117676995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfb1b28f8e68cb8f3e8734990e03424588ca25a16bf1883182c4b8ede619968`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99abc53ec2eca0dd072a2cc7fab9a934fd1b6a6a083bd93240cfc7b80a4210b`  
		Last Modified: Tue, 17 Mar 2026 03:25:27 GMT  
		Size: 105.6 MB (105601768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811e81c873626d10286438e225ebfa3bd0abeb8e53f29fa4cf9337e9675a9d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 376.3 KB (376283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608adc20c86b8592654ca33378bfb966f088ace2d840683a5093077c5d4f0d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d631be142011e9589eb9f51e2ff9e564cccde3e55fa6ec2ff28a54412a9bf1`  
		Last Modified: Tue, 17 Mar 2026 03:25:26 GMT  
		Size: 27.2 MB (27160351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:ac0c0441c404dc3e0f43580372b1dce6e2022881a39ca7505b26b2893e1b749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0c6f224bccc3e121e9e6d1bd5f16ec7123d762bbdf028036f86348780fd334`

```dockerfile
```

-	Layers:
	-	`sha256:0cda80f251b22178cdd01adf265d453144aab8dd6c45ac45c6d9bab8e9ce047e`  
		Last Modified: Tue, 17 Mar 2026 03:25:26 GMT  
		Size: 24.8 MB (24772666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b020317d4aefbf9d6679bd8c83d4b79e2cba2f488f828b7a43a5f083a0cb00d6`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:673660c925aeed56d042fe95a504226c5e3e7437fa21860643ab275f4c5f48a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:0cb65e798bfa9dbfe97a773fcf5cd322617f419afc0e61986cdec3cb0409bc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1083384718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8ca4438c4e2a32324bcc2f98d40d40c860e14a4d0f5f191053b44afce4565a`
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
# Tue, 17 Mar 2026 02:19:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:32 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:18 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:18:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733af0eb21948dafdba3174060d605a7a5ce37ef697e776ecdbcb5daa178b9d`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 683.9 KB (683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640a8010e6bda8de7f8d1c280d352ca1a547af8e23b3f7beb3840292846e9bd`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 6.8 MB (6751703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320dc2ec0b5cd3c55ef3f2e91e0549838485b3598dce50d390b3f4253f3c646`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 94.1 KB (94075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff09f05c982f53d0ecd47e2996c8fb168a31676c0c1f68841620f8ef113f0e8`  
		Last Modified: Tue, 17 Mar 2026 02:20:51 GMT  
		Size: 122.9 MB (122871643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f719d557608cd72ca6c0848ed9385a0a9a4c1d7b79e56b43afd124ab63727`  
		Last Modified: Tue, 17 Mar 2026 02:20:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d8b1d4752eaa500c6efc8db16cb8b457b543e0b16daa36cd38cd6b2b7b45e`  
		Last Modified: Tue, 17 Mar 2026 03:22:51 GMT  
		Size: 110.2 MB (110189194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a79975d2590faffad5964efa3ffcf70a8fdcdf4e4c793df399827287af1e83`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 376.3 KB (376275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01c121ff57367529a268f24be813245351e804f51e8e9dc6b4da3ac95b116fa`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 2.5 KB (2528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333f1ace39e22f1185f96b57b8f58282d8f0fae9cf0ccc9c5e5ce86615bf3eea`  
		Last Modified: Tue, 17 Mar 2026 03:22:49 GMT  
		Size: 28.1 MB (28074955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8ea38f657233a16eee65e26447c72fae06a56440ae220f627ea9c00d478334`  
		Last Modified: Tue, 17 Mar 2026 04:21:00 GMT  
		Size: 784.6 MB (784608258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:70eb82c653aae5508ffd082e2ddbf5952dbeeb3a4d951dac6993187e37dac2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60935687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9f5c57292e0e87839f0a3d3ed6f44d81b98ccdc87bd3cc74ccc8571d6997af`

```dockerfile
```

-	Layers:
	-	`sha256:83746e9dd84f5de2ec087e8533f5ed6008d3c37a66f5ecef61cacbfff0bf2fff`  
		Last Modified: Tue, 17 Mar 2026 04:20:47 GMT  
		Size: 60.9 MB (60926336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f6594ec7bde2328d5869361cbb8595f656dc53a8f00c3ebe9d7a9dcc203524`  
		Last Modified: Tue, 17 Mar 2026 04:20:44 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:974db85f78096e2ae99c4277c9072fbb2a18e92da17876eeccc013b8e27c6abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.0 MB (986019338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7a0fba274b3685ea68b5a3adf4068dad59744c9d59208e7b6eae72872256c3`
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
# Tue, 17 Mar 2026 02:24:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:52 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:44 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:15:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4032add1c3a62b531b452e08894f5b539c0ebfd5c41101aad071c963e7bc4118`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 684.1 KB (684058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085966617c2b05eb1bf8873d4280874b657172aa69a68c66409865ade8eec292`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 6.8 MB (6765000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a8e5be68a9bcecd8ad2b7c43f79072eca8f7dcc81717386af1707d76c3c4c7`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 94.2 KB (94245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f355398debccf560edf88d2aa155d7c6101b838903729fc38bf416cc8448374`  
		Last Modified: Tue, 17 Mar 2026 02:26:17 GMT  
		Size: 117.7 MB (117676995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfb1b28f8e68cb8f3e8734990e03424588ca25a16bf1883182c4b8ede619968`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99abc53ec2eca0dd072a2cc7fab9a934fd1b6a6a083bd93240cfc7b80a4210b`  
		Last Modified: Tue, 17 Mar 2026 03:25:27 GMT  
		Size: 105.6 MB (105601768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811e81c873626d10286438e225ebfa3bd0abeb8e53f29fa4cf9337e9675a9d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 376.3 KB (376283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608adc20c86b8592654ca33378bfb966f088ace2d840683a5093077c5d4f0d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d631be142011e9589eb9f51e2ff9e564cccde3e55fa6ec2ff28a54412a9bf1`  
		Last Modified: Tue, 17 Mar 2026 03:25:26 GMT  
		Size: 27.2 MB (27160351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4ffd70054ca1d1b611554e782951a5232b271d4143182b928004ae83f20290`  
		Last Modified: Tue, 17 Mar 2026 04:18:37 GMT  
		Size: 698.8 MB (698788210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:31f0ed54b58418e82f7fdb4c9fca8396851c5ec216704d2b971f7be7536df15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60866289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12b3bf3e14491b470a5a08dd351952ec0e26417cd626f2bda74585111d461b6`

```dockerfile
```

-	Layers:
	-	`sha256:0787d05cbc878db60e9c7661299d809b79a189ab4afab2d1259cb7224327d6ba`  
		Last Modified: Tue, 17 Mar 2026 04:18:27 GMT  
		Size: 60.9 MB (60856857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f480641ba7f3af817b2470daa82c4e1f87a736c57025a31f7e237fc35ca19f`  
		Last Modified: Tue, 17 Mar 2026 04:18:23 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:673660c925aeed56d042fe95a504226c5e3e7437fa21860643ab275f4c5f48a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:0cb65e798bfa9dbfe97a773fcf5cd322617f419afc0e61986cdec3cb0409bc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1083384718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8ca4438c4e2a32324bcc2f98d40d40c860e14a4d0f5f191053b44afce4565a`
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
# Tue, 17 Mar 2026 02:19:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:32 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:18 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:18:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733af0eb21948dafdba3174060d605a7a5ce37ef697e776ecdbcb5daa178b9d`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 683.9 KB (683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640a8010e6bda8de7f8d1c280d352ca1a547af8e23b3f7beb3840292846e9bd`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 6.8 MB (6751703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320dc2ec0b5cd3c55ef3f2e91e0549838485b3598dce50d390b3f4253f3c646`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 94.1 KB (94075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff09f05c982f53d0ecd47e2996c8fb168a31676c0c1f68841620f8ef113f0e8`  
		Last Modified: Tue, 17 Mar 2026 02:20:51 GMT  
		Size: 122.9 MB (122871643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f719d557608cd72ca6c0848ed9385a0a9a4c1d7b79e56b43afd124ab63727`  
		Last Modified: Tue, 17 Mar 2026 02:20:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d8b1d4752eaa500c6efc8db16cb8b457b543e0b16daa36cd38cd6b2b7b45e`  
		Last Modified: Tue, 17 Mar 2026 03:22:51 GMT  
		Size: 110.2 MB (110189194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a79975d2590faffad5964efa3ffcf70a8fdcdf4e4c793df399827287af1e83`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 376.3 KB (376275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01c121ff57367529a268f24be813245351e804f51e8e9dc6b4da3ac95b116fa`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 2.5 KB (2528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333f1ace39e22f1185f96b57b8f58282d8f0fae9cf0ccc9c5e5ce86615bf3eea`  
		Last Modified: Tue, 17 Mar 2026 03:22:49 GMT  
		Size: 28.1 MB (28074955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8ea38f657233a16eee65e26447c72fae06a56440ae220f627ea9c00d478334`  
		Last Modified: Tue, 17 Mar 2026 04:21:00 GMT  
		Size: 784.6 MB (784608258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:70eb82c653aae5508ffd082e2ddbf5952dbeeb3a4d951dac6993187e37dac2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60935687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9f5c57292e0e87839f0a3d3ed6f44d81b98ccdc87bd3cc74ccc8571d6997af`

```dockerfile
```

-	Layers:
	-	`sha256:83746e9dd84f5de2ec087e8533f5ed6008d3c37a66f5ecef61cacbfff0bf2fff`  
		Last Modified: Tue, 17 Mar 2026 04:20:47 GMT  
		Size: 60.9 MB (60926336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f6594ec7bde2328d5869361cbb8595f656dc53a8f00c3ebe9d7a9dcc203524`  
		Last Modified: Tue, 17 Mar 2026 04:20:44 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:974db85f78096e2ae99c4277c9072fbb2a18e92da17876eeccc013b8e27c6abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.0 MB (986019338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7a0fba274b3685ea68b5a3adf4068dad59744c9d59208e7b6eae72872256c3`
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
# Tue, 17 Mar 2026 02:24:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:52 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:44 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:15:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4032add1c3a62b531b452e08894f5b539c0ebfd5c41101aad071c963e7bc4118`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 684.1 KB (684058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085966617c2b05eb1bf8873d4280874b657172aa69a68c66409865ade8eec292`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 6.8 MB (6765000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a8e5be68a9bcecd8ad2b7c43f79072eca8f7dcc81717386af1707d76c3c4c7`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 94.2 KB (94245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f355398debccf560edf88d2aa155d7c6101b838903729fc38bf416cc8448374`  
		Last Modified: Tue, 17 Mar 2026 02:26:17 GMT  
		Size: 117.7 MB (117676995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfb1b28f8e68cb8f3e8734990e03424588ca25a16bf1883182c4b8ede619968`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99abc53ec2eca0dd072a2cc7fab9a934fd1b6a6a083bd93240cfc7b80a4210b`  
		Last Modified: Tue, 17 Mar 2026 03:25:27 GMT  
		Size: 105.6 MB (105601768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811e81c873626d10286438e225ebfa3bd0abeb8e53f29fa4cf9337e9675a9d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 376.3 KB (376283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608adc20c86b8592654ca33378bfb966f088ace2d840683a5093077c5d4f0d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d631be142011e9589eb9f51e2ff9e564cccde3e55fa6ec2ff28a54412a9bf1`  
		Last Modified: Tue, 17 Mar 2026 03:25:26 GMT  
		Size: 27.2 MB (27160351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4ffd70054ca1d1b611554e782951a5232b271d4143182b928004ae83f20290`  
		Last Modified: Tue, 17 Mar 2026 04:18:37 GMT  
		Size: 698.8 MB (698788210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:31f0ed54b58418e82f7fdb4c9fca8396851c5ec216704d2b971f7be7536df15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60866289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12b3bf3e14491b470a5a08dd351952ec0e26417cd626f2bda74585111d461b6`

```dockerfile
```

-	Layers:
	-	`sha256:0787d05cbc878db60e9c7661299d809b79a189ab4afab2d1259cb7224327d6ba`  
		Last Modified: Tue, 17 Mar 2026 04:18:27 GMT  
		Size: 60.9 MB (60856857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f480641ba7f3af817b2470daa82c4e1f87a736c57025a31f7e237fc35ca19f`  
		Last Modified: Tue, 17 Mar 2026 04:18:23 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:258d00503f89585c49d9c6e3d8b2d2118687c36eb970ac7531e5e8d908d9dc90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:7f8b2fa6ca5b5439b09c53c235658363e3dfac0325bf5402dd2d58c9020845c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298776460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72a7a4b4f0b36b161bbfc0c9fdbfac83c9d0525cf0ebfab1f69f3e17f059ea8`
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
# Tue, 17 Mar 2026 02:19:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:32 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:18 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733af0eb21948dafdba3174060d605a7a5ce37ef697e776ecdbcb5daa178b9d`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 683.9 KB (683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640a8010e6bda8de7f8d1c280d352ca1a547af8e23b3f7beb3840292846e9bd`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 6.8 MB (6751703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320dc2ec0b5cd3c55ef3f2e91e0549838485b3598dce50d390b3f4253f3c646`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 94.1 KB (94075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff09f05c982f53d0ecd47e2996c8fb168a31676c0c1f68841620f8ef113f0e8`  
		Last Modified: Tue, 17 Mar 2026 02:20:51 GMT  
		Size: 122.9 MB (122871643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f719d557608cd72ca6c0848ed9385a0a9a4c1d7b79e56b43afd124ab63727`  
		Last Modified: Tue, 17 Mar 2026 02:20:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d8b1d4752eaa500c6efc8db16cb8b457b543e0b16daa36cd38cd6b2b7b45e`  
		Last Modified: Tue, 17 Mar 2026 03:22:51 GMT  
		Size: 110.2 MB (110189194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a79975d2590faffad5964efa3ffcf70a8fdcdf4e4c793df399827287af1e83`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 376.3 KB (376275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01c121ff57367529a268f24be813245351e804f51e8e9dc6b4da3ac95b116fa`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 2.5 KB (2528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333f1ace39e22f1185f96b57b8f58282d8f0fae9cf0ccc9c5e5ce86615bf3eea`  
		Last Modified: Tue, 17 Mar 2026 03:22:49 GMT  
		Size: 28.1 MB (28074955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:34364ca6123378d9e09886b5a85e7af5d25e86eb055cede8c1d8d33d0e7950e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6461d8af0070b9cc224f352b3ca99290fda6b337272bf44c2b432fde63700c08`

```dockerfile
```

-	Layers:
	-	`sha256:3b460ea356b62d263160f53a0c5e7af91db668eeffc557e12c10c1c16ba6edbe`  
		Last Modified: Tue, 17 Mar 2026 03:22:49 GMT  
		Size: 24.8 MB (24750404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf536bcd2a322707b3913ce3c35fca9fff4822dd46b014b9a8efddb77bbc7dbf`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5edd16869ad274b3457437a50594e8d34fd121e9420cf30149231c112e4651fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287231128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b9ecccb229b0d7104a5c89db0dfdc55e8c11380430fade01f0f544fd67138c`
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
# Tue, 17 Mar 2026 02:24:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:52 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:44 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4032add1c3a62b531b452e08894f5b539c0ebfd5c41101aad071c963e7bc4118`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 684.1 KB (684058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085966617c2b05eb1bf8873d4280874b657172aa69a68c66409865ade8eec292`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 6.8 MB (6765000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a8e5be68a9bcecd8ad2b7c43f79072eca8f7dcc81717386af1707d76c3c4c7`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 94.2 KB (94245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f355398debccf560edf88d2aa155d7c6101b838903729fc38bf416cc8448374`  
		Last Modified: Tue, 17 Mar 2026 02:26:17 GMT  
		Size: 117.7 MB (117676995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfb1b28f8e68cb8f3e8734990e03424588ca25a16bf1883182c4b8ede619968`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99abc53ec2eca0dd072a2cc7fab9a934fd1b6a6a083bd93240cfc7b80a4210b`  
		Last Modified: Tue, 17 Mar 2026 03:25:27 GMT  
		Size: 105.6 MB (105601768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811e81c873626d10286438e225ebfa3bd0abeb8e53f29fa4cf9337e9675a9d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 376.3 KB (376283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608adc20c86b8592654ca33378bfb966f088ace2d840683a5093077c5d4f0d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d631be142011e9589eb9f51e2ff9e564cccde3e55fa6ec2ff28a54412a9bf1`  
		Last Modified: Tue, 17 Mar 2026 03:25:26 GMT  
		Size: 27.2 MB (27160351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:ac0c0441c404dc3e0f43580372b1dce6e2022881a39ca7505b26b2893e1b749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0c6f224bccc3e121e9e6d1bd5f16ec7123d762bbdf028036f86348780fd334`

```dockerfile
```

-	Layers:
	-	`sha256:0cda80f251b22178cdd01adf265d453144aab8dd6c45ac45c6d9bab8e9ce047e`  
		Last Modified: Tue, 17 Mar 2026 03:25:26 GMT  
		Size: 24.8 MB (24772666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b020317d4aefbf9d6679bd8c83d4b79e2cba2f488f828b7a43a5f083a0cb00d6`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:258d00503f89585c49d9c6e3d8b2d2118687c36eb970ac7531e5e8d908d9dc90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:7f8b2fa6ca5b5439b09c53c235658363e3dfac0325bf5402dd2d58c9020845c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298776460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72a7a4b4f0b36b161bbfc0c9fdbfac83c9d0525cf0ebfab1f69f3e17f059ea8`
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
# Tue, 17 Mar 2026 02:19:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:32 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:18 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733af0eb21948dafdba3174060d605a7a5ce37ef697e776ecdbcb5daa178b9d`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 683.9 KB (683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640a8010e6bda8de7f8d1c280d352ca1a547af8e23b3f7beb3840292846e9bd`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 6.8 MB (6751703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320dc2ec0b5cd3c55ef3f2e91e0549838485b3598dce50d390b3f4253f3c646`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 94.1 KB (94075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff09f05c982f53d0ecd47e2996c8fb168a31676c0c1f68841620f8ef113f0e8`  
		Last Modified: Tue, 17 Mar 2026 02:20:51 GMT  
		Size: 122.9 MB (122871643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f719d557608cd72ca6c0848ed9385a0a9a4c1d7b79e56b43afd124ab63727`  
		Last Modified: Tue, 17 Mar 2026 02:20:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00d8b1d4752eaa500c6efc8db16cb8b457b543e0b16daa36cd38cd6b2b7b45e`  
		Last Modified: Tue, 17 Mar 2026 03:22:51 GMT  
		Size: 110.2 MB (110189194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a79975d2590faffad5964efa3ffcf70a8fdcdf4e4c793df399827287af1e83`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 376.3 KB (376275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01c121ff57367529a268f24be813245351e804f51e8e9dc6b4da3ac95b116fa`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 2.5 KB (2528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333f1ace39e22f1185f96b57b8f58282d8f0fae9cf0ccc9c5e5ce86615bf3eea`  
		Last Modified: Tue, 17 Mar 2026 03:22:49 GMT  
		Size: 28.1 MB (28074955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:34364ca6123378d9e09886b5a85e7af5d25e86eb055cede8c1d8d33d0e7950e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6461d8af0070b9cc224f352b3ca99290fda6b337272bf44c2b432fde63700c08`

```dockerfile
```

-	Layers:
	-	`sha256:3b460ea356b62d263160f53a0c5e7af91db668eeffc557e12c10c1c16ba6edbe`  
		Last Modified: Tue, 17 Mar 2026 03:22:49 GMT  
		Size: 24.8 MB (24750404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf536bcd2a322707b3913ce3c35fca9fff4822dd46b014b9a8efddb77bbc7dbf`  
		Last Modified: Tue, 17 Mar 2026 03:22:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5edd16869ad274b3457437a50594e8d34fd121e9420cf30149231c112e4651fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287231128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b9ecccb229b0d7104a5c89db0dfdc55e8c11380430fade01f0f544fd67138c`
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
# Tue, 17 Mar 2026 02:24:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:52 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:44 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4032add1c3a62b531b452e08894f5b539c0ebfd5c41101aad071c963e7bc4118`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 684.1 KB (684058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085966617c2b05eb1bf8873d4280874b657172aa69a68c66409865ade8eec292`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 6.8 MB (6765000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a8e5be68a9bcecd8ad2b7c43f79072eca8f7dcc81717386af1707d76c3c4c7`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 94.2 KB (94245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f355398debccf560edf88d2aa155d7c6101b838903729fc38bf416cc8448374`  
		Last Modified: Tue, 17 Mar 2026 02:26:17 GMT  
		Size: 117.7 MB (117676995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfb1b28f8e68cb8f3e8734990e03424588ca25a16bf1883182c4b8ede619968`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99abc53ec2eca0dd072a2cc7fab9a934fd1b6a6a083bd93240cfc7b80a4210b`  
		Last Modified: Tue, 17 Mar 2026 03:25:27 GMT  
		Size: 105.6 MB (105601768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811e81c873626d10286438e225ebfa3bd0abeb8e53f29fa4cf9337e9675a9d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 376.3 KB (376283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1608adc20c86b8592654ca33378bfb966f088ace2d840683a5093077c5d4f0d0`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 2.5 KB (2524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d631be142011e9589eb9f51e2ff9e564cccde3e55fa6ec2ff28a54412a9bf1`  
		Last Modified: Tue, 17 Mar 2026 03:25:26 GMT  
		Size: 27.2 MB (27160351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ac0c0441c404dc3e0f43580372b1dce6e2022881a39ca7505b26b2893e1b749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0c6f224bccc3e121e9e6d1bd5f16ec7123d762bbdf028036f86348780fd334`

```dockerfile
```

-	Layers:
	-	`sha256:0cda80f251b22178cdd01adf265d453144aab8dd6c45ac45c6d9bab8e9ce047e`  
		Last Modified: Tue, 17 Mar 2026 03:25:26 GMT  
		Size: 24.8 MB (24772666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b020317d4aefbf9d6679bd8c83d4b79e2cba2f488f828b7a43a5f083a0cb00d6`  
		Last Modified: Tue, 17 Mar 2026 03:25:24 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:e3753bb7345ae66d20a85360064a017bc73ee132b51af1f3a57d0cecf72c0425
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:a733b6a58c9518f8d23031ca2917d1e6fed5cf66897c36bf517d7690632fb23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160133508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74430c7fab4a92b84797b5d3cc7b6691d5f4878209120ba613373234089b0ed7`
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
# Tue, 17 Mar 2026 02:19:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:32 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733af0eb21948dafdba3174060d605a7a5ce37ef697e776ecdbcb5daa178b9d`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 683.9 KB (683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640a8010e6bda8de7f8d1c280d352ca1a547af8e23b3f7beb3840292846e9bd`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 6.8 MB (6751703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320dc2ec0b5cd3c55ef3f2e91e0549838485b3598dce50d390b3f4253f3c646`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 94.1 KB (94075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff09f05c982f53d0ecd47e2996c8fb168a31676c0c1f68841620f8ef113f0e8`  
		Last Modified: Tue, 17 Mar 2026 02:20:51 GMT  
		Size: 122.9 MB (122871643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f719d557608cd72ca6c0848ed9385a0a9a4c1d7b79e56b43afd124ab63727`  
		Last Modified: Tue, 17 Mar 2026 02:20:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:e9e5b4a1443e3e1bf4072ca79d1258b2ff7424b7da25f76688a9f3bc217454de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18503158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444a11dfca0a3c8682adae2970b145ee758812dcbd35a963e2a2b3397f730e1f`

```dockerfile
```

-	Layers:
	-	`sha256:696a56d95d98337f9f57a1a3ae0c5720c24c702ef54665172e5704de8a023d19`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 18.5 MB (18488549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27233ab89252b591c61a9ba75ce4ef04b6f2f6535289ba65d511689ca8fb4c40`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:73a83bd86e2d78244a86e55d465a714581790157ef3012657229198889e9a99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154090202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd4f42dccd24054800ef113a447df83b0079d199dd841700024024b894b74b`
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
# Tue, 17 Mar 2026 02:24:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:52 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4032add1c3a62b531b452e08894f5b539c0ebfd5c41101aad071c963e7bc4118`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 684.1 KB (684058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085966617c2b05eb1bf8873d4280874b657172aa69a68c66409865ade8eec292`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 6.8 MB (6765000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a8e5be68a9bcecd8ad2b7c43f79072eca8f7dcc81717386af1707d76c3c4c7`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 94.2 KB (94245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f355398debccf560edf88d2aa155d7c6101b838903729fc38bf416cc8448374`  
		Last Modified: Tue, 17 Mar 2026 02:26:17 GMT  
		Size: 117.7 MB (117676995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfb1b28f8e68cb8f3e8734990e03424588ca25a16bf1883182c4b8ede619968`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:becee6d238d8febef1090bd3d96c0d3412ee36cefac5904217e495f0277c7cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d691f88e442cc910100f203b35a37e7990e6436700cd76fac5ba937fd05a7f`

```dockerfile
```

-	Layers:
	-	`sha256:4753a18709ca6baa0e04eb09c5a6060ab69bdd6cc8205565039c3389fe9e7505`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 18.5 MB (18462560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84b870f9fa5c36e25a8db2f6cc983183fb4a796cbc18fe8da972c5bd16f6f50`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:e3753bb7345ae66d20a85360064a017bc73ee132b51af1f3a57d0cecf72c0425
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:a733b6a58c9518f8d23031ca2917d1e6fed5cf66897c36bf517d7690632fb23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160133508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74430c7fab4a92b84797b5d3cc7b6691d5f4878209120ba613373234089b0ed7`
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
# Tue, 17 Mar 2026 02:19:13 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:32 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:18 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733af0eb21948dafdba3174060d605a7a5ce37ef697e776ecdbcb5daa178b9d`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 683.9 KB (683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640a8010e6bda8de7f8d1c280d352ca1a547af8e23b3f7beb3840292846e9bd`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 6.8 MB (6751703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320dc2ec0b5cd3c55ef3f2e91e0549838485b3598dce50d390b3f4253f3c646`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 94.1 KB (94075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff09f05c982f53d0ecd47e2996c8fb168a31676c0c1f68841620f8ef113f0e8`  
		Last Modified: Tue, 17 Mar 2026 02:20:51 GMT  
		Size: 122.9 MB (122871643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f719d557608cd72ca6c0848ed9385a0a9a4c1d7b79e56b43afd124ab63727`  
		Last Modified: Tue, 17 Mar 2026 02:20:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e9e5b4a1443e3e1bf4072ca79d1258b2ff7424b7da25f76688a9f3bc217454de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18503158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444a11dfca0a3c8682adae2970b145ee758812dcbd35a963e2a2b3397f730e1f`

```dockerfile
```

-	Layers:
	-	`sha256:696a56d95d98337f9f57a1a3ae0c5720c24c702ef54665172e5704de8a023d19`  
		Last Modified: Tue, 17 Mar 2026 02:20:48 GMT  
		Size: 18.5 MB (18488549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27233ab89252b591c61a9ba75ce4ef04b6f2f6535289ba65d511689ca8fb4c40`  
		Last Modified: Tue, 17 Mar 2026 02:20:47 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:73a83bd86e2d78244a86e55d465a714581790157ef3012657229198889e9a99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154090202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd4f42dccd24054800ef113a447df83b0079d199dd841700024024b894b74b`
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
# Tue, 17 Mar 2026 02:24:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:52 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:44 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Mar 2026 02:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4032add1c3a62b531b452e08894f5b539c0ebfd5c41101aad071c963e7bc4118`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 684.1 KB (684058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085966617c2b05eb1bf8873d4280874b657172aa69a68c66409865ade8eec292`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 6.8 MB (6765000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a8e5be68a9bcecd8ad2b7c43f79072eca8f7dcc81717386af1707d76c3c4c7`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 94.2 KB (94245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f355398debccf560edf88d2aa155d7c6101b838903729fc38bf416cc8448374`  
		Last Modified: Tue, 17 Mar 2026 02:26:17 GMT  
		Size: 117.7 MB (117676995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfb1b28f8e68cb8f3e8734990e03424588ca25a16bf1883182c4b8ede619968`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:becee6d238d8febef1090bd3d96c0d3412ee36cefac5904217e495f0277c7cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18477294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d691f88e442cc910100f203b35a37e7990e6436700cd76fac5ba937fd05a7f`

```dockerfile
```

-	Layers:
	-	`sha256:4753a18709ca6baa0e04eb09c5a6060ab69bdd6cc8205565039c3389fe9e7505`  
		Last Modified: Tue, 17 Mar 2026 02:26:14 GMT  
		Size: 18.5 MB (18462560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84b870f9fa5c36e25a8db2f6cc983183fb4a796cbc18fe8da972c5bd16f6f50`  
		Last Modified: Tue, 17 Mar 2026 02:26:13 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:86808dfea395039494b4ce75d666c10264c353435b19fa8aecf74014a4500dd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:3f3434e8c66b35b4362d43b3c68d4debb705121fc5f16e850b6174f3c304be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297737941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2b861d78ba166e07b81f0322c6e47e9a5a15c07400fb36c636a290ede57179`
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
# Tue, 17 Mar 2026 02:19:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:20:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:20:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:20:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:20:05 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4573c7be9d73705c0bb791e2cc7a3cdf038683b9864c37cacf1e7d37b35f8`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 683.9 KB (683886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368d690de1e3b7bc830ed3cfcc7712dfbe68a7c08dacb836cbd611c9e4dc41a`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 6.8 MB (6751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece1eb6223c5724538b469a1a0ab386a04f51a8415716356c2b58e64bfabda59`  
		Last Modified: Tue, 17 Mar 2026 02:20:31 GMT  
		Size: 94.1 KB (94091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c84744087b27b97a38f3a63730cb34997b7bd8897f443bd24cae94191cafc9`  
		Last Modified: Tue, 17 Mar 2026 02:20:34 GMT  
		Size: 121.9 MB (121879621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b8a2170ee1435217998b618da53396cb6dd965ab36f53083e01c662b6bc00`  
		Last Modified: Tue, 17 Mar 2026 02:20:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38077e6cfcbd5baf66472415e8a5d780f3de0dafa51d29468a03ecf6f9f8135f`  
		Last Modified: Tue, 17 Mar 2026 03:22:34 GMT  
		Size: 110.2 MB (110185787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449b29ed7335849798c88a6d5e97ab5f026c70338148cae7dbd88769de9d7ac9`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 397.5 KB (397528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf5de7d8b8ef94434270e8f7f6907642bd8ff1a706fe5da83278f624ddcc679`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615ef4778d0e24a85c04be1043b9f2a4efcb7435745fb881f91c76c43230449`  
		Last Modified: Tue, 17 Mar 2026 03:22:32 GMT  
		Size: 28.0 MB (28010658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:bf3566f1f09c8118d736c936f8d9a1441accd489d516c4c0cc4ce205565840e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54591db849ffc7e9320f0f8b07f6aff008c44e2800052d8b4421c0fb50eca387`

```dockerfile
```

-	Layers:
	-	`sha256:4b44b6d9082678531c67b5b4669eb393bb2bde2e284208bf385d1745b965f939`  
		Last Modified: Tue, 17 Mar 2026 03:22:31 GMT  
		Size: 24.6 MB (24571546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ee0f1caabf1f9ddb69204af7f718f229e0be39a1a7af06bc7ed3ca02613880`  
		Last Modified: Tue, 17 Mar 2026 03:22:30 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:39e0457ec2d2b4a983c3fbc10989608149c95801cd935d78b47acf315b092689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286253348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353be99d01e2ddf62f150321868a918f3e04cc033646c6096b9642752fce4c6f`
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
# Tue, 17 Mar 2026 02:24:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:51 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:25:56 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Mar 2026 02:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:25:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:25:56 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:24:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fea7bb6a53c36da8c8f418e272e9aa6d2f438851fd6321f099a7c8181ee3f3`  
		Last Modified: Tue, 17 Mar 2026 02:26:26 GMT  
		Size: 684.0 KB (684042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69bb424697dd6812c95d01160609a8beb614b0848e1b22409ce6a4607a3fb`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 6.8 MB (6765012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e562919faf985671753e63630ed9813bd3e261af2ef9eef2f11771ef790ee`  
		Last Modified: Tue, 17 Mar 2026 02:26:27 GMT  
		Size: 94.2 KB (94236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72df34e90ecee635227f37e80530183d7ff158f9ee3601907cd9ed66555ff3bc`  
		Last Modified: Tue, 17 Mar 2026 02:26:30 GMT  
		Size: 116.7 MB (116738169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9ccc54bee1d6b7b4d1660cb215140cbe5a8ddc85458e03d53bc3523406874`  
		Last Modified: Tue, 17 Mar 2026 02:26:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b4a8ad856ea6339c44417d49ca205c68a95d17f01148a70b8e3f039f3e946`  
		Last Modified: Tue, 17 Mar 2026 03:25:12 GMT  
		Size: 105.6 MB (105598022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcc6c0a18c005b79ece467126eef3247c61cb22d0a0033c8bbad8e7cd9e6d0f`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 397.5 KB (397525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce9715a303f4f20401efab555ff525c6d6e5512fcf959ba0fef1577655a158`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73015f6cee846794d7d549c4f42139f5b316b765d8d90d686ff890466a6550c6`  
		Last Modified: Tue, 17 Mar 2026 03:25:10 GMT  
		Size: 27.1 MB (27103932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:1324a34d5164c61970d483eccc2194346ac044db00db0600f1517a13d155e78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6eef6b99bcd6aa01e5cf0fadd1f84f804417a2aa22cd3054b2c8722a340f74b`

```dockerfile
```

-	Layers:
	-	`sha256:12b8c77b02fb73641998a275cf6ac00bf2dbba608dcd95044d60b0559351145c`  
		Last Modified: Tue, 17 Mar 2026 03:25:09 GMT  
		Size: 24.6 MB (24593807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0cf20a84f6f792840ed0856e3d11d4be39be3cb96b5ce98fcf507e953c59967`  
		Last Modified: Tue, 17 Mar 2026 03:25:08 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:f790a9b8147bb016aa1e6e4cb4e2113b24941414f99346ed2c66227e13548c1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

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

### `ros:rolling` - unknown; unknown

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

### `ros:rolling` - linux; arm64 variant v8

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

### `ros:rolling` - unknown; unknown

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

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:6b87d905fe62638a4377f75c1aae143931cc5d73572fff684c148153a0304065
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

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

### `ros:rolling-perception-noble` - unknown; unknown

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

### `ros:rolling-perception-noble` - linux; arm64 variant v8

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

### `ros:rolling-perception-noble` - unknown; unknown

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

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:f790a9b8147bb016aa1e6e4cb4e2113b24941414f99346ed2c66227e13548c1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

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

### `ros:rolling-ros-base-noble` - unknown; unknown

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

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

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

### `ros:rolling-ros-base-noble` - unknown; unknown

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

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:b1e8e7cec034dd09b179be382a6b5782aa78f55c207bd1e01fe061f5acfbdfc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c383f64648dbdac701e1003a66ea110362396d92e4fe609def1d4d23e9e9c6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173792134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69edf43e6e0fff4dab5edcceb27e8e22d9d91e0cb6aeab958c6cfcf0de34b5df`
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

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:5342dea70b71b20a33ba0edc2d9c5b4005570bda6808c462e7016ea89ea426c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19431994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d7256ba5081776b9a2943da90c29ca971962c8796832e3f094d12cffa37f80`

```dockerfile
```

-	Layers:
	-	`sha256:2668f1a3b46013ba0c9fa9432a15e712db3a9520d3666ac68fe68a189d49d3e3`  
		Last Modified: Tue, 17 Mar 2026 02:21:31 GMT  
		Size: 19.4 MB (19417372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d17af51955f4bda4f92e3e0fec6e7d6d38bb9d5cf7234718b3b3fdf1f07dba`  
		Last Modified: Tue, 17 Mar 2026 02:21:30 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a8e018a7e06260f245f22aec9d55d5c49a8106d39651293b97287bbec47fab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167376535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d621d83bb7081037ad550e318741601de7214d820a82fa297e5aa5ca7292214`
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

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:86759c8f002027b47d6986dafcb9fb7ae0b9f163fb08790937cce262b7fd4896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19406328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b349b47c175b53c136ec18e6ce4fa2927086d720f7e1b53de4de6295d72404a7`

```dockerfile
```

-	Layers:
	-	`sha256:e7cc09dec0d91b6505ca752c9c81434c9b093fdda14f0cbeea38818d47a3b849`  
		Last Modified: Tue, 17 Mar 2026 02:27:22 GMT  
		Size: 19.4 MB (19391581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd67238c8d14a44be21455eff8f7ce69131b87b7407ed23209efa000511cd94`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:b1e8e7cec034dd09b179be382a6b5782aa78f55c207bd1e01fe061f5acfbdfc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c383f64648dbdac701e1003a66ea110362396d92e4fe609def1d4d23e9e9c6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173792134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69edf43e6e0fff4dab5edcceb27e8e22d9d91e0cb6aeab958c6cfcf0de34b5df`
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

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5342dea70b71b20a33ba0edc2d9c5b4005570bda6808c462e7016ea89ea426c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19431994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d7256ba5081776b9a2943da90c29ca971962c8796832e3f094d12cffa37f80`

```dockerfile
```

-	Layers:
	-	`sha256:2668f1a3b46013ba0c9fa9432a15e712db3a9520d3666ac68fe68a189d49d3e3`  
		Last Modified: Tue, 17 Mar 2026 02:21:31 GMT  
		Size: 19.4 MB (19417372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d17af51955f4bda4f92e3e0fec6e7d6d38bb9d5cf7234718b3b3fdf1f07dba`  
		Last Modified: Tue, 17 Mar 2026 02:21:30 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a8e018a7e06260f245f22aec9d55d5c49a8106d39651293b97287bbec47fab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167376535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d621d83bb7081037ad550e318741601de7214d820a82fa297e5aa5ca7292214`
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

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:86759c8f002027b47d6986dafcb9fb7ae0b9f163fb08790937cce262b7fd4896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19406328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b349b47c175b53c136ec18e6ce4fa2927086d720f7e1b53de4de6295d72404a7`

```dockerfile
```

-	Layers:
	-	`sha256:e7cc09dec0d91b6505ca752c9c81434c9b093fdda14f0cbeea38818d47a3b849`  
		Last Modified: Tue, 17 Mar 2026 02:27:22 GMT  
		Size: 19.4 MB (19391581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd67238c8d14a44be21455eff8f7ce69131b87b7407ed23209efa000511cd94`  
		Last Modified: Tue, 17 Mar 2026 02:27:21 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json
