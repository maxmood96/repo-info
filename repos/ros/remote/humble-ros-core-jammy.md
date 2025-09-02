## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:96e7c973f3040ba5cefd5e811e38f4601f27031ee988bf9bec3f187ba33c1850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:fd55de2d01e47736c2da6642ba6f9646e1c8a0cbf18155dd227864e030823a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141434133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11a4f706454ccb2d77974fce401f7530fafac260a72748aa0e6feaf5f146888`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4205dd24072fa6c493e735b2530ed8c82d47cbce110866bfba44553e9c4ff6`  
		Last Modified: Tue, 02 Sep 2025 00:14:01 GMT  
		Size: 1.2 MB (1213974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2705f0adc4adce62066a1177a7e58cebab9068990c3a4ab2f7291a1c70afc11`  
		Last Modified: Tue, 02 Sep 2025 00:14:01 GMT  
		Size: 6.0 MB (5995240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba91d05e8ff7416d5bb177525057440404b9a1c4bdd77f7549d7f7da6f6c014`  
		Last Modified: Tue, 02 Sep 2025 00:14:01 GMT  
		Size: 97.2 KB (97173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e756fe699fedf8270691740b6f43d00359cec0bebe067e5b98c8872cbd8fd0e0`  
		Last Modified: Tue, 02 Sep 2025 00:14:13 GMT  
		Size: 104.6 MB (104590615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a886e9df23356de168fcfac31a587b1c0a6e9e6f85e9348f2f06959e818123`  
		Last Modified: Mon, 01 Sep 2025 23:41:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e2130972343945919bc34b40849b8f1cdc7fb1cdc3e9a8bca4cd3dda49e07ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17669302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c198e1d69cfc0dd3427d46f8584e05a5388a3355eae8eb9e5c6bafc0e2871753`

```dockerfile
```

-	Layers:
	-	`sha256:ea634d6f0dffbabfddbc29c152d4c121fc6c594979bf22d812998f4e61c2ce6c`  
		Last Modified: Tue, 02 Sep 2025 01:17:23 GMT  
		Size: 17.7 MB (17654645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f231fa30ac2ef8ea403bee2fede924f717caa910d3caac705fb74d308721c6`  
		Last Modified: Tue, 02 Sep 2025 01:17:24 GMT  
		Size: 14.7 KB (14657 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

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

### `ros:humble-ros-core-jammy` - unknown; unknown

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
