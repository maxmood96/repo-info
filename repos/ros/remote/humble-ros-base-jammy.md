## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:80a4f6329aad64f14b600133cb3fd279d0bf666feeca5abef3f10bb41b0916ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:252e7914962d04ea3c1e0b74a2aee993a0810a2c7b0e4380ca360510d7d11c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262008279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b07102ad8990d51397310a5c2a99ccac61df66d6f71f7006855345ba9af8c7a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe16f16e758e935c1c96db55cab2c8fcb9333349a3dde4d5d817fdf4906b50e`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c146a1c76f7bb3f9c955ea3af947c7b804cd5620175cabc85202d9c15f7ae4`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 3.6 MB (3624644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63aabead1b305894335a0b5bbab1c50c1cb50806eea408b18ce12ad5abb3e15`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b9e6737719d4f9c92b5df085885635291d9e9b311a874bcbfb06d5b277c0f1`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0d5fe24a834743f0e5ab1fe4b0d2f1fe9b96a3f455381a42089c2c16b29e0`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 106.5 MB (106530091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff204289c89177613a9c9282e3cd07301d68b6bc8e75625994eb96d25f7ffbad`  
		Last Modified: Sat, 17 Aug 2024 02:02:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17604984d3c226f9af9ddc4c76bbdbf6329f20bd317bba55ac221a89f78509de`  
		Last Modified: Sat, 17 Aug 2024 04:07:36 GMT  
		Size: 97.9 MB (97936001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759dfa6c3117134cd7385d39c7a1e2f81ff00d294235ac6a16a31ba6bfbdf602`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 336.4 KB (336415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8369f26ac446b6797caae036f291c10f1a09d6c31c0356bf810a96aa00cb38`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1d9a2fd5a80dade3857fa54fcc8475b78c15a96524cac91006be6a427639f`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.8 MB (22825487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:4388c1bfd0ce8378e22b995628e9203539fc6002a0805384672245af4441b24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22690679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9de804a26bb10457cf42f0ca8313f620f1083621c5bb0d56b102e132ded8b6`

```dockerfile
```

-	Layers:
	-	`sha256:d7143bc60a3c3877400ec04e3efe617b29d6bc5ecb8efcf6cb34b1639c657463`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 22.7 MB (22673557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e274b66c66e82169ce34eb3366fdb49fd1d5f6fdc3c8e8918257376878509d`  
		Last Modified: Sat, 17 Aug 2024 04:07:34 GMT  
		Size: 17.1 KB (17122 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:de0f7970708530dd7e6b15ea99c1277f125a23d6a82343ce2d2672ad1fb6492b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254520837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c724ca630052da62807e05387c435120e456b3b67aeb0b76c1f50264d7c847`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c92e67449590912b6c7755a150613269346b5015b668c99f2db49450f6a8e8`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 1.2 MB (1215007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2693553852f919b16b21546e1d8543a7ad744597e5f6749446017c3790d7277`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 3.6 MB (3595960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9fe7ebd0a06ee011e10d604fd769d9ff4552a42b94b0887d4e53098983bf75`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074b02edbde483a99adecce394a1c8fe6ec4582c39bad3ac5050bd5c6a5466b`  
		Last Modified: Sat, 17 Aug 2024 03:57:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52f3878065eb3ee88c776c4daebe7310fe219adc004d71d843d7ae13921f44b`  
		Last Modified: Sat, 17 Aug 2024 03:57:12 GMT  
		Size: 104.3 MB (104266794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd9444ec78d82b8472db5e98823f37ae6d6f2c2f73640f40d3764e0b2813ae`  
		Last Modified: Sat, 17 Aug 2024 03:57:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400875eb816dd007a1f3a4d1d620c988c9e102b70ccc1e87a56d5f4adac19218`  
		Last Modified: Sat, 17 Aug 2024 08:11:18 GMT  
		Size: 95.5 MB (95496712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dce2bd3adc9c50d20f2fd0ee9f4d1ff3795f663b6f84c5e361effe45601d3e`  
		Last Modified: Sat, 17 Aug 2024 08:11:16 GMT  
		Size: 336.4 KB (336411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ab41a5e698c889953e1b84485d25d10a2b2a7dfbdf8affca8a1bc052e08bf9`  
		Last Modified: Sat, 17 Aug 2024 08:11:16 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad1b2c6149792b532ea62cbce2735ace6578d53fb39f0df47109065457ab68d`  
		Last Modified: Sat, 17 Aug 2024 08:11:17 GMT  
		Size: 22.2 MB (22246361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:655e6ebf42bb300ba105474e52994d88b6afff315c5be1373a562773a31005e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22704077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75aa3c6fcb70b3a19b0d5690582fd8ddf323250e7f5b910587f25bbaa851c79`

```dockerfile
```

-	Layers:
	-	`sha256:bf51138bb3a9e975f0e9b2cbac43943358afe5025819c82b4d7350ff5bd1c680`  
		Last Modified: Sat, 17 Aug 2024 08:11:16 GMT  
		Size: 22.7 MB (22686582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886d6f1e8eb3e66d85ee78ad73c2b389e6b11f499ba2ce170d65eb1ad4a77b98`  
		Last Modified: Sat, 17 Aug 2024 08:11:15 GMT  
		Size: 17.5 KB (17495 bytes)  
		MIME: application/vnd.in-toto+json
