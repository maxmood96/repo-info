## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:adad8d1b38cfe98f399622668a70ef29eda149b3ebbd3f2ffcfdf34c55fde0b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:c61fdc63cea06cdd8f60b18946b68f880d874335e1d20cc0d1314dda5fbc8753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324648965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82552e91249d1ba40267d08e9383d38caed5b1e1f93af3ac8b3942ba290f124`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 10 Jun 2025 04:58:20 GMT
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
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2081cac45e5fb7bc52c7bf496d2ccc3433f84dd8702adc9fa84d467cc2be5543`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 683.9 KB (683917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fb1361c757ec00d31a8c6c88058fd62b23da12af4290edf2d3b2c636f6da5a`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 6.7 MB (6746865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4540fb962b4d5de83708d3245134aac24f8adcb8d8457e317648dfe877db60`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 94.1 KB (94146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eebe16a8832263871186c0dda7eaada9cdcfd4f1a4bcc90feccdb47acfff940`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 148.8 MB (148814487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda935e56c9a4a7f7f77e60fc31b89aa8dc68da689983df8cab450bf7bace1b`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31523257a1ece06c9814d06f6f4500a1508b114157f084262f1375ac4b301c`  
		Last Modified: Thu, 09 Oct 2025 22:21:38 GMT  
		Size: 110.2 MB (110186408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0540c997b5b21d64ae334358cb01b6ad38b6e430b4932715c3df365b46e62dd`  
		Last Modified: Thu, 09 Oct 2025 22:21:21 GMT  
		Size: 355.9 KB (355919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a89c2b76c491ee8a948ecad02d5f072b7c91d6cb9aa7b9250b70807a74c3e4`  
		Last Modified: Thu, 09 Oct 2025 22:21:21 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdbe5600458c88310171992d7be5d531219154f5349a6bfa4c66e1ee540b97b`  
		Last Modified: Thu, 09 Oct 2025 22:21:25 GMT  
		Size: 28.0 MB (28041410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d6eea44b9c24f7c2277ddee36ee144ce2858450f7934aa27732a21b7a25edef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25599452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6557af2b42004ea87a0bf383c8c533a0c62815056822bbc1816d05225dc8aeed`

```dockerfile
```

-	Layers:
	-	`sha256:2d558d2bcfa4da04ef1dd696c16c1da7f1cb7779cb63a43f7fddc37daf2b413b`  
		Last Modified: Fri, 10 Oct 2025 04:18:25 GMT  
		Size: 25.6 MB (25583044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe3becadeb1f538cf54541762d114906f48808d1c27f9513c5602f4139c48fc`  
		Last Modified: Fri, 10 Oct 2025 04:18:26 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a326b460e7303396f216281d8be53cc3a0e043173a4fb3e857b0381302065325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312619515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e257454898276e987dab05d31bb9139c5b6d5e7df250e68fa08bf664fbba5027`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 04:58:20 GMT
ARG RELEASE
# Tue, 10 Jun 2025 04:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 04:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 04:58:20 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 10 Jun 2025 04:58:20 GMT
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
	-	`sha256:14560a455baad8eacfe612b059e56e9c5ca08dec61a49e2ca1d556759a08beea`  
		Last Modified: Thu, 09 Oct 2025 22:19:37 GMT  
		Size: 143.1 MB (143142590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc9bd3503415fa5eb2be4bb24bbf854e74951b39a17b36da6a34665776ee9ce`  
		Last Modified: Thu, 09 Oct 2025 22:19:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e0cb3cad29da748fe594c88a3719b3d1430a411f3ae08a0f829caf26716bb0`  
		Last Modified: Thu, 09 Oct 2025 22:21:27 GMT  
		Size: 105.6 MB (105594578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485768f0ebc63a01498da99077e40e13951c1e733cd5250949c230159dc378c`  
		Last Modified: Thu, 09 Oct 2025 22:21:17 GMT  
		Size: 355.9 KB (355911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e331a5c34e96c531bfd92ba0076334a10f4831f68cb6ee87753ed4a5bd786bba`  
		Last Modified: Thu, 09 Oct 2025 22:21:18 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a428a6dab2527ff03838d1a6e14d7e2f3e3f28e30e4d2c03d172c7f4d93581b`  
		Last Modified: Thu, 09 Oct 2025 22:21:20 GMT  
		Size: 27.1 MB (27123310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d1dca904577beb8be94b0adec66da4b1875c614b0a2c2cad655026ed551fdb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25622046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980a1d9597fa9484a6010d3aa6c785e49def7a38b4cb96a62cf77a4b203d102f`

```dockerfile
```

-	Layers:
	-	`sha256:af18c7872ff92f1f0ee5d706009354731942a8a4fda7cf09165c88d774a1ed1e`  
		Last Modified: Fri, 10 Oct 2025 04:18:49 GMT  
		Size: 25.6 MB (25605502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c486b6493e8e69c219c3558d0f2b7870216e3310c177ab5003f911ae8067255a`  
		Last Modified: Fri, 10 Oct 2025 04:18:50 GMT  
		Size: 16.5 KB (16544 bytes)  
		MIME: application/vnd.in-toto+json
