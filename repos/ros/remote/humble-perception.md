## `ros:humble-perception`

```console
$ docker pull ros@sha256:a7db64c10d040328ad0a90efdc8d0b8a27291c2d2fa36375e6b94aa40abd4fc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:b20d86ce714fa1598a4699d7c2375151778e578efe1ae3b64dd839bdcd8c6e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **956.7 MB (956701004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846866bb638b0b0fcb4ce964e439ce5d40d734eb4e4835a4ccd9416fc33525b5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:18:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:18:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:18:49 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:31 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:19:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:19:31 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Mar 2026 02:19:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:31 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:19:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:19:31 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:21:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:21:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:21:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:21:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:16:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfd2c34a991a09624371b32b6fcf6e92986a8301e422f6a558b4e8f4f18329a`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 1.2 MB (1213999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b63153c9a2ebb39e2467cf3e67d0cdf495bd07a8890b0f80e6d844df6cb0fce`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 6.0 MB (5994245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2aa55869bdf08d5e26fbd25963cad70c5139100319ef54869a9d35af58a886`  
		Last Modified: Tue, 17 Mar 2026 02:19:59 GMT  
		Size: 97.1 KB (97096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c3d498b896bd0d680b2966d17c9d2a0a912ba15945ea1193c3a3043d7908b`  
		Last Modified: Tue, 17 Mar 2026 02:20:02 GMT  
		Size: 105.8 MB (105841728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c68a8c01cb6477e1a800c4558943962ec4f2c0d391d4ec763c020fa40e39af`  
		Last Modified: Tue, 17 Mar 2026 02:20:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00489cc6396a88167e4531371de562751a3957af6d065052b4fa6a9101754ef`  
		Last Modified: Tue, 17 Mar 2026 03:22:02 GMT  
		Size: 98.2 MB (98161888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58e0f5560d48a980dcdfafaa9138ccfed55255b73cb78a233ef6f401930119`  
		Last Modified: Tue, 17 Mar 2026 03:21:59 GMT  
		Size: 387.9 KB (387862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a1815cda1265b38c5ca51367bd334346bf36e68d477352e705d56b62746afd`  
		Last Modified: Tue, 17 Mar 2026 03:22:00 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054b9fca4703875b30fd2d09bd01eaff8b9323487ffb2748dfa7e414eb745d59`  
		Last Modified: Tue, 17 Mar 2026 03:22:01 GMT  
		Size: 23.3 MB (23321779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b9cba4c2c0773c9d0c89ea1e9ff7b1930aabedbb8cfef61b453ec558e50d72`  
		Last Modified: Tue, 17 Mar 2026 04:19:22 GMT  
		Size: 692.1 MB (692141182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1a5fe1e3acd7b8c5b613ff23eeb060ad61547d831bfb2f7e85e80f9a46fcd10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58809545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febf37c356056c207c6d8ed9f7ed43f4a7413bb479aba871403bdb2060ed0040`

```dockerfile
```

-	Layers:
	-	`sha256:533fe82ccdd42ee03af95c25b191174f930b4af85b104e6e693bf6a4bc474c77`  
		Last Modified: Tue, 17 Mar 2026 04:19:11 GMT  
		Size: 58.8 MB (58800193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f09f6e8efc857fb1da9df43355514af22c8a3a9831b28bec595bdb694d43b90`  
		Last Modified: Tue, 17 Mar 2026 04:19:08 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:305332cbfecf2a9facf6b1d27668db8f4e400f2f46b01531682e4af8e7ac245b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.2 MB (917221480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5a5f34f20878aecc0aaae3139971140dfeedbc60f454032bb85d0b9dcf65e4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:23:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:04 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:24:50 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Mar 2026 02:24:50 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Mar 2026 02:24:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:50 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 02:24:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Mar 2026 02:24:50 GMT
CMD ["bash"]
# Tue, 17 Mar 2026 03:23:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:24:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Mar 2026 03:24:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Mar 2026 03:24:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 04:15:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08eef9390c8d17a2867d2cc67d4ec838c93c03a7045dadcdeb0e9bd339e8db`  
		Last Modified: Tue, 17 Mar 2026 02:25:16 GMT  
		Size: 1.2 MB (1214207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baacc168eca73410a17a8b087d985e0d659de747ff5e3f5a00d5b462df941040`  
		Last Modified: Tue, 17 Mar 2026 02:25:16 GMT  
		Size: 5.9 MB (5948658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcd5bd5f34de5076585c79ef1dd14ccdbd39f658cee916aeebde11ee7e95f65`  
		Last Modified: Tue, 17 Mar 2026 02:25:16 GMT  
		Size: 97.3 KB (97256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3732d4ac40268f48126bab964c6e31a9ac6eeec5a94ed0c805ad4c2b81a4c7c7`  
		Last Modified: Tue, 17 Mar 2026 02:25:19 GMT  
		Size: 103.6 MB (103575625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd97b542b267c300e8a50b87930c719a06c2db81cbf6d6d2246ee634fa990ff`  
		Last Modified: Tue, 17 Mar 2026 02:25:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aee43032cde39f43d6a9e817caa6b6665d8c258fe8c3977c9a45b5d107a487c`  
		Last Modified: Tue, 17 Mar 2026 03:24:59 GMT  
		Size: 95.8 MB (95794345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac49b75192da8a3641cda3227e83bb92fc2daa7bd7acad284d20a73ea3d29f16`  
		Last Modified: Tue, 17 Mar 2026 03:24:56 GMT  
		Size: 387.9 KB (387861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697e29309a868c92d06b09f5c37329b44ab966c59cc087bc46428063007882bd`  
		Last Modified: Tue, 17 Mar 2026 03:24:56 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4a500067d77cd184cd441ba27926afd3dd8a4d133de19b91cfa4d7229ece9a`  
		Last Modified: Tue, 17 Mar 2026 03:24:58 GMT  
		Size: 22.7 MB (22719223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a1cbcb484d570fccaa51baaa58ae982e28df774ed0bd5e020d50a980961a52`  
		Last Modified: Tue, 17 Mar 2026 04:17:56 GMT  
		Size: 660.1 MB (660092583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:d34c10a408ccf7bc8bf52b2b5e8235fff8f597b5cc65fcfe99e3091ca1f8f6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58793946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d8d035f16dbf1d029176401925f5610aab616a49f7ab5865d7b9f821e34d68`

```dockerfile
```

-	Layers:
	-	`sha256:bd85d26cc1109c5f2e6fe090da692b159c64ab4e14566155f5f52dcd3724ecdc`  
		Last Modified: Tue, 17 Mar 2026 04:17:48 GMT  
		Size: 58.8 MB (58784514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f7cddda71556b4e7bd904db4a95cf58dd6a12c54b14fbc251193b4e57c2371`  
		Last Modified: Tue, 17 Mar 2026 04:17:43 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
