## `ros:humble-perception`

```console
$ docker pull ros@sha256:70d8ab67ea4cac670db524f9e7095536aeead79f578c8142ff2b6a48e065e31a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:2d0b52aa815d3342863d3cd24e7f8065b6dfb5a0d78ac99fd7918409ce6f628a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.9 MB (955926195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2941a4d3d5c0362dc16ccabd8e7e40d6bb09bb1721107eafa1c9a75c724028d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:53:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:06 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 20:54:45 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 20:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 20:54:45 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:45:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:45:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:45:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:46:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a8e3ada8f618169b57768a6e62adc5b4af07d0209a93f1fdbf6ef8ce8479f1`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 1.2 MB (1215547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd358c4c08448ffd11c0958b21ecd32e6379061f941d586cf4c76a28ee837809`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 6.0 MB (5994365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf96e61ad269ae729e2d85ef0baba1d0e8a2a8b8793c365d1e4fbeb6c5509b9`  
		Last Modified: Wed, 15 Apr 2026 20:55:09 GMT  
		Size: 97.2 KB (97163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4858fc5748850341f9a6eb1c5fca3016eda83db7833c5b56a64c261d1e619f`  
		Last Modified: Wed, 15 Apr 2026 20:55:13 GMT  
		Size: 104.9 MB (104872855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd7919b7abedda1fa31f5bf8a06f4007ba2ab1d6c9fe37fd4433cddc2f5e0d2`  
		Last Modified: Wed, 15 Apr 2026 20:55:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45ba2ee710139051388eae90cb6e670a31c05af43e98627a2d1711d2fd9c70`  
		Last Modified: Wed, 15 Apr 2026 21:46:44 GMT  
		Size: 98.2 MB (98158243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef8df8e2fe30a40fa7b72a18e14cf9ef6e7f658cfe5e0f1077ab38bf60d5318`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 393.0 KB (393032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8764faa03981d66386f3a858722bc29141e0f26d47a8445e9c9c18510df4a`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 2.5 KB (2516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97534683f7c4591bc92e7a96a484cee7d3fc51d096d9773c164c69a4e145aa93`  
		Last Modified: Wed, 15 Apr 2026 21:46:42 GMT  
		Size: 23.3 MB (23334771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9a3a9bf9e52c568b7b527c7c37de029b686dea10aa1177245f2dac8041b415`  
		Last Modified: Wed, 15 Apr 2026 22:33:41 GMT  
		Size: 692.1 MB (692121008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c55a462df92ed03b3502ef70822be1ddd0482be24a99ead1c91371123b5c3fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58945086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24739044944ee8fc2adfd1de8571780d5f7304aa579c81c5d2f114e00b497acc`

```dockerfile
```

-	Layers:
	-	`sha256:32e0d7cc1de5ae6c59dfb166c690d781216933defd58a96686adda921631938a`  
		Last Modified: Wed, 15 Apr 2026 22:33:28 GMT  
		Size: 58.9 MB (58935734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ebace2d36cca824ead71102fbda04a247c86cbdb4d757f452630502ba49d25`  
		Last Modified: Wed, 15 Apr 2026 22:33:25 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:058beaf47da4acbe6da25a933cae828ee72f74667f6c284bf4fa3c18c0c57843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **916.5 MB (916499048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9f9d0fd19386a385411843e69deeea21c4eb63f303bf669dff3ecc185be1c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:30 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 15 Apr 2026 21:02:11 GMT
ENV ROS_DISTRO=humble
# Wed, 15 Apr 2026 21:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 21:02:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 15 Apr 2026 21:02:12 GMT
CMD ["bash"]
# Wed, 15 Apr 2026 21:58:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:58:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 15 Apr 2026 21:58:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 15 Apr 2026 21:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:37:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c2a0a46477190f0fa6eb8e1e24937a7a892a2da4dbfde5fedbff1165bc202f`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 1.2 MB (1215780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3d402648b828b47f89d64b7e7e7aa20ed8278ae37c701230808b7ff6266b`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 5.9 MB (5948659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b1a9f3d6434e09d0c3553ce1602fdaa06bf41a5cb1e81eaba5d388ef3f9e73`  
		Last Modified: Wed, 15 Apr 2026 21:02:38 GMT  
		Size: 97.3 KB (97282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2a633b06933c84562c54062201c1d1e0115d0309e004101ca6f8bad53e75e`  
		Last Modified: Wed, 15 Apr 2026 21:02:41 GMT  
		Size: 102.6 MB (102624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd5ee001a0f676fb3515f3e51de0d6d59ce44b9ed65795991b7dc06bc652dcb`  
		Last Modified: Wed, 15 Apr 2026 21:02:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c7e9eb84bd5c3985eff3fd8415c04a41b5a94fb1a49ea566696e134c79b55`  
		Last Modified: Wed, 15 Apr 2026 21:59:18 GMT  
		Size: 95.8 MB (95795267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea249effcab0d693d068bc41ee0aed2d26a367ba55d8f7112b5371d5f6f017`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 393.0 KB (393024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f80a79325a2dd8eb06c0a86ef1bba3a0becb31cc638213b88be7d8fd8fecb3d`  
		Last Modified: Wed, 15 Apr 2026 21:59:15 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889d1e226215be958de1e435f8c6682297aedd0a218347bf5e08a083fb501ada`  
		Last Modified: Wed, 15 Apr 2026 21:59:16 GMT  
		Size: 22.7 MB (22728119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9170d494e27e9dece2e37208438457682c8cfe1848dabf5889ebe7c823eb9fe`  
		Last Modified: Wed, 15 Apr 2026 22:40:14 GMT  
		Size: 660.1 MB (660086945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:64d98835332be1f2b865ebb376fe2f156c0844103afa355ccc022a17ae975784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b69be88306a1c32932f464a84f47e89ddf33777cf6c4e126887934c291b157e`

```dockerfile
```

-	Layers:
	-	`sha256:2379763680d837a98e95b5046cd024689ef1fbf0c3af75cfa42b32717172cccf`  
		Last Modified: Wed, 15 Apr 2026 22:40:03 GMT  
		Size: 58.9 MB (58920055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfe58f9b93c7484fbb92e2fd1d7cf5c0ae250ce4919bf20136c43d2b26eadc3`  
		Last Modified: Wed, 15 Apr 2026 22:40:00 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
