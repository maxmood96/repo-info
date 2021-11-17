## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:536a7cc159838758a8e7fdf820c740e4d412235df62f3ba4b65bc8e4098bbdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:1cfa864fcdb3733b854fcb2bc2d474a1727099f22e78fd57b90fad7130b52db6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300418498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480154696b7d95f4e24afb577c43ef157189e425d7b5c53d6563ebe1c6c060f8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:51 GMT
ADD file:cb5ed7070880d4c0177fbe6dd278adb7926e38cd73e6abd582fd8d67e4bbf06c in / 
# Wed, 17 Nov 2021 02:20:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 22:36:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:36:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 17 Nov 2021 22:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 17 Nov 2021 22:36:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 22:36:28 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Nov 2021 22:36:29 GMT
ENV ROS_DISTRO=noetic
# Wed, 17 Nov 2021 22:37:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:37:37 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 17 Nov 2021 22:37:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Nov 2021 22:37:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1230f17f526cb07307d41462355b10488b994e8bdafe0d8f275a405fa3b33831`  
		Last Modified: Wed, 17 Nov 2021 02:26:06 GMT  
		Size: 50.4 MB (50437098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f64a2cee9a8973db7ffaff43c62f68f0db43144b718c8339856ff2d039b430`  
		Last Modified: Wed, 17 Nov 2021 22:43:20 GMT  
		Size: 10.9 MB (10891910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d367fa9b39ce393432a2a974cff50cc6c0a295b0c00a6a71152b947621dfd2`  
		Last Modified: Wed, 17 Nov 2021 22:43:18 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54972089aecf2d558033d5c01eb20f1a2fc64c872aca23ad9ab78f45f335f6e4`  
		Last Modified: Wed, 17 Nov 2021 22:43:18 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d68c1a3d9a31ff02e5ed0caf544e9e047643eeaa48073c11c2aff158e93739`  
		Last Modified: Wed, 17 Nov 2021 22:43:56 GMT  
		Size: 239.1 MB (239087074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb488c1f6198579f8b779a8d04bba2ad192ec739f12e0996b08295f67e238be`  
		Last Modified: Wed, 17 Nov 2021 22:43:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1d5d6bfb3b509cc14ffc23365eeae922fda11315d06f94f67d4f251a4c1cbc7a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244216114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336e2f75901b61589671bc6aa79e96c5fa7303c5eef2b6e609ec750f592a6673`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:55:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:55:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 17 Nov 2021 09:55:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 17 Nov 2021 09:55:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:55:40 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Nov 2021 09:55:41 GMT
ENV ROS_DISTRO=noetic
# Wed, 17 Nov 2021 09:57:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:57:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 17 Nov 2021 09:57:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Nov 2021 09:57:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e1e6c972c4d10ef0b28be7441b9faba756aef9d8502c13834239097e49`  
		Last Modified: Wed, 17 Nov 2021 10:05:24 GMT  
		Size: 10.7 MB (10688089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1a10d650dd3ccec5c33cb88fd591b4d3377d74b6bc192bfc5703c3377d2490`  
		Last Modified: Wed, 17 Nov 2021 10:05:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5555e0dff8030a1664f72dbd55c2ccb0f9643856a0543a792754ce07a9a295`  
		Last Modified: Wed, 17 Nov 2021 10:05:22 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aba732adf84216832ef6ac06de2d7a0f183d75a35f86164d76ad6c20b84e81d`  
		Last Modified: Wed, 17 Nov 2021 10:05:54 GMT  
		Size: 184.3 MB (184302665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77ffa64df86146e7a47c4de87957d94a0df3a134a9c3b631ac299b4ac79f716`  
		Last Modified: Wed, 17 Nov 2021 10:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
