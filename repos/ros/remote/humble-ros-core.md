## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:5347abc91db332401fa14673fd25fb62dc09ab00997d3474f2239b2ad069e31e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f8d31125691e6812c518e45a40d5d77a5121386e403f4c8dd0f97e873d2982ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141117230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68909db07fd3dc39e8169db2c142713d8dc6e5eba38a14a7839e13e3ce5e6a73`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=humble
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
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

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:bd0ca565fc59c0c1208b26e3f700c6514fa67e53e5a2d5c5c7386c0adc81e039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d10853feccfb70270ad34f70e1eb5d421fc43b7fd69b05dabfbbf6355221`

```dockerfile
```

-	Layers:
	-	`sha256:5a5c125230f6584d09dfd7c10f5844b530953d501c02a7e94e387a08daf3c0fb`  
		Last Modified: Tue, 03 Jun 2025 15:03:32 GMT  
		Size: 17.2 MB (17178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:692fab7bca6366a7f97def51a99777e08e3d56ae668564e84c4838e55f815625`  
		Last Modified: Tue, 03 Jun 2025 15:03:33 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:847f8b03153f6788afc452fb21381a4f4f324a84a364db4608f5e3f082131fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136615077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7490281af90c1b6168ea2a27788739b1d5f41fb48860a9f6658b91f5bec70fb9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=humble
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
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

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:24c707190f42a141fe476a8b07054d02fa6182cf0eb74be690d04db08eb0f042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17181749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2afd51ddbc6fd2da98c6ce5b696a86e691aa21d5cb90098fa14f169c7cc116`

```dockerfile
```

-	Layers:
	-	`sha256:e56880343aa1b076b6efc3c98478d22c9cd7b199a6032625944347b3ffb1fd64`  
		Last Modified: Tue, 03 Jun 2025 15:03:34 GMT  
		Size: 17.2 MB (17165218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e91c7c7e8aa97357ceddc670cb2c2202e7366c3bfb91fb298b7f0840652a4fa`  
		Last Modified: Tue, 03 Jun 2025 15:03:35 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json
