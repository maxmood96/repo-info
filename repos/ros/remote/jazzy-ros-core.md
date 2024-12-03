## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:520d3772a70153f2f2506316e15e36399f0fe280ea888999a042a9425b14c9fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c44a53d5dab47e7276c07318d6c22a13f89c7a2638d72bddc0ce2039ae744ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156691094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950aa5188a19b69e1e8e6c42e862c9fe4702d2c7b895efa9d876a7fe5b36639e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb9b5148ae557dba975bb84acfb09e3d5ecb3b30a6664c1b158038437ff864`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 684.0 KB (684039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec79256506a8ed2c76d26fb5263d09a717a558dbad31f97bc79a412b71bc3d5`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 3.6 MB (3560620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa924df05280940cb19b9e74ac5885a2f67622eab697a7433b583a120694239`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 2.0 KB (2002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f3e08353bf8f53937fa7168cbad7d39df3214474bc9b07557880d6ff63b08`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01218c18dd3d57f0fd398836513b6b50fbe554ff4b460941357ebfb7289972`  
		Last Modified: Tue, 03 Dec 2024 02:17:25 GMT  
		Size: 122.7 MB (122691998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a4d000285c3d2a81b20a96c50372bd1cde9b88f7611ccaa417fea7a3c85459`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:694962901120f2c591e49b2b01e2f6c5cd204330b17e14cd0a338a7f99e0065c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17855393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d431685361c68448abf19459b83eb80bb43c07f2a77700206a60767210e84498`

```dockerfile
```

-	Layers:
	-	`sha256:c8590a6bd06b598630753c31e3acc5f74f4ebbb1c4876213c4f5ff180992e3a4`  
		Last Modified: Tue, 03 Dec 2024 02:17:24 GMT  
		Size: 17.8 MB (17839021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2fcb11cdee9d9e936b57fddaea730582222df362094aa30647fea9a427b8a5`  
		Last Modified: Tue, 03 Dec 2024 02:17:23 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5c1806dbcd5b7527c7bc7d8b83bbedb4564d5ea0c65d11d49dadfdb2d62f67d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150649176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010a702f7c8a4c69a683842d5c8520f3636f5fcfc1dc8568a249e31c91d7b72a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 May 2024 15:02:00 GMT
ARG RELEASE
# Thu, 23 May 2024 15:02:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 23 May 2024 15:02:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 23 May 2024 15:02:00 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Thu, 23 May 2024 15:02:00 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 15:02:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 May 2024 15:02:00 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENV LANG=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 23 May 2024 15:02:00 GMT
ENV ROS_DISTRO=jazzy
# Thu, 23 May 2024 15:02:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 15:02:00 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Thu, 23 May 2024 15:02:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 23 May 2024 15:02:00 GMT
CMD ["bash"]
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
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 3.6 MB (3559389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff1a4bcf4b73f4061b395e10618dfbe9b65ec7c26dc6ca185da014def6fa5c`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14439d57b5de5c25064fb2813b769c47d82006ef2777517c4ae416351d77522`  
		Last Modified: Sat, 16 Nov 2024 03:40:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88656ab2aa8b4c276fa4728d3578e2aa637b914c7cc65e1016f5861ad78de29a`  
		Last Modified: Sat, 16 Nov 2024 03:40:47 GMT  
		Size: 117.5 MB (117510931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c462529133b7263830c6dade28a2ef5fae040e0cc3fe2b0b11853d1315966b0a`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:c3d06634ad49f526c9dfb80699dac3411fba026893f84c2a5dfaa78a30cfd0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5095b458edeeaa9e3ca31b389b9e637783b161cb6fc8e78789ac513cf9ce626e`

```dockerfile
```

-	Layers:
	-	`sha256:e773c09b27c41896245d719de1c3658205379f24d4b8d118c799f5f4193afbab`  
		Last Modified: Sat, 16 Nov 2024 03:40:44 GMT  
		Size: 17.8 MB (17812312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d9a8681a94cf80ca665bc0f22d15dc1ce7347866ac7cc9635d7e4ca0c763e04`  
		Last Modified: Sat, 16 Nov 2024 03:40:46 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json
