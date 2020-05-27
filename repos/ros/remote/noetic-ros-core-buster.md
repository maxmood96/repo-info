## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:57394dee3e0149846c2a56c44ee1a5edd113b01c0b950841749e8715930d7c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:6dde1b447061f2d391dc4d3c35015cc7b738b8022c190f540ed26ff8012c7980
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300090627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4f1c4d8f1ec8f6bcf5274a05b812d11d67ad1f1321e5fb97980f6ab1a0250a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 06:28:12 GMT
ADD file:fb54c709daa205bf9d04eb3d90ba068db4c34dfe3b6ec0d7691f677286120903 in / 
# Fri, 15 May 2020 06:28:13 GMT
CMD ["bash"]
# Wed, 27 May 2020 01:32:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:32:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 01:32:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 01:32:34 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 01:32:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 01:32:35 GMT
ENV ROS_DISTRO=noetic
# Wed, 27 May 2020 01:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:33:44 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 01:33:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 01:33:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:376057ac6fa17f65688c56977118e2e764b27c348b3f70637fa829cd2a12b200`  
		Last Modified: Fri, 15 May 2020 06:37:20 GMT  
		Size: 50.4 MB (50391294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8414f05e9d7866ccb09d6c12bffe517dbed01796d379b94ff6b0770b033c5a6`  
		Last Modified: Wed, 27 May 2020 01:41:58 GMT  
		Size: 10.9 MB (10889343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516488eba09f3ee350bd860fcde1a77e8fded44cd0d73c1d38f31168c7fb2df2`  
		Last Modified: Wed, 27 May 2020 01:41:56 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0678db7e4fd2cd1e19b4e34680b821e27743d7cec864d22adcc09347221944f9`  
		Last Modified: Wed, 27 May 2020 01:41:56 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18958b3f6adbdd4706051abe00b90ba861588fa198287d6cb479f837d72bb8c`  
		Last Modified: Wed, 27 May 2020 01:42:46 GMT  
		Size: 238.8 MB (238808157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0dd0d7aa0f76d7ded8e0eb4b9326f5beee9a9995cf4e49d684260c7354e9d`  
		Last Modified: Wed, 27 May 2020 01:41:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f9d20f3ce48a74caa83c12d6b6a7b0d6d3663361acb344ff534d38994762652f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244087879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02f369acca718741956f3caa7cf43da505bbaba5307d911ea673b9038289267`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 12:43:21 GMT
ADD file:be06dd722febf4e72f7e626f70029986a5c75880941cabd553f695dd66bcbaff in / 
# Fri, 15 May 2020 12:43:25 GMT
CMD ["bash"]
# Wed, 27 May 2020 01:54:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:54:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 27 May 2020 01:54:10 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 27 May 2020 01:54:11 GMT
ENV LANG=C.UTF-8
# Wed, 27 May 2020 01:54:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 27 May 2020 01:54:12 GMT
ENV ROS_DISTRO=noetic
# Wed, 27 May 2020 01:56:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 27 May 2020 01:57:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 27 May 2020 01:57:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 27 May 2020 01:57:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d23bf71de5e1fea32788576972e233e80db7c51d831ed7edb269102dab298bf1`  
		Last Modified: Fri, 15 May 2020 12:53:11 GMT  
		Size: 49.2 MB (49170530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b60fb50c8ea31b54cc46f12ab0d1fd3e5e6cf82fd105f3b64b1a303923e8023`  
		Last Modified: Wed, 27 May 2020 02:13:36 GMT  
		Size: 10.9 MB (10881938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b57313e61481ab8ef41707267913409cffee22e3c38e776c2e1f4076fc851f0`  
		Last Modified: Wed, 27 May 2020 02:13:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021333177021b14f86a9cf17ea32c7ff93184c16151100ff28c7c73bfe4fb38e`  
		Last Modified: Wed, 27 May 2020 02:13:34 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813d2e881a112128213672f80539376dd9ffa7753c8bc65eafe0cbe873bfc4af`  
		Last Modified: Wed, 27 May 2020 02:14:32 GMT  
		Size: 184.0 MB (184033572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a700f415ed8b45c6e31d8a49b8752fafa2b475b3a48ad5d0a8373416f25fdc6d`  
		Last Modified: Wed, 27 May 2020 02:13:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
