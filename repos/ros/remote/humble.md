## `ros:humble`

```console
$ docker pull ros@sha256:21f9b375b1d4a89a6be7df9f9e16226adb6c22a0b00636c4aaebb0f1d94d447f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:75c0cb090ceb7df06886e441dd4bc631926bbcdd7afc0e0d81a0b602c7b8676d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263536467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bffe566456e658f822a7fe6639d7416c2bcd8d721adcb683ee798e30393dda`
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
# Thu, 02 May 2024 03:53:09 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:54:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 03:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:54:45 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:55:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:55:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:55:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 03:56:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1879d69635a4959bc89d1dde41dcc2301611c85aaa81c97927842f2c91aa21ab`  
		Last Modified: Thu, 02 May 2024 04:23:13 GMT  
		Size: 106.5 MB (106483069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6f24d072dea4bb47d142b42a63cf859b9f4b3465cdc8d7a969a16a0d41ce0`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf28d34f5067790b257e942b80bb9163a6e065cbdd25f31f22ec0b2184d60f`  
		Last Modified: Thu, 02 May 2024 04:23:36 GMT  
		Size: 98.1 MB (98144552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ce4e76da8053503a90eab1800bcc134e4fe971d8ce33cd3b1f49cca69a8e62`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 318.6 KB (318631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504ec22124445470d795d45cf380d7f456cb8ab82eb4331070d9541a058567c`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe5a8233a9ad7f74178a851247c83d9ba97f54c0dbef6d4fcd429b6de002874`  
		Last Modified: Thu, 02 May 2024 04:23:27 GMT  
		Size: 23.1 MB (23101378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c31d82f3ba351376d516d401d19762509aa1d9ccef236b2218bb0a56de160921
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256155507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3835b03b534ad13ede7d3581db60cdee3e5a002fb585c9bb666c093ee785588`
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
# Thu, 02 May 2024 01:50:39 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 01:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 01:51:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:51:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:52:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:52:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:52:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 01:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:509cd74b317af888c828eaa210af614cdc02cf60c703efb6a96fbfefbc117d98`  
		Last Modified: Thu, 02 May 2024 02:28:41 GMT  
		Size: 104.2 MB (104203704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79337a550a6b91ed51d48ae3efe36d87a32a0f53df59b33e1af0a19c4a616ad1`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26db6393e0d50752ece84aa012c083ec2e765fbc6c29d51b7332a383c0edfa11`  
		Last Modified: Thu, 02 May 2024 02:29:00 GMT  
		Size: 95.7 MB (95689496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7673b38fa65d4dd14d96df37491248cf3d2301a7f0fb2ab2a7adee845f4fb1`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 318.6 KB (318615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040d7a25c1861364a9439ae412e6675c329c4870c86961a7190455ebb6e78f99`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d776fd0281a8bf1b7893046cd99c81b1ba582c0b59fc6235cf52e743dbb409`  
		Last Modified: Thu, 02 May 2024 02:28:53 GMT  
		Size: 22.5 MB (22520746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
