## `ros:iron-perception`

```console
$ docker pull ros@sha256:7e65fa15ffc4472181b6194d6eb8ed930b9cb74eaee1d74b50f8590df1e7cda1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:f51d42ad93a735c39eb7ec4b078cd4bbf1e1011685de5d6c33f636e81d19aad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **967.7 MB (967697381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d7060d9b5361a1253b95818600b086e28370d76d5f3e4185f5c5186fef2086`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/iron/final/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3462f71d2a0e18954d5184197e3d81efd3f0f9532354e4efe8a9c00e89b52f9d`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 1.2 MB (1208107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613b3bdd3f675c9e6f115690c98f70841a8d5409c2abca2142578b657f0fdafe`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 3.6 MB (3625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c84f42f76f81695686241b905d92e4291c9c1f2e464b66234a989764d3ff2f6`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f679410b03e667d0a75866f5f27e525633bfd06e12beab159454064db254c8b2`  
		Last Modified: Mon, 10 Mar 2025 18:13:38 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9ddb9e9f15efe8ba457c6acec0d3f45b8e95c55dd3ce4eb51a949a9d1c1ea2`  
		Last Modified: Mon, 10 Mar 2025 18:13:41 GMT  
		Size: 131.8 MB (131807751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb65600ace7adaf01c69182fded1b02b1ddb5154b6e699eca14753a650c912b5`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60391d4a0a6e2a93edbb62bac36e015bea0682e45fca645e4f591ca9957cef4e`  
		Last Modified: Mon, 10 Mar 2025 19:12:09 GMT  
		Size: 85.0 MB (84977124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569c5e1d9be8c2cd97f0730c37bad04cf50abf80d3775d9ef9805050600a5cd`  
		Last Modified: Mon, 10 Mar 2025 19:12:07 GMT  
		Size: 325.7 KB (325735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36c4817e53bdbebd33189fe48a8bc6cad63f5659a0c32f87370e186df06ccea`  
		Last Modified: Mon, 10 Mar 2025 19:12:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0171da437077181109566035cc20b251d499221e473ad73e504373419a4fbd81`  
		Last Modified: Mon, 10 Mar 2025 19:12:08 GMT  
		Size: 23.7 MB (23735840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c553efda4c30cb8426a74feac040950a1079d83a6f8d8b135331b174815b6f`  
		Last Modified: Mon, 10 Mar 2025 20:14:03 GMT  
		Size: 692.5 MB (692475220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:895b16181ba3d7ed4fce94da0803ca48a0c169b502424b119d3aef94c367045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58343920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad86a6988ed9994d5d158e3cd2398ff821c78d93d48eb8046f1310d71c520798`

```dockerfile
```

-	Layers:
	-	`sha256:c739b044ca3ebe8a10a7efd6bf37d157c8b3a8c76ee32adce3db74bb80b0a7dc`  
		Last Modified: Mon, 10 Mar 2025 20:13:53 GMT  
		Size: 58.3 MB (58334245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad4553492561c3683e3ba46b1aaa1b6f00257d377323cfdd5cdc890dd41515c`  
		Last Modified: Mon, 10 Mar 2025 20:13:52 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c2d646af6511ab428a2ba7117da03ca084621c34687c9aaa7570672765024156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.8 MB (920822770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17370a663650148bc07b68ff1b14d5ced6075680c25d322f40cd6918f883c96`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 May 2023 06:46:37 GMT
ARG RELEASE
# Wed, 31 May 2023 06:46:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 31 May 2023 06:46:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 31 May 2023 06:46:37 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 31 May 2023 06:46:37 GMT
CMD ["/bin/bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENV LANG=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 31 May 2023 06:46:37 GMT
ENV ROS_DISTRO=iron
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Wed, 31 May 2023 06:46:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 31 May 2023 06:46:37 GMT
CMD ["bash"]
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 May 2023 06:46:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0bfece1d5df372ac2f8404edb6ab6f04310cb7578f9e31329eb26ebc084f487a`  
		Last Modified: Tue, 04 Feb 2025 14:47:10 GMT  
		Size: 121.8 MB (121825178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9250bf185b1a4c8850fefbdb740dcf3f379adf745c3255f7a8407fa0a57f1dc`  
		Last Modified: Tue, 04 Feb 2025 14:47:07 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ded77ac56df8a405c3c26852271748c1e71a81c45ee63a0d55740630ad56d7`  
		Last Modified: Tue, 04 Feb 2025 22:02:00 GMT  
		Size: 82.7 MB (82654236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4004f3b862a873c62b82c3b21e9865458c2c533493f0e0e9683cbe10414ede5a`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 322.0 KB (321974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d17c1a13e6b326395e65fd406b1ab982bb3aeaa3a440bb38ae18f1c0ff6175`  
		Last Modified: Tue, 04 Feb 2025 22:01:57 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a6e0521a8e25a70f9ea7a1a52c29b5da861405a6379670fd3f6fead37eab0`  
		Last Modified: Tue, 04 Feb 2025 22:01:58 GMT  
		Size: 23.1 MB (23128256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015ec4af46888f62648318abad124a0d38a2737e066e7b246a8838cbc0f3114`  
		Last Modified: Wed, 05 Feb 2025 03:41:09 GMT  
		Size: 660.7 MB (660726430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:iron-perception` - unknown; unknown

```console
$ docker pull ros@sha256:68d9f40c89126ca023d59f5a8387f9a0a5a8f732f332b2bd0aa8d12039ef1242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58337410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04468e939411fd563b8c55d6757a4cc3566d5833a9a14cb75d3a0ffa8809ad4`

```dockerfile
```

-	Layers:
	-	`sha256:35f150f237de2487144fab9d9b62f4b595dea43f3b95ad8c2da448722cf807ac`  
		Last Modified: Wed, 05 Feb 2025 03:40:58 GMT  
		Size: 58.3 MB (58327655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f507137f1eb5fdee1d4065c364e4477c5b82aa2279e9fc02fccf973cd4edd1e1`  
		Last Modified: Wed, 05 Feb 2025 03:40:56 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json
