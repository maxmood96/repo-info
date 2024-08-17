## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:b033b43f1b8f568f1aecf2f1a6491358487e3aa72def88bea5e411520d67e757
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

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

### `ros:jazzy-perception-noble` - unknown; unknown

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

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:64e6ec792eff7c3d11f24baf60fb0eba99c3a7f093a70b8ea40bb35301cd1c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.3 MB (565254776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccff6588f7c05f70d285128536b8912d546e14653184acae07d04443318b33d9`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bcc4261342272a0b424b2401e4e9c1ea3ea48e2a0be3cb37d3d60ce914fda`  
		Last Modified: Fri, 05 Jul 2024 20:47:53 GMT  
		Size: 117.3 MB (117265893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64869f6a58555ee8828021c2ebca140ab2ebc780b737e8bcf35b2779cba239`  
		Last Modified: Fri, 05 Jul 2024 20:47:51 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04377fa51164b0ddeff26326acbec8bcf286902f25984a00ad5b9770309eaa5c`  
		Last Modified: Fri, 05 Jul 2024 21:19:13 GMT  
		Size: 111.0 MB (110952468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de20866bb5b0e8c5cd02eb7bdafdbf97e9d2c76e843c86834718b03e927523a7`  
		Last Modified: Fri, 05 Jul 2024 21:19:10 GMT  
		Size: 320.7 KB (320662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b3fd79a1b761f8269b08686ff60c0d760bed1b9e7081c0572fbc0314c0d8`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ee15bddfe47248908eaa975ae8811c53faa743b28e8556d61b5a7bf116436`  
		Last Modified: Fri, 05 Jul 2024 21:19:11 GMT  
		Size: 26.7 MB (26671682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f292cc5e2c1d0ccbfad936c8fff806ac8f3c83d0f44fe829959695f7c85aa114`  
		Last Modified: Fri, 05 Jul 2024 23:53:01 GMT  
		Size: 277.0 MB (276955400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:e405f8232bd606164745daf0a13194b463000d9f73fd49adc7e7bfc53d820977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41863716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2c2b8f2ba753e63be83d21547cf8aa3ceada6608e6b30a6f366d597e6f53e9`

```dockerfile
```

-	Layers:
	-	`sha256:726cc8db93af593d08fdec232f81afc286061c7296a3e4cda432fbf27531f650`  
		Last Modified: Fri, 05 Jul 2024 23:52:56 GMT  
		Size: 41.9 MB (41853701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7caadde2ffb44d7d9da6c08b609e069bf4b6b76a5584d3e68679bb422484c28`  
		Last Modified: Fri, 05 Jul 2024 23:52:54 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.in-toto+json
