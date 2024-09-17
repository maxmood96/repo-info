## `ros:humble`

```console
$ docker pull ros@sha256:5738897a3ddda0974c460e4426062f668a0598dbea4162c98d20dbd6bc7b3796
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:e2bf5d73089ecafac2f14de05e7cbc1b20ab7568185e2011cec508286dcc6b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262007961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6987833c468f25c50e4802a0a8fe13182025fd5be69f3fc7f4550d5a5afa89b0`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e134650a58527f750ae8240053485a2f137352ecf756235b1e1e6fdb2e58bd5`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 1.2 MB (1214677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1e367d2c4dd5ee27bf7de101f8a5375cd32e0c78aaf62c8575c0e6b6b6d85`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 3.6 MB (3624633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33f588ed24bdf5fad71de96bbb5b7fc275fda37756cef0ed01956e6f35ebb4a`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6852c2b80f647da68213c7078cdb71485445219e260e3465e6f38a0bb1ad627`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d91075c9ed31da02a9b4c33814db9286e4b1b259d48c139ab0c58bb41ea233`  
		Last Modified: Tue, 17 Sep 2024 01:01:11 GMT  
		Size: 106.5 MB (106531769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6410a8272a83deb81f823b1cb3bf041f95c7d711601610c50de02837a1fab738`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a0131e0c73a7071017bbc743e74591d78261e5fb886e39f5f89da54721d7a`  
		Last Modified: Tue, 17 Sep 2024 01:58:30 GMT  
		Size: 97.9 MB (97933888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319799ae1afd30876970d7bb2b3200269a4a1d49c448e6183e6ad42d0439b017`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92d07b72e749b4d1f35a36946f6470904304c610e8208688ab5bd132580e74e`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82b3fc9b8259a2df8418e0bd1c22651c30c4d5d33aefdb144429af07a39515`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.8 MB (22824416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:10163c349a13ba6ae506742ac20d9c43d56817b576158f89a814bb63fadaa8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22690706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c55608b8e01eddea7d327e54582b480f389f8fe8d0b0af572aa4c2ee5d1635`

```dockerfile
```

-	Layers:
	-	`sha256:d587c79cc328a77c3ac363aebc882987b88d872d5daeb13bc9b430dfa5416131`  
		Last Modified: Tue, 17 Sep 2024 01:58:29 GMT  
		Size: 22.7 MB (22673585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6fc7ed6f0445f1c7823fa43bc6979f8f17efd432b5c51f659d218c913a4ead`  
		Last Modified: Tue, 17 Sep 2024 01:58:28 GMT  
		Size: 17.1 KB (17121 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

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

### `ros:humble` - unknown; unknown

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
