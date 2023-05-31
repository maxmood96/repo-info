## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:fceffafd11fa99593f5db42dd7a1cc71340c470c8a5dc91faee05d678ba0beeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e4a0b8de43eaee8ee1082866770a9f8e881ff8360c5cf4aecd41aa5fcf143bca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161892712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9c4a7224a595097733c7cf81bfbdeef3d29f17ddb706341998c7258db81f41`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 21:45:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:45:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:45:39 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 03 May 2023 21:45:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 May 2023 21:45:41 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 21:45:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 17:25:50 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 17:29:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 May 2023 17:29:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 31 May 2023 17:29:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 17:29:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d709c34b032e9c25f3ef7dbc9cc5be0ab87d014082e04d1f4a5d20e2970446b`  
		Last Modified: Wed, 03 May 2023 22:04:52 GMT  
		Size: 1.2 MB (1239802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58a8c29b4dfa9054fe01f5590245b9ad2e27c309027d00b628451f55bfde59c`  
		Last Modified: Wed, 03 May 2023 22:04:50 GMT  
		Size: 3.8 MB (3828401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707c946d99b6f2ae4da84c6c0af0b3204f17c5371e0ef1e1968fc20d3c812123`  
		Last Modified: Wed, 03 May 2023 22:04:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89451566146a587c0f7bde9c5bd208af5e73072fa556ff6ad6ac85c213406cb6`  
		Last Modified: Wed, 03 May 2023 22:04:49 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56b0611d6c6c3e22e553e0042ab39e3ed4b4214dc9230412e22704fba3d9fe5`  
		Last Modified: Wed, 31 May 2023 17:50:04 GMT  
		Size: 126.4 MB (126391882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70f0a0b21eca468b4344a7f6723cb2517bc5498bcacc3f6471b4399c426c23`  
		Last Modified: Wed, 31 May 2023 17:49:45 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4f8ac7da579ec9e890290c7789b17c0c6c34dfeee92458d25a2bef03c97f15d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157135443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5974e60c0b8aa9da210a9dced83766f8dd63878ca4c758bbf7f884d2971c193`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 18:40:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:40:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:40:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 03 May 2023 18:40:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 May 2023 18:40:43 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 18:40:44 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 18:41:21 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 18:43:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 31 May 2023 18:43:52 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 31 May 2023 18:43:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 18:43:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe39e5ef2f67d96ada5275fbc781d159428991d033cbee5a50e0b5b94ed1764`  
		Last Modified: Wed, 03 May 2023 19:01:25 GMT  
		Size: 1.2 MB (1240441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5271495fcffa1108252b6f2555e695bf0ad66a1468909a8461002e1a31a1c23b`  
		Last Modified: Wed, 03 May 2023 19:01:23 GMT  
		Size: 3.8 MB (3800745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e07c8e039094a3d58f02821bc3eff246bf32f8fb86ff03c65a9bde2bb7ab1`  
		Last Modified: Wed, 03 May 2023 19:01:22 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb152ff223d153fa6d0817fe489190d70fcb6dd9df7b5d1a7163ac27e0fb090`  
		Last Modified: Wed, 03 May 2023 19:01:22 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d351d5ea1b8591a747a00967847e2bace2612b889c6a34c01f99253824234`  
		Last Modified: Wed, 31 May 2023 19:00:50 GMT  
		Size: 123.7 MB (123702404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224c08e904b58619c7d3c3e7783425b7fb5faf629f9b9a064c85e74a401f77b6`  
		Last Modified: Wed, 31 May 2023 19:00:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
