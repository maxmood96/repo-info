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
$ docker pull ros@sha256:370191995451bb63f2e37bb2f6636a09f66ca810d0865703058361dc6ac70c87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:50ca1476252d8fe40674d7dea071c26fb42150aa2caeb802d8c28eebb4e7eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263188860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5ee94de7e3852df5106a42cfeab65f5ab15d194963accc6886e8641cc08a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:6d5170a3809927780690b6aa99b24993fe9d338800198d4b8bf4c9dc84bb9598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770354243fc7649f5cb1beb98b9a2f7e0668df502b493957f0d1ce6acc9ea75`

```dockerfile
```

-	Layers:
	-	`sha256:b46162c66a49438be9b0ca0afc097ed4b1ead8c95b9953ed9fc1b7088211f252`  
		Last Modified: Fri, 14 Nov 2025 02:17:47 GMT  
		Size: 23.7 MB (23678894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3a59713e8a6d17917071f2a700a2b1634fab032b25eddc10b2b25a98a95f45`  
		Last Modified: Fri, 14 Nov 2025 02:17:48 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eea6e5a39edbbb606c3ab6a9755da16b0164b38883bd56f39ebf3268841960bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255747329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e63ae3b688e64872daf5a5e363a67e43249ef25fc4da49c363aec409953cd64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:292b8380d247e9ac7d575be970a46b0a90e4568fa92841ebd697d87c1240d9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23708396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a922522fecc436cb20f7040b0227e8dc8c46b5f9ac9981d9425fb52d2ab0d397`

```dockerfile
```

-	Layers:
	-	`sha256:6f10a08a03a11cd3796fdc3b6159f068cf58a7b55c4910257a8d3300f71e55e9`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 23.7 MB (23691911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb23ec2ff4e9d03fd8af8d8d1f01c4a5c73fdbd14991061c2dd3fac91a32092c`  
		Last Modified: Fri, 14 Nov 2025 02:18:09 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:b28e43e044e231ed2f13f6d351586191037e6ff4de8dfd49c8bba7c4ef59575b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:cd95809fb5038fd44edf79e271b48038a9f54c803dd057cfab4ada139d4da977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.2 MB (955165950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38c757f5c9847defc2c884ec0dea713341a46d4c57f4085f9af2de9f437edd`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921fc85add6643dfaca09b6d4648b9a390d9c25a0a7b76a339eddd1abbce10a`  
		Last Modified: Thu, 02 Oct 2025 08:42:30 GMT  
		Size: 98.0 MB (97961155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff84f73176326d41acddc485f9bb72d1fb4023657107c3be33f1cc35bf9967`  
		Last Modified: Thu, 02 Oct 2025 08:42:23 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077021ac2104c3764dc0ea75f26afc46bc0ff43df66f57352f9984201ac3b88d`  
		Last Modified: Thu, 02 Oct 2025 08:42:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f36953130fd4527f52aa6fb545f561ac1a6ced8e51eb6bdc3245648a772f9`  
		Last Modified: Thu, 02 Oct 2025 08:42:26 GMT  
		Size: 23.3 MB (23318499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec12be7f73945dd776113708f0deb24b26153cebc4a2cfbfb92753be821195`  
		Last Modified: Thu, 02 Oct 2025 13:18:33 GMT  
		Size: 692.1 MB (692065609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3abbef0fd6d5fd5a1af78a6568be69ccde5283c27d7e6c56b0c8ca00d1f66c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58777209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b97d9adebcc2f4b35c1c7f94788fd4d2191fca9d9801f63466c41828f8ed11`

```dockerfile
```

-	Layers:
	-	`sha256:c4dc946f3e88502c233637ff403efcca49da9f493ba42cb19ea6ec5c40d70b3a`  
		Last Modified: Thu, 02 Oct 2025 13:17:21 GMT  
		Size: 58.8 MB (58767814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad2bd5128e7058c90801145de9f9fa359dfe880c2a2290bb8ca0a4b1f1fd1d1`  
		Last Modified: Thu, 02 Oct 2025 13:17:22 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3b3b6ff97b4b53dd43e628fafbb647a88f6f51221d42d95c2bdf2223357f6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915609144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a0d501c7ddfa99ac60b138d72d94f81ea235108131d6732a35a4f3f8011ab2`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed460bd7610e695293d4aad069edacd2754484b0f55e8dfc4e3a8975b61299`  
		Last Modified: Thu, 02 Oct 2025 03:14:51 GMT  
		Size: 95.5 MB (95536513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a893c7ab244785cc16456c334bb289d0f040a1c336fbd113a913a0eb8a33`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e433a4c2230dce1a5c2cd4a3f00afd6ad4255d21ceffab538d491b369a751d`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4bf5c7c27cec9add8df7118cd31c934b55e265db6bb75c5d7da8b912340ad`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 22.7 MB (22715620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5e2cb20c1dc183518b13ed55eccd22d11d50b212a21d414606337cc6c9dfa8`  
		Last Modified: Thu, 02 Oct 2025 04:21:25 GMT  
		Size: 660.0 MB (660004040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:95b26e59188683835237e4192a1143316b84eaff8fe03e7b9c33c92e1101a8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58761610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd567ee08a59ee70095b9e58ed96d33edd2ddf1154a0ca31f825d9da5e75bd3`

```dockerfile
```

-	Layers:
	-	`sha256:919c156d38ce0596b3d6b68493b917d2213f9ac75124f2e6c45cf24ab74b5e9f`  
		Last Modified: Thu, 02 Oct 2025 04:19:12 GMT  
		Size: 58.8 MB (58752135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a37e5fdd450e9e532057f7bb383c800c970154102b4dabb6d8170b92d8bbb5`  
		Last Modified: Thu, 02 Oct 2025 04:19:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:b28e43e044e231ed2f13f6d351586191037e6ff4de8dfd49c8bba7c4ef59575b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:cd95809fb5038fd44edf79e271b48038a9f54c803dd057cfab4ada139d4da977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.2 MB (955165950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c38c757f5c9847defc2c884ec0dea713341a46d4c57f4085f9af2de9f437edd`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3acafe09bcaac051ef6d1f97c0d2d173c28b505278e8f1e352a4a38b3e6d53`  
		Last Modified: Thu, 02 Oct 2025 05:18:00 GMT  
		Size: 1.2 MB (1214024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb63b1a7685a896ac7f919e64c1bb1c2f836892f3b8d0b2d150496a95cdd84e`  
		Last Modified: Thu, 02 Oct 2025 05:18:03 GMT  
		Size: 6.0 MB (5995057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d979177940451251cb1465ddc2a4d20b9165b080ce72028029a0972462d2687`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 97.1 KB (97120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79595a0d502923d1f8007afd19da2017254078ed965e44ae4494abeb5ae95275`  
		Last Modified: Thu, 02 Oct 2025 05:18:08 GMT  
		Size: 104.6 MB (104600746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8627d2f078576b7acfca765aa3f0dc5295ae62399615969ca25316ff869c80b1`  
		Last Modified: Thu, 02 Oct 2025 05:17:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921fc85add6643dfaca09b6d4648b9a390d9c25a0a7b76a339eddd1abbce10a`  
		Last Modified: Thu, 02 Oct 2025 08:42:30 GMT  
		Size: 98.0 MB (97961155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fff84f73176326d41acddc485f9bb72d1fb4023657107c3be33f1cc35bf9967`  
		Last Modified: Thu, 02 Oct 2025 08:42:23 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077021ac2104c3764dc0ea75f26afc46bc0ff43df66f57352f9984201ac3b88d`  
		Last Modified: Thu, 02 Oct 2025 08:42:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f36953130fd4527f52aa6fb545f561ac1a6ced8e51eb6bdc3245648a772f9`  
		Last Modified: Thu, 02 Oct 2025 08:42:26 GMT  
		Size: 23.3 MB (23318499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ec12be7f73945dd776113708f0deb24b26153cebc4a2cfbfb92753be821195`  
		Last Modified: Thu, 02 Oct 2025 13:18:33 GMT  
		Size: 692.1 MB (692065609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:3abbef0fd6d5fd5a1af78a6568be69ccde5283c27d7e6c56b0c8ca00d1f66c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58777209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b97d9adebcc2f4b35c1c7f94788fd4d2191fca9d9801f63466c41828f8ed11`

```dockerfile
```

-	Layers:
	-	`sha256:c4dc946f3e88502c233637ff403efcca49da9f493ba42cb19ea6ec5c40d70b3a`  
		Last Modified: Thu, 02 Oct 2025 13:17:21 GMT  
		Size: 58.8 MB (58767814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad2bd5128e7058c90801145de9f9fa359dfe880c2a2290bb8ca0a4b1f1fd1d1`  
		Last Modified: Thu, 02 Oct 2025 13:17:22 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3b3b6ff97b4b53dd43e628fafbb647a88f6f51221d42d95c2bdf2223357f6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915609144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a0d501c7ddfa99ac60b138d72d94f81ea235108131d6732a35a4f3f8011ab2`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acf2e35d271b16f5560e89ab696b0b3860e769bdd01a98be8d27f2b303af9b`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 1.2 MB (1214273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc15a8d1c24650e7b013c9200269a76754b2ebe61c4c0c7c702ce9f71ffa1f0`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 5.9 MB (5940017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee1af528a3785d2b72ab104c943f6ca6d0139eff238112c82bf3a9ddb6d098`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 97.3 KB (97302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1903d03b380fc6eff49a30428f62cd153e71d401b3121f93b65c9b42a9495b`  
		Last Modified: Thu, 02 Oct 2025 01:33:09 GMT  
		Size: 102.3 MB (102341319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff1d9c6fb2a0e50f3f08713eb4a2f3474bd3246332d422e24690b33c09309f4`  
		Last Modified: Thu, 02 Oct 2025 01:33:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed460bd7610e695293d4aad069edacd2754484b0f55e8dfc4e3a8975b61299`  
		Last Modified: Thu, 02 Oct 2025 03:14:51 GMT  
		Size: 95.5 MB (95536513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4a893c7ab244785cc16456c334bb289d0f040a1c336fbd113a913a0eb8a33`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 374.3 KB (374273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e433a4c2230dce1a5c2cd4a3f00afd6ad4255d21ceffab538d491b369a751d`  
		Last Modified: Thu, 02 Oct 2025 03:14:45 GMT  
		Size: 2.5 KB (2485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4bf5c7c27cec9add8df7118cd31c934b55e265db6bb75c5d7da8b912340ad`  
		Last Modified: Thu, 02 Oct 2025 02:28:56 GMT  
		Size: 22.7 MB (22715620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5e2cb20c1dc183518b13ed55eccd22d11d50b212a21d414606337cc6c9dfa8`  
		Last Modified: Thu, 02 Oct 2025 04:21:25 GMT  
		Size: 660.0 MB (660004040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:95b26e59188683835237e4192a1143316b84eaff8fe03e7b9c33c92e1101a8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58761610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd567ee08a59ee70095b9e58ed96d33edd2ddf1154a0ca31f825d9da5e75bd3`

```dockerfile
```

-	Layers:
	-	`sha256:919c156d38ce0596b3d6b68493b917d2213f9ac75124f2e6c45cf24ab74b5e9f`  
		Last Modified: Thu, 02 Oct 2025 04:19:12 GMT  
		Size: 58.8 MB (58752135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a37e5fdd450e9e532057f7bb383c800c970154102b4dabb6d8170b92d8bbb5`  
		Last Modified: Thu, 02 Oct 2025 04:19:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:370191995451bb63f2e37bb2f6636a09f66ca810d0865703058361dc6ac70c87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:50ca1476252d8fe40674d7dea071c26fb42150aa2caeb802d8c28eebb4e7eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263188860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5ee94de7e3852df5106a42cfeab65f5ab15d194963accc6886e8641cc08a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:6d5170a3809927780690b6aa99b24993fe9d338800198d4b8bf4c9dc84bb9598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770354243fc7649f5cb1beb98b9a2f7e0668df502b493957f0d1ce6acc9ea75`

```dockerfile
```

-	Layers:
	-	`sha256:b46162c66a49438be9b0ca0afc097ed4b1ead8c95b9953ed9fc1b7088211f252`  
		Last Modified: Fri, 14 Nov 2025 02:17:47 GMT  
		Size: 23.7 MB (23678894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3a59713e8a6d17917071f2a700a2b1634fab032b25eddc10b2b25a98a95f45`  
		Last Modified: Fri, 14 Nov 2025 02:17:48 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eea6e5a39edbbb606c3ab6a9755da16b0164b38883bd56f39ebf3268841960bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255747329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e63ae3b688e64872daf5a5e363a67e43249ef25fc4da49c363aec409953cd64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:292b8380d247e9ac7d575be970a46b0a90e4568fa92841ebd697d87c1240d9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23708396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a922522fecc436cb20f7040b0227e8dc8c46b5f9ac9981d9425fb52d2ab0d397`

```dockerfile
```

-	Layers:
	-	`sha256:6f10a08a03a11cd3796fdc3b6159f068cf58a7b55c4910257a8d3300f71e55e9`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 23.7 MB (23691911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb23ec2ff4e9d03fd8af8d8d1f01c4a5c73fdbd14991061c2dd3fac91a32092c`  
		Last Modified: Fri, 14 Nov 2025 02:18:09 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:370191995451bb63f2e37bb2f6636a09f66ca810d0865703058361dc6ac70c87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:50ca1476252d8fe40674d7dea071c26fb42150aa2caeb802d8c28eebb4e7eaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263188860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c5ee94de7e3852df5106a42cfeab65f5ab15d194963accc6886e8641cc08a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cff80b11e7ea34ab86bcacd5b24c0151cb62a2f2b139d6c1dff241d417b66a`  
		Last Modified: Fri, 14 Nov 2025 00:36:31 GMT  
		Size: 98.0 MB (97964021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d91a7c7692ffd77b73c4f0cfc282e9680679ee57af898c603e0061783a606d`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 379.6 KB (379568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa9edd4f4cd759ffb53f1ce62adb1e2d69606221ce90ee89d1bb1afdfa04ad`  
		Last Modified: Fri, 14 Nov 2025 00:36:20 GMT  
		Size: 2.5 KB (2520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46530456e3880c32393b7059d657070ca80668f06d33fe132f74fd8f963806a0`  
		Last Modified: Fri, 14 Nov 2025 00:36:21 GMT  
		Size: 23.3 MB (23318823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:6d5170a3809927780690b6aa99b24993fe9d338800198d4b8bf4c9dc84bb9598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23695242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1770354243fc7649f5cb1beb98b9a2f7e0668df502b493957f0d1ce6acc9ea75`

```dockerfile
```

-	Layers:
	-	`sha256:b46162c66a49438be9b0ca0afc097ed4b1ead8c95b9953ed9fc1b7088211f252`  
		Last Modified: Fri, 14 Nov 2025 02:17:47 GMT  
		Size: 23.7 MB (23678894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3a59713e8a6d17917071f2a700a2b1634fab032b25eddc10b2b25a98a95f45`  
		Last Modified: Fri, 14 Nov 2025 02:17:48 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eea6e5a39edbbb606c3ab6a9755da16b0164b38883bd56f39ebf3268841960bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255747329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e63ae3b688e64872daf5a5e363a67e43249ef25fc4da49c363aec409953cd64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729efb00a70a0c0d928c0d62fc7184f4fd90cccd1b759d3b0e773aa94d685e1f`  
		Last Modified: Fri, 14 Nov 2025 00:37:25 GMT  
		Size: 95.6 MB (95574007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb022b88586414ed2ea4c8996cb1f01bb5a2e8de09e64f6311f0f7e5c4ef65`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 379.6 KB (379566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d16b1d4d71c6246168df8eca3aae32364fa518f6904aea25ec565c4706572a`  
		Last Modified: Fri, 14 Nov 2025 00:37:15 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ef97a6139a6958755971439bb4f5b21436f50e9ba6363101346a306ddbbaf`  
		Last Modified: Fri, 14 Nov 2025 00:37:17 GMT  
		Size: 22.7 MB (22715657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:292b8380d247e9ac7d575be970a46b0a90e4568fa92841ebd697d87c1240d9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23708396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a922522fecc436cb20f7040b0227e8dc8c46b5f9ac9981d9425fb52d2ab0d397`

```dockerfile
```

-	Layers:
	-	`sha256:6f10a08a03a11cd3796fdc3b6159f068cf58a7b55c4910257a8d3300f71e55e9`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 23.7 MB (23691911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb23ec2ff4e9d03fd8af8d8d1f01c4a5c73fdbd14991061c2dd3fac91a32092c`  
		Last Modified: Fri, 14 Nov 2025 02:18:09 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:41fcc905f0f9a4457176b13c45cdf96aa4ca78e87c5f763bbcb4ba258c2a1119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1b7bc03289086014c668f8ccbe79e695b7f9fa664f2051244fb533876a369136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141523928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e99193c4c42d72a55a8eeb26d95b92f9a7f9af8346609b53d94bc893fefc11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:57ee80c600998f8068442d113d8ee0807739ea0cee8a65b156ac18446ec45740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17673284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc69088c126bb40646628a29e6042c71b1ef516c177b297846f1b3e501c680a4`

```dockerfile
```

-	Layers:
	-	`sha256:535aba84158df29180f4d18bcf63138b4978a8857127d895ae421b3178d05351`  
		Last Modified: Fri, 14 Nov 2025 02:17:56 GMT  
		Size: 17.7 MB (17658670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f247ca3c0dd8eb3914bb57ace0c3123fb7aed0a60249243405bf499b7297d951`  
		Last Modified: Fri, 14 Nov 2025 02:17:57 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9d310b586219f0b7d8f2aa5ce679665a8af4419f46764657ef98ed57ff59afa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137075606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a19568c32acb20a4beceb411c7f804c416477cdf0650b552bcd3b6ccaa48b3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:b28ade8a1be229037c3460e86d228d12aec37861ea89367f43b2555aa64eb72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17659754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc44cf26dd1a8be6ed576aeb6e90218d77a16a5fdf113460581a48a4b72ae61`

```dockerfile
```

-	Layers:
	-	`sha256:5efcbfc6973cc010f2b29699d4069d9dd1e31ed9002c537e0f7f4890ff52ff6d`  
		Last Modified: Fri, 14 Nov 2025 02:18:13 GMT  
		Size: 17.6 MB (17645015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8c54a7e88ccb06665fc5ccd966a53155e343cf9ff7e93db8a779a4656afd18`  
		Last Modified: Fri, 14 Nov 2025 02:18:14 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:41fcc905f0f9a4457176b13c45cdf96aa4ca78e87c5f763bbcb4ba258c2a1119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1b7bc03289086014c668f8ccbe79e695b7f9fa664f2051244fb533876a369136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141523928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e99193c4c42d72a55a8eeb26d95b92f9a7f9af8346609b53d94bc893fefc11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:34:29 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:34:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0141529a775c84277272b36bdcb0a1e5b3b5dcd84278ade77a4196b9b2282de`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 1.2 MB (1214093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33ee036c174cbb0c42963e661f34e354ab74050d1cf9aa89bd59262b521a73`  
		Last Modified: Thu, 13 Nov 2025 23:35:02 GMT  
		Size: 6.0 MB (5995198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077c07b8ae5b2a94b882610efb215cd67e3614d117a0f4261c93579b1a9621f`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 97.2 KB (97191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f68bb720c68840b09c9d260514f2dd9b1688a529ff534450d8af54c19575558`  
		Last Modified: Thu, 13 Nov 2025 23:35:12 GMT  
		Size: 104.7 MB (104680453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66580f77fd4cfeb9be2caa28c9841848eabf40f340d2412cc7a38dd9b35a2de0`  
		Last Modified: Thu, 13 Nov 2025 23:35:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:57ee80c600998f8068442d113d8ee0807739ea0cee8a65b156ac18446ec45740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17673284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc69088c126bb40646628a29e6042c71b1ef516c177b297846f1b3e501c680a4`

```dockerfile
```

-	Layers:
	-	`sha256:535aba84158df29180f4d18bcf63138b4978a8857127d895ae421b3178d05351`  
		Last Modified: Fri, 14 Nov 2025 02:17:56 GMT  
		Size: 17.7 MB (17658670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f247ca3c0dd8eb3914bb57ace0c3123fb7aed0a60249243405bf499b7297d951`  
		Last Modified: Fri, 14 Nov 2025 02:17:57 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9d310b586219f0b7d8f2aa5ce679665a8af4419f46764657ef98ed57ff59afa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137075606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a19568c32acb20a4beceb411c7f804c416477cdf0650b552bcd3b6ccaa48b3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:51 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:33:35 GMT
ENV ROS_DISTRO=humble
# Thu, 13 Nov 2025 23:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:33:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:33:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0384257e8ceb3da36a15f3bafc96847af59fb775cdc666458d27edcfd9b187f`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 1.2 MB (1214260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05540726e7bedf91a61e708c3e6a79cdbb0eaf69a17706b9eff453d3e9671801`  
		Last Modified: Thu, 13 Nov 2025 23:34:10 GMT  
		Size: 5.9 MB (5939824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec98954ce15533534b2019d64194c6e3d944f3e7c377d51e50936c74154d27`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 97.3 KB (97291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb991aa5691822095540349089295bb993c313a861c62818de0f20dee126201a`  
		Last Modified: Thu, 13 Nov 2025 23:34:21 GMT  
		Size: 102.4 MB (102440159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62a0dad0635de07dfec723e49bc082bf6975da918c6d0ad4cfc1f0c8e557fd5`  
		Last Modified: Thu, 13 Nov 2025 23:34:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:b28ade8a1be229037c3460e86d228d12aec37861ea89367f43b2555aa64eb72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17659754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc44cf26dd1a8be6ed576aeb6e90218d77a16a5fdf113460581a48a4b72ae61`

```dockerfile
```

-	Layers:
	-	`sha256:5efcbfc6973cc010f2b29699d4069d9dd1e31ed9002c537e0f7f4890ff52ff6d`  
		Last Modified: Fri, 14 Nov 2025 02:18:13 GMT  
		Size: 17.6 MB (17645015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8c54a7e88ccb06665fc5ccd966a53155e343cf9ff7e93db8a779a4656afd18`  
		Last Modified: Fri, 14 Nov 2025 02:18:14 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:c5705f613a6427d07be6f3d0aba40068e16c3dea05604e1c95c63eac79fea658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:681694dce70804868341b866fce5f8f86582030365772ae9a5be108b0a05a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295937776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea524e20e2080c9aed93becdef12964c3d068b0fad0cee3fcfd10ba145d7f33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:9961876ad27e37456d0f6e52d4bbf09cf51839c9b7b4df64c33041aa746ce7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e3e5912803cb2bdda7f03558c402c46d02e328783e95b380d496be344130b`

```dockerfile
```

-	Layers:
	-	`sha256:6ea56e3ff74d3e080e78e83a3aeaf07ea40b29f3ff6d947e9165f101d3bbd74f`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 24.5 MB (24544143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e944a9cd91fcd09d96336d2a0eb56da13f45ec8f6388ddbda77a26fcc107f3f`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:462af74e10cf889815cf401917626987fe9007341fdeb79c7ab58dc7d41b4ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2982ce015e6626d11b7fda013ffd30c09997fde2672ba464a03d23906dbce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:b8b43856e654d0fc72f295303ee53ae6d08e0e8dd7ed43713208d868bb089cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a63b0c075a33b8ab755fbc30142ba4034eded4448383f1115d2fec3dac282f`

```dockerfile
```

-	Layers:
	-	`sha256:757f2f8f7137b442bf37112c5b0e6e073805a55ce194e37e577a66c39a4390d4`  
		Last Modified: Fri, 14 Nov 2025 02:18:33 GMT  
		Size: 24.6 MB (24566416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f535be96aa6aebb0fc43577f12f4bd69d0c29b1fc7da9391df5a85f1400f7a2`  
		Last Modified: Fri, 14 Nov 2025 02:18:34 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:ce43a7f6fb6d6b2c7b8e6c0f9f33bad1f17331b06dd2c2be3a0b4dbfbfebe791
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:6b2a2f4da80d4558014734d8e07bca4ef8f0699474db2c299981756d50f7d27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081069008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d74b5b0734ae63a5e98ff7cb8d4c2302c16e3c71270548f2f5b13c2ad6dce`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d108b0455d26874467bb535ac1b0fb32de8c484d3ffd3710dbea124ffc245adb`  
		Last Modified: Thu, 09 Oct 2025 21:24:11 GMT  
		Size: 120.1 MB (120110076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d51c9d4c4e7ee2f490765efc765899f07ad09fdba245ea055344af0b2e9f2d`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36af06f6ea928bae29ab81e26c4b9c86a6fcd53abfc26c09e3d892679ba309`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 110.2 MB (110182197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41918390b2c6a6dc558d65d0c6c2961345a18ba76758672d27188711abc1c0a4`  
		Last Modified: Thu, 09 Oct 2025 22:21:04 GMT  
		Size: 378.6 KB (378566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04beb5559111f3e67bb33a9f809f6f48b46b864c326c7929e27268c217812922`  
		Last Modified: Thu, 09 Oct 2025 22:21:03 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e60e3858f8ce453118ccbb8f050ce6fd37bb2be26ba42111ce1a376bd19c9fb`  
		Last Modified: Thu, 09 Oct 2025 22:21:11 GMT  
		Size: 28.0 MB (27998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffb5005bc4b98e65f44bcdd882087eca373f09d6dfa49bb5aa2c0243c5a40f0`  
		Last Modified: Fri, 10 Oct 2025 04:43:34 GMT  
		Size: 785.1 MB (785148377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c9bda4db142150ddf32bef39d06b94d125883c589bf702cb02b297ff39f2a595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60714715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce914a0caaf81baff1e0bf336f88b050adf78fc5193edc7f2fb88d6bcc012ee`

```dockerfile
```

-	Layers:
	-	`sha256:0e93a43ffdc6454a38ee6eee73c37c6881580f352d03152e8ef60591e6b7199c`  
		Last Modified: Fri, 10 Oct 2025 04:17:50 GMT  
		Size: 60.7 MB (60705333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dcc51f87619c01901960ae1e13bcff779f3384ffc04d779dffe6de4d35c58ec`  
		Last Modified: Fri, 10 Oct 2025 04:17:52 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c32cebb92edd6f37d6e00c52effcf3531a10df53a97647711b18630b0f6b063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.5 MB (979526410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e2324f62274b44046fbd92360287237910aa4025f9ea2c2dae42377a7c320a`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb091d265588996d309a696050b8d873efa1a977c33604e5241d0745dae157`  
		Last Modified: Thu, 09 Oct 2025 21:26:15 GMT  
		Size: 114.9 MB (114893499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1fd8e39aed1e99b329b904170291216c4df87e9a05ceb6e27c4e277cef7e6e`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095a784b3b596b61762df7cc4a5b6b7c1eac9e65fe28df5b367b898945487963`  
		Last Modified: Thu, 09 Oct 2025 22:21:27 GMT  
		Size: 105.6 MB (105591210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaa47f3fcdb4ec2a9d6dc3dffc6e5120ff9e2adc87862b6d659c3a7d1c774b3`  
		Last Modified: Thu, 09 Oct 2025 22:21:16 GMT  
		Size: 378.6 KB (378568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c8c6a1a45bbff1319860478a95a64ccdd0c0ae9d251b59ce95cc74055ae1e`  
		Last Modified: Thu, 09 Oct 2025 22:21:16 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19515dadcdaaa740f70b490c4215ebc580a396e3c86fe1f5ab905ad29efb8fc`  
		Last Modified: Thu, 09 Oct 2025 22:49:40 GMT  
		Size: 27.1 MB (27097082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f171c14846542ed296c675afa9d8ea3c55bd4cea30691e02a185c8d9fb4d88a`  
		Last Modified: Fri, 10 Oct 2025 06:37:37 GMT  
		Size: 695.2 MB (695162942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:92516cf0ed9ffd640dec74fb1bbfb90d4c79374a05148b15e278e2eb2668b075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c39e9e9c9bcdf50a443387e6b7ba8e42b4a8a47706a66a5ed8ae0afa7371b3`

```dockerfile
```

-	Layers:
	-	`sha256:fe6d24a4cd4e06659f5d1719f8d4deb7587a6487e0e2db8e3a249f4b94a9e34f`  
		Last Modified: Fri, 10 Oct 2025 04:19:46 GMT  
		Size: 60.6 MB (60635858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6af18564ea9310b70fd7921a32ec73c1a5e689e84d5c4f2527b90df5a02b70`  
		Last Modified: Fri, 10 Oct 2025 04:19:47 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:ce43a7f6fb6d6b2c7b8e6c0f9f33bad1f17331b06dd2c2be3a0b4dbfbfebe791
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:6b2a2f4da80d4558014734d8e07bca4ef8f0699474db2c299981756d50f7d27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081069008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d74b5b0734ae63a5e98ff7cb8d4c2302c16e3c71270548f2f5b13c2ad6dce`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d108b0455d26874467bb535ac1b0fb32de8c484d3ffd3710dbea124ffc245adb`  
		Last Modified: Thu, 09 Oct 2025 21:24:11 GMT  
		Size: 120.1 MB (120110076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d51c9d4c4e7ee2f490765efc765899f07ad09fdba245ea055344af0b2e9f2d`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36af06f6ea928bae29ab81e26c4b9c86a6fcd53abfc26c09e3d892679ba309`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 110.2 MB (110182197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41918390b2c6a6dc558d65d0c6c2961345a18ba76758672d27188711abc1c0a4`  
		Last Modified: Thu, 09 Oct 2025 22:21:04 GMT  
		Size: 378.6 KB (378566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04beb5559111f3e67bb33a9f809f6f48b46b864c326c7929e27268c217812922`  
		Last Modified: Thu, 09 Oct 2025 22:21:03 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e60e3858f8ce453118ccbb8f050ce6fd37bb2be26ba42111ce1a376bd19c9fb`  
		Last Modified: Thu, 09 Oct 2025 22:21:11 GMT  
		Size: 28.0 MB (27998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffb5005bc4b98e65f44bcdd882087eca373f09d6dfa49bb5aa2c0243c5a40f0`  
		Last Modified: Fri, 10 Oct 2025 04:43:34 GMT  
		Size: 785.1 MB (785148377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c9bda4db142150ddf32bef39d06b94d125883c589bf702cb02b297ff39f2a595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60714715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce914a0caaf81baff1e0bf336f88b050adf78fc5193edc7f2fb88d6bcc012ee`

```dockerfile
```

-	Layers:
	-	`sha256:0e93a43ffdc6454a38ee6eee73c37c6881580f352d03152e8ef60591e6b7199c`  
		Last Modified: Fri, 10 Oct 2025 04:17:50 GMT  
		Size: 60.7 MB (60705333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dcc51f87619c01901960ae1e13bcff779f3384ffc04d779dffe6de4d35c58ec`  
		Last Modified: Fri, 10 Oct 2025 04:17:52 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c32cebb92edd6f37d6e00c52effcf3531a10df53a97647711b18630b0f6b063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.5 MB (979526410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e2324f62274b44046fbd92360287237910aa4025f9ea2c2dae42377a7c320a`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb091d265588996d309a696050b8d873efa1a977c33604e5241d0745dae157`  
		Last Modified: Thu, 09 Oct 2025 21:26:15 GMT  
		Size: 114.9 MB (114893499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1fd8e39aed1e99b329b904170291216c4df87e9a05ceb6e27c4e277cef7e6e`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095a784b3b596b61762df7cc4a5b6b7c1eac9e65fe28df5b367b898945487963`  
		Last Modified: Thu, 09 Oct 2025 22:21:27 GMT  
		Size: 105.6 MB (105591210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaa47f3fcdb4ec2a9d6dc3dffc6e5120ff9e2adc87862b6d659c3a7d1c774b3`  
		Last Modified: Thu, 09 Oct 2025 22:21:16 GMT  
		Size: 378.6 KB (378568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c8c6a1a45bbff1319860478a95a64ccdd0c0ae9d251b59ce95cc74055ae1e`  
		Last Modified: Thu, 09 Oct 2025 22:21:16 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19515dadcdaaa740f70b490c4215ebc580a396e3c86fe1f5ab905ad29efb8fc`  
		Last Modified: Thu, 09 Oct 2025 22:49:40 GMT  
		Size: 27.1 MB (27097082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f171c14846542ed296c675afa9d8ea3c55bd4cea30691e02a185c8d9fb4d88a`  
		Last Modified: Fri, 10 Oct 2025 06:37:37 GMT  
		Size: 695.2 MB (695162942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:92516cf0ed9ffd640dec74fb1bbfb90d4c79374a05148b15e278e2eb2668b075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c39e9e9c9bcdf50a443387e6b7ba8e42b4a8a47706a66a5ed8ae0afa7371b3`

```dockerfile
```

-	Layers:
	-	`sha256:fe6d24a4cd4e06659f5d1719f8d4deb7587a6487e0e2db8e3a249f4b94a9e34f`  
		Last Modified: Fri, 10 Oct 2025 04:19:46 GMT  
		Size: 60.6 MB (60635858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6af18564ea9310b70fd7921a32ec73c1a5e689e84d5c4f2527b90df5a02b70`  
		Last Modified: Fri, 10 Oct 2025 04:19:47 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:c5705f613a6427d07be6f3d0aba40068e16c3dea05604e1c95c63eac79fea658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:681694dce70804868341b866fce5f8f86582030365772ae9a5be108b0a05a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295937776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea524e20e2080c9aed93becdef12964c3d068b0fad0cee3fcfd10ba145d7f33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:9961876ad27e37456d0f6e52d4bbf09cf51839c9b7b4df64c33041aa746ce7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e3e5912803cb2bdda7f03558c402c46d02e328783e95b380d496be344130b`

```dockerfile
```

-	Layers:
	-	`sha256:6ea56e3ff74d3e080e78e83a3aeaf07ea40b29f3ff6d947e9165f101d3bbd74f`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 24.5 MB (24544143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e944a9cd91fcd09d96336d2a0eb56da13f45ec8f6388ddbda77a26fcc107f3f`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:462af74e10cf889815cf401917626987fe9007341fdeb79c7ab58dc7d41b4ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2982ce015e6626d11b7fda013ffd30c09997fde2672ba464a03d23906dbce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b8b43856e654d0fc72f295303ee53ae6d08e0e8dd7ed43713208d868bb089cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a63b0c075a33b8ab755fbc30142ba4034eded4448383f1115d2fec3dac282f`

```dockerfile
```

-	Layers:
	-	`sha256:757f2f8f7137b442bf37112c5b0e6e073805a55ce194e37e577a66c39a4390d4`  
		Last Modified: Fri, 14 Nov 2025 02:18:33 GMT  
		Size: 24.6 MB (24566416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f535be96aa6aebb0fc43577f12f4bd69d0c29b1fc7da9391df5a85f1400f7a2`  
		Last Modified: Fri, 14 Nov 2025 02:18:34 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:c5705f613a6427d07be6f3d0aba40068e16c3dea05604e1c95c63eac79fea658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:681694dce70804868341b866fce5f8f86582030365772ae9a5be108b0a05a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295937776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea524e20e2080c9aed93becdef12964c3d068b0fad0cee3fcfd10ba145d7f33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:9961876ad27e37456d0f6e52d4bbf09cf51839c9b7b4df64c33041aa746ce7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e3e5912803cb2bdda7f03558c402c46d02e328783e95b380d496be344130b`

```dockerfile
```

-	Layers:
	-	`sha256:6ea56e3ff74d3e080e78e83a3aeaf07ea40b29f3ff6d947e9165f101d3bbd74f`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 24.5 MB (24544143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e944a9cd91fcd09d96336d2a0eb56da13f45ec8f6388ddbda77a26fcc107f3f`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:462af74e10cf889815cf401917626987fe9007341fdeb79c7ab58dc7d41b4ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2982ce015e6626d11b7fda013ffd30c09997fde2672ba464a03d23906dbce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b8b43856e654d0fc72f295303ee53ae6d08e0e8dd7ed43713208d868bb089cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a63b0c075a33b8ab755fbc30142ba4034eded4448383f1115d2fec3dac282f`

```dockerfile
```

-	Layers:
	-	`sha256:757f2f8f7137b442bf37112c5b0e6e073805a55ce194e37e577a66c39a4390d4`  
		Last Modified: Fri, 14 Nov 2025 02:18:33 GMT  
		Size: 24.6 MB (24566416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f535be96aa6aebb0fc43577f12f4bd69d0c29b1fc7da9391df5a85f1400f7a2`  
		Last Modified: Fri, 14 Nov 2025 02:18:34 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:467a18374bb776485a1720fc68400b5ed1bac94defd59064e881f3f05f1631c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c420ad6abf1e51f3fdf82a69e107601c4a9e0ef4433fb446cb0bcd829c2cc3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157370334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2944457b1a8ed0d61ede200277c61c7d8cee537cf0efebb74d5af34807313e1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:aa6f6782fb8809d1bdc11cc0c39268ca1f92a4361dde84b2144d0f6d757bbe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2aec48da4050c47322daa0c5d5b229e2dd930655ef7535791496ec90d58b25`

```dockerfile
```

-	Layers:
	-	`sha256:82536b918e41be2698e73a79e1d27e387ec53ce1fc2c9d80f9147f2deede39c8`  
		Last Modified: Fri, 14 Nov 2025 02:18:29 GMT  
		Size: 18.3 MB (18300584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedbc50bfebc9bcdaa2e2ffde4d36995eea034731102d1d2c38550bf4ca41bd2`  
		Last Modified: Fri, 14 Nov 2025 02:18:31 GMT  
		Size: 14.6 KB (14598 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f89dfa391a2e2e87e7d9ece24fafd916df612422c1917fcd6db0cf9285e5d139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151307684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281158ddbed9d2ece10045e53849ad1a4014acfeaedd71e8596c82e203918f10`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:598a7a2553b79860a5e1507079e269b151f344672a5245e849678eb8148d808b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18289315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cbd7d7c2a1bec5bfedf88f6bc329b070c59adb966e6f536249e99e6ed7afe6`

```dockerfile
```

-	Layers:
	-	`sha256:76bd73b0f67cbb130195955194720d3f9ae34819328c3d09aa28ff0e95eb181a`  
		Last Modified: Fri, 14 Nov 2025 02:18:45 GMT  
		Size: 18.3 MB (18274590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042300afc3122faebbb64fad817226bc3428cc12a33bec01b770a4136c6bedeb`  
		Last Modified: Fri, 14 Nov 2025 02:18:46 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:467a18374bb776485a1720fc68400b5ed1bac94defd59064e881f3f05f1631c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c420ad6abf1e51f3fdf82a69e107601c4a9e0ef4433fb446cb0bcd829c2cc3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157370334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2944457b1a8ed0d61ede200277c61c7d8cee537cf0efebb74d5af34807313e1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:aa6f6782fb8809d1bdc11cc0c39268ca1f92a4361dde84b2144d0f6d757bbe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18315182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2aec48da4050c47322daa0c5d5b229e2dd930655ef7535791496ec90d58b25`

```dockerfile
```

-	Layers:
	-	`sha256:82536b918e41be2698e73a79e1d27e387ec53ce1fc2c9d80f9147f2deede39c8`  
		Last Modified: Fri, 14 Nov 2025 02:18:29 GMT  
		Size: 18.3 MB (18300584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedbc50bfebc9bcdaa2e2ffde4d36995eea034731102d1d2c38550bf4ca41bd2`  
		Last Modified: Fri, 14 Nov 2025 02:18:31 GMT  
		Size: 14.6 KB (14598 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f89dfa391a2e2e87e7d9ece24fafd916df612422c1917fcd6db0cf9285e5d139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151307684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281158ddbed9d2ece10045e53849ad1a4014acfeaedd71e8596c82e203918f10`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:598a7a2553b79860a5e1507079e269b151f344672a5245e849678eb8148d808b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18289315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cbd7d7c2a1bec5bfedf88f6bc329b070c59adb966e6f536249e99e6ed7afe6`

```dockerfile
```

-	Layers:
	-	`sha256:76bd73b0f67cbb130195955194720d3f9ae34819328c3d09aa28ff0e95eb181a`  
		Last Modified: Fri, 14 Nov 2025 02:18:45 GMT  
		Size: 18.3 MB (18274590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042300afc3122faebbb64fad817226bc3428cc12a33bec01b770a4136c6bedeb`  
		Last Modified: Fri, 14 Nov 2025 02:18:46 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:300c9505e7261fc80d1aa75c3b1b4beabad4223329ff9d9cd41f608f794df243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:0cc6b0e7d3502ad36eeefc5143505caa15c34cc9f5ab554738732a25b0d917f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311030510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b55dbd0930b08c6f1b091089737b918a73cd9b17a8d0e6d2780cce35b15bf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:0c96703cc6405f14d42e6348a531553c713f4c179dda4974ad64c2f60aeafd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64817ffa8ae718817fbbf00fb0576b8bc53dff162855c53d975b2f3bbb98c32`

```dockerfile
```

-	Layers:
	-	`sha256:5709b9ba52bdf82559bb29618ebccf96f4b01358b316409e5f9d82a413f91448`  
		Last Modified: Fri, 14 Nov 2025 02:18:35 GMT  
		Size: 24.7 MB (24650335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7692c8f6f42bdae33ec2302b3a1c6c86524cf78aede683f6edfb91f5b09a8d75`  
		Last Modified: Fri, 14 Nov 2025 02:18:36 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfc7ec8e8eb439842ca4bcd2f56faa2d0d9b62accad6d220a0985288dc119db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299376599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1899ee8dff90370a8507bd0b1f9315f5203e2085e259642ff4e929efa5246cd4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:d1f76759f0ac3ca705dcc4a37e8c233beb36ac6917e0bc2ef1eba4bcf07871e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a76dd5e9d7e6883d644c5b0b55de743605a2cf961ccac1deb7217ade910f6`

```dockerfile
```

-	Layers:
	-	`sha256:c9e538338867200639c593c1d6b3397b23eae1eddaea021ddeab641705c00a5d`  
		Last Modified: Fri, 14 Nov 2025 02:18:59 GMT  
		Size: 24.7 MB (24672596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91de0fa134b2151a75b51f9e4355bbf5e8746ee15d6a76f7bb13ef422a45bfb`  
		Last Modified: Fri, 14 Nov 2025 02:19:00 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:2e20dcd2750bda5cba97df5f8383daae9797c45ad87cb0c017a13fb8d7c3447e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:361f2141aad13d7cc20ed77ef63af12c7d5c918c348a4bcb8ae5170a1d975e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1096476019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59f899e278fed1f76c2109d800beb593aa1c4563585b810ddc178c429f37fa2`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ad95cd04f77e0c5e96a8b537442f4b5d8be45febd447202f388d3a44663a30`  
		Last Modified: Thu, 09 Oct 2025 22:19:29 GMT  
		Size: 135.0 MB (134981480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b48f84fffbd5e61ea1d7e61e4143c8c98c1f4a0bff60b9411fd58aa4c63864`  
		Last Modified: Thu, 09 Oct 2025 21:25:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1dce87a7f4acd9c8a37db6070c5901c6b8b29cfcc2e7bde7ff0808cddffd70`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 110.2 MB (110185948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30531d5abaa989826e78461584cd1956e1f59a63a17a0494374eb70a69ce2229`  
		Last Modified: Thu, 09 Oct 2025 22:21:08 GMT  
		Size: 362.7 KB (362682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30687b244cc914ab1a8ae574c29b80cfb7d1c51ffbf978065c7872711fe0512`  
		Last Modified: Thu, 09 Oct 2025 22:21:08 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292b4fa4c8d3eb0f4f13b4294e62df33588750da9560b319522a4e08a4060761`  
		Last Modified: Thu, 09 Oct 2025 22:21:10 GMT  
		Size: 28.1 MB (28051019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8b44c5b87cfe04949369004450a1bee5e45cd3d5a0345073182becc0c308b0`  
		Last Modified: Fri, 10 Oct 2025 05:32:13 GMT  
		Size: 785.6 MB (785644004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:45b2a4a40e18cf016a599f53b363b7fd3dbc8e749d77933a9f6130e3c8d2b8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baceb00dc4478e065e5d57e7603fe2fc5398bf38a16f3ce9de04b758040165a`

```dockerfile
```

-	Layers:
	-	`sha256:a99c85984285d9c066d5766ad1ed18ad54d0a0144d5b1fbc52e229e75dd87c66`  
		Last Modified: Fri, 10 Oct 2025 04:18:09 GMT  
		Size: 60.8 MB (60822377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73345984bf88af39e94d5390054ab4e53e5cdf8501f9e375b11101b63b404849`  
		Last Modified: Fri, 10 Oct 2025 04:18:11 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7d735971062021cf4d17d00aae8b17fffab1b6fc3730851b36918e1ebe808b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.9 MB (994859800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7093827230ea194acc0147e48c35015b8ecbbac4ada03693f43b0c565b1ae2ac`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f2e5bdb9ebc2dd1e4a97e4c4f8f6a4caa1a8d2b8c88779e314bfedf21b5eb`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431df98e5fde48f4218abb39181387c9329df717368142b9f365818c84a2731`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283f352fd757879170ef433d2bc7b2b87844a7e64a56c215fd7e8bcf52511b33`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcf903136d1425abdcfe45e487f28e07cfa1010e029bb0e9ea8ac6096c30939`  
		Last Modified: Thu, 09 Oct 2025 22:19:34 GMT  
		Size: 129.7 MB (129703599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680295d190e67764ff4359841a9d2f64ece12ca1088d22d70f40d69e908a05fc`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54999cd408b26d5a3591d807fe057f8f0496922b72c4ae057adb587b840f699`  
		Last Modified: Thu, 09 Oct 2025 22:21:32 GMT  
		Size: 105.6 MB (105594196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1813b12f5e0a79795a4d2d720c543dde8ed912e3a4265f5b9fa49285e11a6362`  
		Last Modified: Thu, 09 Oct 2025 22:21:26 GMT  
		Size: 362.7 KB (362687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b681a1245bedf2115e5b1ae357a6ae27fc654b24b46971ec2d199a75baa48ca5`  
		Last Modified: Thu, 09 Oct 2025 22:21:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437755691707c3c0f86472a9d675632fbcef51af972b17e23294315534f28aa6`  
		Last Modified: Thu, 09 Oct 2025 22:21:28 GMT  
		Size: 27.1 MB (27137484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625ccd079bb91aa531aa5f06c2384793e6ce719d62a54935099818729f67cc53`  
		Last Modified: Fri, 10 Oct 2025 09:02:17 GMT  
		Size: 695.7 MB (695658762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:fe8c9403f8df1db8e170269280631136aa14f6f0dba0666452d73bf17cfa607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7a7af5d9c7e7cc28f5178102d872a7cdf51e627e46cc06476d0c83a83141f2`

```dockerfile
```

-	Layers:
	-	`sha256:4f72b0bd41848fd9b57203b25b8ee26e3018d5fd2dac321da5f838cbdaadb0a7`  
		Last Modified: Fri, 10 Oct 2025 04:20:27 GMT  
		Size: 60.8 MB (60752902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b3753960dcfd1210c031f6eee993e09a85867e2af1988a1ebdfd491e222036`  
		Last Modified: Fri, 10 Oct 2025 04:20:28 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:2e20dcd2750bda5cba97df5f8383daae9797c45ad87cb0c017a13fb8d7c3447e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:361f2141aad13d7cc20ed77ef63af12c7d5c918c348a4bcb8ae5170a1d975e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1096476019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59f899e278fed1f76c2109d800beb593aa1c4563585b810ddc178c429f37fa2`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ad95cd04f77e0c5e96a8b537442f4b5d8be45febd447202f388d3a44663a30`  
		Last Modified: Thu, 09 Oct 2025 22:19:29 GMT  
		Size: 135.0 MB (134981480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b48f84fffbd5e61ea1d7e61e4143c8c98c1f4a0bff60b9411fd58aa4c63864`  
		Last Modified: Thu, 09 Oct 2025 21:25:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1dce87a7f4acd9c8a37db6070c5901c6b8b29cfcc2e7bde7ff0808cddffd70`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 110.2 MB (110185948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30531d5abaa989826e78461584cd1956e1f59a63a17a0494374eb70a69ce2229`  
		Last Modified: Thu, 09 Oct 2025 22:21:08 GMT  
		Size: 362.7 KB (362682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30687b244cc914ab1a8ae574c29b80cfb7d1c51ffbf978065c7872711fe0512`  
		Last Modified: Thu, 09 Oct 2025 22:21:08 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292b4fa4c8d3eb0f4f13b4294e62df33588750da9560b319522a4e08a4060761`  
		Last Modified: Thu, 09 Oct 2025 22:21:10 GMT  
		Size: 28.1 MB (28051019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8b44c5b87cfe04949369004450a1bee5e45cd3d5a0345073182becc0c308b0`  
		Last Modified: Fri, 10 Oct 2025 05:32:13 GMT  
		Size: 785.6 MB (785644004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:45b2a4a40e18cf016a599f53b363b7fd3dbc8e749d77933a9f6130e3c8d2b8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baceb00dc4478e065e5d57e7603fe2fc5398bf38a16f3ce9de04b758040165a`

```dockerfile
```

-	Layers:
	-	`sha256:a99c85984285d9c066d5766ad1ed18ad54d0a0144d5b1fbc52e229e75dd87c66`  
		Last Modified: Fri, 10 Oct 2025 04:18:09 GMT  
		Size: 60.8 MB (60822377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73345984bf88af39e94d5390054ab4e53e5cdf8501f9e375b11101b63b404849`  
		Last Modified: Fri, 10 Oct 2025 04:18:11 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7d735971062021cf4d17d00aae8b17fffab1b6fc3730851b36918e1ebe808b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.9 MB (994859800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7093827230ea194acc0147e48c35015b8ecbbac4ada03693f43b0c565b1ae2ac`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f2e5bdb9ebc2dd1e4a97e4c4f8f6a4caa1a8d2b8c88779e314bfedf21b5eb`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431df98e5fde48f4218abb39181387c9329df717368142b9f365818c84a2731`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283f352fd757879170ef433d2bc7b2b87844a7e64a56c215fd7e8bcf52511b33`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcf903136d1425abdcfe45e487f28e07cfa1010e029bb0e9ea8ac6096c30939`  
		Last Modified: Thu, 09 Oct 2025 22:19:34 GMT  
		Size: 129.7 MB (129703599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680295d190e67764ff4359841a9d2f64ece12ca1088d22d70f40d69e908a05fc`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54999cd408b26d5a3591d807fe057f8f0496922b72c4ae057adb587b840f699`  
		Last Modified: Thu, 09 Oct 2025 22:21:32 GMT  
		Size: 105.6 MB (105594196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1813b12f5e0a79795a4d2d720c543dde8ed912e3a4265f5b9fa49285e11a6362`  
		Last Modified: Thu, 09 Oct 2025 22:21:26 GMT  
		Size: 362.7 KB (362687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b681a1245bedf2115e5b1ae357a6ae27fc654b24b46971ec2d199a75baa48ca5`  
		Last Modified: Thu, 09 Oct 2025 22:21:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437755691707c3c0f86472a9d675632fbcef51af972b17e23294315534f28aa6`  
		Last Modified: Thu, 09 Oct 2025 22:21:28 GMT  
		Size: 27.1 MB (27137484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625ccd079bb91aa531aa5f06c2384793e6ce719d62a54935099818729f67cc53`  
		Last Modified: Fri, 10 Oct 2025 09:02:17 GMT  
		Size: 695.7 MB (695658762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fe8c9403f8df1db8e170269280631136aa14f6f0dba0666452d73bf17cfa607f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7a7af5d9c7e7cc28f5178102d872a7cdf51e627e46cc06476d0c83a83141f2`

```dockerfile
```

-	Layers:
	-	`sha256:4f72b0bd41848fd9b57203b25b8ee26e3018d5fd2dac321da5f838cbdaadb0a7`  
		Last Modified: Fri, 10 Oct 2025 04:20:27 GMT  
		Size: 60.8 MB (60752902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b3753960dcfd1210c031f6eee993e09a85867e2af1988a1ebdfd491e222036`  
		Last Modified: Fri, 10 Oct 2025 04:20:28 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:300c9505e7261fc80d1aa75c3b1b4beabad4223329ff9d9cd41f608f794df243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0cc6b0e7d3502ad36eeefc5143505caa15c34cc9f5ab554738732a25b0d917f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311030510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b55dbd0930b08c6f1b091089737b918a73cd9b17a8d0e6d2780cce35b15bf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:0c96703cc6405f14d42e6348a531553c713f4c179dda4974ad64c2f60aeafd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64817ffa8ae718817fbbf00fb0576b8bc53dff162855c53d975b2f3bbb98c32`

```dockerfile
```

-	Layers:
	-	`sha256:5709b9ba52bdf82559bb29618ebccf96f4b01358b316409e5f9d82a413f91448`  
		Last Modified: Fri, 14 Nov 2025 02:18:35 GMT  
		Size: 24.7 MB (24650335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7692c8f6f42bdae33ec2302b3a1c6c86524cf78aede683f6edfb91f5b09a8d75`  
		Last Modified: Fri, 14 Nov 2025 02:18:36 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfc7ec8e8eb439842ca4bcd2f56faa2d0d9b62accad6d220a0985288dc119db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299376599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1899ee8dff90370a8507bd0b1f9315f5203e2085e259642ff4e929efa5246cd4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d1f76759f0ac3ca705dcc4a37e8c233beb36ac6917e0bc2ef1eba4bcf07871e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a76dd5e9d7e6883d644c5b0b55de743605a2cf961ccac1deb7217ade910f6`

```dockerfile
```

-	Layers:
	-	`sha256:c9e538338867200639c593c1d6b3397b23eae1eddaea021ddeab641705c00a5d`  
		Last Modified: Fri, 14 Nov 2025 02:18:59 GMT  
		Size: 24.7 MB (24672596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91de0fa134b2151a75b51f9e4355bbf5e8746ee15d6a76f7bb13ef422a45bfb`  
		Last Modified: Fri, 14 Nov 2025 02:19:00 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:300c9505e7261fc80d1aa75c3b1b4beabad4223329ff9d9cd41f608f794df243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:0cc6b0e7d3502ad36eeefc5143505caa15c34cc9f5ab554738732a25b0d917f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311030510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b55dbd0930b08c6f1b091089737b918a73cd9b17a8d0e6d2780cce35b15bf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0c96703cc6405f14d42e6348a531553c713f4c179dda4974ad64c2f60aeafd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64817ffa8ae718817fbbf00fb0576b8bc53dff162855c53d975b2f3bbb98c32`

```dockerfile
```

-	Layers:
	-	`sha256:5709b9ba52bdf82559bb29618ebccf96f4b01358b316409e5f9d82a413f91448`  
		Last Modified: Fri, 14 Nov 2025 02:18:35 GMT  
		Size: 24.7 MB (24650335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7692c8f6f42bdae33ec2302b3a1c6c86524cf78aede683f6edfb91f5b09a8d75`  
		Last Modified: Fri, 14 Nov 2025 02:18:36 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfc7ec8e8eb439842ca4bcd2f56faa2d0d9b62accad6d220a0985288dc119db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299376599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1899ee8dff90370a8507bd0b1f9315f5203e2085e259642ff4e929efa5246cd4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d1f76759f0ac3ca705dcc4a37e8c233beb36ac6917e0bc2ef1eba4bcf07871e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a76dd5e9d7e6883d644c5b0b55de743605a2cf961ccac1deb7217ade910f6`

```dockerfile
```

-	Layers:
	-	`sha256:c9e538338867200639c593c1d6b3397b23eae1eddaea021ddeab641705c00a5d`  
		Last Modified: Fri, 14 Nov 2025 02:18:59 GMT  
		Size: 24.7 MB (24672596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91de0fa134b2151a75b51f9e4355bbf5e8746ee15d6a76f7bb13ef422a45bfb`  
		Last Modified: Fri, 14 Nov 2025 02:19:00 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:7221a3ace60bd89dcdbab43b4b1c0dc29ae4e00fb3ab89fd53cdfb5725cbdf5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:71dffd91d6e05f2e6fb45a8f7c50adcc2779d07a91595905ec03e5a810199301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172415875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11db19880322bbd67862dfc2668cc144ef548aad87cd147f492b537f99c1a71b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:d683b1784008e72cb46ee49f7aa1d28df7c5ef4d1b6dd66ff304a4b62851ee57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18414499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cb14a7e3cce46457f63428bed76fd754b0b6abfced533286faed0b625530fa`

```dockerfile
```

-	Layers:
	-	`sha256:e4985fd057570c468fc96bb62df258c03eab74a70dc3c1c4c9bb61c9031c5c57`  
		Last Modified: Fri, 14 Nov 2025 02:18:47 GMT  
		Size: 18.4 MB (18399890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9eb7602ba2f229898a075b0bb9ccb526ee341b72841cac812ee928dd4c276b`  
		Last Modified: Fri, 14 Nov 2025 02:18:48 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fc8363ba6068263da3fbe69ff00c316ac5ab301e59a29b22af32a39c6f6fcc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166270581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c070658d53fb2c816128f320b7611bd518d5c72fa0e1e202f7447826935b244`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:e77fe1c1ab6c85d180018fe72ed0ae259123b544157dd5fada0b6bf56dab92aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18388630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562cb007d439e1943b0dc24fb0a7f7cbd3b63be2f92b1420520b1965411c3055`

```dockerfile
```

-	Layers:
	-	`sha256:b1d52c2f0d04c47a47a556afa1e39562421798149d31731cf700f01b96548d1b`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 18.4 MB (18373896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1c6e57343393f4961be238044bd8bdb6d721666a95455baced9aeac752aad7`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:7221a3ace60bd89dcdbab43b4b1c0dc29ae4e00fb3ab89fd53cdfb5725cbdf5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:71dffd91d6e05f2e6fb45a8f7c50adcc2779d07a91595905ec03e5a810199301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172415875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11db19880322bbd67862dfc2668cc144ef548aad87cd147f492b537f99c1a71b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d683b1784008e72cb46ee49f7aa1d28df7c5ef4d1b6dd66ff304a4b62851ee57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18414499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cb14a7e3cce46457f63428bed76fd754b0b6abfced533286faed0b625530fa`

```dockerfile
```

-	Layers:
	-	`sha256:e4985fd057570c468fc96bb62df258c03eab74a70dc3c1c4c9bb61c9031c5c57`  
		Last Modified: Fri, 14 Nov 2025 02:18:47 GMT  
		Size: 18.4 MB (18399890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9eb7602ba2f229898a075b0bb9ccb526ee341b72841cac812ee928dd4c276b`  
		Last Modified: Fri, 14 Nov 2025 02:18:48 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fc8363ba6068263da3fbe69ff00c316ac5ab301e59a29b22af32a39c6f6fcc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166270581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c070658d53fb2c816128f320b7611bd518d5c72fa0e1e202f7447826935b244`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e77fe1c1ab6c85d180018fe72ed0ae259123b544157dd5fada0b6bf56dab92aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18388630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562cb007d439e1943b0dc24fb0a7f7cbd3b63be2f92b1420520b1965411c3055`

```dockerfile
```

-	Layers:
	-	`sha256:b1d52c2f0d04c47a47a556afa1e39562421798149d31731cf700f01b96548d1b`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 18.4 MB (18373896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1c6e57343393f4961be238044bd8bdb6d721666a95455baced9aeac752aad7`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:c5705f613a6427d07be6f3d0aba40068e16c3dea05604e1c95c63eac79fea658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:681694dce70804868341b866fce5f8f86582030365772ae9a5be108b0a05a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295937776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea524e20e2080c9aed93becdef12964c3d068b0fad0cee3fcfd10ba145d7f33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:9961876ad27e37456d0f6e52d4bbf09cf51839c9b7b4df64c33041aa746ce7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24560764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50e3e5912803cb2bdda7f03558c402c46d02e328783e95b380d496be344130b`

```dockerfile
```

-	Layers:
	-	`sha256:6ea56e3ff74d3e080e78e83a3aeaf07ea40b29f3ff6d947e9165f101d3bbd74f`  
		Last Modified: Fri, 14 Nov 2025 02:18:08 GMT  
		Size: 24.5 MB (24544143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e944a9cd91fcd09d96336d2a0eb56da13f45ec8f6388ddbda77a26fcc107f3f`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:462af74e10cf889815cf401917626987fe9007341fdeb79c7ab58dc7d41b4ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c2982ce015e6626d11b7fda013ffd30c09997fde2672ba464a03d23906dbce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:b8b43856e654d0fc72f295303ee53ae6d08e0e8dd7ed43713208d868bb089cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a63b0c075a33b8ab755fbc30142ba4034eded4448383f1115d2fec3dac282f`

```dockerfile
```

-	Layers:
	-	`sha256:757f2f8f7137b442bf37112c5b0e6e073805a55ce194e37e577a66c39a4390d4`  
		Last Modified: Fri, 14 Nov 2025 02:18:33 GMT  
		Size: 24.6 MB (24566416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f535be96aa6aebb0fc43577f12f4bd69d0c29b1fc7da9391df5a85f1400f7a2`  
		Last Modified: Fri, 14 Nov 2025 02:18:34 GMT  
		Size: 16.8 KB (16769 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:029b235468abbd489780a439ae35b739bd05a42edb5c5f10f3e1b3db30300f36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:f414f0f55ca18ecd31844deff5e7697d982790844e447b13a6450f6271592997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324675620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41af6baddc4abfe59e2d6f0cf880a9a9b36c18d8411d5ee7164aafada8498f01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:66ddeffd7daf51f32eabea4b4f291a53e86fc95d72aa6df4af2dd0ca9a76ed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25740803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03df47cab50819f0c219786a9e845ce6ac771bb36997070a09d31f320b6e5b60`

```dockerfile
```

-	Layers:
	-	`sha256:71c54244bdb403b3d6b44098fafb232e6f53cbbb40ade9e8486caab58fa02dc0`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 25.7 MB (25724438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c9352a53a21487108f4767012a0672567fca97fed315ee748096c737db26b`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28fd4ade8c7eeceef74187f01cf26800f5d7c67ff22f62fa27a16b65746aaf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312650455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf90b6fa04814069b7cc74317cdd9f3421e7b712843f32141043c5a76571cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:fb6bccc15b557ab67edb1d332e3a80ade8893c2865d1fc4f5c4bceb31e487a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25763398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41117bc44e3f37051e031a19cc2981fd6dc98b44d7b0a5d736009df486bc0eb`

```dockerfile
```

-	Layers:
	-	`sha256:e94a7abd29f5ed0717d069409d1949ec6ce56cee5dea8dbc3aca8199a0894a25`  
		Last Modified: Fri, 14 Nov 2025 02:19:27 GMT  
		Size: 25.7 MB (25746896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6bfa8cb739cd81e1891288b2e14a5ec0f76cc16c406310bc7fc5d4f551b125`  
		Last Modified: Fri, 14 Nov 2025 02:19:28 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:6548f34d9b39dac04cd04d12091e02f85f4dd1f0281eaeb719a5554ec1022251
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:215ef5e5b3accb594a01e94ee587fb34cb66802f977d5d676fda596c30237d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1110232556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac03b00087ddd7f4c21dae6bf46a990f5c67e408ee0c07c2b2efe614e06a50e`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2081cac45e5fb7bc52c7bf496d2ccc3433f84dd8702adc9fa84d467cc2be5543`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fb1361c757ec00d31a8c6c88058fd62b23da12af4290edf2d3b2c636f6da5a`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 6.7 MB (6746865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4540fb962b4d5de83708d3245134aac24f8adcb8d8457e317648dfe877db60`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 94.1 KB (94146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebe16a8832263871186c0dda7eaada9cdcfd4f1a4bcc90feccdb47acfff940`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 148.8 MB (148814487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda935e56c9a4a7f7f77e60fc31b89aa8dc68da689983df8cab450bf7bace1b`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31523257a1ece06c9814d06f6f4500a1508b114157f084262f1375ac4b301c`  
		Last Modified: Thu, 09 Oct 2025 22:21:38 GMT  
		Size: 110.2 MB (110186408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0540c997b5b21d64ae334358cb01b6ad38b6e430b4932715c3df365b46e62dd`  
		Last Modified: Thu, 09 Oct 2025 22:21:21 GMT  
		Size: 355.9 KB (355919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a89c2b76c491ee8a948ecad02d5f072b7c91d6cb9aa7b9250b70807a74c3e4`  
		Last Modified: Thu, 09 Oct 2025 22:21:21 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdbe5600458c88310171992d7be5d531219154f5349a6bfa4c66e1ee540b97b`  
		Last Modified: Thu, 09 Oct 2025 22:21:25 GMT  
		Size: 28.0 MB (28041410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8594db11d287c122a10d408292f761579200651cd578e9c20f7ebf936734a7`  
		Last Modified: Fri, 10 Oct 2025 04:51:16 GMT  
		Size: 785.6 MB (785583591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:cd6ec8a0c1119ad1bce40c64dbfec64d157ef2779651a19d937ac7acf3555f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61765049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d00bb02cf403da5418ea96608d6770c672f6aa6e7038b2bb43410ad240704d`

```dockerfile
```

-	Layers:
	-	`sha256:fda67f5e7fde0a586b368a251d7a4081baf87691c6b5725970be737450147efa`  
		Last Modified: Fri, 10 Oct 2025 04:18:27 GMT  
		Size: 61.8 MB (61755647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27bc81a73dfc4ddbdd5ddc5f962c4d2516bf656d333d0a5a06ef6341207e2dd6`  
		Last Modified: Fri, 10 Oct 2025 04:18:28 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f25d409da9b57a9c6c510bfb3a1b7b396ca4ee15abeafa6bbf22243b4aa2a660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1008163589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8583103026b5f948a98467fddbc131b7471ccf2a9bca728c9f240bc6a33818`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14560a455baad8eacfe612b059e56e9c5ca08dec61a49e2ca1d556759a08beea`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 143.1 MB (143142590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9bd3503415fa5eb2be4bb24bbf854e74951b39a17b36da6a34665776ee9ce`  
		Last Modified: Thu, 09 Oct 2025 22:19:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e0cb3cad29da748fe594c88a3719b3d1430a411f3ae08a0f829caf26716bb0`  
		Last Modified: Thu, 09 Oct 2025 22:21:27 GMT  
		Size: 105.6 MB (105594578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485768f0ebc63a01498da99077e40e13951c1e733cd5250949c230159dc378c`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 355.9 KB (355911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331a5c34e96c531bfd92ba0076334a10f4831f68cb6ee87753ed4a5bd786bba`  
		Last Modified: Thu, 09 Oct 2025 22:21:18 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a428a6dab2527ff03838d1a6e14d7e2f3e3f28e30e4d2c03d172c7f4d93581b`  
		Last Modified: Thu, 09 Oct 2025 22:21:20 GMT  
		Size: 27.1 MB (27123310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd1451456cfa7c64dcc43098258983ccf79a8b3d3cdc9a946f8ee7b185a3c2`  
		Last Modified: Fri, 10 Oct 2025 03:41:12 GMT  
		Size: 695.5 MB (695544074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:99ef217b63bceeb3d18584a119dffc889b3324979c93711fb6a518a0e44772e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61695850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772c6806ff746065396d27d8fc0099582f1d45add28de7c0cf0136bd61faee26`

```dockerfile
```

-	Layers:
	-	`sha256:d44a13c140c1f7488f8bd99896bcb99ebaaae2c4013d074cb8e643333a112444`  
		Last Modified: Fri, 10 Oct 2025 04:20:47 GMT  
		Size: 61.7 MB (61686369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1362d753974736423c980e4154c0df006042bd4477b4ef31c5ccc808a635e9f`  
		Last Modified: Fri, 10 Oct 2025 04:20:48 GMT  
		Size: 9.5 KB (9481 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:6548f34d9b39dac04cd04d12091e02f85f4dd1f0281eaeb719a5554ec1022251
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:215ef5e5b3accb594a01e94ee587fb34cb66802f977d5d676fda596c30237d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1110232556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac03b00087ddd7f4c21dae6bf46a990f5c67e408ee0c07c2b2efe614e06a50e`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2081cac45e5fb7bc52c7bf496d2ccc3433f84dd8702adc9fa84d467cc2be5543`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fb1361c757ec00d31a8c6c88058fd62b23da12af4290edf2d3b2c636f6da5a`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 6.7 MB (6746865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4540fb962b4d5de83708d3245134aac24f8adcb8d8457e317648dfe877db60`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 94.1 KB (94146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebe16a8832263871186c0dda7eaada9cdcfd4f1a4bcc90feccdb47acfff940`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 148.8 MB (148814487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda935e56c9a4a7f7f77e60fc31b89aa8dc68da689983df8cab450bf7bace1b`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31523257a1ece06c9814d06f6f4500a1508b114157f084262f1375ac4b301c`  
		Last Modified: Thu, 09 Oct 2025 22:21:38 GMT  
		Size: 110.2 MB (110186408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0540c997b5b21d64ae334358cb01b6ad38b6e430b4932715c3df365b46e62dd`  
		Last Modified: Thu, 09 Oct 2025 22:21:21 GMT  
		Size: 355.9 KB (355919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a89c2b76c491ee8a948ecad02d5f072b7c91d6cb9aa7b9250b70807a74c3e4`  
		Last Modified: Thu, 09 Oct 2025 22:21:21 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdbe5600458c88310171992d7be5d531219154f5349a6bfa4c66e1ee540b97b`  
		Last Modified: Thu, 09 Oct 2025 22:21:25 GMT  
		Size: 28.0 MB (28041410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8594db11d287c122a10d408292f761579200651cd578e9c20f7ebf936734a7`  
		Last Modified: Fri, 10 Oct 2025 04:51:16 GMT  
		Size: 785.6 MB (785583591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:cd6ec8a0c1119ad1bce40c64dbfec64d157ef2779651a19d937ac7acf3555f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61765049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d00bb02cf403da5418ea96608d6770c672f6aa6e7038b2bb43410ad240704d`

```dockerfile
```

-	Layers:
	-	`sha256:fda67f5e7fde0a586b368a251d7a4081baf87691c6b5725970be737450147efa`  
		Last Modified: Fri, 10 Oct 2025 04:18:27 GMT  
		Size: 61.8 MB (61755647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27bc81a73dfc4ddbdd5ddc5f962c4d2516bf656d333d0a5a06ef6341207e2dd6`  
		Last Modified: Fri, 10 Oct 2025 04:18:28 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f25d409da9b57a9c6c510bfb3a1b7b396ca4ee15abeafa6bbf22243b4aa2a660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1008163589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8583103026b5f948a98467fddbc131b7471ccf2a9bca728c9f240bc6a33818`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14560a455baad8eacfe612b059e56e9c5ca08dec61a49e2ca1d556759a08beea`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 143.1 MB (143142590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9bd3503415fa5eb2be4bb24bbf854e74951b39a17b36da6a34665776ee9ce`  
		Last Modified: Thu, 09 Oct 2025 22:19:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e0cb3cad29da748fe594c88a3719b3d1430a411f3ae08a0f829caf26716bb0`  
		Last Modified: Thu, 09 Oct 2025 22:21:27 GMT  
		Size: 105.6 MB (105594578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485768f0ebc63a01498da99077e40e13951c1e733cd5250949c230159dc378c`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 355.9 KB (355911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331a5c34e96c531bfd92ba0076334a10f4831f68cb6ee87753ed4a5bd786bba`  
		Last Modified: Thu, 09 Oct 2025 22:21:18 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a428a6dab2527ff03838d1a6e14d7e2f3e3f28e30e4d2c03d172c7f4d93581b`  
		Last Modified: Thu, 09 Oct 2025 22:21:20 GMT  
		Size: 27.1 MB (27123310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd1451456cfa7c64dcc43098258983ccf79a8b3d3cdc9a946f8ee7b185a3c2`  
		Last Modified: Fri, 10 Oct 2025 03:41:12 GMT  
		Size: 695.5 MB (695544074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:99ef217b63bceeb3d18584a119dffc889b3324979c93711fb6a518a0e44772e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61695850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772c6806ff746065396d27d8fc0099582f1d45add28de7c0cf0136bd61faee26`

```dockerfile
```

-	Layers:
	-	`sha256:d44a13c140c1f7488f8bd99896bcb99ebaaae2c4013d074cb8e643333a112444`  
		Last Modified: Fri, 10 Oct 2025 04:20:47 GMT  
		Size: 61.7 MB (61686369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1362d753974736423c980e4154c0df006042bd4477b4ef31c5ccc808a635e9f`  
		Last Modified: Fri, 10 Oct 2025 04:20:48 GMT  
		Size: 9.5 KB (9481 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:029b235468abbd489780a439ae35b739bd05a42edb5c5f10f3e1b3db30300f36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:f414f0f55ca18ecd31844deff5e7697d982790844e447b13a6450f6271592997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324675620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41af6baddc4abfe59e2d6f0cf880a9a9b36c18d8411d5ee7164aafada8498f01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:66ddeffd7daf51f32eabea4b4f291a53e86fc95d72aa6df4af2dd0ca9a76ed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25740803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03df47cab50819f0c219786a9e845ce6ac771bb36997070a09d31f320b6e5b60`

```dockerfile
```

-	Layers:
	-	`sha256:71c54244bdb403b3d6b44098fafb232e6f53cbbb40ade9e8486caab58fa02dc0`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 25.7 MB (25724438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c9352a53a21487108f4767012a0672567fca97fed315ee748096c737db26b`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28fd4ade8c7eeceef74187f01cf26800f5d7c67ff22f62fa27a16b65746aaf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312650455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf90b6fa04814069b7cc74317cdd9f3421e7b712843f32141043c5a76571cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fb6bccc15b557ab67edb1d332e3a80ade8893c2865d1fc4f5c4bceb31e487a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25763398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41117bc44e3f37051e031a19cc2981fd6dc98b44d7b0a5d736009df486bc0eb`

```dockerfile
```

-	Layers:
	-	`sha256:e94a7abd29f5ed0717d069409d1949ec6ce56cee5dea8dbc3aca8199a0894a25`  
		Last Modified: Fri, 14 Nov 2025 02:19:27 GMT  
		Size: 25.7 MB (25746896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6bfa8cb739cd81e1891288b2e14a5ec0f76cc16c406310bc7fc5d4f551b125`  
		Last Modified: Fri, 14 Nov 2025 02:19:28 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:029b235468abbd489780a439ae35b739bd05a42edb5c5f10f3e1b3db30300f36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:f414f0f55ca18ecd31844deff5e7697d982790844e447b13a6450f6271592997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324675620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41af6baddc4abfe59e2d6f0cf880a9a9b36c18d8411d5ee7164aafada8498f01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ce9f7a316883bfc98e61ca8daa6375c6da50cafdfa85179993462ccdd487b`  
		Last Modified: Fri, 14 Nov 2025 00:36:58 GMT  
		Size: 110.2 MB (110187245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd5e5070fd29a8c753b2de8d407a4abde0375c9b87f0e6d79b5eaac109ec7`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 360.6 KB (360566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecebcb6d8e697b2f3a67cae5173e1720c301480051226726d5e49cd344bcac`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eebc0c9343354909e51a450637213bc65cd5c91d45e429df1276e62c143dee5`  
		Last Modified: Fri, 14 Nov 2025 00:36:51 GMT  
		Size: 27.8 MB (27802204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:66ddeffd7daf51f32eabea4b4f291a53e86fc95d72aa6df4af2dd0ca9a76ed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25740803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03df47cab50819f0c219786a9e845ce6ac771bb36997070a09d31f320b6e5b60`

```dockerfile
```

-	Layers:
	-	`sha256:71c54244bdb403b3d6b44098fafb232e6f53cbbb40ade9e8486caab58fa02dc0`  
		Last Modified: Fri, 14 Nov 2025 02:19:02 GMT  
		Size: 25.7 MB (25724438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74c9352a53a21487108f4767012a0672567fca97fed315ee748096c737db26b`  
		Last Modified: Fri, 14 Nov 2025 02:19:03 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28fd4ade8c7eeceef74187f01cf26800f5d7c67ff22f62fa27a16b65746aaf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312650455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf90b6fa04814069b7cc74317cdd9f3421e7b712843f32141043c5a76571cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6091bd1596cc9c94b3cf84cb131436ea38de25e0618787e197518ed2db80f`  
		Last Modified: Fri, 14 Nov 2025 00:37:41 GMT  
		Size: 105.6 MB (105596555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3a9ff141db5b9d69a0e41e760ca068e881815f7be18d25824ea2a0c1818f3`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 360.6 KB (360561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cd29b3de7a5c35ea79ca53c67b77daf2a0dca29a89e827bb0eec950d914d2`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b2ee5e669e6632fe1d194fc920793372c6aeeedd6313ee11622b66897930c`  
		Last Modified: Fri, 14 Nov 2025 00:37:37 GMT  
		Size: 26.9 MB (26891440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:fb6bccc15b557ab67edb1d332e3a80ade8893c2865d1fc4f5c4bceb31e487a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25763398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41117bc44e3f37051e031a19cc2981fd6dc98b44d7b0a5d736009df486bc0eb`

```dockerfile
```

-	Layers:
	-	`sha256:e94a7abd29f5ed0717d069409d1949ec6ce56cee5dea8dbc3aca8199a0894a25`  
		Last Modified: Fri, 14 Nov 2025 02:19:27 GMT  
		Size: 25.7 MB (25746896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6bfa8cb739cd81e1891288b2e14a5ec0f76cc16c406310bc7fc5d4f551b125`  
		Last Modified: Fri, 14 Nov 2025 02:19:28 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:93b84a38701fceb5d2b3bb1af7c5e63f8c7106f97334988ebf3244751202214a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:060cbce5038073f7d5a63629be758b379639ab8ace7e068c5b210e41185b7ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186323097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0ba5853c1c34d18315354e9621dd98fa71117cd372d3f383518a4158523450`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ebc496359d848b519a2da908b7e10b3f4e11e9c830bbc698ed802bb0113e5f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19490117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aadcd78feaae35a9e17bd1fe13b7fe468a146a513dfbaafb127910cd7db7ff3`

```dockerfile
```

-	Layers:
	-	`sha256:250c3cc3dad4910e142f62d5761d9543093cb4dc804858bd1066deca41ca6719`  
		Last Modified: Fri, 14 Nov 2025 02:19:13 GMT  
		Size: 19.5 MB (19475496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6393b8b9aac1f57c4a22cbbabae5a9bdfe54987e996408957e2be50cdab1aa`  
		Last Modified: Fri, 14 Nov 2025 02:19:14 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3460929d04dcdb8665ce9145d51cc2a63fbd6aa6db4fe992a62371260a7e3296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179799404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ea179f9f5087f290e587f9d4208ccbdd6380c75efe8473f697716b52c26d4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:dde8b3acc1adbc96d591369682c585f9deafa73dd52bcd5903ec7fa80bae38c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19464446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d86f9d7077bae3423cb51daf8d9fe4b8740853d101a14a625907c0813a7dc47`

```dockerfile
```

-	Layers:
	-	`sha256:d3acc2ae7593ba1acb6e43436377a32994a41c71db40800d21fc59107a451ddc`  
		Last Modified: Fri, 14 Nov 2025 02:19:30 GMT  
		Size: 19.4 MB (19449700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed016523c0ff6ea390cde8313cc9344362a8235fd5fc0f4520262916d62dd716`  
		Last Modified: Fri, 14 Nov 2025 02:19:31 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:93b84a38701fceb5d2b3bb1af7c5e63f8c7106f97334988ebf3244751202214a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:060cbce5038073f7d5a63629be758b379639ab8ace7e068c5b210e41185b7ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186323097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0ba5853c1c34d18315354e9621dd98fa71117cd372d3f383518a4158523450`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:41 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e859821e0442ece0b7c9f42ee8bcdfdad70f04374296a0341f99d1b376c5fa0`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 683.9 KB (683916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5287ecfab6903c1f04dc7eb19db93c17deaeea31b96bef58d717b45f2c1f381`  
		Last Modified: Thu, 13 Nov 2025 23:38:23 GMT  
		Size: 6.7 MB (6747192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1391505c3b5afdfe5141ea504ca465b721466073e736110bbae8d00f5277076`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 94.1 KB (94107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b150d605cbf49762e7160bf96073e12929d3fd3225eaee62cfa1277c65c988`  
		Last Modified: Fri, 14 Nov 2025 00:35:10 GMT  
		Size: 149.1 MB (149072998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711191b04df06da29609c7f663aca5b507baf432896470fb9544ddc7f887c1c8`  
		Last Modified: Thu, 13 Nov 2025 23:38:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ebc496359d848b519a2da908b7e10b3f4e11e9c830bbc698ed802bb0113e5f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19490117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aadcd78feaae35a9e17bd1fe13b7fe468a146a513dfbaafb127910cd7db7ff3`

```dockerfile
```

-	Layers:
	-	`sha256:250c3cc3dad4910e142f62d5761d9543093cb4dc804858bd1066deca41ca6719`  
		Last Modified: Fri, 14 Nov 2025 02:19:13 GMT  
		Size: 19.5 MB (19475496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6393b8b9aac1f57c4a22cbbabae5a9bdfe54987e996408957e2be50cdab1aa`  
		Last Modified: Fri, 14 Nov 2025 02:19:14 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3460929d04dcdb8665ce9145d51cc2a63fbd6aa6db4fe992a62371260a7e3296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179799404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ea179f9f5087f290e587f9d4208ccbdd6380c75efe8473f697716b52c26d4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:24 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 13 Nov 2025 23:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a2cea4c13e33edea2b72ed3f9d4748ba6dc241cee0acd04c241e80435bc823`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 684.0 KB (684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc69d87f518d8d7ac1084d666faf5003052bd6348dfeb6767064dd5c8442de`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 6.8 MB (6759913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8b3301cd177c6ecf92c07deffe541461e7bc3543f8757723651628c28cf02`  
		Last Modified: Thu, 13 Nov 2025 23:37:54 GMT  
		Size: 94.2 KB (94204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a3e81481b556e57eef37b150639372f8d46f43b27b5097e8d669ff949ebff`  
		Last Modified: Fri, 14 Nov 2025 00:35:58 GMT  
		Size: 143.4 MB (143399101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f535c7019fbee286fb2b8dc53062e4d553b2a26164163daa0eed14cea9867155`  
		Last Modified: Thu, 13 Nov 2025 23:37:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:dde8b3acc1adbc96d591369682c585f9deafa73dd52bcd5903ec7fa80bae38c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19464446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d86f9d7077bae3423cb51daf8d9fe4b8740853d101a14a625907c0813a7dc47`

```dockerfile
```

-	Layers:
	-	`sha256:d3acc2ae7593ba1acb6e43436377a32994a41c71db40800d21fc59107a451ddc`  
		Last Modified: Fri, 14 Nov 2025 02:19:30 GMT  
		Size: 19.4 MB (19449700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed016523c0ff6ea390cde8313cc9344362a8235fd5fc0f4520262916d62dd716`  
		Last Modified: Fri, 14 Nov 2025 02:19:31 GMT  
		Size: 14.7 KB (14746 bytes)  
		MIME: application/vnd.in-toto+json
