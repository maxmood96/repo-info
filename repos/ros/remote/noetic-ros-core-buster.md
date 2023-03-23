## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:921d7f306bcbbc10e3c70a4add3d5085eaa9616654c7cf35484cc71078ac018f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:7785269a093c90620b0dd7d1f33e681c451d7533ccf299ec651e41a0031b80bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300588636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1146a51e430cec8a22d8d8ad7332fc4e618b36b40ab651202f07f910aa0b4fa5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:09 GMT
ADD file:9ea7d74fdfdb29946ab72e1aea5810331debe27db7e50a0fc4e0d5a192ab6166 in / 
# Wed, 01 Mar 2023 04:10:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 17:01:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 17:01:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 01 Mar 2023 17:01:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 01 Mar 2023 17:01:13 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 17:01:13 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Mar 2023 17:01:13 GMT
ENV ROS_DISTRO=noetic
# Wed, 01 Mar 2023 17:02:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 17:02:40 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 01 Mar 2023 17:02:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Mar 2023 17:02:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d8a6bce2a40cb0c3e3cc6646bfeccfb2ac5b303c39ea70d67e30406d270f2009`  
		Last Modified: Wed, 01 Mar 2023 04:14:42 GMT  
		Size: 50.4 MB (50449101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a1ffc835f48ecec7c683701866277b285e39a42777bb6819d705ba54c9b7ee`  
		Last Modified: Wed, 01 Mar 2023 17:09:08 GMT  
		Size: 10.9 MB (10896984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ab4ec3b1ff1518ff16c31e9e4f4b239089fdad9819bb1b0806733d42d30b73`  
		Last Modified: Wed, 01 Mar 2023 17:09:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9841b85e22a255629ec6b026e828d764cdc3c990de2d2c70eef2cfa655083074`  
		Last Modified: Wed, 01 Mar 2023 17:09:06 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fcea5877730e4a516a82878a4f5f98da043bd4cc6f242e907c49f88c966f58`  
		Last Modified: Wed, 01 Mar 2023 17:09:38 GMT  
		Size: 239.2 MB (239240139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e461f854cd1f5763471d57c32aadc9f1bf067ff5b25408ead48199dee31c5f5`  
		Last Modified: Wed, 01 Mar 2023 17:09:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6733f50bf49e5ebc9e9b2f05c47cc1519731c45ea16caab58e3aa86b4ab33462
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244569690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d60ce06228047cd37fd09ec239c06f2453b0b8a8646191bc9812abaf869293f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:16 GMT
ADD file:35dd833b036748f887e8224e9c5f09846aa5d1d6e1798d12a6355c28e0a087d3 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:33:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:33:58 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 23 Mar 2023 13:33:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 23 Mar 2023 13:33:59 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 13:33:59 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 Mar 2023 13:33:59 GMT
ENV ROS_DISTRO=noetic
# Thu, 23 Mar 2023 13:35:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:35:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 23 Mar 2023 13:35:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 Mar 2023 13:35:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6a9fffb8d1cb480140dc56a24c58a5d1a284109cd8a640a3719bcda5963d1298`  
		Last Modified: Thu, 23 Mar 2023 00:48:25 GMT  
		Size: 49.2 MB (49239721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b91b6ee30b4f087c1ea96a05e201aa3276826cf050c362f762e574ea8d86196`  
		Last Modified: Thu, 23 Mar 2023 13:41:47 GMT  
		Size: 10.9 MB (10902622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d333b25ec98b602feadfb03e74536f86cb100c88c3ae41708f4f69207cbe5ea`  
		Last Modified: Thu, 23 Mar 2023 13:41:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898783a42a69a03c055068412e53662687477c3f7dd14e4799ce9b2e7ad2e20c`  
		Last Modified: Thu, 23 Mar 2023 13:41:46 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315cb2c48234779972c6290c195d46ff35df3ccfa9bd8fd99f77ea76c46012e1`  
		Last Modified: Thu, 23 Mar 2023 13:42:07 GMT  
		Size: 184.4 MB (184424937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b25a7c52da25a6ef93080a6fe8585d11832b187dce74bd60fed4d5a82e2d8d4`  
		Last Modified: Thu, 23 Mar 2023 13:41:46 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
