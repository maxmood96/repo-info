## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:be7350a0efd17925415a6a3a076d6009b425af7500b0a5cdb5d717e87ef46f39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:ce6609ec2188d0eadd61640fb598c0aff629a84d88970423b8f341ead2515683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297326820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acefc0d3f654319d0a8acbfda596ca2b0431744931b3a0ac8f94a618d83d8d77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:22 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:05 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:31:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:05 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5c47e47d448610a4c35e5fbaa052b0ec857309d5c4d05d0373bc40a63457a`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 683.9 KB (683946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8111e2b52230b6bdb7c7c9db7714d2463c6bce8b064f715ffff136acc6f0d2`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 6.7 MB (6749482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbfe68028602895a8f68cf50a08afa43f426b24f07f9b198ae78ceabd934991`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 94.2 KB (94160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60fc3786d0396a22473a6b7b79a0afe2ac50e450187cf36e59fd111ac60c6d`  
		Last Modified: Tue, 17 Feb 2026 20:31:35 GMT  
		Size: 121.5 MB (121480309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cf234ec8f8764d70601c05423308a37a501ea670106efafa4c4bac0b081dd`  
		Last Modified: Tue, 17 Feb 2026 20:31:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b3d9a566e114da54d21bf58e4966463e527b60b3804930a6ea605d2121e10`  
		Last Modified: Tue, 17 Feb 2026 21:30:41 GMT  
		Size: 110.2 MB (110184420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b854746bc8abeda04290f546ed981825386ca433ccb4ce033b00e37ec7a762`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f7b716a7040942361f3e8f793c2f0b83c5cd5b3fd97a9a8e257272797914ba`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764a19249b8029c3c30665053cae88c2468e2160996f4ec6c15e3e6bd29819be`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 28.0 MB (28010609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c7d52fb9b437e9975a169b8ba5cb32e7c2c993e4340df84818e379770a2a2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24588155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad88720731506dc7d0868322c1d0f61fadec9061136675a508bbbbbfe7a1863f`

```dockerfile
```

-	Layers:
	-	`sha256:7505f29b7ee944b557282d7acf9ff742cd1e597e9ddbe42ee7cbbf9b815600d1`  
		Last Modified: Tue, 17 Feb 2026 21:30:38 GMT  
		Size: 24.6 MB (24571534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959b4701f17e17abc6067e5dca9717fe2a8ad033cc3f8ca53a67856cdc739e18`  
		Last Modified: Tue, 17 Feb 2026 21:30:37 GMT  
		Size: 16.6 KB (16621 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:88b0bd4c0718167fb546b239f659b98c56b17899bc3156377fbfdf6c4b196d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285711414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275afdcded52da5bf8cad64931e82672234c6074a99241159d31ae5280221085`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:30:00 GMT
ENV ROS_DISTRO=jazzy
# Tue, 17 Feb 2026 20:30:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:00 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316588a5c2f0a293c1be86bfccadc187c4feed7958a93c14cfb6adb763e9c0ea`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 684.1 KB (684117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f027f20df8200c1bca1a49d25125514171ad73ebf3c1da9819933829315b0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 6.8 MB (6762503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510cc38551ed57228e7ebdd685eaf742fe4fcfea7497205d334cb4fe553845e9`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 94.3 KB (94283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed24768c59b5d134a0704c2567aab7300b36251f97ccba0d93bca18d37f1be6`  
		Last Modified: Tue, 17 Feb 2026 20:30:32 GMT  
		Size: 116.2 MB (116208395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316f07a73845af83d8730297d105e626a9bf1c43c009fe946daf4df9084dc0e`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6cdbf5638e01baf5f4ec197a800f353f617358a1f43b6e151d1b64251e8b7f`  
		Last Modified: Tue, 17 Feb 2026 21:30:51 GMT  
		Size: 105.6 MB (105596998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e52aaae05d7a458e18396f7f0f9d755c781112f84751e5817d0e88bc34ea2`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 393.6 KB (393578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799712497a09e97750515f98342d57c7f654171747df8aec170c19c3be4ff36`  
		Last Modified: Tue, 17 Feb 2026 21:30:48 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9582f114d28d219dd1cb06cba385dde792616b75950048223ee0564239480a`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 27.1 MB (27103726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:80a2566beea4dcf1870c72f3cc922773e2f1edc087ec2ce375b65933d18b50a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24610565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1c12faadee9c9c6ad804eb672a2f7fbdaba301508b89d3bce85bbdd08fa1e9`

```dockerfile
```

-	Layers:
	-	`sha256:b4d27de917d41f43c9ee5e6f21583acb273448abcdfc67cd0e43ab70da52bec9`  
		Last Modified: Tue, 17 Feb 2026 21:30:49 GMT  
		Size: 24.6 MB (24593795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2581bfe955c6a730daea90de82dcfc3db1ad1ee1b5b4edef75bb22c2fdcbb7`  
		Last Modified: Tue, 17 Feb 2026 21:30:47 GMT  
		Size: 16.8 KB (16770 bytes)  
		MIME: application/vnd.in-toto+json
