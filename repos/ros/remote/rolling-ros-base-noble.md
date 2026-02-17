## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:0b43ca8bb2b1c618139b527fbc345e05024c7daa0b654bbf51a496a6a3ff15f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:ec7109087c5e59a4cfbf1ca8aef22c0a20e5b26ea06c1bc665695fa2396e67b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311776265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4be1fea49cd0e8e0285a854bd5de7270ef475881253ef9d8bd09029876cb77c`
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

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f6330a9672aefce6f5636e5d5ea0571abe0e95233c109a966b4ad1a0c5d94b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25637355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c436b9c719e9efb83e8d56860b98a13dc9cbe3516270ca528abca59e02d59f`

```dockerfile
```

-	Layers:
	-	`sha256:d9cc8355dd05b5855b535ebd9d724ef97e19c678ef84f57cc6740f444d7a48a5`  
		Last Modified: Tue, 17 Feb 2026 21:30:55 GMT  
		Size: 25.6 MB (25620991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa164f4d7ae83b6a4c224d7db8adf4552b29218daf00d021361ef916a662df0a`  
		Last Modified: Tue, 17 Feb 2026 21:30:54 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4fdd7b5ed66b33350063a7fb066fb057275c668a72db872fe062fb83639f77f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299700892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bcf89f4996d8601126e407ccbd5081f913b2545c1e48d6e55de878aaa183d6`
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

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:7dd40f7f6feaa0f035cbe9c7a9773bf1320d68764d5703fa30754dccc21ae87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25659947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074f694a516f67301a8f73e90ffc609df3070a55ed8dcfcc95f95fabe9692fd8`

```dockerfile
```

-	Layers:
	-	`sha256:9361dce8b643dcdb0f9e2a00abf93bd8770c467f83280781acca62a0d3f76702`  
		Last Modified: Tue, 17 Feb 2026 21:31:00 GMT  
		Size: 25.6 MB (25643445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6a1c50a9e6a7cb079ca09d9e038bfac24f8052ec8de6ca371c4c42dc313ea4f`  
		Last Modified: Tue, 17 Feb 2026 21:30:59 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
