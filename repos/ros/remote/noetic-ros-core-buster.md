## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:b7a1ab1e58bc0a701bcda78648f04290697fce9ddcc00affe8fd548b696e453c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:2a4b90935f4fc43465af808ac2fafe40d23ae53c5d942ae8c903ac2b6722a06a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300426658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784f655f06d9d4392b5f6143f4296c48f1b01585b8829d59e49d32b3b710845b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:37:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:37:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Mar 2022 10:37:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Mar 2022 10:38:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:38:59 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Mar 2022 10:38:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Mar 2022 10:38:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c133b370766b6f5552e000ccf033e32442276773c2cd08a21a0ac9f18259d3`  
		Last Modified: Wed, 02 Mar 2022 10:43:37 GMT  
		Size: 10.9 MB (10892098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ae26f65841562882d5b66361657c9e58e057d74f3ecdca875adcf248f594eb`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c03d38883523f98928ace45a667c9a6f9c1e357c09c22bc32e9f75e3ee391`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3c4ec48c4a1bce55afcd9bbda77e99d790164b04caa20748eb0bd7b2dd5ae`  
		Last Modified: Wed, 02 Mar 2022 10:44:10 GMT  
		Size: 239.1 MB (239095099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970c2b44800a0ec91c9c10e46c3e219d142dbbce8abf085f6c89e01de485a28a`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:808f91e96a8fdedd8e00b09fb21a9606925e79a42c523c6c9c67aea659f413e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244239449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd5db636ffd3810e1818d774de9be4bf18f548223425b48b7a14b73c4ce82b9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:57:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:57:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 18 Mar 2022 00:58:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 18 Mar 2022 00:58:40 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 00:58:41 GMT
ENV LC_ALL=C.UTF-8
# Fri, 18 Mar 2022 00:58:42 GMT
ENV ROS_DISTRO=noetic
# Fri, 18 Mar 2022 01:00:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 01:00:08 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 18 Mar 2022 01:00:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 18 Mar 2022 01:00:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cb989cba7dc1d50cf620a207810dfda41194cf7c3488cada787f5828ee2090`  
		Last Modified: Fri, 18 Mar 2022 01:24:22 GMT  
		Size: 10.7 MB (10688147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dc0d7ec12bfae1925877797eaff4b9a4ba48083fd8920a4ccff5b5dd0bb07e`  
		Last Modified: Fri, 18 Mar 2022 01:24:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eae995b77a571bfa585e4b04eb18f60b0cec5688a13afb5be92ba9e38eefe23`  
		Last Modified: Fri, 18 Mar 2022 01:24:21 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743fda29b26873c08cbc5f7efdb9b3a02f08b87dcfc7a69a0f8f684a88c92237`  
		Last Modified: Fri, 18 Mar 2022 01:24:53 GMT  
		Size: 184.3 MB (184325939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d63919ef43f47b1ff0002843cb0ab133ab048f94d0241d53d989f63971f26a`  
		Last Modified: Fri, 18 Mar 2022 01:24:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
