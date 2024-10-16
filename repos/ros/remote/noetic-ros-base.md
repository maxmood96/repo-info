## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:992d4705e197ac6bd3b72515b5ccbbd89ea1e6f70273c7dd48a3f7cf6672c780
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:c64e618fe3f69ee3215a13e75af121030f5f2f4488c7946c7f30d0e3b5d178e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263074418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b0870daa11b6d9466bca105cac304479054ef23f54c9e852547fb2a1ac034c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce9cbddae4588e8fc7fbd8a300da9a758a948cd04ec3b1368624a184de13e71`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 1.2 MB (1198681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83ce5ea8c74b3a8fcc0da7e664a139640a83469a255feedac928b11410dee6c`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 5.4 MB (5361806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10601306d61ee865bd7a1828296a8cea1d16886115c83b655becfee0c1eb596c`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1783bc90edda4ccf720a22d16ac2d0d51ddd52f7adfb85b8e78f8b55df2b12c7`  
		Last Modified: Wed, 02 Oct 2024 01:59:36 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53631aa1770cb44838f8b3c2ec05c4fa0d7f3448b7902d982a8c4bdbc99a32d8`  
		Last Modified: Wed, 02 Oct 2024 01:59:39 GMT  
		Size: 177.0 MB (177026126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073ca5c651827208ff792ccdfe8392da87f425c6a0a51a8da7674ad1f0b38f45`  
		Last Modified: Wed, 02 Oct 2024 01:59:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a4c7db9a2b67fc82092197aa045b09b0d18aae3b9ec8679436fb272da6a35`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 50.7 MB (50728246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7ae8432b253ca6b11586d40ec216b7f86f0dbc9ab8613908376e536dd39669`  
		Last Modified: Wed, 02 Oct 2024 02:59:42 GMT  
		Size: 330.1 KB (330107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35406b7f105a6551bcad94df324847d50717d89035510b0a9e4948b93122311c`  
		Last Modified: Wed, 02 Oct 2024 02:59:42 GMT  
		Size: 915.9 KB (915935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:9ea2192ed22fc55edb39258fb4b661bed350aa507a8db70d61dd8c1c2430fc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27600780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfd49779650ba0abaf75b87c3c1df5267b684cc8b9f3a0265cf9efaacb87afb`

```dockerfile
```

-	Layers:
	-	`sha256:e72e5164e39a8570cd3fa8358feb84fec97428ae31141724867c75afe98590b5`  
		Last Modified: Wed, 02 Oct 2024 02:59:42 GMT  
		Size: 27.6 MB (27587123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0418fabe623fcfafc4fa0ee2557167ade6720b6d3064a54e1e2580f787e156f`  
		Last Modified: Wed, 02 Oct 2024 02:59:42 GMT  
		Size: 13.7 KB (13657 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:665efd9c21f6e7dd7e1ecd97e6f9b421775e63b55167828fb04dfdeff26aa088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228288413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bd77e448977f3464d7b7411f33d0f7e7db4181e0c68af48c71a9bd3c34404b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf021129bf98dbf1d45831c02f005365ad9f6e65f2c00cc8e5e4b795dd7b81`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 1.2 MB (1198819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c18aaec3d60d50757f8d4e610ff18dd91bb54b38b2a1624ba22963deb0554b`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 4.5 MB (4487363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76988805d937c32e95625d04f6a3a561ee4feaf82eb48fd5d9502e1c28e7c082`  
		Last Modified: Wed, 16 Oct 2024 02:32:38 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b15be849ecb15e904949ad5b4b76855e4d560b6c8a711e75536ff0176a9352`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbae15540814491585c39eeed2e610a7ce8f10980b6234bd9e9e28860e7ff27`  
		Last Modified: Wed, 16 Oct 2024 02:32:43 GMT  
		Size: 157.5 MB (157517036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c61b02ccda3db25327a374133aa1fb86419164045f707000d1b8c7f6e896e05`  
		Last Modified: Wed, 16 Oct 2024 02:32:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b450c86af2668fbfeff608edb2127c5008dce25e7960e258c77b4050f665b`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 40.3 MB (40284152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c38799fac5256ed234e4fe653153099f46c04672bc4994aa6bf7785a1726a`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 331.3 KB (331276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a225158d1859182a815bd5a7ba8429ab8ab1bb51a4db5ae89222bb30b8a1d0ba`  
		Last Modified: Wed, 16 Oct 2024 03:18:51 GMT  
		Size: 846.9 KB (846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:9bc66574adabc536cff0ca51f33d6a859efc2166256401492dbe4d2c742aeb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27371952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778fd253c2c9f0084aad03ac5f3d8d49a375c0ac42f7d25966b0cc12d841f319`

```dockerfile
```

-	Layers:
	-	`sha256:158c083e6830094fc49e0429b98e613165957001bccd5c321f312f6b09d3e584`  
		Last Modified: Wed, 16 Oct 2024 03:18:52 GMT  
		Size: 27.4 MB (27358168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed656d35de762e9baed95088a4d31b34a03cdc9ad04dccbd81dc4ea4b1763cc`  
		Last Modified: Wed, 16 Oct 2024 03:18:50 GMT  
		Size: 13.8 KB (13784 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e317c94efc821597009d9fb3fa5a0db8fee08a8a9d010852986b9c13e6988c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250189216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03e6c05479a847440a256d79340ecccf68bee3d3c012b07dbf18b94a8d13193`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7692d171772b08f5a9d0dc4a7b1ae51b870e77829dd8e7c0a62b1f9817239`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 1.2 MB (1198705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f9119823a2bf386bf829a11e39290d3f3441a7210eb39b4a7342f8481643ac`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 5.3 MB (5342090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e39a30d323d034154408ec363b1f3afbe72ed9d424be55808a92a6309b120d`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da5b2e66f57fc3b781b4d81c9514dee9b08decd9306330cd58833771758139`  
		Last Modified: Wed, 16 Oct 2024 04:13:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70554c999e53a1aad7c55aafc6f0ddb8095bd7b1eb3c0dc38e07aec7896ae2cf`  
		Last Modified: Wed, 16 Oct 2024 04:13:13 GMT  
		Size: 171.5 MB (171452633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acdb47098b878011f0003ad6c94e50363b2156e2bb6951fa21f9012a17f1bcf`  
		Last Modified: Wed, 16 Oct 2024 04:13:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2103d332713160aa2196205de34c2914b0072edd6edfd48482dbb2d4a3d6`  
		Last Modified: Wed, 16 Oct 2024 06:04:28 GMT  
		Size: 45.0 MB (44990886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38185782b6690ae35720744a5321274a8651237c9d6900cebc10a000409af2e5`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 331.3 KB (331287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843243ae0d09c7eda36f37ac0bc9801a113bf37beb05fae37942f88241e275c`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 897.3 KB (897322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d7f07c89fc0129e2bc9f71244b1268d8bb57d4dd4bb75c39e92aff6bb4f70694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27558911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b6391e8cfeba2048a60ff13c4dd745bfca46b0d85bce4c5e87c1cc065abe62`

```dockerfile
```

-	Layers:
	-	`sha256:8dc7119ced5dc25252d4e6119082fe12de268a860443343a56495e723d0bca38`  
		Last Modified: Wed, 16 Oct 2024 06:04:27 GMT  
		Size: 27.5 MB (27545099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e2265e87cc5692dd2c4402c7bbff074b3cf227f920f9cc95d923bbccec1eb7`  
		Last Modified: Wed, 16 Oct 2024 06:04:26 GMT  
		Size: 13.8 KB (13812 bytes)  
		MIME: application/vnd.in-toto+json
