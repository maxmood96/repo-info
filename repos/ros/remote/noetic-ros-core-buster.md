## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:33e9fda2cd23a5c8fddad5793a83210b4eabb2811acadb56918fa24bd410bcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:8d2f0348a63f0ddc9f687d6570ac8eccb535cba8432646e7003ce4663c60710c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300556419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92706ca0936b04151dc9fa4d6227a049abbbd804d0d6e815430735d326da6311`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:33 GMT
ADD file:dc52371b5f4608e5887e8c657ff951d1895e0047960f44b153c4a55ebf1726d5 in / 
# Thu, 09 Feb 2023 03:20:33 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 11:02:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:02:10 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 09 Feb 2023 11:02:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 09 Feb 2023 11:02:12 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 11:02:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 09 Feb 2023 11:02:12 GMT
ENV ROS_DISTRO=noetic
# Thu, 09 Feb 2023 11:03:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 11:03:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 09 Feb 2023 11:03:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 09 Feb 2023 11:03:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b2404786f3febb4866f85b0c8f52b0b0b94dfdb6543e94cd65f961c68f325ff7`  
		Last Modified: Thu, 09 Feb 2023 03:25:32 GMT  
		Size: 50.4 MB (50449613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb999b8f3a9c7e636ecfd923eab21dab4ad56a6e3e310ae695a43fd62c15d1e6`  
		Last Modified: Thu, 09 Feb 2023 11:09:45 GMT  
		Size: 10.9 MB (10897059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd0c17feddc0d5789db91293690ac182ed96538d0ded0ccd2d0f5f469cdee78`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bffc213c160645ebd9d58dae23404a6674a1d8406053e9df8404ea590e0076a1`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c4103f7699bacf08762eca77b1ff9ec4d55eb718fe790240abc06fb3b16474`  
		Last Modified: Thu, 09 Feb 2023 11:10:16 GMT  
		Size: 239.2 MB (239207331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0d003a8d1db0ecd1033580e9d3bbba3e32d9bb734b95c13e106d204b27065d`  
		Last Modified: Thu, 09 Feb 2023 11:09:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:55aed9d35e66b740bdf5d6a7ec786f7b1ccc2b86f82a298a18d07c98335a87a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244571461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa8fae09c5ca8a3e3ee00729f90344c724e58db573c46921dde685023ce1f8e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 12:29:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 12:29:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 01 Mar 2023 12:29:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 01 Mar 2023 12:29:13 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 12:29:13 GMT
ENV LC_ALL=C.UTF-8
# Wed, 01 Mar 2023 12:29:13 GMT
ENV ROS_DISTRO=noetic
# Wed, 01 Mar 2023 12:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 12:30:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 01 Mar 2023 12:30:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 01 Mar 2023 12:30:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a788fbcf95c26646fbabe7bb6f29416ca2663c0cfd87e1ccac361a7459568915`  
		Last Modified: Wed, 01 Mar 2023 12:37:20 GMT  
		Size: 10.9 MB (10902711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46d425485295faa6248cc3b6ce203089f5c51e6d6bd9ec2c65a3724f0986ba0`  
		Last Modified: Wed, 01 Mar 2023 12:37:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de7b8f0c8434b3ef1c87e53a130007029f5fd37ea81634299d1e8226d10b4d5`  
		Last Modified: Wed, 01 Mar 2023 12:37:19 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6b26d79f53cceae9c1d805e9d806a04c531a4290ef45b9f07bdc82202a1edd`  
		Last Modified: Wed, 01 Mar 2023 12:37:41 GMT  
		Size: 184.4 MB (184426336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e132bc958bc874cc517925ada16c2f3e782550fa85b319f3c4d921c3056fa77`  
		Last Modified: Wed, 01 Mar 2023 12:37:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
