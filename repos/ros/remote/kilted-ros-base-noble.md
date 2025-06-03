## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:05fbaa47c2dba428ace8029629d9fe934714d722c2547efdeb3cac20eb240be5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:ee1774383c9cad7a1271137968365a8194e15e1d95c9c8586d1cc0eb48609c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307931601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7165188ee2fef0206f2313918ec7174371eb8b097ef90a391fcda93ca2fd376`
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

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:bdbd3d5946f23c07b9d1829c3c3608a595e5b398ed1114a61c3a49b4b2edd15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24058903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd05059ad2d1e9d1284dd334efdd90fa1837e55781c331d129b62040e25671c`

```dockerfile
```

-	Layers:
	-	`sha256:bb94b1f6b73396b6dd3fb62e27d0a0d45c89eff37848cbdcb598020a2edb111b`  
		Last Modified: Tue, 03 Jun 2025 16:22:03 GMT  
		Size: 24.0 MB (24041748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98f2cde3c8e9c63ab897d391a7e4e5146715104733b096bebc7d8de2a93ab4d`  
		Last Modified: Tue, 03 Jun 2025 16:22:04 GMT  
		Size: 17.2 KB (17155 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9738a3c655b5d2a70740ca44177d898d0903386a7e4e14f0aeeb26f864c2d2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296294521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d56e6bd0867da7572a158a1202a1c8135979fc7ed9490eee83ff8f96631d81`
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

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d58079499e5f2e037d23726fed0c59ccf11dbbc7b18520b98045f9d2e198a789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24081294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572f6fcf89e612b8275436b4dbab71af8ae142db4934c553daf5cf1db4e5e909`

```dockerfile
```

-	Layers:
	-	`sha256:6f958c6fe6a3363c2a910682373793f8992d5ca69601fd01096e7c40829ebc7e`  
		Last Modified: Tue, 03 Jun 2025 12:26:02 GMT  
		Size: 24.1 MB (24064002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5747e3ba8d50f6d49b3aa1589307931755cf73c600486b41f0984e9d0a49c1c`  
		Last Modified: Tue, 03 Jun 2025 12:26:01 GMT  
		Size: 17.3 KB (17292 bytes)  
		MIME: application/vnd.in-toto+json
