## `ros:humble-perception`

```console
$ docker pull ros@sha256:527b97c83d9c71ff409e8c6642738b82b48a132b3714c0c8e732223709c91e13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:c77eda74a754d4c524cec964915039e03d481d1ea48c4910d574bcd767866a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.6 MB (954581186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cbd73b8471c0fd212efc2644580e776706062de6f04228783f2c19b6caa5de`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc3f3fda5033a747f4a1ec31069170d4ca68a86959654bd6d66aa04d272005b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 1.2 MB (1207573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9d8461cf4a7456a6bb953604596f7705b4d671b209d38e4cc6679e4a40a52b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 3.6 MB (3625025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9d2f77ec1a79d387e31fbbd4f09afe459288d5d31a37e070d9ed20fa7aa77b`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b473f6b69e3e1138f395fcc51ad215c50c1ff082c4ac233cd667d2314eba451`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7736667635de13df8ee65e968cfe0f8a29613c479af29c0b81cab777c7f56bae`  
		Last Modified: Tue, 04 Feb 2025 04:31:24 GMT  
		Size: 106.6 MB (106612459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e07623aac56c94d57a3409f91154f7e37f058d58ac7a3bfda82734fd192f5c`  
		Last Modified: Tue, 04 Feb 2025 04:31:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726033011fa4e598cf994e76eb5f8a6b8d23167836e44f1314d7b99effc07c17`  
		Last Modified: Tue, 04 Feb 2025 05:26:55 GMT  
		Size: 98.0 MB (97950928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c5691fcc72019ac31a877904b867333878f615e5cbcba3c315c11b06937a9`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 349.5 KB (349547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ac1ca67067e3dfa4c16b9e13f64baa5dad4e6b1edd27a7b3eaa440be7d325`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 2.4 KB (2410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ea86b324fe2cda680c1dd3831bb148b05ba29045c2c331f1e7e1a51ea7e343`  
		Last Modified: Tue, 04 Feb 2025 05:26:54 GMT  
		Size: 23.3 MB (23289302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a6b09646f76213c67e7350a4fbcdd52eaccbc8f206176889cbd3e8b710a980`  
		Last Modified: Tue, 04 Feb 2025 06:17:58 GMT  
		Size: 692.0 MB (692005532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:3f1cb5744e995ac50d50567d00be2bc562e418c4731d34aedb59a06718a56b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57533358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f15e3e884574297f7362f78f25aa08797030d4f25475f10236a64c72b18d59d`

```dockerfile
```

-	Layers:
	-	`sha256:a9c593a5d46786265686afa39d31e616e1b59194117bfd83164e5edc467d1d51`  
		Last Modified: Tue, 04 Feb 2025 06:17:42 GMT  
		Size: 57.5 MB (57523657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c834d3825c60c3fba606890e49af93371922552a4be5bd15f488e602ae4897b`  
		Last Modified: Tue, 04 Feb 2025 06:17:41 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0c889a4cf75531a6c768b58bb77fbd8456601357eb2bac7660a2c489df25c662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914089948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441542988372f2c0b97a3cdd453bb1d905e01d3d9afbe8a8a2566da93226a6c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:48f820de24ad6ec8445c6b22cb0048286de3789be116cb819f1632d833f980fe`  
		Last Modified: Tue, 17 Sep 2024 03:02:08 GMT  
		Size: 104.2 MB (104248768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a45581323c34fb26086d975e1aad2476e027d2d6dbc7fbc43a7ba8a057463d6`  
		Last Modified: Tue, 17 Sep 2024 03:02:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d7fb3f2145a764dae68a91d33961df7d08270335a1149b4c8ec231a7c68ef`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 95.5 MB (95501362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2056cdee121a8f7aba7d544f9dbc2098f1068d24b38c5c380143b5c965aaec9`  
		Last Modified: Tue, 17 Sep 2024 06:12:10 GMT  
		Size: 338.0 KB (337991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaafba2dac67131d8abb8cc1c154deefa1f261c8a6ea45890c38a327ab8ecba`  
		Last Modified: Tue, 17 Sep 2024 06:12:09 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc16a1d1ac077be73e099a09b28bd4a72f6e448919e903104f9f40a9ccdd13d`  
		Last Modified: Tue, 17 Sep 2024 06:12:12 GMT  
		Size: 22.2 MB (22246214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8345062cb5a1abbd168f691c276ca112ca7cbb0cd616074b75569f75fbf22fc`  
		Last Modified: Tue, 17 Sep 2024 07:55:21 GMT  
		Size: 659.6 MB (659581507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:fca4eab27a353e516af1c9bdff8eaa806c8f246c4ff94179c82a219cdc552087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57277343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946504180fcd7de189dc50ba066d98b3027685bea9af3a111d27e3ed35849f2b`

```dockerfile
```

-	Layers:
	-	`sha256:7aee9a0de81444b73a032acb30eeb9cd7e05587924310ed6e8c8e202abd64f78`  
		Last Modified: Tue, 17 Sep 2024 07:55:10 GMT  
		Size: 57.3 MB (57267315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27253494f59cfdec38ca070f76f3af12d4efeb3f6f852f31fd9a0404fc97a911`  
		Last Modified: Tue, 17 Sep 2024 07:55:07 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.in-toto+json
