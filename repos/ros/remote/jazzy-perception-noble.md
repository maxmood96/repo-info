## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:29a62aed6ef63bdaddf44cfc1b7450c46019c5115b143b6a43ef60e0bbadcbf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:785e3523795c0adcd9589c3ec81ffdb5633748c103699c9a7378e1c5554bdb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080858776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4010bcc04ec130643e20154991f087f2f8c339e1055086f971ea5b59ec137ab6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:56 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 20:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:56 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b14e46a263d7cfdea10cbfd77ad3253ba8910fafc9efd5cf753ea214f6d1d`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 684.0 KB (683959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5712b646304bae8bead154f8d5e373aac7c2db78d8204e423399b1eeb38e7feb`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 6.8 MB (6751699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c4ee959ad90d19586a8d7df5142a3e3df16d13d4135f9ad5fd9b00038b79ad`  
		Last Modified: Wed, 15 Apr 2026 20:55:24 GMT  
		Size: 94.1 KB (94094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2bbede12e25d080e6b1da939f670831419a81b0de8726867bc9c9f36b201d`  
		Last Modified: Wed, 15 Apr 2026 20:55:28 GMT  
		Size: 120.2 MB (120185821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf704656fe97b1dcd450fb82c1bf317e92674e5a79f884d454181e341bc859ba`  
		Last Modified: Wed, 15 Apr 2026 20:55:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb934869c0062075d3924ee67ff17ece2c114ca0ce2144abe6c484a11464706b`  
		Last Modified: Wed, 15 Apr 2026 21:46:57 GMT  
		Size: 110.2 MB (110191800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41de78adfb4b31cd70fec97b302a53039d85ae134cb88b28504b1a8f234d3f6a`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 406.0 KB (406035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56562b7711ce2dc52c7a11d2b429e85a9c969d469ef5eaf0530876ced6355d92`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f238e0cbb8a4936a6230dd0b4e08a4fb91563787eabed4ed52c321cb254083f5`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 28.3 MB (28253633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3d5793cf19f8d8069608d8e87dae2c4eae72e0c890187a944c2510d753d95f`  
		Last Modified: Wed, 15 Apr 2026 22:32:23 GMT  
		Size: 784.6 MB (784556055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a14355e57eed7747efa4f7048777789883e9893fca6321961d3b9521411e1bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60978187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eeaf2eb2d7a04518afbc17d34f110e4d13c0b6b246d83236b2638001ac67be`

```dockerfile
```

-	Layers:
	-	`sha256:70b10207c8104daa621e4757e764b3f8db982ed8c5d169aedbfee21fb5d8a296`  
		Last Modified: Wed, 15 Apr 2026 22:32:04 GMT  
		Size: 61.0 MB (60968849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be47fcbe8309e1f93ff259c93f02e67d6828ade5651dcc478961db45df8c258e`  
		Last Modified: Wed, 15 Apr 2026 22:32:01 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4b857ae12a8171bcfd6a9edb975fe5c9cec9b2b052cceb3847d376b03c514b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.5 MB (983486943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a122d53d86c230c37fc5f21fdafe09fef6c6c994591a2e322ad29f7407c935c8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:38 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:22 GMT
ENV ROS_DISTRO=jazzy
# Wed, 15 Apr 2026 21:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:22 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e530260cc5f592f7e8b33d25b40c28a66919cea3ada42810e38129f3d03821`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 684.2 KB (684192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd1512c538a0728692bd9bf2a089c9cb0246480616fe1b5f722a9650cfd57d6`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 6.8 MB (6765057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a45732ac51762c5a6976f61c21b88660dc6186ddf65169a122095add10dd22`  
		Last Modified: Wed, 15 Apr 2026 21:02:51 GMT  
		Size: 94.3 KB (94299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5644c4503b02ae0755384bfbf2fcdf94322388105e752b98890d3d3b8d285e45`  
		Last Modified: Wed, 15 Apr 2026 21:02:54 GMT  
		Size: 115.0 MB (114967994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aba794b199825528eae9c19c737ac2698f977a7fb55d8511d7aa8f01878b15`  
		Last Modified: Wed, 15 Apr 2026 21:02:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b1652e06603234b577f2609a4675b0d8db5ae2bc8e9a76c212aa8372ec83b`  
		Last Modified: Wed, 15 Apr 2026 21:59:32 GMT  
		Size: 105.6 MB (105603863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b1a61548270d1f294994d9d5c6b7ef600aa93cf0406dd697efd56a47fcaeef`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 406.0 KB (406033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab229f387e85cf75d9d2c2b9a816695857692067ddf66c147963519b872f6edd`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9fea2d7bdf03859ee3389c8beb5c8fa13ae0d91f3d7eb8ea185f0dcb5cbda`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 27.3 MB (27343654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66526070dc88a16887fa155319e571a0bd7f8c249066944c0ec2e53646e2ff5e`  
		Last Modified: Wed, 15 Apr 2026 22:40:53 GMT  
		Size: 698.7 MB (698743384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e764d6b3e596e57a32f2910bd5cbe3e4e850138462742ff450f4889ab34e782b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60908783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9904456d1e64c4c85290a928980388d58140c41fa568c08a6f04ad7d4830d5dd`

```dockerfile
```

-	Layers:
	-	`sha256:047888e96168e6a93962e56186aa92edaea683addd34711e5d87b0d8a6abf88f`  
		Last Modified: Wed, 15 Apr 2026 22:40:39 GMT  
		Size: 60.9 MB (60899365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f564481ff937fbb44528eb5f3e2847c8f77ebbb3b7bfcc2814a8465e25883310`  
		Last Modified: Wed, 15 Apr 2026 22:40:36 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.in-toto+json
