## `ros:iron-perception`

```console
$ docker pull ros@sha256:efc24a544e0be5d17f4ed46e7c7387ce54ac418e8aa6ad59d567d6593d99df20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:d26dd16cbcbd997d0c7733567a7ba93bb6299681bae4aa00e457cc42e48b2564
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.9 MB (959858909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117e319358fa15fcf13e9e4c0e0762b409ac8a6f74ef6a3065b316ea3860ee47`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:19:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:19:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:19:27 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 17 Jan 2024 08:19:28 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 17 Jan 2024 08:19:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 08:19:28 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Jan 2024 08:29:16 GMT
ENV ROS_DISTRO=iron
# Wed, 17 Jan 2024 08:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:30:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 17 Jan 2024 08:30:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jan 2024 08:30:05 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 08:30:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:30:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Jan 2024 08:30:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 17 Jan 2024 08:30:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:32:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da4158c1796fdf3290b33130c94d61658490350332349edfc8ce4efb7e40b2`  
		Last Modified: Wed, 17 Jan 2024 08:37:03 GMT  
		Size: 1.2 MB (1216199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b255e5b6ecd708d89a94cf949aa22e792def44df162bda933a732cd23166e`  
		Last Modified: Wed, 17 Jan 2024 08:37:02 GMT  
		Size: 3.8 MB (3828998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b54915a2b753d73bef87bb311bba508a235517ea06f823ed945e7780c6ea501`  
		Last Modified: Wed, 17 Jan 2024 08:37:00 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58126d36f7fcdeee8c0634c3db008d3bd373292caf67204befb405e4be3d24a9`  
		Last Modified: Wed, 17 Jan 2024 08:37:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339f3ed03a2333552f0cb64fb2e1842df2e782ec675734afb453557b9ff752f3`  
		Last Modified: Wed, 17 Jan 2024 08:39:48 GMT  
		Size: 124.2 MB (124213172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db72eabeba6f7e8f878873f28b048ff0363ac35c7c3fee28bd8860b3c6fc485`  
		Last Modified: Wed, 17 Jan 2024 08:39:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720c563e2b4cbc07c7c051485788b3dd5a5a2f3b403bdac5957487210cfcc076`  
		Last Modified: Wed, 17 Jan 2024 08:40:08 GMT  
		Size: 85.2 MB (85170415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837c0fdb5c23e6bb4bc32ead3d9a024f356c1e68e7ed4673f9252f56edaf44ba`  
		Last Modified: Wed, 17 Jan 2024 08:39:57 GMT  
		Size: 310.0 KB (309988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b155736b2e7d77e72aad676bd44c4ed29f3833e80ae373e56e6cf6fd6ee700d`  
		Last Modified: Wed, 17 Jan 2024 08:39:57 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c07249ad936984220ad4927c7db4e2f315d3b3f99d18b69b2d6e2f207fb645`  
		Last Modified: Wed, 17 Jan 2024 08:40:00 GMT  
		Size: 23.7 MB (23733121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9a6f30e607a90a5d47dee6ca20db5bef6377b2f3f372bca2058ce39f868bfe`  
		Last Modified: Wed, 17 Jan 2024 08:41:48 GMT  
		Size: 690.9 MB (690934921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cc6be110deb9a9dd2046ed3cae5981440271496856469117b2e8a6952f707cee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.1 MB (920099446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92a6cd27d1cf7210751004ca9c189cd7f2cf26cb8e6f377f354260314ba669f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:48:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:48:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:48:41 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 17 Jan 2024 07:48:42 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 17 Jan 2024 07:48:42 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 07:48:42 GMT
ENV LC_ALL=C.UTF-8
# Wed, 17 Jan 2024 08:00:15 GMT
ENV ROS_DISTRO=iron
# Wed, 17 Jan 2024 08:01:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:01:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 17 Jan 2024 08:01:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 17 Jan 2024 08:01:08 GMT
CMD ["bash"]
# Wed, 17 Jan 2024 08:01:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:01:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 17 Jan 2024 08:01:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 17 Jan 2024 08:01:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:03:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4f514e1260adbe3ba8baa42d4f9a9086cbf9299b6d7068882e8d30aa12bcc9`  
		Last Modified: Wed, 17 Jan 2024 08:07:32 GMT  
		Size: 1.2 MB (1216488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d9d057bcf8336ad1f73b5ec5765daed816a52ca71ae19bbd18af57e1a96379`  
		Last Modified: Wed, 17 Jan 2024 08:07:30 GMT  
		Size: 3.8 MB (3800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819b9998df89ce1f731210a11883797f464f3864c0bd79591c8fef249460cd00`  
		Last Modified: Wed, 17 Jan 2024 08:07:29 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fc651ee741faeba360c00a4c5d5afe3336c6b7ae929afb46d5223fc3f1cec9`  
		Last Modified: Wed, 17 Jan 2024 08:07:29 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc579135df7b7535cbaa3d2a4235dea2748621eba9bdd7e6b4fe84f1fe6cba87`  
		Last Modified: Wed, 17 Jan 2024 08:10:12 GMT  
		Size: 121.7 MB (121673399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeceafbe02e3d7785607584d5e90e5f237d19808231228e55d3eadc438c8f1ff`  
		Last Modified: Wed, 17 Jan 2024 08:09:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af81c11df2731bdf4242b28eac23fa9482eb865425caef5f0cd41cb88658b9c`  
		Last Modified: Wed, 17 Jan 2024 08:10:28 GMT  
		Size: 82.8 MB (82844261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811f9047c1baee2a9ab1bf9bf3cc1ef5fbd0ad626df7abeddbae27d0f7a62046`  
		Last Modified: Wed, 17 Jan 2024 08:10:20 GMT  
		Size: 310.0 KB (309987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8464b08483fd1890f64dbe98b26cf4ac76d2e04489728b308537c781c4da97fd`  
		Last Modified: Wed, 17 Jan 2024 08:10:20 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7f451001e8655881c3f32982b9a1118a9a6b6194a77990df257932a68d8353`  
		Last Modified: Wed, 17 Jan 2024 08:10:23 GMT  
		Size: 23.1 MB (23119405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bdfb2715fae0e7dfaa9550e0055dcdc0c7d5a1df794e6ba1936270a2bcf794`  
		Last Modified: Wed, 17 Jan 2024 08:11:53 GMT  
		Size: 658.7 MB (658730386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
