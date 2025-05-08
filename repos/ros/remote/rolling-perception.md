## `ros:rolling-perception`

```console
$ docker pull ros@sha256:e54e10c2d191d6ad480f3c413ff966491b971fc8340010397e2d24156cb1aed9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:70eaa77f69d6ddaea2080e0e05d970cc3fcf076a4dbaa73de9ebcd02100933d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076508504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299ddac61c4799e06f6fe8fa12514e6b77efca77ad475a1dcef174f7c8dbfad4`
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
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58656080ce4e514db97d48231c0550506b43ded0130443d21377404c5676e68c`  
		Last Modified: Thu, 08 May 2025 17:23:01 GMT  
		Size: 683.7 KB (683653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5280560f16e6b782d3d30066e883cde4f6ae00c93b471b1532ba1ffe433849`  
		Last Modified: Thu, 08 May 2025 17:23:04 GMT  
		Size: 3.6 MB (3563327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e13385225e06971837651b173e32024deee9d17b3a7ff7822581578169463d`  
		Last Modified: Thu, 08 May 2025 17:23:01 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac4da06df8db42cea91479fb1ac419030728eea0efccdb53898b7f8e02aad68`  
		Last Modified: Thu, 08 May 2025 17:23:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0f30c7c1fee655e61d28c053019364c45d06de7db5f65613543ab002e8e21b`  
		Last Modified: Thu, 08 May 2025 17:23:09 GMT  
		Size: 123.3 MB (123290202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8dd1339a4e357ac978e3b91a0bfbe872b80ba84c685cac468507cb5980f3e9`  
		Last Modified: Thu, 08 May 2025 17:23:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4430a9c67f3082ef2a27c67f3a124730e4460a1ddca076b95ebf4956f98cdf08`  
		Last Modified: Thu, 08 May 2025 17:23:14 GMT  
		Size: 110.2 MB (110179959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddda9180ac085885a72846451f8b4696913303dc74381a73f869e1c07874a325`  
		Last Modified: Thu, 08 May 2025 17:23:05 GMT  
		Size: 342.3 KB (342324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75c2793236ce1fa40ecc9b868aa2aeac46e9d8feb19fe9bb4b36178a013e1e6`  
		Last Modified: Thu, 08 May 2025 17:23:06 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159f84a44ae90bbcb44ed3c560a13e16554ce2ed270281c4e25df0477eef3b8e`  
		Last Modified: Thu, 08 May 2025 17:23:09 GMT  
		Size: 28.0 MB (27969385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd58c7da830a24b1246db716b532f987ee29875b9c20dc3cc945cd347e0e6b2`  
		Last Modified: Mon, 05 May 2025 17:14:57 GMT  
		Size: 780.8 MB (780757219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:ca1203e46c46978298678106755b79947386fbb856fcaf95fd425fa4f6e7c09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59577709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfc39840b84e9cbd32998f96c0375638cbaf708795057da2ac1c014b1a870ee`

```dockerfile
```

-	Layers:
	-	`sha256:7787446da4894e7bb85f3757464afd86c1edbff1e4d3d9c82a93790505a32e0f`  
		Last Modified: Mon, 05 May 2025 17:14:45 GMT  
		Size: 59.6 MB (59567999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf136f2752a58c7f149ba1f5a29710be855d7a57331d57a7fa1671046e1b877`  
		Last Modified: Mon, 05 May 2025 17:14:44 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:08587dc4a5ce17cd0949741e08afc1194804c1e0b9b72a9b137c3d684596fe84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.1 MB (975124320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b536254b9ad4dba3657e0e17dad6a478a3ef5e34f82551abaf5cf1041ba160`
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
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2e6d631663d69d931328844662622971edf603268f55d74da74b2f1832435b`  
		Last Modified: Thu, 08 May 2025 17:05:37 GMT  
		Size: 683.7 KB (683725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ec84cbb756b62af9e3d14e9f2de6ea3bab2ef3004d88f35527f5b06731e5de`  
		Last Modified: Thu, 08 May 2025 17:05:38 GMT  
		Size: 3.6 MB (3561582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3c6650198856d89ceb2205e3faf841383f08c4f761180ffb26aff4c61888cb`  
		Last Modified: Thu, 08 May 2025 17:05:39 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4f33a49a4d32aa02eb8d0ed177d6f1618ea6ed82efb0abb3c82978bf9b2487`  
		Last Modified: Thu, 08 May 2025 17:05:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13f1440921d6c455b0c453b9a65e79b665657a36ee08beedc3e331c4c25011d`  
		Last Modified: Thu, 08 May 2025 17:22:46 GMT  
		Size: 118.1 MB (118061733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be707329a911eeedcd5bc240ead95bd8af739c7b6f591ca0cde4104a5fafec3`  
		Last Modified: Thu, 08 May 2025 17:22:38 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c5cc438bb16467b7aafccf2ccc425854905fd4f1fed0e53d83f776a7d984db`  
		Last Modified: Thu, 08 May 2025 17:22:48 GMT  
		Size: 105.6 MB (105593530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c10d95728d44f00acef2cef3d35178bf418d690b7bb58050bd89c7ddebdc626`  
		Last Modified: Thu, 08 May 2025 17:22:39 GMT  
		Size: 343.4 KB (343382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5cd5f5290b840aa0c43626c0a6e9267fa7b4bf7e74641d3be63adfda8bfafc`  
		Last Modified: Thu, 08 May 2025 17:22:40 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b5c5eeb051e61a27e62dfa028976bcec2520807980515bdfa848348bf7d1ce`  
		Last Modified: Thu, 08 May 2025 17:22:42 GMT  
		Size: 27.1 MB (27061279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6cb86231111a7216edc76110e39d81e4125a4e925eea5d52132acbc6d26106`  
		Last Modified: Tue, 06 May 2025 01:44:53 GMT  
		Size: 691.0 MB (690967273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:aa57db82648b69a120b29386ffee576c01790da3d182d15e23cca7f54577b1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59531789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acded046cc452a2d1f8ffbf4e5fd6d7b8fc1a1c8b40b8cd92889e8a8492cdac7`

```dockerfile
```

-	Layers:
	-	`sha256:0639c45192c1b5a1d76f4391b4109a6a6dcf28b079b392f863a167635ba5a7ff`  
		Last Modified: Tue, 06 May 2025 01:44:42 GMT  
		Size: 59.5 MB (59521999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af316609919e7dc42f2e8b8154ba070aa3ae3d329896e4708f8c9223448e3366`  
		Last Modified: Tue, 06 May 2025 01:44:39 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
