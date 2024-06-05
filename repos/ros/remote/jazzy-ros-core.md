## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:4977e21d0255e135eca0d146f7beb97a1ba5333997b31fbcef58b6c0a52927ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c46bcfde6f9df1617f990578e150d3219966daad7c3d2b3367ba40f0d90f4f3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157459298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c1f59356d8f13ff011d5cf98bfa751c5d758e69d55abf64e9c69b2224147a8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:99c388abb370564e65ec4ae9823d6ad580fe327192c9d24180f807f29ab9ccd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151611614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46d34d1522815ee822844042a400ff171999be5f292158a22d3eddb527678e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
