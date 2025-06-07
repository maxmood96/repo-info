## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:aae7ff4a15cf29b5b5778d1336dd517ca6a56c22d41ccea2f023e159ea210b50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:0da0ccddff27ff4d866b049ff299d635e82c26ff991a2399ebcd53a516de24b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **956.8 MB (956755055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1393f5af4e9d6a98cae984b3a97d309f2d73cffb7c699c57be1757cde3dfb314`
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
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b17bad935a250b0f3181515901f46fdea9e4c194f184429609f901df8273622d`  
		Last Modified: Sat, 07 Jun 2025 00:12:02 GMT  
		Size: 487.9 MB (487864216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-buster` - unknown; unknown

```console
$ docker pull ros@sha256:1cfe43a1921f49d949f480b665ab28b89d493a02d5870ed32b855e937b79d471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59328907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26251b0478bbf742ebaf519cb40bb2feb04d02179b1277ffc09d0d1071415a50`

```dockerfile
```

-	Layers:
	-	`sha256:a7d4a57941d7c71a63e0f2025de589a4b1e3642bd1a5da477a18ac2326dd48d0`  
		Last Modified: Sat, 07 Jun 2025 01:24:33 GMT  
		Size: 59.3 MB (59320148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5a382023f8c4c45c46236cf217b0c689960db72d37efe9d01dd59e15737b14`  
		Last Modified: Sat, 07 Jun 2025 01:24:35 GMT  
		Size: 8.8 KB (8759 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:570c2469028f06a3d93d0f10deefbcdff6a93f6f3cc365fd5aa94dd5f2029289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.8 MB (872809620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9bde51e42528e3185da946acc14b45333d28fc4b94bea2ba1f5e54379cc3e`
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
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:23d65d5786c0815372fc68ca25f797ba61d4e353b192d5778a6a8d0b9ce76d07`  
		Last Modified: Sat, 07 Jun 2025 11:58:38 GMT  
		Size: 464.8 MB (464807097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-buster` - unknown; unknown

```console
$ docker pull ros@sha256:70a67f6813b3142a60807e9fee34e7913264a769eec6f5c86b149f5e76eb2b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59278875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dd91edb0da4391ce129d06f9326a6c53afcd047d67d0de1cf67c4b3a8330d1`

```dockerfile
```

-	Layers:
	-	`sha256:fc8f1032642d3fcf1574ac66063e6878765e4e41f8510a546bd4f13d074219a9`  
		Last Modified: Sat, 07 Jun 2025 01:26:19 GMT  
		Size: 59.3 MB (59270037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f32074d69511e0011da707f78b758d882de5528f9b7dbf6607727f8e6d5c7c6`  
		Last Modified: Sat, 07 Jun 2025 01:26:21 GMT  
		Size: 8.8 KB (8838 bytes)  
		MIME: application/vnd.in-toto+json
