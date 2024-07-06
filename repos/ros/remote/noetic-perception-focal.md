## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:e4061cbfcbcf1367c0c7d1686dcbf19e74fd120065c6c05dc5f7b00a8169651f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:cafdc84812d38e9beb867c6e685877b65242324dd066d8fd6921da4542f57a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **833.7 MB (833687707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7bd014c5668a534bb0d60068dc02723507e593e319f814bb43069fccb85e29`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541596f8b358e9f0225f58281f3a5f29192357a2d9eba92a600eb4e7486da20`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 1.2 MB (1198610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904313c44f3c8af3a115d7f73029cf8628f3992e20054ad796c7781e3417adbf`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 5.4 MB (5361726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a0710e8ce116746283a133d532bfc0552b821c541c640314b033605b7efc16`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab8426a021e540c85fbeac7e60cc406e2b6038505811aa7a132de889ee284fb`  
		Last Modified: Fri, 05 Jul 2024 19:58:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb19495c8176c1c1ca74fa7251646aa38ade801d766bc5893d14708c768d452`  
		Last Modified: Fri, 05 Jul 2024 19:58:08 GMT  
		Size: 177.0 MB (176997016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df37cf2580810a1de28e2d3533ee7cee4d9439b281ae37a403f9ed021d1c2c8`  
		Last Modified: Fri, 05 Jul 2024 19:58:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186322a3cea702902612730d9773240ba365416e4c881cd7f65aa3aaf16b8d2`  
		Last Modified: Fri, 05 Jul 2024 20:52:57 GMT  
		Size: 50.7 MB (50728295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456a721c0061025155715d1703a2583ac18725b1e672cd8a9b047902f2c06159`  
		Last Modified: Fri, 05 Jul 2024 20:52:55 GMT  
		Size: 324.4 KB (324353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e4b749804c2f2606caf5e90a7cf23b41f8e07f3c271f12be85c9bfc25cfb39`  
		Last Modified: Fri, 05 Jul 2024 20:52:56 GMT  
		Size: 915.7 KB (915726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538aa884f13f0fbbecb2f87bc2c269238424d5c4865726a309809b6fdc583f0`  
		Last Modified: Fri, 05 Jul 2024 23:00:00 GMT  
		Size: 570.6 MB (570647743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:82b56d33e818ff4e7fc49522d44bb35d8423ccb6b17c284f77a3c1a83c2642e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51529569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a07370b124d0ba39abb20a78640ab84d8883602ebda5c756f9157cbdd5de4c7`

```dockerfile
```

-	Layers:
	-	`sha256:1f08121f24c2857329cd8014c24e64535289884a8c5122d16c01e9951e4c3c67`  
		Last Modified: Fri, 05 Jul 2024 22:59:53 GMT  
		Size: 51.5 MB (51520230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b4d2d6af6227372b12954f178f336cc19a08236b5fc54ee3577ccad38985cf`  
		Last Modified: Fri, 05 Jul 2024 22:59:53 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:9776038b9285e80487cb906f7d0d18b139a966bd0ec03a7c39c475035840e064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.8 MB (724751831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdc0809248e5c108bec50bdf8320294716d56ff19320d7a8785715cb61f4f9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f30cf37c3fd58825124b0f1bf686ac079d10bcea99ba8b2f6d1b21eacaa54d2`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 1.2 MB (1200145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d046f7fdbe893bfdae348a80dd5560e508012ed4d254d0b451554a52492062`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 4.5 MB (4488723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8c7896dff426ab4df0a37bc9f58570f0376c96a6b25482adba107154dcfca`  
		Last Modified: Fri, 05 Jul 2024 20:02:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68053c27827f8faf9453f43780db0948212bbb2fd5f1cd4bade0f6841a0283c2`  
		Last Modified: Fri, 05 Jul 2024 20:02:14 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf01d6db61aed61d096a4784518c9f045efa6cc61f20ff23c985ed4b92e77d`  
		Last Modified: Fri, 05 Jul 2024 20:02:18 GMT  
		Size: 157.5 MB (157470886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67194fb46b1c786ab9722506fa148b7c7df2462d50ab143fb103e9e328580345`  
		Last Modified: Fri, 05 Jul 2024 20:02:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b3cbee8cd7966ab19c2b1b496c2e63f3bf648e75d0a193b4c9e4c3bd0bd45`  
		Last Modified: Fri, 05 Jul 2024 20:53:35 GMT  
		Size: 40.3 MB (40292719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96907702e36b8490d4868107a57136333d7ab5e6868155993b7c16cc4045a4`  
		Last Modified: Fri, 05 Jul 2024 20:53:34 GMT  
		Size: 324.3 KB (324348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beed2409eb0c2d20ed05fbf1195d2222a0a5fe212e98eaa585684a77c7876258`  
		Last Modified: Fri, 05 Jul 2024 20:53:34 GMT  
		Size: 848.2 KB (848189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e0507dd9adff5e4217a3caeb9a2be5a342b2bf76cc34ef435d83a5f1ca51f9`  
		Last Modified: Fri, 05 Jul 2024 23:13:45 GMT  
		Size: 496.5 MB (496500973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:2e183530601c28cfbcb509f21ba01166dd4674835bcac6f269e4f062fdde7f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51165989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5db57c61bcc41db1bd2eca0c3904f8db5fcd79d4411eb4f633b8affb2e49e1b`

```dockerfile
```

-	Layers:
	-	`sha256:12f5aba226fb9ed8b25f4cc03489b77edee7eac62caac43f2a47e4ca3af3a6ad`  
		Last Modified: Fri, 05 Jul 2024 23:13:31 GMT  
		Size: 51.2 MB (51156589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269f18ec324ec7ec7510c2cad33aa570cf227e40e7aa5e938a16542823d6243f`  
		Last Modified: Fri, 05 Jul 2024 23:13:29 GMT  
		Size: 9.4 KB (9400 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:98d0f6e6a7e6f14de8f2caebb884d9996a8b9fb1dd9b5ad2350a5426329ef591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783747495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435bcdc37313e5f4e90b9747e5e41b2d0b2389ff11ca071b84450de68fc8118e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673e4e44515715664ff9b2a5adb09e1648eff1a4b4ab899b7f6e8c0fd752044`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 1.2 MB (1198574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d43d7d1a5f54ed2b85024e0d77f531ab91aa86aaabf9295f8868e2b8b3fcc3`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 5.3 MB (5341923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51eeb6a70063854832d2bd61b77b12d2874732b9b97a8ef4fea5ed42ea7afbe`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8394cfb37cac04ee2395560d7f228818c20a645b59d5d90d402e4872be51f0`  
		Last Modified: Fri, 05 Jul 2024 20:38:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299cb0f1714f02b1afbd480f617ed5188ebcc116920b7ad55e0aa5f62072fcd3`  
		Last Modified: Fri, 05 Jul 2024 20:38:45 GMT  
		Size: 171.4 MB (171400210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f7aa3b966ba0823727bca51b3aa86fcc3a7526a20d5eedc1ea559c07a277c`  
		Last Modified: Fri, 05 Jul 2024 20:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbe3a4b4bb81c8588d409832b8b9a4d18c33deda1e9dd948a1322f4eb51b2d`  
		Last Modified: Fri, 05 Jul 2024 21:11:07 GMT  
		Size: 45.0 MB (44991162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23044a43a251087ebb107523fd2852210f657781326ee28dc25f10b42e15873`  
		Last Modified: Fri, 05 Jul 2024 21:11:05 GMT  
		Size: 324.4 KB (324355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c1313d338a7f0902d34209cf3a139ed951fd941917020df4b5683f7ee198ed`  
		Last Modified: Fri, 05 Jul 2024 21:11:06 GMT  
		Size: 897.2 KB (897231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3098a2393d38456687956fd785ce01b3bbccdb0e65189cd422eae46c064a4fbb`  
		Last Modified: Fri, 05 Jul 2024 23:14:28 GMT  
		Size: 533.6 MB (533617353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1f9dcf6da877ad8c47333f4a64916820d6be2295c8836006df3924997815243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51399293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3873ae954d85747a292bb3ef3490ddefeea63f587f43259940ef0f7ab89bf9b5`

```dockerfile
```

-	Layers:
	-	`sha256:227ded306c207b39796058486140a7eb7f27db310ff3ac784de51468a4678137`  
		Last Modified: Fri, 05 Jul 2024 23:14:18 GMT  
		Size: 51.4 MB (51389592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872855a2a4ff89a530372847623f90a890632155b50dd16c50e888694dea1ac7`  
		Last Modified: Fri, 05 Jul 2024 23:14:17 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json
