## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:103e437cb6af8b2cd1094ed931b5c03646f4d3d31b83aa28e3f3589fc681b939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:95705e5b3c156cff67597c9a3d8558329cda64a186cc72a52e23134083ea952b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089005089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175f376366e5ddcad8a8c023b6595fc1cdacd15625c1c9ae6f292b5883b13831`
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
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0330af77e2c89a74ee65a57294d62e06cde4784557cca3da750873c26c0ed846`  
		Last Modified: Fri, 23 May 2025 22:27:21 GMT  
		Size: 110.2 MB (110180376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068c5edb581ac55ae26e486c35f2f00cb6697ceb751a8193be32605040de1695`  
		Last Modified: Fri, 23 May 2025 22:27:19 GMT  
		Size: 343.4 KB (343423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef9d463f4212cee7f53a6dbeb38d74b1cdbe79dbb7b3b7f0b148a51fa1e2b12`  
		Last Modified: Fri, 23 May 2025 22:27:19 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99fb4f0977966392255a088ca7e2c783d25b8ddaf292dda347bed74b74e7393`  
		Last Modified: Fri, 23 May 2025 22:27:19 GMT  
		Size: 28.0 MB (28034318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccee48a62003bec48b4c9d5a856f4a105a4d4053d90a31b2beb8ba71b5e9f0c`  
		Last Modified: Fri, 23 May 2025 23:11:47 GMT  
		Size: 781.1 MB (781077151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4818a4d76bd79acbd859a2c55c23ca1ea1209f95bc4a7d9fb057f1b6cb7aab93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59961518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5333774855f3104b82201412008971c5c4558dc88ee10a52d159594b159ffa11`

```dockerfile
```

-	Layers:
	-	`sha256:d23df6822dec2f038d2bf3b67ef0c09aed1feb8fd11f6be305cf68ad5ad77e45`  
		Last Modified: Fri, 23 May 2025 23:11:35 GMT  
		Size: 60.0 MB (59951817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae67206cb4c7e7224e3a7c0ac8bde5dfd8b057a00b25a1193c9a047dbfc5e77`  
		Last Modified: Fri, 23 May 2025 23:11:33 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0e74e89a42e47171c40bf3933eb6562e2c0ddd51099466352f7e840b981cc266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.4 MB (988368606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca92a1f6199eab2a2a622b22ee0d1c0c1daba889424a0367d9f88a2a7675542`
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
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a5cbdbd8c75f25306fd7ca6eb25be1d1572cd036394c9c38f865882cb7f19f4c`  
		Last Modified: Fri, 23 May 2025 22:28:18 GMT  
		Size: 105.6 MB (105594559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ef8ab318bfc49e66a2b134cf7787901ed7b9cd4e0ff0b971c4c5a4d7fbad8b`  
		Last Modified: Fri, 23 May 2025 22:28:15 GMT  
		Size: 343.4 KB (343427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5892a56beec9f7e930680652b930d09c091baef633eccc9115c710dee42092d`  
		Last Modified: Fri, 23 May 2025 22:28:15 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ffe341d6a39efa0aa6aa8d2ef02958520eb6127df5081384f2361de3b8ac39`  
		Last Modified: Fri, 23 May 2025 22:28:16 GMT  
		Size: 27.9 MB (27930411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1df3273cfe502a1c4b97faa9a47f2af9cdb245170ed35a26d000f97653869a`  
		Last Modified: Fri, 23 May 2025 23:17:45 GMT  
		Size: 691.3 MB (691281737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:b876e16470ebf9dffb38aa669370bb8af63cd888e9dbf0b7ad5ee5e3392b0633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59913263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ca282a19892de3a4a6bd208650f9be664b3166fea30ca9b09c809d2ea01d41`

```dockerfile
```

-	Layers:
	-	`sha256:2fc3b07a0fe4d74a680baec013894e8dc906620516eee23e61d6b5ad2795d0f6`  
		Last Modified: Fri, 23 May 2025 23:17:31 GMT  
		Size: 59.9 MB (59903482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c239085f9924db69fdcb60d171b1c4257479cbcacab1fd0449af944220e069e1`  
		Last Modified: Fri, 23 May 2025 23:17:29 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json
