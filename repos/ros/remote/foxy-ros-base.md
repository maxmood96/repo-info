## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:afd8508e9f193cf3d3fe298f68a14e4f4ac80527cb0bc5ff6943c4300d950e99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1555cf64b24b344baeb5af796878a8b4f2051c3f38c88cc162dd46ee104e8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254968863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc76cc006e617b12323eed3c811587b1714b6f7b41ecae986c2d939807d0100`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905dfb1bab3312147382cf593a88dfd91dcde255426f42b174c0a00cbfee3d49`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 1.2 MB (1194819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf200ef89210ac612db81e54c264d517b910910145ae871d765696f0b2599d`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 5.4 MB (5363903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09efa67422b34d4c77e03962a93fb1c22f91239484ef3e692b04953247ee3d`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc4be6b715533df3810ad59eb7a493b1ad5a0fcd129ace37d611a85328e0d7`  
		Last Modified: Fri, 06 Jun 2025 22:49:35 GMT  
		Size: 125.6 MB (125595150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aec951983b4c0ff57c8185a118737d2aa6abd2979e54efa7007c42e388e3ce`  
		Last Modified: Fri, 06 Jun 2025 23:09:21 GMT  
		Size: 73.3 MB (73323708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a36983631da54649d3973eca83d8f7b9bdff7368406fac4f29468e0bb26c3b`  
		Last Modified: Fri, 06 Jun 2025 23:09:19 GMT  
		Size: 301.2 KB (301159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87633dc1f860b5a814b4544ede1903f1dc53029e982d7bc3b4b6dc51e679c0f1`  
		Last Modified: Fri, 06 Jun 2025 23:09:19 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f026747287ad82fbc819b8c857e70adb1d75218fc3f41221b1591bf802e9d0`  
		Last Modified: Sat, 07 Jun 2025 02:12:32 GMT  
		Size: 21.7 MB (21672857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:43ed1b9a60d768ff82cc5df477a2fd2d487148f2a0e514daed7bca4cba295e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22643474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a24c1e03c14698278a3bd385e83c37d021a5750bc0cc12b39d4ce57ef71341`

```dockerfile
```

-	Layers:
	-	`sha256:0c7f62558466bf857633ef7626050e6cbb7c77b8dfa7dba89463c82e5f4af2d3`  
		Last Modified: Sat, 07 Jun 2025 01:19:24 GMT  
		Size: 22.6 MB (22626355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e2aae5698e322871b42ae00b147c2953c832c98d1fa28241763a7164ec12c4`  
		Last Modified: Sat, 07 Jun 2025 01:19:25 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:487e2b121107be08d3dcfb759fdb0bc25f1622902a7b6fedb85236a602b4d789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229776472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce8a3d24ba5fc59286d4d98bf1349762b4946e63eecc2f6418de304af3f76b7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd563e74b9280d17b11bae86038561c7184eda5ae05a08570ac236ede7caab26`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f376c0b3101d22149ca2d878d920aa16f69ba90b157b102210f0b0216b96c6`  
		Last Modified: Fri, 06 Jun 2025 23:12:25 GMT  
		Size: 108.9 MB (108878978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8bbf8c8a1cae034a096fd542d615567aabad879961709c67a9d412fa9cb10c`  
		Last Modified: Fri, 06 Jun 2025 23:12:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0828ae3bcc02cebe074457715b9015f612b41f3505eec2d509eb84191059d1`  
		Last Modified: Sat, 07 Jun 2025 00:45:00 GMT  
		Size: 67.7 MB (67674946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008d8e892d97a7ab8afd15de5401052d67d5d1a11424408fe9bdf6f8facd4ea`  
		Last Modified: Sat, 07 Jun 2025 00:44:57 GMT  
		Size: 301.2 KB (301159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e8afc91b0fc0fc13a30cd50b392436315c3301fc5dd8378e1bad63c83b178`  
		Last Modified: Sat, 07 Jun 2025 00:44:58 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7067dec2b246676b2e5d3e65aa8474d14fed126303588ae5ebd0040f9b0c2`  
		Last Modified: Sat, 07 Jun 2025 00:45:00 GMT  
		Size: 20.4 MB (20398057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:633ba80f46ca8fc360c6e93718a0f1006c287c8686db18b94cf9b54933a0d868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21563319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a424bdf2cc314396cca76f67161f150f45a995d96282b4256b5ad6cd5e25c277`

```dockerfile
```

-	Layers:
	-	`sha256:641f149cbb13fed4a2d3b7cf31a8214f520e730368002d5ee11037d2d7fc11f1`  
		Last Modified: Sat, 07 Jun 2025 01:19:39 GMT  
		Size: 21.5 MB (21546063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6850a9c9bc9c1da1ad6c90721c65cecef6622936daac15d6f1a08d200cb0e34`  
		Last Modified: Sat, 07 Jun 2025 01:19:40 GMT  
		Size: 17.3 KB (17256 bytes)  
		MIME: application/vnd.in-toto+json
