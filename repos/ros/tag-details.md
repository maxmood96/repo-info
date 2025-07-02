<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
-	[`ros:kilted`](#roskilted)
-	[`ros:kilted-perception`](#roskilted-perception)
-	[`ros:kilted-perception-noble`](#roskilted-perception-noble)
-	[`ros:kilted-ros-base`](#roskilted-ros-base)
-	[`ros:kilted-ros-base-noble`](#roskilted-ros-base-noble)
-	[`ros:kilted-ros-core`](#roskilted-ros-core)
-	[`ros:kilted-ros-core-noble`](#roskilted-ros-core-noble)
-	[`ros:latest`](#roslatest)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:6faa295af1dddacafa9e4f381c9500ca2a7ee215503056f5eab2f450a5f267e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:e4be824130baa1dcac4398eed53559f98ecac0a89315f8681490a8a0c5271dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263031039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866fe3a0fcff7b5c28380b45856b8ff5066e9da8ee6b6d1268bdd8b78bf13448`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f13fa6ab986f8a280cbd08782691746d11fdd96ae24043b73dd15954626359`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 1.2 MB (1214019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3bc629d3d1edb01c22bf6804bd1a42bf1f18eb8cd6d4ca072796ff2ed0898`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 6.0 MB (5991642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627cb8e9cbe801b080f67968716035054c4fb0334ae5bb622abd71b03a74ff8`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 97.2 KB (97159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8193ec0dfde00ae6a93f483fdb9c3d553d9555dd62946ee33781171b80f681e`  
		Last Modified: Wed, 02 Jul 2025 04:13:12 GMT  
		Size: 104.6 MB (104552104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e5ec44afb815e06d47e77ab069ab5bb950f7f36b751ad8b2103057d98c4ce`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fd9e74e6fd05a516cea0b71abc9baf18606effe4543e6337901025fbe4eb0`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 98.0 MB (97959535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c6f0311484b8b07ef741892d26236263307cdb1798f283cfcca3109fe97a`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 363.5 KB (363513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a88d1d3274993db9497c692378fd53e3a7ef81905672d82b75b5e9b33ffc9`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f8638479e522ab3779b4570a1b2c8d65c44b3d80a4f28e78ac598e1efd1419`  
		Last Modified: Wed, 02 Jul 2025 05:11:20 GMT  
		Size: 23.3 MB (23314712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:1eb9c3e49979825d585296aacc13e3ecd821ef674fd5014872f6bd2e5ac9766f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23682649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27eaee7b91b45acb572a6c20dbc784f3216e6219d298ae4813ecba901d400a2`

```dockerfile
```

-	Layers:
	-	`sha256:bf1668290a349236f80b93f19e5fdaa82f67b7182afdc87d5ef5e261653a87de`  
		Last Modified: Wed, 02 Jul 2025 07:17:22 GMT  
		Size: 23.7 MB (23666259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1547542991f104030d7f07dcbe29f6d2d14ecd700dd4fe8caa74a9dd1fa2a939`  
		Last Modified: Wed, 02 Jul 2025 07:17:23 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b9f1c3872615663f504b882b66503d267ed703123596b276ed8a477e3380c451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255428828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed6b1b8d0ad8944e97a0a7e04f56276c1f560eb1517de98e0692579c7b9e9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc154224d775815f0aab30a07a0cba6ca4082b1f09da8355b44aae7c044072`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 1.2 MB (1214196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ffaf60e2489601d3859a11b446b804c7ffb4fe05453885d2411185892b572`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 5.9 MB (5936657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf686f829ca2dfefc31c3f2441114fb0b8ee56bd206a8a7a392cafbf51cd46a`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 97.3 KB (97292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0cd27ef0672066e0e81841bf837a1be14b43325e417a2be373825e06849ca`  
		Last Modified: Wed, 02 Jul 2025 06:25:55 GMT  
		Size: 102.2 MB (102244927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e7d9c15fcb9e5e2600df9e9dece9c12d2a99ea9e8ff316cbfb1e1b8492daa`  
		Last Modified: Wed, 02 Jul 2025 06:25:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7d044aa87162eeff0af0fe069ace5000d2c1f33d306ddd4ede182d486e8faa`  
		Last Modified: Wed, 02 Jul 2025 09:13:10 GMT  
		Size: 95.5 MB (95508902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861b98f01417c33693842112a9d40af4ca6b0e4748e48ded467bec59890f9a4b`  
		Last Modified: Wed, 02 Jul 2025 09:13:03 GMT  
		Size: 363.5 KB (363507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37abcabf329d1b7e5974fb4cae01c6a89c4e8ea7b3dcc79db7730a2e6ecd7ea3`  
		Last Modified: Wed, 02 Jul 2025 09:13:04 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c85f68cfc7b7c6424cc6a6bc39794c212bc7adafc690678ee7fdeb8ff312a`  
		Last Modified: Wed, 02 Jul 2025 09:13:05 GMT  
		Size: 22.7 MB (22701403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:196be4d53d6c572779baaa62ec73ebd6a9f4963022f3dcca35a0043193697ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23668558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410c13f7b9600825b3dfb1be1ce8b3c94143540d8bab3ac8e4e96cc5e4d07641`

```dockerfile
```

-	Layers:
	-	`sha256:d5eed918dd5363ea0483b9860d9c6b26650176d4190ad3d16016c4b51954c348`  
		Last Modified: Wed, 02 Jul 2025 10:17:35 GMT  
		Size: 23.7 MB (23652030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2b606950b1500ae1e3400c90f11279deae645f8b1193281e9eda71b16772a7`  
		Last Modified: Wed, 02 Jul 2025 10:17:36 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:00fbf8e467786a587de1f3552cf298cfb1751ab9d1338956dd3b56beb3eca96e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:acf128849a3369507a6a4ceb548b8b88495776e5441fc42fc2f0044a6ff5f341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.9 MB (954901851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3779b408ba04f4d762b59d53198cf1fa73d196c3ce5661a1ffa9cb84d08dbc06`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f13fa6ab986f8a280cbd08782691746d11fdd96ae24043b73dd15954626359`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 1.2 MB (1214019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3bc629d3d1edb01c22bf6804bd1a42bf1f18eb8cd6d4ca072796ff2ed0898`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 6.0 MB (5991642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627cb8e9cbe801b080f67968716035054c4fb0334ae5bb622abd71b03a74ff8`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 97.2 KB (97159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8193ec0dfde00ae6a93f483fdb9c3d553d9555dd62946ee33781171b80f681e`  
		Last Modified: Wed, 02 Jul 2025 04:13:12 GMT  
		Size: 104.6 MB (104552104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e5ec44afb815e06d47e77ab069ab5bb950f7f36b751ad8b2103057d98c4ce`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fd9e74e6fd05a516cea0b71abc9baf18606effe4543e6337901025fbe4eb0`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 98.0 MB (97959535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c6f0311484b8b07ef741892d26236263307cdb1798f283cfcca3109fe97a`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 363.5 KB (363513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a88d1d3274993db9497c692378fd53e3a7ef81905672d82b75b5e9b33ffc9`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f8638479e522ab3779b4570a1b2c8d65c44b3d80a4f28e78ac598e1efd1419`  
		Last Modified: Wed, 02 Jul 2025 05:11:20 GMT  
		Size: 23.3 MB (23314712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81167327080034190e8b4afacb869f0b09a72dd3d0ecde42cc9a5c1785c39567`  
		Last Modified: Wed, 02 Jul 2025 08:12:56 GMT  
		Size: 691.9 MB (691870812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:ea19cacfab70339d3a693bd9e1f937b81573c5d84e2e5c51b09b11ae2eade7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58716654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec8a2da138eeb95ff9204fd21911a109d9eb9d70f85ff46839f82f342845506`

```dockerfile
```

-	Layers:
	-	`sha256:e786222e804489e19ca314d5ecb462a3df364bea472bcbdd15a6d618606eeb0e`  
		Last Modified: Wed, 02 Jul 2025 07:17:26 GMT  
		Size: 58.7 MB (58707260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce3902ff94e48b704ee061aa1c8ea640ddfd11d15095cb844414418f93be4b5`  
		Last Modified: Wed, 02 Jul 2025 07:17:27 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eca65ab72d71d70f5620090f363ca0c4aeb32f6fe8a1067ce4b5738fc0d83005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.2 MB (915232898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2749cbeed3567bb1371d1ffddd215af75a68e2b3b4ddf5029bf89931c1c6561e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc154224d775815f0aab30a07a0cba6ca4082b1f09da8355b44aae7c044072`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 1.2 MB (1214196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ffaf60e2489601d3859a11b446b804c7ffb4fe05453885d2411185892b572`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 5.9 MB (5936657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf686f829ca2dfefc31c3f2441114fb0b8ee56bd206a8a7a392cafbf51cd46a`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 97.3 KB (97292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0cd27ef0672066e0e81841bf837a1be14b43325e417a2be373825e06849ca`  
		Last Modified: Wed, 02 Jul 2025 06:25:55 GMT  
		Size: 102.2 MB (102244927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e7d9c15fcb9e5e2600df9e9dece9c12d2a99ea9e8ff316cbfb1e1b8492daa`  
		Last Modified: Wed, 02 Jul 2025 06:25:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7d044aa87162eeff0af0fe069ace5000d2c1f33d306ddd4ede182d486e8faa`  
		Last Modified: Wed, 02 Jul 2025 09:13:10 GMT  
		Size: 95.5 MB (95508902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861b98f01417c33693842112a9d40af4ca6b0e4748e48ded467bec59890f9a4b`  
		Last Modified: Wed, 02 Jul 2025 09:13:03 GMT  
		Size: 363.5 KB (363507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37abcabf329d1b7e5974fb4cae01c6a89c4e8ea7b3dcc79db7730a2e6ecd7ea3`  
		Last Modified: Wed, 02 Jul 2025 09:13:04 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c85f68cfc7b7c6424cc6a6bc39794c212bc7adafc690678ee7fdeb8ff312a`  
		Last Modified: Wed, 02 Jul 2025 09:13:05 GMT  
		Size: 22.7 MB (22701403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96c7910e464f00199c36221b3c19d162eef56f9f1ed131e0c291da5e87d982c`  
		Last Modified: Wed, 02 Jul 2025 16:28:11 GMT  
		Size: 659.8 MB (659804070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:96cdf6d5655981c122e9672473e0bd33e21e7a64296579a62eb2d989163df125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58673810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a91b63f812310eec0f4709d51cdf5a21643e80667ebed9e8b89f2db2cee5da4`

```dockerfile
```

-	Layers:
	-	`sha256:71aa01dcd6f58d6a080fcefb6be404c3f2a45a912ebc305abcf40299b79651ae`  
		Last Modified: Wed, 02 Jul 2025 16:18:41 GMT  
		Size: 58.7 MB (58664335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8f4ca7b1888c2dc560ef300c12524743681a5ff3c2bafa6350bfe9b267bdc20`  
		Last Modified: Wed, 02 Jul 2025 16:18:42 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:00fbf8e467786a587de1f3552cf298cfb1751ab9d1338956dd3b56beb3eca96e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:acf128849a3369507a6a4ceb548b8b88495776e5441fc42fc2f0044a6ff5f341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.9 MB (954901851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3779b408ba04f4d762b59d53198cf1fa73d196c3ce5661a1ffa9cb84d08dbc06`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f13fa6ab986f8a280cbd08782691746d11fdd96ae24043b73dd15954626359`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 1.2 MB (1214019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3bc629d3d1edb01c22bf6804bd1a42bf1f18eb8cd6d4ca072796ff2ed0898`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 6.0 MB (5991642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627cb8e9cbe801b080f67968716035054c4fb0334ae5bb622abd71b03a74ff8`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 97.2 KB (97159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8193ec0dfde00ae6a93f483fdb9c3d553d9555dd62946ee33781171b80f681e`  
		Last Modified: Wed, 02 Jul 2025 04:13:12 GMT  
		Size: 104.6 MB (104552104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e5ec44afb815e06d47e77ab069ab5bb950f7f36b751ad8b2103057d98c4ce`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fd9e74e6fd05a516cea0b71abc9baf18606effe4543e6337901025fbe4eb0`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 98.0 MB (97959535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c6f0311484b8b07ef741892d26236263307cdb1798f283cfcca3109fe97a`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 363.5 KB (363513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a88d1d3274993db9497c692378fd53e3a7ef81905672d82b75b5e9b33ffc9`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f8638479e522ab3779b4570a1b2c8d65c44b3d80a4f28e78ac598e1efd1419`  
		Last Modified: Wed, 02 Jul 2025 05:11:20 GMT  
		Size: 23.3 MB (23314712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81167327080034190e8b4afacb869f0b09a72dd3d0ecde42cc9a5c1785c39567`  
		Last Modified: Wed, 02 Jul 2025 08:12:56 GMT  
		Size: 691.9 MB (691870812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:ea19cacfab70339d3a693bd9e1f937b81573c5d84e2e5c51b09b11ae2eade7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58716654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec8a2da138eeb95ff9204fd21911a109d9eb9d70f85ff46839f82f342845506`

```dockerfile
```

-	Layers:
	-	`sha256:e786222e804489e19ca314d5ecb462a3df364bea472bcbdd15a6d618606eeb0e`  
		Last Modified: Wed, 02 Jul 2025 07:17:26 GMT  
		Size: 58.7 MB (58707260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce3902ff94e48b704ee061aa1c8ea640ddfd11d15095cb844414418f93be4b5`  
		Last Modified: Wed, 02 Jul 2025 07:17:27 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eca65ab72d71d70f5620090f363ca0c4aeb32f6fe8a1067ce4b5738fc0d83005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.2 MB (915232898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2749cbeed3567bb1371d1ffddd215af75a68e2b3b4ddf5029bf89931c1c6561e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc154224d775815f0aab30a07a0cba6ca4082b1f09da8355b44aae7c044072`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 1.2 MB (1214196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ffaf60e2489601d3859a11b446b804c7ffb4fe05453885d2411185892b572`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 5.9 MB (5936657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf686f829ca2dfefc31c3f2441114fb0b8ee56bd206a8a7a392cafbf51cd46a`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 97.3 KB (97292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0cd27ef0672066e0e81841bf837a1be14b43325e417a2be373825e06849ca`  
		Last Modified: Wed, 02 Jul 2025 06:25:55 GMT  
		Size: 102.2 MB (102244927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e7d9c15fcb9e5e2600df9e9dece9c12d2a99ea9e8ff316cbfb1e1b8492daa`  
		Last Modified: Wed, 02 Jul 2025 06:25:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7d044aa87162eeff0af0fe069ace5000d2c1f33d306ddd4ede182d486e8faa`  
		Last Modified: Wed, 02 Jul 2025 09:13:10 GMT  
		Size: 95.5 MB (95508902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861b98f01417c33693842112a9d40af4ca6b0e4748e48ded467bec59890f9a4b`  
		Last Modified: Wed, 02 Jul 2025 09:13:03 GMT  
		Size: 363.5 KB (363507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37abcabf329d1b7e5974fb4cae01c6a89c4e8ea7b3dcc79db7730a2e6ecd7ea3`  
		Last Modified: Wed, 02 Jul 2025 09:13:04 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c85f68cfc7b7c6424cc6a6bc39794c212bc7adafc690678ee7fdeb8ff312a`  
		Last Modified: Wed, 02 Jul 2025 09:13:05 GMT  
		Size: 22.7 MB (22701403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96c7910e464f00199c36221b3c19d162eef56f9f1ed131e0c291da5e87d982c`  
		Last Modified: Wed, 02 Jul 2025 16:28:11 GMT  
		Size: 659.8 MB (659804070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:96cdf6d5655981c122e9672473e0bd33e21e7a64296579a62eb2d989163df125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58673810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a91b63f812310eec0f4709d51cdf5a21643e80667ebed9e8b89f2db2cee5da4`

```dockerfile
```

-	Layers:
	-	`sha256:71aa01dcd6f58d6a080fcefb6be404c3f2a45a912ebc305abcf40299b79651ae`  
		Last Modified: Wed, 02 Jul 2025 16:18:41 GMT  
		Size: 58.7 MB (58664335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8f4ca7b1888c2dc560ef300c12524743681a5ff3c2bafa6350bfe9b267bdc20`  
		Last Modified: Wed, 02 Jul 2025 16:18:42 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:6faa295af1dddacafa9e4f381c9500ca2a7ee215503056f5eab2f450a5f267e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e4be824130baa1dcac4398eed53559f98ecac0a89315f8681490a8a0c5271dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263031039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866fe3a0fcff7b5c28380b45856b8ff5066e9da8ee6b6d1268bdd8b78bf13448`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f13fa6ab986f8a280cbd08782691746d11fdd96ae24043b73dd15954626359`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 1.2 MB (1214019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3bc629d3d1edb01c22bf6804bd1a42bf1f18eb8cd6d4ca072796ff2ed0898`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 6.0 MB (5991642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627cb8e9cbe801b080f67968716035054c4fb0334ae5bb622abd71b03a74ff8`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 97.2 KB (97159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8193ec0dfde00ae6a93f483fdb9c3d553d9555dd62946ee33781171b80f681e`  
		Last Modified: Wed, 02 Jul 2025 04:13:12 GMT  
		Size: 104.6 MB (104552104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e5ec44afb815e06d47e77ab069ab5bb950f7f36b751ad8b2103057d98c4ce`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fd9e74e6fd05a516cea0b71abc9baf18606effe4543e6337901025fbe4eb0`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 98.0 MB (97959535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c6f0311484b8b07ef741892d26236263307cdb1798f283cfcca3109fe97a`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 363.5 KB (363513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a88d1d3274993db9497c692378fd53e3a7ef81905672d82b75b5e9b33ffc9`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f8638479e522ab3779b4570a1b2c8d65c44b3d80a4f28e78ac598e1efd1419`  
		Last Modified: Wed, 02 Jul 2025 05:11:20 GMT  
		Size: 23.3 MB (23314712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:1eb9c3e49979825d585296aacc13e3ecd821ef674fd5014872f6bd2e5ac9766f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23682649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27eaee7b91b45acb572a6c20dbc784f3216e6219d298ae4813ecba901d400a2`

```dockerfile
```

-	Layers:
	-	`sha256:bf1668290a349236f80b93f19e5fdaa82f67b7182afdc87d5ef5e261653a87de`  
		Last Modified: Wed, 02 Jul 2025 07:17:22 GMT  
		Size: 23.7 MB (23666259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1547542991f104030d7f07dcbe29f6d2d14ecd700dd4fe8caa74a9dd1fa2a939`  
		Last Modified: Wed, 02 Jul 2025 07:17:23 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b9f1c3872615663f504b882b66503d267ed703123596b276ed8a477e3380c451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255428828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed6b1b8d0ad8944e97a0a7e04f56276c1f560eb1517de98e0692579c7b9e9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc154224d775815f0aab30a07a0cba6ca4082b1f09da8355b44aae7c044072`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 1.2 MB (1214196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ffaf60e2489601d3859a11b446b804c7ffb4fe05453885d2411185892b572`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 5.9 MB (5936657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf686f829ca2dfefc31c3f2441114fb0b8ee56bd206a8a7a392cafbf51cd46a`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 97.3 KB (97292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0cd27ef0672066e0e81841bf837a1be14b43325e417a2be373825e06849ca`  
		Last Modified: Wed, 02 Jul 2025 06:25:55 GMT  
		Size: 102.2 MB (102244927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e7d9c15fcb9e5e2600df9e9dece9c12d2a99ea9e8ff316cbfb1e1b8492daa`  
		Last Modified: Wed, 02 Jul 2025 06:25:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7d044aa87162eeff0af0fe069ace5000d2c1f33d306ddd4ede182d486e8faa`  
		Last Modified: Wed, 02 Jul 2025 09:13:10 GMT  
		Size: 95.5 MB (95508902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861b98f01417c33693842112a9d40af4ca6b0e4748e48ded467bec59890f9a4b`  
		Last Modified: Wed, 02 Jul 2025 09:13:03 GMT  
		Size: 363.5 KB (363507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37abcabf329d1b7e5974fb4cae01c6a89c4e8ea7b3dcc79db7730a2e6ecd7ea3`  
		Last Modified: Wed, 02 Jul 2025 09:13:04 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c85f68cfc7b7c6424cc6a6bc39794c212bc7adafc690678ee7fdeb8ff312a`  
		Last Modified: Wed, 02 Jul 2025 09:13:05 GMT  
		Size: 22.7 MB (22701403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:196be4d53d6c572779baaa62ec73ebd6a9f4963022f3dcca35a0043193697ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23668558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410c13f7b9600825b3dfb1be1ce8b3c94143540d8bab3ac8e4e96cc5e4d07641`

```dockerfile
```

-	Layers:
	-	`sha256:d5eed918dd5363ea0483b9860d9c6b26650176d4190ad3d16016c4b51954c348`  
		Last Modified: Wed, 02 Jul 2025 10:17:35 GMT  
		Size: 23.7 MB (23652030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2b606950b1500ae1e3400c90f11279deae645f8b1193281e9eda71b16772a7`  
		Last Modified: Wed, 02 Jul 2025 10:17:36 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:6faa295af1dddacafa9e4f381c9500ca2a7ee215503056f5eab2f450a5f267e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:e4be824130baa1dcac4398eed53559f98ecac0a89315f8681490a8a0c5271dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263031039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866fe3a0fcff7b5c28380b45856b8ff5066e9da8ee6b6d1268bdd8b78bf13448`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f13fa6ab986f8a280cbd08782691746d11fdd96ae24043b73dd15954626359`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 1.2 MB (1214019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3bc629d3d1edb01c22bf6804bd1a42bf1f18eb8cd6d4ca072796ff2ed0898`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 6.0 MB (5991642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627cb8e9cbe801b080f67968716035054c4fb0334ae5bb622abd71b03a74ff8`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 97.2 KB (97159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8193ec0dfde00ae6a93f483fdb9c3d553d9555dd62946ee33781171b80f681e`  
		Last Modified: Wed, 02 Jul 2025 04:13:12 GMT  
		Size: 104.6 MB (104552104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e5ec44afb815e06d47e77ab069ab5bb950f7f36b751ad8b2103057d98c4ce`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60fd9e74e6fd05a516cea0b71abc9baf18606effe4543e6337901025fbe4eb0`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 98.0 MB (97959535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c3c6f0311484b8b07ef741892d26236263307cdb1798f283cfcca3109fe97a`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 363.5 KB (363513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a88d1d3274993db9497c692378fd53e3a7ef81905672d82b75b5e9b33ffc9`  
		Last Modified: Wed, 02 Jul 2025 05:11:18 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f8638479e522ab3779b4570a1b2c8d65c44b3d80a4f28e78ac598e1efd1419`  
		Last Modified: Wed, 02 Jul 2025 05:11:20 GMT  
		Size: 23.3 MB (23314712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:1eb9c3e49979825d585296aacc13e3ecd821ef674fd5014872f6bd2e5ac9766f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23682649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27eaee7b91b45acb572a6c20dbc784f3216e6219d298ae4813ecba901d400a2`

```dockerfile
```

-	Layers:
	-	`sha256:bf1668290a349236f80b93f19e5fdaa82f67b7182afdc87d5ef5e261653a87de`  
		Last Modified: Wed, 02 Jul 2025 07:17:22 GMT  
		Size: 23.7 MB (23666259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1547542991f104030d7f07dcbe29f6d2d14ecd700dd4fe8caa74a9dd1fa2a939`  
		Last Modified: Wed, 02 Jul 2025 07:17:23 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b9f1c3872615663f504b882b66503d267ed703123596b276ed8a477e3380c451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255428828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed6b1b8d0ad8944e97a0a7e04f56276c1f560eb1517de98e0692579c7b9e9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc154224d775815f0aab30a07a0cba6ca4082b1f09da8355b44aae7c044072`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 1.2 MB (1214196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ffaf60e2489601d3859a11b446b804c7ffb4fe05453885d2411185892b572`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 5.9 MB (5936657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf686f829ca2dfefc31c3f2441114fb0b8ee56bd206a8a7a392cafbf51cd46a`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 97.3 KB (97292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0cd27ef0672066e0e81841bf837a1be14b43325e417a2be373825e06849ca`  
		Last Modified: Wed, 02 Jul 2025 06:25:55 GMT  
		Size: 102.2 MB (102244927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e7d9c15fcb9e5e2600df9e9dece9c12d2a99ea9e8ff316cbfb1e1b8492daa`  
		Last Modified: Wed, 02 Jul 2025 06:25:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7d044aa87162eeff0af0fe069ace5000d2c1f33d306ddd4ede182d486e8faa`  
		Last Modified: Wed, 02 Jul 2025 09:13:10 GMT  
		Size: 95.5 MB (95508902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861b98f01417c33693842112a9d40af4ca6b0e4748e48ded467bec59890f9a4b`  
		Last Modified: Wed, 02 Jul 2025 09:13:03 GMT  
		Size: 363.5 KB (363507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37abcabf329d1b7e5974fb4cae01c6a89c4e8ea7b3dcc79db7730a2e6ecd7ea3`  
		Last Modified: Wed, 02 Jul 2025 09:13:04 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c85f68cfc7b7c6424cc6a6bc39794c212bc7adafc690678ee7fdeb8ff312a`  
		Last Modified: Wed, 02 Jul 2025 09:13:05 GMT  
		Size: 22.7 MB (22701403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:196be4d53d6c572779baaa62ec73ebd6a9f4963022f3dcca35a0043193697ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23668558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410c13f7b9600825b3dfb1be1ce8b3c94143540d8bab3ac8e4e96cc5e4d07641`

```dockerfile
```

-	Layers:
	-	`sha256:d5eed918dd5363ea0483b9860d9c6b26650176d4190ad3d16016c4b51954c348`  
		Last Modified: Wed, 02 Jul 2025 10:17:35 GMT  
		Size: 23.7 MB (23652030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2b606950b1500ae1e3400c90f11279deae645f8b1193281e9eda71b16772a7`  
		Last Modified: Wed, 02 Jul 2025 10:17:36 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:d21de608727d2a35d8c18d046a6831095f606625c02801f556cfc8c2a1a48ff3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:53ce411ffe6a22cffe914ca2edc054bd4eae46531d3b2091bb78126ae1817a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141390805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9b0c38263a503d36ee6d0272961b8d6ef8c31e46affe7558c99e3a2dbaf978`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f13fa6ab986f8a280cbd08782691746d11fdd96ae24043b73dd15954626359`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 1.2 MB (1214019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3bc629d3d1edb01c22bf6804bd1a42bf1f18eb8cd6d4ca072796ff2ed0898`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 6.0 MB (5991642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627cb8e9cbe801b080f67968716035054c4fb0334ae5bb622abd71b03a74ff8`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 97.2 KB (97159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8193ec0dfde00ae6a93f483fdb9c3d553d9555dd62946ee33781171b80f681e`  
		Last Modified: Wed, 02 Jul 2025 04:13:12 GMT  
		Size: 104.6 MB (104552104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e5ec44afb815e06d47e77ab069ab5bb950f7f36b751ad8b2103057d98c4ce`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:da7fe027355a19b72156ad4422c4b03f3038dc891e8bc7a0abf8e5093d77cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17669194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78cc6f04c930c7cb2866474ef63501f9566e893767c933439f61b9eb2fb10f0`

```dockerfile
```

-	Layers:
	-	`sha256:fef8aa11b00286b2ed95500e594643596e2ae4cb0500ec743c3c0520c65beee8`  
		Last Modified: Wed, 02 Jul 2025 07:17:34 GMT  
		Size: 17.7 MB (17654538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f2c9596bc92f7fb415f438d983a1492d6f6db30613f2169cda236f0a96bcd`  
		Last Modified: Wed, 02 Jul 2025 07:17:35 GMT  
		Size: 14.7 KB (14656 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1b19dc5b53055508d9855af4aeb600e6f61f833dc6a35b30337e2b558ed92b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136852540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca62413fef99d06016bc734c24a1bb668aa0c5b2ef6e8a85030f04fdec60a6a5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc154224d775815f0aab30a07a0cba6ca4082b1f09da8355b44aae7c044072`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 1.2 MB (1214196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ffaf60e2489601d3859a11b446b804c7ffb4fe05453885d2411185892b572`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 5.9 MB (5936657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf686f829ca2dfefc31c3f2441114fb0b8ee56bd206a8a7a392cafbf51cd46a`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 97.3 KB (97292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0cd27ef0672066e0e81841bf837a1be14b43325e417a2be373825e06849ca`  
		Last Modified: Wed, 02 Jul 2025 06:25:55 GMT  
		Size: 102.2 MB (102244927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e7d9c15fcb9e5e2600df9e9dece9c12d2a99ea9e8ff316cbfb1e1b8492daa`  
		Last Modified: Wed, 02 Jul 2025 06:25:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fcc3c3793b1edc29b5eee5a73a497253ab49b2dacf209e82ee4427047ecc2964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17628422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f40cf9a544a74a9bb33abb51c00f700e8f54b3194e42448b9187c3ad3f16c62`

```dockerfile
```

-	Layers:
	-	`sha256:e3fd9463f0b226980fa1789b9f8ba6f8137cd8ab47aaca81bfd8d44bf1b139ac`  
		Last Modified: Wed, 02 Jul 2025 07:17:47 GMT  
		Size: 17.6 MB (17613641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc28a970cca1c2373b07dfd44fd41f425f65353da4e6d68e87d6d33351441be`  
		Last Modified: Wed, 02 Jul 2025 07:17:48 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:d21de608727d2a35d8c18d046a6831095f606625c02801f556cfc8c2a1a48ff3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:53ce411ffe6a22cffe914ca2edc054bd4eae46531d3b2091bb78126ae1817a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141390805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9b0c38263a503d36ee6d0272961b8d6ef8c31e46affe7558c99e3a2dbaf978`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f13fa6ab986f8a280cbd08782691746d11fdd96ae24043b73dd15954626359`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 1.2 MB (1214019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3bc629d3d1edb01c22bf6804bd1a42bf1f18eb8cd6d4ca072796ff2ed0898`  
		Last Modified: Wed, 02 Jul 2025 04:13:06 GMT  
		Size: 6.0 MB (5991642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9627cb8e9cbe801b080f67968716035054c4fb0334ae5bb622abd71b03a74ff8`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 97.2 KB (97159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8193ec0dfde00ae6a93f483fdb9c3d553d9555dd62946ee33781171b80f681e`  
		Last Modified: Wed, 02 Jul 2025 04:13:12 GMT  
		Size: 104.6 MB (104552104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e5ec44afb815e06d47e77ab069ab5bb950f7f36b751ad8b2103057d98c4ce`  
		Last Modified: Wed, 02 Jul 2025 04:13:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:da7fe027355a19b72156ad4422c4b03f3038dc891e8bc7a0abf8e5093d77cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17669194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78cc6f04c930c7cb2866474ef63501f9566e893767c933439f61b9eb2fb10f0`

```dockerfile
```

-	Layers:
	-	`sha256:fef8aa11b00286b2ed95500e594643596e2ae4cb0500ec743c3c0520c65beee8`  
		Last Modified: Wed, 02 Jul 2025 07:17:34 GMT  
		Size: 17.7 MB (17654538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48f2c9596bc92f7fb415f438d983a1492d6f6db30613f2169cda236f0a96bcd`  
		Last Modified: Wed, 02 Jul 2025 07:17:35 GMT  
		Size: 14.7 KB (14656 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1b19dc5b53055508d9855af4aeb600e6f61f833dc6a35b30337e2b558ed92b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136852540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca62413fef99d06016bc734c24a1bb668aa0c5b2ef6e8a85030f04fdec60a6a5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc154224d775815f0aab30a07a0cba6ca4082b1f09da8355b44aae7c044072`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 1.2 MB (1214196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ffaf60e2489601d3859a11b446b804c7ffb4fe05453885d2411185892b572`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 5.9 MB (5936657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf686f829ca2dfefc31c3f2441114fb0b8ee56bd206a8a7a392cafbf51cd46a`  
		Last Modified: Wed, 02 Jul 2025 06:25:44 GMT  
		Size: 97.3 KB (97292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e0cd27ef0672066e0e81841bf837a1be14b43325e417a2be373825e06849ca`  
		Last Modified: Wed, 02 Jul 2025 06:25:55 GMT  
		Size: 102.2 MB (102244927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548e7d9c15fcb9e5e2600df9e9dece9c12d2a99ea9e8ff316cbfb1e1b8492daa`  
		Last Modified: Wed, 02 Jul 2025 06:25:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:fcc3c3793b1edc29b5eee5a73a497253ab49b2dacf209e82ee4427047ecc2964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17628422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f40cf9a544a74a9bb33abb51c00f700e8f54b3194e42448b9187c3ad3f16c62`

```dockerfile
```

-	Layers:
	-	`sha256:e3fd9463f0b226980fa1789b9f8ba6f8137cd8ab47aaca81bfd8d44bf1b139ac`  
		Last Modified: Wed, 02 Jul 2025 07:17:47 GMT  
		Size: 17.6 MB (17613641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc28a970cca1c2373b07dfd44fd41f425f65353da4e6d68e87d6d33351441be`  
		Last Modified: Wed, 02 Jul 2025 07:17:48 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:c759f6424661403697c7853a851207a2ab58781bdb89c240339541252dd8a947
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:f5c8f6ebc2e4033533eb045ff8952a52c8f14eda9d601ba54187ab1d7a25e438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295690709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5c46408d6eb6acac780c416c3911f89619489c478efe80799bddebf4c1f3af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad66aa49d81043255b5a68fe8370c44ed1bb417a34d56921b5b6e54aad5e8d43`  
		Last Modified: Wed, 02 Jul 2025 05:11:35 GMT  
		Size: 110.2 MB (110183478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22750c2ee1c83973e70b463b77f04591f765297af3b530faf78d8f8ed830ff1`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 368.0 KB (367976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63a806b355a8c725520e98243260911eac03cbb661780b860888e786128635`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc65c67c30109fc2ccd6dc11a29c0f2680360d72516f305af61d8dfe881a29`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (27965355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:7582b6c1248178e77adfae99361728288005df8f0abc9d7d0663ce2457b19a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24546251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d89f79ee0222f23486dfa10abbdbd26946edf33232e03ca8f9069e9e56c08de`

```dockerfile
```

-	Layers:
	-	`sha256:33e7ca868a61f1ade7ef63d4016c645b019cb17ab5bd8aacba13bd01eee266b8`  
		Last Modified: Wed, 02 Jul 2025 07:17:41 GMT  
		Size: 24.5 MB (24529587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8245d24d84e6d877693b0225acc3c0a1f1db6df7a10b132c28bbdd4947eeb5f3`  
		Last Modified: Wed, 02 Jul 2025 07:17:42 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3f0664e804cdece42022fc377e0dea5bff9bd0d26d30b632a668b29c15dada34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284134893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26d377b653accbd2690e4bb391d3a00f274f558248e288e1f357fdf66fadd34`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736106426b42d80857f05a708ed6cd5e9650eda12b095660b23f5188719dc07`  
		Last Modified: Wed, 02 Jul 2025 09:16:05 GMT  
		Size: 105.6 MB (105590987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f6f9545192a9608660f621dde4c7267a9c0757e2be323d7aed12460e2f2572`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 368.0 KB (367978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67487dd6e705c0eea7666a23c0fe353532dd278d9f0f5591a0b8f530bf461d09`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df12486781526bb96d0db46f630672fe88462cf8622b5f864aaec2e770eea30`  
		Last Modified: Wed, 02 Jul 2025 09:16:00 GMT  
		Size: 27.1 MB (27072114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:e6be0bdcda31b2afd199507e994ff67bbfc8d0ce905da4e78a501a43e73b8b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24568673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3495f419552b8f23bbb157ab88b37378bf20d2f34d54e6535a4c832f82bbb9`

```dockerfile
```

-	Layers:
	-	`sha256:f18f7a78abb706290d89fa3915ea7be74c3e39cc4aec179affa63d732cc96e9e`  
		Last Modified: Wed, 02 Jul 2025 10:17:50 GMT  
		Size: 24.6 MB (24551860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a283f2837d521fb527f032d19868776e4b9b126eda033fb325f5fdc0731d2fb0`  
		Last Modified: Wed, 02 Jul 2025 10:17:50 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:d7ce3cfbeb723fe4bf8ff9b9d051688de0233809b77f2d39022b6fa39dab2953
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:d719d6624830384c299e913517dc1f3ac53ee44fb34cb13dc0e3e5e72b5629aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076313178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012ba2b95052a7e654e7f01271510eccf4129f8f9d61ee680406dd4092047219`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad66aa49d81043255b5a68fe8370c44ed1bb417a34d56921b5b6e54aad5e8d43`  
		Last Modified: Wed, 02 Jul 2025 05:11:35 GMT  
		Size: 110.2 MB (110183478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22750c2ee1c83973e70b463b77f04591f765297af3b530faf78d8f8ed830ff1`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 368.0 KB (367976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63a806b355a8c725520e98243260911eac03cbb661780b860888e786128635`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc65c67c30109fc2ccd6dc11a29c0f2680360d72516f305af61d8dfe881a29`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (27965355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acadc09cb60efa4d4bce02a9f89e9281004c6b71b61d3b0a2dde3b2ea243caa4`  
		Last Modified: Wed, 02 Jul 2025 08:21:39 GMT  
		Size: 780.6 MB (780622469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3c5de313d3bdaadec85ebaaa22768414f6377de6fef7eba3c43c515d263a4937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60684111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73037ae8af05bdebfe68ebd4550991e6b12ff11c8733be00615f92a66138aa97`

```dockerfile
```

-	Layers:
	-	`sha256:4cedc11a742aa7c12e683330f376d5466430bc23f91170239fcfda4ef8760e14`  
		Last Modified: Wed, 02 Jul 2025 07:17:48 GMT  
		Size: 60.7 MB (60674729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8076a3c706cb06872a3dc48318a5869c82127f63e305856f04e7d51d48cbedca`  
		Last Modified: Wed, 02 Jul 2025 07:17:50 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d3cdd9a49764a4b1995d77b618bd99ff4a08b4013e28ce46eb7f4c53a4b9e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.9 MB (974939252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e46283ce15093f2702ed0f47fe580db78018050343196c7b50097fdab5ed4f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736106426b42d80857f05a708ed6cd5e9650eda12b095660b23f5188719dc07`  
		Last Modified: Wed, 02 Jul 2025 09:16:05 GMT  
		Size: 105.6 MB (105590987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f6f9545192a9608660f621dde4c7267a9c0757e2be323d7aed12460e2f2572`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 368.0 KB (367978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67487dd6e705c0eea7666a23c0fe353532dd278d9f0f5591a0b8f530bf461d09`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df12486781526bb96d0db46f630672fe88462cf8622b5f864aaec2e770eea30`  
		Last Modified: Wed, 02 Jul 2025 09:16:00 GMT  
		Size: 27.1 MB (27072114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc0dce9d2bcb4504b0533c3588df6962826356537ce90e83fe0fd527f9a94f9`  
		Last Modified: Wed, 02 Jul 2025 16:25:39 GMT  
		Size: 690.8 MB (690804359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:23b8beb898ca60de4f68fe72226df1e6a92fd57874f852a8542563e2dd9eb396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60614718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbed990af87636b53e5e5b1fbc56b88716f849b564cabb500d7f45209354976`

```dockerfile
```

-	Layers:
	-	`sha256:1f8e655a47b49af83a8c1de004ea3f9f7ee72191e7f73b65516bd7ab58793eaa`  
		Last Modified: Wed, 02 Jul 2025 16:19:01 GMT  
		Size: 60.6 MB (60605256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096c8afb5ed6a96f78b15340b1dd99aefd3e2fdfcbceedf154b24eb5e2cb6916`  
		Last Modified: Wed, 02 Jul 2025 16:19:03 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:d7ce3cfbeb723fe4bf8ff9b9d051688de0233809b77f2d39022b6fa39dab2953
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:d719d6624830384c299e913517dc1f3ac53ee44fb34cb13dc0e3e5e72b5629aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076313178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012ba2b95052a7e654e7f01271510eccf4129f8f9d61ee680406dd4092047219`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad66aa49d81043255b5a68fe8370c44ed1bb417a34d56921b5b6e54aad5e8d43`  
		Last Modified: Wed, 02 Jul 2025 05:11:35 GMT  
		Size: 110.2 MB (110183478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22750c2ee1c83973e70b463b77f04591f765297af3b530faf78d8f8ed830ff1`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 368.0 KB (367976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63a806b355a8c725520e98243260911eac03cbb661780b860888e786128635`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc65c67c30109fc2ccd6dc11a29c0f2680360d72516f305af61d8dfe881a29`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (27965355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acadc09cb60efa4d4bce02a9f89e9281004c6b71b61d3b0a2dde3b2ea243caa4`  
		Last Modified: Wed, 02 Jul 2025 08:21:39 GMT  
		Size: 780.6 MB (780622469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:3c5de313d3bdaadec85ebaaa22768414f6377de6fef7eba3c43c515d263a4937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60684111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73037ae8af05bdebfe68ebd4550991e6b12ff11c8733be00615f92a66138aa97`

```dockerfile
```

-	Layers:
	-	`sha256:4cedc11a742aa7c12e683330f376d5466430bc23f91170239fcfda4ef8760e14`  
		Last Modified: Wed, 02 Jul 2025 07:17:48 GMT  
		Size: 60.7 MB (60674729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8076a3c706cb06872a3dc48318a5869c82127f63e305856f04e7d51d48cbedca`  
		Last Modified: Wed, 02 Jul 2025 07:17:50 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d3cdd9a49764a4b1995d77b618bd99ff4a08b4013e28ce46eb7f4c53a4b9e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.9 MB (974939252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e46283ce15093f2702ed0f47fe580db78018050343196c7b50097fdab5ed4f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736106426b42d80857f05a708ed6cd5e9650eda12b095660b23f5188719dc07`  
		Last Modified: Wed, 02 Jul 2025 09:16:05 GMT  
		Size: 105.6 MB (105590987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f6f9545192a9608660f621dde4c7267a9c0757e2be323d7aed12460e2f2572`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 368.0 KB (367978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67487dd6e705c0eea7666a23c0fe353532dd278d9f0f5591a0b8f530bf461d09`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df12486781526bb96d0db46f630672fe88462cf8622b5f864aaec2e770eea30`  
		Last Modified: Wed, 02 Jul 2025 09:16:00 GMT  
		Size: 27.1 MB (27072114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc0dce9d2bcb4504b0533c3588df6962826356537ce90e83fe0fd527f9a94f9`  
		Last Modified: Wed, 02 Jul 2025 16:25:39 GMT  
		Size: 690.8 MB (690804359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:23b8beb898ca60de4f68fe72226df1e6a92fd57874f852a8542563e2dd9eb396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60614718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbed990af87636b53e5e5b1fbc56b88716f849b564cabb500d7f45209354976`

```dockerfile
```

-	Layers:
	-	`sha256:1f8e655a47b49af83a8c1de004ea3f9f7ee72191e7f73b65516bd7ab58793eaa`  
		Last Modified: Wed, 02 Jul 2025 16:19:01 GMT  
		Size: 60.6 MB (60605256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096c8afb5ed6a96f78b15340b1dd99aefd3e2fdfcbceedf154b24eb5e2cb6916`  
		Last Modified: Wed, 02 Jul 2025 16:19:03 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:c759f6424661403697c7853a851207a2ab58781bdb89c240339541252dd8a947
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:f5c8f6ebc2e4033533eb045ff8952a52c8f14eda9d601ba54187ab1d7a25e438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295690709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5c46408d6eb6acac780c416c3911f89619489c478efe80799bddebf4c1f3af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad66aa49d81043255b5a68fe8370c44ed1bb417a34d56921b5b6e54aad5e8d43`  
		Last Modified: Wed, 02 Jul 2025 05:11:35 GMT  
		Size: 110.2 MB (110183478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22750c2ee1c83973e70b463b77f04591f765297af3b530faf78d8f8ed830ff1`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 368.0 KB (367976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63a806b355a8c725520e98243260911eac03cbb661780b860888e786128635`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc65c67c30109fc2ccd6dc11a29c0f2680360d72516f305af61d8dfe881a29`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (27965355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:7582b6c1248178e77adfae99361728288005df8f0abc9d7d0663ce2457b19a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24546251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d89f79ee0222f23486dfa10abbdbd26946edf33232e03ca8f9069e9e56c08de`

```dockerfile
```

-	Layers:
	-	`sha256:33e7ca868a61f1ade7ef63d4016c645b019cb17ab5bd8aacba13bd01eee266b8`  
		Last Modified: Wed, 02 Jul 2025 07:17:41 GMT  
		Size: 24.5 MB (24529587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8245d24d84e6d877693b0225acc3c0a1f1db6df7a10b132c28bbdd4947eeb5f3`  
		Last Modified: Wed, 02 Jul 2025 07:17:42 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3f0664e804cdece42022fc377e0dea5bff9bd0d26d30b632a668b29c15dada34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284134893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26d377b653accbd2690e4bb391d3a00f274f558248e288e1f357fdf66fadd34`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736106426b42d80857f05a708ed6cd5e9650eda12b095660b23f5188719dc07`  
		Last Modified: Wed, 02 Jul 2025 09:16:05 GMT  
		Size: 105.6 MB (105590987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f6f9545192a9608660f621dde4c7267a9c0757e2be323d7aed12460e2f2572`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 368.0 KB (367978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67487dd6e705c0eea7666a23c0fe353532dd278d9f0f5591a0b8f530bf461d09`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df12486781526bb96d0db46f630672fe88462cf8622b5f864aaec2e770eea30`  
		Last Modified: Wed, 02 Jul 2025 09:16:00 GMT  
		Size: 27.1 MB (27072114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:e6be0bdcda31b2afd199507e994ff67bbfc8d0ce905da4e78a501a43e73b8b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24568673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3495f419552b8f23bbb157ab88b37378bf20d2f34d54e6535a4c832f82bbb9`

```dockerfile
```

-	Layers:
	-	`sha256:f18f7a78abb706290d89fa3915ea7be74c3e39cc4aec179affa63d732cc96e9e`  
		Last Modified: Wed, 02 Jul 2025 10:17:50 GMT  
		Size: 24.6 MB (24551860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a283f2837d521fb527f032d19868776e4b9b126eda033fb325f5fdc0731d2fb0`  
		Last Modified: Wed, 02 Jul 2025 10:17:50 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:c759f6424661403697c7853a851207a2ab58781bdb89c240339541252dd8a947
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:f5c8f6ebc2e4033533eb045ff8952a52c8f14eda9d601ba54187ab1d7a25e438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295690709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5c46408d6eb6acac780c416c3911f89619489c478efe80799bddebf4c1f3af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad66aa49d81043255b5a68fe8370c44ed1bb417a34d56921b5b6e54aad5e8d43`  
		Last Modified: Wed, 02 Jul 2025 05:11:35 GMT  
		Size: 110.2 MB (110183478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22750c2ee1c83973e70b463b77f04591f765297af3b530faf78d8f8ed830ff1`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 368.0 KB (367976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63a806b355a8c725520e98243260911eac03cbb661780b860888e786128635`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc65c67c30109fc2ccd6dc11a29c0f2680360d72516f305af61d8dfe881a29`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (27965355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7582b6c1248178e77adfae99361728288005df8f0abc9d7d0663ce2457b19a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24546251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d89f79ee0222f23486dfa10abbdbd26946edf33232e03ca8f9069e9e56c08de`

```dockerfile
```

-	Layers:
	-	`sha256:33e7ca868a61f1ade7ef63d4016c645b019cb17ab5bd8aacba13bd01eee266b8`  
		Last Modified: Wed, 02 Jul 2025 07:17:41 GMT  
		Size: 24.5 MB (24529587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8245d24d84e6d877693b0225acc3c0a1f1db6df7a10b132c28bbdd4947eeb5f3`  
		Last Modified: Wed, 02 Jul 2025 07:17:42 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3f0664e804cdece42022fc377e0dea5bff9bd0d26d30b632a668b29c15dada34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284134893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26d377b653accbd2690e4bb391d3a00f274f558248e288e1f357fdf66fadd34`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736106426b42d80857f05a708ed6cd5e9650eda12b095660b23f5188719dc07`  
		Last Modified: Wed, 02 Jul 2025 09:16:05 GMT  
		Size: 105.6 MB (105590987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f6f9545192a9608660f621dde4c7267a9c0757e2be323d7aed12460e2f2572`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 368.0 KB (367978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67487dd6e705c0eea7666a23c0fe353532dd278d9f0f5591a0b8f530bf461d09`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df12486781526bb96d0db46f630672fe88462cf8622b5f864aaec2e770eea30`  
		Last Modified: Wed, 02 Jul 2025 09:16:00 GMT  
		Size: 27.1 MB (27072114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e6be0bdcda31b2afd199507e994ff67bbfc8d0ce905da4e78a501a43e73b8b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24568673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3495f419552b8f23bbb157ab88b37378bf20d2f34d54e6535a4c832f82bbb9`

```dockerfile
```

-	Layers:
	-	`sha256:f18f7a78abb706290d89fa3915ea7be74c3e39cc4aec179affa63d732cc96e9e`  
		Last Modified: Wed, 02 Jul 2025 10:17:50 GMT  
		Size: 24.6 MB (24551860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a283f2837d521fb527f032d19868776e4b9b126eda033fb325f5fdc0731d2fb0`  
		Last Modified: Wed, 02 Jul 2025 10:17:50 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:9d2c6cf976c3819b1423d646d71b3571c1ae79b10480bd7b00c73e1e57d19748
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:87a6bec8689eb8299ca5bf7065b994df4345a312cc91333d36afbbf4ae5521fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157171438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c34c30ae19587c16e48deb0e2c79f66ca42a3bd518ff1f9cb128bf4fbac1bbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:57f546e00a2e9a2b998ec6f62f13c7434a948e8bcfca880bacaae5a3a1b525d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18309089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e8b3ebd1c3fd8f991467aaadc8d910478d6de8cbc6e0c485a0d88ebbce2d2f`

```dockerfile
```

-	Layers:
	-	`sha256:ca5040fc8da57ac37a2566346523cd9e4e3d425aff40f2ac565a65c5908bdb25`  
		Last Modified: Wed, 02 Jul 2025 07:17:54 GMT  
		Size: 18.3 MB (18294446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83896e6358063c249e8ce7d16eda8adcd9cd65189a300d3a39a78585b908a25`  
		Last Modified: Wed, 02 Jul 2025 07:17:55 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f732493fe5877da6b04b02156795aa6da912a8e6b6d4649294ec4230b517a550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151101359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce1228054e42dc12e90dd096c6b317e868eef394d4b95d10cb36f71a28dcd86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:768b49f1f18def116d7ac6f02c7f327b839957f935f9ef3ac4e71abc9995edc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18283220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a339e9d643a2a09474de8315d5d2f502d3081f51c1344044b993fe702d7407a`

```dockerfile
```

-	Layers:
	-	`sha256:f26f2c06d2835cc809f9a71ca9f1d7d072e6ca9ea76e7a7d1b2692c80b36be81`  
		Last Modified: Wed, 02 Jul 2025 07:18:07 GMT  
		Size: 18.3 MB (18268452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfef5223b7b48f5fbd8268ff766a086e20b2fc7c9e93e040509cf4fec9f4b716`  
		Last Modified: Wed, 02 Jul 2025 07:18:08 GMT  
		Size: 14.8 KB (14768 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:9d2c6cf976c3819b1423d646d71b3571c1ae79b10480bd7b00c73e1e57d19748
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:87a6bec8689eb8299ca5bf7065b994df4345a312cc91333d36afbbf4ae5521fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157171438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c34c30ae19587c16e48deb0e2c79f66ca42a3bd518ff1f9cb128bf4fbac1bbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:57f546e00a2e9a2b998ec6f62f13c7434a948e8bcfca880bacaae5a3a1b525d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18309089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e8b3ebd1c3fd8f991467aaadc8d910478d6de8cbc6e0c485a0d88ebbce2d2f`

```dockerfile
```

-	Layers:
	-	`sha256:ca5040fc8da57ac37a2566346523cd9e4e3d425aff40f2ac565a65c5908bdb25`  
		Last Modified: Wed, 02 Jul 2025 07:17:54 GMT  
		Size: 18.3 MB (18294446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83896e6358063c249e8ce7d16eda8adcd9cd65189a300d3a39a78585b908a25`  
		Last Modified: Wed, 02 Jul 2025 07:17:55 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f732493fe5877da6b04b02156795aa6da912a8e6b6d4649294ec4230b517a550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151101359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce1228054e42dc12e90dd096c6b317e868eef394d4b95d10cb36f71a28dcd86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:768b49f1f18def116d7ac6f02c7f327b839957f935f9ef3ac4e71abc9995edc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18283220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a339e9d643a2a09474de8315d5d2f502d3081f51c1344044b993fe702d7407a`

```dockerfile
```

-	Layers:
	-	`sha256:f26f2c06d2835cc809f9a71ca9f1d7d072e6ca9ea76e7a7d1b2692c80b36be81`  
		Last Modified: Wed, 02 Jul 2025 07:18:07 GMT  
		Size: 18.3 MB (18268452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfef5223b7b48f5fbd8268ff766a086e20b2fc7c9e93e040509cf4fec9f4b716`  
		Last Modified: Wed, 02 Jul 2025 07:18:08 GMT  
		Size: 14.8 KB (14768 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:ff35b75fc35505ede9607df277b24cdef86d3c082bcd052e8164ef6170923e96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:d1731a84608298b7f9f3fc44a8a1353fe606a84c37d45fc6b68b728027e004da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308239796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fcfdc00a096c70701d65348ff2df89721886af9a97465f38aa7555c54f620e`
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
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
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
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a35d9d6945cc374a7bbfe3995e6dbc6b123699603aaa8c7990a77a4dc1369`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110186022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65b252b4fd53b5ea6489534264475297a3f51a4fe0598b9ff93a0abfeab59d`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 349.5 KB (349530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80acbf80c434da40993753a67a3ba8d7b3d0beab94fd257e6e037407515b0c7`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdfa16ecda5fcc480a52ecea59a92cb7df654f4ec78d25471bde0870d708f60`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (28035850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:56d8757abb7bd23f0b728f08b8a755058cea330b1a606b3f1a48ad4f8d61950e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24652798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd1416d76e876a1ba870e664e0c4f11df9a0071aa1f5d29c6b85b70ce8712d3`

```dockerfile
```

-	Layers:
	-	`sha256:efbd9ad746fa0f176367a3bb5d6e282eaa4961549e2f032b87020bb0a651a9b0`  
		Last Modified: Wed, 02 Jul 2025 07:18:01 GMT  
		Size: 24.6 MB (24636408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90eb727f87e7370c4afad7493905205e3ada84dfacab887fb7693bc0dc33796d`  
		Last Modified: Wed, 02 Jul 2025 07:18:02 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:87260e8b0f77e8183629f6e5a4b941306bc9d5e5d01c0e973cf0ec47ccd62455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296584050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51dd28410a8cd6823800155dfabe062d03afe081337cfae7c4145458d0b2f42`
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
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
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
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245c50a57c3d0b1f339d0824f2a936f99bba2fe0eeabb7766b65f4098430a010`  
		Last Modified: Wed, 02 Jul 2025 09:17:49 GMT  
		Size: 105.6 MB (105594130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784cd5894385f601f510027e6896f3227810a6905fff4495333cd2a05ec3edda`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 349.5 KB (349526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e758c429f764c8cd2ba3728865a6864d8ea589351940ceb59a0821349978a8`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14c6084c7ea506309951bfcf6196eeb524a3efd7b732fc211de2f4ef708527`  
		Last Modified: Wed, 02 Jul 2025 09:17:46 GMT  
		Size: 27.1 MB (27128913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:c5d49a60f3d8a21b64f0a6cca3d2a2c3a01d0fc85089e53d319f1beb55784a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24675196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd06b388bfacd51354ff4652dccc92dc593e5129ddead6df4b98172f9a41742f`

```dockerfile
```

-	Layers:
	-	`sha256:43bf9269c2eae35bccdccce11f98d160b9312c872d39ccdaaebaacc3b053df78`  
		Last Modified: Wed, 02 Jul 2025 10:17:57 GMT  
		Size: 24.7 MB (24658669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70d138ae4a633ac50de1359477ed9b134136250430003ef3a2eedfb3cbe88a9`  
		Last Modified: Wed, 02 Jul 2025 10:17:58 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:02248d162c0810f7e8e253d1f0da81f62fb78d6d69e52aa1a42f0235d8ffdf9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:e1ad65669608fc7e11be058eb56a6e324ffe66dd92cb8431d7191941a72a7988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089468164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2072229b981af9f439007905ef76b52bbd1f274c890b316f2b28820b2afdfa2c`
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
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a35d9d6945cc374a7bbfe3995e6dbc6b123699603aaa8c7990a77a4dc1369`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110186022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65b252b4fd53b5ea6489534264475297a3f51a4fe0598b9ff93a0abfeab59d`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 349.5 KB (349530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80acbf80c434da40993753a67a3ba8d7b3d0beab94fd257e6e037407515b0c7`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdfa16ecda5fcc480a52ecea59a92cb7df654f4ec78d25471bde0870d708f60`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (28035850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a336c75d1a418190091c4dd0e9e617ee21f5a43d5e3250874545d0b86c099b16`  
		Last Modified: Wed, 02 Jul 2025 13:44:57 GMT  
		Size: 781.2 MB (781228368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:6c658b53db9e02743e60280034bcc96d1d188472e3a1bacf462e351196b1c6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60833904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94c686fa064203c6a40722524940d4765944afb88bbb9be17019ffb81aa8ae5`

```dockerfile
```

-	Layers:
	-	`sha256:9357acf14b760c0ab796add917ac7161f7e5ae3c9336bca24a055488ab8ae0cf`  
		Last Modified: Wed, 02 Jul 2025 07:18:07 GMT  
		Size: 60.8 MB (60824509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cd757cdd55eab76c9f6182c3b6b9e201e0f8f743f5c4c0f29906258b593c22`  
		Last Modified: Wed, 02 Jul 2025 07:18:08 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:65dda2b1da4506a8ada257c74b91c8f916334b2fa6835c1931fdc6f4da27d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.0 MB (988014104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19518177178a7218e20fd621d3233dead129dc27307e8269599c03ac7e1d6927`
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
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
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
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245c50a57c3d0b1f339d0824f2a936f99bba2fe0eeabb7766b65f4098430a010`  
		Last Modified: Wed, 02 Jul 2025 09:17:49 GMT  
		Size: 105.6 MB (105594130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784cd5894385f601f510027e6896f3227810a6905fff4495333cd2a05ec3edda`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 349.5 KB (349526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e758c429f764c8cd2ba3728865a6864d8ea589351940ceb59a0821349978a8`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14c6084c7ea506309951bfcf6196eeb524a3efd7b732fc211de2f4ef708527`  
		Last Modified: Wed, 02 Jul 2025 09:17:46 GMT  
		Size: 27.1 MB (27128913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a9b0bcbfb8e7f6162f026e2dd0a844f577c9ff623578aebbb7e00cae7f1eec`  
		Last Modified: Wed, 02 Jul 2025 20:04:04 GMT  
		Size: 691.4 MB (691430054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9c30a5f79379181fb9031c34ebbbcefd454e372ca24f2fcd8051fa631b2864e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60764511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f461b5ac616f8b12e7247b7ccf5f72197e673bf76bdbd97897abff7f1304a901`

```dockerfile
```

-	Layers:
	-	`sha256:5a40692661b4b8a510b80b7ea80d44bd8935c37734fbd5cf83779030b4c730df`  
		Last Modified: Wed, 02 Jul 2025 16:19:27 GMT  
		Size: 60.8 MB (60755036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107ed9ef037676b7b73d027b4a2edf7765585c61aadca17b188ecaa509a4bec0`  
		Last Modified: Wed, 02 Jul 2025 16:19:29 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:02248d162c0810f7e8e253d1f0da81f62fb78d6d69e52aa1a42f0235d8ffdf9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:e1ad65669608fc7e11be058eb56a6e324ffe66dd92cb8431d7191941a72a7988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089468164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2072229b981af9f439007905ef76b52bbd1f274c890b316f2b28820b2afdfa2c`
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
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a35d9d6945cc374a7bbfe3995e6dbc6b123699603aaa8c7990a77a4dc1369`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110186022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65b252b4fd53b5ea6489534264475297a3f51a4fe0598b9ff93a0abfeab59d`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 349.5 KB (349530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80acbf80c434da40993753a67a3ba8d7b3d0beab94fd257e6e037407515b0c7`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdfa16ecda5fcc480a52ecea59a92cb7df654f4ec78d25471bde0870d708f60`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (28035850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a336c75d1a418190091c4dd0e9e617ee21f5a43d5e3250874545d0b86c099b16`  
		Last Modified: Wed, 02 Jul 2025 13:44:57 GMT  
		Size: 781.2 MB (781228368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:6c658b53db9e02743e60280034bcc96d1d188472e3a1bacf462e351196b1c6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60833904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94c686fa064203c6a40722524940d4765944afb88bbb9be17019ffb81aa8ae5`

```dockerfile
```

-	Layers:
	-	`sha256:9357acf14b760c0ab796add917ac7161f7e5ae3c9336bca24a055488ab8ae0cf`  
		Last Modified: Wed, 02 Jul 2025 07:18:07 GMT  
		Size: 60.8 MB (60824509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cd757cdd55eab76c9f6182c3b6b9e201e0f8f743f5c4c0f29906258b593c22`  
		Last Modified: Wed, 02 Jul 2025 07:18:08 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:65dda2b1da4506a8ada257c74b91c8f916334b2fa6835c1931fdc6f4da27d77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.0 MB (988014104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19518177178a7218e20fd621d3233dead129dc27307e8269599c03ac7e1d6927`
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
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
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
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245c50a57c3d0b1f339d0824f2a936f99bba2fe0eeabb7766b65f4098430a010`  
		Last Modified: Wed, 02 Jul 2025 09:17:49 GMT  
		Size: 105.6 MB (105594130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784cd5894385f601f510027e6896f3227810a6905fff4495333cd2a05ec3edda`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 349.5 KB (349526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e758c429f764c8cd2ba3728865a6864d8ea589351940ceb59a0821349978a8`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14c6084c7ea506309951bfcf6196eeb524a3efd7b732fc211de2f4ef708527`  
		Last Modified: Wed, 02 Jul 2025 09:17:46 GMT  
		Size: 27.1 MB (27128913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a9b0bcbfb8e7f6162f026e2dd0a844f577c9ff623578aebbb7e00cae7f1eec`  
		Last Modified: Wed, 02 Jul 2025 20:04:04 GMT  
		Size: 691.4 MB (691430054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9c30a5f79379181fb9031c34ebbbcefd454e372ca24f2fcd8051fa631b2864e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60764511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f461b5ac616f8b12e7247b7ccf5f72197e673bf76bdbd97897abff7f1304a901`

```dockerfile
```

-	Layers:
	-	`sha256:5a40692661b4b8a510b80b7ea80d44bd8935c37734fbd5cf83779030b4c730df`  
		Last Modified: Wed, 02 Jul 2025 16:19:27 GMT  
		Size: 60.8 MB (60755036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107ed9ef037676b7b73d027b4a2edf7765585c61aadca17b188ecaa509a4bec0`  
		Last Modified: Wed, 02 Jul 2025 16:19:29 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:ff35b75fc35505ede9607df277b24cdef86d3c082bcd052e8164ef6170923e96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d1731a84608298b7f9f3fc44a8a1353fe606a84c37d45fc6b68b728027e004da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308239796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fcfdc00a096c70701d65348ff2df89721886af9a97465f38aa7555c54f620e`
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
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
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
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a35d9d6945cc374a7bbfe3995e6dbc6b123699603aaa8c7990a77a4dc1369`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110186022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65b252b4fd53b5ea6489534264475297a3f51a4fe0598b9ff93a0abfeab59d`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 349.5 KB (349530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80acbf80c434da40993753a67a3ba8d7b3d0beab94fd257e6e037407515b0c7`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdfa16ecda5fcc480a52ecea59a92cb7df654f4ec78d25471bde0870d708f60`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (28035850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:56d8757abb7bd23f0b728f08b8a755058cea330b1a606b3f1a48ad4f8d61950e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24652798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd1416d76e876a1ba870e664e0c4f11df9a0071aa1f5d29c6b85b70ce8712d3`

```dockerfile
```

-	Layers:
	-	`sha256:efbd9ad746fa0f176367a3bb5d6e282eaa4961549e2f032b87020bb0a651a9b0`  
		Last Modified: Wed, 02 Jul 2025 07:18:01 GMT  
		Size: 24.6 MB (24636408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90eb727f87e7370c4afad7493905205e3ada84dfacab887fb7693bc0dc33796d`  
		Last Modified: Wed, 02 Jul 2025 07:18:02 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:87260e8b0f77e8183629f6e5a4b941306bc9d5e5d01c0e973cf0ec47ccd62455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296584050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51dd28410a8cd6823800155dfabe062d03afe081337cfae7c4145458d0b2f42`
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
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
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
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245c50a57c3d0b1f339d0824f2a936f99bba2fe0eeabb7766b65f4098430a010`  
		Last Modified: Wed, 02 Jul 2025 09:17:49 GMT  
		Size: 105.6 MB (105594130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784cd5894385f601f510027e6896f3227810a6905fff4495333cd2a05ec3edda`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 349.5 KB (349526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e758c429f764c8cd2ba3728865a6864d8ea589351940ceb59a0821349978a8`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14c6084c7ea506309951bfcf6196eeb524a3efd7b732fc211de2f4ef708527`  
		Last Modified: Wed, 02 Jul 2025 09:17:46 GMT  
		Size: 27.1 MB (27128913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:c5d49a60f3d8a21b64f0a6cca3d2a2c3a01d0fc85089e53d319f1beb55784a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24675196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd06b388bfacd51354ff4652dccc92dc593e5129ddead6df4b98172f9a41742f`

```dockerfile
```

-	Layers:
	-	`sha256:43bf9269c2eae35bccdccce11f98d160b9312c872d39ccdaaebaacc3b053df78`  
		Last Modified: Wed, 02 Jul 2025 10:17:57 GMT  
		Size: 24.7 MB (24658669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70d138ae4a633ac50de1359477ed9b134136250430003ef3a2eedfb3cbe88a9`  
		Last Modified: Wed, 02 Jul 2025 10:17:58 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:ff35b75fc35505ede9607df277b24cdef86d3c082bcd052e8164ef6170923e96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:d1731a84608298b7f9f3fc44a8a1353fe606a84c37d45fc6b68b728027e004da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308239796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fcfdc00a096c70701d65348ff2df89721886af9a97465f38aa7555c54f620e`
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
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
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
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a35d9d6945cc374a7bbfe3995e6dbc6b123699603aaa8c7990a77a4dc1369`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110186022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65b252b4fd53b5ea6489534264475297a3f51a4fe0598b9ff93a0abfeab59d`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 349.5 KB (349530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80acbf80c434da40993753a67a3ba8d7b3d0beab94fd257e6e037407515b0c7`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdfa16ecda5fcc480a52ecea59a92cb7df654f4ec78d25471bde0870d708f60`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (28035850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:56d8757abb7bd23f0b728f08b8a755058cea330b1a606b3f1a48ad4f8d61950e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24652798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd1416d76e876a1ba870e664e0c4f11df9a0071aa1f5d29c6b85b70ce8712d3`

```dockerfile
```

-	Layers:
	-	`sha256:efbd9ad746fa0f176367a3bb5d6e282eaa4961549e2f032b87020bb0a651a9b0`  
		Last Modified: Wed, 02 Jul 2025 07:18:01 GMT  
		Size: 24.6 MB (24636408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90eb727f87e7370c4afad7493905205e3ada84dfacab887fb7693bc0dc33796d`  
		Last Modified: Wed, 02 Jul 2025 07:18:02 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:87260e8b0f77e8183629f6e5a4b941306bc9d5e5d01c0e973cf0ec47ccd62455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296584050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51dd28410a8cd6823800155dfabe062d03afe081337cfae7c4145458d0b2f42`
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
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
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
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245c50a57c3d0b1f339d0824f2a936f99bba2fe0eeabb7766b65f4098430a010`  
		Last Modified: Wed, 02 Jul 2025 09:17:49 GMT  
		Size: 105.6 MB (105594130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784cd5894385f601f510027e6896f3227810a6905fff4495333cd2a05ec3edda`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 349.5 KB (349526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e758c429f764c8cd2ba3728865a6864d8ea589351940ceb59a0821349978a8`  
		Last Modified: Wed, 02 Jul 2025 09:17:44 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14c6084c7ea506309951bfcf6196eeb524a3efd7b732fc211de2f4ef708527`  
		Last Modified: Wed, 02 Jul 2025 09:17:46 GMT  
		Size: 27.1 MB (27128913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c5d49a60f3d8a21b64f0a6cca3d2a2c3a01d0fc85089e53d319f1beb55784a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24675196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd06b388bfacd51354ff4652dccc92dc593e5129ddead6df4b98172f9a41742f`

```dockerfile
```

-	Layers:
	-	`sha256:43bf9269c2eae35bccdccce11f98d160b9312c872d39ccdaaebaacc3b053df78`  
		Last Modified: Wed, 02 Jul 2025 10:17:57 GMT  
		Size: 24.7 MB (24658669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70d138ae4a633ac50de1359477ed9b134136250430003ef3a2eedfb3cbe88a9`  
		Last Modified: Wed, 02 Jul 2025 10:17:58 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:1c98e9e217e46d7639dea565310d4d16bfa4344497d462f7eabc986dd540aaed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:66ebd667679864d6c3909cf0118fcf297c1637a5e6ac2130ee7975104f615dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169665930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f3dd85b3b713e8b2a683701a16f694f940b6d5bb4fef68a3c02b0dc36ae54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:0bb9aed55d0d4d06007bb8526d1be866c3f502747b9578c835a9fbeb3af129ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18409046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438abb225bc0c0a13743692b5efc63a9e9c99b84fcae261c26170c2ca4ff69c4`

```dockerfile
```

-	Layers:
	-	`sha256:235dd6d354142de573fa1971dd61c5d979b88f6f3e7bb04760c9d605003e407a`  
		Last Modified: Wed, 02 Jul 2025 07:18:14 GMT  
		Size: 18.4 MB (18394394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:991e63c05a19dbef16187b2618b81fe7733770759fe47e243a06adbe6dab412b`  
		Last Modified: Wed, 02 Jul 2025 07:18:15 GMT  
		Size: 14.7 KB (14652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:065a8d4842aaa4c1847306c1b451169c37ea0603640b8df06ffb85a0cdb0c770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163508984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f8b581927a631c339f5005390b6410ba687042cd4674304e5fdcbde98b962e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:30f6ebe521d295e5a1f3b0203a711e2f36997c9ddfe68bb1de891faeec4be0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18383177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa94f2e5f0330b5935119de149195befce7f8a8586fc2a5a0d3ce6613b55fa62`

```dockerfile
```

-	Layers:
	-	`sha256:fa72359fc133638f37196f0dbe634d106a73ea75b9339ad16c09717620b9433d`  
		Last Modified: Wed, 02 Jul 2025 07:18:28 GMT  
		Size: 18.4 MB (18368400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25bf6a808bc8cf713ad8b0eb9e55102448fe77c5a4dc07b9edd75a50f636d386`  
		Last Modified: Wed, 02 Jul 2025 07:18:29 GMT  
		Size: 14.8 KB (14777 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:1c98e9e217e46d7639dea565310d4d16bfa4344497d462f7eabc986dd540aaed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:66ebd667679864d6c3909cf0118fcf297c1637a5e6ac2130ee7975104f615dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169665930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f3dd85b3b713e8b2a683701a16f694f940b6d5bb4fef68a3c02b0dc36ae54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b35fcb4c72e4e1b576c9ad4eeb168575fdcd9f08aa9626159697d08f85f11d`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 683.8 KB (683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6ec29354bbb917479948bd512e7a37b5a78b548201e41ab844f5cd27b0a73`  
		Last Modified: Wed, 02 Jul 2025 04:13:15 GMT  
		Size: 6.7 MB (6745540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910605ef6993fba7a0021d6777f55c01af1f52d7fc5fcaaaefba86d25561efe4`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (94001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47410432c7f18b2fef7279829cc16c86748b308925bb2b928a0d1f18b5a9faf0`  
		Last Modified: Wed, 02 Jul 2025 04:13:19 GMT  
		Size: 132.4 MB (132424061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e057fb5b5c66bd780fcacedc32a3c495cf63933eda6c5c80a9db3df9b484c53`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0bb9aed55d0d4d06007bb8526d1be866c3f502747b9578c835a9fbeb3af129ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18409046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438abb225bc0c0a13743692b5efc63a9e9c99b84fcae261c26170c2ca4ff69c4`

```dockerfile
```

-	Layers:
	-	`sha256:235dd6d354142de573fa1971dd61c5d979b88f6f3e7bb04760c9d605003e407a`  
		Last Modified: Wed, 02 Jul 2025 07:18:14 GMT  
		Size: 18.4 MB (18394394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:991e63c05a19dbef16187b2618b81fe7733770759fe47e243a06adbe6dab412b`  
		Last Modified: Wed, 02 Jul 2025 07:18:15 GMT  
		Size: 14.7 KB (14652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:065a8d4842aaa4c1847306c1b451169c37ea0603640b8df06ffb85a0cdb0c770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163508984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f8b581927a631c339f5005390b6410ba687042cd4674304e5fdcbde98b962e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Jun 2025 04:32:14 GMT
ARG RELEASE
# Tue, 03 Jun 2025 04:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Jun 2025 04:32:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 03 Jun 2025 04:32:14 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7528a0593a687366e793711eb7a036e8bf103509785a61913bf5858f83940`  
		Last Modified: Wed, 02 Jul 2025 06:29:33 GMT  
		Size: 127.1 MB (127115953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94731d288701fbac725cde2c66a4c866e7bc2a7e160fbd0f835eb50ae626e5a`  
		Last Modified: Wed, 02 Jul 2025 06:29:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:30f6ebe521d295e5a1f3b0203a711e2f36997c9ddfe68bb1de891faeec4be0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18383177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa94f2e5f0330b5935119de149195befce7f8a8586fc2a5a0d3ce6613b55fa62`

```dockerfile
```

-	Layers:
	-	`sha256:fa72359fc133638f37196f0dbe634d106a73ea75b9339ad16c09717620b9433d`  
		Last Modified: Wed, 02 Jul 2025 07:18:28 GMT  
		Size: 18.4 MB (18368400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25bf6a808bc8cf713ad8b0eb9e55102448fe77c5a4dc07b9edd75a50f636d386`  
		Last Modified: Wed, 02 Jul 2025 07:18:29 GMT  
		Size: 14.8 KB (14777 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:c759f6424661403697c7853a851207a2ab58781bdb89c240339541252dd8a947
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:f5c8f6ebc2e4033533eb045ff8952a52c8f14eda9d601ba54187ab1d7a25e438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295690709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5c46408d6eb6acac780c416c3911f89619489c478efe80799bddebf4c1f3af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510bd5ae6239c24f2fef8dba0bfedf92a85b22ec70f234ea081506ad10968c5`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 683.8 KB (683772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815c2eb0a0c4951a0b305dbddbcfde72c32b736b31fd5224e85c9a5343924ba`  
		Last Modified: Wed, 02 Jul 2025 04:13:09 GMT  
		Size: 6.7 MB (6745404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab81ee57c8932bb1346856f757778b241a8e5dcca1b02bfaede22bb9fe39555`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 94.0 KB (93979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe881751967e0f2c873cd5e85a47f635bff56d8c13b8f678c88e13784fd21e`  
		Last Modified: Wed, 02 Jul 2025 04:13:18 GMT  
		Size: 119.9 MB (119929721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ea7413a64fc4b22a00644cd56977378c07a95e6d0b298e78efa4baa0b873d`  
		Last Modified: Wed, 02 Jul 2025 04:13:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad66aa49d81043255b5a68fe8370c44ed1bb417a34d56921b5b6e54aad5e8d43`  
		Last Modified: Wed, 02 Jul 2025 05:11:35 GMT  
		Size: 110.2 MB (110183478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22750c2ee1c83973e70b463b77f04591f765297af3b530faf78d8f8ed830ff1`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 368.0 KB (367976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e63a806b355a8c725520e98243260911eac03cbb661780b860888e786128635`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc65c67c30109fc2ccd6dc11a29c0f2680360d72516f305af61d8dfe881a29`  
		Last Modified: Wed, 02 Jul 2025 05:11:25 GMT  
		Size: 28.0 MB (27965355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:7582b6c1248178e77adfae99361728288005df8f0abc9d7d0663ce2457b19a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24546251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d89f79ee0222f23486dfa10abbdbd26946edf33232e03ca8f9069e9e56c08de`

```dockerfile
```

-	Layers:
	-	`sha256:33e7ca868a61f1ade7ef63d4016c645b019cb17ab5bd8aacba13bd01eee266b8`  
		Last Modified: Wed, 02 Jul 2025 07:17:41 GMT  
		Size: 24.5 MB (24529587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8245d24d84e6d877693b0225acc3c0a1f1db6df7a10b132c28bbdd4947eeb5f3`  
		Last Modified: Wed, 02 Jul 2025 07:17:42 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3f0664e804cdece42022fc377e0dea5bff9bd0d26d30b632a668b29c15dada34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284134893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26d377b653accbd2690e4bb391d3a00f274f558248e288e1f357fdf66fadd34`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7416a1af977576fae6a0a8c3c2855ff1842e82acf36b7276ea4e1c86948179`  
		Last Modified: Wed, 02 Jul 2025 06:28:19 GMT  
		Size: 114.7 MB (114708328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766513cfa1e97be3234dbb9d5cc138268a46ceeb0d128e542b5624fa784d2136`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736106426b42d80857f05a708ed6cd5e9650eda12b095660b23f5188719dc07`  
		Last Modified: Wed, 02 Jul 2025 09:16:05 GMT  
		Size: 105.6 MB (105590987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f6f9545192a9608660f621dde4c7267a9c0757e2be323d7aed12460e2f2572`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 368.0 KB (367978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67487dd6e705c0eea7666a23c0fe353532dd278d9f0f5591a0b8f530bf461d09`  
		Last Modified: Wed, 02 Jul 2025 09:15:58 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df12486781526bb96d0db46f630672fe88462cf8622b5f864aaec2e770eea30`  
		Last Modified: Wed, 02 Jul 2025 09:16:00 GMT  
		Size: 27.1 MB (27072114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:e6be0bdcda31b2afd199507e994ff67bbfc8d0ce905da4e78a501a43e73b8b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24568673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3495f419552b8f23bbb157ab88b37378bf20d2f34d54e6535a4c832f82bbb9`

```dockerfile
```

-	Layers:
	-	`sha256:f18f7a78abb706290d89fa3915ea7be74c3e39cc4aec179affa63d732cc96e9e`  
		Last Modified: Wed, 02 Jul 2025 10:17:50 GMT  
		Size: 24.6 MB (24551860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a283f2837d521fb527f032d19868776e4b9b126eda033fb325f5fdc0731d2fb0`  
		Last Modified: Wed, 02 Jul 2025 10:17:50 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:1a7e19fa2d58171255f3f9a7a82b1afd4c7a6af366ece56845ecb2b9a73e9863
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:5cdc37bfe31bf795e7d81a6f00dfc4e0364f8c521d2972788d73b77288939e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308220446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72f9c81b3ab31a485c1703e525dad2aa09296ce0caabc1132684552739b6cde`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcffa4abafb7ede5ec75389b55e4e36fc64d99306eb3a34d5efcea8775bec12`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110185283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd41262773d2505a4003851c5c45d572effbce42010711603e88ea0c8ad0a36e`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 346.7 KB (346688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c95e84a6b5f769319af314a910888e4978710b6ca98d90a42d1b5d5e01cd6f`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75ec61d69c1def2f1e185c02f880666563593f62844279b713ff44c35f2f07`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 28.0 MB (28033451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:e27cea9583e52fc0d60ea377b967a69542e2692aaff89c7470af6d836d34b1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24533433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07f975a56cd54a04589a5ad52f0e0e4420551792cac47eb8c5a89bbeec3b86b`

```dockerfile
```

-	Layers:
	-	`sha256:4e43f49e9e74006b7cff18e98d021456eadb85c52db3afa68c6842e4a1b650c1`  
		Last Modified: Wed, 02 Jul 2025 07:18:23 GMT  
		Size: 24.5 MB (24517025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653827fa9ddf396343f546cc01698d8eea594cbb2ba9c2203691561fe7c7072d`  
		Last Modified: Wed, 02 Jul 2025 07:18:24 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ef5e04d2dcd7163fa7d203798a546de0b07df4511745f38f89ca7a9fd53555e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296552688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611ceb0eb7c8dcca42b47c73117a08824891ee46a7c65b3c3787ee912adba54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80205a32428d80d47d738a520ae436ad7d1aaca7a54a3b8bc5b46b3fefc0b8`  
		Last Modified: Wed, 02 Jul 2025 06:30:50 GMT  
		Size: 127.1 MB (127092365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e416b86f6cb653b375173be75b902fa6b1fd9c4fd4e49908e63a7c2421b648`  
		Last Modified: Wed, 02 Jul 2025 06:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e314143ed85ce5aa0c241e6768e4b92669b8e1b02edc45346d44423c8bd2443a`  
		Last Modified: Wed, 02 Jul 2025 12:22:18 GMT  
		Size: 105.6 MB (105593706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34207e24a8a07dc3ff1a902b0fe19bb7884e357933dcd197c04c71b451096c`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 346.7 KB (346684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395d451f2057b0929605a42481b24f88bcabc12a3517673c10486aa560b00fb`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be4dff02fcea1f18e0ae82f4a7d7e4a19a2aa39a50ba3424b9334da68c5054`  
		Last Modified: Wed, 02 Jul 2025 09:19:32 GMT  
		Size: 27.1 MB (27124444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:84244240769b4c3a1b092382084d0576690ef4ac2c28507336eab02ab4a83a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24555831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc40ba637e62741d2c4480dc001040c95ccc8145ecd8ea5f3dd0c4b9490c284`

```dockerfile
```

-	Layers:
	-	`sha256:aca3bdafc932e97d5fab88c7e6605dd2a6cbfca112c82a9829a26169cbacb6aa`  
		Last Modified: Wed, 02 Jul 2025 10:18:04 GMT  
		Size: 24.5 MB (24539286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508005913bc29fc1b6ed1f34839efe116ff23c662353db12fa415c0586018a4a`  
		Last Modified: Wed, 02 Jul 2025 10:18:05 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:7828f6884668d1e8c37e43ff2dced7f8a52f10ca10fbb8d431174bb7452ee7f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:c181d56d5ca2bbcfea740493d845e434491304f080fd19d3857b30202f459ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089544530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d3b320810dedcaae0713e0022a31a67631f3916cce15bce23770f6e9cb7391`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcffa4abafb7ede5ec75389b55e4e36fc64d99306eb3a34d5efcea8775bec12`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110185283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd41262773d2505a4003851c5c45d572effbce42010711603e88ea0c8ad0a36e`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 346.7 KB (346688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c95e84a6b5f769319af314a910888e4978710b6ca98d90a42d1b5d5e01cd6f`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75ec61d69c1def2f1e185c02f880666563593f62844279b713ff44c35f2f07`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 28.0 MB (28033451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5a51e1412b85bf0ab03d97327964d03dbdcb524381a8eb3488479b9b748a9d`  
		Last Modified: Wed, 02 Jul 2025 13:39:40 GMT  
		Size: 781.3 MB (781324084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1d0ef093789d9d47c090c8812423b36c1ad03d51dc46c31109729f40144e8716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af082832aae34b368fbbcc201a560dcf96a5bee8fbe279d01b440004ce53541`

```dockerfile
```

-	Layers:
	-	`sha256:6674b79429655bb5e931efafdb8a3c2e1539d47757ec7ddb24bf40e1a2c887ab`  
		Last Modified: Wed, 02 Jul 2025 07:18:29 GMT  
		Size: 60.7 MB (60706519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e21bd56e8cb39a47f317ee28aaced36c12845621756857a92fb9ab37bb15476`  
		Last Modified: Wed, 02 Jul 2025 07:18:30 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:544ec53f5ea35911760fd2e60c2d2bd7af6e755a1293a82badd162080bc44680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.0 MB (988024087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10aa454c898af357ed4fc14d9e5638a9c1de2a798e97640f3af535bd8920a92`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80205a32428d80d47d738a520ae436ad7d1aaca7a54a3b8bc5b46b3fefc0b8`  
		Last Modified: Wed, 02 Jul 2025 06:30:50 GMT  
		Size: 127.1 MB (127092365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e416b86f6cb653b375173be75b902fa6b1fd9c4fd4e49908e63a7c2421b648`  
		Last Modified: Wed, 02 Jul 2025 06:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e314143ed85ce5aa0c241e6768e4b92669b8e1b02edc45346d44423c8bd2443a`  
		Last Modified: Wed, 02 Jul 2025 12:22:18 GMT  
		Size: 105.6 MB (105593706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34207e24a8a07dc3ff1a902b0fe19bb7884e357933dcd197c04c71b451096c`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 346.7 KB (346684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395d451f2057b0929605a42481b24f88bcabc12a3517673c10486aa560b00fb`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be4dff02fcea1f18e0ae82f4a7d7e4a19a2aa39a50ba3424b9334da68c5054`  
		Last Modified: Wed, 02 Jul 2025 09:19:32 GMT  
		Size: 27.1 MB (27124444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b95bc64f21bf60d8056200700abdfeb2911bd477e38a253d7ce5879dff2a0eb`  
		Last Modified: Wed, 02 Jul 2025 19:53:26 GMT  
		Size: 691.5 MB (691471399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:f25174161b6a6bf46b35a06d8dd93c514eb5f28f704a8386017ce81330417326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60646530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748ed28c10c443350de54f246a54aa5f18eed2772c46dff79157f8741781a125`

```dockerfile
```

-	Layers:
	-	`sha256:619ec0c57346adaab86f50dc26eb5d596ce62ea9af138d2c770bc8820d56f49c`  
		Last Modified: Wed, 02 Jul 2025 16:19:19 GMT  
		Size: 60.6 MB (60637046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5665b4a74f5ffe6a5c7089bc14f3aafa3d19ead481fbcf586731331bee9248`  
		Last Modified: Wed, 02 Jul 2025 16:19:20 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:7828f6884668d1e8c37e43ff2dced7f8a52f10ca10fbb8d431174bb7452ee7f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:c181d56d5ca2bbcfea740493d845e434491304f080fd19d3857b30202f459ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089544530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d3b320810dedcaae0713e0022a31a67631f3916cce15bce23770f6e9cb7391`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcffa4abafb7ede5ec75389b55e4e36fc64d99306eb3a34d5efcea8775bec12`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110185283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd41262773d2505a4003851c5c45d572effbce42010711603e88ea0c8ad0a36e`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 346.7 KB (346688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c95e84a6b5f769319af314a910888e4978710b6ca98d90a42d1b5d5e01cd6f`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75ec61d69c1def2f1e185c02f880666563593f62844279b713ff44c35f2f07`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 28.0 MB (28033451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5a51e1412b85bf0ab03d97327964d03dbdcb524381a8eb3488479b9b748a9d`  
		Last Modified: Wed, 02 Jul 2025 13:39:40 GMT  
		Size: 781.3 MB (781324084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1d0ef093789d9d47c090c8812423b36c1ad03d51dc46c31109729f40144e8716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af082832aae34b368fbbcc201a560dcf96a5bee8fbe279d01b440004ce53541`

```dockerfile
```

-	Layers:
	-	`sha256:6674b79429655bb5e931efafdb8a3c2e1539d47757ec7ddb24bf40e1a2c887ab`  
		Last Modified: Wed, 02 Jul 2025 07:18:29 GMT  
		Size: 60.7 MB (60706519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e21bd56e8cb39a47f317ee28aaced36c12845621756857a92fb9ab37bb15476`  
		Last Modified: Wed, 02 Jul 2025 07:18:30 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:544ec53f5ea35911760fd2e60c2d2bd7af6e755a1293a82badd162080bc44680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.0 MB (988024087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10aa454c898af357ed4fc14d9e5638a9c1de2a798e97640f3af535bd8920a92`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80205a32428d80d47d738a520ae436ad7d1aaca7a54a3b8bc5b46b3fefc0b8`  
		Last Modified: Wed, 02 Jul 2025 06:30:50 GMT  
		Size: 127.1 MB (127092365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e416b86f6cb653b375173be75b902fa6b1fd9c4fd4e49908e63a7c2421b648`  
		Last Modified: Wed, 02 Jul 2025 06:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e314143ed85ce5aa0c241e6768e4b92669b8e1b02edc45346d44423c8bd2443a`  
		Last Modified: Wed, 02 Jul 2025 12:22:18 GMT  
		Size: 105.6 MB (105593706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34207e24a8a07dc3ff1a902b0fe19bb7884e357933dcd197c04c71b451096c`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 346.7 KB (346684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395d451f2057b0929605a42481b24f88bcabc12a3517673c10486aa560b00fb`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be4dff02fcea1f18e0ae82f4a7d7e4a19a2aa39a50ba3424b9334da68c5054`  
		Last Modified: Wed, 02 Jul 2025 09:19:32 GMT  
		Size: 27.1 MB (27124444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b95bc64f21bf60d8056200700abdfeb2911bd477e38a253d7ce5879dff2a0eb`  
		Last Modified: Wed, 02 Jul 2025 19:53:26 GMT  
		Size: 691.5 MB (691471399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f25174161b6a6bf46b35a06d8dd93c514eb5f28f704a8386017ce81330417326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60646530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748ed28c10c443350de54f246a54aa5f18eed2772c46dff79157f8741781a125`

```dockerfile
```

-	Layers:
	-	`sha256:619ec0c57346adaab86f50dc26eb5d596ce62ea9af138d2c770bc8820d56f49c`  
		Last Modified: Wed, 02 Jul 2025 16:19:19 GMT  
		Size: 60.6 MB (60637046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5665b4a74f5ffe6a5c7089bc14f3aafa3d19ead481fbcf586731331bee9248`  
		Last Modified: Wed, 02 Jul 2025 16:19:20 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:1a7e19fa2d58171255f3f9a7a82b1afd4c7a6af366ece56845ecb2b9a73e9863
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:5cdc37bfe31bf795e7d81a6f00dfc4e0364f8c521d2972788d73b77288939e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308220446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72f9c81b3ab31a485c1703e525dad2aa09296ce0caabc1132684552739b6cde`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcffa4abafb7ede5ec75389b55e4e36fc64d99306eb3a34d5efcea8775bec12`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110185283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd41262773d2505a4003851c5c45d572effbce42010711603e88ea0c8ad0a36e`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 346.7 KB (346688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c95e84a6b5f769319af314a910888e4978710b6ca98d90a42d1b5d5e01cd6f`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75ec61d69c1def2f1e185c02f880666563593f62844279b713ff44c35f2f07`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 28.0 MB (28033451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:e27cea9583e52fc0d60ea377b967a69542e2692aaff89c7470af6d836d34b1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24533433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07f975a56cd54a04589a5ad52f0e0e4420551792cac47eb8c5a89bbeec3b86b`

```dockerfile
```

-	Layers:
	-	`sha256:4e43f49e9e74006b7cff18e98d021456eadb85c52db3afa68c6842e4a1b650c1`  
		Last Modified: Wed, 02 Jul 2025 07:18:23 GMT  
		Size: 24.5 MB (24517025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653827fa9ddf396343f546cc01698d8eea594cbb2ba9c2203691561fe7c7072d`  
		Last Modified: Wed, 02 Jul 2025 07:18:24 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ef5e04d2dcd7163fa7d203798a546de0b07df4511745f38f89ca7a9fd53555e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296552688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611ceb0eb7c8dcca42b47c73117a08824891ee46a7c65b3c3787ee912adba54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80205a32428d80d47d738a520ae436ad7d1aaca7a54a3b8bc5b46b3fefc0b8`  
		Last Modified: Wed, 02 Jul 2025 06:30:50 GMT  
		Size: 127.1 MB (127092365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e416b86f6cb653b375173be75b902fa6b1fd9c4fd4e49908e63a7c2421b648`  
		Last Modified: Wed, 02 Jul 2025 06:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e314143ed85ce5aa0c241e6768e4b92669b8e1b02edc45346d44423c8bd2443a`  
		Last Modified: Wed, 02 Jul 2025 12:22:18 GMT  
		Size: 105.6 MB (105593706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34207e24a8a07dc3ff1a902b0fe19bb7884e357933dcd197c04c71b451096c`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 346.7 KB (346684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395d451f2057b0929605a42481b24f88bcabc12a3517673c10486aa560b00fb`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be4dff02fcea1f18e0ae82f4a7d7e4a19a2aa39a50ba3424b9334da68c5054`  
		Last Modified: Wed, 02 Jul 2025 09:19:32 GMT  
		Size: 27.1 MB (27124444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:84244240769b4c3a1b092382084d0576690ef4ac2c28507336eab02ab4a83a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24555831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc40ba637e62741d2c4480dc001040c95ccc8145ecd8ea5f3dd0c4b9490c284`

```dockerfile
```

-	Layers:
	-	`sha256:aca3bdafc932e97d5fab88c7e6605dd2a6cbfca112c82a9829a26169cbacb6aa`  
		Last Modified: Wed, 02 Jul 2025 10:18:04 GMT  
		Size: 24.5 MB (24539286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508005913bc29fc1b6ed1f34839efe116ff23c662353db12fa415c0586018a4a`  
		Last Modified: Wed, 02 Jul 2025 10:18:05 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:1a7e19fa2d58171255f3f9a7a82b1afd4c7a6af366ece56845ecb2b9a73e9863
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:5cdc37bfe31bf795e7d81a6f00dfc4e0364f8c521d2972788d73b77288939e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308220446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72f9c81b3ab31a485c1703e525dad2aa09296ce0caabc1132684552739b6cde`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcffa4abafb7ede5ec75389b55e4e36fc64d99306eb3a34d5efcea8775bec12`  
		Last Modified: Wed, 02 Jul 2025 05:11:27 GMT  
		Size: 110.2 MB (110185283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd41262773d2505a4003851c5c45d572effbce42010711603e88ea0c8ad0a36e`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 346.7 KB (346688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c95e84a6b5f769319af314a910888e4978710b6ca98d90a42d1b5d5e01cd6f`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75ec61d69c1def2f1e185c02f880666563593f62844279b713ff44c35f2f07`  
		Last Modified: Wed, 02 Jul 2025 05:11:23 GMT  
		Size: 28.0 MB (28033451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e27cea9583e52fc0d60ea377b967a69542e2692aaff89c7470af6d836d34b1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24533433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07f975a56cd54a04589a5ad52f0e0e4420551792cac47eb8c5a89bbeec3b86b`

```dockerfile
```

-	Layers:
	-	`sha256:4e43f49e9e74006b7cff18e98d021456eadb85c52db3afa68c6842e4a1b650c1`  
		Last Modified: Wed, 02 Jul 2025 07:18:23 GMT  
		Size: 24.5 MB (24517025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653827fa9ddf396343f546cc01698d8eea594cbb2ba9c2203691561fe7c7072d`  
		Last Modified: Wed, 02 Jul 2025 07:18:24 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ef5e04d2dcd7163fa7d203798a546de0b07df4511745f38f89ca7a9fd53555e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296552688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611ceb0eb7c8dcca42b47c73117a08824891ee46a7c65b3c3787ee912adba54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80205a32428d80d47d738a520ae436ad7d1aaca7a54a3b8bc5b46b3fefc0b8`  
		Last Modified: Wed, 02 Jul 2025 06:30:50 GMT  
		Size: 127.1 MB (127092365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e416b86f6cb653b375173be75b902fa6b1fd9c4fd4e49908e63a7c2421b648`  
		Last Modified: Wed, 02 Jul 2025 06:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e314143ed85ce5aa0c241e6768e4b92669b8e1b02edc45346d44423c8bd2443a`  
		Last Modified: Wed, 02 Jul 2025 12:22:18 GMT  
		Size: 105.6 MB (105593706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34207e24a8a07dc3ff1a902b0fe19bb7884e357933dcd197c04c71b451096c`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 346.7 KB (346684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a395d451f2057b0929605a42481b24f88bcabc12a3517673c10486aa560b00fb`  
		Last Modified: Wed, 02 Jul 2025 09:19:26 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be4dff02fcea1f18e0ae82f4a7d7e4a19a2aa39a50ba3424b9334da68c5054`  
		Last Modified: Wed, 02 Jul 2025 09:19:32 GMT  
		Size: 27.1 MB (27124444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:84244240769b4c3a1b092382084d0576690ef4ac2c28507336eab02ab4a83a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24555831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc40ba637e62741d2c4480dc001040c95ccc8145ecd8ea5f3dd0c4b9490c284`

```dockerfile
```

-	Layers:
	-	`sha256:aca3bdafc932e97d5fab88c7e6605dd2a6cbfca112c82a9829a26169cbacb6aa`  
		Last Modified: Wed, 02 Jul 2025 10:18:04 GMT  
		Size: 24.5 MB (24539286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508005913bc29fc1b6ed1f34839efe116ff23c662353db12fa415c0586018a4a`  
		Last Modified: Wed, 02 Jul 2025 10:18:05 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:dc578a780f969c27d4eca6b8a1ce0a482a11034012c9c20d377cfe9cf6b49335
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:a7f8504bc633056c364e3f6d99e5f7ff04e058526bb3d52fb032d3de8a9038a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a25ace67f66dacdb993f06f9e82370c801912f2d717f0797aa041f2f42b999c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:38a94f29cc7965911c3c9110b3bfa6b8860f25adfbb8508e0ca0a36be1fa37a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18312309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d26f79f09f7b72ab53ad2dd176573fadf7f4af07a13293f9053c42db7fb25af`

```dockerfile
```

-	Layers:
	-	`sha256:03919e412d7535fa4ee1db1b05bb40fe9968c40931079ed9cd9c4bce90277226`  
		Last Modified: Wed, 02 Jul 2025 07:18:33 GMT  
		Size: 18.3 MB (18297644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4065d67af5621efef8c1441e3088e6c0ff7576b9c18ade75fc1655afb22a1e6`  
		Last Modified: Wed, 02 Jul 2025 07:18:33 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89d9724ded43eb34411b0cb602be12daeb99966c15b1e78f0a01ddd1415aa6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163485397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf4f60c551638a7621157a3ae03b6a5ed9659a983e64a54c2fdb093feed8446`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80205a32428d80d47d738a520ae436ad7d1aaca7a54a3b8bc5b46b3fefc0b8`  
		Last Modified: Wed, 02 Jul 2025 06:30:50 GMT  
		Size: 127.1 MB (127092365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e416b86f6cb653b375173be75b902fa6b1fd9c4fd4e49908e63a7c2421b648`  
		Last Modified: Wed, 02 Jul 2025 06:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:88c6acb8d58ecca3506cfcee5e6cc152ddb2f1f3e204489de3042695c69298a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18286440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb45d223c5bec05a4d2da002eb8cb78939d445481b293e3bf3a0771de5b5d02`

```dockerfile
```

-	Layers:
	-	`sha256:a747702af18d6ff618a54d3f2fa07227a4717e1973974421e54f993bad3cd495`  
		Last Modified: Wed, 02 Jul 2025 07:18:46 GMT  
		Size: 18.3 MB (18271650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2e29e55a91cc90b3d04da26d178dcacdae066c7e9f69cb18b3127fafca20ad`  
		Last Modified: Wed, 02 Jul 2025 07:18:47 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:dc578a780f969c27d4eca6b8a1ce0a482a11034012c9c20d377cfe9cf6b49335
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:a7f8504bc633056c364e3f6d99e5f7ff04e058526bb3d52fb032d3de8a9038a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a25ace67f66dacdb993f06f9e82370c801912f2d717f0797aa041f2f42b999c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d91b30c7ff9e55f538edeb417f53d4dfb70cc741627149d8b2bc11bb4c6d855`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 683.8 KB (683757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440c05e0c6d584917470bf0bc6bf509bcd76b9d9764f2423cb91dfa3e85246d`  
		Last Modified: Wed, 02 Jul 2025 04:13:14 GMT  
		Size: 6.7 MB (6745407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac55c4ebd36770b2e03164d34f70b12811197e63c53da6d33184e1f4971a1d76`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 94.0 KB (93995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2e7ff368031161d10e8464ade9bd7caecbbe51f61c0c96f634858e2cbbe1c`  
		Last Modified: Wed, 02 Jul 2025 04:13:22 GMT  
		Size: 132.4 MB (132410874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a3327298c7d6a49febab8e70915f0fc56946fe8468d9b8499c90f344e9f08`  
		Last Modified: Wed, 02 Jul 2025 04:13:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:38a94f29cc7965911c3c9110b3bfa6b8860f25adfbb8508e0ca0a36be1fa37a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18312309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d26f79f09f7b72ab53ad2dd176573fadf7f4af07a13293f9053c42db7fb25af`

```dockerfile
```

-	Layers:
	-	`sha256:03919e412d7535fa4ee1db1b05bb40fe9968c40931079ed9cd9c4bce90277226`  
		Last Modified: Wed, 02 Jul 2025 07:18:33 GMT  
		Size: 18.3 MB (18297644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4065d67af5621efef8c1441e3088e6c0ff7576b9c18ade75fc1655afb22a1e6`  
		Last Modified: Wed, 02 Jul 2025 07:18:33 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89d9724ded43eb34411b0cb602be12daeb99966c15b1e78f0a01ddd1415aa6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163485397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf4f60c551638a7621157a3ae03b6a5ed9659a983e64a54c2fdb093feed8446`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0442a1d4a79025dbcdcfbd815172d59b26c114b17cdaa8f9c3df7fa970cb7d3`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 683.9 KB (683864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4422f12af1f3a17b517d83fc3fe632ead7aee3effa0b2c855c2393df3d367`  
		Last Modified: Wed, 02 Jul 2025 06:28:01 GMT  
		Size: 6.8 MB (6758851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b92ecee5f5684c84f0ba3f0a3be55b1af194fe26708d1468ab483ea7203e7c`  
		Last Modified: Wed, 02 Jul 2025 06:28:00 GMT  
		Size: 94.1 KB (94103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80205a32428d80d47d738a520ae436ad7d1aaca7a54a3b8bc5b46b3fefc0b8`  
		Last Modified: Wed, 02 Jul 2025 06:30:50 GMT  
		Size: 127.1 MB (127092365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e416b86f6cb653b375173be75b902fa6b1fd9c4fd4e49908e63a7c2421b648`  
		Last Modified: Wed, 02 Jul 2025 06:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:88c6acb8d58ecca3506cfcee5e6cc152ddb2f1f3e204489de3042695c69298a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18286440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb45d223c5bec05a4d2da002eb8cb78939d445481b293e3bf3a0771de5b5d02`

```dockerfile
```

-	Layers:
	-	`sha256:a747702af18d6ff618a54d3f2fa07227a4717e1973974421e54f993bad3cd495`  
		Last Modified: Wed, 02 Jul 2025 07:18:46 GMT  
		Size: 18.3 MB (18271650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2e29e55a91cc90b3d04da26d178dcacdae066c7e9f69cb18b3127fafca20ad`  
		Last Modified: Wed, 02 Jul 2025 07:18:47 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json
