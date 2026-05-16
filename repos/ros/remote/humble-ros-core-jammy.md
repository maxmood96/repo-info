## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:4cbeac7831833f8d6fa4cb1f9f8e22c188853468e76b3d5b9cc58148a8c8f64b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:25eb7f67dc506ea6d0b20607b7d515c2540184659b6e5a953aa32e95c68038ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141910069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5ff2cf0fc3550f6d97992e902daefb312111dcf16adeb40e66760cf0ddd545`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:38 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:12 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2f449b78b8d36897aea1040c6dd78e2b773973b294be524f49e165bfbe125`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 1.2 MB (1215641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac297fbc77e6a50d3a6d12f6e9262ec93242659e840df00ae124230b06fbac9`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 6.0 MB (5994928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930c26f75b5fbc2a66379d9609e3c60712d47fd16ce99fbc72dd04ee8393370`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 97.3 KB (97321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef0c9426369b52a088411a845380681810dac51295fcd84b599778327158e`  
		Last Modified: Fri, 15 May 2026 21:21:41 GMT  
		Size: 104.9 MB (104865299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296fda14f02da11d1ad24cca977186293b353b0009e0aaa7fe7553a281eea6b7`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:1576e00d0d67e3a7786bbc58fada59f494df83d686e728d09e5180f0cc911378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17817518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2260bd209e5895fef62196030eb8c96cf48b1a919b39cc0e7a48d3cc19e0e37`

```dockerfile
```

-	Layers:
	-	`sha256:70821dc7924a8105c6bffa9596291d764662ec8e52b3f7f913970b677c80d3ea`  
		Last Modified: Fri, 15 May 2026 21:21:39 GMT  
		Size: 17.8 MB (17802893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae29c7b239f1a7945f7b2ea0d568f90f19f08835a41254c7cec5b790549637c`  
		Last Modified: Fri, 15 May 2026 21:21:38 GMT  
		Size: 14.6 KB (14625 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1c305dd839535098175c5a74801cb6f46d567bae965d06255c3ecb38948ef9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137488202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da437ad6ced3d4358d1b294160910882d2d48a7d861bce0e59c0cf000cdc4dc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:58 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.jammy_all.deb     && echo "767884cf4ed03116b9d64438930a832ed854147ae435279a7924dfdf60f94433 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 15 May 2026 21:21:38 GMT
ENV ROS_DISTRO=humble
# Fri, 15 May 2026 21:21:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:38 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:21:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 15 May 2026 21:21:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014468f30de87eb3d94e1b88324914631a7cb089f3a169ac1fdf744a3559d160`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 1.2 MB (1215772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aa30806c2ef3e7edf65a7b21cd978099a1d8d1f6acae2bf635a2ce301a0c6`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 5.9 MB (5949306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffd7a28491d8a8dd0417985b138019425d43e2ace5c9df92c5b58f01fd051db`  
		Last Modified: Fri, 15 May 2026 21:22:04 GMT  
		Size: 97.4 KB (97415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b7d15ae4637078cf236f336680a72ee13366378f16c6c4bfcb58d37831bfa`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 102.6 MB (102618891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270eea7f6dffd18476eaf9cdb8a366a0b0f04caf38c5044baf6b36d82d89d68b`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:643646f92a7fc2d126ef0fd296a0fa5fb7ceb0dcf0113c21a44630adafa3f422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17803989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be331f2dffa893dc0153e29beecd1879efa7228d6089406a1c3da7caa6b6cf1`

```dockerfile
```

-	Layers:
	-	`sha256:7cfd9d450c98036fb7be03d024712288a62767f3c55bfc2002c9dc02c9e6fd27`  
		Last Modified: Fri, 15 May 2026 21:22:05 GMT  
		Size: 17.8 MB (17789238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9d7a480daf84256773f69d71eb314a43a3a8c9142697a75a31ed5214e70720`  
		Last Modified: Fri, 15 May 2026 21:22:03 GMT  
		Size: 14.8 KB (14751 bytes)  
		MIME: application/vnd.in-toto+json
