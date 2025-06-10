## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:32370c500818eaefb8491d7d85e9f415541b7f4bfec8afc59c4240653e7a77e4
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
		Last Modified: Tue, 10 Jun 2025 00:01:06 GMT  
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
$ docker pull ros@sha256:d7efbaa115a4a825bdc1f90869df8ad35ed3e3eb6b6b3643abb8f877136b66ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.3 MB (730298178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995d91d47349518216523bccdc7d0593305ee53562e721467a4787f15188b2a5`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:72144390a2a542ff23fda8fe3461654816cd91594878a1029d7197a649333a54`  
		Last Modified: Tue, 10 Jun 2025 11:55:46 GMT  
		Size: 437.5 MB (437506317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:fa86167eab0b7a9df620f6ef2ae3adcc284d87fefda29b22f0b14c8940747b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52464673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf5a208671fc459661a3f7858f76e166585f4aa250083d11fb19efbd8aa0454`

```dockerfile
```

-	Layers:
	-	`sha256:2dfc448a893133e4d2df58110950ed24036fddbb6f2a4c42123159f7515c966b`  
		Last Modified: Tue, 10 Jun 2025 01:18:48 GMT  
		Size: 52.5 MB (52455239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f505f527d26f2ef883856404c4045e61e0d29db33a171e94e5a69e628ac3c1`  
		Last Modified: Tue, 10 Jun 2025 01:18:49 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fa8a2054fdbbe5d74054681e5ab88ea2b1b02cf1f68feb71083c90ae88c6ef6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.0 MB (906986380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c7e5698db4a1cf6a46a76f19ff551acb51b66fb799bcd06289be0b11caa471`
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8965a1cbf95bb1c0a0fdbf2e84e831095239fa093c88df83b4813cd360bf61d`  
		Last Modified: Mon, 09 Jun 2025 23:22:48 GMT  
		Size: 44.0 MB (44025805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c9101971e6e544417587498e848cd906a5072fe880df3a870c6735f518bf5`  
		Last Modified: Mon, 09 Jun 2025 22:23:05 GMT  
		Size: 348.0 KB (348026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679ea0da59a1556edaba85a9966e6296db829e778f72481bfbe4a9859f6c4c2`  
		Last Modified: Mon, 09 Jun 2025 22:23:09 GMT  
		Size: 954.7 KB (954730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e716aef459894de40b20955ac0ac75e343d47ba24a293a310e828c3a4c8ce70`  
		Last Modified: Tue, 10 Jun 2025 04:58:23 GMT  
		Size: 463.3 MB (463259314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1a32d960102ccb3b00fc1a03f651e635b5f82971954ab338cf059ff923abb9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53583004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b1d0f1a004945510423272c396a6d608060d5bd86220b839656a4ea3399ad7`

```dockerfile
```

-	Layers:
	-	`sha256:493356d0c2543bdcbb8784bda13e7e0ca5b279ff3975d2c6ddf7361dd1bf58a4`  
		Last Modified: Tue, 10 Jun 2025 01:19:47 GMT  
		Size: 53.6 MB (53573551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323c13b9db44e4e32b2cacd68646ca58d74255b872286957e71b6698160012e8`  
		Last Modified: Tue, 10 Jun 2025 01:19:48 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.in-toto+json
