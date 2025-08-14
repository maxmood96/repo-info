## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:e6728b9ece72f383a3f573ac42ab3df9f197d7784d4b9260ac5933b62373bc7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1ddcb749207d9390c205e372543d800ae3bd8351182bfad77f15b6cdff076a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141424966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ffc2601d2f392c4290ece2828e7acbe10049e8859d9ca7045ec5eef3bf3298`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b660084749371d069f921040a4fd644dd612af0b6c49a62da486ab5570ab3`  
		Last Modified: Tue, 12 Aug 2025 17:56:33 GMT  
		Size: 1.2 MB (1214020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146caa6e438614ec1a4691e35f239ffdf79e5484472d13d5371f8435eb40c00`  
		Last Modified: Tue, 12 Aug 2025 17:56:31 GMT  
		Size: 6.0 MB (5995314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f16346373fec485486a8a417c01db653ab08c41a8a584599a1dee0a7e97f3c`  
		Last Modified: Tue, 12 Aug 2025 17:56:31 GMT  
		Size: 97.1 KB (97149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ca3259567d61027fb2a9a419ca64c71255a0ae49f3dc2fdd46d1b387ed7950`  
		Last Modified: Tue, 12 Aug 2025 17:56:44 GMT  
		Size: 104.6 MB (104581293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff17287297b63ed8841e34c2306fc84dd688a1f6e692bd2bb16c052e30c24ab1`  
		Last Modified: Tue, 12 Aug 2025 17:56:31 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:af99f89f2fb585f979fbdfe94a22d1ba83cf44dc68f0e62a752958466ff62207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17669274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2980775700d876e2a57fdd07258859a67de3672e1d6193c40170ea564462ff`

```dockerfile
```

-	Layers:
	-	`sha256:b7d209c29b4b6162a496cd033f7936fd18bb1795b5e1d7bb07180b4980207585`  
		Last Modified: Tue, 12 Aug 2025 19:17:32 GMT  
		Size: 17.7 MB (17654617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebd547a577e906a971979362f15ba671632ad369a7e23b268e874eaffc2faba`  
		Last Modified: Tue, 12 Aug 2025 19:17:33 GMT  
		Size: 14.7 KB (14657 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:574915621f8da37130736137dad44f9c4a04d4f3c993e12299a8a5dddb445362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136894331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f671336df5cb03b22e3799e4690af950f874cc52ff2724fec15ad09195959f`
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
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3413538d349f34643db7890061af65431ab5eed6cefd879692cd3c858f9ca2`  
		Last Modified: Tue, 12 Aug 2025 21:04:44 GMT  
		Size: 1.2 MB (1214253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d2273514f7012f909f7c1472d8f5340ed9119a3f46752cad7705f39ca84e31`  
		Last Modified: Tue, 12 Aug 2025 21:04:44 GMT  
		Size: 5.9 MB (5939779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bbe0bfd7eadceb47a12ac0d96fa7b9e08244b0375ff7dba570c85625a176f5`  
		Last Modified: Tue, 12 Aug 2025 21:04:43 GMT  
		Size: 97.3 KB (97300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de148676c2b7a41926a9dd1197c85f396169405dacf02baa600ce8a4ad4a87c3`  
		Last Modified: Tue, 12 Aug 2025 21:04:54 GMT  
		Size: 102.3 MB (102283556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bc3d3b69ae746ff83fe854c8253b45aa7248f9ee7cf73ee8fcd57fe9868871`  
		Last Modified: Tue, 12 Aug 2025 21:04:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:dc7d1b1ca2d47ae73f77882ed70348950badcaa226c3040393c517f75a044c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17655745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651d4a35d15823c6404bd5b1b41d7f948884f762ebcede40cf651e544bd301e4`

```dockerfile
```

-	Layers:
	-	`sha256:5be9bb528977c628b8c1b0d343414667c554bf1bfde9389add1db05b379d748e`  
		Last Modified: Tue, 12 Aug 2025 22:17:33 GMT  
		Size: 17.6 MB (17640966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c462f2c5d9c0876e066c567a268a0dd0c4cf82edbae87f4ff697444ccaa932c`  
		Last Modified: Tue, 12 Aug 2025 22:17:35 GMT  
		Size: 14.8 KB (14779 bytes)  
		MIME: application/vnd.in-toto+json
