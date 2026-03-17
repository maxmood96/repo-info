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
