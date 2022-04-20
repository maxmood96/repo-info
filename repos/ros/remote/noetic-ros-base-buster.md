## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:e8d3f1b71626a3c53aeb5a67fdf9363f35dc897f7d36bff8133c8b29bad08e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:6b4406b04c3846197e0bd36ebd863516ccf681c16a0bee86361a33ef668549c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463345909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920dd0639d765b1780c742f8ab16fc2f50932373bfde99d3bb475d7b813f7067`
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
# Wed, 20 Apr 2022 17:38:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 17:39:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 20 Apr 2022 17:39:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:757a381d58433d12adbc8267c4306c48e05ceab27e9b7180e6ab5153115398a9`  
		Last Modified: Wed, 20 Apr 2022 17:43:51 GMT  
		Size: 86.6 MB (86566693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2d2e540aad82640f395c83b534034224c4743c463281a9308bcd39e755a9a5`  
		Last Modified: Wed, 20 Apr 2022 17:43:39 GMT  
		Size: 309.3 KB (309290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc64f783db31ecba0dea771f5c67d54898bd9e111176ecd00620deaa53fef6e`  
		Last Modified: Wed, 20 Apr 2022 17:43:49 GMT  
		Size: 76.0 MB (75976251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:93dbc8057d883b94580a8234ec329cda459fea35afe75515fb0f9a61d8be3e83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402814804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd23d08ebda2ecf5c0c0951aace97a48e98f0e7ff9ff80bc25cb84f4d52d6288`
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
# Wed, 20 Apr 2022 12:12:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 12:12:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 20 Apr 2022 12:13:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:dd36c64b99b0defab15ab0ce0f85dbf6fbab02bd969287c79becce5d9293059c`  
		Last Modified: Wed, 20 Apr 2022 12:19:38 GMT  
		Size: 84.4 MB (84352350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359920e3958bfbe6523bec5a0c24d8479e58e68ab41c3c437aa9806e83e776e`  
		Last Modified: Wed, 20 Apr 2022 12:19:27 GMT  
		Size: 309.2 KB (309235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e22341ca497d2ab03ede7e0d29948509d06168bfff83be501fc2c9fb1499be`  
		Last Modified: Wed, 20 Apr 2022 12:19:37 GMT  
		Size: 73.9 MB (73865013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
