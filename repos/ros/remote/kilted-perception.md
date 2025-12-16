## `ros:kilted-perception`

```console
$ docker pull ros@sha256:597eb7c1b6ef46d03c1306786771714cef4064d5654887ca996713712185a190
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:39acb6f9dbe66091f760eb26611744af06f98cc62d21a8ebb6e826ceea4ab104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1095999495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3065d8b3834d1c8b2fa54e8585dca47f3a383187ecf1ab1ad05190a0ea929`
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
# Fri, 14 Nov 2025 01:18:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
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
	-	`sha256:5fe6b475c9d5d0fec8f295a27b9c88c7e104854439857ec2508c68a04327c933`  
		Last Modified: Fri, 14 Nov 2025 05:51:37 GMT  
		Size: 785.0 MB (784968985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:49b431be399ca5fe716018c10a722888c1fa293c5be0710962d4a84c3257101b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60831768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3e84ea6271ee0ddf4c85b11145a84b6e7efe869fc8a1a05673e392f0ef2c1a`

```dockerfile
```

-	Layers:
	-	`sha256:4846b83d86f5b32056c650890347f732ff8a4c09aaad50f312de07d40693ab51`  
		Last Modified: Fri, 14 Nov 2025 05:18:06 GMT  
		Size: 60.8 MB (60822416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e11511c30e26ba831e3130603c6135fa399dce361debb54e7debc7755ac46e`  
		Last Modified: Fri, 14 Nov 2025 05:18:08 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d69e6b68fbf0b451f2d2916f8320507c33e47620dea9c9609ff663bb0e5bd47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.3 MB (994340523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67faf80aeacd3fac0059ebc1e8ab26ce58f1016a22fea364f281a5d6103c1f51`
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
# Fri, 14 Nov 2025 01:34:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
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
	-	`sha256:d9ec05d315c3cb7241734afa22b2b434a0e74d932c29d5d3e00d0d27e8b1a342`  
		Last Modified: Fri, 14 Nov 2025 06:02:24 GMT  
		Size: 695.0 MB (694963924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:03337ba5432546dcb0a55a48d697155319d747795cc06ec0447dcc510d22d2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60762373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760579d59a40d6d4b825b88fe7a6a01c47c48a4ac352b70eb03ac1622161c190`

```dockerfile
```

-	Layers:
	-	`sha256:d5dc70d9db7a43715963e98a03df7919d4e1749a716a4262a67bba890d0ce0e7`  
		Last Modified: Fri, 14 Nov 2025 05:19:34 GMT  
		Size: 60.8 MB (60752941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:813bbfb4e7dd5d9cfaffd99d1a7feba515a6390671be13bda5c0949e7effd486`  
		Last Modified: Fri, 14 Nov 2025 05:19:35 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
