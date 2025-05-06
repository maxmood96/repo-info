## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:f4e8c1160bb1646955b1826663e2a63c1ee7badfe1127200499c271862686a62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:4c07f1ff715bcf8d199c8af7856cdac1a2d15e089563a09ecbc6ff27415011e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295751285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9c55244fa9bd1b8dfe3183cbdb866a42cc9660f86939e56607b4824776b3a5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58656080ce4e514db97d48231c0550506b43ded0130443d21377404c5676e68c`  
		Last Modified: Mon, 05 May 2025 16:37:05 GMT  
		Size: 683.7 KB (683653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5280560f16e6b782d3d30066e883cde4f6ae00c93b471b1532ba1ffe433849`  
		Last Modified: Mon, 05 May 2025 16:37:05 GMT  
		Size: 3.6 MB (3563327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e13385225e06971837651b173e32024deee9d17b3a7ff7822581578169463d`  
		Last Modified: Mon, 05 May 2025 16:37:05 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac4da06df8db42cea91479fb1ac419030728eea0efccdb53898b7f8e02aad68`  
		Last Modified: Mon, 05 May 2025 16:37:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0f30c7c1fee655e61d28c053019364c45d06de7db5f65613543ab002e8e21b`  
		Last Modified: Mon, 05 May 2025 16:37:08 GMT  
		Size: 123.3 MB (123290202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8dd1339a4e357ac978e3b91a0bfbe872b80ba84c685cac468507cb5980f3e9`  
		Last Modified: Mon, 05 May 2025 16:37:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4430a9c67f3082ef2a27c67f3a124730e4460a1ddca076b95ebf4956f98cdf08`  
		Last Modified: Mon, 05 May 2025 17:05:15 GMT  
		Size: 110.2 MB (110179959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddda9180ac085885a72846451f8b4696913303dc74381a73f869e1c07874a325`  
		Last Modified: Mon, 05 May 2025 17:05:14 GMT  
		Size: 342.3 KB (342324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75c2793236ce1fa40ecc9b868aa2aeac46e9d8feb19fe9bb4b36178a013e1e6`  
		Last Modified: Mon, 05 May 2025 17:05:14 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159f84a44ae90bbcb44ed3c560a13e16554ce2ed270281c4e25df0477eef3b8e`  
		Last Modified: Mon, 05 May 2025 17:05:14 GMT  
		Size: 28.0 MB (27969385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:7a4f99a0337d22a31133ab7c9b0f987c7b0fa48e1b17a4beba9e58a4997f7fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23856846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d4dcd9ed13b80755b1808feff06539ecced2a000908e78caeba6b96257046e`

```dockerfile
```

-	Layers:
	-	`sha256:8baf26a0224b66d6cf8cd1503d08e6a511bd2de48aac90e51e8c602cc04234b8`  
		Last Modified: Mon, 05 May 2025 17:05:14 GMT  
		Size: 23.8 MB (23839673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5365bc3a87d97ab5f12ff25cc657856c2cc7c559583ee28d8b08c10164e302a`  
		Last Modified: Mon, 05 May 2025 17:05:13 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f876356a2086f050c9398ff359c9e322df60117afce6183dc6422b9aed69c7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284157047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120e8c9ea0aa200fa98198ebd30161918ed7bca41631b5978a26f98008defb64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2e6d631663d69d931328844662622971edf603268f55d74da74b2f1832435b`  
		Last Modified: Mon, 05 May 2025 18:20:50 GMT  
		Size: 683.7 KB (683725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ec84cbb756b62af9e3d14e9f2de6ea3bab2ef3004d88f35527f5b06731e5de`  
		Last Modified: Mon, 05 May 2025 18:20:50 GMT  
		Size: 3.6 MB (3561582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3c6650198856d89ceb2205e3faf841383f08c4f761180ffb26aff4c61888cb`  
		Last Modified: Mon, 05 May 2025 18:20:49 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4f33a49a4d32aa02eb8d0ed177d6f1618ea6ed82efb0abb3c82978bf9b2487`  
		Last Modified: Mon, 05 May 2025 18:20:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13f1440921d6c455b0c453b9a65e79b665657a36ee08beedc3e331c4c25011d`  
		Last Modified: Mon, 05 May 2025 18:22:19 GMT  
		Size: 118.1 MB (118061733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be707329a911eeedcd5bc240ead95bd8af739c7b6f591ca0cde4104a5fafec3`  
		Last Modified: Mon, 05 May 2025 18:22:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c5cc438bb16467b7aafccf2ccc425854905fd4f1fed0e53d83f776a7d984db`  
		Last Modified: Mon, 05 May 2025 22:52:43 GMT  
		Size: 105.6 MB (105593530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c10d95728d44f00acef2cef3d35178bf418d690b7bb58050bd89c7ddebdc626`  
		Last Modified: Mon, 05 May 2025 22:52:41 GMT  
		Size: 343.4 KB (343382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5cd5f5290b840aa0c43626c0a6e9267fa7b4bf7e74641d3be63adfda8bfafc`  
		Last Modified: Mon, 05 May 2025 22:52:40 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b5c5eeb051e61a27e62dfa028976bcec2520807980515bdfa848348bf7d1ce`  
		Last Modified: Mon, 05 May 2025 22:52:42 GMT  
		Size: 27.1 MB (27061279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:96b943b5197e755b3a3822d804c287b3f265ceac7c930511f28f669c68443f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23879527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b18445a301f327a09bc457d09955b3416b15e1956de25290ddd4cd6622942b`

```dockerfile
```

-	Layers:
	-	`sha256:28addfe1b00c92d4484700ff238b43c7bccde6263b6dd032cfbadb889f19653a`  
		Last Modified: Mon, 05 May 2025 22:52:41 GMT  
		Size: 23.9 MB (23862217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e68a26771f5f37f606cd1c8f6c0de8a0904fd8657fb56e8d8c44c228fb5c5e3`  
		Last Modified: Mon, 05 May 2025 22:52:40 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json
