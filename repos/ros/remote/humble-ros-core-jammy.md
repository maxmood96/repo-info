## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:a0395bb52b4f4c8b4977a20824db2273a46e52f60b2b996df3c99ac49b427140
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:106d4b5a60ef0bc99273a649a2bfde77e85e4534a71a6a4c5b5a0a4dc4cf505f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140983467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f4d4c297e560ce90a32daebd55a59616dba25425d91e2e61bb05776de44e36`
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
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:5c0817abf7dbe2caea4238658e8eb92343f1a1eb3101a854f31becabf3e23e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17132371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e7f3820b1d1a115cdc2d4c2c740011014eca976f4511f57fa4b7c1af37cfdf`

```dockerfile
```

-	Layers:
	-	`sha256:f1988ae116051e5b6fbef351c6c0e586d52041f19f8855cea830c7337536d118`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 17.1 MB (17115980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d07e3c46d650153503b859cecbbdb6e227ec04af7edba06567387821730fceb9`  
		Last Modified: Tue, 04 Feb 2025 04:31:22 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3806eb2651f779bf01b574270fc6a5be22d07fb1f99626f7fdd69c60c5faf6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4f051f0b8340cf13bdd7a6b7eb1c56d8f5982c6b96c5c39cdd13d0a9aba615`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
ENV ROS_DISTRO=humble
# Tue, 19 Dec 2023 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 09:23:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 19 Dec 2023 09:23:55 GMT
CMD ["bash"]
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

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e34dbb31dbfe74281470afdad75b47d36303936ef781af1bac0f37733df00d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17119150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29649a14b3da89bd7784772d27ad77776deba0513efbee5512e64410005d81db`

```dockerfile
```

-	Layers:
	-	`sha256:6e11afaf702d198971cfa9183713bb9e325735a8ef7bdcc6eab308e6af7d5724`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 17.1 MB (17102619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123c790614416b1a5e5be406526c3e1fcb74f17e04a59629e62702b2b7271d56`  
		Last Modified: Tue, 04 Feb 2025 14:45:26 GMT  
		Size: 16.5 KB (16531 bytes)  
		MIME: application/vnd.in-toto+json
