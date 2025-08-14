## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:473121e01e2c1b3b4dd2dd168a6504ed4eae3d7c92efc03a250738caf55bfc76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d858af25b06dabbe214f1eba28d5fdf3ee86e6cd647839d4c65878e82724e8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310392632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69110c2cab624698144b3dc8649592dffae7d9a7654b6d768c7ddf8afd0f4d23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
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
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a17f0f86a2431d05dd4a34c4fbbb4a747dac4bab4254879d078c1818831e92`  
		Last Modified: Tue, 12 Aug 2025 17:56:22 GMT  
		Size: 683.8 KB (683793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b6cb66428e1fc775159e5edbb6bc37577692d3146da60691abf4b6995bf129`  
		Last Modified: Tue, 12 Aug 2025 17:56:24 GMT  
		Size: 6.7 MB (6746722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfbde8ebb1c8cf11a7732b7f094815b9fbc6ec05d7da1c933280ca5fd5698d3`  
		Last Modified: Tue, 12 Aug 2025 17:56:22 GMT  
		Size: 94.1 KB (94061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f982a2a875c7ba22c0fc2f9c1c78302d3284fd5d41329559bcb0b331e9a43574`  
		Last Modified: Tue, 12 Aug 2025 17:56:37 GMT  
		Size: 134.6 MB (134566972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2dfdd713c9a04516e171d12b8eaa8565ddc6cad986964b024703db97ec4afc`  
		Last Modified: Tue, 12 Aug 2025 17:56:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558d18df77b53ed70131eccce44dc01529436cbe76de2b4731bf9a5ec8168f3`  
		Last Modified: Tue, 12 Aug 2025 18:08:05 GMT  
		Size: 110.2 MB (110184580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2ac44e3ee34cf94151277cfed4ab78c26593051570d40b692281524a0a1b20`  
		Last Modified: Tue, 12 Aug 2025 18:07:45 GMT  
		Size: 352.4 KB (352437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37200875dd0cf3baefc89cc65ecd10b3968d75042fbcf5751b63f54e584c9a7e`  
		Last Modified: Tue, 12 Aug 2025 18:07:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e3b740a5bd3e38fa3da9cdcf9c822467c288faef093b37867c8baf5989ca36`  
		Last Modified: Tue, 12 Aug 2025 18:07:49 GMT  
		Size: 28.0 MB (28038206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:abd2056765c580d42517afbca7cd1db1adcfeeb6110f89169e58bb31dcf40090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24534894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de83bfecd96c3a796df36a7a1f90d9e2e8d5a8261364b4f585c0e6a63af70be`

```dockerfile
```

-	Layers:
	-	`sha256:16b142741d17579e29c8cc2e7c87ac6c647f8cdd969341840da2705a57d0f94f`  
		Last Modified: Tue, 12 Aug 2025 19:18:33 GMT  
		Size: 24.5 MB (24518486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb2a82ca1f5491f9edcd8fbb8fc4335d2fc44f370625b1750b4d72b8e0101b6b`  
		Last Modified: Tue, 12 Aug 2025 19:18:34 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:91f49d3943b8f5a73e4adfd58870afec88276191f1fd49a7a8289f3ca297b53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298754440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d3fe33da31f1eaaa4d7ce0ff071020a9efa6fe67a48d91a2d1628f51dd25f7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 10 Jun 2025 04:58:20 GMT
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
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4fca2469212f7c463fa14e87fe769d2a219fecf58125d538219a566e9b9ec9`  
		Last Modified: Tue, 12 Aug 2025 21:07:03 GMT  
		Size: 684.0 KB (683970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8101d7e467e40dcfb7a696c7d00d28a9434914ea87bae800f81106c8e471f29e`  
		Last Modified: Tue, 12 Aug 2025 21:07:03 GMT  
		Size: 6.8 MB (6759892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883862c530c4be898d18cd02b3b2123fa8a5ea159a5132eca0eef18580a0faa5`  
		Last Modified: Tue, 12 Aug 2025 21:07:02 GMT  
		Size: 94.2 KB (94211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d194f3a8bc2607370aa62995f0b184b133e317282e29af806497ef043c0a13d6`  
		Last Modified: Wed, 13 Aug 2025 03:32:57 GMT  
		Size: 129.3 MB (129288135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5e11a61da7887a347f196979a7b818f7d26d60ce957fe1491c32525fb607df`  
		Last Modified: Tue, 12 Aug 2025 21:10:12 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b174b07e4fd82c1ed915d1c09be6c2e0d68b3f2e56f8086bd40cfe7db6e8ddf`  
		Last Modified: Wed, 13 Aug 2025 00:15:10 GMT  
		Size: 105.6 MB (105593476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edd2563a26e5f677ea8ee2fe2f5e4b7f6045083eeae9823b9f9896cb6cc3cb7`  
		Last Modified: Wed, 13 Aug 2025 00:15:00 GMT  
		Size: 352.4 KB (352436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e8d5b7bd6c7ce007dabd35e360e1bacf2df3ca6857316041805234527a9ccd`  
		Last Modified: Wed, 13 Aug 2025 00:15:00 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5edbfa648ef62a2c40305c41c70cdedb50659862a1b93e3511ad89b05c40178`  
		Last Modified: Wed, 13 Aug 2025 00:15:02 GMT  
		Size: 27.1 MB (27119279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:a2585c6511f51d96a5fe4dd299debb4972d3be2453c7ff2752c7925317b632e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24557290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210cf8245fa15173b6d3084aae69c614201f7cef1cd8aa7e665562f9d2e02f0a`

```dockerfile
```

-	Layers:
	-	`sha256:abb4543798ad3d97c4b6bd70260846d1b39cffbb476d86d812056655d6a57f0f`  
		Last Modified: Wed, 13 Aug 2025 01:18:08 GMT  
		Size: 24.5 MB (24540746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d7b6e2b0b0aa4d2b28c2e944ca2e02df71f59281eef2f49271dd55844ffc37`  
		Last Modified: Wed, 13 Aug 2025 01:18:09 GMT  
		Size: 16.5 KB (16544 bytes)  
		MIME: application/vnd.in-toto+json
