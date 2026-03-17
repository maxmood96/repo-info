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
