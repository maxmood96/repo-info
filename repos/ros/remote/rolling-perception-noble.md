## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:8bd1f1a59baba9582b49c3f0635b53b7b3c02d7548f3e929584992d683c138fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:730a6a1c912c894414aefa47596f08ac82fb0ec5655d51f42a34965f96c9980b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1090057994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26ec79acf8d8dff7745be6903062a45dfc2ae41eadf7e45a64ecf53c0aa902f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV LC_ALL=C.UTF-8
# Tue, 10 Jun 2025 04:58:20 GMT
ENV ROS_DISTRO=rolling
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 10 Jun 2025 04:58:20 GMT
CMD ["bash"]
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 04:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.13.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29647462da8b7248faa562686afd7d3260fe5f9ebcad7199b3fc188188ec2cb6`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 683.8 KB (683831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8cf1676bf842067dd91d4304cd9e00b68f99f9e3fdbb5aaf3bfbd7f42b6bdd`  
		Last Modified: Tue, 10 Jun 2025 17:40:51 GMT  
		Size: 6.7 MB (6745430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a2963d62bf807e13e004c105aaff40d7c2b5bf0ec34a98c73b58948b204ebf`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 94.0 KB (94036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086be9840220e0654dbe8ca646f01473644e65977961a84a0d7fd5ef2163ff7c`  
		Last Modified: Tue, 10 Jun 2025 17:43:16 GMT  
		Size: 132.3 MB (132309948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15678d18204d5f60c2a8207755206c234b0e17d078a20bf91a9d36d9cde82f4`  
		Last Modified: Tue, 10 Jun 2025 17:40:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedfb4bf8b8e902565ca4bf76bd01fbd97589a22c2575b1a0bf2ce1556469bd4`  
		Last Modified: Tue, 10 Jun 2025 18:07:59 GMT  
		Size: 110.2 MB (110181766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590c8430593334b1f6946c46594eeb49e569c4926cc781b2fdcd1953e74a0901`  
		Last Modified: Tue, 10 Jun 2025 17:54:24 GMT  
		Size: 345.2 KB (345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778a971a98427a1b752d46f529f10ee0f7205bba5c70472f2cdc2497640cb32`  
		Last Modified: Tue, 10 Jun 2025 17:54:28 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a12a756a3ec6476a14b345873c04ca4092bad41b026c1645cb18909376affe7`  
		Last Modified: Tue, 10 Jun 2025 18:07:57 GMT  
		Size: 28.0 MB (28033477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33b7eba10116f6fd513a1381fe487069fb876edf9325f201928f5b8aafd979c`  
		Last Modified: Tue, 10 Jun 2025 18:12:31 GMT  
		Size: 781.9 MB (781946296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:dd9f70275eeec1f2defa103f749ae272651088c127c5a31f4e448c4924231598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60722368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fa4a3732416f7ba7d6156f372e5a0b5390269e3c58db5ba7df0223048fe07b`

```dockerfile
```

-	Layers:
	-	`sha256:dac54bf38ec26753c0aaf86dc2b25ce19e4e4222be131746006eba026efe2133`  
		Last Modified: Tue, 10 Jun 2025 19:17:45 GMT  
		Size: 60.7 MB (60712964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59459eed1f339eb69717821235d82120f7283992fb21b1f20caf57633459b4a9`  
		Last Modified: Tue, 10 Jun 2025 19:17:46 GMT  
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
		Last Modified: Fri, 06 Jun 2025 13:56:56 GMT  
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
