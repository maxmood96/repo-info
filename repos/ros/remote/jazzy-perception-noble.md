## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:ce43a7f6fb6d6b2c7b8e6c0f9f33bad1f17331b06dd2c2be3a0b4dbfbfebe791
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:6b2a2f4da80d4558014734d8e07bca4ef8f0699474db2c299981756d50f7d27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1081069008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d74b5b0734ae63a5e98ff7cb8d4c2302c16e3c71270548f2f5b13c2ad6dce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1093e90b494a8cf5c26d88b9121c20432cfed972a3596da60382e67ff19b37ab`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 683.9 KB (683927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc95d893b22a2295a2886c6467a97ee5dade130bea11f8994e4f764607dc781`  
		Last Modified: Thu, 09 Oct 2025 21:24:02 GMT  
		Size: 6.7 MB (6746996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aee44d69d92942ce7f9b6acc7104f12ee9caef6adadcb1a39d72cfde21076f`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 94.2 KB (94157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d108b0455d26874467bb535ac1b0fb32de8c484d3ffd3710dbea124ffc245adb`  
		Last Modified: Thu, 09 Oct 2025 21:24:11 GMT  
		Size: 120.1 MB (120110076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d51c9d4c4e7ee2f490765efc765899f07ad09fdba245ea055344af0b2e9f2d`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36af06f6ea928bae29ab81e26c4b9c86a6fcd53abfc26c09e3d892679ba309`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 110.2 MB (110182197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41918390b2c6a6dc558d65d0c6c2961345a18ba76758672d27188711abc1c0a4`  
		Last Modified: Thu, 09 Oct 2025 22:21:04 GMT  
		Size: 378.6 KB (378566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04beb5559111f3e67bb33a9f809f6f48b46b864c326c7929e27268c217812922`  
		Last Modified: Thu, 09 Oct 2025 22:21:03 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e60e3858f8ce453118ccbb8f050ce6fd37bb2be26ba42111ce1a376bd19c9fb`  
		Last Modified: Thu, 09 Oct 2025 22:21:11 GMT  
		Size: 28.0 MB (27998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffb5005bc4b98e65f44bcdd882087eca373f09d6dfa49bb5aa2c0243c5a40f0`  
		Last Modified: Fri, 10 Oct 2025 04:43:34 GMT  
		Size: 785.1 MB (785148377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c9bda4db142150ddf32bef39d06b94d125883c589bf702cb02b297ff39f2a595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60714715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce914a0caaf81baff1e0bf336f88b050adf78fc5193edc7f2fb88d6bcc012ee`

```dockerfile
```

-	Layers:
	-	`sha256:0e93a43ffdc6454a38ee6eee73c37c6881580f352d03152e8ef60591e6b7199c`  
		Last Modified: Fri, 10 Oct 2025 04:17:50 GMT  
		Size: 60.7 MB (60705333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dcc51f87619c01901960ae1e13bcff779f3384ffc04d779dffe6de4d35c58ec`  
		Last Modified: Fri, 10 Oct 2025 04:17:52 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c32cebb92edd6f37d6e00c52effcf3531a10df53a97647711b18630b0f6b063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.5 MB (979526410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e2324f62274b44046fbd92360287237910aa4025f9ea2c2dae42377a7c320a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea461ae627ab7b7cd6d4b25cdf53fffafc54e65b4ff6ff3a02d3d49b91d96071`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 684.2 KB (684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a21bae08cf45f3689ecd30ecc6446aae60082c47632facd058cb8cd91a6915`  
		Last Modified: Thu, 09 Oct 2025 21:26:01 GMT  
		Size: 6.8 MB (6760158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eb69984a6abb2f7a2c8c70a49497dbdac46d19f02c4ba45bfb8e65d1b52c7b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 94.4 KB (94418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eb091d265588996d309a696050b8d873efa1a977c33604e5241d0745dae157`  
		Last Modified: Thu, 09 Oct 2025 21:26:15 GMT  
		Size: 114.9 MB (114893499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1fd8e39aed1e99b329b904170291216c4df87e9a05ceb6e27c4e277cef7e6e`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095a784b3b596b61762df7cc4a5b6b7c1eac9e65fe28df5b367b898945487963`  
		Last Modified: Thu, 09 Oct 2025 22:21:27 GMT  
		Size: 105.6 MB (105591210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaa47f3fcdb4ec2a9d6dc3dffc6e5120ff9e2adc87862b6d659c3a7d1c774b3`  
		Last Modified: Thu, 09 Oct 2025 22:21:16 GMT  
		Size: 378.6 KB (378568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c8c6a1a45bbff1319860478a95a64ccdd0c0ae9d251b59ce95cc74055ae1e`  
		Last Modified: Thu, 09 Oct 2025 22:21:16 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19515dadcdaaa740f70b490c4215ebc580a396e3c86fe1f5ab905ad29efb8fc`  
		Last Modified: Thu, 09 Oct 2025 22:49:40 GMT  
		Size: 27.1 MB (27097082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f171c14846542ed296c675afa9d8ea3c55bd4cea30691e02a185c8d9fb4d88a`  
		Last Modified: Thu, 09 Oct 2025 22:56:00 GMT  
		Size: 695.2 MB (695162942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:92516cf0ed9ffd640dec74fb1bbfb90d4c79374a05148b15e278e2eb2668b075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60645320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c39e9e9c9bcdf50a443387e6b7ba8e42b4a8a47706a66a5ed8ae0afa7371b3`

```dockerfile
```

-	Layers:
	-	`sha256:fe6d24a4cd4e06659f5d1719f8d4deb7587a6487e0e2db8e3a249f4b94a9e34f`  
		Last Modified: Fri, 10 Oct 2025 04:19:46 GMT  
		Size: 60.6 MB (60635858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6af18564ea9310b70fd7921a32ec73c1a5e689e84d5c4f2527b90df5a02b70`  
		Last Modified: Fri, 10 Oct 2025 04:19:47 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
