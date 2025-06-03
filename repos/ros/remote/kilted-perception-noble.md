## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:ca1add8668b7f3619328affff18c72a6160cde1d85241c51436dae77e293f8eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:546aac0eeffa0943f6912c23af0efa62ad7b187a3d01ab71ab7b8a38faa60275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089277886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b14c24431435142b8cf4610bb4d438cb9241e38ad7f954eec16d40b68dce6f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc922f2ce7df1733459b033fa462a421a0413670300a8b9c5c35ab7b81bc65eb`  
		Last Modified: Tue, 03 Jun 2025 16:19:30 GMT  
		Size: 683.8 KB (683816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01414ea5181d9da01a2e35570eba4ae2e37593bd21d531dfdf78f234660a7b3c`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 6.7 MB (6745536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a09807d31167f2bd782983408d9ff7419d23b415ca575a3c7b3619165ad094`  
		Last Modified: Tue, 03 Jun 2025 16:19:31 GMT  
		Size: 94.0 KB (94039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099b8cd8b60f4a5d2476fd99e6adc027584cdef11cf59f36cc9b81b31e0ebf4`  
		Last Modified: Tue, 03 Jun 2025 17:07:48 GMT  
		Size: 132.4 MB (132407147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402357658db93f168fcdf893f1c237364dea1ba24a8b5536a3c46e931231791`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760e6e89b71699480f8948db367864cbf4a35b90d807163f094494c524c2b1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 110.2 MB (110182872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d239340021c39b9ae17dd1ad6e2bdfa92f900c692b22d4241368481334529`  
		Last Modified: Tue, 03 Jun 2025 17:09:39 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc049f401682dbbb9f894685070e5d9b0cba96536602e5b27d53355e49b7ff07`  
		Last Modified: Tue, 03 Jun 2025 17:09:40 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5aa038c7c32f417f8539341ca0488c6b029047e95884c31aca6a67db8edf6d`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 28.0 MB (28035155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910602e69e66a1c59ee2737ab00fa9a113e8789504b8e425892e10fc3b6a2da8`  
		Last Modified: Tue, 03 Jun 2025 17:54:49 GMT  
		Size: 781.1 MB (781067576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:75e51cf47b3016df9606305344bdbba224b85c7b1f545e0575838a95f8750d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59970890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23a0780f6d3694eee9317b88ce129337339ef6a3549a513b72cc0bfb6eb08f2`

```dockerfile
```

-	Layers:
	-	`sha256:a414c569b6fccc39562dfb526c99ce7f2db815233fd7e9ce5d814f5e4182f37c`  
		Last Modified: Tue, 03 Jun 2025 19:18:31 GMT  
		Size: 60.0 MB (59961495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40fe2cbcfe864c58bba5a3665b351fea005b02bb97d51164b7d83b9c64970ca`  
		Last Modified: Tue, 03 Jun 2025 19:18:33 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3c354eddd9d7ec8ab36f34a4477d0561ad2d833775e4fbfa7f208fc6edf5d3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.8 MB (987847888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86cfacd10f18fc3e9996f657e50e2ad5cda49f495527733cb3ae4012d6e9dc3f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9dfc24d4fa426deae9efc62cbc01e2c3bb6b1c57bb5d84b579c4f9c66cbe7134`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 127.1 MB (127103875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbbfd9589f7267a767b8f6ae79bf51b4c883e0a07f96139115cc4f1275110f`  
		Last Modified: Tue, 03 Jun 2025 16:23:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07caf8524de34d67d57f2d53ff16540c50ffd4a8515c4f8fb920b3a8467d9a0`  
		Last Modified: Tue, 03 Jun 2025 17:13:37 GMT  
		Size: 105.6 MB (105596816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3310082fb526791a2fd6dd8b7db9d9d2d4bedf73089c00d1c00a145b3cabd7fc`  
		Last Modified: Tue, 03 Jun 2025 17:13:30 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b43e885b2baa4a904b1d45c018b239b5e48ea556a2a972f4828509e59adb5`  
		Last Modified: Tue, 03 Jun 2025 17:13:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c526d3858a93fb6548b4e772344dacc787c3418de5ec76d7be75e226cb7783`  
		Last Modified: Tue, 03 Jun 2025 17:13:32 GMT  
		Size: 27.1 MB (27128379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89f2bcdbfcaa52d114143ced1cfe5056df821a0ecd09b105c9828d99e5d2ce8`  
		Last Modified: Tue, 03 Jun 2025 19:21:00 GMT  
		Size: 691.3 MB (691283291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:454ac3b487aa611233064c701fb45f09e9dedfb901c5137d8cf559ad838f263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59922635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5724da4991e8d76e8566bbc9e4487bcfe4ef768ea4b8791373e2d950562b735a`

```dockerfile
```

-	Layers:
	-	`sha256:e534fc4de8bbb3018d38148f8d77f8871e56d94decd08af90f16170c443541d5`  
		Last Modified: Tue, 03 Jun 2025 19:20:00 GMT  
		Size: 59.9 MB (59913160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a75af4b2c0c88922b34ef647d1824949542ef9782eda38647dba5297011e6110`  
		Last Modified: Tue, 03 Jun 2025 19:20:02 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
