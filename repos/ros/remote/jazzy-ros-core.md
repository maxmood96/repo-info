## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:4105a494b85f18158af57db415bb7c16d56c20d5c4876839f685622e66236ce6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:0b689a7bda0cbe6f36d277c2ef98a5ffdb2ec19e08b66e37a237495cb35ebb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156859115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5ef3f679bb70c0cdc2fb54a107d72d78bc2218abe0efed505e094eb927ce3a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=jazzy
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db6612a791b94a9bf8fabae0aa79d724aeeb933eee71621a8b97650e5c989b7`  
		Last Modified: Thu, 08 May 2025 17:06:19 GMT  
		Size: 683.7 KB (683654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3983963a90e8fa68690e05966e629ff5a9883d85bcc023046d90d9f68d636`  
		Last Modified: Thu, 08 May 2025 17:06:20 GMT  
		Size: 3.6 MB (3563319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5443d20d5093c36fbdb72dc61460392cbdb629c68c4519b2075ff007364a8d3a`  
		Last Modified: Thu, 08 May 2025 17:06:18 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c5e46a5a33f034e5d6b276d25aad71c24e71feea8742bb4a9fb4c07acd7c22`  
		Last Modified: Thu, 08 May 2025 17:06:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247a03c6dd3d195fd6087d50e6c4e22e336d3a02b38275631e3743c39976ec5e`  
		Last Modified: Thu, 08 May 2025 17:06:26 GMT  
		Size: 122.9 MB (122892142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941b252d0546e6b8fee519dd212cd7c65b9527f946aaa1d8fc88ee0a12559edf`  
		Last Modified: Thu, 08 May 2025 17:06:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f5a7cb47f32cab80f00827639c57d7f32c68b625b6d9419b091d6d11da48a125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17847213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75a327705f72ccd18b82db7abd9c87d306ce286cb90a3c6da718debddc100b6`

```dockerfile
```

-	Layers:
	-	`sha256:356e2d2db18daa4b7277699e68d69e03099d40dc056b2ca108afa27b68ae6c06`  
		Last Modified: Mon, 05 May 2025 16:37:15 GMT  
		Size: 17.8 MB (17830841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a2a9e2ef2575f60bbcd3d5f413d18530c1b389520da80b7cca16c39a1cf766`  
		Last Modified: Mon, 05 May 2025 16:37:14 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a4a670b83aaa2b52f77f0c90ccfcf950975792ffb8dc80bb993b6edd56ed015a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150777058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468c8b2c609f48c10ea5e5a83ab245911d97d22da9faeebd99627e00cbb3696`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=jazzy
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2e6d631663d69d931328844662622971edf603268f55d74da74b2f1832435b`  
		Last Modified: Thu, 08 May 2025 17:05:37 GMT  
		Size: 683.7 KB (683725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ec84cbb756b62af9e3d14e9f2de6ea3bab2ef3004d88f35527f5b06731e5de`  
		Last Modified: Thu, 08 May 2025 17:05:38 GMT  
		Size: 3.6 MB (3561582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3c6650198856d89ceb2205e3faf841383f08c4f761180ffb26aff4c61888cb`  
		Last Modified: Thu, 08 May 2025 17:05:39 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4f33a49a4d32aa02eb8d0ed177d6f1618ea6ed82efb0abb3c82978bf9b2487`  
		Last Modified: Thu, 08 May 2025 17:05:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617abecb85c9162d81ea2cbe7eaa782a047b0551dac5a24381cb2e1912668b3f`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 117.7 MB (117682404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ea95c5199fdd922b6236aaecfa05b1338a5a59763fa9e9010a537880b343fa`  
		Last Modified: Thu, 08 May 2025 17:05:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:b24a190b5f02b44122109faacc799239f59a86d09dd26aef4aed794f97f6156d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17821359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefee86c5eb3bc93767aa1dde202dc072c8e216122cc12ccbee55ae35d243dc5`

```dockerfile
```

-	Layers:
	-	`sha256:e20bdd000bdc8219194f287460b36068b32a3f0a740ab58681cf33fd379ca8c3`  
		Last Modified: Mon, 05 May 2025 18:20:50 GMT  
		Size: 17.8 MB (17804847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ef0fd124bb035b76a3e9cd7a7d59338d1837a68f7ac2b722370cd6b20ea874`  
		Last Modified: Mon, 05 May 2025 18:20:49 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json
