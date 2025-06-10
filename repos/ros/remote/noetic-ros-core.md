## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:fd6279f04e51fa61201a791da9a156129941887b95b614ae0cec7865ef49de4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:4c1435fd85be3edde3820f0d132ab30a6b030209dce4fa3ac428a2aa5a763caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.2 MB (409194642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9281103cce09d925abe6b7134ab3c5b7bb9158e57a2204c51175217dda4dfe9a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:acff80a38330a5a31d0736188c6f91a6220386cb22d5b19408f60acc98cd582b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29781814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c24c58ac29d31ce7d0aa7430c667961e4b5181a5e91efb301ac607f0ca640f9`

```dockerfile
```

-	Layers:
	-	`sha256:bf597893336763c20337f61fa235a39c41a481325d1f6a9ab15bb920f947b93a`  
		Last Modified: Mon, 09 Jun 2025 22:18:58 GMT  
		Size: 29.8 MB (29765457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4da31b4968be25636f6e96bc2ce17cbed293aecc74937629fce47cca4065560`  
		Last Modified: Mon, 09 Jun 2025 22:19:00 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:c9e79028edfa3207701777e232184aa095648173286b93c3b19d9a97d3d6c654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261696848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caab418962bcabcb4389a9852474cf889e69a8d8d42aed069ceadf6e08e87170`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:45:56 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:45:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:45:59 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 08 Apr 2025 10:45:59 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:4c3fe52db1c08dad3c7b6b220a14c86045074042d36e2c837dc2e40edd56be00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28755073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fb167ab0b004a48773cd9ba1e91987d02409e11ceb243fab07138e5769e8b6`

```dockerfile
```

-	Layers:
	-	`sha256:345b20852b51b4b6a90c0fabf2ca2dd4375862857d3eae23f1cfb10b7c447edb`  
		Last Modified: Mon, 09 Jun 2025 22:19:29 GMT  
		Size: 28.7 MB (28738610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31718c26115b6a7913cdc7b31880af107a5250f8ed21e8e0a487886e86c638da`  
		Last Modified: Mon, 09 Jun 2025 22:19:30 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:446b7e7c0ee9571f99fc8d3e1ef435baf74bcc773df03e227aaf9324c4cfc487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398398505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3a318d716d43e4d58ff35bfb131e0c92a6d772bdc9b48a60c8b85cb45f3ab1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:b82397ddb14c1819024f3133edd632651900407665e47afb69a7a70ca4698c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29577759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00752124d606eab9110ae3b228009aec9a84d6e855f843d44c7f21d59e4b9f5`

```dockerfile
```

-	Layers:
	-	`sha256:1c5a7501f9ea236e6fed5cb2b25a2eac5942a034eb162f3a8571451242cfcce0`  
		Last Modified: Mon, 09 Jun 2025 22:19:59 GMT  
		Size: 29.6 MB (29561268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13f1cc9ce0308d5c8ea9a10a3ad42a6fa44f30f50c2e5bd97d8b926ac07b0c9`  
		Last Modified: Mon, 09 Jun 2025 22:20:00 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json
