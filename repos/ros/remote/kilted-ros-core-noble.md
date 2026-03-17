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
