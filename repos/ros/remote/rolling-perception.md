## `ros:rolling-perception`

```console
$ docker pull ros@sha256:11468c851f5e7188d67d5a04f2d058a85f988eb58bde0e170ff7c1fdfaab8a03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:4d0408f003403561bdd5671e86f77a5a04de8895bd1d403e251fda5fa2383468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.6 MB (623626152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6714b4a319257d9f08fd60a8147e4570cc3db552386155c149327614682d45e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683ce39351d82fd950e092e88b264489382ee7a8011bb25a91ae065931834d76`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 683.7 KB (683724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3b9772f3202bbb08e9a737743bfada3868c76ea9cc44b353bf9b1deb0ac13`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 3.6 MB (3560038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9ce07c40bfee960a575dea3c30d31c04682b9fb99b7fa7238d0d2ddf23eb4`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca4c8456ef5db1377c36a0880dd7a288494a5cac776ca008c8f481539e99eb`  
		Last Modified: Wed, 16 Oct 2024 16:18:27 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032b417bf94d18d3f038ffdda1575d627239628cc4d017bebeea601ce15e2178`  
		Last Modified: Wed, 16 Oct 2024 16:18:30 GMT  
		Size: 123.8 MB (123784480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f9730083900838d53743e27311546041b1c9515db812aad84ceda8a05b1609`  
		Last Modified: Wed, 16 Oct 2024 16:18:28 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7364f5477bdc9da8a17ce52ab9e1dc99529ed027d60b900a55464e5c2c105`  
		Last Modified: Wed, 16 Oct 2024 16:52:25 GMT  
		Size: 114.2 MB (114150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d6655c69c5f870a29f002ad0bdaa1dbcf9ffc196cde9e412ea4d8b25eee6ec`  
		Last Modified: Wed, 16 Oct 2024 16:52:24 GMT  
		Size: 324.2 KB (324186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731937156a11bb4527af7ad606a98d20b233f49a0262119d0465397b4b762c66`  
		Last Modified: Wed, 16 Oct 2024 16:52:23 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465df9be9fcb873a8d873692c10b30345a14bbdb1bf033f45339a2086785af1b`  
		Last Modified: Wed, 16 Oct 2024 16:52:24 GMT  
		Size: 27.5 MB (27533706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b4a43fae3aa74e6eb617b0114014c706ae45ebd1af49f6f5785200ebbb40f`  
		Last Modified: Wed, 16 Oct 2024 17:38:18 GMT  
		Size: 323.8 MB (323834168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:90b2f2f6d76874d103f90603bf9185802fd168a2d5e1b08469bb2c404f80c688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42145363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c6925d25d09cd2bc7fed291f37e704284d67eecc9988717a0f131b7339dd85`

```dockerfile
```

-	Layers:
	-	`sha256:b5f9ea19c7a42cb071b4032834152526c0acea591bd25ae9c963ba413f8b1e7f`  
		Last Modified: Wed, 16 Oct 2024 17:38:13 GMT  
		Size: 42.1 MB (42135649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8d69ad2d9e423b3022007652ff42f5d26c6020c914d4966acd53fbf02262e7`  
		Last Modified: Wed, 16 Oct 2024 17:38:13 GMT  
		Size: 9.7 KB (9714 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1fe15163b5346b6f7e83c821e94755c58ea3dac48ec741d445b36dbbe0bcca8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.7 MB (566716133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e5f5ac7873a86a0a8be1ced235fd73a5cd1c453adcb7272f735e283aefdb08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75906b0dbbabb024c7f890638530898ee5c0c44e20c5f9b2843574dc92ee4e4e`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 683.8 KB (683843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f509c8e504eee35bdf2f7a4cbcc4941d472d9a497b7f511c549dc7c5b8a4e`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 3.6 MB (3559114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed51f7b48cfd97dfccaca6e9172453c23a61383c3cbd8b7db4643cef6c1bc5b`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969caf6e5719f51692ea48756b21810e0471a7e3f778cd747e55d3becbd5e265`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ebdd9e47436c4391ff4f96f57db9ce3f74dadcba2a10820af55318e09901a5`  
		Last Modified: Wed, 16 Oct 2024 04:17:15 GMT  
		Size: 118.6 MB (118568656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6cc5189b8f5cfc989c33a8d416b71f388bda6054059e70948ed2ee8f2d8eab`  
		Last Modified: Wed, 16 Oct 2024 04:17:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c8f574aa06a037708ba67d3b5f9f6b218b47bad90f05e0e4c156e1d487fcc6`  
		Last Modified: Wed, 16 Oct 2024 06:08:59 GMT  
		Size: 111.0 MB (111008282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449d9067c3fad38e318f960312845df4672da2f2a6eca44113f104cc8f3a6efa`  
		Last Modified: Wed, 16 Oct 2024 06:08:56 GMT  
		Size: 324.2 KB (324199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e46397b7857aefb2727930b24e9a4af2da410d2aab6a4803ad3384ba69f8be`  
		Last Modified: Wed, 16 Oct 2024 06:08:56 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc10351ba64d3e3d15709e92ec43f1007366a864bd3630b21bc9f1416c9932`  
		Last Modified: Wed, 16 Oct 2024 06:08:58 GMT  
		Size: 26.7 MB (26685087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875dad34177699a1ad9d052a5e0da8c60845c9794ec4e51efd4fce3eaf0e0052`  
		Last Modified: Wed, 16 Oct 2024 07:13:20 GMT  
		Size: 277.0 MB (276996204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:d769ca9fa51005ee5143628dfe16ce143eed7a8c82dec7fcb543147c1c03b0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42143534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127d94eae1e1747f1fa83b3257941445a4a9295d8c1c64bcda0f6dbbec007bb6`

```dockerfile
```

-	Layers:
	-	`sha256:c4b563ca2df630465fcdd1caa3ad41fa150d8e738263477757d374b3bd7241ce`  
		Last Modified: Wed, 16 Oct 2024 07:13:14 GMT  
		Size: 42.1 MB (42133740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f008014f2d9bb45276a883eb3faf7d63538db4ef353b1519fa6a15b4a61381`  
		Last Modified: Wed, 16 Oct 2024 07:13:12 GMT  
		Size: 9.8 KB (9794 bytes)  
		MIME: application/vnd.in-toto+json
