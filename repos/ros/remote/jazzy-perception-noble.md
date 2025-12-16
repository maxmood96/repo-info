## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:23ac13cf396221df5cd83dd0b636d920b23ed9b0651c25ba061c0881a90de458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:fdfa5ace8d17e58758391a86579b8e59eb8be21ce6461ae34311dc9854178342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080404531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f17afa977e9553bf8f9d364af72bbbc94a03684c231ebe65e75e3420c16111b`
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
# Thu, 13 Nov 2025 23:35:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:33 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:36:14 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:36:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:36:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:36:14 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:35:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:35:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:35:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:35:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:18:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7599b009ea097aa778e0d1ff97f7ab0dad2381f4e6348b7885090cd5544bcc29`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 683.9 KB (683894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a34f0fc738d411b401c35a9622d233b029551d8ab2d349b1e7f7dd0a97936`  
		Last Modified: Thu, 13 Nov 2025 23:36:52 GMT  
		Size: 6.7 MB (6747169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f1e1be724939fb6a48ae8947ce67eb644f63e7eef7a28111f530d95e79a28`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 94.1 KB (94106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130f554dc5131ca30bb3cca2803ec4a2d298833d60d8ffabe7a3cb4afea71c9`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 120.1 MB (120120282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172928eab2e2b55a426daa21320f98060ea4fd34cd2e8271d708edb2c3c951e3`  
		Last Modified: Thu, 13 Nov 2025 23:36:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f2d4cfe835e848ead8d3a0e1e848a39826efc324110adcbcb695d7f7db5d5`  
		Last Modified: Fri, 14 Nov 2025 00:36:41 GMT  
		Size: 110.2 MB (110182642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a74b9673c9eef5af9581531354dc9aafa93b711ce45ec7809bae06b30e2309`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 383.3 KB (383321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e03ba678944b9e5a8a4797a5c3d056b2f2f2fd3d1f197fb7b387a827560adb`  
		Last Modified: Fri, 14 Nov 2025 00:36:28 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb9f09a0b5483fd5ffbf4d12b9ce1b43e2e60a0deea946903460ef8183834e1`  
		Last Modified: Fri, 14 Nov 2025 00:36:30 GMT  
		Size: 28.0 MB (27998968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bace735bfd1b5a18bc9885894ac02044ab2640d66910d38779034a0f110c984a`  
		Last Modified: Fri, 14 Nov 2025 05:46:26 GMT  
		Size: 784.5 MB (784466755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5da1f098830431730c35068caf61beb59e75268e96b28158e3af6be140b246b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60715361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8127ae88fe25268781a0baac627c8d614e8de9bf7c94b195d98770541698c6e`

```dockerfile
```

-	Layers:
	-	`sha256:a0aae68ce3687e68b79a811d89042cea004876b89bc43c7b058ee6e1be35956d`  
		Last Modified: Fri, 14 Nov 2025 05:17:53 GMT  
		Size: 60.7 MB (60706022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78dc0fdcdbe6caa1e02fcc1bb56ec272f8bde016e1d8f49fba170da78496c021`  
		Last Modified: Fri, 14 Nov 2025 05:17:55 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:938f6facaf3810263df124947e631d03e075f5c535f56263274bceae993b75cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.9 MB (978876409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d90f810db0dd1f5f69d47386e8b01c828cde37a2545a362e14a97276f499e9`
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
# Thu, 13 Nov 2025 23:34:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 13 Nov 2025 23:35:26 GMT
ENV ROS_DISTRO=jazzy
# Thu, 13 Nov 2025 23:35:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:35:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 13 Nov 2025 23:35:26 GMT
CMD ["bash"]
# Fri, 14 Nov 2025 00:36:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:36:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 14 Nov 2025 00:36:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 14 Nov 2025 00:36:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9194fd0d9680db2205731529116eadbbbc8027cfff9aceb7487f9c934ad7bc3e`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 684.0 KB (684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946995b31a424fe6ec0f5dd123c93a8bd1961e062bd418b5b057578e21c5c8bc`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 6.8 MB (6759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d098b84a269afa0a803df77b1179a40e820a32854f590ab7ff373e8eb5ed5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 94.2 KB (94197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b736617adc2c17f98e0578d4c8830f36185acd9d89bb802dd5a4a33f37f51cf2`  
		Last Modified: Thu, 13 Nov 2025 23:36:15 GMT  
		Size: 114.9 MB (114907375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6df2d828da46459a8d1d5b906a8ac82b3b7356bebc393ac95f13eb3448931ab`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e72f85d1873c408b02be903df3b2a1c981707ea1c7e2403acf281daf4a100bc`  
		Last Modified: Fri, 14 Nov 2025 00:37:40 GMT  
		Size: 105.6 MB (105592948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85fe5367a87b0de3fdad83e79334f4f0af211a041e0f74bdd647fc08b45c3c`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 383.3 KB (383325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117401b5bc7988910ecc3e807810a0e375daef8a3fb1d5c2c5640452e3b4103`  
		Last Modified: Fri, 14 Nov 2025 00:37:24 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28b6f7e263db31eeee7cfc75186985e1cc6a5418322ca5a59d692bc43a7035`  
		Last Modified: Fri, 14 Nov 2025 00:37:26 GMT  
		Size: 27.1 MB (27096953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f7f5e89623d6ff02f526197860623344d614b00161b33893d9822c2cced15`  
		Last Modified: Fri, 14 Nov 2025 10:37:16 GMT  
		Size: 694.5 MB (694492997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4e1ffd49122ba0d4cd551a720ad25a563c6d760cf536511898c390c807b819dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f44731e791978aefb0dd67afb2c84b5951cc6ef71452f4ff0f500a15123f0c`

```dockerfile
```

-	Layers:
	-	`sha256:4d7f0359dd9afa8d1d7b4f1a150ae315c5e631d568fe619014ce90bbe8a7c5a0`  
		Last Modified: Fri, 14 Nov 2025 05:19:19 GMT  
		Size: 60.6 MB (60636547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234858944fcb5e1cc376a120a72ad87bb19b675630a0be21aca85e44b0c454d4`  
		Last Modified: Fri, 14 Nov 2025 05:19:20 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json
