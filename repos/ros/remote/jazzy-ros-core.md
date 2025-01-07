## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:c9f62ef0e6b4244ce87b11a8e9e642ef2d82e6859c56da2ce0aab593713fa8c2
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
$ docker pull ros@sha256:8bff0a5b4d3ceab383123dc85e70b619c3bec5e75064fd54dd165cce1cbea04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150644193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b25a3ba2ede8e929394fe7f5134a014ece98ae6643fdbdab34438c416cf44e`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828cafb5606bfc377030b11684ade4e9ef094c5c8866214772783aeefc65dd3e`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 684.2 KB (684168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c673bfa5b508b4c5473b5d450e971cdb23a088fdd04c3bc04bc7016a57396a`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 3.6 MB (3559491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75b4ec669cbefd2d68a727cdba4a382b80cd85f1930c4c17ea0f72808c33af2`  
		Last Modified: Tue, 03 Dec 2024 10:21:25 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb025d30ba4de809090f9a665f12e338cb143fc5b85c065932d10e06f6d155a`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b494426cf0020c43838c91deb89a9ce6da60bcac380a766a5a3103053fc4a0de`  
		Last Modified: Tue, 03 Dec 2024 10:21:30 GMT  
		Size: 117.5 MB (117505391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c8974010aba9f0fb6ac664cee0cae14553b8820fc0de89028fb2488ebf0691`  
		Last Modified: Tue, 03 Dec 2024 10:21:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:65d421b1d011ce1a1155e495ad81ccdaf4bf7a7feb85772109a9a24d5f367d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17829504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0890295141e4d78d93bf5925237e3c761696a63540f3c715a3e9d19431e5e7`

```dockerfile
```

-	Layers:
	-	`sha256:f29a7572d5880618c65c5e1277aa903d7a0f205f9ba473e18cbefd71f42034fc`  
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 17.8 MB (17812992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a395a77a70de1d7127398167ea8f2851f9129b1c291ab02b3e0b171e1fefea9d`  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json
