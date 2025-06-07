## `ros:eloquent-ros-base-bionic`

```console
$ docker pull ros@sha256:febdb27cd14b3aec28f43947654ecd7b1bedb57f71e00dac3de13fc7be39eb59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:eloquent-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:c91add70af23e43835e9056abefd104f80ce27068f26e1ddd0e506a8d1c4e19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282594519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4255e56cfa63ed38b6354052a71a7e4ca5519e8736fd7fe7f5538cfcc0434b6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 14 Dec 2020 01:00:59 GMT
ARG RELEASE
# Mon, 14 Dec 2020 01:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Dec 2020 01:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Dec 2020 01:00:59 GMT
LABEL org.opencontainers.image.version=18.04
# Mon, 14 Dec 2020 01:00:59 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Mon, 14 Dec 2020 01:00:59 GMT
CMD ["/bin/bash"]
# Mon, 14 Dec 2020 01:00:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
ENV LANG=C.UTF-8
# Mon, 14 Dec 2020 01:00:59 GMT
ENV LC_ALL=C.UTF-8
# Mon, 14 Dec 2020 01:00:59 GMT
ENV ROS_DISTRO=eloquent
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 14 Dec 2020 01:00:59 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4cd763c4f102fe26075ed12bdf3a53ae0335b10b75246e333d1729551946783b`  
		Last Modified: Sat, 07 Jun 2025 00:07:52 GMT  
		Size: 63.5 MB (63538581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fff6ed272ffd78a1c88497de95987c8fce161eadab2a2aa622ff9f73754035c`  
		Last Modified: Sat, 07 Jun 2025 00:07:49 GMT  
		Size: 270.6 KB (270593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa858cf34fe14ce5c1c0fa29d97687cca30e5a655f7e9695cf7d56123c83fc9`  
		Last Modified: Sat, 07 Jun 2025 00:07:49 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a644f5d92179411288e51b40f3dc04ae03506a62ed4fc7520de3825e253791a`  
		Last Modified: Sat, 07 Jun 2025 00:07:49 GMT  
		Size: 4.4 MB (4371111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros-base-bionic` - unknown; unknown

```console
$ docker pull ros@sha256:20b21fd7564bf522031f2bf4f0841a9cf62edf6827e9d8f5740735a1400531a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21862315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2191a5d33e2f672a84fbb767ee85cb46581526651c8661ed56cd17e8e66308e`

```dockerfile
```

-	Layers:
	-	`sha256:040ebe487d61dfeeb5fab35dcacedbe6fe965318df2a69e768e82c3c00663296`  
		Last Modified: Sat, 07 Jun 2025 01:18:56 GMT  
		Size: 21.8 MB (21845129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f8ff712ad7d5905c40062f867d48a1045d33c284e54d0d057d4cdba3ded80a4`  
		Last Modified: Sat, 07 Jun 2025 01:18:57 GMT  
		Size: 17.2 KB (17186 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:eloquent-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:38be42e2edeae9ea7fcb75f87233f7169943b84b8ae9838c0a863b6d4b636d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234483296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2100d01c2319293a7478d106df96fab2719fddad0fe7aa3b08b9135f2d02f19f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 14 Dec 2020 01:00:59 GMT
ARG RELEASE
# Mon, 14 Dec 2020 01:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Dec 2020 01:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Dec 2020 01:00:59 GMT
LABEL org.opencontainers.image.version=18.04
# Mon, 14 Dec 2020 01:00:59 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Mon, 14 Dec 2020 01:00:59 GMT
CMD ["/bin/bash"]
# Mon, 14 Dec 2020 01:00:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
ENV LANG=C.UTF-8
# Mon, 14 Dec 2020 01:00:59 GMT
ENV LC_ALL=C.UTF-8
# Mon, 14 Dec 2020 01:00:59 GMT
ENV ROS_DISTRO=eloquent
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 14 Dec 2020 01:00:59 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1fb8d49e612f90dbec0d4f6098780f2774bb5dbe5c337a08c12dfc9c9c91772f`  
		Last Modified: Sat, 07 Jun 2025 11:54:13 GMT  
		Size: 48.0 MB (48033459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a708b6f1ffe3041048665490416c1fc43edde90b804472bd3cbf061690275a`  
		Last Modified: Sat, 07 Jun 2025 00:50:07 GMT  
		Size: 270.6 KB (270583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88fd6411454093f479c8f57eb421bcad3db00e85ea1c237cd4b373dc61bb1ec`  
		Last Modified: Sat, 07 Jun 2025 00:50:09 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed43a02e09f372e640782153786f049698f1e2ca6d284a807f278882be9591cc`  
		Last Modified: Sat, 07 Jun 2025 00:50:13 GMT  
		Size: 3.3 MB (3282567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros-base-bionic` - unknown; unknown

```console
$ docker pull ros@sha256:d21312557ba3e4780c755a585dbaa706b1e1f8a70dfff7c35cf66f799df691fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20615672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fb5413c0a0bca14b55ce9b95cc25ba2448da3a1e8499eb9506afc0bf6727ac`

```dockerfile
```

-	Layers:
	-	`sha256:c68268bf4878f9d81d352d46d13f559ad4ebffecba71452ad8d873e97793206b`  
		Last Modified: Sat, 07 Jun 2025 01:19:14 GMT  
		Size: 20.6 MB (20598379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccfbf1c65622f092908f4e53322b49afb565cba455443a16e2bb3aa3addd5a40`  
		Last Modified: Sat, 07 Jun 2025 01:19:15 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:eloquent-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:66b8531725d3f39cfa0e41075e4be9a571da052f40ad7fbe1d6dc654903cca1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256616780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a3e69f9bb195e1d45d576124ef87420d950af175cf0afcb17d5a1d4f69574a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 14 Dec 2020 01:00:59 GMT
ARG RELEASE
# Mon, 14 Dec 2020 01:00:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 14 Dec 2020 01:00:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 14 Dec 2020 01:00:59 GMT
LABEL org.opencontainers.image.version=18.04
# Mon, 14 Dec 2020 01:00:59 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Mon, 14 Dec 2020 01:00:59 GMT
CMD ["/bin/bash"]
# Mon, 14 Dec 2020 01:00:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN echo "deb http://snapshots.ros.org/eloquent/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
ENV LANG=C.UTF-8
# Mon, 14 Dec 2020 01:00:59 GMT
ENV LC_ALL=C.UTF-8
# Mon, 14 Dec 2020 01:00:59 GMT
ENV ROS_DISTRO=eloquent
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 14 Dec 2020 01:00:59 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 14 Dec 2020 01:00:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a6f983474caee00ea13129800634333ba0c7f0086baafc12988656531e1fca45`  
		Last Modified: Sat, 07 Jun 2025 11:47:10 GMT  
		Size: 56.2 MB (56229815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4e6d8c04cfc3c6b1ff35f4e5584b2cb24c50af48e5264ab0783a942ad48275`  
		Last Modified: Sat, 07 Jun 2025 00:56:51 GMT  
		Size: 270.6 KB (270588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887a1ed262af20f43df18c98781b3a61f2854cd42b378eee06d320f34b919727`  
		Last Modified: Sat, 07 Jun 2025 00:56:54 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e3b715715fcc3753494a91bf3d0bfbe61ba651b34c917fce18a016ff1e47c`  
		Last Modified: Sat, 07 Jun 2025 00:56:57 GMT  
		Size: 3.7 MB (3717264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:eloquent-ros-base-bionic` - unknown; unknown

```console
$ docker pull ros@sha256:b006532f5d64b48c4b0267c7247f900faebbcbb1582c28a86607fba5dda9c40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20774658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19690a60fad52cb8774ec2ede4f437f5904606bed75c3674089ec0991a2faa5f`

```dockerfile
```

-	Layers:
	-	`sha256:91d6a39b12c9f97c83c85534864a2eec1e72d5becb407dc261b0f97c40f384f6`  
		Last Modified: Sat, 07 Jun 2025 01:19:30 GMT  
		Size: 20.8 MB (20757335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d63df88950f1b3550e82d360b12b7adfaa096d298c7ac4ba3b954568666c1a94`  
		Last Modified: Sat, 07 Jun 2025 01:19:31 GMT  
		Size: 17.3 KB (17323 bytes)  
		MIME: application/vnd.in-toto+json
