## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:46f4f84935e605fd771196decb9dfe1e2657ddcfee6799ed8130ea587bec175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:09cfd88a39f947bdd8748daa71cabf9350280f68118a62617e6651a5a637246f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159717420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53c5a1919b2412065f601e22bfef6b4a2e972de5e03257e7ac9bc09c7296349`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:04:48 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 04:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:05:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:05:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:05:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d91e0671b73494532cc2f2cb058e2ed66c603366141af0db09b78520be2657`  
		Last Modified: Thu, 02 May 2024 04:25:47 GMT  
		Size: 124.2 MB (124231063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa36c1c6f86bfca1f25e223d165bfc1e4c9f85816464694f59e1a52c3918db`  
		Last Modified: Thu, 02 May 2024 04:25:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ebedf8eb9e357afecda1950f766cbf2a8154f189fa44a9db2a32df3a8f3757da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155142231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9c55419e1a1830f07e05de1ec6330fbcb959692e4c52042a1d91bd56ecd453`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:07:37 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 02:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:08:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:08:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a674d9efb72e31cf3dadb7136dc3ff9bd2661e49d9aebc1766fda9652435fa`  
		Last Modified: Thu, 02 May 2024 02:31:09 GMT  
		Size: 121.7 MB (121721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f0ee788352297555d68b026eac715cd3ed64835dbac315ed8cbe05a0f20c2e`  
		Last Modified: Thu, 02 May 2024 02:30:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
