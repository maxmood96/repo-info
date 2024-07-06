## `ros:rolling-perception`

```console
$ docker pull ros@sha256:76aa96b7e4b62a1dbba7a2ddfb97934ae2e0c6af0ab279d0ac3d94412c2a1624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:1ed84ac6685fd235096e232cfaaabcb6def046b3aa0aa59718dc28f0435f27a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.1 MB (622107340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1ca4b6085a51f04c933c36ed727d2e4a9d2bbd13596c95ee7a14327b3d77e4`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f265dd1822d4bbda2f1664e89c70840207a1cb0f581e84bcae46c1c171fcf05f`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 681.8 KB (681846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928cb5f378100586d71a3f255bfe5fa4132b083e7865faab44a222e87b804bdf`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 3.6 MB (3558081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c330d2857efd338c3ffa191ca727dcc48f9935769f3a656679f59aa808305d`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e8991caeb96415de4fc0f3a65a35f66a7ccf9a27ed08f39a93c8037d290f41`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15aa456906e686b25d81fe30c2b8713c36e49eacd1b7b8d9e80feb7f38d6d2cf`  
		Last Modified: Fri, 05 Jul 2024 19:57:34 GMT  
		Size: 122.4 MB (122440869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d92833e9bcf5d58c3df73aed11c11222570327151eb3b8c271b060b0e22f43`  
		Last Modified: Fri, 05 Jul 2024 19:57:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6528b2c546be6197bcbea9d097ccaef9187ae8ed7adc32d4048e7fc4a91aef8`  
		Last Modified: Fri, 05 Jul 2024 20:52:56 GMT  
		Size: 114.1 MB (114108908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08475095e9a8825a734c5df3c889023dc187785bfb5925a068035d92b56f36c0`  
		Last Modified: Fri, 05 Jul 2024 20:52:54 GMT  
		Size: 315.6 KB (315620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12707b75d5c2f6bfcdbf3dbbe23d469df9341a431ecaf5d341005298cf3245bc`  
		Last Modified: Fri, 05 Jul 2024 20:52:54 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7062b9a2b1c85ccb83851bc9bb035fab5be0aca4ed0385643fc733c9c8d1cde`  
		Last Modified: Fri, 05 Jul 2024 20:52:54 GMT  
		Size: 27.4 MB (27446092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ff6d17c9a30b432bd7eac0f1b6bcb0e549a07fdaf696674b38a4c0fe11cb98`  
		Last Modified: Fri, 05 Jul 2024 22:58:20 GMT  
		Size: 323.8 MB (323845870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:b5b1d796301039f27915856f1bb5b5f83cf64471013bcb404dc6e47e084f5f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41905383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a2fd3cf9dab4bb906a5ffbe45194fa97ac6269a0af5f50bca690b3bbe683e5`

```dockerfile
```

-	Layers:
	-	`sha256:b3ee6cee12b18384c4f570c621974a613f04872de55136c53c384a41b30c8937`  
		Last Modified: Fri, 05 Jul 2024 22:58:17 GMT  
		Size: 41.9 MB (41895707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c523ec25316b676dedddbee85a09ca75b987289a568b360cac5c8f55ae9a5f8`  
		Last Modified: Fri, 05 Jul 2024 22:58:16 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

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

### `ros:rolling-perception` - unknown; unknown

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
