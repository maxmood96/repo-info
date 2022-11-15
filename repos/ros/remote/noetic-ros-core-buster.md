## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:9045252f47d753b9c47a51705a8fc37dfecff1a9a1dd381d1b0b82f28f76755e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:8b3fb34c9d4df88d9042412d63874e2ae0fe54ec178a8008c4ec4ddc6486a8c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300544591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c29052fbf7fa34dfacad78c4fdc8353c75a7a67398e94d107a429525479a76e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:03 GMT
ADD file:96ca7e18b6141668321140f8ae1a496641f631313035513f1f9314e9dad2cd71 in / 
# Tue, 15 Nov 2022 04:05:04 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:09:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:09:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 15 Nov 2022 14:09:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 15 Nov 2022 14:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 14:09:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 15 Nov 2022 14:09:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 15 Nov 2022 14:10:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:10:38 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 15 Nov 2022 14:10:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 15 Nov 2022 14:10:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2730d739afad9b8ff3e3029e23fd69d9533603751d6e42053ce0068c2b58e258`  
		Last Modified: Tue, 15 Nov 2022 04:09:05 GMT  
		Size: 50.4 MB (50448823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050e80b3f85a5310349e1ba47f11fe807f2c447d5358f6207db81eb48fb2b5e1`  
		Last Modified: Tue, 15 Nov 2022 14:17:21 GMT  
		Size: 10.9 MB (10896874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d8bcd08342a708663e781db1d732df0583ec7e20a6545afe34e2db45c681f3`  
		Last Modified: Tue, 15 Nov 2022 14:17:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6992da17af56fed0afceb107f48e33fb328ce20f2c086147f7025f9db0333d9e`  
		Last Modified: Tue, 15 Nov 2022 14:17:19 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21027d057c2994560e78eb41d5b87a4472dbd12f943e76faa7c63fd554351677`  
		Last Modified: Tue, 15 Nov 2022 14:17:52 GMT  
		Size: 239.2 MB (239196483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11a9ed5ead225330619570c47bef0fb905868ad736d096e89862a1d2b514a4f`  
		Last Modified: Tue, 15 Nov 2022 14:17:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ea0e03de4581586ce6d534f9e6fc2c2bf8e50a50168b9b0afb57d3fbe4f7582d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244519823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65702135bd10e5f317ce9f171437335f2de36dbf8ab6a4ba4da9465bdefaaffa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:26 GMT
ADD file:2122642b8ad9a333f73cba41ff9cc829542740e0e3c88379a7c9511fbfc28991 in / 
# Tue, 15 Nov 2022 01:41:27 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 11:01:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:01:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 15 Nov 2022 11:01:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 15 Nov 2022 11:01:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Nov 2022 11:01:16 GMT
ENV LC_ALL=C.UTF-8
# Tue, 15 Nov 2022 11:01:16 GMT
ENV ROS_DISTRO=noetic
# Tue, 15 Nov 2022 11:02:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:02:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 15 Nov 2022 11:02:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 15 Nov 2022 11:02:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:34983cc1fd1c67f0d8b7b8b4320539206a1c098388b3a671abe88b45f157978d`  
		Last Modified: Tue, 15 Nov 2022 01:44:52 GMT  
		Size: 49.2 MB (49233786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0d6aa77dc7e3e6cb404ca839ffe05429dc865c6f53f61d199627cddc197c0a`  
		Last Modified: Tue, 15 Nov 2022 11:09:47 GMT  
		Size: 10.9 MB (10902568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3955f704bc1936a82d8f59acffc7b268f5b37cb949b1eae1f51ddb2efb63f8c9`  
		Last Modified: Tue, 15 Nov 2022 11:09:46 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eb3e975face0a771cbbe4d7fcbaecd10a64dc2553cc0d0d405eabcd005d5a8`  
		Last Modified: Tue, 15 Nov 2022 11:09:46 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec0a529ecc45627e8b17f5c8845fa00a9cca8cd87cfa9629ee2b23196501416`  
		Last Modified: Tue, 15 Nov 2022 11:10:09 GMT  
		Size: 184.4 MB (184381056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b039cb484dc03fe448fd378fdeeb38fa7aed48361105571b0a99aa20163544cb`  
		Last Modified: Tue, 15 Nov 2022 11:09:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
