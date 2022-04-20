## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:89d2d4a66f45461a687e24602ae35bce5ce102bccf86d41a7a1c9b6163cd6e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:84351d18f44271dd8a4ace0db9e9a7c7ffa02a108ff424b3abcd8b055312a296
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300493675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdddb757d3d82bc10e186b274307e6f5b72f5aeb6590ba010135f94263fd1881`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 17:37:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:37:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 17:37:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 17:37:26 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 17:38:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:38:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 17:38:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 17:38:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20546aaa06f50802eafdb39e7339d4cb6230c7a1aff32a53c46d1fcfed8f2dd5`  
		Last Modified: Wed, 20 Apr 2022 17:43:00 GMT  
		Size: 10.9 MB (10892097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abde7f24de9cf0bbb2249385441601015b239338b7901eae3402cb42a98c589`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afac4f8c5429cab550330c262feb633f708f9eda06ab0962fa784c88a9c3459a`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8609835955c8073fb8ee41d1c9ebb686c08c5a154f81dc42e1ee92614d6e430`  
		Last Modified: Wed, 20 Apr 2022 17:43:31 GMT  
		Size: 239.2 MB (239162184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb06026309bf4ee95de3a56281f392cddaad08a74c5056617cee6a3cbad0840`  
		Last Modified: Wed, 20 Apr 2022 17:42:58 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3a167a3e4a34b48fdac018fdb84126e3a9ea5c99e0a51cda3cfa472cba4e59aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244288206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d559d174d4ed076af61ea7fde4dca79121305b27a81c85da84fb2ed1dd24c426`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 12:10:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:10:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 20 Apr 2022 12:10:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 20 Apr 2022 12:10:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 12:10:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 20 Apr 2022 12:10:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 20 Apr 2022 12:11:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:11:39 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 20 Apr 2022 12:11:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 20 Apr 2022 12:11:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3957d218911547e664ee734939dc71ad089b29ed94b50f538786d667373e1ce5`  
		Last Modified: Wed, 20 Apr 2022 12:18:50 GMT  
		Size: 10.7 MB (10688204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2c217f5a5971a62fad5aac5564915eaf89c57b2110a7751a364f5a0de02dd7`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4a549feaf8502a671617c04bc2c2a084e6374b096bd615bebf4d2b3278be0a`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a05822887f56bc9d0b9364d7c755b5baee6c94b00f61dd5c41b4c2392919797`  
		Last Modified: Wed, 20 Apr 2022 12:19:19 GMT  
		Size: 184.4 MB (184369896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8501994f2ad5e8e01905fad8c5f1491a035971eab743a788c7208cf18255c4e`  
		Last Modified: Wed, 20 Apr 2022 12:18:49 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
