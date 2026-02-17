## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:3acd13deada29af2d41dab37f0ad3c48c5ea7a89fd109ef9c82c561c13b38476
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:7ba2f865e5c89b86dd1149e03d2cc6b85e925422e436ed6d6876560ed786c2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158735704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5433c1cc2c3a0f52c726d84f56bbb42f2c19a2311ac1f1938a7ff4de372364cf`
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

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:c8a78d4a306bcd35b2cbb4f9d8eec46bec49d2e0c5eae491f325a7b98dc7e681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9324915ce63b75e3a48d8e3d286fe74d3e1dcfbb06f3b3f45ba2b570670400d`

```dockerfile
```

-	Layers:
	-	`sha256:3e2c361af4d2b9e40c7cfa68112fd8acb81f41791f53921b213170ab7f6ae23c`  
		Last Modified: Tue, 17 Feb 2026 20:31:33 GMT  
		Size: 18.3 MB (18327867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5888590af6f53c5aee7a3722ab80113f530742cb7bd8f0227c9daf9a24cd4d`  
		Last Modified: Tue, 17 Feb 2026 20:31:32 GMT  
		Size: 14.6 KB (14600 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e9b09a496cab2e0ad7a0355ff0731285e214f73d72f560ed220d71321516dcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152614615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fabb98f88137bd3e0a7f098cfc28fcda5020a95b987330330d3d6839588d188`
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

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:02678a7cebe104e42e8b1689dbcaa54f8a2aeb0476e13a6a1a06c28dd45335cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ade2b6030bd5dceaa50b139ff0a6e2daf6d8ebc1db41667f92edfa7ca25a107`

```dockerfile
```

-	Layers:
	-	`sha256:17e7077600b10636d6c91d92f5865c7ea1c370c2e0f3152a89baa9935108d915`  
		Last Modified: Tue, 17 Feb 2026 20:30:30 GMT  
		Size: 18.3 MB (18301873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea531b1091e37cc0075a567a3cf435ed4a3b8942d11fc8b5b1f372b499b8f287`  
		Last Modified: Tue, 17 Feb 2026 20:30:29 GMT  
		Size: 14.7 KB (14725 bytes)  
		MIME: application/vnd.in-toto+json
