## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:21b7da66ee0d65c550cbed91587c8810d4cb777cb7c7eb92fc0e69cdecc46381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:30cf486cd3f11948045fd18cdb6fa778338c142d5f7abe9ec32e9257530c377a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.5 MB (953543306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63371e14e0d53aff5126aeef880c96dea62a10d32c8a68540d98bd08fbdf55a7`
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
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:db56ea45ed094c2beaf5aba9df68b40e9c61caf09ab723bafcba20d2bdf2d3d1`  
		Last Modified: Sat, 17 Aug 2024 05:03:05 GMT  
		Size: 691.5 MB (691535027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:420afda6ba38bc2046b1e967e849e432ab4a23aeef6d0ca6d0ded3d24c5bcc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57278510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7bf8f012926616bda590036a7f925e0192c6be3c0831b72ad1d187b2f5673f`

```dockerfile
```

-	Layers:
	-	`sha256:8486c26d631dd874974d8d960ac3dc6668cd1538c46813fec23c32cb27ab6b6e`  
		Last Modified: Sat, 17 Aug 2024 05:02:58 GMT  
		Size: 57.3 MB (57268843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fff7b226ef2c58eac33e5e0b1ed793ad19b7bb354be75b0b240c2c3b0a6817`  
		Last Modified: Sat, 17 Aug 2024 05:02:56 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:16bd49838e20662690a1bf11d86036698d945e341bd6df7dd183dc4204a083ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.0 MB (913998378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9f24a4e170c2397fbcf41fd765b8e9af5d3c2432ad7b7221e51268bb4f32c0`
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
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a22138245460f5f446d9b864b2b906cdade1e583b80ddd2bc7ab687d52da5062`  
		Last Modified: Sat, 17 Aug 2024 10:31:54 GMT  
		Size: 659.5 MB (659477541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:05eca2fe374661612f88f2b392f967a462d2f2f762f8a67d8c53480368ab74ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57275083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3d47f68c2f4fb3922934d42c236a11e53189184692b01f5f0d18321a1a378b`

```dockerfile
```

-	Layers:
	-	`sha256:351192ec86f6905ad26dc5d9699b44f2c86cf181999be878bd84bfb8359fe0a8`  
		Last Modified: Sat, 17 Aug 2024 10:31:42 GMT  
		Size: 57.3 MB (57265055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef2fe9d94f883638694c1418316369235d03253ffa5929cb59b80e6119651385`  
		Last Modified: Sat, 17 Aug 2024 10:31:40 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.in-toto+json
