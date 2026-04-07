## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:b4cb947f343cb7aae84f2c568fb08c98ea48923f8e3015a7be3a72e011c7d6a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:c20aff77ba56b7be673f61e98c1137439a74ee4e572ef48b905af2f44c2ce278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1080579520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7305a62a09a778c80206513c1dcd51ca8f1bfe31bfbb2a9608b00eaa50ecf82`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:27 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:27 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2df0147e83f87e8e0773aa75602bee1eb50ceec4c9f515f2f1182b82bcf9`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 684.1 KB (684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d75d23a6c680dfa13a647dd3cf5db5f8ae9f87a17e3efb6e695fe061f9f6260`  
		Last Modified: Tue, 07 Apr 2026 02:28:56 GMT  
		Size: 6.8 MB (6751855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986f07e48752367934b73ae08576189a8e277ac5f37c4519c1f39ca5870b044e`  
		Last Modified: Tue, 07 Apr 2026 02:28:55 GMT  
		Size: 94.3 KB (94253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5519a86acbf1f18e15faa4bf0be57e2da1e65732c6dbfbac0d9fb0ac44576a`  
		Last Modified: Tue, 07 Apr 2026 02:28:58 GMT  
		Size: 120.4 MB (120412417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371cc9eed49f9903f8c0ebfb943d0dfef56e463785c84800dd55fbd6f9b40e3`  
		Last Modified: Tue, 07 Apr 2026 02:28:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8dd6647a3c1e7d18001a45a8789638361caf8dfef0f307b190a1384f0a2413`  
		Last Modified: Tue, 07 Apr 2026 03:31:11 GMT  
		Size: 110.2 MB (110188982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6af0b3531a3918b50c613a65fd716cbff3bb7b3243c89bb4312d5e60cdf14e`  
		Last Modified: Tue, 07 Apr 2026 03:31:07 GMT  
		Size: 405.7 KB (405659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf926922fb8b2b3271f1be2185badc4d52812efb69c4186e57f4bb5b97e60cb`  
		Last Modified: Tue, 07 Apr 2026 03:31:08 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e9897748f310d88fd17993769228e2f42207223ca0c90914f25c4d40da3c7`  
		Last Modified: Tue, 07 Apr 2026 03:31:09 GMT  
		Size: 28.0 MB (28010350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbbb9f561c02a517af508d90c638f9dd5ca527ecb662bef78029d81a4d998b0`  
		Last Modified: Tue, 07 Apr 2026 05:01:23 GMT  
		Size: 784.3 MB (784295715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:9857cc23020ae6f264eef773a1a0d3a6941eab6cef0f6d4d3e49366da3da17a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60738111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d7c7b6e6c7e49675baf9db45b607a422716c651fb221ee97ae8fde4f1efc8a`

```dockerfile
```

-	Layers:
	-	`sha256:f1988328b5c59e064ec2867182b834eafdbf7ebc3c62d1def734792f095c61d0`  
		Last Modified: Tue, 07 Apr 2026 05:00:44 GMT  
		Size: 60.7 MB (60728772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a903f7162cbe7e88b054e9415f3bd534f5a37ac61466fc5cc12526a5d645ffc`  
		Last Modified: Tue, 07 Apr 2026 05:00:42 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c5520caba868b61968962c494030ffc68c3b41b4f75933e4d7facc94836de030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.2 MB (983187921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9ad98273a04e2c42a7f3063705bff5f522e1b2f4330b8e3b23386b9eaa608f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:55 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:33:45 GMT
ENV ROS_DISTRO=jazzy
# Tue, 07 Apr 2026 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:33:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:33:46 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:02:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d31541b1d8d1b3d218fba43000cb12270f551607798e615c32f5c659c019fb5`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 684.2 KB (684202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db22f2cce3a01e224a54fd88e4b34db843b7b5ea6da1c036bd2b9ec317262c`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 6.8 MB (6765111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc4a8210e22651b45d0b1d6ece27755ec3e5b2e07d4b23d461b295d2ba8f30`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 94.3 KB (94328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21236c0dfc681ff5d94fac0319bd28d98dbc58bbfb85c9bec0d0e00c04cce8b`  
		Last Modified: Tue, 07 Apr 2026 02:34:19 GMT  
		Size: 115.2 MB (115207286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d3a43b9d78c7f272dd8156356f6842d6031b8c267e016defaf96c1b7cb592`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9161909dfa0ad7f5997c40a973a116ed80646d74843f0a597dc20ed3e125a8e7`  
		Last Modified: Tue, 07 Apr 2026 03:43:19 GMT  
		Size: 105.6 MB (105602757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acde01ab9a2e4a57c5d4f65c24cb93972ea90a24913b0a6fe47933637d93d94`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 405.7 KB (405655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e592252c9ae49ff56f1b4f86b18208ba2ccc2fd338f6501a7ce53ed3d869dd`  
		Last Modified: Tue, 07 Apr 2026 03:43:16 GMT  
		Size: 2.5 KB (2519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b8c78e8323633d8f1b0a4cbde5ac8aca13922c7dc16e99313d98fb1d9169c`  
		Last Modified: Tue, 07 Apr 2026 03:43:17 GMT  
		Size: 27.1 MB (27103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48105a07856f73b4deb14484aa74c7d18c537b920940151130b841e1754d08f9`  
		Last Modified: Tue, 07 Apr 2026 05:05:35 GMT  
		Size: 698.4 MB (698448300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:6d826aedb138c604e66e75465414efb0e2d605a0c902bf195df5367c48cdf4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60668699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337aa2b208f38b5c7f9a943462907748a37fa3cbf9c8939d5f9e7e3fca787065`

```dockerfile
```

-	Layers:
	-	`sha256:365572da5e6b035d1a8c167bb682d0d4c6e4bf3cdefad6223e93cf9c947e6fc4`  
		Last Modified: Tue, 07 Apr 2026 05:05:21 GMT  
		Size: 60.7 MB (60659280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513be45092d456f84f1fd7fba9da7d6900f60e315f6862d10258d34ac5e28785`  
		Last Modified: Tue, 07 Apr 2026 05:05:18 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json
