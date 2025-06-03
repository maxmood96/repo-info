## `ros:kilted-perception`

```console
$ docker pull ros@sha256:dab26ca3d146f97e2d07b8f339a256faf798231cb8433e0f7d4a5ac329363aae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:cfa513cd5bda79570f98caa5b2be2cf67715702d323a29e728aa27ef83dbf6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1088999001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343fcf51db30970016135d73864802f3cd4e8d0476f94ff695834f94d51151bc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Fri, 23 May 2025 20:53:19 GMT
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40688eb6ab717091b8ab853e446d63d8b599a40537433633e49421fc01e8ba47`  
		Last Modified: Tue, 03 Jun 2025 13:38:53 GMT  
		Size: 683.8 KB (683829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511cefe64e624a5297e6da7346ff47e3eeb63abae54ce95b69973dfa5472361b`  
		Last Modified: Tue, 03 Jun 2025 13:38:53 GMT  
		Size: 3.6 MB (3563712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaf3966317ae1566784e8b9428d42d9648e8bb216743f683047325d99626124`  
		Last Modified: Tue, 03 Jun 2025 13:38:53 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f48ffbd9bb786430457fa415a40d5ee2774efe6b9ca8071aa074d6dbf3cc277`  
		Last Modified: Tue, 03 Jun 2025 13:38:54 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7767b77e49a35d6dcfa96835cae86b747e3f835e474d864c4c636a0ac0d6b3`  
		Last Modified: Tue, 03 Jun 2025 13:39:09 GMT  
		Size: 135.4 MB (135403352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14018904b0b743f343c924cd937830d4550971e84cabb257732dcf66431c2b47`  
		Last Modified: Tue, 03 Jun 2025 13:38:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f47960427d73f74a7f2115f825f2bc60bac1967482a68a64b81b694b113700`  
		Last Modified: Tue, 03 Jun 2025 13:39:05 GMT  
		Size: 110.2 MB (110181823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeabb39dae26373a956a0d2edd3f461326f490f89d8c8568d2da91adf2e1c85`  
		Last Modified: Tue, 03 Jun 2025 13:38:56 GMT  
		Size: 343.7 KB (343731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cba3aab14cc159b2f31dd309c04c3c462ab7d37a2240db4684db8880580ee8`  
		Last Modified: Tue, 03 Jun 2025 13:38:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb24e494585517847245f7bee3feb2de70d2259ffda504ac3a21109e07b5752f`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 28.0 MB (28034338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e0ac6f682c12a6d58c3417869d5811ff453068d95ed48e199d7a93f3797ffe`  
		Last Modified: Tue, 03 Jun 2025 13:44:17 GMT  
		Size: 781.1 MB (781067400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:b45fe31f6ebc173d9c3f767cbfaf1988aa1d0bfc114c797c54686c2614314e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59961506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5189cc41bb007cfde33a207d0c6bb790ed3bed791f43096177f496a969827904`

```dockerfile
```

-	Layers:
	-	`sha256:2ec92ce9597290f9ec70d89bd70eb58e2780b59d414a9ee9cf24bc45d44deaf3`  
		Last Modified: Tue, 03 Jun 2025 11:12:30 GMT  
		Size: 60.0 MB (59951805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae63a0594bc5ff111b7790a57d64128280605f0dd845adbdf5e796ae48bc92e`  
		Last Modified: Tue, 03 Jun 2025 11:12:29 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

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

### `ros:kilted-perception` - unknown; unknown

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
