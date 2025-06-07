## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:1b5258a52cde9ba6a3654be38129dd6e23b712cc3477a88f550a07c51405c6a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:3c703cda8d6c960f18154d02d814851d799de21bff37d7e399dcad773a38b0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.9 MB (468890839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc95f7f46fe341bda43e8ebb584144cd0611f829aa9c963141bacf792cfb82d1`
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

### `ros:noetic-ros-base-buster` - unknown; unknown

```console
$ docker pull ros@sha256:1da5ee3f6804ce94d1110fa0cdc6968c1cd3bc468f08f1ce76262e25da42a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34826860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f79eec168d920e106901a51aae775418dde83a14b6a7adc0f4ce0eb0e46ef3`

```dockerfile
```

-	Layers:
	-	`sha256:a32f3b46efcfa8fb2ad66b6c91d768dbeb237efa910db0a45be4db0ca0da6412`  
		Last Modified: Sat, 07 Jun 2025 01:24:46 GMT  
		Size: 34.8 MB (34814393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69c6703a0456f6de29f41105532c115779a46000aaa2231068473d41f4f1bcc`  
		Last Modified: Sat, 07 Jun 2025 01:24:47 GMT  
		Size: 12.5 KB (12467 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2fc3d7f3dfbd0889dd1906ad0a16da7a574f33550ce1eea25240c2a6e39d4a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 MB (408002523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0b8cd91df090cac52cffacee3d6c8338d66bc4c6252db200d657451d635711`
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
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Fri, 13 Dec 2024 16:38:19 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f35ccbf79a842b1dc8f347bdf3cd4c9e8ff3d04fedab80030644cc1c81fd2b`  
		Last Modified: Sat, 07 Jun 2025 10:13:46 GMT  
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
		Last Modified: Sat, 07 Jun 2025 11:56:56 GMT  
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

### `ros:noetic-ros-base-buster` - unknown; unknown

```console
$ docker pull ros@sha256:158da41a2b6609fed94f433fe67115014183dc8c90c858094ef6ef4ea8f9372c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34759866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c529ee173b67030df9897f9188739117563c03185aa060c541aa588af7ff5ef`

```dockerfile
```

-	Layers:
	-	`sha256:a39582f7caba66e0b6c47b53b0319f0bce58873aa12916506bb86933f42e8f77`  
		Last Modified: Sat, 07 Jun 2025 01:25:25 GMT  
		Size: 34.7 MB (34747277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6fb0d8505e06b72e294cba3cb60a53f55f1f4247ed35511feb8e08265061751`  
		Last Modified: Sat, 07 Jun 2025 01:25:26 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json
