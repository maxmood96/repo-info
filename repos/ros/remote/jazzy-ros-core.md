## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:ac144e294be0f59216c87e91e1dcf3924bfba6be77cd20a903a1f9c381029fb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e95cd08316c3edcdddb24118520cdce67edeac83ee7e403ed63ff90d0a0c9e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157339442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a791e9737e1dcb1c008632170507b55e84e7bc04bbf418b55562438c59b2c4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad268d3577575b8a090cd6e684e1bfe2743e4ff225fd68d59f6cc8d1311efc1`  
		Last Modified: Tue, 02 Sep 2025 00:13:52 GMT  
		Size: 683.8 KB (683827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8905021a0e9d1029ab7dd7f84415090e39e65ca21a7df47ef3c9979f86d6f8a`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 6.7 MB (6746681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b374353b323cb503e72f9217993e9545747c2635f474858cf301ab4eb3dc7e2`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 94.1 KB (94067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948960a889906032c1cfe6c7576e66036370fc2303edc1886125832bb4feb838`  
		Last Modified: Tue, 02 Sep 2025 00:23:50 GMT  
		Size: 120.1 MB (120091608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2cb1a3fd6fea1facb4eefd901cc55e8b4e196e5ece372ee5fbe3602870e7c`  
		Last Modified: Tue, 02 Sep 2025 00:13:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:41ad83544f53e0ca0e68cfb8f32cf79cacdbdf01c0412b3bb87a1bb81b788709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18314534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15caa1c5bacf8e6622515bb2599f6a7378bf675a0b5d176f869e682227fbf42`

```dockerfile
```

-	Layers:
	-	`sha256:4444fae313851bbc6e61b013c47f2efb317c2e0b0fb0a868433999a4049d800c`  
		Last Modified: Tue, 02 Sep 2025 01:17:38 GMT  
		Size: 18.3 MB (18299891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73e9d1f35d06bd10aa9d79ead34659cdb324b7b69f895f5a3154ad42db8507c`  
		Last Modified: Tue, 02 Sep 2025 01:17:40 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ac8eb3cc381493bb29f24b5739388ff79ae38e4424f0e7ab5edfba69f389e8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151275251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb8fcf79ae794d1338cbe3735e480a34627167f7d388bd54884ef23250f093f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a1aeeb021ff56f6549713871ea035936891c67787fb388f08e69e57ccaa5f2`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ffa2a8671f1746a19c7af89127b62a1f22836df01caa93a61d61b0d2574661`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 6.8 MB (6759788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a01a08d6a7cb15e63953b7781299b8e80e32583b1030aa55d13094df1d2d7`  
		Last Modified: Tue, 02 Sep 2025 02:55:38 GMT  
		Size: 94.2 KB (94161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4efba9b395ff1f9acecfa58641bb667b903285e0ef042738741ad9d8159dee`  
		Last Modified: Tue, 02 Sep 2025 02:55:47 GMT  
		Size: 114.9 MB (114876950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fdfdfe0ba6ec7783a4b4e7f923dd952363d4366df0d404978067fee5587ee6`  
		Last Modified: Tue, 02 Sep 2025 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:cabab05c2926774b83a01085d3c7f1114dee13967a673390257357b677752395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18288665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a03fa8b4140fa3bf7a28e3b639edb4174446ad7725157c19d43835697719f2c`

```dockerfile
```

-	Layers:
	-	`sha256:71241c8d0f742618b738faf7014e6bdddf2100ecd76d81ced99ed18ea8d33ff4`  
		Last Modified: Tue, 02 Sep 2025 04:18:03 GMT  
		Size: 18.3 MB (18273897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ba98c50dbf222fdf1aaeb2242fc9042d06b35dfd887e5a814610c5c10525e9`  
		Last Modified: Tue, 02 Sep 2025 04:18:04 GMT  
		Size: 14.8 KB (14768 bytes)  
		MIME: application/vnd.in-toto+json
