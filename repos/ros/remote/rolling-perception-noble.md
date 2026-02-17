## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:fb8086e4295ca2d3412d809fd1ef981f4a98cf5805e71f5564fa20efb33f2d48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:1884bd21776b273efb12261ead653db80a4ae9425ec5abfbeac669eb0aa5676e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1096229150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d57bea1a7fabaccfef058f3b510c1a02c43467c9be2d3fb6f1a15b718aae4c3`
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
# Tue, 17 Feb 2026 20:31:33 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:50 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:32:34 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:32:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:32:34 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:53:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0a5bfb681d3138ae54e2531c0db5baff7335a111bc7e1b4bb8b45918f145c4`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 683.9 KB (683924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514b27b4f1c66b438e12bd5df078fc6801c86ec4695a3b50d075b6c9609cfa3`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 6.7 MB (6749453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003d390a14412348f6a3973f77e5325024e5a26cb6e5bdc19b58df399edcdde`  
		Last Modified: Tue, 17 Feb 2026 20:33:02 GMT  
		Size: 94.2 KB (94159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac08644448065e069d28bc056cf5686de74d3d492c22d24157cd2a686d303d`  
		Last Modified: Tue, 17 Feb 2026 20:33:06 GMT  
		Size: 136.1 MB (136117170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41ad160e2ef9188750380c1f7e1e63f64726d880305f9acdbda9a58b52f86ae`  
		Last Modified: Tue, 17 Feb 2026 20:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812ef68b8c806cd8e903009ab4882feb9e9ea56176b99719ea0e3c7ebbfac1f4`  
		Last Modified: Tue, 17 Feb 2026 21:30:57 GMT  
		Size: 110.2 MB (110188830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60572606e296b3d090dc856f0b55084a6e2d0ad69bbf5971816665902bb4bfb9`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 367.7 KB (367683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a46da188376f13cd0fa38e85a153c20688d45f128f8e0b541b3ac68cc23df`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 2.5 KB (2517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564a4e1fd4e992445106871cb0338c26eea2bf2558c4a42b33a7b9606ebc52b4`  
		Last Modified: Tue, 17 Feb 2026 21:30:56 GMT  
		Size: 27.8 MB (27844723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d2037de5d82347ca4d0a0d9736def979448a5d5a7bb945dc30a390ca12c24d`  
		Last Modified: Tue, 17 Feb 2026 21:56:30 GMT  
		Size: 784.5 MB (784452885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:602d977f68716e850e22a295eaafe3450181da8da32528af410672f6b7391329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61804780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cac23806c69f0d0cbbf1683f32ab20f781f935e0016ccf9285bc06275b7599e`

```dockerfile
```

-	Layers:
	-	`sha256:2ddf8a1416f7d33457b5127ef6b1f6a63c3a45213218851a9ee43f32daa27076`  
		Last Modified: Tue, 17 Feb 2026 21:56:18 GMT  
		Size: 61.8 MB (61795419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f4def1dede899b783201d1d5b712dba0cdbda0ca9139ead34bc6c6a4e266b9`  
		Last Modified: Tue, 17 Feb 2026 21:56:15 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a6729dd234543ac2e1d3ebf62ef2a70c69dc74f3d843b787950c9a6450405b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **998.3 MB (998319143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b83837afd9c25b9027a997821fd94e1ab8ac79f2aaa5f8dea9736dfabea0cc`
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
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Feb 2026 20:31:29 GMT
ENV ROS_DISTRO=rolling
# Tue, 17 Feb 2026 20:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:29 GMT
CMD ["bash"]
# Tue, 17 Feb 2026 21:29:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:29:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Feb 2026 21:29:59 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Feb 2026 21:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:87f0d786fa0e455b088600e866b59b73b6102a305124a32a1180a5ab261f08cc`  
		Last Modified: Tue, 17 Feb 2026 20:32:04 GMT  
		Size: 130.4 MB (130393285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfe3a3a3cad8d96e5c085256e9dfe0726825eed266def97da735eb9d3a41cae`  
		Last Modified: Tue, 17 Feb 2026 20:32:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dbe63264e1ed1c4f3e5e806897b787c7e5d70a66666a164214f314edacd021`  
		Last Modified: Tue, 17 Feb 2026 21:31:03 GMT  
		Size: 105.6 MB (105601575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3f84333d023de739abbd5700103a0cb9bfc6f3c3ca019a07b45f1fc73504e`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 367.7 KB (367679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d5eb6309d46d62dfb27dc6f4e5b31f76a785a45edfbf560aee4d5e5091e72b`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f253acc6e2219780d32daada961d2c5b2592e94cd1719fad650ff143dd9205c`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 26.9 MB (26929636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543423e6e5a3857ebd4d024734955f3cd9173641862eb322c5814b2c0be13123`  
		Last Modified: Tue, 17 Feb 2026 21:56:35 GMT  
		Size: 698.6 MB (698618251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:1d6711c83675114e2c338a45cbd68677708091daf2771ecebc3d9d567a8384f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61735573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec08d47ed0590f71a05f40fb9642dad349315c629d295f376155aa1cc771d3d9`

```dockerfile
```

-	Layers:
	-	`sha256:92fcc244968d9640cc62bf6f1c73a151d0cd304ae35b8fa810f8ab20f2b52bed`  
		Last Modified: Tue, 17 Feb 2026 21:56:23 GMT  
		Size: 61.7 MB (61726132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207c8407681709a69a1163579d31df40ed4f1f3cf3c448aac2cb404be63c1239`  
		Last Modified: Tue, 17 Feb 2026 21:56:21 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
