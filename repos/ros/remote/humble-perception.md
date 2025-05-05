## `ros:humble-perception`

```console
$ docker pull ros@sha256:a618a6ece49f4e9f6b8e1a9e8433c75405c76461d84de342340ed47515fc9e23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:b5c6ae3c2af0b27c7aa45670a2e1420470f0418c9e8d64ec6b6bbfd832a76c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.4 MB (954410616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd76c60238277341f88abc5d4159446cbf37ec47bc7740831f3eec7279db66b`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc0cb75a96fc365033e9c90cb0697634a996ee830f32708e403456ed01f4d52`  
		Last Modified: Mon, 05 May 2025 16:36:57 GMT  
		Size: 1.2 MB (1214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4b4e896071636d3437de6efb01a5545c16484eb75b086d3d310b105c98a95`  
		Last Modified: Mon, 05 May 2025 16:36:57 GMT  
		Size: 3.6 MB (3625685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3e7277c8168821d69668561f0684a23df95676641b2f5bd5939191de98b0dd`  
		Last Modified: Mon, 05 May 2025 16:36:57 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172492cea75e76031d73eebab577b7807873b0ab5dd42540f0472724085f12fc`  
		Last Modified: Mon, 05 May 2025 16:36:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c0dd50fef2133f73e56fb7b321bd941e63e5126799a68a6c46d7639ae32857`  
		Last Modified: Mon, 05 May 2025 16:36:59 GMT  
		Size: 106.6 MB (106624981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c48063d83a7c29eb89d52e692df6949bd3682caf3db40bec20778eff8176e`  
		Last Modified: Mon, 05 May 2025 16:36:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e893907ceaa195a693dedfd545a53935733a67350077cc004aa4f25023430fb2`  
		Last Modified: Mon, 05 May 2025 17:05:13 GMT  
		Size: 98.0 MB (97953904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d021f2e34f666bc8664cff4806c8662a806201edef9ff624154ba152b0ada1c5`  
		Last Modified: Mon, 05 May 2025 17:05:12 GMT  
		Size: 359.0 KB (359036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f137b6ba43f0df1ad8e21f42cb7c57d4412b897e0c6d7b5fdd3e9a4dcfc42075`  
		Last Modified: Mon, 05 May 2025 17:05:12 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed447533d41473355fd6a2e0e7ae69b04a36d09b4960da437d919c2de5ae2cb`  
		Last Modified: Mon, 05 May 2025 17:05:12 GMT  
		Size: 23.3 MB (23292617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa45741a6fe5c31fa8691242237a44ae6da770ead56dd350f5f0a018787601d`  
		Last Modified: Mon, 05 May 2025 17:14:56 GMT  
		Size: 691.8 MB (691802765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:bbd2a3b42fbd5bcaf3a45854ffa585e714e216168f17508140c3b7283ae7bdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57563900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a2e3b14a443b483b7d1166b217c47f5c9235db5f2c57a0b7ccd5adbdad05f1`

```dockerfile
```

-	Layers:
	-	`sha256:4ac995e5d911a60994aa7c8f4b290e2ada10db641fe19a9dfff97856d5b0e492`  
		Last Modified: Mon, 05 May 2025 17:14:42 GMT  
		Size: 57.6 MB (57554200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c51f88eceee775201390ddf4b8692e4560a34f53fd6e179f2d71b67fe2db8dd`  
		Last Modified: Mon, 05 May 2025 17:14:41 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c6068858585b810b119716b56e82029f0efc2d786e0fe910c5dd02cefc3269e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.8 MB (914775035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea4653fafc01b58c3bf71fe62e26cdd7ab9096eb303354c407c90ffaa6934cf`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b176523f9dd38625182aa1b27b731e23ace16310f4aba981578607d69798e5`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 1.2 MB (1214000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad677ba37f9174678ec5ae93d4ec686d5c911990dfd68f2917a2d78607aaaaa6`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 3.6 MB (3596994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dc6ed59947c90b653cb852244d8678f5c628a0287a08d61ac58f91cd15623e`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1f378741874b2ef719a549823a1ad8ac08f65e893d7e78e8c44dd32aa56ac2`  
		Last Modified: Wed, 09 Apr 2025 09:11:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163ae49ef6d582016a4496c4ac205ec01fba6474497e21655b3690b6264a05f`  
		Last Modified: Wed, 09 Apr 2025 09:11:19 GMT  
		Size: 104.4 MB (104357788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec322fe64af860101529ee59c11078c6c4bf13e33bb86cce625573f864fbaaa4`  
		Last Modified: Wed, 09 Apr 2025 09:11:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9335efb50570b40c8e99d4d8ba1626bdd3c483b88821cadcc2c7951e66c934c`  
		Last Modified: Wed, 09 Apr 2025 15:48:35 GMT  
		Size: 95.5 MB (95507833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d00d661fc473ddb2ed4d4c449bee3578a8dbf5dd5c6b94bdd554db62ec7050`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 355.2 KB (355188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe0ab15fb9ec7776a199f2ec6b805bda50bfa4b7f61d62e1260037f014958b`  
		Last Modified: Wed, 09 Apr 2025 15:48:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3f377ab8d078e1d999c61a1a8eabce42d1e4957ec847196cb1d1d486476773`  
		Last Modified: Wed, 09 Apr 2025 15:48:33 GMT  
		Size: 22.7 MB (22679387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f82afa7fe30db9520b3553d5e337c2a981ba50618d3450107010232917fc14e`  
		Last Modified: Wed, 09 Apr 2025 19:06:26 GMT  
		Size: 659.7 MB (659704684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:7585018c458783e6803d8774f8c02d4122a4d9a9707e10800b47bd99d1a5285f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57546616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511d63b5626b7bd01dc8b420e78289d1f8503f40735cd396e570645660b177e`

```dockerfile
```

-	Layers:
	-	`sha256:6f0a1a7850d55418d470c566c2aa186f18e31750a5761c8447cffe86c6122298`  
		Last Modified: Wed, 09 Apr 2025 19:06:11 GMT  
		Size: 57.5 MB (57536835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fc7c0b482cb5909f48abab8635eb4602a7dcb8f705ee4271af9a3a3aeac922`  
		Last Modified: Wed, 09 Apr 2025 19:06:09 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.in-toto+json
