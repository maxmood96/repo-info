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
