## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:71d48128e6191b3bf3cd4675f8c67de744bde2172a861458d02b8e0db86002ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f6b84216b442ce5da9685254c057957bf3886eaa9d499335f649b934818db1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157770288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781050140efd09eeef164262d9bf94f51792e014e7eef28c2c9f2b45831cb903`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052dda1b260e91b11278fbdffdb9ce31c81162ae198c613d45527a4a1e6d050e`  
		Last Modified: Wed, 16 Oct 2024 16:18:22 GMT  
		Size: 683.7 KB (683727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aebb502a2b85527c69a23080629eb47bf5ca908fd2b52d014fa3038b7dea40`  
		Last Modified: Wed, 16 Oct 2024 16:18:22 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4794221ebf57646ab7b66a7f81267c8314c7d946035bf247805572c4e98e54d2`  
		Last Modified: Wed, 16 Oct 2024 16:18:22 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f56724ac000a260b5f46d9fe7ffe8a1b864e09654bc69a7027ad597d4f359f`  
		Last Modified: Wed, 16 Oct 2024 16:18:22 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aeb3b85ac38b3ac061e1863e2d67cfb04de602269aa5bff3edce9bb0020a30`  
		Last Modified: Wed, 16 Oct 2024 16:18:25 GMT  
		Size: 123.8 MB (123773725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee69c15418411e4c34b8f580c1bede85fe7e648507450ffce1e7a82ebe1c3017`  
		Last Modified: Wed, 16 Oct 2024 16:18:23 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fc6dceb2ac33ee906fe6d9d462ace1b078489b298677f9d0eb1f3502e81fefcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17809239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8309bbae8a5a29ef85f1e686350e3795c5c1481b2bc3504c5d9df66ab003662a`

```dockerfile
```

-	Layers:
	-	`sha256:1025e05ae4255eecf5b38833adb848219165f6683e9b05305877a06edf666d2f`  
		Last Modified: Wed, 16 Oct 2024 16:18:23 GMT  
		Size: 17.8 MB (17793084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f4060aea0bff38f34f924719b417c506b049d406e910f36614f5283e1a00852`  
		Last Modified: Wed, 16 Oct 2024 16:18:22 GMT  
		Size: 16.2 KB (16155 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6141fed47c2de8c3879c374fbbda7f2c267000c511d528a2bd1a7cfb43a7b9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151695117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10ab1dca4f5a017554cb01e7523b5933d77286073e38c55e1db31f7e13e111c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75906b0dbbabb024c7f890638530898ee5c0c44e20c5f9b2843574dc92ee4e4e`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 683.8 KB (683843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f509c8e504eee35bdf2f7a4cbcc4941d472d9a497b7f511c549dc7c5b8a4e`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 3.6 MB (3559114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed51f7b48cfd97dfccaca6e9172453c23a61383c3cbd8b7db4643cef6c1bc5b`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969caf6e5719f51692ea48756b21810e0471a7e3f778cd747e55d3becbd5e265`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a470154f77a7c7c7a8a312b42be914cf7ecbb022df4d1a56f2a705c6f7c296`  
		Last Modified: Wed, 16 Oct 2024 04:15:42 GMT  
		Size: 118.6 MB (118563844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f32c28d2bd76edb76a580f3c3a6b856a2458d58b0121e6f53d0fd9ae25ed7a`  
		Last Modified: Wed, 16 Oct 2024 04:15:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:21df5a8da107631cf61a9ec1865ca43ec6dd8e12931de311fc00dfe0f2f36981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373e48a77e2dc7fbd05ac00f149963ee9981c5a02bd26df7e1d1ccb8df9b3ae4`

```dockerfile
```

-	Layers:
	-	`sha256:6b140ad49582a6eebc387af6676b0587f469959a30650a7efd671f3be791a7a4`  
		Last Modified: Wed, 16 Oct 2024 04:15:39 GMT  
		Size: 17.8 MB (17767055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795b97ce3ec48f23fc37cc56e08722bb43d558608028b5fe1ef5fbee2aa2ffd7`  
		Last Modified: Wed, 16 Oct 2024 04:15:38 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
