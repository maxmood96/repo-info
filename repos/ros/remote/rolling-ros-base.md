## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:71467108f94c59643e784908dfa53b238a0f9816952648513e4109acaab82f41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:8ecf336bc5e823d5b02f03ad44131d43e07400718432dff20118bccc10dabe20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308111698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f821cc6d142fe25acd62e71ff4592f74337ca046a4ed8b5b000bd37ee7341c8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29647462da8b7248faa562686afd7d3260fe5f9ebcad7199b3fc188188ec2cb6`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 683.8 KB (683831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8cf1676bf842067dd91d4304cd9e00b68f99f9e3fdbb5aaf3bfbd7f42b6bdd`  
		Last Modified: Tue, 10 Jun 2025 17:40:51 GMT  
		Size: 6.7 MB (6745430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a2963d62bf807e13e004c105aaff40d7c2b5bf0ec34a98c73b58948b204ebf`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 94.0 KB (94036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086be9840220e0654dbe8ca646f01473644e65977961a84a0d7fd5ef2163ff7c`  
		Last Modified: Tue, 10 Jun 2025 17:43:16 GMT  
		Size: 132.3 MB (132309948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15678d18204d5f60c2a8207755206c234b0e17d078a20bf91a9d36d9cde82f4`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedfb4bf8b8e902565ca4bf76bd01fbd97589a22c2575b1a0bf2ce1556469bd4`  
		Last Modified: Tue, 10 Jun 2025 18:07:59 GMT  
		Size: 110.2 MB (110181766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590c8430593334b1f6946c46594eeb49e569c4926cc781b2fdcd1953e74a0901`  
		Last Modified: Tue, 10 Jun 2025 17:54:24 GMT  
		Size: 345.2 KB (345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778a971a98427a1b752d46f529f10ee0f7205bba5c70472f2cdc2497640cb32`  
		Last Modified: Tue, 10 Jun 2025 17:54:28 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a12a756a3ec6476a14b345873c04ca4092bad41b026c1645cb18909376affe7`  
		Last Modified: Tue, 10 Jun 2025 18:07:57 GMT  
		Size: 28.0 MB (28033477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:21de65aa82619907580ed7b48e5c0e04be26009c3a2f120173cceb634237f981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24539932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f30173422c557e85fc5f3a9439c736a008811671d24b770a517d13d523297ef`

```dockerfile
```

-	Layers:
	-	`sha256:b23274f049278016b8ea12831dc81a7695d25589e25dbf2505dcf4402d484257`  
		Last Modified: Tue, 10 Jun 2025 19:17:35 GMT  
		Size: 24.5 MB (24523524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868a8f818db8271c59f7a0446cb4dd27d641ce8ee126ffbef9c5d185c7de7015`  
		Last Modified: Tue, 10 Jun 2025 19:17:36 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bf4caadd7eea9a8926c5546902344c59e883dc47859c103fd2bec0d2f060f0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296453696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7d4ff7af311d586876215b87c1f87589cd73021e4b114170b2058d66081fb7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f46fee428ca8064da8e42ab2a83edde8864b2387c92ad4288a4f0a8f4dea7b0d`  
		Last Modified: Tue, 10 Jun 2025 18:23:31 GMT  
		Size: 127.0 MB (126997135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c56dbcf3bcee78c66e7611653fffffc90f5c02e8a46764509d6a4168c73778`  
		Last Modified: Tue, 10 Jun 2025 18:23:16 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fae5e91ffe6d48fa6890f1367c170da0c10e901ec4337a30791a899b68a883`  
		Last Modified: Tue, 10 Jun 2025 18:45:36 GMT  
		Size: 105.6 MB (105596040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f565bdcba0c35ecd1cd3d834fbcb8a96e7f87e42d22d85cc01708bea55ed5dc6`  
		Last Modified: Tue, 10 Jun 2025 18:45:28 GMT  
		Size: 345.2 KB (345208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8718eda1d80b4639b71439e318296b002a6b947659a62c101ef0700615df21c`  
		Last Modified: Tue, 10 Jun 2025 18:45:28 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633c9dcdacf75d6cc0ef05e66749bc40bc374e58679978adc043c1b7e1a8e57e`  
		Last Modified: Tue, 10 Jun 2025 18:45:31 GMT  
		Size: 27.1 MB (27123509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:7d1a37a49879ceae1d1fa6c0c09e2bdb7ad5a62099767bcb874a84d49c0506db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24562330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74bf7dca688d1859e574c9cfb05dc88a29389bf0b4c90647a495c1fc1d73bdd`

```dockerfile
```

-	Layers:
	-	`sha256:b5482aad171d09c918c0aefa3a6197182010577ec51990f8778bf441735a2180`  
		Last Modified: Tue, 10 Jun 2025 19:17:56 GMT  
		Size: 24.5 MB (24545785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9615559a7af261ba562363b965361e9d06a309632d9225a6d7a06710b28eb62d`  
		Last Modified: Tue, 10 Jun 2025 19:17:58 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json
