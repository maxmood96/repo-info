## `ros:eloquent-ros-core`

```console
$ docker pull ros@sha256:23f26935e76182dad399aee3b9a5bd5d8509c6261cf64ad977c297e6fb5d9676
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:eloquent-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:64828402ebab4f27deb72ce453695c4f98744c131aa6d4bace9d0c395c767537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214411765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8018b0fcae712662426e4afe668cec5131d7d7044a59175ab745930729e70e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=eloquent
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Fri, 13 Dec 2024 13:10:33 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479d6516b5b71644b6cc96d844b23830cbf0d1ab4f7c4a9180dbb003352974a`  
		Last Modified: Fri, 06 Jun 2025 22:49:22 GMT  
		Size: 818.8 KB (818769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b06a714936526a1264026982671e2fd973aabc5e3a06382de9a5ff2039dbaf0`  
		Last Modified: Fri, 06 Jun 2025 22:49:23 GMT  
		Size: 4.7 MB (4688743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9a5f477bff1dc9a46e96f21b664baa2c61c24f38a784517fa45c4440fa48d9`  
		Last Modified: Fri, 06 Jun 2025 22:49:23 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2ad959edfc7117efd0d3c75f21de5fc71c696f3c566f6d4f963abc4178886d`  
		Last Modified: Fri, 06 Jun 2025 22:49:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88090f0cf723f1c40ededf8978a6634972fec544dbcef35613d7a6f975f5fd`  
		Last Modified: Fri, 06 Jun 2025 23:07:34 GMT  
		Size: 183.2 MB (183210181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef0a1c07f2aa35a613d990a378483fc39698ed4ec70214f61088c71c59b47d8`  
		Last Modified: Fri, 06 Jun 2025 22:49:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:021c5ed51da049ba55a42fb49fac6e59280c55da22c456ffbd97a8b6136894ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19062562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89f2486de153673aca68258fc97da4e48fe1dbfc376c37c86bdfe071ce82f62`

```dockerfile
```

-	Layers:
	-	`sha256:a053058187d5c32ac9734aef56d93f451f352c5ae0c3229a7f6219ee87d63fa2`  
		Last Modified: Sat, 07 Jun 2025 01:19:09 GMT  
		Size: 19.0 MB (19047382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c8008084b8bef56c294fe5402ceceebf8be35b489058045d58ca9caf473ac2`  
		Last Modified: Sat, 07 Jun 2025 01:19:10 GMT  
		Size: 15.2 KB (15180 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:eloquent-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:0e46d3d0e1ad008d03e60cc0e523c56bd9b87f84724c136453f05082507cd549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182894245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae152fa98a841347b4804ae4365c009c48bc97125357a858f9141ccb9ccf128`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=eloquent
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:33728956a279755bb5e348de30626ffff0023b589d4fae264c2722ad7c06e207`  
		Last Modified: Fri, 13 Dec 2024 23:12:36 GMT  
		Size: 21.4 MB (21399001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49dc90beb658024e96db38e10eb9d3d5e95151611e5a8b1e4aac7ea6e45313`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 820.1 KB (820137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd276fdf8bc17a3ae89b76a87869626c84e29eb535dbb5b183ac80bae85c02c`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 3.9 MB (3900545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b029d64f9143b80260f4b5b994450da65eef021667391fbce44a5f2aa0f4398`  
		Last Modified: Fri, 06 Jun 2025 23:10:10 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30d7b9793ce6e39fe204512d45290f47261186305bb67b812db91174e635176`  
		Last Modified: Fri, 06 Jun 2025 23:25:13 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733d36e0267ac31385145d2451947c564af6e00b7c40a2b0609fe6a7b1221f3d`  
		Last Modified: Sat, 07 Jun 2025 11:53:59 GMT  
		Size: 156.8 MB (156771762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60f6ce791c835a931f96cd4ecb40b4c458df0e59a8f7474a54fb368ed4a9453`  
		Last Modified: Fri, 06 Jun 2025 23:25:16 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:dfaf47c25dad1d744710e7709fb45cb9fcfaa8c1432ba2d9468b691389e4885e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17916144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c7d24692d6701e963d7f2329ca6d3d6da6105f752b12b43b27cdd7a82d6481`

```dockerfile
```

-	Layers:
	-	`sha256:7401f98ffcf408084db8e91f0fc69136163bfc1f89d59c4792545bf18b2282a0`  
		Last Modified: Sat, 07 Jun 2025 01:19:23 GMT  
		Size: 17.9 MB (17900858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c67f6f4724e2e8417473c4af23afa1aab99ec234568facb90c8b538c94e1c53`  
		Last Modified: Sat, 07 Jun 2025 01:19:24 GMT  
		Size: 15.3 KB (15286 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:eloquent-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7f95477c7216671de0f9c65750f935b9a39ceb3040aa96372077fc48d5ccebcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196396642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb7303581f53cfe49ad558bbca4e7be94ba02c2fcb9f57ebf2397f3bf674348`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=eloquent
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Fri, 13 Dec 2024 14:46:44 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6559b6c0a95271b577d553166080f5d9965d9e2d2b1732c96a566175205af31f`  
		Last Modified: Fri, 06 Jun 2025 22:59:17 GMT  
		Size: 818.8 KB (818832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99d6787c1aa8369d0f0e3a1051c56c004c0b42816139b09e85d5fed6e44a27`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 4.3 MB (4270397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5c6de79efb0ec1e3e319f9a58fd5e398fcb65ffb3eff75ff9ff1cff87f158`  
		Last Modified: Fri, 06 Jun 2025 22:59:18 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f53cf949d0a3b8bf9cdb088732c432b8d3952789160aacd1caddd73b9c02c`  
		Last Modified: Fri, 06 Jun 2025 23:22:54 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a1bc71fd481d7d8718010e4e6b76a3efdbf1727fff82166ddec47c8dc073c`  
		Last Modified: Sat, 07 Jun 2025 11:46:50 GMT  
		Size: 168.6 MB (168591100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092ab5015c6f828f787cad76d98dd4c33d3eb5fe8ad9d21e52f9d05925893a56`  
		Last Modified: Fri, 06 Jun 2025 23:22:59 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:798bff93322d445758d67cca3aff3433d8053ecd6027b9bc8d411b19b7ac4c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86343b49fb01f6f2cc557ccd0f197e7836ffe9286fd284c4e8fe4c657620497b`

```dockerfile
```

-	Layers:
	-	`sha256:15c69f56ad2c761f98124deeaec366151a3557d982ac1d67964315ada88160e5`  
		Last Modified: Sat, 07 Jun 2025 01:19:38 GMT  
		Size: 18.1 MB (18071635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d8ede8b01fa4b734df37922ffe937285b505e0710f43ad606a2ca55a8d8ccf`  
		Last Modified: Sat, 07 Jun 2025 01:19:39 GMT  
		Size: 15.3 KB (15314 bytes)  
		MIME: application/vnd.in-toto+json
