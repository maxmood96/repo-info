## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:f937665254139ed2b8f4808ca4c548e2f2070cf5c608e59646b898d2a5f236d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:d91e519e95f0b8b2db0b4cdd27fd945440d3188145ac8ee6f8076e298e30d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280008678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91424a21f01d49712381ed4ec9492922a1c592f0db2041adb37fb139d23294fb`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627070c22110350c23cc50089a841b8c4257eb28ce66dea53acf5039c3230e34`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 1.2 MB (1198823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8728cedb8ba29fe02ce989c70421066de64c666b6a99582f25178d88aa15436`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 5.4 MB (5361869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127793489f3bb50eb05db40cab2ed332c4a29fd05b34138da31541fbd7e63b1`  
		Last Modified: Wed, 16 Oct 2024 16:18:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87538de7941b612134ab50edd68c6e0f52c6f7ddfedb7fb0c5130b6a6ca0ae77`  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11090410af8961388a4a44a929c9fbc8eb6000dac2075e09c4392d7ec0a60ae4`  
		Last Modified: Wed, 16 Oct 2024 16:18:35 GMT  
		Size: 177.0 MB (177040113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e07f0bec1e43c18cd93acea1d11ffd7fc0409d8b06afa3a0c107f8ad80b105a`  
		Last Modified: Wed, 16 Oct 2024 16:18:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a60a3d4f5d8a2ba79f6b17c46970171ea46e7dbc4f8a206d7ce90d28b64e0`  
		Last Modified: Wed, 16 Oct 2024 16:52:11 GMT  
		Size: 50.7 MB (50721153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadb065133b9b742d6bbbca49aa896b94a18f93aa7c33c890cfb3e6b73cb0f53`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 331.3 KB (331289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272267b4195536b2a923055b1e37c0166a7414c13ab20177450be71783a6c666`  
		Last Modified: Wed, 16 Oct 2024 16:52:10 GMT  
		Size: 916.0 KB (915988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9d9237bb39bb101226779bd2f01dab6f3b6aff4e0c8fc10c46469431cf4046`  
		Last Modified: Wed, 16 Oct 2024 17:36:40 GMT  
		Size: 16.9 MB (16925916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:3cf0b425d1c22db00808aeb39d5d3fde0d4c6e39884070e8146afd788f768dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29491473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ac62215124cb3578c207e6bd59eb20bd2e39d0f9bda4dbbc9941c26e96e0da`

```dockerfile
```

-	Layers:
	-	`sha256:34dcef24a3df80a39bae3735bf5e3f9b3fa6f890723da83cfe868a9cb3fb217f`  
		Last Modified: Wed, 16 Oct 2024 17:36:40 GMT  
		Size: 29.5 MB (29482145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c06faaa779bface7b979a8bb2887c7c3afec9c59dd4fd4099851c90bf5426166`  
		Last Modified: Wed, 16 Oct 2024 17:36:39 GMT  
		Size: 9.3 KB (9328 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:e66a7229a6e41943d5d92e32ced3e41419860b76577ae17ae49ba0fc3c67fdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243313694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad79328eaa1883562a8fbae9d2c4d9d0385591e22c72bad81e62ded14ffe5fb5`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:2a516110ed97a8a9c62bc914fa45ffa19c58e02fc5aa3b09f5f24402e2014fb5`  
		Last Modified: Wed, 16 Oct 2024 04:07:09 GMT  
		Size: 15.0 MB (15025281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:68570be7ced8626254f62462eeb9bf9b465048b44fecc79effdef5f9832b7262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29246325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b71494b6d37b215bf54b5a742df626a31af502742d8a95164c4c62e6174c1`

```dockerfile
```

-	Layers:
	-	`sha256:32b49dd89be20c5af9d2aab4e96989d4572aa7ee7094c8a4e7e95d01ebc770f7`  
		Last Modified: Wed, 16 Oct 2024 04:07:09 GMT  
		Size: 29.2 MB (29236935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb4bda7c098c3bbf1cc0d3c49cc430385167dc11410dddb7b747b5ae1e4c517`  
		Last Modified: Wed, 16 Oct 2024 04:07:07 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a2656272b0d5a0339bb058920703f0e459958a14a563fd5399f30400463f95fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266714763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23da81ce6994f2b702cbb2eb2e3cb1061e85cde4cae8c6ea5f2b85042e3e7e22`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:562ebad0d899b2bb76a94924c63b4828f32ec62d002e22bb27c12ef016824b17`  
		Last Modified: Wed, 16 Oct 2024 06:51:19 GMT  
		Size: 16.5 MB (16525547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:5e0c69f753483a9b0aac48698d4332e7dd42daef7d96b5d8f966d3ba1af2a7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29440689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703aba797d97946e2f244b1a36067f5cb7dea8e33bdb3644600e74634560ad2b`

```dockerfile
```

-	Layers:
	-	`sha256:03d0a06781a1903992c1a35c53b2b80c4e66ece9bb6315275774522a7804df6e`  
		Last Modified: Wed, 16 Oct 2024 06:51:19 GMT  
		Size: 29.4 MB (29431279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aaba00a0cedf7f43546495e768fea4c0730efda9d4d573bbd8882fc6494f149`  
		Last Modified: Wed, 16 Oct 2024 06:51:18 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json
