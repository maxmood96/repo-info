## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:05af2f7c2f615914a808d3e72c74c119590198f207b9fc4a55f9ae2f1810d6e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:d719d6624830384c299e913517dc1f3ac53ee44fb34cb13dc0e3e5e72b5629aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076313178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012ba2b95052a7e654e7f01271510eccf4129f8f9d61ee680406dd4092047219`
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
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad66aa49d81043255b5a68fe8370c44ed1bb417a34d56921b5b6e54aad5e8d43`  
		Last Modified: Wed, 02 Jul 2025 05:11:35 GMT  
		Size: 110.2 MB (110183478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22750c2ee1c83973e70b463b77f04591f765297af3b530faf78d8f8ed830ff1`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 368.0 KB (367976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63a806b355a8c725520e98243260911eac03cbb661780b860888e786128635`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc65c67c30109fc2ccd6dc11a29c0f2680360d72516f305af61d8dfe881a29`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (27965355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acadc09cb60efa4d4bce02a9f89e9281004c6b71b61d3b0a2dde3b2ea243caa4`  
		Last Modified: Wed, 02 Jul 2025 08:21:39 GMT  
		Size: 780.6 MB (780622469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3c5de313d3bdaadec85ebaaa22768414f6377de6fef7eba3c43c515d263a4937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60684111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73037ae8af05bdebfe68ebd4550991e6b12ff11c8733be00615f92a66138aa97`

```dockerfile
```

-	Layers:
	-	`sha256:4cedc11a742aa7c12e683330f376d5466430bc23f91170239fcfda4ef8760e14`  
		Last Modified: Wed, 02 Jul 2025 07:17:48 GMT  
		Size: 60.7 MB (60674729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8076a3c706cb06872a3dc48318a5869c82127f63e305856f04e7d51d48cbedca`  
		Last Modified: Wed, 02 Jul 2025 07:17:50 GMT  
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
