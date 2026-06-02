## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:ce241352eb294cc26f99fc3b0d5a3aa9777781e6f197a9fc20e109befa08ab89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:97552ea9286484fdd62ac01f9091d7f08778dd8abcae35800ae66f84c89deb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296525362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca1dd27516e3749ee2d2648bf9f7db6092623e968f5c6fef9ba190ec662869e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:13 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:14:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:15:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:15:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:15:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685092803da43ca941292a896dd8f48ce1a8d91790f69c2b1c79155b9a69b145`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 684.1 KB (684100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe1f8d3291d469cb43e34c42805d2fc2b1c783dcf66f4ee0525af8f9949005`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 6.8 MB (6752403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ad6cfd35f7eb6e09d5e6988027d6d14d4616a251e4b6f7b15d46610e5da6bf`  
		Last Modified: Tue, 02 Jun 2026 08:22:21 GMT  
		Size: 94.3 KB (94312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16adb782f56ae8a50f40642754bde93ad1b585f0ec4ad386db098320f795644c`  
		Last Modified: Tue, 02 Jun 2026 08:22:24 GMT  
		Size: 120.8 MB (120789572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd387be3eedd271dde548d6e8d372f2d0df9203a335b5a07277419fd3a25c6f5`  
		Last Modified: Tue, 02 Jun 2026 08:22:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7591985e47a84095a344162d1c2db751bf489e751dcd4e74636cfe7ce1b56c32`  
		Last Modified: Tue, 02 Jun 2026 09:15:51 GMT  
		Size: 110.2 MB (110196246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a097140c3e1ce3192ceaafb4247254801b5536f5ff6e4e935df9b35d20218973`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 384.0 KB (383978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112170637d27b54fc305ed87c92758f6cac238c074fe0c0e11226c3e22c94c3`  
		Last Modified: Tue, 02 Jun 2026 09:15:48 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac36c7d12f9264e8c13e70c4be0a94ec42d19a7fa9ef2e9020fa697cb5aee914`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 27.9 MB (27889252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:da0b9b34cfa4f2e02f46cb4fc2a787b180e0641b84d8016dcd778ce344654314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24756730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd08bdac497a708635a7ef3b13fa4d7f0a33c206dbb9b8070fe0fa5b4fc7296`

```dockerfile
```

-	Layers:
	-	`sha256:a8a0a8146a51875f4d1c7b2dff7bfcb1314329bdd1ce751fe21d86868b5e9778`  
		Last Modified: Tue, 02 Jun 2026 09:15:49 GMT  
		Size: 24.7 MB (24740384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741fcf5c9fad5dbc7ff704534dc39fc9955edcba1567c6601e32c35d09516087`  
		Last Modified: Tue, 02 Jun 2026 09:15:47 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:837b40120856c929d7b0bc72c906aa8867506fd90f211d09afd0d9c221529050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284932276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ed99ef2ffe5535866e73b80ee91b3ec4592eb05dfc499de418d75fe7d3d97c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:21:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:30 GMT
RUN curl -L -s -f -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.2.0/ros2-apt-source_1.2.0.noble_all.deb     && echo "0804d9b13db770eb87019be414cd78378835228ad5fa801fc88758596dd8f7e5 */tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 08:22:09 GMT
ENV ROS_DISTRO=kilted
# Tue, 02 Jun 2026 08:22:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:09 GMT
CMD ["bash"]
# Tue, 02 Jun 2026 09:23:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:23:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 02 Jun 2026 09:23:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 02 Jun 2026 09:23:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b416145b2d0ffb7ae21a537e749877dcd599e74b4d9f478ff90dc7ca53b9bd61`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 684.2 KB (684232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6875267f1b9da5a58d88bcee0d575c2e293237fb4742314202eabbc1d1df8`  
		Last Modified: Tue, 02 Jun 2026 08:22:37 GMT  
		Size: 6.8 MB (6765733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42269c28912bc00b80ac1cd7f69237e55b1853486f06e98f684b3b531cad7572`  
		Last Modified: Tue, 02 Jun 2026 08:22:36 GMT  
		Size: 94.4 KB (94402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e07f457aff02417cb213909621dc479df8474c419987ecb0627cd88fd7bc2a6`  
		Last Modified: Tue, 02 Jun 2026 08:22:40 GMT  
		Size: 115.5 MB (115517604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c855c40a83380b5b946026099a869c99e32021af8b48e3604c5218a4e9c70`  
		Last Modified: Tue, 02 Jun 2026 08:22:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77bfb824aac72d5c1073df5f5acb6b7a3c20d107adec44a222da0c810d8c94`  
		Last Modified: Tue, 02 Jun 2026 09:24:11 GMT  
		Size: 105.6 MB (105609755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4428427f205c2c454f011d2825db888344ddc8501ace447a350671bfef15670a`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 384.0 KB (383972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a251bc17a680222bf4f00827205fce57a7a1229a19ed87b70fb066f99a0c5910`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c18e61574b544d7fd789fc4baed9d75abfd91e2912379743520d5aaf7a68bf6`  
		Last Modified: Tue, 02 Jun 2026 09:24:09 GMT  
		Size: 27.0 MB (26997482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:fc1f84921a10b9d8372250c8a0c7383a420b806af7113c19003dbbd81b3b2116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24779128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b424d98817a45c88ad6e9be8319164e8cf15446b0a06493dcbd1391ba2e20`

```dockerfile
```

-	Layers:
	-	`sha256:2c4c5656e0cbb0d23a6940cd6150585c72d47642167049cdd5528bcae835580d`  
		Last Modified: Tue, 02 Jun 2026 09:24:08 GMT  
		Size: 24.8 MB (24762644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b762863b72c4c0fdc52e8ddbef2ec008f88a2585163002ec2ede4de40e2f48d0`  
		Last Modified: Tue, 02 Jun 2026 09:24:07 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json
