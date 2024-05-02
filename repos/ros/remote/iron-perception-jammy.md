## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:b4aa7d47c5efb8c4e8ffdcd6020b45211dec6381a0bd13ffc3bbdc4a6378296d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:7f6dfc11086c40bebfabe083bd773cf272d6fe6f0f5f25947fb88c6cec2b5ae2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961130287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f36a9892612a1dcee82a9459d97660383eb1d7fd8a1213e0bd79b7e2991a01c`
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
# Thu, 02 May 2024 04:06:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:06:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 04:06:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 04:06:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:422fedfa5dfaebcc566c7e92541fc27655abe22d8a1f0169b92ff8f1e26027db`  
		Last Modified: Thu, 02 May 2024 04:26:06 GMT  
		Size: 85.2 MB (85172267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253d6e13893607b9fd2bb089d76803f28222334db07a7e6c039347d211e28e75`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 304.2 KB (304160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341714e0e3da5410ec70095a96eeb8251f8070cf3591b0862e78b4fd412f594`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dae7fb87701eea4937f651281711cb460971549f82ead0db6ae4e1e9f3d9b3`  
		Last Modified: Thu, 02 May 2024 04:26:00 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb85359bb36b142d7f4bd7d8edd9d15e7b05c147f516fa87054fefd9ea0f5798`  
		Last Modified: Thu, 02 May 2024 04:27:46 GMT  
		Size: 692.2 MB (692199894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4afb846ea1d60da761e40c312388f609133bbdee6c5b3b5988744649e9329ccd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921508016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc015eebaf2949da9137113386c2c7922a66a5bb30b9cd2760d113372b57896`
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
# Thu, 02 May 2024 02:08:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:08:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:09:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:10:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e141b1e1a2efbe10e3f3075a2d730ebe345b8504c8f84c2ffdfaebc832d186d5`  
		Last Modified: Thu, 02 May 2024 02:31:26 GMT  
		Size: 82.8 MB (82848104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d081fe18a08dd428be0bea55cb3f204c354537ddf7f84b6ba9b308188be65a5`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 304.2 KB (304158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ce52124298db734bb8b0baef727eb109dbb79d7d7201081235658d7da6d8c`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 2.5 KB (2525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f5e0de463364cf7347335adf553225674b10caba09d044b782b6383a48194a`  
		Last Modified: Thu, 02 May 2024 02:31:21 GMT  
		Size: 23.1 MB (23120959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce8148c703f48a18bb69e9fae192639680768cf3617ad602db9c21d28ede665`  
		Last Modified: Thu, 02 May 2024 02:32:59 GMT  
		Size: 660.1 MB (660090039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
