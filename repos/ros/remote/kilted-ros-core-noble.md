## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:775e087be29b0cb51bce946ef951129b52467fd2c9855c37936f4647b0a88ae0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:8707fba43fda6f15bba7593189718319de5ec11a1bd4d4435c8a4452f469f450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169367374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eea049178ae193a3353def1b01b0453b1afe58bd561e9cca4e03dfa29fa51e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b91156110ebf5bcf8aff955155a3cac5c871a529c0956749cbd2e38258a3de7`  
		Last Modified: Fri, 23 May 2025 22:09:03 GMT  
		Size: 683.7 KB (683661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00676700a9a647dc4f7d22e0482fe6f4beacc969218897119327f2450823d67b`  
		Last Modified: Fri, 23 May 2025 22:09:03 GMT  
		Size: 3.6 MB (3563568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f027fb8836d362e986aabf6bc09c600e7dd68d9babac9be88ab53491d01bc86`  
		Last Modified: Fri, 23 May 2025 22:09:03 GMT  
		Size: 2.0 KB (2004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fe00d49e9d68067a0ad084bcc4f9dd7d1331c48d3dd776eb1250d6f27b6484`  
		Last Modified: Fri, 23 May 2025 22:09:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e9a0daafb0c3935bf2adb5b03cc81e3e3bb1b24f04e6c6cc874c48d131ade9`  
		Last Modified: Fri, 23 May 2025 22:09:06 GMT  
		Size: 135.4 MB (135400142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a875d6cf24d0d087ce03f230aedb7c853e4a081d23d611ea274587c8cfdac634`  
		Last Modified: Fri, 23 May 2025 22:09:04 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:38b8949e902b502a677b7ad8fb7294dada49a0cdc159581cf08aff484e8bee00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17981837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a50e805645b3732fd925310f283807cc8b8ad00edb18f6c66e331e67677d64b`

```dockerfile
```

-	Layers:
	-	`sha256:8849e95c8b5b4bba97d40418ae1272cd0c3df591624f2064825e5d2c70e69faa`  
		Last Modified: Fri, 23 May 2025 22:09:03 GMT  
		Size: 18.0 MB (17965452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5bd202d5acaa50fdf042f103785c65a76d502395feb5665f40cdc2a2d7ef97f`  
		Last Modified: Fri, 23 May 2025 22:09:03 GMT  
		Size: 16.4 KB (16385 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e3ce9590e6865c9583ff31ef27b37a947af8170d9239fdad5f791a89e0217b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163216009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765d7e9d1c7325ca927ffaa8ec52f89a859c08af97e9fe7179b5951f2ea91df3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
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
	-	`sha256:c5521c7833883a23f201df68ad3ae57170125b4a5031ea5b88220aad4c815876`  
		Last Modified: Fri, 23 May 2025 22:10:06 GMT  
		Size: 130.1 MB (130121355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071ba6d4b5b51d519bdefb818da3d77c29ad710ef3724c04aed51928889c95d8`  
		Last Modified: Fri, 23 May 2025 22:10:03 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:782e0f6ea90288f6716749a7be74958aab6a1189f6853138654428622b5c1feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17955983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4d17b92ada2de91b18d456390de77538a7494ddd13caa80cd452b6319e7b70`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f3d777f5b8e6b8f3cc991e8d0e79eac8f562c6e78d4bbea2e81d8271c3079`  
		Last Modified: Fri, 23 May 2025 22:10:03 GMT  
		Size: 17.9 MB (17939458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e73872300f68d98dfa7c383b00959869c2cda7e6b4604747f98b9c8cc7ac29`  
		Last Modified: Fri, 23 May 2025 22:10:02 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
