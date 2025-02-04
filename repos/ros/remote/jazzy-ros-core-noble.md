## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:3c9377cf130468a9ef7bc90ce88bdf5ad8189898f7c1b776c57b0d4fc6045feb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:18f15f3f8432b1be111fb72ebbc410047664b4f680bd7744e6634057abcf3514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157691422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0d4bd6e28d429945958565be6e95e3ff8e96b506bbc107b3d243d73bad465`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304b0a16a8c4686c1ae17356937b1b3bdaf0753b3311050abeb20562d0b3ec6`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 679.7 KB (679671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb30b279e5182888c1ce5be1be8b6ef62da8c7af113d92327c1b685afb4e2bc`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 3.6 MB (3560942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7cc1887f83d20d948f86dead37ce8706504781f9cfa1e2912f3db6419e7a7`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4b7644d00b5e8121cbac43707d89d79b1578e713231dfe85d556a5c1b2e57`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7850fddc977116096c2669bcd969bb3ddbc023b18e0828e31b7e1170b7ce6`  
		Last Modified: Tue, 04 Feb 2025 04:48:12 GMT  
		Size: 123.7 MB (123694054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb43dbf2da736a743b2be0e44c373dd969448b32853643bd272d4567cc9ebb7`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4e853e6ef796bb2d217a79ef893c3ad8cb8fe145cac13c5bce5a3583380b7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17833423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258279ca1f78057a4fec6b81d1a3e316064fc445a26ff51a436550f38144c4b2`

```dockerfile
```

-	Layers:
	-	`sha256:9416d105ea50d8bc71eaec30085ce9241512676de54ca8e9b677506aeec54a6b`  
		Last Modified: Tue, 04 Feb 2025 04:48:04 GMT  
		Size: 17.8 MB (17817051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11467de67a55ad20db85450e4773d6022a5f7016ce15beeea6ccead6f4dd7275`  
		Last Modified: Tue, 04 Feb 2025 04:48:03 GMT  
		Size: 16.4 KB (16372 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

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

### `ros:jazzy-ros-core-noble` - unknown; unknown

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
		Last Modified: Tue, 03 Dec 2024 10:21:26 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json
