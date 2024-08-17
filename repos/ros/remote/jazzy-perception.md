## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:622099c2a0224b07ab20ebfca3ff0212d31c9a29c555d186789b3a10a0309d44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:9721a557af20ca112f87b3f4f4f2c90d185c8b124ce14919da6ade8893aa6365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.3 MB (622307110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62e02d29aa74c5427677f8c369119c9a35ea7ac3b1cb6681a94e7cf365a3444`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231ab47c15a27b3ce71add215647fa446f7c20c201669fcc618384dd6d359f`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 114.1 MB (114108371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2ddbfff71328815b9d462dc8736b0b948827a0fe49d01ad659e492fab0d824`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 328.5 KB (328524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba5e4c7da887eff6854454625bdb4da2c0747b9a9ec347d090469b6f6b92689`  
		Last Modified: Sat, 17 Aug 2024 04:07:49 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b1803d5e9a059d8305e0a234086c642f09dc8f07bcf7f2107957f9fe4190bc`  
		Last Modified: Sat, 17 Aug 2024 04:07:50 GMT  
		Size: 27.5 MB (27526250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c66a41979b8169ee20d35dbcff1aeaf0501bf4ed5470b9b381cfcb0fd4dc936`  
		Last Modified: Sat, 17 Aug 2024 05:01:02 GMT  
		Size: 323.9 MB (323882501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:070a4a87ea16ad69f88f56641333bbf78fd659711d25027a5216955b7d49b4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42087818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3112ecae3386112a7ceb210652c2afc032260796e595f81c45a31bb1e27fc6`

```dockerfile
```

-	Layers:
	-	`sha256:693b12a1d382eb76cb7deafc15cf40868d14845be164c4f9bc1f0847a0477068`  
		Last Modified: Sat, 17 Aug 2024 05:00:57 GMT  
		Size: 42.1 MB (42078164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235fb0f78ea7c34accf9303c933f15d8ceda456f5f94467e1f7dd4ecd9f0346f`  
		Last Modified: Sat, 17 Aug 2024 05:00:57 GMT  
		Size: 9.7 KB (9654 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:928a5bf6ddb51c9be15335e01b9fc6554af88d911535fbbc7d30089bd250da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.4 MB (565376585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9537015f66f36b879ce98894ab02cd2a3f38059e392ebfc05106da4bb84e7a82`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a631a99905201093a192b96d6b9344a759bab04da8001fa7f2bd7df0eb20f436`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 682.9 KB (682877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2beccfb7f73210b53f07f3b786019cbd7b54faebe00e559e8511b67575df29`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 3.6 MB (3557897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fdcea445bfe641533a4e4eb218d30dd044e1fb979c59c9ffb8d6d41c654c4`  
		Last Modified: Sat, 17 Aug 2024 04:01:16 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a42c4dd663c96d6c786e46499dedfb50ea24fb2702a2108d9a94cb3aa990a`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dc6c6c7dbc5ee2a9530e7f4b5388510310ae9b6d6fe273f77997dfbdcfc0ba`  
		Last Modified: Sat, 17 Aug 2024 04:01:21 GMT  
		Size: 117.3 MB (117339297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d6f7979d4b52bb159a593e4dbf4ac389e95d564ab873898d95f3809725b7f9`  
		Last Modified: Sat, 17 Aug 2024 04:01:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21228be30b147a777ae826d9686d0c9e42292fe8f2e03426afe429515f4e8e4`  
		Last Modified: Sat, 17 Aug 2024 08:15:42 GMT  
		Size: 111.0 MB (110953219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6730f5ca772fa791ca3b2c695e4ca27011626ebf0aef90fc361e3edf1d31b31`  
		Last Modified: Sat, 17 Aug 2024 08:15:39 GMT  
		Size: 328.5 KB (328525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78251190870174ebb8fbf17380a81620385d4421f81297beccdd527597018dab`  
		Last Modified: Sat, 17 Aug 2024 08:15:39 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b0f759b996dd0bd6d43025f64cc3d81c3b8002e19cc1f25c6040eeeab11c9`  
		Last Modified: Sat, 17 Aug 2024 08:15:41 GMT  
		Size: 26.7 MB (26672404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa526b246d4416acf01e3ad78ed6b4629c8d77659ce38076d013fbe4ba6d5793`  
		Last Modified: Sat, 17 Aug 2024 10:45:21 GMT  
		Size: 277.0 MB (276993784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:05a328a409abee26b7de62a2de28ec757eb3fa9b912f202c52ccaac48bd55c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a8b870b0256b3fec350104795c8b73aa62b8a67e94190842bb915ff5f82100`

```dockerfile
```

-	Layers:
	-	`sha256:04d21b49b8f2e490ecfe40e995c0a871508a5ba2e5938c2458deff522c59d61c`  
		Last Modified: Sat, 17 Aug 2024 10:45:17 GMT  
		Size: 42.1 MB (42076257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1bcf5fcf24b91b432f44e859e425308d0a46c3f7a0c6fd4bedbbad3542a7e4a`  
		Last Modified: Sat, 17 Aug 2024 10:45:15 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.in-toto+json
