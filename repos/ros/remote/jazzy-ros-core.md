## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:b51ed536b813977e896125e9ac2e745a74aca3b10847aff5c45093d7f7d80e45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c3a9ceff3edfec9fc63459ea92ef5e473510aad5aea29ade4101ab9c839de792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156459027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f9c9d1f4f96f564799ca35fddfbcbe3a650c406c5d27d232736185e4c8f9ec`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b756ced399254e747c9c6ac1e76375fe9f65dbe1502fb738c36183836ba5832`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 681.8 KB (681791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea19ff7adf3c4016c0a20705cc19d24c1b1466712489d86bc2e1c7b135a2b2`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc9e4928305147e4caacb53dedefb534025bf9acc46d7df929c53d4b5dd2a9e`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65a720349f2400c5cc114d51cc7bd8f26e2add810dcaeac1ae2cf405296a29d`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1863956d9c40d901be9b293083945e3cb1a74a8aa4d851eb0277dded81a8c`  
		Last Modified: Sat, 17 Aug 2024 02:06:24 GMT  
		Size: 122.5 MB (122510397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f5e1f9ba0240968079682dcd7a70f5fe4c0644774c7234d6a207b23e43c7e`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ac901699e0aaf04540d695e22d515b703afdeffb7185199f693ca4034507f87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17797751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bc8dcff98f5eda95a4d3e0e3b7865615c87b41426f13ddd65fa44b197343a0`

```dockerfile
```

-	Layers:
	-	`sha256:f70d61afa5d73ea7219344ff9211919e97e842df31c7eb23972807c6554f035b`  
		Last Modified: Sat, 17 Aug 2024 02:06:21 GMT  
		Size: 17.8 MB (17781633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4116a48d0697b3b27bd73b6b1d84237eb64296c95b252b6c972becaeb3ac96b1`  
		Last Modified: Sat, 17 Aug 2024 02:06:20 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0735fa978d810ce18436f4a2a878b85cde76abe4a25c133f1cdc67e3e8f392c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150426224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce3767c071631aca39aa64a13f562d9d09e697506e77acd8acd49f5ae576fd2`
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
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
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
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a631a99905201093a192b96d6b9344a759bab04da8001fa7f2bd7df0eb20f436`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 682.9 KB (682877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2beccfb7f73210b53f07f3b786019cbd7b54faebe00e559e8511b67575df29`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 3.6 MB (3557897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fdcea445bfe641533a4e4eb218d30dd044e1fb979c59c9ffb8d6d41c654c4`  
		Last Modified: Sat, 17 Aug 2024 04:01:16 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740a42c4dd663c96d6c786e46499dedfb50ea24fb2702a2108d9a94cb3aa990a`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dc6c6c7dbc5ee2a9530e7f4b5388510310ae9b6d6fe273f77997dfbdcfc0ba`  
		Last Modified: Sat, 17 Aug 2024 04:01:21 GMT  
		Size: 117.3 MB (117339297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d6f7979d4b52bb159a593e4dbf4ac389e95d564ab873898d95f3809725b7f9`  
		Last Modified: Sat, 17 Aug 2024 04:01:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fe7c3c0fde4bf693112adb1a1f59d7ff0a5fa412e3ad2a465b7ba5eecea4ce5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17771999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85deaf0e71663b95f37b8243dc4908a2ac1ddecd101b4b96aff4bf1fb7bd11bc`

```dockerfile
```

-	Layers:
	-	`sha256:0789beb0fa5f919d5afc90970cae2304758384dddf29a35472eca1287fe91625`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 17.8 MB (17755604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4f87bbde0cb962454bf36059d1cc000ce210c20d307d631020c81626cd706b`  
		Last Modified: Sat, 17 Aug 2024 04:01:17 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json
