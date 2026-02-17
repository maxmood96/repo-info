## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:90a7231938e53e367080f47c9ce6a3fb3e7e8a5c02eb64e5f4f9cb615eae4801
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:716004ebca998e69176b8c2f6c399320e452cac8144b5f03e13eb12cea2cb9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173372512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17a5c05fc884214d502b2048f1a86b8504d233c5b1bc1d4f1f171fde2158614`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:60f41e275d1480fa60827ad6386e173c23e666a2fbf650abdcc115b6572a5efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19415119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dba9d087660dd3f9b505be497048d6f29b0fcda8bcad68dc7327955773c3de7`

```dockerfile
```

-	Layers:
	-	`sha256:caeddb8e57cc56e0080db6c3aa098ecdeddc992332f965223590a8ac42fc14af`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 19.4 MB (19400498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f411a45a2d55c6121d3858126942fc12db430ab74262b3b35f1a04b2c41119d`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:26c36bae9cf9c9576fa8f4e10cbba12fca9dd921b4300745875b770e4d3efd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166799503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b596d417c1846bdb71037d2b4b533197845800ee50318d1ddff0e2df78c111`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7c6c8e2197c18e7e40ac3fbada7b38bc28e86725c789738e2b4592d820853c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19389449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3325a8af056f02534bf06ab7b41cad8c585df26b869af0196236dab648cf940d`

```dockerfile
```

-	Layers:
	-	`sha256:1a782685011acb4d3409906f1a6f6c4b4cfed78eaea29a4bcb4044c988ab14f9`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 19.4 MB (19374702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8007784bbce4ff567142be2f49680b9e157ee1534c04bd1f3961cb4bc946d87d`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json
