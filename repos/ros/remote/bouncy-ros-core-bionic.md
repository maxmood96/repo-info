## `ros:bouncy-ros-core-bionic`

```console
$ docker pull ros@sha256:7926238f6421ee9ae9a9450bad3bcb30c6367958df20968947fa6d8b83a7a1ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:bouncy-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:10e691452973faa6eee60df69074d3db3e79c353f36060259476c8334222bb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262491540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c4968fd3aaeb4845024d70ed3a53b59c1f6cc7ac3d2e9c7b74454fbf36f941`
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
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/bouncy/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN pip3 install -U     argcomplete # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=bouncy
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-core=0.5.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b1e3c8b757d51598781f5333af160d7d8fcc65bfc687b752486745db4a3b2031`  
		Last Modified: Fri, 06 Jun 2025 22:50:28 GMT  
		Size: 818.8 KB (818750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387c98b30c7039cf7b5028db31f744b94a5c455e63b98a09c040d703326c1210`  
		Last Modified: Fri, 06 Jun 2025 23:07:47 GMT  
		Size: 159.1 MB (159063859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aa0df3611f4e67df012abf2619626f88aee8c78ed97443de951a77f67fc6ad`  
		Last Modified: Fri, 06 Jun 2025 22:50:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1126a71440e68a2df42eed56dec5b39bc1307346e2e5aa336e83942ad390a324`  
		Last Modified: Fri, 06 Jun 2025 22:50:29 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab1b6dabe441aa01ea4e2cc942653e1a0881962714512ed95e109d99748042c`  
		Last Modified: Fri, 06 Jun 2025 22:50:31 GMT  
		Size: 28.0 MB (27965707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04965c90651dd310eb2592249de165a031acf4dedc4150c2db99b191a8b1e9ae`  
		Last Modified: Fri, 06 Jun 2025 22:50:30 GMT  
		Size: 1.8 MB (1830035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9994d8b58570f45e2e56c32bb4e013a3d539585808a43490bf5d2fb1a82226`  
		Last Modified: Fri, 06 Jun 2025 22:50:30 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b2bf2a16608510d952b3ad5b6006b20a3b85dac7d96d3088ac3c2e1595743c`  
		Last Modified: Fri, 06 Jun 2025 22:50:32 GMT  
		Size: 344.5 KB (344470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2567a7fd9fd60bb0804286910395dc3ab03e3c080aa068b09bebf2e8cf1ce5`  
		Last Modified: Fri, 06 Jun 2025 22:50:35 GMT  
		Size: 46.8 MB (46772100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2672b5d5fbdb7fb549587f28cdc042fe15edd62d518e8c93e0c16a4b31642`  
		Last Modified: Fri, 06 Jun 2025 22:50:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:bouncy-ros-core-bionic` - unknown; unknown

```console
$ docker pull ros@sha256:b41d188d25906ddb0de5d51a698b7aad427a6d0fb8af11de4d378f1fe8c56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19399467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3eaeebd8d13bf1b23d4b93a3e59da410355251cb10f148b357b67c62fff7c59`

```dockerfile
```

-	Layers:
	-	`sha256:4ae574d5946926a6f81c84466ed66552d8d7b2c6f86860795351bd3b7b5cf5b1`  
		Last Modified: Sat, 07 Jun 2025 01:17:55 GMT  
		Size: 19.4 MB (19374274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83508094efa0dcaffbe3b36e2eb5caef5c9b7a8cabad471eab417fd25b3c488e`  
		Last Modified: Sat, 07 Jun 2025 01:17:56 GMT  
		Size: 25.2 KB (25193 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:bouncy-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1309e6c34ac90a0fb3ca8dc0f19dbe0b9a997bd3e3343313de13736716c1f158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239760789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1e9669318ce48c1847e4bec783ed62077c6f4c71943b1cb223526c6f24b88d`
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
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/bouncy/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN pip3 install -U     argcomplete # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=bouncy
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-core=0.5.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:2da943fc9d36da891f643cb8846da026acaf282a4cd7307acd04f4d7d57030e1`  
		Last Modified: Fri, 06 Jun 2025 23:51:37 GMT  
		Size: 818.8 KB (818806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0387700f6cd8093562ae937213c0a814a6dc71f8797f21027defef5d9fb84ae5`  
		Last Modified: Sun, 08 Jun 2025 00:25:06 GMT  
		Size: 150.7 MB (150693162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1f3390227b1fb5e963224d2395409771e29a7d99e10472a0604e2e878b8330`  
		Last Modified: Sat, 07 Jun 2025 00:15:17 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1f6165b1ebaca215b5fa24cd4d0bed0bdcd8a3ecaa7aa3f69b06e69df594a7`  
		Last Modified: Sat, 07 Jun 2025 00:15:19 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0d685842f9d880fcd732185b42ddf8bd4fc2573775369e79d6279614694517`  
		Last Modified: Sat, 07 Jun 2025 11:47:14 GMT  
		Size: 26.7 MB (26662158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c6dd3a9273a7d6128a17f676b1ca7eb606ee3332721509ef6c9b571eb5369`  
		Last Modified: Sat, 07 Jun 2025 00:15:23 GMT  
		Size: 1.8 MB (1830224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e4dc2ec3f6609e5bbc8b98a661688ceeafe774a5fd4893c4f0ad544175d5be`  
		Last Modified: Sat, 07 Jun 2025 00:15:26 GMT  
		Size: 2.6 KB (2558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6b298f85cfbb54bb624c0d5b5796920746dada35e43f36274c4cd3162ac1bb`  
		Last Modified: Sat, 07 Jun 2025 00:15:29 GMT  
		Size: 344.4 KB (344434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f121ee6230c1202f1a853153b1063bdda79eb290818138ffb8cfed8da17f20`  
		Last Modified: Sat, 07 Jun 2025 11:47:23 GMT  
		Size: 36.7 MB (36693132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc3be15db344e35384b8657b4e2ee890f173390be36decf1421fffd62e04d6`  
		Last Modified: Sat, 07 Jun 2025 00:15:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:bouncy-ros-core-bionic` - unknown; unknown

```console
$ docker pull ros@sha256:ad57ccc9e29da00fc2db0fb050bff458ed869cb949a7dd5f38774ee992fd431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18282311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf881ad60b8be73d37162b6c30952f48a9ed2a181545e0f9f897d6971566695`

```dockerfile
```

-	Layers:
	-	`sha256:36d824c23554a20ab6913c7ee2b20334847f20533d7bb688330297bfcb05983b`  
		Last Modified: Sat, 07 Jun 2025 01:18:11 GMT  
		Size: 18.3 MB (18256924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a33a88e7486d3526813354292dd7b42d0e68e667f78b4d4e9a2651a92e5837`  
		Last Modified: Sat, 07 Jun 2025 01:18:12 GMT  
		Size: 25.4 KB (25387 bytes)  
		MIME: application/vnd.in-toto+json
