## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:762b2a20b2b34582ac75f6488ee1abf82e69758d229fc81392c33a98d554e0d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:33ace09ae17fbc0d3b7d0f1669dde23bf6e437b92906596597df39f407e54a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295774899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c7fc7283aebfb6096dfd2e79e918fc9d52d2347e19a961e674cc9c26073466`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f9f16d221b9a193b1a080b2673609f80f64ede41f3f81c206698e992ac9fa1`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 683.8 KB (683811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88f57e92d728e668d2ec085a2a883a4a34de7358c5ae73ab669d9d0dbd34242`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 3.6 MB (3563720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46c7bf8a560bdecd06b706f996ae07581fd85ea16d14584cfa8cec8aef4d2cc`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341fb3faa63f0489dab4f0a12e3b29eff9ce565faa7156b7f3d9055ed3ba6007`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f2ce02ff513de028c65887ea53630d7a99c801a501871898ce4c97695115ad`  
		Last Modified: Tue, 03 Jun 2025 13:31:05 GMT  
		Size: 123.3 MB (123309297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434c602a34bcd520302797433be6f8c41329d0a12bbfced7922b0ac74276902`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80f66809e8d851621b51dc33d9630198a62ce80e16f7feab75496a1f23798`  
		Last Modified: Tue, 03 Jun 2025 13:31:02 GMT  
		Size: 110.2 MB (110181616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3999dc1f9ecc560440d5247cd73447037c04c5053ce5b1f73f8f060a0ebe9e7b`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 346.1 KB (346125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b40755095da1c5c4d3434a4e38fe190acfc281ffa2d0da3d71cbcd14a05d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:46 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e955cd61a0672a29fcb7c5dd1cdb21cd12c405f549aee9fc4807c6eb9fcc97`  
		Last Modified: Tue, 03 Jun 2025 13:30:54 GMT  
		Size: 28.0 MB (27969498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:261a2d39729d32e8b987fb3094c7b6ab3bd6a46f34f4558c21546adf149a8fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23937163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c631e48c9639cb44d9a24863c6ece90fd0d8c5897d014cc98be1aac5f96565cb`

```dockerfile
```

-	Layers:
	-	`sha256:aecc145e6f9f2b7644fcea82b10b6136d467a4fa390b4f7f53bdbb796e2ac2ae`  
		Last Modified: Tue, 03 Jun 2025 16:22:49 GMT  
		Size: 23.9 MB (23919990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954bad2c0aa876fef2d7c6ba11ea7a47b0ed601864f1e97b3f1e776f949edfb4`  
		Last Modified: Tue, 03 Jun 2025 16:22:50 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4cbc4ee627009b2ba60e17d771f2b48867839d8def9e67a05a436021bb11ef28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284188180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa15ee14597b706b96d0d8e06362b7f7f6c546298e87d35feb594f45cbfcf17`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:3182864e52220424abbc2ed14f34194efd7a8651cbd58c9013d59badb6ce10bb`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 3.6 MB (3562006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30261ce10ab5a3b7dce5ba78a1a951d5652cbf529e166b904f1bd8067ae7ab`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3ede17908e49502f7fe6ff9399c21b4349b35f3533c331faba1f2970ddeecb`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1f4c48fa47caf9afea890bd995e3397de16a54fd781888ecbaa9b5688368a9`  
		Last Modified: Tue, 03 Jun 2025 14:19:52 GMT  
		Size: 118.1 MB (118081461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a93e6dc2b884b097ad111c9c09580eebb409db03ba379e3e847dc36468a587`  
		Last Modified: Tue, 03 Jun 2025 13:56:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111fa49d32c398c3cdb3a803afd70fc1e29cf19976c5f78d4abee039f51d5eaa`  
		Last Modified: Tue, 03 Jun 2025 14:19:55 GMT  
		Size: 105.6 MB (105595311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ed73042d776eadb29364537e29fe84b0364092210fc1bf8040a7d844c8092b`  
		Last Modified: Tue, 03 Jun 2025 13:56:39 GMT  
		Size: 346.1 KB (346129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b0bd3c3945caa5d7a8dbc804f7e2a188e63f662b849c402e7f95a56a190ed`  
		Last Modified: Tue, 03 Jun 2025 13:56:42 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405f57d0b137d304f12eac8e652319d0198fa221a68bc4301d89673692609d1`  
		Last Modified: Tue, 03 Jun 2025 14:19:45 GMT  
		Size: 27.1 MB (27061888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:493d435c02a0caf2dedf6b54cdc168604027057ec4dae0270750ae553c0850eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23959554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd462f2101777f41253166dcb282038b0ee7145ceb6dcbc4f545f1027769b970`

```dockerfile
```

-	Layers:
	-	`sha256:b21a7701c9bab0c6032fa0a14f10785e9d5d67e754a5695e3675922fa982d71e`  
		Last Modified: Tue, 03 Jun 2025 16:22:51 GMT  
		Size: 23.9 MB (23942244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:780925582b64d792eb1613df51e1564ce5df0be4d8524dd1a9733150be92dce8`  
		Last Modified: Tue, 03 Jun 2025 16:22:52 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json
