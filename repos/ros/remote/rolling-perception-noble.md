## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:a76f32445d492945f71a4528f44b4d827c4155bd79164516136d598056168f13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:3f2d37055468da6c7188e60edcf3df6ac45b70b47b7de0bf2141f5c4c50e965c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.3 MB (622316797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a1749f83183cf95a2907270f4bcbd0d4b9bcd8b01e2e4a21cd3cc3410d2b51`
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
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
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
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0b17c6baac96d7db756a7a29271089771bf845d1d2432b8f383c32c74472e`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 681.8 KB (681782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be7a60531895114faa95659381ee5d79a0bbdec6a321017c9aff00134bc8ab5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 3.6 MB (3558001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77c28c37ead45f6f3ab8771374309bfff363eb3e7ea0ad231db189ebe26601`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b5df6e0234cd732806fcc6630fd52485c16c03f0853b68883fbc7fef826d29`  
		Last Modified: Sat, 17 Aug 2024 02:02:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c766166599f96e34cb2517326be1441db40166fb32fd32ca8f9a39e38c9ff`  
		Last Modified: Sat, 17 Aug 2024 02:02:51 GMT  
		Size: 122.5 MB (122509116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a979a9b024852c29b6166681ad284ae2d3cf59860c752d019cc71ed4d7de73a5`  
		Last Modified: Sat, 17 Aug 2024 02:02:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03f050a79216294d81d03356aabd6e4abd4924598128d7ea323b9128cc0565`  
		Last Modified: Sat, 17 Aug 2024 04:08:04 GMT  
		Size: 114.1 MB (114108736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e926b2d3bf9abb3fd0e15a5257b583a67cae7c52b9a696426506667837e26bc`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 320.9 KB (320920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f60140c3504caeb6f476b0852b3390c32695e11cdf799985c4253fde45ee5cd`  
		Last Modified: Sat, 17 Aug 2024 04:08:01 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645072ffb7af51c31166b7ab9edc25ad864b066dbeaf65d8af3bea0d414ebcca`  
		Last Modified: Sat, 17 Aug 2024 04:08:02 GMT  
		Size: 27.5 MB (27522529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78361a8dc26dcdd27a5dca24a2261ab5dbd5e3c39df6f3f3a7743d452177b9bc`  
		Last Modified: Sat, 17 Aug 2024 05:01:03 GMT  
		Size: 323.9 MB (323904508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a1be4bc8fc97bba990687ea44be74dd6740f66c4d83a5ffce56e0c2a5c4a799d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42109146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00eb30528ac32db8d4d5bcbdf5794b344e9b0a1cb427f094f3a0a84bdc1f6b7`

```dockerfile
```

-	Layers:
	-	`sha256:72eebd0a522c1d1dfe25ccb9832e49aaa42511c88a42566048b1033fb2c8bd1b`  
		Last Modified: Sat, 17 Aug 2024 05:00:59 GMT  
		Size: 42.1 MB (42099471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09e4cbd90c1eddd317271b910b71e214019b21342ec050ad25513662e425e53`  
		Last Modified: Sat, 17 Aug 2024 05:00:58 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5adfcf0be037e0486ea8ace6b21f1f2b7d690d028051922c6429cc57b299f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.2 MB (565173371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aba5062482007d0ca60675410a5ae0106c3c58c0245a2c99ae1b47a7da70fb`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
# Fri, 24 May 2024 16:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b51afdfa888108b5327eaa25f853a74f2c27da7625d948bc55801e64f6ca7`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 682.9 KB (682859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f820b5d2d06b509882a9cc403aeb5252f4c3f607b1f19440dfad83e210a4c`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 3.6 MB (3557860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44530f29d7b23d361456650ea1c47949c67bb960670945ab3965c4a0343ecd4e`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6a1ba10484c96c3d670c92fa3def01f5a86f8625fc602e8c98deb062a7a64`  
		Last Modified: Fri, 05 Jul 2024 20:47:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31c2175f6e9ecbe2c063179e8a46328b43cf72c74eab1ed37301f4e2c34620`  
		Last Modified: Fri, 05 Jul 2024 20:49:21 GMT  
		Size: 117.3 MB (117260265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8d191f93979eb95d46e111543c38c9a5e230be59354a67b050df7dee576514`  
		Last Modified: Fri, 05 Jul 2024 20:49:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0e211c2d874c04c82212c51e030d4d0b957ffdf0731f88f14395ce31aebfa6`  
		Last Modified: Fri, 05 Jul 2024 21:20:38 GMT  
		Size: 111.0 MB (110952482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed28c146690a6b6d0c23e6039516c8a68652b2114c3e7fa132676858c0ea707`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 315.6 KB (315622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65e0e5567bd2dddc8c8313e29ed4dc953966eb0eae751c0c6fdf882562e2fb`  
		Last Modified: Fri, 05 Jul 2024 21:20:35 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f7c3b40f4c3fa7abe72c030795ccfd8da56d2ce93c1b680b820a0a2c8fc52`  
		Last Modified: Fri, 05 Jul 2024 21:20:37 GMT  
		Size: 26.6 MB (26596158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7149c896fc2d09209c22d7d3e4ca3e8d66d022c6312b01ccde812cef4528c7`  
		Last Modified: Sat, 06 Jul 2024 00:08:32 GMT  
		Size: 277.0 MB (276960185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:46794aae958acf1c2ff0276d86c89261e7927b2b15a00a502c7f2080280f70bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41906123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887bae5de03a16d10f2c16c9b20d59a329134a4a4fc1e16a6ccbf97eabe3de0d`

```dockerfile
```

-	Layers:
	-	`sha256:a1c4d5a47d6297e67e7c3ab01a17bb50a9f6b6bfdfd7a425ba5392700121160b`  
		Last Modified: Sat, 06 Jul 2024 00:08:26 GMT  
		Size: 41.9 MB (41896087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b195fe2807ecab22bb053979f9e687c233b5b8cfa7c951b16fb823c0604215`  
		Last Modified: Sat, 06 Jul 2024 00:08:24 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.in-toto+json
