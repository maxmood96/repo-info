## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:798a723225796a1bea8735d954a38035bb946cbeee11c71640db01677d92ea8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:dcc537033332d0b6d529fcccc8cec6d8dc1f36f9989411faa05b2db621124c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076852624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7afaeb0f6fda19fcbdf3f1dbc88ef35e35af0cb057e4e6b3175b5a71d2b376`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec2bd3b8a8f3149ca52fdd8464cc064b20a97e958bb5eb957e5b7915305000`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 683.8 KB (683801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1b31239b2b35443682de4bbe0887e0c643f5eb132ac575e10939de024389`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0363a0b27809e7e539adb870f5b03b5ca8f2306972a10b327fb08237cbc8d`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 94.0 KB (94040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eccfcfedb004370eed4e1c1f60b458a47d4e95994d4a128760d0914abca62`  
		Last Modified: Tue, 03 Jun 2025 17:07:49 GMT  
		Size: 120.3 MB (120308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969676f34d01f0babe0b34b6b856a9a446b5d4eb7c892d7518f26d14ddaf5ee`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3954bf150c0d49e6d74db1a5d2b4d6570c4ab4c65b9a577104b7ac61566b3a7e`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 110.2 MB (110182190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba3bab3f8fe24c8fc9585595879d8f6f868ecd6478ad3709275d08bdb302d3`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 345.2 KB (345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a6a75acc942e5de996b2186911beebd15b860314a71ba703deaa5f6aeba1e`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c847ce82317f1f015c442ef92e2df42c44e8c72d961ad6f436cacb503d5e2d5a`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 28.0 MB (27970572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10db0817839e16c700162efb170904730f0a5f267c8b1dfb02132ae47cace6ae`  
		Last Modified: Tue, 03 Jun 2025 19:22:31 GMT  
		Size: 780.8 MB (780804434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4639866a8c7e89c0627770661bce6147387c4460994d2063f1f9a8b90a703b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adc09ae99fb26a1a7c4010d6965a055c8f4f38fed6d35d370b24450344de616`

```dockerfile
```

-	Layers:
	-	`sha256:3eeb62ea365d75d0b41c42c28a1718ccfb2b7c215ac219e276340a34770697b7`  
		Last Modified: Tue, 03 Jun 2025 19:18:55 GMT  
		Size: 59.8 MB (59835922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86825c66abef002e8378d3a94a98d2030e186d2c2388d5f0a48386f23a076619`  
		Last Modified: Tue, 03 Jun 2025 19:18:57 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cd2169194fa099dbd8f1e3a2ee6b8ce97e195846976927493208fb6ced657c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.5 MB (975499606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98cba738a75cf8b2c8c5677e9e1f984253f10844ae2a5fdc712b8e5a6b69082`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd2483f06750140b5ef1d9528213984e55b6d22ec6260f43ebb6d9d32604e64`  
		Last Modified: Tue, 03 Jun 2025 16:24:19 GMT  
		Size: 115.1 MB (115069346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff94e561c546a1336514aa0a8683915423278ab9bf7fdc6580fcff40f64e26`  
		Last Modified: Tue, 03 Jun 2025 16:24:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee15e60a6b4f2e94d7ea44ffadb43de986c57c1efd5949178c6e8ca09725bf`  
		Last Modified: Tue, 03 Jun 2025 17:15:35 GMT  
		Size: 105.6 MB (105595486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba8562f5f48d7a0d879f6d9ddad45ef49cf00bf690ac7ef334d9c9ce7091bbc`  
		Last Modified: Tue, 03 Jun 2025 17:15:08 GMT  
		Size: 345.2 KB (345215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b24a6aa92e176ae9c16c4107cbfeb29fd061d0e6317e95406c3218cf08e96`  
		Last Modified: Tue, 03 Jun 2025 17:15:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523672174b6d88922a7eebb2d1ebfb5361bc77559dd09c08f9c9cbe7a855604b`  
		Last Modified: Tue, 03 Jun 2025 17:15:11 GMT  
		Size: 27.1 MB (27062440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10971441dcc1bf6a5bd937e6f581e951b5c355290b9aef4eede1272cd6736eea`  
		Last Modified: Tue, 03 Jun 2025 18:03:04 GMT  
		Size: 691.0 MB (691035285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:be61bcfdc93c74a523bfcf94742a01a90344c0bbe930967c91e7159912114a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59797071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00515e5dac7750558c15a136132a6d448db12534485b39a213c26ead1efa735e`

```dockerfile
```

-	Layers:
	-	`sha256:931685824977a3f5db5072a45968a8f852d5b5acffd76251688e161a5ea5dbec`  
		Last Modified: Tue, 03 Jun 2025 19:20:43 GMT  
		Size: 59.8 MB (59787587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8588f456d0c75104e9c4cfe44540e8294ed344675783209e1e46b80f0c9e389`  
		Last Modified: Tue, 03 Jun 2025 19:20:45 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json
