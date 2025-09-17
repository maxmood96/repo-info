## `ros:kilted-perception`

```console
$ docker pull ros@sha256:a544bac310f509de1755830b91c176ea283dec709c2e88ddce914f4b31856ad7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:ff71f2194c043f247fad9ab7ff360caa47e1f0f80d21a83908dd1c640859659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1095789877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7882bd433024cf1971d7b0b580111ebb50683d8599ddbdf8a487b1aefdcabe`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df8e2597bb5081a304f28b13049febe272f2c6d03097adb5bf569346c6a5f5`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 683.9 KB (683859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1827b068556f57886cad395350cded398b71c780dad810d9cb5f48aeb1bd5`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 6.7 MB (6746894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251ab4ea82f37711412e2ce34dff17f73d11caef6a5cb3c8f4a23bb24242ff66`  
		Last Modified: Mon, 15 Sep 2025 22:26:52 GMT  
		Size: 94.1 KB (94080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c92407c0c99f8ce4496a5f8ab4a6883930dd204426676dc03f36394b96ef20c`  
		Last Modified: Mon, 15 Sep 2025 23:19:20 GMT  
		Size: 135.0 MB (134968079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb84c0ca29118539fdb1987693ba26bbb7fef03bad6c1349885f8189f99491`  
		Last Modified: Mon, 15 Sep 2025 22:26:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ad4e0967c4f2fc54b1fc8c9371361914af0419279ef3a09f8f9ecbc3e17f3f`  
		Last Modified: Mon, 15 Sep 2025 23:21:05 GMT  
		Size: 110.2 MB (110185503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c3dabe47646cba938ba7076a97e47b843b10a81d035548e0c5ae09767aa456`  
		Last Modified: Mon, 15 Sep 2025 23:21:00 GMT  
		Size: 362.0 KB (361999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f256a20a09d470c8e0eb81166c3ecc100e308702d21403458d3e9acb78178d`  
		Last Modified: Mon, 15 Sep 2025 23:21:00 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428752ea94da6d6c5f53cfad376970875b81973b8f3c9bc747f9a9e63e679329`  
		Last Modified: Mon, 15 Sep 2025 23:21:05 GMT  
		Size: 28.1 MB (28050584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75dac3dfc4bfcbc5878189378dacb7de7b810e63674511c1f112016a35af24c`  
		Last Modified: Tue, 16 Sep 2025 05:41:59 GMT  
		Size: 785.0 MB (784972764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:4b915a495a15cc28f3e5731900bc645a2a9b05295f324413366c2bafe3925a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fb9e4489bad5a3dc9902d83ae8f02d197dffbb0b36a85bf2442f1536e4f63d`

```dockerfile
```

-	Layers:
	-	`sha256:d6c5a5ec63104f75c3c1cb9b79c5ee1f05b9bc7071f47ed4550ac5b7c1b5cea3`  
		Last Modified: Tue, 16 Sep 2025 01:18:09 GMT  
		Size: 60.8 MB (60822353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d034e593f848a66c145deb5c0acf1b08a6dfb279d7f20d20727a457c10129b4a`  
		Last Modified: Tue, 16 Sep 2025 01:18:11 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:062ba562a65504dd3eedbb74cdf8fd2411f203a178ad84d7c1cbfca44a368f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.1 MB (994149870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f77f3a8c5ca66eb1bcae289e4c1c2665ffa5e06288fc67b776244e99ad686c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c509e55b08b478a9c488a0dd55c7c274587d88664a1e1d7ac3147918e5d2b`  
		Last Modified: Mon, 15 Sep 2025 22:23:51 GMT  
		Size: 684.0 KB (684016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5f901baef4b99efe03f4dd1cc51b0b249fca699f0146d3dd0e31ebab587695`  
		Last Modified: Mon, 15 Sep 2025 22:23:51 GMT  
		Size: 6.8 MB (6759940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a9a09aa4cdd656a929b8daf83db234156540057e4fbfe3b36348f311805c3e`  
		Last Modified: Mon, 15 Sep 2025 22:23:51 GMT  
		Size: 94.3 KB (94267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8651d2643c6b1311861fc1a4214b7624613cbc31ba8a4fd1bcf29cb1e3985a4`  
		Last Modified: Mon, 15 Sep 2025 23:19:20 GMT  
		Size: 129.7 MB (129689601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8ed0138fce5e2a18b234ba7d9930c6b693a292bc46b687272061427a240166`  
		Last Modified: Mon, 15 Sep 2025 22:23:47 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae954c6850165e8bb822b38281327aba2bc9f20a91297d4114ce41b4a7f3cc5e`  
		Last Modified: Mon, 15 Sep 2025 23:20:58 GMT  
		Size: 105.6 MB (105593836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086ce7a2326031f6b94c6fdd85e89902d3a993ee73ad3ba32c4f3888e0d68ead`  
		Last Modified: Mon, 15 Sep 2025 23:20:52 GMT  
		Size: 362.0 KB (362004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63177c1add437c895e7fdabb1131dceea8eefd93a13e07766518530f638b4cc`  
		Last Modified: Mon, 15 Sep 2025 23:20:52 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f23048a7a420855a7040e04b2035e62fc42e7da922a9146172a29d46b5077ed`  
		Last Modified: Mon, 15 Sep 2025 23:20:54 GMT  
		Size: 27.1 MB (27137347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a46add338ea15d64646cb9d7064048f73086d6738f4e40063c6fed1ddd3621`  
		Last Modified: Wed, 17 Sep 2025 13:55:42 GMT  
		Size: 695.0 MB (694964894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:dbb75c76d035a8ecfe53705e95a7905049a6b7747914640ac7198077555c3a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9df6b519b764817545957548955534d5a487c15547dbfd0cf79b2d5b1060ff`

```dockerfile
```

-	Layers:
	-	`sha256:3eb7dbefa29bcea5f4c3c270b8dfa074890ad309daa383314b237035c5d4e717`  
		Last Modified: Tue, 16 Sep 2025 01:20:02 GMT  
		Size: 60.8 MB (60752878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9ac13cd55e263224dc3555ccbb5b24baecb90caeae914f3061c05da47d1345`  
		Last Modified: Tue, 16 Sep 2025 01:20:04 GMT  
		Size: 9.5 KB (9474 bytes)  
		MIME: application/vnd.in-toto+json
