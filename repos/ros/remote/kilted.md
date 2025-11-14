## `ros:kilted`

```console
$ docker pull ros@sha256:300c9505e7261fc80d1aa75c3b1b4beabad4223329ff9d9cd41f608f794df243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:0cc6b0e7d3502ad36eeefc5143505caa15c34cc9f5ab554738732a25b0d917f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311030510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b55dbd0930b08c6f1b091089737b918a73cd9b17a8d0e6d2780cce35b15bf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:29 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:12 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:12 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62007cb49257843537b65b3bbdaf707b5871ef64f1a8d5ed321d27dac19d02`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e40102df5f4419def75c9186767f570a74c4747b6d7e81669cc29088c7222`  
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 6.7 MB (6747201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd34bf896a216fb9c6b14fe4ac3803f1e2afb1d1c98d8ccc3d91489412240a`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaee011da6a6650de0f4b7abc9f61851fd0dfc6024cfb11d719090268e7989f`  
		Last Modified: Fri, 14 Nov 2025 00:35:13 GMT  
		Size: 135.2 MB (135165768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e366a6fb86992b7af714641a40bf051564a320cfaf8b988422ba0e42f4bd3d`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a4e021e34b75541412ae13991b850429c96b37058e0ea0593a8054baa92b8f`  
		Last Modified: Fri, 14 Nov 2025 00:36:56 GMT  
		Size: 110.2 MB (110186847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a28696bceb573929b846fccce0b0969f5c4895a6399aa0a140f077150895ec`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 367.3 KB (367255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6cc1cb612143c0ae175d482eaefa05a4d8a991248cc187e6931dd06fd9a71`  
		Last Modified: Fri, 14 Nov 2025 00:36:45 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2248883bff98c826dcb62fb2d8cfaf9fa9ee71d51c7e596727a6a6de8c6862`  
		Last Modified: Fri, 14 Nov 2025 00:36:49 GMT  
		Size: 28.1 MB (28058037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:0c96703cc6405f14d42e6348a531553c713f4c179dda4974ad64c2f60aeafd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24666681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64817ffa8ae718817fbbf00fb0576b8bc53dff162855c53d975b2f3bbb98c32`

```dockerfile
```

-	Layers:
	-	`sha256:5709b9ba52bdf82559bb29618ebccf96f4b01358b316409e5f9d82a413f91448`  
		Last Modified: Fri, 14 Nov 2025 02:18:35 GMT  
		Size: 24.7 MB (24650335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7692c8f6f42bdae33ec2302b3a1c6c86524cf78aede683f6edfb91f5b09a8d75`  
		Last Modified: Fri, 14 Nov 2025 02:18:36 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dfc7ec8e8eb439842ca4bcd2f56faa2d0d9b62accad6d220a0985288dc119db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299376599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1899ee8dff90370a8507bd0b1f9315f5203e2085e259642ff4e929efa5246cd4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:05 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:37:08 GMT
ENV ROS_DISTRO=kilted
# Thu, 13 Nov 2025 23:37:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:37:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:37:08 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661353d5f4097e42530a69d350b138e88a8addec8ba83da6b0f3acce5a4e1235`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 684.0 KB (684026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1acf785e35e1a9733e34531c124aa9ebbdcda63ac72b4d62e89864b4c738ca`  
		Last Modified: Thu, 13 Nov 2025 23:37:46 GMT  
		Size: 6.8 MB (6759920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba7305aa8cec1e9406f89ddbb1f21280e1d2946b47a2d3c2507740910d1626`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 94.2 KB (94198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae8b0d26ce5b36ff47c6396ea460b2f6b7cb43df672d73e91bc3afe89e26804`  
		Last Modified: Fri, 14 Nov 2025 00:35:55 GMT  
		Size: 129.9 MB (129870285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771e1781c499b7fc410a0948f7f40193819962442023563122b2b4836c59df3`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6400fae56d55a701bf336c144e30bdab0e937f7ee2fac429a0e071ec3d916258`  
		Last Modified: Fri, 14 Nov 2025 00:37:47 GMT  
		Size: 105.6 MB (105596209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0179176f3b98962ff26121739ccba062dad541b523250a03d9c98633f231ec30`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 367.3 KB (367259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842e1008365173c3b93bee5a8c2e24edbf2bfaf545b95122988b4575a17ca003`  
		Last Modified: Fri, 14 Nov 2025 00:37:31 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f2da56ff148e913010cd349895433f4273f727e8e78c53b3c37891b2581e09`  
		Last Modified: Fri, 14 Nov 2025 00:37:33 GMT  
		Size: 27.1 MB (27140034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:d1f76759f0ac3ca705dcc4a37e8c233beb36ac6917e0bc2ef1eba4bcf07871e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24689079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a76dd5e9d7e6883d644c5b0b55de743605a2cf961ccac1deb7217ade910f6`

```dockerfile
```

-	Layers:
	-	`sha256:c9e538338867200639c593c1d6b3397b23eae1eddaea021ddeab641705c00a5d`  
		Last Modified: Fri, 14 Nov 2025 02:18:59 GMT  
		Size: 24.7 MB (24672596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e91de0fa134b2151a75b51f9e4355bbf5e8746ee15d6a76f7bb13ef422a45bfb`  
		Last Modified: Fri, 14 Nov 2025 02:19:00 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
