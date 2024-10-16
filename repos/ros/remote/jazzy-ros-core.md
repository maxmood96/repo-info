## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:09ccc592b8102244dcdda135d79715da11fa7b4188631503cb8baa3a62b24028
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1d008c18bdb5bdf1cbdcc688400a70f63420e136aba084a76c6ee2aa278cc49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156661330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c26764c04ca065b71f5f81dc9dff615588739426d1eca946c2fd84a8c30127`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8482975072cd0a0d630920c4c872f2d5e88cc212cff096177260ff1006f883b`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 683.7 KB (683706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c40938900c81ecdae1d6f62b49e2175c396aa4f3255e9c6c32b634364e57cc6`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 3.6 MB (3560128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a37febe7812efd5687665ec7fe420688d4464e02b2f3376e442cc1e50f9014`  
		Last Modified: Sat, 12 Oct 2024 00:01:33 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cf892f7e024165b3c3b94213d3c171e01212fbfb113a13574bf1609dba11b0`  
		Last Modified: Sat, 12 Oct 2024 00:01:33 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d112f720c4670f7c99793a7838a37ee1515ab0394ddf57e49becd1c4204f560`  
		Last Modified: Sat, 12 Oct 2024 00:01:36 GMT  
		Size: 122.7 MB (122664569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b8a934f13c77b28bc4fd03f6150d43bf257620c525384558ccf1ea3b14f08e`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:0b125b3cc94e5c4db987cfac54cc2a989d3d1c938d7ba9a9548292b69779dc91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17809227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f539b8c77835011fd2d260560c3ddcfd4e0905ae6fad601d2f24bca009f71be`

```dockerfile
```

-	Layers:
	-	`sha256:0d64638b00c121df9fe95b4ed16f9b5d549d38ec013e3f0fe189350c05469307`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
		Size: 17.8 MB (17793072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4088e47d2c4a490ed07c1d5463a2325050685f06b01731e3eddb4dcfa5feec27`  
		Last Modified: Sat, 12 Oct 2024 00:01:34 GMT  
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
