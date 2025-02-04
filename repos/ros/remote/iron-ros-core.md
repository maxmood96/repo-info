## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:d34f6a88f7d8a1a7bf69354fc77b7dcd694a86fd3b3feb80535e4c1b4e3ed7c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:a17d0ea11441918a3123f1e1b0f1e747834dc04d4befab5f510e78aaed2bd377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158726449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323b58cbd6c267a1beb6acfd91e8a308043a9fcd736fd2b79a2d1e0b5bb96c5b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84978cd4920dbb6ce11792e880709796810884d9945087cff06a0b57cf496ca`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 1.2 MB (1207606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8477dd187360dc43e3f8b3b9094455579676d805dba6e105e0bba7d5ff67cfb`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 3.6 MB (3625035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37fe4809b99d383618c439a60815c0606887006924f154f8fd0209d279bed7`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeae0ad7c3a66464a0e67535cabdddec74030230337cfcd74e28118e7096df9`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f68e1fb716a6f991cef2069792082fcf733f82146983818f7b61cb9254eef4`  
		Last Modified: Tue, 04 Feb 2025 04:32:53 GMT  
		Size: 124.4 MB (124355396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834eacd2fda9baf4d52ab0b35cf309f08a7ce54cc18714f117e36ffebf7f583`  
		Last Modified: Tue, 04 Feb 2025 04:32:49 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:8d2f19a7e9ffa69f1bdaa7236fa87fb4f547998813011fc3dda01d2e655780a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19239624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a54437b77a771a5e519c3edc8beabac03709746d15337a4ac64a2b4e052404`

```dockerfile
```

-	Layers:
	-	`sha256:1e65cfb9c6b885cf70251a15e76c64765a1f23e949fca3a6d1379191c0d8c84f`  
		Last Modified: Tue, 04 Feb 2025 04:32:51 GMT  
		Size: 19.2 MB (19223259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa322610441eacd176794563fc77ecf963c30e408adeebb9fe7c1d9e2220db1`  
		Last Modified: Tue, 04 Feb 2025 04:32:48 GMT  
		Size: 16.4 KB (16365 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:12f9b2170e11a52d7305a6abfc8bb645aab71b33f043ba22ebc6cc32b3734255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153937505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c722353942070e3f847ee536084d2325e447aaac0266310901b1e32861e4a027`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 09:23:55 GMT
ARG RELEASE
# Tue, 19 Dec 2023 09:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Dec 2023 09:23:55 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Dec 2023 09:23:55 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 19 Dec 2023 09:23:55 GMT
ENV ROS_DISTRO=iron
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc648e781bb9c3ead233b1bdec9bbcf8d27119e3cc6f1578606a8207d368c17b`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 1.2 MB (1214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f6a3854a04c1db4b9e20e2199a111c1895a6875a996ff14f888b188f914505`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 3.6 MB (3595881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0556b8e337d14626adab2437afe4e58ff50a87bceded7cbb7b91cee3dd16281`  
		Last Modified: Tue, 17 Sep 2024 03:02:03 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c827c4b6d4a096daefeda34c696a00ade75c99fc663a2e1f1ceed2c8a543f74a`  
		Last Modified: Tue, 17 Sep 2024 03:02:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38e07acad4888bbb5c3c0ac5f99f96ef89a27985c87714eaa7cfda6c49e108`  
		Last Modified: Tue, 17 Sep 2024 03:03:37 GMT  
		Size: 121.8 MB (121765870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc435aaa7d7ea82804ddb887ec95aa7c68d1ab2fc9eb981be93a3f3b82d87f7`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:fe3e2587f80367fb6a901726f98e5e7cafbfed122e76959c37b4be19a0e682a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19205110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59933117d1d7e6494fac00353e9f7d062440e6c742e377e8b8ce5ffcff9d705`

```dockerfile
```

-	Layers:
	-	`sha256:c7e2c2cc282e969e8a2423aa026fabf25f64fea551c239037d8bb3f75816d5af`  
		Last Modified: Tue, 17 Sep 2024 03:03:34 GMT  
		Size: 19.2 MB (19188722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9155a360922796df69257bca56a3ee38501648e2e96bccc1801d913175aa1ba3`  
		Last Modified: Tue, 17 Sep 2024 03:03:33 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json
