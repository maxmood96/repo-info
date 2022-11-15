## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:4dffb51fe745dc708ef5407b8140f974f4529c60ad913b0b20ce7be0755fcf6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:6d3fa1e52d72f2aac6b3c1826851bdb6f90ed09ca3de75193011b27bba91a1c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.6 MB (484586435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446f46aefa1703d9998d518113860d4b021674eaab91d1cac01a7b6f8cbf7d05`
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
# Tue, 15 Nov 2022 14:11:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:11:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 15 Nov 2022 14:11:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:12:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:01f31d494c64a80d7def3cfd48da2a51be60eece07dd4e1e3e5610b4d7010478`  
		Last Modified: Tue, 15 Nov 2022 14:18:11 GMT  
		Size: 86.6 MB (86584973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85acc3837ea20ae7ab209c27727e989114bdddabf07c2d35414e82256ad4f785`  
		Last Modified: Tue, 15 Nov 2022 14:17:59 GMT  
		Size: 328.1 KB (328123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a668996e7d023b897fe956d678fbf3f0c0d5044f4418a2ca81cbef8d33120734`  
		Last Modified: Tue, 15 Nov 2022 14:18:10 GMT  
		Size: 76.0 MB (75977768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3647ddcb7b7cca26b8abd4c96e174ed1fcaf9e7072eb7e3e58c6bd94ef00c82a`  
		Last Modified: Tue, 15 Nov 2022 14:18:26 GMT  
		Size: 21.2 MB (21150980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6f306e83d45a83ae93754835c3eec4ef2457c3c74a656d18b08e2a6153ca04ad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.1 MB (424121361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550c834ac3286574f74c3276903dbd1035ba34279beb2948f5e8ce36b56f06a3`
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
# Tue, 15 Nov 2022 11:03:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:03:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 15 Nov 2022 11:03:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 11:04:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:cfa787bdebdd6e7b0820bb59f70b63ad6b222698c18f8d4208b31ee8f12f781b`  
		Last Modified: Tue, 15 Nov 2022 11:10:34 GMT  
		Size: 84.4 MB (84371231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cd46bf0af5382b66346d8967c0d9de11e028d2ce44b491452432b6375130e2`  
		Last Modified: Tue, 15 Nov 2022 11:10:25 GMT  
		Size: 328.1 KB (328125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3658fda8fc78decc2782203a4a0a9905242d6c87dee1c0526a27dd719748b7`  
		Last Modified: Tue, 15 Nov 2022 11:10:33 GMT  
		Size: 74.1 MB (74089671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b20af995e6bd2a2e18ead3083d8bfcf90d71f630f10c06d1da58fabd959e54d`  
		Last Modified: Tue, 15 Nov 2022 11:10:43 GMT  
		Size: 20.8 MB (20812511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
