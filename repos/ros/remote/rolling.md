## `ros:rolling`

```console
$ docker pull ros@sha256:935a36ae357cc6cebffa2d001f177c51e288238491413692b7945809107567f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

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

### `ros:rolling` - unknown; unknown

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

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c1729587f830060d464b407290da7ea361d19bcc413161b8bf69fd58878d2edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289719929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7557b45ba545ca264375afc7126fc65a7bd80040a2bd71db044022d09e3c56d2`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
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
	-	`sha256:49ebdd9e47436c4391ff4f96f57db9ce3f74dadcba2a10820af55318e09901a5`  
		Last Modified: Wed, 16 Oct 2024 04:17:15 GMT  
		Size: 118.6 MB (118568656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6cc5189b8f5cfc989c33a8d416b71f388bda6054059e70948ed2ee8f2d8eab`  
		Last Modified: Wed, 16 Oct 2024 04:17:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c8f574aa06a037708ba67d3b5f9f6b218b47bad90f05e0e4c156e1d487fcc6`  
		Last Modified: Wed, 16 Oct 2024 06:08:59 GMT  
		Size: 111.0 MB (111008282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449d9067c3fad38e318f960312845df4672da2f2a6eca44113f104cc8f3a6efa`  
		Last Modified: Wed, 16 Oct 2024 06:08:56 GMT  
		Size: 324.2 KB (324199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e46397b7857aefb2727930b24e9a4af2da410d2aab6a4803ad3384ba69f8be`  
		Last Modified: Wed, 16 Oct 2024 06:08:56 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc10351ba64d3e3d15709e92ec43f1007366a864bd3630b21bc9f1416c9932`  
		Last Modified: Wed, 16 Oct 2024 06:08:58 GMT  
		Size: 26.7 MB (26685087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:865e0d5a80806a8d6bf9c9cbc631cb44615316b24ef16b574a7942f7d7bc0e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23894478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39aa2c53c6f424c68f1cd75a502a94f66ed035849e3e6d68c45f3ed96cdb95b`

```dockerfile
```

-	Layers:
	-	`sha256:539af978e800fa823d6ffb03f5fae18d7484f2c7feafb443d8649ea71656030d`  
		Last Modified: Wed, 16 Oct 2024 06:08:57 GMT  
		Size: 23.9 MB (23877165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530e83c6b807741d6b4455342a5031e283e4eef3e023b9388b682cd2260ab09e`  
		Last Modified: Wed, 16 Oct 2024 06:08:56 GMT  
		Size: 17.3 KB (17313 bytes)  
		MIME: application/vnd.in-toto+json
