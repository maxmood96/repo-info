## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:22c43c0ae043ef89c72f6f3228924221f6cd356e08c196fa14264abda6a49137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:f3c6f5c0b3b2d6aef9b44d6c4334847dcb014aa578b05012476220a5bca0def2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172346463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1d6dd5376df1f7b6389f6b351972d34efc4a74efbb3de675b21dfebd846a65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:59 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:40 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:28:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ca7acf7841f558108ce9a5dd706711d2aac1bbeafcbfcc3595ea409f1af`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 684.1 KB (684115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb08429f10cde91ba9d6efcd40a3128318fd36e1c54446047006101444152b`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 6.8 MB (6751868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922e3c3105cd5fc48317ad03a86ad31e5e771049e40cdb997f056a6ebaf80828`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 94.3 KB (94270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b130472c2ddda6ec9ee73684e3950b34a37a46cda5dd70fa961e767e43d5f`  
		Last Modified: Tue, 07 Apr 2026 02:29:15 GMT  
		Size: 135.1 MB (135082556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49950df5229690d297a4fff95b7786781a0aaa782fed19c78dfbd7388762455e`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1b96ecb8416ed40d535d13a6eebe2dee3176928cd83be7c8e726ee0d6f912d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19431994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db31f2f92304481c917c1cc4669c2d3141ff051858ad5b3f3ad671475dacbd9c`

```dockerfile
```

-	Layers:
	-	`sha256:38d8b4a091c49852cccc107d94726f979393da8891bb832abf819ce795a917e3`  
		Last Modified: Tue, 07 Apr 2026 02:29:13 GMT  
		Size: 19.4 MB (19417372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20512c1e7bd56f1a4f6342e576938573513f237f45904fc85ec4c06943f0ffca`  
		Last Modified: Tue, 07 Apr 2026 02:29:12 GMT  
		Size: 14.6 KB (14622 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2d381eddfb4f845059f26be1f39ff84a8efda8a7ffd1e6f8ff56984eeada6af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165837981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa54c30092cbba01cad3de9b74a2e50b9054e6b8fb6ad1c00a26ed1022dcfdd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:34:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:36 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 07 Apr 2026 02:35:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3315ad3221dce8431ae9ca0e6dd11a472c6a47538732d0d825f0acd2dba9b4`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 684.2 KB (684205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e747992a39814d1da3be26382edd5d47af1b5e7217c73c161cdbc90463d88`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 6.8 MB (6765039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0b80e5bd1fd7cfbd373d23c999c7d3b25a286a16f06933678a8b749f4ddbb1`  
		Last Modified: Tue, 07 Apr 2026 02:35:56 GMT  
		Size: 94.3 KB (94323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd664a49b8a1a34a7176fb8f11d133ca6dd76d086affcab10b027e9de99d6dc`  
		Last Modified: Tue, 07 Apr 2026 02:36:06 GMT  
		Size: 129.4 MB (129420142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23b6c82deb556349d7aefe79a579d796b6ca69e07db9ca0bf9607a836b6775`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ba5eff58741065d750dd1412e6dc1a5340831452f7bfeb84929235d77114ad74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19406327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d14d57199743b390b3db2691756e04d3b7a2a22bbefceabce203abe2eae7d0`

```dockerfile
```

-	Layers:
	-	`sha256:182afa8fa2196e632f5e179bee4ea8b72c9d44ccbdb7f40c9e3bb9427e1427a3`  
		Last Modified: Tue, 07 Apr 2026 02:35:58 GMT  
		Size: 19.4 MB (19391581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19de5763163292cba089dd297d9bdf02c1b42b41bc6ac90511347a58e564b8c`  
		Last Modified: Tue, 07 Apr 2026 02:35:57 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json
