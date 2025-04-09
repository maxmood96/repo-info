## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:9749355a0760334fa5ea3c660f2de1ecc5e8a5af8047e4bbaa9afa8a7843da80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:561bc71a341d9fbbd9033130e6169e694b7b65b1421fc275fcd1dbbd2c642e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295272900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1c91a9db1d4fc2a12994eecbd53314dd033c5736121813e86f1fbe63c08e8b`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99045de81e0ba6719056bf2f0ce498cbf21af1b487ae254a8029468870d7c38`  
		Last Modified: Wed, 09 Apr 2025 02:16:15 GMT  
		Size: 110.2 MB (110168410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b46bb8ea31ea3e10dd20185d404b80ee03662025531244d5d3b6d61fced8ce`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 356.2 KB (356177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4841899d1cdb57bc04b3bbf79194535ab00343424557f75d8cccce9707527e0`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95af3af51f9bcc09e226669a67bbb42e8b545ad11919419b32b21fe4800926a9`  
		Last Modified: Wed, 09 Apr 2025 02:16:13 GMT  
		Size: 28.0 MB (27956829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:bbd0c9bb7264a59bef954e2ab06327ddf888c5e16944205d6d37c9b10d02b910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23873558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6d4da1096826cfcdfa4642bb1209351096b952fe72ad6b14bfa910012603a`

```dockerfile
```

-	Layers:
	-	`sha256:d037ff389fdf436000187f50d596eee4e1b48f1831027d14f67349308fe3597a`  
		Last Modified: Wed, 09 Apr 2025 02:16:12 GMT  
		Size: 23.9 MB (23856129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9757a312f6b889d67ccabe5e9cf0a8bb60aeadd421d16cbc25b95a39c233f7db`  
		Last Modified: Wed, 09 Apr 2025 02:16:11 GMT  
		Size: 17.4 KB (17429 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d595b8976f0b5119d374417bc2a702c13ce73bceeb7339b5013ee430e64799e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283730024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d837f6fc140dfe7bff23330f794cc63f7342fd87fcca57c21efd0dcb3d9d12f`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46007cb290c9c61d3be471686a736ee17b9fac514d4a3ee75010c0ff00e86e0a`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 683.7 KB (683730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c743169635f1311f3b83c0db23367bb49da554ccc36aed60f0560db69fb31c`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 3.6 MB (3561575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d49b1f526488311879e130a8efc035c71e0bfc7b62c561004139c1a01340b1`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bdb94284e8bd83926f228dee3a3d21bee9da2bbbed34c32bd397c9fa0b5d90`  
		Last Modified: Wed, 09 Apr 2025 09:15:15 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51db1d103846823a3853812410eb4b9bd8f5b3617f9aecc91125cf41829688c`  
		Last Modified: Wed, 09 Apr 2025 09:15:19 GMT  
		Size: 117.6 MB (117629816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6afbed0c982bda3351b79854d33ca654f92ce16f4a3e1f4a6cccc802ca0c67`  
		Last Modified: Wed, 09 Apr 2025 09:15:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33b60cccfa6e20c4f0cbe401b3aa68469d974314165628c6b0a5c9f657bf8ef`  
		Last Modified: Wed, 09 Apr 2025 15:53:05 GMT  
		Size: 105.6 MB (105592543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2658de70d02b6e6aa725cf85a7fb82de72d74f9db5f084d807c493e28ecf8f12`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 356.2 KB (356171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249d37e4f0bc9edcb6b72103b259bef7281147ee0a52a7b76b3fdf64b789de89`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22198870635e9bffbbdbcb985a3cb5f54ed99b3ba235edadac2e73de50feead`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 27.1 MB (27054339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:66b5ce3015f296a2f74d14dc1c57ed5422ae90b49dd75bac08ffac49eb52e2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23896263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8356baa88c23b40176e255283b4dd73f5cdcbb8e80196749c8ed31f03760dc`

```dockerfile
```

-	Layers:
	-	`sha256:77ec9aa048cc157a919eacbeef9a5d6a025ddcca0afaa16102b6116c7ff4b3f6`  
		Last Modified: Wed, 09 Apr 2025 15:53:03 GMT  
		Size: 23.9 MB (23878685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd8b0a7dfded98791c294b62bfa5c74a8688e976cf84b777cb6d75a9aceafa8`  
		Last Modified: Wed, 09 Apr 2025 15:53:02 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json
