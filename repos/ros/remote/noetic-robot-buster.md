## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:00db4766b53b521172c851e064a73ad6e1a582ac56c763b5252a597b98fde01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:285314dcc66a39197a93f0aa9829d9cc1ec8118a8f864836e5c8ca3f18cf71ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490041623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d2fa049b37263601ae1a261a8e05071a167ce50330096314b99a0cda313cd1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/noetic/final/debian buster main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Fri, 13 Dec 2024 15:13:43 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592cee934a9adff7342cbbc6a887ade3408c48439779f6324665510a2b3eee1a`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 10.7 MB (10700658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53725fd6a1efa565e80ffec22dfec1aec196082d80e59ddfb11f79d86d6aa39a`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7027ac027521944b4d527509c9e64408524f714db5f3eb7db24b36c3947c519`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b8fa11775b938ce704d7a0e85f3a5a1c670d8a5505742c10c987346deb2055`  
		Last Modified: Fri, 06 Jun 2025 23:07:41 GMT  
		Size: 244.7 MB (244711338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208bc360693340c0084653cad3e347704144ab9bb29bf9a0d8ab2952fcc7e6a0`  
		Last Modified: Fri, 06 Jun 2025 22:49:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0d80b0a0ea1e0c1b2770823169a4e01bacae845663d3fcc04d778d3fd4bc87`  
		Last Modified: Fri, 06 Jun 2025 23:09:55 GMT  
		Size: 86.7 MB (86742730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02371c7a619a2796618c00c9d5991b12b2f40e5fc712e305ea45ba04a51f93`  
		Last Modified: Fri, 06 Jun 2025 23:09:52 GMT  
		Size: 342.3 KB (342289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e964541e47dbbf41bc12e1cf1d2a73fac0a0fc0ec871db35f2d2c06562f61b2c`  
		Last Modified: Fri, 06 Jun 2025 23:09:58 GMT  
		Size: 75.7 MB (75732043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07b52f5a238a44ca9660c92298aca628e050fdcbf881f8d079b7b494345da8a`  
		Last Modified: Sat, 07 Jun 2025 00:08:59 GMT  
		Size: 21.2 MB (21150784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-buster` - unknown; unknown

```console
$ docker pull ros@sha256:a5730a654f7d1f70f561d97257b38b9acb526acc30a5f8507228faeb88be57f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36949720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a41842974f86369017146ebdc56ad7528fb701415b691c327221c8cd57c2b0b`

```dockerfile
```

-	Layers:
	-	`sha256:ba27d2fca40f55d50558a76b72d2e1f0f3660343f8432fc651c72dd9a9677fa3`  
		Last Modified: Sat, 07 Jun 2025 01:24:38 GMT  
		Size: 36.9 MB (36941003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2398fea90826adf7f1c1352fb72a08114f5553596dab38f6ae64648300d132fe`  
		Last Modified: Sat, 07 Jun 2025 01:24:39 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cc5b2da880a83c0f43b8d42420d5f25f5d897a14a356d2b2adc3747ba385678e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.8 MB (428822882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b39116058bfd0e9ad2b641803906f4dbf60891542508867671af00d128be5c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/noetic/final/debian buster main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Fri, 13 Dec 2024 16:38:19 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f35ccbf79a842b1dc8f347bdf3cd4c9e8ff3d04fedab80030644cc1c81fd2b`  
		Last Modified: Fri, 06 Jun 2025 23:01:09 GMT  
		Size: 10.7 MB (10706443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0feb157d1ea993f3e44f6dc61b202f82dd11284dd48665846def3c4bee2a5a4`  
		Last Modified: Fri, 06 Jun 2025 23:08:38 GMT  
		Size: 4.0 KB (3987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1160b9b3c836ab8493c6ea91b3af6c6d942ca85290dc7c9b7f8fad0f0f8bea`  
		Last Modified: Fri, 06 Jun 2025 23:08:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daed68793c5fc7a0ae25e2497c554fcaa1cd4391a8020ec7c70ed8ea909d86a`  
		Last Modified: Fri, 06 Jun 2025 23:01:13 GMT  
		Size: 189.0 MB (189042883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37659a0e86f6f971277bd12fd260edde892e084b66f66a075189c47c74edbca6`  
		Last Modified: Fri, 06 Jun 2025 23:08:48 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b289594a7bd7b1edaebd7104359d7bd85e9a51d886943729f3eceed708a49fb9`  
		Last Modified: Fri, 06 Jun 2025 23:27:32 GMT  
		Size: 84.5 MB (84542674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f0bb93669058d316bb0429b64271ecfa7423d599e50f5caa6b71512b8726c`  
		Last Modified: Fri, 06 Jun 2025 23:27:29 GMT  
		Size: 342.3 KB (342288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9eed758429cf9261443d85b01c4126a5e514e392ad6569658a6b346a1a3726`  
		Last Modified: Fri, 06 Jun 2025 23:27:32 GMT  
		Size: 73.9 MB (73910570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687853f53f21c728245da9425b285f08e7bb264dd72e4ab987d36d35c3a56ab`  
		Last Modified: Sat, 07 Jun 2025 00:31:42 GMT  
		Size: 20.8 MB (20820359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-buster` - unknown; unknown

```console
$ docker pull ros@sha256:9c003759809382955e522a00e93bfd3de8c8c384292c660e830cc93bb9254a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36880310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a82d85eb901eca3652182dfa6718891098a4a279703c7394ebd749a507e7c9d`

```dockerfile
```

-	Layers:
	-	`sha256:ff53e87e4c9183ba53d60a6eb7cc6e2e4eade75bd408b12e53804fbdda34d56f`  
		Last Modified: Sat, 07 Jun 2025 01:25:17 GMT  
		Size: 36.9 MB (36871513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c9655ef3118843557210ab2c85c57717d0afaa7ea5178cde9830b1597381cf`  
		Last Modified: Sat, 07 Jun 2025 01:25:18 GMT  
		Size: 8.8 KB (8797 bytes)  
		MIME: application/vnd.in-toto+json
