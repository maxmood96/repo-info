## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:78f0f141ef2292e6b57762e1a329091ec4332ceaf8b0c99fd0467980e32aa495
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:8360a8a3f35bd59f94e9c4b2068e805f82a58f36864fe359482474eec78c32d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298655989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77856e9bcca7d1c5f764527dcbe88d8a52ae1c0b4559baec8d07d64a7228eaab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce450d3cec92d952ac282860d51dd456a0a7f8291e239c707abe0e1be191ca1`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 683.7 KB (683703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6fda2b3a1f9bc93f10e32c59c206e893f4171f3f780376252b1d015e775e7f`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 3.6 MB (3560091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a811bdfc164a2919f11f77a0d3956e6eaa0616b3872a5281a02f3aa2c2582575`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d525325ea8e09d24717475bc7ebba7d15803e4cbb329b673a6a9305f7d542e`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd192ce0803868a565ccd85257480e827e75a1250defbfed757fb9fa479b2d33`  
		Last Modified: Sat, 12 Oct 2024 00:02:10 GMT  
		Size: 122.7 MB (122667784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ff71b488639f9ffe665466acdbe25b20fb1a21143ebd4c9a99eb42953bbe7b`  
		Last Modified: Sat, 12 Oct 2024 00:02:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0105f2effcfe2e7fb58999ca849b96403c60b0340db438bb40e91166bf5ea502`  
		Last Modified: Sat, 12 Oct 2024 00:57:07 GMT  
		Size: 114.1 MB (114131978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5863e4a247597a9d4c398752759faf63356ab025ac291afe06f464535a0c101`  
		Last Modified: Sat, 12 Oct 2024 00:57:04 GMT  
		Size: 324.0 KB (323959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d0ecfb5a5283ee58e13dbecf4f18f432bbb51c2e6a8202c3fa21e3d3166b3c`  
		Last Modified: Sat, 12 Oct 2024 00:57:04 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6029ca4b9ca247c94112615ff3f887a5ce5625f93981b6d9eeb768f605bee6b`  
		Last Modified: Sat, 12 Oct 2024 00:57:05 GMT  
		Size: 27.5 MB (27533112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:84e86f886a495227560965c5a2330cfae71f1197d57b90415f64d191727237e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23871608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39334566c0724a0b5f6ea1f95ee1364a9d07d2170e934b7b4f6249cc3c9f1a0`

```dockerfile
```

-	Layers:
	-	`sha256:63d3dfda42a8bd322d7120a5be5aae910d423ad8d0328cf47179ace236f9890c`  
		Last Modified: Sat, 12 Oct 2024 00:57:05 GMT  
		Size: 23.9 MB (23854432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8d6f9b6dd301848d6eee90140a5c7bc0dd9fa9a6ac6a5512afeb0de4334bdf`  
		Last Modified: Sat, 12 Oct 2024 00:57:04 GMT  
		Size: 17.2 KB (17176 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:83a6a2c3e16b7f1f316b66765a06ebf5b43962c6e4eeb6c86126a2b80b04dfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288609993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5839b17e880a426f007233d10dbdca8f08fe6e666721a4644dc030a61964f2d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 May 2024 16:49:54 GMT
ARG RELEASE
# Fri, 24 May 2024 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 May 2024 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 24 May 2024 16:49:54 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Fri, 24 May 2024 16:49:54 GMT
CMD ["/bin/bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 16:49:54 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 24 May 2024 16:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 16:49:54 GMT
CMD ["bash"]
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d6764830c4e87fa9dfa3c423571f555682d76d7e9b15dfcb0ee30ee583aac982`  
		Last Modified: Sat, 12 Oct 2024 02:17:56 GMT  
		Size: 117.5 MB (117496665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1427fcb67de7af9a3d735f3478d0c0f7ac0534d7220efae02d58895b648f61bb`  
		Last Modified: Sat, 12 Oct 2024 02:17:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e277af16be8d93d36dfc7bf0ddff0836a7624e21f2556ed87cda388e04d6cd78`  
		Last Modified: Sat, 12 Oct 2024 06:11:00 GMT  
		Size: 111.0 MB (110971172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031fc8712cf0476cbf65618a5970b54c281532a0a26d1f9b8311e9acf21a386b`  
		Last Modified: Sat, 12 Oct 2024 06:10:57 GMT  
		Size: 323.9 KB (323946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ebb6149ee0cc3f7d6301e9816af7f66269409151fca1e7673184e78f004a6f`  
		Last Modified: Sat, 12 Oct 2024 06:10:57 GMT  
		Size: 2.4 KB (2427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031794857cac2e96db8410e040932c595918f3e4e289fe19c76119391142b239`  
		Last Modified: Sat, 12 Oct 2024 06:10:58 GMT  
		Size: 26.7 MB (26684672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5a32c8ca76f39a189f838bfa00bf4f942affcefb453e730d5f2ea5fe1a182e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23894419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1af0e08aa58673af936e7fe5a97f632be92aafb046b4d476edb235dd616c7b`

```dockerfile
```

-	Layers:
	-	`sha256:f26a0966a62276582787e5dd6ce6acef4e1897487a67d2c0804aacfec1f6a060`  
		Last Modified: Sat, 12 Oct 2024 06:10:58 GMT  
		Size: 23.9 MB (23877105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885e13937251799a7a78cc5d5b926e9281dea8e72508df1c5b3fe27b1d68fe42`  
		Last Modified: Sat, 12 Oct 2024 06:10:57 GMT  
		Size: 17.3 KB (17314 bytes)  
		MIME: application/vnd.in-toto+json
