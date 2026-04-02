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
