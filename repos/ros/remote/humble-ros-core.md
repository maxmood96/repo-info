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
