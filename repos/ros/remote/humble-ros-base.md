## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:846db6e1cee81e5cb54a23dc5d5f80e55a0d475d55429e04fa37915f35a96456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

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

### `ros:humble-ros-base` - unknown; unknown

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

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f54ebef77411238c363ffa41c70aea5a5b82a9252eb603dc9fe254e8dfcdafd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254487091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7def2430910b25be630d50ae54e362972f05e3303a481678618afa4ef9999f3`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642777190e2c5930ac7f878fcb35527c46d6b7806e34faa9ae2a2f0f2bfc13c3`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 1.2 MB (1215039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cca9e422648b2272f0a008c1788be89473c191a0280907424111492c6f717b`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 3.6 MB (3595841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a2a40ed4df2c9327fdd1b01955d91f677beb62aad8cc8200659c5c961c0cb`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3100c5fcabc07ac370c534681779696f958519d1d69bdbc1be2daeb4d4dea9`  
		Last Modified: Fri, 05 Jul 2024 20:42:07 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5a80cf954f3da0bbead621f6f187a31b68fa9fe9b3f2347e28dbc3ff02bd9b`  
		Last Modified: Fri, 05 Jul 2024 20:42:11 GMT  
		Size: 104.3 MB (104254849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75bcda3628cc9b6c17574b9aa6fe792c98769b671e75adcf704f65de24caec`  
		Last Modified: Fri, 05 Jul 2024 20:42:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4439a92ef939d81c051b27134091b79a13540430388ff45e86d5325966519d3`  
		Last Modified: Fri, 05 Jul 2024 21:13:31 GMT  
		Size: 95.5 MB (95495749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529ccd4c7e7ac9c164f4a51eb05822f9c9a40454975e7bb68807b5dca18a1878`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 329.6 KB (329602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f45e43b591bf8f05661f79aed916d88281ff16bbe1683306bb95ee26cff09e0`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a6c377510a80093944d7501857f77200004ec3481e20b26d7f1e3b8d2be95`  
		Last Modified: Fri, 05 Jul 2024 21:13:30 GMT  
		Size: 22.2 MB (22231077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:401301555f37d6f4b9919d331dbb2b4960db5a9cc5e6e522613a3e5d3b74ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22577041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badfde6436cd6a8bf70d6704bc12e7c369eb9c94463e1be4f552ae66f76dcda5`

```dockerfile
```

-	Layers:
	-	`sha256:d73cc2e273d6f9b5e8669998741db2fbbfe0a5255b1ec1316712b8cc6831ae0c`  
		Last Modified: Fri, 05 Jul 2024 21:13:29 GMT  
		Size: 22.6 MB (22559546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a06c7da23d98936ba075ebee1b2af25a8df694c5917dff8d1239a1eec87bbd2`  
		Last Modified: Fri, 05 Jul 2024 21:13:28 GMT  
		Size: 17.5 KB (17495 bytes)  
		MIME: application/vnd.in-toto+json
