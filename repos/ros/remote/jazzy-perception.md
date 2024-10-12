## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:ab5c5845a01db039316929aad136520a7a036636969ab74b4211d26e93333066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:f4345909853d5ee92b9885ee3785ae3f79f451acb11f8fb6e1af3099aea47493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.6 MB (622553753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57faa2a134be7f82ab1b1bf8ec11e70eb0f1804de730a53bd534ba2194a50d3`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:7cea74593c90939ba3b8c0a137933189d8684ceb415da4003de0dff394cf310a`  
		Last Modified: Sat, 12 Oct 2024 00:57:11 GMT  
		Size: 114.1 MB (114131892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e41d6636b6aef9f25d96f0c090992a11bbe05acde5a71259f58da412deda7f`  
		Last Modified: Sat, 12 Oct 2024 00:57:09 GMT  
		Size: 335.4 KB (335382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2133898faf909aa255ccc404d9ec95e8697f9d5d5b86f9b5812c62e6b5e9e36`  
		Last Modified: Sat, 12 Oct 2024 00:57:09 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a0f69de29ef4eb4db6bc4ecd98e621b3b4c24120a6137747651d2dabb7146b`  
		Last Modified: Sat, 12 Oct 2024 00:57:10 GMT  
		Size: 27.5 MB (27530386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ecc83c8d616e37933dd6692418e2a59d71814b64223b43c5fa953c6cb22272`  
		Last Modified: Sat, 12 Oct 2024 01:57:22 GMT  
		Size: 323.9 MB (323892328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:451ba7eb92f7702b802b68f5158eaea193a71218230ea5c7ab57885e9e0915d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42100563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b4ad18a2460c1b2ecc1053d8d454ab07fdfc5c50cf7289787fcb28c8082da0`

```dockerfile
```

-	Layers:
	-	`sha256:ab187003d42812c20cca1d7044b7aaa610d39bcaa983d37ac6230e4e59c9ea08`  
		Last Modified: Sat, 12 Oct 2024 01:57:16 GMT  
		Size: 42.1 MB (42090871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3253fab938194db90261b311aa9ca75152407048d762839f0b44c99cd3b414`  
		Last Modified: Sat, 12 Oct 2024 01:57:14 GMT  
		Size: 9.7 KB (9692 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6a9edfae931826c8f4358a297a59a584f1056183c41fdac458dad6031a3dc74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.6 MB (565628129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52c5d63f5600fa678bc77278bb076b8d8b2773dc05d7ac7223c0209ef537071`
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
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
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
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:aa632790f7aa9921e06459b6b5062bb3737b68b411d367e142f37fe01bdbd937`  
		Last Modified: Sat, 12 Oct 2024 06:09:16 GMT  
		Size: 111.0 MB (110971374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25e540ab0c88b94ac25e8227c14d667907cb2a6e350d399560ec533e8dd3c4`  
		Last Modified: Sat, 12 Oct 2024 06:09:13 GMT  
		Size: 335.4 KB (335384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bde22961187449f51af543a2254ad6ff670a5214eadefde398c4fa2d81e0a5b`  
		Last Modified: Sat, 12 Oct 2024 06:09:13 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dad41f1900848ee66cfb6f7c445d6199c04e7e3d85578276d0c129e8577d4d`  
		Last Modified: Sat, 12 Oct 2024 06:09:14 GMT  
		Size: 26.7 MB (26681416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c780ad7efc1c78ecd4af08e2472087942a5e3a652d88c9ae7d7503565a12332`  
		Last Modified: Sat, 12 Oct 2024 06:55:49 GMT  
		Size: 277.0 MB (277014847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:735666e6f9f424810285cb4a4e143435a6d442f6b1f2f4329cf0b3fa0eb8f25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42098736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a120a5caed3fe63d667dee79af4583d9bd99ad43182b83872f7f93d34456a2`

```dockerfile
```

-	Layers:
	-	`sha256:ff3b02be8f6b0de0daec35748cac8713a18ec82890469d89bbd93da8780a8360`  
		Last Modified: Sat, 12 Oct 2024 06:55:45 GMT  
		Size: 42.1 MB (42088964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41cbf992ea91dfebf048db707cb81128ef2a190750dfeac08a9d350c33976b1b`  
		Last Modified: Sat, 12 Oct 2024 06:55:43 GMT  
		Size: 9.8 KB (9772 bytes)  
		MIME: application/vnd.in-toto+json
