## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:8010f4d02097469cf14b0cd3835c2693cb708b52a7ee5bffca4e66161db3b226
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
$ docker pull ros@sha256:ef5fdebeaa881604208c067f96d42b61331825309e559c093e24e9e89c7d3d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.0 MB (953023137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d1e228d78fdb8d64b885b3a15a6b05732187206079883723b81f3dc87f7eb7`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:281e59625cef2e9db605bf16166bd89c3dd232e78ed0dcdcd563b7893aa85ba3`  
		Last Modified: Mon, 09 Jun 2025 21:47:27 GMT  
		Size: 492.8 MB (492750345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:db8251d53d5c9539ee64f406ca69c5cedbe3d894efc9bff3f792e4ef5057ca22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d22f8356ce708dcea7b039482148d9135ea7974309d628290e8b0f5b4621f3`

```dockerfile
```

-	Layers:
	-	`sha256:dc3773e4d74b9393c411008916dc91aa2d7d6dd3a4918c7e6872b66579e98878`  
		Last Modified: Mon, 09 Jun 2025 22:18:39 GMT  
		Size: 53.7 MB (53730591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d0934d33825d3fea55238e02051fbdebb494b9638955248d524a9d29405ba3`  
		Last Modified: Mon, 09 Jun 2025 22:18:40 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:e369bf14da3d93f9be6ad671f4681b2b488f5f0056278a79723286d2ed2d239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.2 MB (725206547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424465548bb231bcb31875ce6e38c94dcfbef64f744da6db98b9817377cb28ce`
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
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Sun, 18 May 2025 18:45:39 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22052e0f4af1fa1026f671cc3091c7c92fc31d9da9086335d89ec24f1c013474`  
		Last Modified: Wed, 04 Jun 2025 10:52:21 GMT  
		Size: 496.9 MB (496872660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1fbf1d0fe5a65fae05c1ee79bb1d59394c0124d36e81e95300cf6b280254b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51466276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cf80209972ecf4daf80b36ce0363eab1a75c5f046a99fe0518fb41a37470a9`

```dockerfile
```

-	Layers:
	-	`sha256:350b1e9cb0d117c5c2ba18f2ba57f6d6ba9d0e72c5c2e793bad9e8f84b8e72e7`  
		Last Modified: Mon, 09 Jun 2025 22:20:07 GMT  
		Size: 51.5 MB (51456843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98581e073cf87a2627f231fe098612edf517b2e20ad820129c446e3afc1f74fb`  
		Last Modified: Mon, 09 Jun 2025 22:20:09 GMT  
		Size: 9.4 KB (9433 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cfcdafb6ae6c5e1c85e054202ee9571e286b88fe215dcad96e2920cf7f3bf7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.0 MB (902042260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e17c4f0db3b8edd25decb5455db77a82b8508882492faacbd0032b51909045e`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8498e3ff194372ace8e0d6adab098ede6183b5fc569779a0da961fce617ec1aa`  
		Last Modified: Fri, 09 May 2025 00:33:55 GMT  
		Size: 651.8 MB (651806563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:e53bdc49d292ca610d7c65ea39ca39d81e6e3db349619076484eb33e90501621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52577752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99522e5bf9afe7bc5271fb30273274c04615e345ca72b41c861478851d82d7b`

```dockerfile
```

-	Layers:
	-	`sha256:0fab2f8af0fefd387cd98b46db31acb42237fcb69539a5c90c9b6a494e6789e4`  
		Last Modified: Mon, 09 Jun 2025 22:21:29 GMT  
		Size: 52.6 MB (52568298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbb944e96c1e06942dbdd8eb1150a055a3c839522f5cd6454f7096b5409e75b`  
		Last Modified: Mon, 09 Jun 2025 22:21:30 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.in-toto+json
