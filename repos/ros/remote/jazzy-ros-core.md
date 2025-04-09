## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:b3c30a4b88f3e3bc9d34520ff39c013241cd03616f37f0da4f1c5cc75a44fc6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:9744fbcc62881fcea353bad7738aca958a88d44a276be7ccb4f80a477f695e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156789041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3891cdac5a34c4785b06deadd61a5aad696e2b64ef94db02049c32dde5e6c3e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=jazzy
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7ada383aa2c6280bac9c268ebaf581c56fbb51fe93d68dadc5767cfe3e8b87`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 683.5 KB (683548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b2291f52139b2d1101b2533972976bfdef5729d6cf631b1fc71aff6d750988`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 3.6 MB (3563175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9160510a993869005d2908d7cc9e22a00b5eba06422a7cb4a6781c99b7799cd`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa283402fed4a52f6893bc3e06b6c82ec6010e19c3b03d2abaafc48dd29f8b25`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21dcfe2ef0f3a4727fa753057273619a0a55a48fcdaeb6b421d2ec396a88d61`  
		Last Modified: Wed, 09 Apr 2025 01:21:01 GMT  
		Size: 122.8 MB (122822201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d32b287957ae96296930b095c3a968ce94f082335911488ffca7004b0fff40`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ae2c87782438c9f18082db68730eeddf0982801f9f1128b7fad27b61a685da98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17847209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b670a0a218271b6fe8031421379c69f9fe5ef702176483949c223bd531a7559`

```dockerfile
```

-	Layers:
	-	`sha256:5607db8b7b0bb9adff5d601bc2d8d1b8e96f590b14f02df6e49e02e136a62063`  
		Last Modified: Wed, 09 Apr 2025 01:20:58 GMT  
		Size: 17.8 MB (17830837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ea2efc84fa43ccb604cf8617c7d39ed37ba7176cb1198e6f72fb356be5e8ef`  
		Last Modified: Wed, 09 Apr 2025 01:20:57 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2fad18cb74d16242525279e44c3fb0fe969deb5b630bce3c690e7d8ab3535739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158757505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264be025260ff1763b69674ba554f6a34cb7de805804e2fb8c0317fbab4bbfcd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=jazzy
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab5679ebed679dd3df1e6843c6b8f39fa8e45a051661cbb57e6e0b119a3cfb3`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 680.6 KB (680594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f185985e6550bd84d688dd66ba0a96385e0d1ad37d682fe238a7a01c0d8901`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 3.6 MB (3560303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc221ca73075ddc99f91aee5566348bad0f2cd626764c842b72eb0aab3c0115`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb1b676ccfe7049a341da1d054040b9421e7c6f7efced7ab1bf2aca22d5831`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d831e1a4059e2f42ef51fb31bbc35c38063fdc8eccaa465d49821f79dd0a5aa`  
		Last Modified: Mon, 10 Mar 2025 18:20:36 GMT  
		Size: 125.6 MB (125620540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a9d5a529cd232eba1f6392b838c02adaeaa7a2e4965c850a645b0fd30779e0`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fe558021bfa3322eeb16d6d945fbfbf8016d4a478e82d81eba16b77d995acbf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17802022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cb55077b9b95eb97ae39e85012560e845ce6cc1c9ee291cf6b0db59e6266bf`

```dockerfile
```

-	Layers:
	-	`sha256:4d1cacb35726ea88903b435ccd7f13d0c1fcae4c6d1dc3428b052110090ed0b0`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 17.8 MB (17785510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b43a019bd57286721cd8892989ae862e4b9cf3e0bcb159d31d255a891794ad`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json
