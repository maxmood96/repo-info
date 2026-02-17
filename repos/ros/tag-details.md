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
$ docker pull ros@sha256:cea207ed28df70fea9cab9592c2b20f6c06222d791255e69c25ee354a003342f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:1914338e20c182141127ffaf36c2a03e40bdc46c216d6456948ff1b675da8aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.4 MB (263415656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540512ac34685e3151c0b4661759a6aa7674c5cc9a6eca80d9767ca40f65f8c9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dec43e28aad1e2cadf4a3049124373963669e4bdc95a2f75e1dd63b3eb7d4`  
		Last Modified: Tue, 17 Feb 2026 21:30:25 GMT  
		Size: 98.2 MB (98162262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf5f7cd1537f5913a85f2ebc069c9789e846bf183dff3a228255ff5cec83d5a`  
		Last Modified: Tue, 17 Feb 2026 21:30:23 GMT  
		Size: 385.7 KB (385692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b69186bf79733d3d6b81c46636fc779e193368bc38db8d3010b68876160cf`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b561868aa7cf7cf04f054a78bd8ea5432a5e5b7616b392f06e30288df496aa06`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.3 MB (23319467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:7a75a5ae722252a8b9844767c6828297b368778a3d70f5504816b7936ca22f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23718026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e88a01f236f2b24fab803387d5f7842537aaa1a1140ffacfa63bdcf5706465`

```dockerfile
```

-	Layers:
	-	`sha256:dc112df1880481e7f97de632618f78f61eb0824afa6205a5a82fbd38878a690a`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.7 MB (23701678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dacecb9f66ba8430cfc5d96bd5a474cdb22ea3a9ba10e6502dc3755a688a6d5`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a71d46b79687b6e952bf21946f8452356aed0e784aa795453c3f9ad831a77b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255978994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4492640c45a0ed6d9d1577ab9c9422eef298d6fe6ad7c5c5ad7baeb45987235`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62216dc13167a74c4b0ea4bceed53adbd12ca59082f9d7d140072fb8303cd3b`  
		Last Modified: Tue, 17 Feb 2026 21:30:43 GMT  
		Size: 95.8 MB (95763594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6985ab4c77e34b80ea8654dbbb36877bb046b39b4e1a89152bff01ec65ae27`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 385.7 KB (385698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2fc45c9db8d6efebbc61a4596bd898b8b84cdbaf4216b4d244de614b5ee3ac`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb3a087f98a0a2ce287e3d474cd5e6ecbbd623963b6f262dd73d5a9f42535c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 22.7 MB (22718722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:e67eca9f579cf443798f93d494f53a37a344e8402945008184215fd239b80173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23731180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b35429dbe94352de3fa3f88e6dc303fed6f8b1ecaac42e9dc736cff388cc50`

```dockerfile
```

-	Layers:
	-	`sha256:c45162ec875974250027133fdb54d13f0e2c46a6440488ef436a7f1202dc417c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 23.7 MB (23714695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efac263ab6565b1d35ef93b62b1b9d3966086fba0a87be6a3769e04eaa6614b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:edd733188896f30860e4966f4ba48d68e55d65ffe5e62dab35d0eeaac8c39efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:acc676afebf4c38d34613a768a80e7d9d8eeaa95b630941fef6017a42578ffde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.5 MB (955538683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d23f1ac705fc4ce44aa854383ae0a7e4938c6d8561dce4a2463a93c94621c13`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dec43e28aad1e2cadf4a3049124373963669e4bdc95a2f75e1dd63b3eb7d4`  
		Last Modified: Tue, 17 Feb 2026 21:30:25 GMT  
		Size: 98.2 MB (98162262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf5f7cd1537f5913a85f2ebc069c9789e846bf183dff3a228255ff5cec83d5a`  
		Last Modified: Tue, 17 Feb 2026 21:30:23 GMT  
		Size: 385.7 KB (385692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b69186bf79733d3d6b81c46636fc779e193368bc38db8d3010b68876160cf`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b561868aa7cf7cf04f054a78bd8ea5432a5e5b7616b392f06e30288df496aa06`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.3 MB (23319467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52268b348904e592ff59e382a161ba93be4dcf836eeafd72c2fa2eaefca6875d`  
		Last Modified: Tue, 17 Feb 2026 21:55:49 GMT  
		Size: 692.1 MB (692123027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e0a3cd1ef3e3f6c71a907a215162c9a85cb84043b07346121859d68ab5fb0c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58802694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105395e78b3d50c31660fd5e1e322b86bc381eefdb239cc3e6ed1989c9ef864a`

```dockerfile
```

-	Layers:
	-	`sha256:01144e078e7cfbc4e9b270382e49fd1f529360038ca5b2eb3613a562e78e90c8`  
		Last Modified: Tue, 17 Feb 2026 21:55:38 GMT  
		Size: 58.8 MB (58793342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71659aa8898127d013ed917a80317dee93c31f9b49503d3a4aba353c74325445`  
		Last Modified: Tue, 17 Feb 2026 21:55:36 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:26e5c42bc916f2c77c59cb38b7c4eb071b92b0a8c65ea6f19691395c299dcdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.0 MB (916045816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741ffae9aa3b34a9e1897ff16652f273bc5798684f8a2d50bb2a45e474ba438d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62216dc13167a74c4b0ea4bceed53adbd12ca59082f9d7d140072fb8303cd3b`  
		Last Modified: Tue, 17 Feb 2026 21:30:43 GMT  
		Size: 95.8 MB (95763594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6985ab4c77e34b80ea8654dbbb36877bb046b39b4e1a89152bff01ec65ae27`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 385.7 KB (385698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2fc45c9db8d6efebbc61a4596bd898b8b84cdbaf4216b4d244de614b5ee3ac`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb3a087f98a0a2ce287e3d474cd5e6ecbbd623963b6f262dd73d5a9f42535c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 22.7 MB (22718722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9099d6f311b19a3abce597dce855a2e4c38498c822ceec77e2e8b8a71fa549`  
		Last Modified: Tue, 17 Feb 2026 21:55:28 GMT  
		Size: 660.1 MB (660066822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:2fa18ac5330e35d1f327a4a0b9565b3774bf97747180760166cd6311213f288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58787095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bab72dea5017b9b3ec1c40fcc1396d3be8271ef37b96e79b33e40cf25006f43`

```dockerfile
```

-	Layers:
	-	`sha256:c036016afe5c3d4f431675ce726bdd329e56f1de8c8efa07bdf97fd2851e2f77`  
		Last Modified: Tue, 17 Feb 2026 21:55:17 GMT  
		Size: 58.8 MB (58777663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30ae5ac2a1bd3937b560515b5a80ce477a27a9b9adbb8a371cee4f2b5783944`  
		Last Modified: Tue, 17 Feb 2026 21:55:14 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:edd733188896f30860e4966f4ba48d68e55d65ffe5e62dab35d0eeaac8c39efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:acc676afebf4c38d34613a768a80e7d9d8eeaa95b630941fef6017a42578ffde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.5 MB (955538683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d23f1ac705fc4ce44aa854383ae0a7e4938c6d8561dce4a2463a93c94621c13`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dec43e28aad1e2cadf4a3049124373963669e4bdc95a2f75e1dd63b3eb7d4`  
		Last Modified: Tue, 17 Feb 2026 21:30:25 GMT  
		Size: 98.2 MB (98162262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf5f7cd1537f5913a85f2ebc069c9789e846bf183dff3a228255ff5cec83d5a`  
		Last Modified: Tue, 17 Feb 2026 21:30:23 GMT  
		Size: 385.7 KB (385692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b69186bf79733d3d6b81c46636fc779e193368bc38db8d3010b68876160cf`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b561868aa7cf7cf04f054a78bd8ea5432a5e5b7616b392f06e30288df496aa06`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.3 MB (23319467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52268b348904e592ff59e382a161ba93be4dcf836eeafd72c2fa2eaefca6875d`  
		Last Modified: Tue, 17 Feb 2026 21:55:49 GMT  
		Size: 692.1 MB (692123027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e0a3cd1ef3e3f6c71a907a215162c9a85cb84043b07346121859d68ab5fb0c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58802694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105395e78b3d50c31660fd5e1e322b86bc381eefdb239cc3e6ed1989c9ef864a`

```dockerfile
```

-	Layers:
	-	`sha256:01144e078e7cfbc4e9b270382e49fd1f529360038ca5b2eb3613a562e78e90c8`  
		Last Modified: Tue, 17 Feb 2026 21:55:38 GMT  
		Size: 58.8 MB (58793342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71659aa8898127d013ed917a80317dee93c31f9b49503d3a4aba353c74325445`  
		Last Modified: Tue, 17 Feb 2026 21:55:36 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:26e5c42bc916f2c77c59cb38b7c4eb071b92b0a8c65ea6f19691395c299dcdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.0 MB (916045816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741ffae9aa3b34a9e1897ff16652f273bc5798684f8a2d50bb2a45e474ba438d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62216dc13167a74c4b0ea4bceed53adbd12ca59082f9d7d140072fb8303cd3b`  
		Last Modified: Tue, 17 Feb 2026 21:30:43 GMT  
		Size: 95.8 MB (95763594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6985ab4c77e34b80ea8654dbbb36877bb046b39b4e1a89152bff01ec65ae27`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 385.7 KB (385698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2fc45c9db8d6efebbc61a4596bd898b8b84cdbaf4216b4d244de614b5ee3ac`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb3a087f98a0a2ce287e3d474cd5e6ecbbd623963b6f262dd73d5a9f42535c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 22.7 MB (22718722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9099d6f311b19a3abce597dce855a2e4c38498c822ceec77e2e8b8a71fa549`  
		Last Modified: Tue, 17 Feb 2026 21:55:28 GMT  
		Size: 660.1 MB (660066822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:2fa18ac5330e35d1f327a4a0b9565b3774bf97747180760166cd6311213f288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58787095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bab72dea5017b9b3ec1c40fcc1396d3be8271ef37b96e79b33e40cf25006f43`

```dockerfile
```

-	Layers:
	-	`sha256:c036016afe5c3d4f431675ce726bdd329e56f1de8c8efa07bdf97fd2851e2f77`  
		Last Modified: Tue, 17 Feb 2026 21:55:17 GMT  
		Size: 58.8 MB (58777663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30ae5ac2a1bd3937b560515b5a80ce477a27a9b9adbb8a371cee4f2b5783944`  
		Last Modified: Tue, 17 Feb 2026 21:55:14 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:cea207ed28df70fea9cab9592c2b20f6c06222d791255e69c25ee354a003342f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1914338e20c182141127ffaf36c2a03e40bdc46c216d6456948ff1b675da8aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.4 MB (263415656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540512ac34685e3151c0b4661759a6aa7674c5cc9a6eca80d9767ca40f65f8c9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dec43e28aad1e2cadf4a3049124373963669e4bdc95a2f75e1dd63b3eb7d4`  
		Last Modified: Tue, 17 Feb 2026 21:30:25 GMT  
		Size: 98.2 MB (98162262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf5f7cd1537f5913a85f2ebc069c9789e846bf183dff3a228255ff5cec83d5a`  
		Last Modified: Tue, 17 Feb 2026 21:30:23 GMT  
		Size: 385.7 KB (385692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b69186bf79733d3d6b81c46636fc779e193368bc38db8d3010b68876160cf`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b561868aa7cf7cf04f054a78bd8ea5432a5e5b7616b392f06e30288df496aa06`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.3 MB (23319467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:7a75a5ae722252a8b9844767c6828297b368778a3d70f5504816b7936ca22f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23718026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e88a01f236f2b24fab803387d5f7842537aaa1a1140ffacfa63bdcf5706465`

```dockerfile
```

-	Layers:
	-	`sha256:dc112df1880481e7f97de632618f78f61eb0824afa6205a5a82fbd38878a690a`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.7 MB (23701678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dacecb9f66ba8430cfc5d96bd5a474cdb22ea3a9ba10e6502dc3755a688a6d5`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a71d46b79687b6e952bf21946f8452356aed0e784aa795453c3f9ad831a77b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255978994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4492640c45a0ed6d9d1577ab9c9422eef298d6fe6ad7c5c5ad7baeb45987235`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62216dc13167a74c4b0ea4bceed53adbd12ca59082f9d7d140072fb8303cd3b`  
		Last Modified: Tue, 17 Feb 2026 21:30:43 GMT  
		Size: 95.8 MB (95763594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6985ab4c77e34b80ea8654dbbb36877bb046b39b4e1a89152bff01ec65ae27`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 385.7 KB (385698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2fc45c9db8d6efebbc61a4596bd898b8b84cdbaf4216b4d244de614b5ee3ac`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb3a087f98a0a2ce287e3d474cd5e6ecbbd623963b6f262dd73d5a9f42535c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 22.7 MB (22718722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:e67eca9f579cf443798f93d494f53a37a344e8402945008184215fd239b80173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23731180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b35429dbe94352de3fa3f88e6dc303fed6f8b1ecaac42e9dc736cff388cc50`

```dockerfile
```

-	Layers:
	-	`sha256:c45162ec875974250027133fdb54d13f0e2c46a6440488ef436a7f1202dc417c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 23.7 MB (23714695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efac263ab6565b1d35ef93b62b1b9d3966086fba0a87be6a3769e04eaa6614b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:cea207ed28df70fea9cab9592c2b20f6c06222d791255e69c25ee354a003342f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1914338e20c182141127ffaf36c2a03e40bdc46c216d6456948ff1b675da8aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.4 MB (263415656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540512ac34685e3151c0b4661759a6aa7674c5cc9a6eca80d9767ca40f65f8c9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7dec43e28aad1e2cadf4a3049124373963669e4bdc95a2f75e1dd63b3eb7d4`  
		Last Modified: Tue, 17 Feb 2026 21:30:25 GMT  
		Size: 98.2 MB (98162262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf5f7cd1537f5913a85f2ebc069c9789e846bf183dff3a228255ff5cec83d5a`  
		Last Modified: Tue, 17 Feb 2026 21:30:23 GMT  
		Size: 385.7 KB (385692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b69186bf79733d3d6b81c46636fc779e193368bc38db8d3010b68876160cf`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b561868aa7cf7cf04f054a78bd8ea5432a5e5b7616b392f06e30288df496aa06`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.3 MB (23319467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:7a75a5ae722252a8b9844767c6828297b368778a3d70f5504816b7936ca22f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23718026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e88a01f236f2b24fab803387d5f7842537aaa1a1140ffacfa63bdcf5706465`

```dockerfile
```

-	Layers:
	-	`sha256:dc112df1880481e7f97de632618f78f61eb0824afa6205a5a82fbd38878a690a`  
		Last Modified: Tue, 17 Feb 2026 21:30:24 GMT  
		Size: 23.7 MB (23701678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dacecb9f66ba8430cfc5d96bd5a474cdb22ea3a9ba10e6502dc3755a688a6d5`  
		Last Modified: Tue, 17 Feb 2026 21:30:22 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a71d46b79687b6e952bf21946f8452356aed0e784aa795453c3f9ad831a77b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255978994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4492640c45a0ed6d9d1577ab9c9422eef298d6fe6ad7c5c5ad7baeb45987235`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62216dc13167a74c4b0ea4bceed53adbd12ca59082f9d7d140072fb8303cd3b`  
		Last Modified: Tue, 17 Feb 2026 21:30:43 GMT  
		Size: 95.8 MB (95763594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6985ab4c77e34b80ea8654dbbb36877bb046b39b4e1a89152bff01ec65ae27`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 385.7 KB (385698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2fc45c9db8d6efebbc61a4596bd898b8b84cdbaf4216b4d244de614b5ee3ac`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb3a087f98a0a2ce287e3d474cd5e6ecbbd623963b6f262dd73d5a9f42535c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 22.7 MB (22718722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e67eca9f579cf443798f93d494f53a37a344e8402945008184215fd239b80173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23731180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b35429dbe94352de3fa3f88e6dc303fed6f8b1ecaac42e9dc736cff388cc50`

```dockerfile
```

-	Layers:
	-	`sha256:c45162ec875974250027133fdb54d13f0e2c46a6440488ef436a7f1202dc417c`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 23.7 MB (23714695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efac263ab6565b1d35ef93b62b1b9d3966086fba0a87be6a3769e04eaa6614b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:6148c7f47a9675737a01831de25a1fc2a07cbcb55c6cd6e8dd13c830b05c9b33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:11c70a102287b0592d9e9b5fabeedc11615fb3b301ce4692f793298f546a3163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141545723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80abeb3297c13c98c0f836eb2184377b0f524882f80b8ef34dcc60bbb11d3e1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:652e2a056f579fe63480e1d81d849a3e5c44e59779794e86c78d4ac3bfe9cc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17696040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f500caf885fbc06ad2fe874993a6b5e35415fa94f65cb9a332debaaf9ee98bf`

```dockerfile
```

-	Layers:
	-	`sha256:af17cf1784658186af363176782bca7625f37ff722b955ac0ce6c8c85fa823c9`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 17.7 MB (17681426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311ad3ad152e9842bc5a81a96f0e2010214cbe7dc15fb9908ba3f97a5ce29266`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3d7af74d41a146cfb65826f2dfcd9060cf5db8fce5e51ce3d8c19cac2a6113ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137108487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae88015583e04ddfa4f0ee76e958c48b3cbbc252ae89d2702ee5533e2e4a3ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:4b4cb824863d060930fff9f12e1f7dbb8377bbe2ad5e263f7bb70ac82675821d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17682510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56afe4995a0f209c9ead007d27e754c18e4671e607d3d894cda8a026db455b82`

```dockerfile
```

-	Layers:
	-	`sha256:959690f92f969525c8001243651525912a56c6b4390d3964235e3e1daf326c48`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 17.7 MB (17667771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204012cbc471431ffa57a2f389bccb1cb1f923ea5d63a63079a72676b289f238`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:6148c7f47a9675737a01831de25a1fc2a07cbcb55c6cd6e8dd13c830b05c9b33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:11c70a102287b0592d9e9b5fabeedc11615fb3b301ce4692f793298f546a3163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141545723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80abeb3297c13c98c0f836eb2184377b0f524882f80b8ef34dcc60bbb11d3e1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:54 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb36daf1fd72d28fa8ec7db41232743c3310a7741ffbc8152bffda0ad41ef11`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 1.2 MB (1214126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd385ae5eca81d51f71602ffd0c89d6ae513071108777acc462ae236d556c3`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 6.0 MB (5993180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03ffd6227ede7b59ad35a384a3c785d3c2db04c4c8a0bcec8b0cfd1097e1cd9`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 97.2 KB (97205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccaa16a8334ff652d9dd37f3c92c179213d69b28d690ee89a1248fa684e142ef`  
		Last Modified: Tue, 17 Feb 2026 20:31:20 GMT  
		Size: 104.7 MB (104703650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a7e01561e2d489e6b3ed49c38ee395e8def51debf09490e489bb6cae204c8`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:652e2a056f579fe63480e1d81d849a3e5c44e59779794e86c78d4ac3bfe9cc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17696040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f500caf885fbc06ad2fe874993a6b5e35415fa94f65cb9a332debaaf9ee98bf`

```dockerfile
```

-	Layers:
	-	`sha256:af17cf1784658186af363176782bca7625f37ff722b955ac0ce6c8c85fa823c9`  
		Last Modified: Tue, 17 Feb 2026 20:31:18 GMT  
		Size: 17.7 MB (17681426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311ad3ad152e9842bc5a81a96f0e2010214cbe7dc15fb9908ba3f97a5ce29266`  
		Last Modified: Tue, 17 Feb 2026 20:31:17 GMT  
		Size: 14.6 KB (14614 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3d7af74d41a146cfb65826f2dfcd9060cf5db8fce5e51ce3d8c19cac2a6113ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137108487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae88015583e04ddfa4f0ee76e958c48b3cbbc252ae89d2702ee5533e2e4a3ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:11 GMT
ENV ROS_DISTRO=humble
# Tue, 17 Feb 2026 20:30:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18645ec48b5cd0e87d0e4506c045b481e37fe9b3b2eb25377907d2ae7ed29051`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 1.2 MB (1214337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b648a1d2602bc1c46cfe4b71c4ab2dfc0fb3fdb33c518b7c63dc71856f941`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 5.9 MB (5947042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e31d31174c558cb94211479bd475553c14e828fa2a2cd3859d32335c4b151`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 97.4 KB (97391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da891479386a1689d6abd774292e94671dd860097637b72325ef426d9ac33033`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 102.5 MB (102464576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b865c43a1147148db9b69f0ce6c6bff04b54689a86aca56ffa1262b4648096b9`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4b4cb824863d060930fff9f12e1f7dbb8377bbe2ad5e263f7bb70ac82675821d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17682510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56afe4995a0f209c9ead007d27e754c18e4671e607d3d894cda8a026db455b82`

```dockerfile
```

-	Layers:
	-	`sha256:959690f92f969525c8001243651525912a56c6b4390d3964235e3e1daf326c48`  
		Last Modified: Tue, 17 Feb 2026 20:30:40 GMT  
		Size: 17.7 MB (17667771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204012cbc471431ffa57a2f389bccb1cb1f923ea5d63a63079a72676b289f238`  
		Last Modified: Tue, 17 Feb 2026 20:30:39 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:be7350a0efd17925415a6a3a076d6009b425af7500b0a5cdb5d717e87ef46f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:ce6609ec2188d0eadd61640fb598c0aff629a84d88970423b8f341ead2515683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297326820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acefc0d3f654319d0a8acbfda596ca2b0431744931b3a0ac8f94a618d83d8d77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b3d9a566e114da54d21bf58e4966463e527b60b3804930a6ea605d2121e10`  
		Last Modified: Tue, 17 Feb 2026 21:30:41 GMT  
		Size: 110.2 MB (110184420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b854746bc8abeda04290f546ed981825386ca433ccb4ce033b00e37ec7a762`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b716a7040942361f3e8f793c2f0b83c5cd5b3fd97a9a8e257272797914ba`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a19249b8029c3c30665053cae88c2468e2160996f4ec6c15e3e6bd29819be`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 28.0 MB (28010609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:c7d52fb9b437e9975a169b8ba5cb32e7c2c993e4340df84818e379770a2a2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad88720731506dc7d0868322c1d0f61fadec9061136675a508bbbbbfe7a1863f`

```dockerfile
```

-	Layers:
	-	`sha256:7505f29b7ee944b557282d7acf9ff742cd1e597e9ddbe42ee7cbbf9b815600d1`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 24.6 MB (24571534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959b4701f17e17abc6067e5dca9717fe2a8ad033cc3f8ca53a67856cdc739e18`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:88b0bd4c0718167fb546b239f659b98c56b17899bc3156377fbfdf6c4b196d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285711414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275afdcded52da5bf8cad64931e82672234c6074a99241159d31ae5280221085`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cdbf5638e01baf5f4ec197a800f353f617358a1f43b6e151d1b64251e8b7f`  
		Last Modified: Tue, 17 Feb 2026 21:30:51 GMT  
		Size: 105.6 MB (105596998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e52aaae05d7a458e18396f7f0f9d755c781112f84751e5817d0e88bc34ea2`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799712497a09e97750515f98342d57c7f654171747df8aec170c19c3be4ff36`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9582f114d28d219dd1cb06cba385dde792616b75950048223ee0564239480a`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 27.1 MB (27103726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:80a2566beea4dcf1870c72f3cc922773e2f1edc087ec2ce375b65933d18b50a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1c12faadee9c9c6ad804eb672a2f7fbdaba301508b89d3bce85bbdd08fa1e9`

```dockerfile
```

-	Layers:
	-	`sha256:b4d27de917d41f43c9ee5e6f21583acb273448abcdfc67cd0e43ab70da52bec9`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 24.6 MB (24593795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2581bfe955c6a730daea90de82dcfc3db1ad1ee1b5b4edef75bb22c2fdcbb7`  
		Last Modified: Tue, 17 Feb 2026 21:30:47 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:cea9c0d5a4394d6521447c893417ba5faade92f190ab177bf2870e368352e196
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:7c0b5f29d1a916cee2b43c5adf54c808fd9add5cafff50a77e5e9a7e46e2edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081629189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6376b15840456614296141b5a1c92efde60d93072b6b7b155c8ca951d75bd63`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b3d9a566e114da54d21bf58e4966463e527b60b3804930a6ea605d2121e10`  
		Last Modified: Tue, 17 Feb 2026 21:30:41 GMT  
		Size: 110.2 MB (110184420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b854746bc8abeda04290f546ed981825386ca433ccb4ce033b00e37ec7a762`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b716a7040942361f3e8f793c2f0b83c5cd5b3fd97a9a8e257272797914ba`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a19249b8029c3c30665053cae88c2468e2160996f4ec6c15e3e6bd29819be`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 28.0 MB (28010609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a248f2bd79ae227592752d26140bca43f6cd49805b445fabbd2379415a637d0`  
		Last Modified: Tue, 17 Feb 2026 21:55:24 GMT  
		Size: 784.3 MB (784302369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:b754b1e403224a2b35a7e3c8092c75f0bacbfb3956697ccc7f3dca68e84444a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60737081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5617ec2c84a591ed8996711042bb670034e20a08c034c9911b7e9b1365aaa1e2`

```dockerfile
```

-	Layers:
	-	`sha256:04f544610ceaf65160fff3518c4466d4dd6c04726db246918fb926a07d22a1af`  
		Last Modified: Tue, 17 Feb 2026 21:55:11 GMT  
		Size: 60.7 MB (60727742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151fa5cb26c3959ecf68e7943343b2407b0561c5b29eebe45151103e99c9f8cf`  
		Last Modified: Tue, 17 Feb 2026 21:55:09 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8b6c0d1a597df8c8010c35b197e6c013bd28ee56772a9c6e2bfc5196e53565aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.2 MB (984165917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458d4d9e3e544078fa2555551fbdd2755eaa276fe77d151dae147867c4ceb96`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cdbf5638e01baf5f4ec197a800f353f617358a1f43b6e151d1b64251e8b7f`  
		Last Modified: Tue, 17 Feb 2026 21:30:51 GMT  
		Size: 105.6 MB (105596998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e52aaae05d7a458e18396f7f0f9d755c781112f84751e5817d0e88bc34ea2`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799712497a09e97750515f98342d57c7f654171747df8aec170c19c3be4ff36`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9582f114d28d219dd1cb06cba385dde792616b75950048223ee0564239480a`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 27.1 MB (27103726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632a26418f08c9068f128ad80934b0ec0503a1623ab7ab56e34428a5f7c2c703`  
		Last Modified: Tue, 17 Feb 2026 21:56:01 GMT  
		Size: 698.5 MB (698454503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:5d115d51e9f2b2a7556dbdc3d028dc52a9627018450a708cfea2277583aac5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60667669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095fc92103fd36beb37abe141ed896124c1f77dece2a9a2735f2a4a095f59bb3`

```dockerfile
```

-	Layers:
	-	`sha256:f5d8ff15b2600356abe956dcd5df0f098cfe69cfc904538939e6f69b4f1fd843`  
		Last Modified: Tue, 17 Feb 2026 21:55:40 GMT  
		Size: 60.7 MB (60658250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cdb7267854d0b2a71fcc8c327810ceececd93dcbab1078c0b636ced02d6789d`  
		Last Modified: Tue, 17 Feb 2026 21:55:37 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:cea9c0d5a4394d6521447c893417ba5faade92f190ab177bf2870e368352e196
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:7c0b5f29d1a916cee2b43c5adf54c808fd9add5cafff50a77e5e9a7e46e2edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081629189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6376b15840456614296141b5a1c92efde60d93072b6b7b155c8ca951d75bd63`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b3d9a566e114da54d21bf58e4966463e527b60b3804930a6ea605d2121e10`  
		Last Modified: Tue, 17 Feb 2026 21:30:41 GMT  
		Size: 110.2 MB (110184420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b854746bc8abeda04290f546ed981825386ca433ccb4ce033b00e37ec7a762`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b716a7040942361f3e8f793c2f0b83c5cd5b3fd97a9a8e257272797914ba`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a19249b8029c3c30665053cae88c2468e2160996f4ec6c15e3e6bd29819be`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 28.0 MB (28010609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a248f2bd79ae227592752d26140bca43f6cd49805b445fabbd2379415a637d0`  
		Last Modified: Tue, 17 Feb 2026 21:55:24 GMT  
		Size: 784.3 MB (784302369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b754b1e403224a2b35a7e3c8092c75f0bacbfb3956697ccc7f3dca68e84444a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60737081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5617ec2c84a591ed8996711042bb670034e20a08c034c9911b7e9b1365aaa1e2`

```dockerfile
```

-	Layers:
	-	`sha256:04f544610ceaf65160fff3518c4466d4dd6c04726db246918fb926a07d22a1af`  
		Last Modified: Tue, 17 Feb 2026 21:55:11 GMT  
		Size: 60.7 MB (60727742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151fa5cb26c3959ecf68e7943343b2407b0561c5b29eebe45151103e99c9f8cf`  
		Last Modified: Tue, 17 Feb 2026 21:55:09 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8b6c0d1a597df8c8010c35b197e6c013bd28ee56772a9c6e2bfc5196e53565aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.2 MB (984165917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458d4d9e3e544078fa2555551fbdd2755eaa276fe77d151dae147867c4ceb96`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cdbf5638e01baf5f4ec197a800f353f617358a1f43b6e151d1b64251e8b7f`  
		Last Modified: Tue, 17 Feb 2026 21:30:51 GMT  
		Size: 105.6 MB (105596998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e52aaae05d7a458e18396f7f0f9d755c781112f84751e5817d0e88bc34ea2`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799712497a09e97750515f98342d57c7f654171747df8aec170c19c3be4ff36`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9582f114d28d219dd1cb06cba385dde792616b75950048223ee0564239480a`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 27.1 MB (27103726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632a26418f08c9068f128ad80934b0ec0503a1623ab7ab56e34428a5f7c2c703`  
		Last Modified: Tue, 17 Feb 2026 21:56:01 GMT  
		Size: 698.5 MB (698454503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5d115d51e9f2b2a7556dbdc3d028dc52a9627018450a708cfea2277583aac5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60667669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095fc92103fd36beb37abe141ed896124c1f77dece2a9a2735f2a4a095f59bb3`

```dockerfile
```

-	Layers:
	-	`sha256:f5d8ff15b2600356abe956dcd5df0f098cfe69cfc904538939e6f69b4f1fd843`  
		Last Modified: Tue, 17 Feb 2026 21:55:40 GMT  
		Size: 60.7 MB (60658250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cdb7267854d0b2a71fcc8c327810ceececd93dcbab1078c0b636ced02d6789d`  
		Last Modified: Tue, 17 Feb 2026 21:55:37 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:be7350a0efd17925415a6a3a076d6009b425af7500b0a5cdb5d717e87ef46f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:ce6609ec2188d0eadd61640fb598c0aff629a84d88970423b8f341ead2515683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297326820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acefc0d3f654319d0a8acbfda596ca2b0431744931b3a0ac8f94a618d83d8d77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b3d9a566e114da54d21bf58e4966463e527b60b3804930a6ea605d2121e10`  
		Last Modified: Tue, 17 Feb 2026 21:30:41 GMT  
		Size: 110.2 MB (110184420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b854746bc8abeda04290f546ed981825386ca433ccb4ce033b00e37ec7a762`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b716a7040942361f3e8f793c2f0b83c5cd5b3fd97a9a8e257272797914ba`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a19249b8029c3c30665053cae88c2468e2160996f4ec6c15e3e6bd29819be`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 28.0 MB (28010609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:c7d52fb9b437e9975a169b8ba5cb32e7c2c993e4340df84818e379770a2a2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad88720731506dc7d0868322c1d0f61fadec9061136675a508bbbbbfe7a1863f`

```dockerfile
```

-	Layers:
	-	`sha256:7505f29b7ee944b557282d7acf9ff742cd1e597e9ddbe42ee7cbbf9b815600d1`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 24.6 MB (24571534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959b4701f17e17abc6067e5dca9717fe2a8ad033cc3f8ca53a67856cdc739e18`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:88b0bd4c0718167fb546b239f659b98c56b17899bc3156377fbfdf6c4b196d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285711414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275afdcded52da5bf8cad64931e82672234c6074a99241159d31ae5280221085`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cdbf5638e01baf5f4ec197a800f353f617358a1f43b6e151d1b64251e8b7f`  
		Last Modified: Tue, 17 Feb 2026 21:30:51 GMT  
		Size: 105.6 MB (105596998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e52aaae05d7a458e18396f7f0f9d755c781112f84751e5817d0e88bc34ea2`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799712497a09e97750515f98342d57c7f654171747df8aec170c19c3be4ff36`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9582f114d28d219dd1cb06cba385dde792616b75950048223ee0564239480a`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 27.1 MB (27103726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:80a2566beea4dcf1870c72f3cc922773e2f1edc087ec2ce375b65933d18b50a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1c12faadee9c9c6ad804eb672a2f7fbdaba301508b89d3bce85bbdd08fa1e9`

```dockerfile
```

-	Layers:
	-	`sha256:b4d27de917d41f43c9ee5e6f21583acb273448abcdfc67cd0e43ab70da52bec9`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 24.6 MB (24593795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2581bfe955c6a730daea90de82dcfc3db1ad1ee1b5b4edef75bb22c2fdcbb7`  
		Last Modified: Tue, 17 Feb 2026 21:30:47 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:be7350a0efd17925415a6a3a076d6009b425af7500b0a5cdb5d717e87ef46f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:ce6609ec2188d0eadd61640fb598c0aff629a84d88970423b8f341ead2515683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297326820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acefc0d3f654319d0a8acbfda596ca2b0431744931b3a0ac8f94a618d83d8d77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b3d9a566e114da54d21bf58e4966463e527b60b3804930a6ea605d2121e10`  
		Last Modified: Tue, 17 Feb 2026 21:30:41 GMT  
		Size: 110.2 MB (110184420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b854746bc8abeda04290f546ed981825386ca433ccb4ce033b00e37ec7a762`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b716a7040942361f3e8f793c2f0b83c5cd5b3fd97a9a8e257272797914ba`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a19249b8029c3c30665053cae88c2468e2160996f4ec6c15e3e6bd29819be`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 28.0 MB (28010609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c7d52fb9b437e9975a169b8ba5cb32e7c2c993e4340df84818e379770a2a2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad88720731506dc7d0868322c1d0f61fadec9061136675a508bbbbbfe7a1863f`

```dockerfile
```

-	Layers:
	-	`sha256:7505f29b7ee944b557282d7acf9ff742cd1e597e9ddbe42ee7cbbf9b815600d1`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 24.6 MB (24571534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959b4701f17e17abc6067e5dca9717fe2a8ad033cc3f8ca53a67856cdc739e18`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:88b0bd4c0718167fb546b239f659b98c56b17899bc3156377fbfdf6c4b196d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285711414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275afdcded52da5bf8cad64931e82672234c6074a99241159d31ae5280221085`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cdbf5638e01baf5f4ec197a800f353f617358a1f43b6e151d1b64251e8b7f`  
		Last Modified: Tue, 17 Feb 2026 21:30:51 GMT  
		Size: 105.6 MB (105596998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e52aaae05d7a458e18396f7f0f9d755c781112f84751e5817d0e88bc34ea2`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799712497a09e97750515f98342d57c7f654171747df8aec170c19c3be4ff36`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9582f114d28d219dd1cb06cba385dde792616b75950048223ee0564239480a`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 27.1 MB (27103726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:80a2566beea4dcf1870c72f3cc922773e2f1edc087ec2ce375b65933d18b50a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1c12faadee9c9c6ad804eb672a2f7fbdaba301508b89d3bce85bbdd08fa1e9`

```dockerfile
```

-	Layers:
	-	`sha256:b4d27de917d41f43c9ee5e6f21583acb273448abcdfc67cd0e43ab70da52bec9`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 24.6 MB (24593795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2581bfe955c6a730daea90de82dcfc3db1ad1ee1b5b4edef75bb22c2fdcbb7`  
		Last Modified: Tue, 17 Feb 2026 21:30:47 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:3acd13deada29af2d41dab37f0ad3c48c5ea7a89fd109ef9c82c561c13b38476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:7ba2f865e5c89b86dd1149e03d2cc6b85e925422e436ed6d6876560ed786c2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158735704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5433c1cc2c3a0f52c726d84f56bbb42f2c19a2311ac1f1938a7ff4de372364cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:c8a78d4a306bcd35b2cbb4f9d8eec46bec49d2e0c5eae491f325a7b98dc7e681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9324915ce63b75e3a48d8e3d286fe74d3e1dcfbb06f3b3f45ba2b570670400d`

```dockerfile
```

-	Layers:
	-	`sha256:3e2c361af4d2b9e40c7cfa68112fd8acb81f41791f53921b213170ab7f6ae23c`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5888590af6f53c5aee7a3722ab80113f530742cb7bd8f0227c9daf9a24cd4d`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e9b09a496cab2e0ad7a0355ff0731285e214f73d72f560ed220d71321516dcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152614615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fabb98f88137bd3e0a7f098cfc28fcda5020a95b987330330d3d6839588d188`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:02678a7cebe104e42e8b1689dbcaa54f8a2aeb0476e13a6a1a06c28dd45335cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ade2b6030bd5dceaa50b139ff0a6e2daf6d8ebc1db41667f92edfa7ca25a107`

```dockerfile
```

-	Layers:
	-	`sha256:17e7077600b10636d6c91d92f5865c7ea1c370c2e0f3152a89baa9935108d915`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea531b1091e37cc0075a567a3cf435ed4a3b8942d11fc8b5b1f372b499b8f287`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:3acd13deada29af2d41dab37f0ad3c48c5ea7a89fd109ef9c82c561c13b38476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:7ba2f865e5c89b86dd1149e03d2cc6b85e925422e436ed6d6876560ed786c2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158735704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5433c1cc2c3a0f52c726d84f56bbb42f2c19a2311ac1f1938a7ff4de372364cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c8a78d4a306bcd35b2cbb4f9d8eec46bec49d2e0c5eae491f325a7b98dc7e681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9324915ce63b75e3a48d8e3d286fe74d3e1dcfbb06f3b3f45ba2b570670400d`

```dockerfile
```

-	Layers:
	-	`sha256:3e2c361af4d2b9e40c7cfa68112fd8acb81f41791f53921b213170ab7f6ae23c`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5888590af6f53c5aee7a3722ab80113f530742cb7bd8f0227c9daf9a24cd4d`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e9b09a496cab2e0ad7a0355ff0731285e214f73d72f560ed220d71321516dcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152614615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fabb98f88137bd3e0a7f098cfc28fcda5020a95b987330330d3d6839588d188`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:02678a7cebe104e42e8b1689dbcaa54f8a2aeb0476e13a6a1a06c28dd45335cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ade2b6030bd5dceaa50b139ff0a6e2daf6d8ebc1db41667f92edfa7ca25a107`

```dockerfile
```

-	Layers:
	-	`sha256:17e7077600b10636d6c91d92f5865c7ea1c370c2e0f3152a89baa9935108d915`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea531b1091e37cc0075a567a3cf435ed4a3b8942d11fc8b5b1f372b499b8f287`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:8da7f7fa59bd12358e5747d01f27cc72b170087d9385b518c409d78a708d054f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:142107517dbd635a465b087c93bd5baaa95ea674edb98971ddfc419b6dd2a710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298136760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1541b452cc1ef1bf23289369e927a6ef6c363a43cf079034898b62b3fa6e9f82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7664201107a73be69a1fcc67abe7b8dfba9f08f8ac21cd6e6653ff31c72386`  
		Last Modified: Tue, 17 Feb 2026 21:30:45 GMT  
		Size: 110.2 MB (110187964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ca4d412f7ba8e088e340e41db78e3af76477eef4de912442cad60baafe980`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 374.4 KB (374406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b84c226681e00ba22043272c1fd02b401bd4ef90eeb5d75340c924016701c0b`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f44533e62581038678d3c036cd8b357f29ecca65c9e45adeafa646d32244d7`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 28.1 MB (28064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:76bd4a9406e75fb1ce91a7ec01a8d57548e73b3fa3ae7e49f06ee73512c442ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24601050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61448b0d6517ebf743ef3cfa18d2cf8db4e3fa89627cf81f55d956619b218ee4`

```dockerfile
```

-	Layers:
	-	`sha256:e96a8d5c8c28953c60992748f592a29c89a24846347219530366abeb2cd963dc`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 24.6 MB (24584703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043e5fa61b540d977a745f78b99a2c7a43cd3f0684aca7f9ca74ad7057c3b7e1`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f485861c48c691bdd94fb5b278fae25bb65e23405ddc307c390ed1125b39b270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286462906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aec7a60265cff1010022fe066e76ac3ccdcd9cd58e296905e9df6d0d5ea935`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:30:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e37013cf9183e38cc9955d643924c43a7498cfc246fcbca68d2cd37ff696`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 105.6 MB (105600489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767953e8490b993e411a343f8bcff3b560c0ca2cbfe5175afe92ff040558a79`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 374.4 KB (374408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ebc39380b97a2003e0ec3a56e4d2013953c1ad0bf4c68d2bc22d7c2a61e80`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c245d1be384cea3eebb42dfd710b8a80c899f2db13badd8d32df1fd718dc4d7a`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 27.1 MB (27146333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:94e9b065f18eabbb67b64926525574cd16faadb1d19518951137e4e3a855c0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24623444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814b86870d96f8d262f86c272889f9c5b9ffcdda5498ee527a6480f2d4b4502d`

```dockerfile
```

-	Layers:
	-	`sha256:46e79985533ff02e1d666e674ccb4d3da616b812b93b3e30d83cfdac9410e698`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 24.6 MB (24606960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a441fb19ad061cae8b01e2aa0398c0b2e5842c36e59b060a46bbb6bcac5092`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:df006176bdbb38a2f4c59f304ee32ac46bac54aa03dc4a0133d269baa49fc468
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:e6f91c3d34b47041c937a5daeb2f0a55c8479b8883b1d7c61252dd304dcaa279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082902200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec818ea038b7bfb7815ab0c942fdd455cf6045c2fb73a15e3307d481bbcfab14`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7664201107a73be69a1fcc67abe7b8dfba9f08f8ac21cd6e6653ff31c72386`  
		Last Modified: Tue, 17 Feb 2026 21:30:45 GMT  
		Size: 110.2 MB (110187964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ca4d412f7ba8e088e340e41db78e3af76477eef4de912442cad60baafe980`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 374.4 KB (374406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b84c226681e00ba22043272c1fd02b401bd4ef90eeb5d75340c924016701c0b`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f44533e62581038678d3c036cd8b357f29ecca65c9e45adeafa646d32244d7`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 28.1 MB (28064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edfa12c0b2f586afbbc2dc086c98d0e4752d1791c77d6e829165d71b09b550`  
		Last Modified: Tue, 17 Feb 2026 21:55:26 GMT  
		Size: 784.8 MB (784765440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:15dec1e8c4da3c20147899d1139e71a89e23f20ec9c336275959c60cd3ac61a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60761103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909cf12fab19f06ec4c6305031a28fddb4bdb2f505e6dd041bcd116d630422f4`

```dockerfile
```

-	Layers:
	-	`sha256:d82a0845919bcfb8dd34f41e681ea13c14b6c107a5328896d2eba075d3837a1b`  
		Last Modified: Tue, 17 Feb 2026 21:55:14 GMT  
		Size: 60.8 MB (60751752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4b33f28b99423ba94d636d48bb079cc4f6f733418cc852f68f1c0f21a268ac`  
		Last Modified: Tue, 17 Feb 2026 21:55:11 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ba057f2b9047d10eddf26a5644878e87b2230a07f5b7390634aefec782d96948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.4 MB (985445837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c5a8b7ca0950611f2b6ac14d4418fe70b141100460122e3161e2a793eb0421`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:30:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e37013cf9183e38cc9955d643924c43a7498cfc246fcbca68d2cd37ff696`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 105.6 MB (105600489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767953e8490b993e411a343f8bcff3b560c0ca2cbfe5175afe92ff040558a79`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 374.4 KB (374408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ebc39380b97a2003e0ec3a56e4d2013953c1ad0bf4c68d2bc22d7c2a61e80`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c245d1be384cea3eebb42dfd710b8a80c899f2db13badd8d32df1fd718dc4d7a`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 27.1 MB (27146333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427bf6b6cc768f90af14376514666a34e1726b5cdb30ce2503fa9afe353ed9e1`  
		Last Modified: Tue, 17 Feb 2026 21:56:14 GMT  
		Size: 699.0 MB (698982931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:750cf893050c09301049d9126bdd06b97686bf543468da9d8c577d1829b97249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60691700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e30d478cf9fe0d997c1002d421ac54a2677edefd8ae07927d8a3d0241206325`

```dockerfile
```

-	Layers:
	-	`sha256:f8677181204ff6c354021d415b10ea0fe48ccc47d3010644cc217a5ea35537c7`  
		Last Modified: Tue, 17 Feb 2026 21:55:58 GMT  
		Size: 60.7 MB (60682268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab58feac95b434cc6637c12fa0d38b78b357de8c42bcebbde3b6b782aa647c2`  
		Last Modified: Tue, 17 Feb 2026 21:55:55 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:df006176bdbb38a2f4c59f304ee32ac46bac54aa03dc4a0133d269baa49fc468
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:e6f91c3d34b47041c937a5daeb2f0a55c8479b8883b1d7c61252dd304dcaa279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082902200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec818ea038b7bfb7815ab0c942fdd455cf6045c2fb73a15e3307d481bbcfab14`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7664201107a73be69a1fcc67abe7b8dfba9f08f8ac21cd6e6653ff31c72386`  
		Last Modified: Tue, 17 Feb 2026 21:30:45 GMT  
		Size: 110.2 MB (110187964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ca4d412f7ba8e088e340e41db78e3af76477eef4de912442cad60baafe980`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 374.4 KB (374406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b84c226681e00ba22043272c1fd02b401bd4ef90eeb5d75340c924016701c0b`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f44533e62581038678d3c036cd8b357f29ecca65c9e45adeafa646d32244d7`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 28.1 MB (28064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71edfa12c0b2f586afbbc2dc086c98d0e4752d1791c77d6e829165d71b09b550`  
		Last Modified: Tue, 17 Feb 2026 21:55:26 GMT  
		Size: 784.8 MB (784765440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:15dec1e8c4da3c20147899d1139e71a89e23f20ec9c336275959c60cd3ac61a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60761103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909cf12fab19f06ec4c6305031a28fddb4bdb2f505e6dd041bcd116d630422f4`

```dockerfile
```

-	Layers:
	-	`sha256:d82a0845919bcfb8dd34f41e681ea13c14b6c107a5328896d2eba075d3837a1b`  
		Last Modified: Tue, 17 Feb 2026 21:55:14 GMT  
		Size: 60.8 MB (60751752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4b33f28b99423ba94d636d48bb079cc4f6f733418cc852f68f1c0f21a268ac`  
		Last Modified: Tue, 17 Feb 2026 21:55:11 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ba057f2b9047d10eddf26a5644878e87b2230a07f5b7390634aefec782d96948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.4 MB (985445837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c5a8b7ca0950611f2b6ac14d4418fe70b141100460122e3161e2a793eb0421`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:30:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e37013cf9183e38cc9955d643924c43a7498cfc246fcbca68d2cd37ff696`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 105.6 MB (105600489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767953e8490b993e411a343f8bcff3b560c0ca2cbfe5175afe92ff040558a79`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 374.4 KB (374408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ebc39380b97a2003e0ec3a56e4d2013953c1ad0bf4c68d2bc22d7c2a61e80`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c245d1be384cea3eebb42dfd710b8a80c899f2db13badd8d32df1fd718dc4d7a`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 27.1 MB (27146333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427bf6b6cc768f90af14376514666a34e1726b5cdb30ce2503fa9afe353ed9e1`  
		Last Modified: Tue, 17 Feb 2026 21:56:14 GMT  
		Size: 699.0 MB (698982931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:750cf893050c09301049d9126bdd06b97686bf543468da9d8c577d1829b97249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60691700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e30d478cf9fe0d997c1002d421ac54a2677edefd8ae07927d8a3d0241206325`

```dockerfile
```

-	Layers:
	-	`sha256:f8677181204ff6c354021d415b10ea0fe48ccc47d3010644cc217a5ea35537c7`  
		Last Modified: Tue, 17 Feb 2026 21:55:58 GMT  
		Size: 60.7 MB (60682268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab58feac95b434cc6637c12fa0d38b78b357de8c42bcebbde3b6b782aa647c2`  
		Last Modified: Tue, 17 Feb 2026 21:55:55 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:8da7f7fa59bd12358e5747d01f27cc72b170087d9385b518c409d78a708d054f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:142107517dbd635a465b087c93bd5baaa95ea674edb98971ddfc419b6dd2a710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298136760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1541b452cc1ef1bf23289369e927a6ef6c363a43cf079034898b62b3fa6e9f82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7664201107a73be69a1fcc67abe7b8dfba9f08f8ac21cd6e6653ff31c72386`  
		Last Modified: Tue, 17 Feb 2026 21:30:45 GMT  
		Size: 110.2 MB (110187964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ca4d412f7ba8e088e340e41db78e3af76477eef4de912442cad60baafe980`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 374.4 KB (374406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b84c226681e00ba22043272c1fd02b401bd4ef90eeb5d75340c924016701c0b`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f44533e62581038678d3c036cd8b357f29ecca65c9e45adeafa646d32244d7`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 28.1 MB (28064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:76bd4a9406e75fb1ce91a7ec01a8d57548e73b3fa3ae7e49f06ee73512c442ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24601050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61448b0d6517ebf743ef3cfa18d2cf8db4e3fa89627cf81f55d956619b218ee4`

```dockerfile
```

-	Layers:
	-	`sha256:e96a8d5c8c28953c60992748f592a29c89a24846347219530366abeb2cd963dc`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 24.6 MB (24584703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043e5fa61b540d977a745f78b99a2c7a43cd3f0684aca7f9ca74ad7057c3b7e1`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f485861c48c691bdd94fb5b278fae25bb65e23405ddc307c390ed1125b39b270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286462906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aec7a60265cff1010022fe066e76ac3ccdcd9cd58e296905e9df6d0d5ea935`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:30:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e37013cf9183e38cc9955d643924c43a7498cfc246fcbca68d2cd37ff696`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 105.6 MB (105600489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767953e8490b993e411a343f8bcff3b560c0ca2cbfe5175afe92ff040558a79`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 374.4 KB (374408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ebc39380b97a2003e0ec3a56e4d2013953c1ad0bf4c68d2bc22d7c2a61e80`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c245d1be384cea3eebb42dfd710b8a80c899f2db13badd8d32df1fd718dc4d7a`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 27.1 MB (27146333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:94e9b065f18eabbb67b64926525574cd16faadb1d19518951137e4e3a855c0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24623444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814b86870d96f8d262f86c272889f9c5b9ffcdda5498ee527a6480f2d4b4502d`

```dockerfile
```

-	Layers:
	-	`sha256:46e79985533ff02e1d666e674ccb4d3da616b812b93b3e30d83cfdac9410e698`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 24.6 MB (24606960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a441fb19ad061cae8b01e2aa0398c0b2e5842c36e59b060a46bbb6bcac5092`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:8da7f7fa59bd12358e5747d01f27cc72b170087d9385b518c409d78a708d054f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:142107517dbd635a465b087c93bd5baaa95ea674edb98971ddfc419b6dd2a710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298136760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1541b452cc1ef1bf23289369e927a6ef6c363a43cf079034898b62b3fa6e9f82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7664201107a73be69a1fcc67abe7b8dfba9f08f8ac21cd6e6653ff31c72386`  
		Last Modified: Tue, 17 Feb 2026 21:30:45 GMT  
		Size: 110.2 MB (110187964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ca4d412f7ba8e088e340e41db78e3af76477eef4de912442cad60baafe980`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 374.4 KB (374406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b84c226681e00ba22043272c1fd02b401bd4ef90eeb5d75340c924016701c0b`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f44533e62581038678d3c036cd8b357f29ecca65c9e45adeafa646d32244d7`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 28.1 MB (28064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:76bd4a9406e75fb1ce91a7ec01a8d57548e73b3fa3ae7e49f06ee73512c442ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24601050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61448b0d6517ebf743ef3cfa18d2cf8db4e3fa89627cf81f55d956619b218ee4`

```dockerfile
```

-	Layers:
	-	`sha256:e96a8d5c8c28953c60992748f592a29c89a24846347219530366abeb2cd963dc`  
		Last Modified: Tue, 17 Feb 2026 21:30:42 GMT  
		Size: 24.6 MB (24584703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043e5fa61b540d977a745f78b99a2c7a43cd3f0684aca7f9ca74ad7057c3b7e1`  
		Last Modified: Tue, 17 Feb 2026 21:30:40 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f485861c48c691bdd94fb5b278fae25bb65e23405ddc307c390ed1125b39b270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286462906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aec7a60265cff1010022fe066e76ac3ccdcd9cd58e296905e9df6d0d5ea935`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:30:00 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4448e37013cf9183e38cc9955d643924c43a7498cfc246fcbca68d2cd37ff696`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 105.6 MB (105600489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767953e8490b993e411a343f8bcff3b560c0ca2cbfe5175afe92ff040558a79`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 374.4 KB (374408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26ebc39380b97a2003e0ec3a56e4d2013953c1ad0bf4c68d2bc22d7c2a61e80`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c245d1be384cea3eebb42dfd710b8a80c899f2db13badd8d32df1fd718dc4d7a`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 27.1 MB (27146333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:94e9b065f18eabbb67b64926525574cd16faadb1d19518951137e4e3a855c0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24623444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814b86870d96f8d262f86c272889f9c5b9ffcdda5498ee527a6480f2d4b4502d`

```dockerfile
```

-	Layers:
	-	`sha256:46e79985533ff02e1d666e674ccb4d3da616b812b93b3e30d83cfdac9410e698`  
		Last Modified: Tue, 17 Feb 2026 21:30:58 GMT  
		Size: 24.6 MB (24606960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a441fb19ad061cae8b01e2aa0398c0b2e5842c36e59b060a46bbb6bcac5092`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:9df9a73dfb4529e331c651c51eb2c5e53d26d38eced642a6176fb8b08bf63ddd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:aa9d0e7a5a0de93b6c9639949b0448387007ac020074a28697d383a19bbbb8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159507664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a637fac4a1da4fd447c291397705f10770529044ada5c1daa8b62addb3f0e732`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f3da8efb9a5a6b1f055cb68405604c87d44ea58741eff33da3035c3404990841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18348767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7537f06471990282961fb3916c96d7d41651d8e17cee33f80cc9de626713e22`

```dockerfile
```

-	Layers:
	-	`sha256:28e18b2dc20ebed812c25b487b3ec251072847ab7fcd13a790aa89b38edcbcbe`  
		Last Modified: Tue, 17 Feb 2026 20:31:51 GMT  
		Size: 18.3 MB (18334158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b2ceb9fbb63c9584290a7c001300912a49e2289cf303a9188e2619aa320340`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b5278f418762522ab382851cd30051434c89a906a27d52c31c57428507db81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153339167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10e29ed1dabff989082530269b5cfb6ac7c965601eb7b7f1d58d5d1c5c213e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:0d96006a3656489e4fbbc326e2951be49e3259ee934af69813f5cf31f46d4c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18322898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f2be7b312b6953c99ac3fe94e7c7075d10e3725bea4eaef7d60ced53078155`

```dockerfile
```

-	Layers:
	-	`sha256:cff3b0d81aa847b8b80f981ab060fad729b96add29e8c0af818cadfadd604c53`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 18.3 MB (18308164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f6184b90f992241505423cab8b7277ed17eb36725fc217a0e32c90171abd36`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:9df9a73dfb4529e331c651c51eb2c5e53d26d38eced642a6176fb8b08bf63ddd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:aa9d0e7a5a0de93b6c9639949b0448387007ac020074a28697d383a19bbbb8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159507664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a637fac4a1da4fd447c291397705f10770529044ada5c1daa8b62addb3f0e732`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:35 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:21 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6258945f1d2a6e861a58388276d97ad9e277485239d40e851988410562ea7`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 684.0 KB (683954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05fb7dae912dbe49e93ba6434ac0d6b402be813c0b373f2d69eb287cc8071e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 6.7 MB (6749467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da204b536633a39ef76265eca1307eb09e44ce38040f08f2bff65c24fa1cf37`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 94.2 KB (94151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6b6def36f07048480e9220add30ca3c423fb273e95213c76a049165ecbaaae`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 122.3 MB (122252285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226eb2247de4862db4e76be01f1b2fea4af11588b4c4a7de5f41a3bc748198e`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f3da8efb9a5a6b1f055cb68405604c87d44ea58741eff33da3035c3404990841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18348767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7537f06471990282961fb3916c96d7d41651d8e17cee33f80cc9de626713e22`

```dockerfile
```

-	Layers:
	-	`sha256:28e18b2dc20ebed812c25b487b3ec251072847ab7fcd13a790aa89b38edcbcbe`  
		Last Modified: Tue, 17 Feb 2026 20:31:51 GMT  
		Size: 18.3 MB (18334158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b2ceb9fbb63c9584290a7c001300912a49e2289cf303a9188e2619aa320340`  
		Last Modified: Tue, 17 Feb 2026 20:31:49 GMT  
		Size: 14.6 KB (14609 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b5278f418762522ab382851cd30051434c89a906a27d52c31c57428507db81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153339167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10e29ed1dabff989082530269b5cfb6ac7c965601eb7b7f1d58d5d1c5c213e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:27 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:13 GMT
ENV ROS_DISTRO=kilted
# Tue, 17 Feb 2026 20:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f486837e1c7893b0d997d722c0b3124671ec83248346e7893f0ff21e8c276`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 684.1 KB (684090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93d611be098da8ea0b2858e9f03622a1e3e5c8f43f2eeb97f878f6859c5f06`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 6.8 MB (6762611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec439fca92fb8631158e3e3796842e521de2575d73ddec227c5a47d83635b6`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 94.3 KB (94269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd84f029fa4b3abe15699eee427345f63d5c5ae19538d7edf00f2b788dfd5a`  
		Last Modified: Tue, 17 Feb 2026 20:30:45 GMT  
		Size: 116.9 MB (116932881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010f081aefa0ee68f583b4c56ea0ce5cdade0407823a2b92c89b1cd4b84161f`  
		Last Modified: Tue, 17 Feb 2026 20:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:0d96006a3656489e4fbbc326e2951be49e3259ee934af69813f5cf31f46d4c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18322898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f2be7b312b6953c99ac3fe94e7c7075d10e3725bea4eaef7d60ced53078155`

```dockerfile
```

-	Layers:
	-	`sha256:cff3b0d81aa847b8b80f981ab060fad729b96add29e8c0af818cadfadd604c53`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 18.3 MB (18308164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f6184b90f992241505423cab8b7277ed17eb36725fc217a0e32c90171abd36`  
		Last Modified: Tue, 17 Feb 2026 20:30:42 GMT  
		Size: 14.7 KB (14734 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:be7350a0efd17925415a6a3a076d6009b425af7500b0a5cdb5d717e87ef46f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:ce6609ec2188d0eadd61640fb598c0aff629a84d88970423b8f341ead2515683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297326820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acefc0d3f654319d0a8acbfda596ca2b0431744931b3a0ac8f94a618d83d8d77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b3d9a566e114da54d21bf58e4966463e527b60b3804930a6ea605d2121e10`  
		Last Modified: Tue, 17 Feb 2026 21:30:41 GMT  
		Size: 110.2 MB (110184420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b854746bc8abeda04290f546ed981825386ca433ccb4ce033b00e37ec7a762`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b716a7040942361f3e8f793c2f0b83c5cd5b3fd97a9a8e257272797914ba`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a19249b8029c3c30665053cae88c2468e2160996f4ec6c15e3e6bd29819be`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 28.0 MB (28010609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:c7d52fb9b437e9975a169b8ba5cb32e7c2c993e4340df84818e379770a2a2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad88720731506dc7d0868322c1d0f61fadec9061136675a508bbbbbfe7a1863f`

```dockerfile
```

-	Layers:
	-	`sha256:7505f29b7ee944b557282d7acf9ff742cd1e597e9ddbe42ee7cbbf9b815600d1`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 24.6 MB (24571534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959b4701f17e17abc6067e5dca9717fe2a8ad033cc3f8ca53a67856cdc739e18`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:88b0bd4c0718167fb546b239f659b98c56b17899bc3156377fbfdf6c4b196d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285711414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275afdcded52da5bf8cad64931e82672234c6074a99241159d31ae5280221085`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cdbf5638e01baf5f4ec197a800f353f617358a1f43b6e151d1b64251e8b7f`  
		Last Modified: Tue, 17 Feb 2026 21:30:51 GMT  
		Size: 105.6 MB (105596998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e52aaae05d7a458e18396f7f0f9d755c781112f84751e5817d0e88bc34ea2`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799712497a09e97750515f98342d57c7f654171747df8aec170c19c3be4ff36`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9582f114d28d219dd1cb06cba385dde792616b75950048223ee0564239480a`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 27.1 MB (27103726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:80a2566beea4dcf1870c72f3cc922773e2f1edc087ec2ce375b65933d18b50a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1c12faadee9c9c6ad804eb672a2f7fbdaba301508b89d3bce85bbdd08fa1e9`

```dockerfile
```

-	Layers:
	-	`sha256:b4d27de917d41f43c9ee5e6f21583acb273448abcdfc67cd0e43ab70da52bec9`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 24.6 MB (24593795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2581bfe955c6a730daea90de82dcfc3db1ad1ee1b5b4edef75bb22c2fdcbb7`  
		Last Modified: Tue, 17 Feb 2026 21:30:47 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:0b43ca8bb2b1c618139b527fbc345e05024c7daa0b654bbf51a496a6a3ff15f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:ec7109087c5e59a4cfbf1ca8aef22c0a20e5b26ea06c1bc665695fa2396e67b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311776265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4be1fea49cd0e8e0285a854bd5de7270ef475881253ef9d8bd09029876cb77c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ef68b8c806cd8e903009ab4882feb9e9ea56176b99719ea0e3c7ebbfac1f4`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 110.2 MB (110188830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60572606e296b3d090dc856f0b55084a6e2d0ad69bbf5971816665902bb4bfb9`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 367.7 KB (367683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a46da188376f13cd0fa38e85a153c20688d45f128f8e0b541b3ac68cc23df`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a4e1fd4e992445106871cb0338c26eea2bf2558c4a42b33a7b9606ebc52b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:56 GMT  
		Size: 27.8 MB (27844723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:f6330a9672aefce6f5636e5d5ea0571abe0e95233c109a966b4ad1a0c5d94b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25637355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c436b9c719e9efb83e8d56860b98a13dc9cbe3516270ca528abca59e02d59f`

```dockerfile
```

-	Layers:
	-	`sha256:d9cc8355dd05b5855b535ebd9d724ef97e19c678ef84f57cc6740f444d7a48a5`  
		Last Modified: Tue, 17 Feb 2026 21:30:55 GMT  
		Size: 25.6 MB (25620991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa164f4d7ae83b6a4c224d7db8adf4552b29218daf00d021361ef916a662df0a`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4fdd7b5ed66b33350063a7fb066fb057275c668a72db872fe062fb83639f77f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299700892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bcf89f4996d8601126e407ccbd5081f913b2545c1e48d6e55de878aaa183d6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dbe63264e1ed1c4f3e5e806897b787c7e5d70a66666a164214f314edacd021`  
		Last Modified: Tue, 17 Feb 2026 21:31:03 GMT  
		Size: 105.6 MB (105601575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3f84333d023de739abbd5700103a0cb9bfc6f3c3ca019a07b45f1fc73504e`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 367.7 KB (367679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d5eb6309d46d62dfb27dc6f4e5b31f76a785a45edfbf560aee4d5e5091e72b`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f253acc6e2219780d32daada961d2c5b2592e94cd1719fad650ff143dd9205c`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 26.9 MB (26929636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:7dd40f7f6feaa0f035cbe9c7a9773bf1320d68764d5703fa30754dccc21ae87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25659947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074f694a516f67301a8f73e90ffc609df3070a55ed8dcfcc95f95fabe9692fd8`

```dockerfile
```

-	Layers:
	-	`sha256:9361dce8b643dcdb0f9e2a00abf93bd8770c467f83280781acca62a0d3f76702`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 25.6 MB (25643445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6a1c50a9e6a7cb079ca09d9e038bfac24f8052ec8de6ca371c4c42dc313ea4f`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:fb8086e4295ca2d3412d809fd1ef981f4a98cf5805e71f5564fa20efb33f2d48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:1884bd21776b273efb12261ead653db80a4ae9425ec5abfbeac669eb0aa5676e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1096229150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d57bea1a7fabaccfef058f3b510c1a02c43467c9be2d3fb6f1a15b718aae4c3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ef68b8c806cd8e903009ab4882feb9e9ea56176b99719ea0e3c7ebbfac1f4`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 110.2 MB (110188830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60572606e296b3d090dc856f0b55084a6e2d0ad69bbf5971816665902bb4bfb9`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 367.7 KB (367683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a46da188376f13cd0fa38e85a153c20688d45f128f8e0b541b3ac68cc23df`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a4e1fd4e992445106871cb0338c26eea2bf2558c4a42b33a7b9606ebc52b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:56 GMT  
		Size: 27.8 MB (27844723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d2037de5d82347ca4d0a0d9736def979448a5d5a7bb945dc30a390ca12c24d`  
		Last Modified: Tue, 17 Feb 2026 21:56:30 GMT  
		Size: 784.5 MB (784452885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:602d977f68716e850e22a295eaafe3450181da8da32528af410672f6b7391329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61804780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cac23806c69f0d0cbbf1683f32ab20f781f935e0016ccf9285bc06275b7599e`

```dockerfile
```

-	Layers:
	-	`sha256:2ddf8a1416f7d33457b5127ef6b1f6a63c3a45213218851a9ee43f32daa27076`  
		Last Modified: Tue, 17 Feb 2026 21:56:18 GMT  
		Size: 61.8 MB (61795419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f4def1dede899b783201d1d5b712dba0cdbda0ca9139ead34bc6c6a4e266b9`  
		Last Modified: Tue, 17 Feb 2026 21:56:15 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a6729dd234543ac2e1d3ebf62ef2a70c69dc74f3d843b787950c9a6450405b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **998.3 MB (998319143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b83837afd9c25b9027a997821fd94e1ab8ac79f2aaa5f8dea9736dfabea0cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dbe63264e1ed1c4f3e5e806897b787c7e5d70a66666a164214f314edacd021`  
		Last Modified: Tue, 17 Feb 2026 21:31:03 GMT  
		Size: 105.6 MB (105601575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3f84333d023de739abbd5700103a0cb9bfc6f3c3ca019a07b45f1fc73504e`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 367.7 KB (367679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d5eb6309d46d62dfb27dc6f4e5b31f76a785a45edfbf560aee4d5e5091e72b`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f253acc6e2219780d32daada961d2c5b2592e94cd1719fad650ff143dd9205c`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 26.9 MB (26929636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543423e6e5a3857ebd4d024734955f3cd9173641862eb322c5814b2c0be13123`  
		Last Modified: Tue, 17 Feb 2026 21:56:35 GMT  
		Size: 698.6 MB (698618251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1d6711c83675114e2c338a45cbd68677708091daf2771ecebc3d9d567a8384f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec08d47ed0590f71a05f40fb9642dad349315c629d295f376155aa1cc771d3d9`

```dockerfile
```

-	Layers:
	-	`sha256:92fcc244968d9640cc62bf6f1c73a151d0cd304ae35b8fa810f8ab20f2b52bed`  
		Last Modified: Tue, 17 Feb 2026 21:56:23 GMT  
		Size: 61.7 MB (61726132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207c8407681709a69a1163579d31df40ed4f1f3cf3c448aac2cb404be63c1239`  
		Last Modified: Tue, 17 Feb 2026 21:56:21 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:fb8086e4295ca2d3412d809fd1ef981f4a98cf5805e71f5564fa20efb33f2d48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:1884bd21776b273efb12261ead653db80a4ae9425ec5abfbeac669eb0aa5676e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1096229150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d57bea1a7fabaccfef058f3b510c1a02c43467c9be2d3fb6f1a15b718aae4c3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ef68b8c806cd8e903009ab4882feb9e9ea56176b99719ea0e3c7ebbfac1f4`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 110.2 MB (110188830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60572606e296b3d090dc856f0b55084a6e2d0ad69bbf5971816665902bb4bfb9`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 367.7 KB (367683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a46da188376f13cd0fa38e85a153c20688d45f128f8e0b541b3ac68cc23df`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a4e1fd4e992445106871cb0338c26eea2bf2558c4a42b33a7b9606ebc52b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:56 GMT  
		Size: 27.8 MB (27844723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d2037de5d82347ca4d0a0d9736def979448a5d5a7bb945dc30a390ca12c24d`  
		Last Modified: Tue, 17 Feb 2026 21:56:30 GMT  
		Size: 784.5 MB (784452885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:602d977f68716e850e22a295eaafe3450181da8da32528af410672f6b7391329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61804780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cac23806c69f0d0cbbf1683f32ab20f781f935e0016ccf9285bc06275b7599e`

```dockerfile
```

-	Layers:
	-	`sha256:2ddf8a1416f7d33457b5127ef6b1f6a63c3a45213218851a9ee43f32daa27076`  
		Last Modified: Tue, 17 Feb 2026 21:56:18 GMT  
		Size: 61.8 MB (61795419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f4def1dede899b783201d1d5b712dba0cdbda0ca9139ead34bc6c6a4e266b9`  
		Last Modified: Tue, 17 Feb 2026 21:56:15 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a6729dd234543ac2e1d3ebf62ef2a70c69dc74f3d843b787950c9a6450405b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **998.3 MB (998319143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b83837afd9c25b9027a997821fd94e1ab8ac79f2aaa5f8dea9736dfabea0cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dbe63264e1ed1c4f3e5e806897b787c7e5d70a66666a164214f314edacd021`  
		Last Modified: Tue, 17 Feb 2026 21:31:03 GMT  
		Size: 105.6 MB (105601575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3f84333d023de739abbd5700103a0cb9bfc6f3c3ca019a07b45f1fc73504e`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 367.7 KB (367679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d5eb6309d46d62dfb27dc6f4e5b31f76a785a45edfbf560aee4d5e5091e72b`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f253acc6e2219780d32daada961d2c5b2592e94cd1719fad650ff143dd9205c`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 26.9 MB (26929636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543423e6e5a3857ebd4d024734955f3cd9173641862eb322c5814b2c0be13123`  
		Last Modified: Tue, 17 Feb 2026 21:56:35 GMT  
		Size: 698.6 MB (698618251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1d6711c83675114e2c338a45cbd68677708091daf2771ecebc3d9d567a8384f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec08d47ed0590f71a05f40fb9642dad349315c629d295f376155aa1cc771d3d9`

```dockerfile
```

-	Layers:
	-	`sha256:92fcc244968d9640cc62bf6f1c73a151d0cd304ae35b8fa810f8ab20f2b52bed`  
		Last Modified: Tue, 17 Feb 2026 21:56:23 GMT  
		Size: 61.7 MB (61726132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207c8407681709a69a1163579d31df40ed4f1f3cf3c448aac2cb404be63c1239`  
		Last Modified: Tue, 17 Feb 2026 21:56:21 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:0b43ca8bb2b1c618139b527fbc345e05024c7daa0b654bbf51a496a6a3ff15f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:ec7109087c5e59a4cfbf1ca8aef22c0a20e5b26ea06c1bc665695fa2396e67b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311776265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4be1fea49cd0e8e0285a854bd5de7270ef475881253ef9d8bd09029876cb77c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ef68b8c806cd8e903009ab4882feb9e9ea56176b99719ea0e3c7ebbfac1f4`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 110.2 MB (110188830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60572606e296b3d090dc856f0b55084a6e2d0ad69bbf5971816665902bb4bfb9`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 367.7 KB (367683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a46da188376f13cd0fa38e85a153c20688d45f128f8e0b541b3ac68cc23df`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a4e1fd4e992445106871cb0338c26eea2bf2558c4a42b33a7b9606ebc52b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:56 GMT  
		Size: 27.8 MB (27844723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:f6330a9672aefce6f5636e5d5ea0571abe0e95233c109a966b4ad1a0c5d94b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25637355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c436b9c719e9efb83e8d56860b98a13dc9cbe3516270ca528abca59e02d59f`

```dockerfile
```

-	Layers:
	-	`sha256:d9cc8355dd05b5855b535ebd9d724ef97e19c678ef84f57cc6740f444d7a48a5`  
		Last Modified: Tue, 17 Feb 2026 21:30:55 GMT  
		Size: 25.6 MB (25620991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa164f4d7ae83b6a4c224d7db8adf4552b29218daf00d021361ef916a662df0a`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4fdd7b5ed66b33350063a7fb066fb057275c668a72db872fe062fb83639f77f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299700892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bcf89f4996d8601126e407ccbd5081f913b2545c1e48d6e55de878aaa183d6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dbe63264e1ed1c4f3e5e806897b787c7e5d70a66666a164214f314edacd021`  
		Last Modified: Tue, 17 Feb 2026 21:31:03 GMT  
		Size: 105.6 MB (105601575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3f84333d023de739abbd5700103a0cb9bfc6f3c3ca019a07b45f1fc73504e`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 367.7 KB (367679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d5eb6309d46d62dfb27dc6f4e5b31f76a785a45edfbf560aee4d5e5091e72b`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f253acc6e2219780d32daada961d2c5b2592e94cd1719fad650ff143dd9205c`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 26.9 MB (26929636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:7dd40f7f6feaa0f035cbe9c7a9773bf1320d68764d5703fa30754dccc21ae87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25659947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074f694a516f67301a8f73e90ffc609df3070a55ed8dcfcc95f95fabe9692fd8`

```dockerfile
```

-	Layers:
	-	`sha256:9361dce8b643dcdb0f9e2a00abf93bd8770c467f83280781acca62a0d3f76702`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 25.6 MB (25643445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6a1c50a9e6a7cb079ca09d9e038bfac24f8052ec8de6ca371c4c42dc313ea4f`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:0b43ca8bb2b1c618139b527fbc345e05024c7daa0b654bbf51a496a6a3ff15f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:ec7109087c5e59a4cfbf1ca8aef22c0a20e5b26ea06c1bc665695fa2396e67b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311776265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4be1fea49cd0e8e0285a854bd5de7270ef475881253ef9d8bd09029876cb77c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ef68b8c806cd8e903009ab4882feb9e9ea56176b99719ea0e3c7ebbfac1f4`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 110.2 MB (110188830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60572606e296b3d090dc856f0b55084a6e2d0ad69bbf5971816665902bb4bfb9`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 367.7 KB (367683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a46da188376f13cd0fa38e85a153c20688d45f128f8e0b541b3ac68cc23df`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a4e1fd4e992445106871cb0338c26eea2bf2558c4a42b33a7b9606ebc52b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:56 GMT  
		Size: 27.8 MB (27844723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f6330a9672aefce6f5636e5d5ea0571abe0e95233c109a966b4ad1a0c5d94b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25637355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c436b9c719e9efb83e8d56860b98a13dc9cbe3516270ca528abca59e02d59f`

```dockerfile
```

-	Layers:
	-	`sha256:d9cc8355dd05b5855b535ebd9d724ef97e19c678ef84f57cc6740f444d7a48a5`  
		Last Modified: Tue, 17 Feb 2026 21:30:55 GMT  
		Size: 25.6 MB (25620991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa164f4d7ae83b6a4c224d7db8adf4552b29218daf00d021361ef916a662df0a`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4fdd7b5ed66b33350063a7fb066fb057275c668a72db872fe062fb83639f77f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299700892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bcf89f4996d8601126e407ccbd5081f913b2545c1e48d6e55de878aaa183d6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dbe63264e1ed1c4f3e5e806897b787c7e5d70a66666a164214f314edacd021`  
		Last Modified: Tue, 17 Feb 2026 21:31:03 GMT  
		Size: 105.6 MB (105601575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3f84333d023de739abbd5700103a0cb9bfc6f3c3ca019a07b45f1fc73504e`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 367.7 KB (367679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d5eb6309d46d62dfb27dc6f4e5b31f76a785a45edfbf560aee4d5e5091e72b`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f253acc6e2219780d32daada961d2c5b2592e94cd1719fad650ff143dd9205c`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 26.9 MB (26929636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7dd40f7f6feaa0f035cbe9c7a9773bf1320d68764d5703fa30754dccc21ae87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25659947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074f694a516f67301a8f73e90ffc609df3070a55ed8dcfcc95f95fabe9692fd8`

```dockerfile
```

-	Layers:
	-	`sha256:9361dce8b643dcdb0f9e2a00abf93bd8770c467f83280781acca62a0d3f76702`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 25.6 MB (25643445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6a1c50a9e6a7cb079ca09d9e038bfac24f8052ec8de6ca371c4c42dc313ea4f`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:90a7231938e53e367080f47c9ce6a3fb3e7e8a5c02eb64e5f4f9cb615eae4801
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:716004ebca998e69176b8c2f6c399320e452cac8144b5f03e13eb12cea2cb9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173372512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17a5c05fc884214d502b2048f1a86b8504d233c5b1bc1d4f1f171fde2158614`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:60f41e275d1480fa60827ad6386e173c23e666a2fbf650abdcc115b6572a5efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19415119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dba9d087660dd3f9b505be497048d6f29b0fcda8bcad68dc7327955773c3de7`

```dockerfile
```

-	Layers:
	-	`sha256:caeddb8e57cc56e0080db6c3aa098ecdeddc992332f965223590a8ac42fc14af`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 19.4 MB (19400498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f411a45a2d55c6121d3858126942fc12db430ab74262b3b35f1a04b2c41119d`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:26c36bae9cf9c9576fa8f4e10cbba12fca9dd921b4300745875b770e4d3efd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166799503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b596d417c1846bdb71037d2b4b533197845800ee50318d1ddff0e2df78c111`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:7c6c8e2197c18e7e40ac3fbada7b38bc28e86725c789738e2b4592d820853c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19389449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3325a8af056f02534bf06ab7b41cad8c585df26b869af0196236dab648cf940d`

```dockerfile
```

-	Layers:
	-	`sha256:1a782685011acb4d3409906f1a6f6c4b4cfed78eaea29a4bcb4044c988ab14f9`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 19.4 MB (19374702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8007784bbce4ff567142be2f49680b9e157ee1534c04bd1f3961cb4bc946d87d`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:90a7231938e53e367080f47c9ce6a3fb3e7e8a5c02eb64e5f4f9cb615eae4801
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:716004ebca998e69176b8c2f6c399320e452cac8144b5f03e13eb12cea2cb9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173372512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17a5c05fc884214d502b2048f1a86b8504d233c5b1bc1d4f1f171fde2158614`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:60f41e275d1480fa60827ad6386e173c23e666a2fbf650abdcc115b6572a5efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19415119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dba9d087660dd3f9b505be497048d6f29b0fcda8bcad68dc7327955773c3de7`

```dockerfile
```

-	Layers:
	-	`sha256:caeddb8e57cc56e0080db6c3aa098ecdeddc992332f965223590a8ac42fc14af`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 19.4 MB (19400498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f411a45a2d55c6121d3858126942fc12db430ab74262b3b35f1a04b2c41119d`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 14.6 KB (14621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:26c36bae9cf9c9576fa8f4e10cbba12fca9dd921b4300745875b770e4d3efd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166799503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b596d417c1846bdb71037d2b4b533197845800ee50318d1ddff0e2df78c111`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7c6c8e2197c18e7e40ac3fbada7b38bc28e86725c789738e2b4592d820853c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19389449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3325a8af056f02534bf06ab7b41cad8c585df26b869af0196236dab648cf940d`

```dockerfile
```

-	Layers:
	-	`sha256:1a782685011acb4d3409906f1a6f6c4b4cfed78eaea29a4bcb4044c988ab14f9`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 19.4 MB (19374702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8007784bbce4ff567142be2f49680b9e157ee1534c04bd1f3961cb4bc946d87d`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 14.7 KB (14747 bytes)  
		MIME: application/vnd.in-toto+json
