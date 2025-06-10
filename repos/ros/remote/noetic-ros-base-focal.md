## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:9ad9f28a6b69e9656e29bd4b8c51d4e42969b40d25f36abf1c5f61a61c89b09e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:4f01fa743be43da0e14ddf2ac29b5118d9c0eb4057c9761c13303b8a52fa9c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460272792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607ca0f020489b85d74ef5ae2f0ce8e901813af48008b0a622fc06cd41bf0d1b`
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
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
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
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ecf093a9124f383e5acc3a78d21be9e4f20515e24b2e0c8169a199d845c1c`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 49.8 MB (49754505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c240714a1b7806b225c5f9dde0ab272ceaa47a40ac7b752cbe0370bbaf3976e`  
		Last Modified: Mon, 09 Jun 2025 21:39:27 GMT  
		Size: 348.0 KB (348012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0451913b17a56844e9c92165120da313434cba935ddb3353799081a241b27c`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 975.6 KB (975633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:c081b974b2e84ce8ba0066b91664245b12a4217c7bf3121b382cfffea9522495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31302280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3aba0ed8be28e189623a99f7b2b073874abfb184f1742a959bb3bc8c2e327c`

```dockerfile
```

-	Layers:
	-	`sha256:f743f4f945c8627b2c94cb0fb0f577742f5489ec6d509d3d8ce4a38f0ba03a06`  
		Last Modified: Mon, 09 Jun 2025 22:18:34 GMT  
		Size: 31.3 MB (31288594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5145030147e7ed7e8d1f4d7fa5d65e7f95d250e533960a796d0481506eb56d0`  
		Last Modified: Mon, 09 Jun 2025 22:18:34 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:31818b9103a0d47738690ff8eaacb928520bf92017fc1c6c4d5cdad9261fa1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292791861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae49cc2167e0598b690cd174a01b8457d8d2f9eca339bedb7b77d4d1c87b38b`
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
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
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
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0306cc8cd95c4d090ded2ccdb527b61a1fa1b77279dcd9d99caee9665231f`  
		Last Modified: Mon, 09 Jun 2025 21:50:36 GMT  
		Size: 29.8 MB (29845900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f895b7132ec2355664c60f7339ba7673f3bc1e481242742ec7c0a792f400b`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 348.0 KB (348006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31d7a3f2c23ccacb5df0f3b9478367ec6c1b2527626899c0d3c6c0386685a1`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 901.1 KB (901107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:02961273e4e5adbf0edbaa55e408869e8a76c8e89bfb3e44cc748d1d47775f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30012724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c4c950bdfdef4c337e4fde12825560ac2c5ab3ed6b230fc9554bed950d65da`

```dockerfile
```

-	Layers:
	-	`sha256:38dd0a9571edf6b5307ea32643bbb13e20f6963b38e69461f06341aa9100f589`  
		Last Modified: Mon, 09 Jun 2025 22:19:07 GMT  
		Size: 30.0 MB (29998944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35dd4a9dda0678fcd4bb804ba29e39fb44b9355c78cd00f096b6a69c4da32903`  
		Last Modified: Mon, 09 Jun 2025 22:19:08 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5626d190770d234143954698dddf98a9cb97a3429922bc05e310d034c5ee7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1a8972be4098e73a367bc535112949e47c4dbd1e183fa1e6f87ea23060dcac`
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
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
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
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Thu, 08 May 2025 19:41:51 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:90249cede2082d3aca1db98135b1ab6e429caf1bbf08b4fa8bccdabcafd0925c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27570563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c578189226a60b3bda679cb5b90bde0c4f7744d0f14b14b8d36142d77e5d57c`

```dockerfile
```

-	Layers:
	-	`sha256:d75e6f47c4ab5594fbea0ec4966288fd99af3dd31e0e15bc514e31ce7c4a43ca`  
		Last Modified: Mon, 09 Jun 2025 22:19:28 GMT  
		Size: 27.6 MB (27556755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa8fdd93e74bccd7e121aacd19ef9d4f55868eff3f212e02c656d6ece48bd74`  
		Last Modified: Mon, 09 Jun 2025 22:19:29 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json
