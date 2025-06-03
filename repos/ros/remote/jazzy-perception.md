## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:2cf1d3940a8fafb123bce354840517cc73bc7ae9795fe7131a503db5c4f2093e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:de4ebe99b08d3836e4a7e321e87411e80b3fbcd1b9879eca6235612ca67aa023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076264209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8e0f8fe6cbadc57a21c094776551e44d396237427c619318da9bb4a874d44c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d996ba9b4edd88c0a1218a4f6b9e82aacbb4cd9c0f44a02d8052de578268d1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:50 GMT  
		Size: 110.2 MB (110179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6c6b25ec0196eb5046ea65df46a24cb5bb13006dc63bca159185fe044eb30`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 365.5 KB (365545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b1a661f69478625db6adb1761fd8f1ccec92717bd44cdfe2b5a06e75f2cb0`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6de655debbb5b7b335e7467749f8aa7e61315197004beb93d7c89b07a9182`  
		Last Modified: Tue, 03 Jun 2025 17:09:38 GMT  
		Size: 28.0 MB (27966270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc50a40fa49ed9f01a972f677ffc41239589ee12e26ac82438ec6776413bd0be`  
		Last Modified: Tue, 03 Jun 2025 20:48:37 GMT  
		Size: 780.6 MB (780603091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:046c9623e5a1ada62ef847141175908f40a41bbb10df5a3f534247f2f55f28dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59868003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363c178ce11ed3d567777710375cf323eb90e1c995775c269ac7454b31a1b762`

```dockerfile
```

-	Layers:
	-	`sha256:264afef4a45c0400b42039ad16568af9575bd48bb40dc45646643447ecb7ff39`  
		Last Modified: Tue, 03 Jun 2025 19:18:00 GMT  
		Size: 59.9 MB (59858621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc14dca7e3197f1ab997206b3a2f54c0bc10eab982be8c9a21505a5d9b084164`  
		Last Modified: Tue, 03 Jun 2025 19:18:02 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e382657e8307c3d96ef26fd8f6b278b32f1a8160e084a29c463b36566b0dddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.9 MB (974862258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21afb422fc28ebce1ad43d086bfa8dbb8f6f513f21eeb344c87ce9f51b685b05`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc0bf39755013a910d8ad1b32b6f3f9b9312ce259a79006dd3607186145d52`  
		Last Modified: Tue, 03 Jun 2025 17:12:16 GMT  
		Size: 105.6 MB (105593170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94701b4069614f2698aa75959641413e64967923478ef666610963cbac10ccd3`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 365.5 KB (365548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7434caed03c758a0b9a196d1551d0566ab0ec6c0e6bf60c1c9f8781f89c879a`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781027cdaf47969f8306b57e6d33eaaeb74013c708798b7c6c7288103ba9595`  
		Last Modified: Tue, 03 Jun 2025 17:12:09 GMT  
		Size: 27.1 MB (27064676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6faf6b462279f62c4ab4e2b672c45387d260df6ea23126ccf0f58da92114612`  
		Last Modified: Tue, 03 Jun 2025 18:46:16 GMT  
		Size: 690.8 MB (690757788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:998fb887f4c965109b01719f09ffa96c99f22a3d559f263f80b69d0954ff1b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59819748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bf67b1fa8bb527620567e307d01187aa155d113fb732d2533ea49ec34792a5`

```dockerfile
```

-	Layers:
	-	`sha256:f7299e63cbb5c7686bf54574126bd82e9838dfa3dec4502022be42a20a480b2b`  
		Last Modified: Tue, 03 Jun 2025 19:19:40 GMT  
		Size: 59.8 MB (59810286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c97c55beb3763c67f17e5496d8a87af2fa407a4de9c18dc557cf1240fd951af`  
		Last Modified: Tue, 03 Jun 2025 19:19:42 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
