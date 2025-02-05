## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:e1af917f820be2e14ebacd00e503b3f40b1287e89119391e45873c98e61e45c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d6574666fdd21d19b03ff6076d1bccac9acd2193ca59ce66ee813c27fe0a393a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262575654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf306e26ba0843f5d704692b8b327249e5db63f982ad7fd7ea6903e7677439b2`
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

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:752706dc193c7b4440c127acad7a083f961ba7a50e54600392df5edcc127ca08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22916182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8852f7e5f9bbec4c1fdadb4afe5efa5d091707658ebe42c6ed00796d111736`

```dockerfile
```

-	Layers:
	-	`sha256:6419770c864e6c71920561349fe82f8e03a1c41204b5d6f5be71cd244ab75c6f`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 22.9 MB (22899026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd662c2bacad1d1e39bc1232c3cddedb4e1b52df4fa76082051ca0c11a62346c`  
		Last Modified: Tue, 04 Feb 2025 05:26:53 GMT  
		Size: 17.2 KB (17156 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3ca05128afeb4e4f0d38f0f070825224dcee2c0267787324cc83a514eec9cb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255013436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae24e7f3083145188e9a54e82aaae6847935def7ec05645d07c20f1af24e6c45`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bffe6c5b51dd4381b4530f9609162ef476ea615c703683f01ed181728c8dc05`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 1.2 MB (1207581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755dc834c9af075d6073c63aef912a8890cf5343bb0cd6a477da3cf1cebec555`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 3.6 MB (3596036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa16ce0cebecd775057f0b71b8f890c546d31bb1248365e7e4ff29ea4870294`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03715c2f02b17e42ca7f45d065e4f9ff91d8b76f32a6830d8ae958ab2263f4a8`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f491672b4b85aa805dff5d8975f4622301f42ca0a3c1d30101ad344e29dfdaed`  
		Last Modified: Tue, 04 Feb 2025 14:45:30 GMT  
		Size: 104.3 MB (104317718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe65565d1bb8cecba8a32487fd77ed001f41c465c3620d4d37906559a0a176f`  
		Last Modified: Tue, 04 Feb 2025 14:45:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c846ed6e7090aaa2ccff9e11e01c5b9378e709da84f1c2ffec0d4f61a156079`  
		Last Modified: Tue, 04 Feb 2025 22:00:32 GMT  
		Size: 95.5 MB (95503766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd8a1e693ddbe548da76d4517f817b1b21ea2d1369cb638dcf03834e35617b0`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 349.6 KB (349572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f23a74087b67d1aa71de7e1b3ae636d64b8f51624905cfa1f259e8fa063ae`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bff3d112e4aa5c0ed4b3bc5f8861d5f256d8e26c812aae599c9990aa9eb612`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.7 MB (22675669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:87bf0341b684c5d1dd3a4f388d3b0c88435f39b67409374d43f50e25f4b99020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22929335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b95eca43db85d42679163104a70bf50de818bbad157bde6ca5bb473017e54f`

```dockerfile
```

-	Layers:
	-	`sha256:fbfb10bd3842c990dc808dde2f7c3b1b7e40de9c6fd4ac61249b25fd83b4b6fe`  
		Last Modified: Tue, 04 Feb 2025 22:00:30 GMT  
		Size: 22.9 MB (22912042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ca9a39c3cfdf84f0e435c61e6c4d11158737219ec616d3f56fd636f54012c8`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 17.3 KB (17293 bytes)  
		MIME: application/vnd.in-toto+json
