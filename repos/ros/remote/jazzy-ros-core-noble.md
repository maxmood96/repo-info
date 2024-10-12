## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:6c1056a6d7feb3f1a733e4b81d1c50feccb93b51559f8b2eeab867f4d6d919c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

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

### `ros:jazzy-ros-core-noble` - unknown; unknown

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

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8e0f5328c09bc2c42ee0b147ca930fcb7bc5b816c3fc74958eaf68389d46386b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150622668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c83de0f2f980c9bc904e6b1d0a20b9a8b0952c5cfd72a362c80c2cb34e66d7`
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
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
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
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e7dee55f25f747749a46fd55e54a8cb4575144df51bb029fb21b3a4a4e14e`  
		Last Modified: Sat, 12 Oct 2024 02:16:32 GMT  
		Size: 683.9 KB (683858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6578e5ff6225e473b6819100fb20754b86075e46504a3fdd52847af426039530`  
		Last Modified: Sat, 12 Oct 2024 02:16:32 GMT  
		Size: 3.6 MB (3559169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb830bd64f150721a51d3ef313053d010dc4176007495390ee8bb4a99bf2b7`  
		Last Modified: Sat, 12 Oct 2024 02:16:31 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fef8abeebd41e59ca1b4346deb0dd8a15be59760d7e7cc57f5a8d0f02dd2676`  
		Last Modified: Sat, 12 Oct 2024 02:16:32 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7eea82ef13fbaae324650f812f81552fea8bd5c92a9e675737fa3d37bcdd7f`  
		Last Modified: Sat, 12 Oct 2024 02:16:35 GMT  
		Size: 117.5 MB (117491556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a27135fc0af12655b9ce75dba531061a6e38a0939c0d6faf6dfaf1f605836c7`  
		Last Modified: Sat, 12 Oct 2024 02:16:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:97b0504950b92d7ff98e81d9acaa22a18a475cfe2f8808624ce963c7dc58b68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc13b14dcb047cac02c91c24522337a85db91c0c80b5b46f37560299b37d8d35`

```dockerfile
```

-	Layers:
	-	`sha256:be13fd3a51812e21915c5c35c8249e5644acc937b2e931a6cf1f7770349975fd`  
		Last Modified: Sat, 12 Oct 2024 02:16:32 GMT  
		Size: 17.8 MB (17767043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90577713b1836853319469acbaf17c03d4c2beba983e3d13d991b879a460957d`  
		Last Modified: Sat, 12 Oct 2024 02:16:31 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
