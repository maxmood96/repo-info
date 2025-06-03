## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:b3180e71890ea8aacb0023e8ce6793751851809cc9319559ed34fdf3e4c8beab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:2839397da38012606d3f6323ba5dcf8e34a1638ac8f383b087d900079c05fc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076612279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b9ded77eb5ffaf74c10277c85e7fc7223f60675b3d9aa0889fac13d76cbcd4`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f9f16d221b9a193b1a080b2673609f80f64ede41f3f81c206698e992ac9fa1`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 683.8 KB (683811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88f57e92d728e668d2ec085a2a883a4a34de7358c5ae73ab669d9d0dbd34242`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 3.6 MB (3563720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46c7bf8a560bdecd06b706f996ae07581fd85ea16d14584cfa8cec8aef4d2cc`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341fb3faa63f0489dab4f0a12e3b29eff9ce565faa7156b7f3d9055ed3ba6007`  
		Last Modified: Tue, 03 Jun 2025 13:30:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f2ce02ff513de028c65887ea53630d7a99c801a501871898ce4c97695115ad`  
		Last Modified: Tue, 03 Jun 2025 13:31:05 GMT  
		Size: 123.3 MB (123309297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434c602a34bcd520302797433be6f8c41329d0a12bbfced7922b0ac74276902`  
		Last Modified: Tue, 03 Jun 2025 13:30:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f80f66809e8d851621b51dc33d9630198a62ce80e16f7feab75496a1f23798`  
		Last Modified: Tue, 03 Jun 2025 13:31:02 GMT  
		Size: 110.2 MB (110181616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3999dc1f9ecc560440d5247cd73447037c04c5053ce5b1f73f8f060a0ebe9e7b`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 346.1 KB (346125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b40755095da1c5c4d3434a4e38fe190acfc281ffa2d0da3d71cbcd14a05d0c`  
		Last Modified: Tue, 03 Jun 2025 13:30:46 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e955cd61a0672a29fcb7c5dd1cdb21cd12c405f549aee9fc4807c6eb9fcc97`  
		Last Modified: Tue, 03 Jun 2025 13:30:54 GMT  
		Size: 28.0 MB (27969498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3f4a15876b42ac2b042f88984f0d71a9c20cd5223a4275a33d3ed30c7ab0a0`  
		Last Modified: Tue, 03 Jun 2025 11:13:46 GMT  
		Size: 780.8 MB (780837380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:eb57c64f3e5496e82beb293b31f2efbb88fd3e577efca206c59924d0fe04d11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59835941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d8d36169ab341667e42231b90bd3feea805da0d3084136437af593731f86e4`

```dockerfile
```

-	Layers:
	-	`sha256:63435aad3b4924b13089751704f3df02103f108acfb046c167abe47be14a781e`  
		Last Modified: Tue, 03 Jun 2025 11:13:32 GMT  
		Size: 59.8 MB (59826232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdeac60e921a49da7d68fb7efcb74938db20de95b82c40aeb8adfd27487d8e9`  
		Last Modified: Tue, 03 Jun 2025 11:13:30 GMT  
		Size: 9.7 KB (9709 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

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

### `ros:rolling-perception-noble` - unknown; unknown

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
