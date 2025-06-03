## `ros:kilted-perception`

```console
$ docker pull ros@sha256:e03b31ffe755dbf3432ddd580a29c6cac8ca3c2a1f79136355a3085933758c88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:cfa513cd5bda79570f98caa5b2be2cf67715702d323a29e728aa27ef83dbf6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1088999001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343fcf51db30970016135d73864802f3cd4e8d0476f94ff695834f94d51151bc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40688eb6ab717091b8ab853e446d63d8b599a40537433633e49421fc01e8ba47`  
		Last Modified: Tue, 03 Jun 2025 13:38:53 GMT  
		Size: 683.8 KB (683829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511cefe64e624a5297e6da7346ff47e3eeb63abae54ce95b69973dfa5472361b`  
		Last Modified: Tue, 03 Jun 2025 13:38:53 GMT  
		Size: 3.6 MB (3563712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaf3966317ae1566784e8b9428d42d9648e8bb216743f683047325d99626124`  
		Last Modified: Tue, 03 Jun 2025 13:38:53 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f48ffbd9bb786430457fa415a40d5ee2774efe6b9ca8071aa074d6dbf3cc277`  
		Last Modified: Tue, 03 Jun 2025 13:38:54 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7767b77e49a35d6dcfa96835cae86b747e3f835e474d864c4c636a0ac0d6b3`  
		Last Modified: Tue, 03 Jun 2025 13:39:09 GMT  
		Size: 135.4 MB (135403352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14018904b0b743f343c924cd937830d4550971e84cabb257732dcf66431c2b47`  
		Last Modified: Tue, 03 Jun 2025 13:38:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f47960427d73f74a7f2115f825f2bc60bac1967482a68a64b81b694b113700`  
		Last Modified: Tue, 03 Jun 2025 13:39:05 GMT  
		Size: 110.2 MB (110181823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeabb39dae26373a956a0d2edd3f461326f490f89d8c8568d2da91adf2e1c85`  
		Last Modified: Tue, 03 Jun 2025 13:38:56 GMT  
		Size: 343.7 KB (343731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cba3aab14cc159b2f31dd309c04c3c462ab7d37a2240db4684db8880580ee8`  
		Last Modified: Tue, 03 Jun 2025 13:38:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb24e494585517847245f7bee3feb2de70d2259ffda504ac3a21109e07b5752f`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 28.0 MB (28034338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e0ac6f682c12a6d58c3417869d5811ff453068d95ed48e199d7a93f3797ffe`  
		Last Modified: Tue, 03 Jun 2025 13:44:17 GMT  
		Size: 781.1 MB (781067400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:b45fe31f6ebc173d9c3f767cbfaf1988aa1d0bfc114c797c54686c2614314e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59961506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5189cc41bb007cfde33a207d0c6bb790ed3bed791f43096177f496a969827904`

```dockerfile
```

-	Layers:
	-	`sha256:2ec92ce9597290f9ec70d89bd70eb58e2780b59d414a9ee9cf24bc45d44deaf3`  
		Last Modified: Tue, 03 Jun 2025 16:17:43 GMT  
		Size: 60.0 MB (59951805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae63a0594bc5ff111b7790a57d64128280605f0dd845adbdf5e796ae48bc92e`  
		Last Modified: Tue, 03 Jun 2025 16:17:45 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a4385f04defed3d0c33a4a762601e6b28bfa5a6c440e9c1cff62c45db68efce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.6 MB (987578518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ed32c3b7a9e04c28eacc711f415f6497b2a6514f0e255212d634a84255f08a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3182864e52220424abbc2ed14f34194efd7a8651cbd58c9013d59badb6ce10bb`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 3.6 MB (3562006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30261ce10ab5a3b7dce5ba78a1a951d5652cbf529e166b904f1bd8067ae7ab`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3ede17908e49502f7fe6ff9399c21b4349b35f3533c331faba1f2970ddeecb`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a602d5eadde99cf0e2a1b5eef954a00e68ffd7b77f3bcf764f02502d2372066`  
		Last Modified: Tue, 03 Jun 2025 15:06:51 GMT  
		Size: 130.1 MB (130123372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f9c9b9568b2d87f3a5ab293e2d4c9fbd71f4dffd99e52cf90997e9ca36cfb9`  
		Last Modified: Tue, 03 Jun 2025 15:06:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38264588243ea616dd51108f28fd01bacfa4f4f8b8d0d9992b894f06c9b8d061`  
		Last Modified: Tue, 03 Jun 2025 15:06:54 GMT  
		Size: 105.6 MB (105596151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a0fbc9639f4dbacf141772ad7cafb19369199dc6d355d3016f948f88930887`  
		Last Modified: Tue, 03 Jun 2025 15:06:39 GMT  
		Size: 343.7 KB (343729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d9a0142be225e7c3542eb77091174803f76691d1a8a374134833906b0e0a8b`  
		Last Modified: Tue, 03 Jun 2025 15:06:38 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b86d5bdb88222257b484aa3a865a7ba6be1a4695a478f248efb25416f8031`  
		Last Modified: Tue, 03 Jun 2025 15:06:44 GMT  
		Size: 27.1 MB (27127919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdd7f0401b5985fe84b8971d36c0f0166bc40a7520999e1732d27a04e8106ae`  
		Last Modified: Tue, 03 Jun 2025 13:44:44 GMT  
		Size: 691.3 MB (691283997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:7b61f738c58f8060037be8fdd0a3004d740ae13ff1dc2d19f8925d583e9bd175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59913251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17a12bbc0c7737b47b1da46b1eb1b0ce323c41df60193e190d73f4c2719fa8c`

```dockerfile
```

-	Layers:
	-	`sha256:322eb5fb763a30ad15c90950cafc79bef7380711f768120979cb2f183fb8fe2b`  
		Last Modified: Tue, 03 Jun 2025 16:19:19 GMT  
		Size: 59.9 MB (59903470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495f31683edae34ea9063b0b0e3108b840379bb28977cd3b06b9169b56a4ab1e`  
		Last Modified: Tue, 03 Jun 2025 16:19:21 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json
