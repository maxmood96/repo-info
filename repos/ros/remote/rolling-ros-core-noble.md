## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:15927484889e80c215ae54d91da7f31ae52afa16a6c4e7cf70222a2db767e8da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:bfba0cea4bc7c89f1f42b5c52e736339b18344027f7c03d48766a6d3663b3f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156664504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1e210c06f575ced6f2c13d268808da1598f468302a3c3cec5bef36391d0b35`
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

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f9882052c5b61893d86a1d70aae7ef1f2399e17c6d9f220f60ac01c22e661445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17830370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fc978779c1722516aeb24ada7ca0e4f59851cda9549a27490a844e07ae7f8a`

```dockerfile
```

-	Layers:
	-	`sha256:e39a1996b00db0a32943df662607a467565e2c82763b12fb4ec68f3c58f56e24`  
		Last Modified: Sat, 12 Oct 2024 00:02:06 GMT  
		Size: 17.8 MB (17814192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f0bcb22324f2dc8d9ba99f493d8bda0f75a79c0d32ce4ec1e29626f6a72d5f`  
		Last Modified: Sat, 12 Oct 2024 00:02:05 GMT  
		Size: 16.2 KB (16178 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5abc755515e55a5fda6fd076b52b102c62d9cbe3888e279f08afaf9f73916c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150627776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2110fe9e053d6a329ae0041a32243f3b5d48abe897a4a79cd383c9a4d2ed5f8d`
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

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a74fdfd366357ac4770d319206b8f6b2267dac8ec3b7df0e44a9bdd1c8d387d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17804474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b161fd9286406870c4ece3c27aab5188ee7a12711de47d51ae0b93b586ccde`

```dockerfile
```

-	Layers:
	-	`sha256:54b4aca4d1aeb6e16563f5aaa8cec43ef57dda505218cde823b6b6649145b98e`  
		Last Modified: Sat, 12 Oct 2024 02:17:53 GMT  
		Size: 17.8 MB (17788163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e94a94361c62e89d29eeb332e45090f8b11ac320d4fb00812e4e7cefaa504086`  
		Last Modified: Sat, 12 Oct 2024 02:17:53 GMT  
		Size: 16.3 KB (16311 bytes)  
		MIME: application/vnd.in-toto+json
