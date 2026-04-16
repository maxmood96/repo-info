## `ros:latest`

```console
$ docker pull ros@sha256:e9b9b98c1a867673789dfa1cb622b780e1ae6e5a0c235b0340d83c2b46f6171c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:d1488d3b99ecd0edaec8349682bc1eadf11bc5b4dc266b3eaaeda8787a724cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296302721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277f4249e792af1be98e76d5e3b71faa7086aaeb9f5a90e902c9461a6ac3e673`
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

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:1dccc7efac09ea940614476c7a5b547d0ef600abe39ff4f2836923babfcd25ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24817696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0d92dd7d19f29c32c1ea2755842da2a2ab1183a28da09c0b6be052ca7097b7`

```dockerfile
```

-	Layers:
	-	`sha256:d6e28e9d8dc85665aed292205faba4faf500071be01e8d54146d31de77320601`  
		Last Modified: Wed, 15 Apr 2026 21:46:55 GMT  
		Size: 24.8 MB (24801075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161d4f87e7b6311a1d2e9ab5aec66c322fd54084eb76940be809f7203137a561`  
		Last Modified: Wed, 15 Apr 2026 21:46:53 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:75f904e512850c074a09b2fcad02f42496358ddedb14b0fb2844b2d063b67f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284743559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed588b014ed59b43c6e00b7ee5394c98c3119afdba85eff2e4e21702aa9ba296`
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

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:2842848376e0b5ae10b35caa0c4bd0f000c55c92fa8ad83d98caa6e544e4ee02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24840114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bed213097eed21c0c47f4129b1dccd0b3629c656c299a11fbb8324b0ccba2`

```dockerfile
```

-	Layers:
	-	`sha256:27fbf0cacc0c47420fa070f1a46d1c49be69a3b5d6cbba50e355ee22c06e4031`  
		Last Modified: Wed, 15 Apr 2026 21:59:30 GMT  
		Size: 24.8 MB (24823344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7348e7326134d81c2a173b26a0de6babefbb17960b8fedb1bf5b857964d25364`  
		Last Modified: Wed, 15 Apr 2026 21:59:28 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json
