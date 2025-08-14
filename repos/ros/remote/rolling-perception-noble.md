## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:69d7b4634d7c0425b196bd3d6be0cc02802e616d01f3bac5cc9cce97eed451dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:f05df60ef5a28b08225b14a5f13c240d0bccaaf23a831450eb19f9d3aa9878c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092342870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5107a80b06877ee9daacb7e5404c89a659d047cf83e41faa72ddef909ac48a14`
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
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:34c34a9b39e8da081156d583ced605827f1ce52353cff35815eeda7b6558fd07`  
		Last Modified: Wed, 13 Aug 2025 22:45:12 GMT  
		Size: 782.0 MB (781950238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c59f94f5b717fa64e40440b7ed7af5702f7c861b0b71f135fb7e3b7207a56536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60694023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c873642fa477e9df908eb69f14d0c36a13289a3fc606baa763073d7a9ab82c58`

```dockerfile
```

-	Layers:
	-	`sha256:edcc370416e91dc78deddc0c07b43196e13fb80f1f4860e98d684ea06fa78b6c`  
		Last Modified: Tue, 12 Aug 2025 19:18:38 GMT  
		Size: 60.7 MB (60684619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa2ab1ff09dad2b2a3612959d5a416f2b3dea3c3fd0e1e724711942a2d845071`  
		Last Modified: Tue, 12 Aug 2025 19:18:40 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2a623e4887bbf62a9ada2682daed35f1213a59a35ddd2a0bf0add9c5886adff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.7 MB (990672625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dccaaf895490f88c19603ce89a70cf52cb81554ae7cc6927b381e1648ba46c`
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
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c2b649fd9dbfaa4be9c1386063009d6f1a8f66436f96c6cfd42da82fb193fb47`  
		Last Modified: Wed, 13 Aug 2025 13:27:12 GMT  
		Size: 691.9 MB (691918185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:91db2e11bde7c575e42557de8f8d54d6105edb4e872fca0bd76cd9a14ca263e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d053564e921a0365eb724612464c10b07684210ea83c4d56fe3daeedc092a1`

```dockerfile
```

-	Layers:
	-	`sha256:51907083263b80f6e8a86b3961e82283544c8c9b3cde9ea878eabdf4ac70951a`  
		Last Modified: Wed, 13 Aug 2025 13:19:36 GMT  
		Size: 60.6 MB (60615143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5999f16eba963ddd9bd11ee7dec3814c7f8afbe5aaafaa205155c5556123f3`  
		Last Modified: Wed, 13 Aug 2025 13:19:37 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json
