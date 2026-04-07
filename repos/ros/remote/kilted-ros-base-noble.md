## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:6c62fad7aa64c94223fa6c327b55684b71e029a63152d183c44330be3327fe6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:5e2dd30c17d2f21f56da6ca00e05aef04512153b20690e45c89e0b517b275f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297328572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b72d1a6b3b1871318ebd8c0fd16e79c2bad75fba76c35fc484cb8b9533f12d4`
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
# Tue, 07 Apr 2026 02:27:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:47 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:28:30 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:28:30 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:30:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:30:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38325f78fe985062202a5d808b2b05fc12ef91b47ce87206380ea44d72b1e225`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d01d91154707602f77f2fc96c923025f4fed5329808472ca5fd6133d1b804b`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 6.8 MB (6751852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91115af12bb2a5a2b1646bc3a4d314da01da1a4e980b4c8b57a00781d35ebd59`  
		Last Modified: Tue, 07 Apr 2026 02:28:59 GMT  
		Size: 94.3 KB (94252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed33e2798ddd6451718af3dc9c6fcdcf2af918d3740522bb8ec01341be69ca2`  
		Last Modified: Tue, 07 Apr 2026 02:29:03 GMT  
		Size: 121.4 MB (121415474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f0b04354c6f34f4ea24545aae77af5a06549191cb74e1b55376d179ec25a7f`  
		Last Modified: Tue, 07 Apr 2026 02:29:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af71c8b2b7800651b1ebed77c93e9e88181449a81ce4d83668d196953b74930f`  
		Last Modified: Tue, 07 Apr 2026 03:31:14 GMT  
		Size: 110.2 MB (110192712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e990202056cce74a97a1d88af992471957a5ca3246b73c8e843be09fcf51b3`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6279757b2e3bf73fe38bd373df54844e8f12e865e560d46c2fb972600fbff380`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d27fadbaedf7924960dc53c887f8ab5fe2cd773a64e3f50c5ba1ef3cb1899b`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 28.1 MB (28074526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b54e568135f0f8ff148878e05d890d5294bba7c82bf4ecf2fd4af5e60d28a32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24766955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d7cc0e91d71baf8abcf9f29fce2de72cbf6704a489563997c366ec576a9fec`

```dockerfile
```

-	Layers:
	-	`sha256:d0790a7ba44e8ae54961ffb4a40a44a692558e0d680b9933e723623eddf955b4`  
		Last Modified: Tue, 07 Apr 2026 03:31:12 GMT  
		Size: 24.8 MB (24750608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1185ed4241993de2b3d22f0692b34be58eea1cbd2c4ee7082ea277948e809f61`  
		Last Modified: Tue, 07 Apr 2026 03:31:10 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d28094b2d31ea8e3ae26e89f2e5e8712bbf6d1296435f0b90146ae0941b45401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285705599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb790354d7fe39725c4875c4b7048ed4ba848ce6e11bd7d1e276c931e9e6b80`
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
# Tue, 07 Apr 2026 02:34:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:34:25 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Apr 2026 02:35:10 GMT
ENV ROS_DISTRO=kilted
# Tue, 07 Apr 2026 02:35:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:35:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Apr 2026 02:35:10 GMT
CMD ["bash"]
# Tue, 07 Apr 2026 03:42:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 07 Apr 2026 03:42:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994cbd5ad3999a6436d4acb7f4e0c8ae5f2c28e2083c469c5ba7ae71645ebca`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 684.2 KB (684222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864490eeb49a94e62a6faa6f09e3ae12a30946a7a7e210d2dc39dcc27fd77b92`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 6.8 MB (6765048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee29e66778cfc35f775b92c6976fdbc937be43255a2096f21d3d4666852e24f`  
		Last Modified: Tue, 07 Apr 2026 02:35:39 GMT  
		Size: 94.3 KB (94316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f8858395961cdd5c21c9d1596b8eab8304cb7630e82a9fef29d4c62ffc1f`  
		Last Modified: Tue, 07 Apr 2026 02:35:42 GMT  
		Size: 116.1 MB (116140250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7f85075ead7ec10011a7e1ab0b46d4921931654ed5daa0419698d2af86463`  
		Last Modified: Tue, 07 Apr 2026 02:35:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c52e72a98ff18024c49e42ee5a244f148f67c229f893f253bb98739e4601b2`  
		Last Modified: Tue, 07 Apr 2026 03:43:37 GMT  
		Size: 105.6 MB (105605517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47880aad4a35736cef7a2c581e364e499a17cda990ef9faf212e5f8dc5dc498`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 379.5 KB (379490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776f56cf9e1966633dc9669e8a06f723d88958d885f0bafeca03338fe3f06d2`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fb55a370964daa8364587fcd75a1c5697db6be6c7a368cc372ca913dd6424`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 27.2 MB (27159980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:021db3c29d874aeaf4a52e6476f55134d6179b1fdc34bb35049b5653866cb55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24789354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987c999ccbbafc31ba85d411659003345fae235c66d28d57d3b667e6c996733f`

```dockerfile
```

-	Layers:
	-	`sha256:d479adab56c856db5a5921e5d2a65dbd9864671d45016bb31549949bde04fb26`  
		Last Modified: Tue, 07 Apr 2026 03:43:35 GMT  
		Size: 24.8 MB (24772870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f21380ebe03c6ff83ee024b4347dca4cfcab0119ce6e0bcbecfac6c3a04eb04`  
		Last Modified: Tue, 07 Apr 2026 03:43:34 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json
