## `ros:bouncy`

```console
$ docker pull ros@sha256:fd2c704da09ab15c1af085f35ddc45c0bfe2c6dab363189df8c4666f3880e520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:bouncy` - linux; amd64

```console
$ docker pull ros@sha256:38bae6623cbe4f8aa86ee53e3e08e82ed73049548ddfac688fb10c16b81153ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265415380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6ba21e1a6d7751ddbf88bd4619e3f4503cb1e4693da50436077f6e37971ef1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 29 Dec 2018 04:54:49 GMT
ARG RELEASE
# Sat, 29 Dec 2018 04:54:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 29 Dec 2018 04:54:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 29 Dec 2018 04:54:49 GMT
LABEL org.opencontainers.image.version=18.04
# Sat, 29 Dec 2018 04:54:49 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["/bin/bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo "deb http://snapshots.ros.org/bouncy/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LANG=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN pip3 install -U     argcomplete # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV ROS_DISTRO=bouncy
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-core=0.5.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-base=0.5.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:dd976951c47b3a27f040eb803edcd43a6a8fa5381a4ed8331ecd2e438b7bc54e`  
		Last Modified: Sat, 07 Jun 2025 00:15:55 GMT  
		Size: 2.9 MB (2923840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:bouncy` - unknown; unknown

```console
$ docker pull ros@sha256:401da627dcf0f8c84ff85b16c430501c2e67c75ce0fe883d5cb82bc6155b0405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce213c26205948bf22376cfda45e56f24560f3a410ad5af9262c6209ed0fd32`

```dockerfile
```

-	Layers:
	-	`sha256:637216b7ead5e8e5cb10daf8cd6552931b3dbee10d03dd90db8e3fbf4d669b81`  
		Last Modified: Sat, 07 Jun 2025 01:17:47 GMT  
		Size: 20.1 MB (20139567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ada029a0124c8552916313eb16f1d27d39471be3620d94c7dd6f7670bf1448c`  
		Last Modified: Sat, 07 Jun 2025 01:17:48 GMT  
		Size: 9.9 KB (9915 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:bouncy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:093ae786115416a4f4ecb5e40c8b8ef3e459ba7620c0450f5ff8b8280ddf2740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242440174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03af8f20ac5218e481068fe472bc19aaf0ce33537553a625dce8f7f23472a22`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 29 Dec 2018 04:54:49 GMT
ARG RELEASE
# Sat, 29 Dec 2018 04:54:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 29 Dec 2018 04:54:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 29 Dec 2018 04:54:49 GMT
LABEL org.opencontainers.image.version=18.04
# Sat, 29 Dec 2018 04:54:49 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["/bin/bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo "deb http://snapshots.ros.org/bouncy/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LANG=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN pip3 install -U     argcomplete # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV ROS_DISTRO=bouncy
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-core=0.5.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-base=0.5.1-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
		Last Modified: Fri, 06 Jun 2025 23:32:26 GMT  
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
		Last Modified: Fri, 06 Jun 2025 23:32:24 GMT  
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
		Last Modified: Fri, 06 Jun 2025 23:32:26 GMT  
		Size: 36.7 MB (36693132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc3be15db344e35384b8657b4e2ee890f173390be36decf1421fffd62e04d6`  
		Last Modified: Sat, 07 Jun 2025 00:15:32 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c5d1d7d9b5eb3d06ffe2015fc2dbe551e8a0b97c0b6b34f946f124b1cc6563`  
		Last Modified: Sat, 07 Jun 2025 00:38:59 GMT  
		Size: 2.7 MB (2679385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:bouncy` - unknown; unknown

```console
$ docker pull ros@sha256:d9758a6bfd994167b2a105d0b22503c2ae51bcdeec1e2f800a5bee57e8d594cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19003848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5b3042ca1c09ea1865590ed4eb64dd5dfd41e5b374a10fd054c2b0d1f9a5b3`

```dockerfile
```

-	Layers:
	-	`sha256:5bf81a81b63adaf64d065300903a641b12b0cffced10563f19f229b33f18097a`  
		Last Modified: Sat, 07 Jun 2025 01:18:03 GMT  
		Size: 19.0 MB (18993841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1fbf408883294c59015c5a3c3dd5539749fb028b327256884ee5163373babbc`  
		Last Modified: Sat, 07 Jun 2025 01:18:04 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.in-toto+json
