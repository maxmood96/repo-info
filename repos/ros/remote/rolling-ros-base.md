## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:ad848c081f616b70f3916cbe5164bfd2e4e466a4e265ff405a3642ef5b652cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1569a90380536a8a55416203fc87501a40cc5686123ae1be1c7b9f66791d5983
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299750562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc58e01c5bb3f94e5a3c6565881b0e2f7d83691e89defb0484cfd8afd346a68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:59:04 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 22:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:59:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:59:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:59:49 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:00:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:00:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:00:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:00:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bf4a81719799814110e9f58b3944ea90c1033a2274eab4e6624992c9f09a`  
		Last Modified: Mon, 17 Jun 2024 23:04:52 GMT  
		Size: 122.4 MB (122447596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cc489dc7cb1f7d20b13283e4b7586c6fe6955dcd75de71f41fb9d4e839d2ef`  
		Last Modified: Mon, 17 Jun 2024 23:04:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126a1d525e956c943a665be6a1bdf2bd1c748cb8a6959056e416b5b858b4f2dc`  
		Last Modified: Mon, 17 Jun 2024 23:05:16 GMT  
		Size: 114.3 MB (114314070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dae707d6964653e32e5684b13a14702cfd58eb44815e4409bee401b4e94f77`  
		Last Modified: Mon, 17 Jun 2024 23:05:01 GMT  
		Size: 313.8 KB (313847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b5327b73417c56e1fd5f8a00a275431abffe89465447f184ec4399a924c693`  
		Last Modified: Mon, 17 Jun 2024 23:05:00 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe718ce59110b6c800a1a2ca943b53eaf075e1e58706b121dff1445fd9d00ef`  
		Last Modified: Mon, 17 Jun 2024 23:05:04 GMT  
		Size: 27.7 MB (27666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b7890dc1eb4f340307aad568e0223085ed2369d7b19b345575f24a192105a16c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289899219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e375df26376d28b4c17bc3c2dbcaf0d36a1b3f6b48c8244d0e1f3089c125dff`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:43:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:44:04 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 23:44:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 23:44:05 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 23:53:20 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 23:54:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:06 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 23:54:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 23:54:06 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:54:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:54:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:54:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:54:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5a7fbe25e3d36bbc3e23956d157e2640f493a3614c18ddf32011d52a3d12c`  
		Last Modified: Mon, 17 Jun 2024 23:56:26 GMT  
		Size: 683.0 KB (682994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed347a619d23bde76d0ac11bb05ee46622970a7b382f4ce0a9ef66cbf9b7298`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 3.8 MB (3754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d5e5704da6f311317b0920e81a37bdbaf3a74659475e878a35f3715f1cdf46`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61cda40c8dae222df86051cac89d4dfd52350839b6ab740cb2571c49d908ecc6`  
		Last Modified: Mon, 17 Jun 2024 23:56:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a2283aa8cd9a67e68a92a1c6ef2ba08fa913e8a9ecd115b9624f2c79b2baf8`  
		Last Modified: Mon, 17 Jun 2024 23:58:10 GMT  
		Size: 117.3 MB (117264050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa7a3a2659c109b159fdd90652b146d33ec87f5c8499db391ee301917cff9fd`  
		Last Modified: Mon, 17 Jun 2024 23:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522c26a1107802862fb3c5b0c7868208a077488d3d0977dfb803db3d598e1142`  
		Last Modified: Mon, 17 Jun 2024 23:58:29 GMT  
		Size: 111.2 MB (111158453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b89ab82cfb68dcf0114114543a7659da00feb606f498aae6ce2aad99b2e9a48`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 313.8 KB (313848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a2bbcf1f89f35dd755ead0f7aeaef3785ca51299465a477cb4c35ba2b4e138`  
		Last Modified: Mon, 17 Jun 2024 23:58:18 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d582da3204ba7dd4dbfd74b023cfe074bf7196ff83bcf9369ff4e29be61a`  
		Last Modified: Mon, 17 Jun 2024 23:58:21 GMT  
		Size: 26.8 MB (26812207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
