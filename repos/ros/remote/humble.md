## `ros:humble`

```console
$ docker pull ros@sha256:9d1c63dad6848296ca0b341f1a72969c974a8052c9825686df358b36c746a164
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:8cc9c13a1aa12c6412c36b1ed838ce0da9034d1e78a04c590d44b7960282c003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262727783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4707f14b469456d2eaf74b17304a6d3e725ca5ec18fbbfeae8cd5cbd2f0630`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76b938bd7208ed5b0eaf7eefe1ae75db592dc2af1a0dc7f1121d43ea3ef16c1`  
		Last Modified: Tue, 03 Jun 2025 13:32:42 GMT  
		Size: 1.2 MB (1214046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e6b18c4447038135f63984efc97b8842e418685dad2282de87c44c48ce44e`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 3.6 MB (3625823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d771cf9dca927f4be9e036769022665873df4fd6fa780bc8163b714c8c68805`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcad84484813c07387f81500606d7843b0eecb7541913bb03acc91b161c7a39c`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465ddcc433f506333cf3b5c4607f2953f2530a9c3166172cd6c61e26fdd90802`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 106.7 MB (106741362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c69a09fd660cffda2e05b1ab7ba3c202d17a35be834c48c0bb4cb2269494343`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1366c775a6afee125db0240ba46a1b496944d8bffdac140657290439cb7f23`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 98.0 MB (97953334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dde60de9f6eb26f19f6dc5856b7ab5af91825d8d948c17d4721a41c2d011d4`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 362.1 KB (362147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1691a8c998bd5fbe5b858f792b7c47b5c449d93e878a1e6a3618e8b9b147fc2`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ae0d38eb04d9de1030ad529c255dcadb83988730f005b3afbdfd33e362fd57`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 23.3 MB (23292613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:bb8915eb3f1b7dea6e9e67c11e7bae24f44b092ecdadbacb2878d4502ad421d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2f3da5c5cc3bfb090086a121d0b72bff7acbd732517f63ad8bfac9c35b6f5c`

```dockerfile
```

-	Layers:
	-	`sha256:67beeb7ab8b8237f50d638e46f80f545e8a13a7de8bef820eba2d6bcdfcd29fb`  
		Last Modified: Tue, 03 Jun 2025 15:02:23 GMT  
		Size: 23.0 MB (23002945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a529ad4880fb3f5124757c8f9891ecd8d9aacdf2a0fd36318d01d7198d06b6`  
		Last Modified: Tue, 03 Jun 2025 15:02:24 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f670430789b9da694145f3b612623d92770fa57e41332bda4ad37485fe443036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255166380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8e5249921014ad6a048e05c4fbe9ceb085e762300219f8d9a1baac305d35b7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7825d6a3f468116a5beb6ccde15d08c8df7fc2b9f4a7050d39cb6c58954659bd`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 3.6 MB (3597269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bfa47600c8c6c6315086fe7b03d9757f0c6b53c056982a8c21a8238b78ec6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a0081f9ea8bc09c1f9324e3d1d0d91d6168740026cc682e27d4f26edf88fcf`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b295fd493b04d6d16baa7f115479270e6159b8e59b7a1fae5f4cf47a2113f7`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 104.4 MB (104445028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c1eb068b65b787000d855e05b64943493a6bae300738c60a274069df0fdaed`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01bd41ffa6d061e4744811f39190575d9b017e2cd8a90339a6404e13e27a7b`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 95.5 MB (95505979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c25052a32652577502f300c765a757515ea4fc8aa41c46ef557d4c1f0198acc`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 362.1 KB (362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e52f4a3b9656efc3b3c635f54ffa71e42f27ee2e730489af1427982a9d92b97`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce85f432dfa5e7b15cc23831296653d9077a1f0f49fde5a2357c4597ebf3b2a`  
		Last Modified: Tue, 03 Jun 2025 13:30:32 GMT  
		Size: 22.7 MB (22680677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:4437fd1503234d397efd453f9e7687fa08b1dc8b8da7c4d87326fc7a568e4167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23033254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b4ebf0c6fa671cfc81085e9a470a143a1b8c21497ff55b2310ed1af51b226b`

```dockerfile
```

-	Layers:
	-	`sha256:dd6ab7ff434b3afbf587e67f6562d1ff9407c29f26a3ef665a0cc9d6179fc6f9`  
		Last Modified: Tue, 03 Jun 2025 15:02:42 GMT  
		Size: 23.0 MB (23015961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e7e6288d0c62cbf9adff834b3dc8bbb72a9f03dc5c02e4f823eba6365f98d2`  
		Last Modified: Tue, 03 Jun 2025 15:02:43 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json
