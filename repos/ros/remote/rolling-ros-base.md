## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:42f7b5ac83c674286dcc2e055226b8fb6deff6f2dcc57e82f58dc7b6ac335f96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:9ea1938d30d851fa79df496aeca4d144b2492a1155b7c063e9da80e7f73ebc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298690837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73009468a2afb304f6c7660197b1d222909f4754d698f432e4b91690683df5a5`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3b2484efd73305009117d35bdc14769dac7cc55a59591b622561a50646fbc`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 683.9 KB (683912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9ee196cfb19dc0d61a08117b1827bc75c1072281719ccd336f9acb1b3c93cd`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 3.6 MB (3560517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d977c02a44f1802debe1eee8710a41198847b4c0d9e6ea5c4a9e893d37a19c8`  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2dc8ecf92fab78948452397647f0e17ff6de87b314612dd9030f699ce17b85`  
		Last Modified: Sat, 16 Nov 2024 02:57:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a665f5b789f6618a5b5333bfaeced39dfa1da05d2fc4bcbe994b40c0050630`  
		Last Modified: Sat, 16 Nov 2024 02:57:59 GMT  
		Size: 122.7 MB (122680298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f731aa396c65b6542509fea891d58ddab177bae76da2dbcb1dbeecf8be19de`  
		Last Modified: Sat, 16 Nov 2024 02:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2931749fcbc5a8423464f2953dac75c839bba7110eb40057b47c9609f91bb21`  
		Last Modified: Sat, 16 Nov 2024 03:51:21 GMT  
		Size: 114.1 MB (114148980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db366bc2268cda50986b7cae4fa1ddabd7b92d8a85d54daad5f28244f0442207`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 326.7 KB (326714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402345e6fb621ea7619b1d18f51c5deb245660494444030ab446d6990881169b`  
		Last Modified: Sat, 16 Nov 2024 03:51:15 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf1712afa1cbeccd1a8995ce8a47f9c4754bd0b3c4127270986815107f4f39`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 27.5 MB (27533744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:8605e5d64f9bf695bd474e9eaa1984c153a4a977d27d4472c5467be934d6a0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23938670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306f92f38f4937f45e8ebaf2fade1ee690fa3b0c3332f161cb7301e12b15448b`

```dockerfile
```

-	Layers:
	-	`sha256:00a0a36b7f27c40b04d0159f5793a5e9b6bb1a08fd3559c4947bae0096b5555d`  
		Last Modified: Sat, 16 Nov 2024 03:51:16 GMT  
		Size: 23.9 MB (23921497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaaa58a5ef3f1a86a2da48bd9e723d2576dc7e62838c6bfc6942c577ffdbbfb`  
		Last Modified: Sat, 16 Nov 2024 03:51:14 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3816010eca888366190324e68b6f07908e34a99af9de61e47d8e2447a9306643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288675915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f59d954e709ebeb4b464484a200658dce24ed33b71a0505ffd44a9622f54a`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81328307e6050d58a3786b0d8d4e0e280336fcbe5e12ed33eafac0e62f39b3c6`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 684.0 KB (683965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dc71d0f9b404e0afdeede800f6310ebab3be587e6a707bfd42f238d09438d`  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336756432be3b9f7f44dd7afbc515faeb978872819b168b6908d418b86736edb`  
		Last Modified: Sat, 16 Nov 2024 03:42:13 GMT  
		Size: 117.5 MB (117515664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870e1f30b2d734ef09cf0ddbc60a50570d5c677f7f244597cd0092ccc28a9734`  
		Last Modified: Sat, 16 Nov 2024 03:42:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6924bb4685c143af5e2bec8959405bd94b82464901eb4ebdd3aedde9908dd1aa`  
		Last Modified: Sat, 16 Nov 2024 04:50:07 GMT  
		Size: 111.0 MB (111007847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7125737b4604e0deee24622b4f35e76bb2a81ea469185a71a4f100a1b17a02b`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 326.7 KB (326708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0549a9b72e086e413b36d2ba5a9a97fc7e361f45714c5af076739e3a30b02d`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8e30c16d2403bfc5a15fba00e5199f46f4591a1eee5d2275906979cf66b30`  
		Last Modified: Sat, 16 Nov 2024 04:50:06 GMT  
		Size: 26.7 MB (26685018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:168cc9da852dfd921589fd0ef6c9923580989080fdb3a1cbe3c38a8e0e2632af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23961372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc732bd5a1356f65079513c8c21328422fc745eb346c6df8edc093784223f083`

```dockerfile
```

-	Layers:
	-	`sha256:2bde361a6a2dac60ee9f7699306abdf35f518b420977d20f3dea5be3d351daae`  
		Last Modified: Sat, 16 Nov 2024 04:50:05 GMT  
		Size: 23.9 MB (23944062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450cfc3d353da63b52ae578cbdf62d291199fe48b1d634f73e1bb91c24ada593`  
		Last Modified: Sat, 16 Nov 2024 04:50:04 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json
