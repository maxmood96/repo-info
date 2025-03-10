## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:ec8fafff40b01e490c6c2af0e3d2b4711afc1af00a6d4862c3080b8e8b0f746f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:3692f5c1524565e2e646d6dfe6a9efc4c21f1a382c99ba462ab39706f6fd200b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307054079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7c26d6ce3e47e66215cc5039602eeb64e43ee8083fe639f3801d4e9dae0836`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e8d3973a6431bf06ae2429fe6043d68076f680d6b9e838871fea0dda80d8a`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 680.3 KB (680326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623b736b410baa5a5818f62b08b2007dd9842030d9973045f5f90da7ee66c55`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 3.6 MB (3561526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2b2c3a23f9902ed270bb51f69b99a73d85d366f06f5a32a28256af861b69d0`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4fa6db600a3081b7a0db34679e3c98dc51777a5ba600aafc114cd49bf17f75`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ad0c45362760291479652f2f15e1f417e3217c27d636ba16b628a3a019d7da`  
		Last Modified: Mon, 10 Mar 2025 18:13:42 GMT  
		Size: 132.2 MB (132193590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d9ebb38bcee87c07ca2ae9f32b3c83fd24b46271f5b8317239ea3c4ec23240`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d161ec889ba0da58e9035bf804942012ec097d5af52fc85bcd4e767d865325`  
		Last Modified: Mon, 10 Mar 2025 19:11:50 GMT  
		Size: 112.6 MB (112554112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89c39128f93c61884a7f3f9346c039943ed9d9b6a2c46d1a0c2f5b4ce5a2433`  
		Last Modified: Mon, 10 Mar 2025 19:11:48 GMT  
		Size: 336.7 KB (336675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd28208977f9090ecc95afc4d45bb631bd128d20efda612a1703eb33f0863e2`  
		Last Modified: Mon, 10 Mar 2025 19:11:48 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d950d8c025a26902de46aad43f0bb4425140694f3edb0daf8fe523a0e2e790`  
		Last Modified: Mon, 10 Mar 2025 19:11:48 GMT  
		Size: 28.0 MB (27968660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:5d42fb24bf78d8d808a93931c16ab5bd5dcdec95ce0c4dcb1546476f8ca02741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23811612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b989442ddd4f4f8e21e6bad5c45dd2630abc5e96b8f7f9828d0f06208486d822`

```dockerfile
```

-	Layers:
	-	`sha256:5b7d9e4cfd06ccf48f6204b9ed735e4da86b623d9c6fc7a2d19779f3b45f7d19`  
		Last Modified: Mon, 10 Mar 2025 19:11:48 GMT  
		Size: 23.8 MB (23794439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4adc89072cf3af3e18f66591f2f801fd5759fcd33f8fe13802bd0e9418936c93`  
		Last Modified: Mon, 10 Mar 2025 19:11:48 GMT  
		Size: 17.2 KB (17173 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c3965d90146b60f277d6b929897b6dd2a120fe3432aa15dec3dc799f863f1d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.2 MB (294215646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37378e7abb230880dd20558f74b1dd28d7a55e6c15092db0f44496dd2499538c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab5679ebed679dd3df1e6843c6b8f39fa8e45a051661cbb57e6e0b119a3cfb3`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 680.6 KB (680594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f185985e6550bd84d688dd66ba0a96385e0d1ad37d682fe238a7a01c0d8901`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 3.6 MB (3560303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc221ca73075ddc99f91aee5566348bad0f2cd626764c842b72eb0aab3c0115`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb1b676ccfe7049a341da1d054040b9421e7c6f7efced7ab1bf2aca22d5831`  
		Last Modified: Mon, 10 Mar 2025 18:18:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b44689c8c5f80874ceb853f0ed27781711765c4a547ae76561a1dd01f51e12`  
		Last Modified: Mon, 10 Mar 2025 18:19:01 GMT  
		Size: 125.7 MB (125738121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef8e47468d6afb7fb6cdfa6a743dc16aebbc27006635613a6083459f600f817`  
		Last Modified: Mon, 10 Mar 2025 18:18:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c8ee1b225c7641ae06b9b1a4257c64ce1962e2d0ede51f7f24e293d961ad32`  
		Last Modified: Mon, 10 Mar 2025 19:23:42 GMT  
		Size: 107.9 MB (107947875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe112d87c57e9e1a35952bff43c440e479425cbb2072bb30d46ec5e48ef1d5ed`  
		Last Modified: Mon, 10 Mar 2025 19:23:38 GMT  
		Size: 336.7 KB (336664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a8f72395d7a538089f03dda01a55179ebe826230899d893a424d7c1f459b2d`  
		Last Modified: Mon, 10 Mar 2025 19:23:38 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdaad10511d6e7fe76c649ec4b3289a2d957beee577fb92766e4a0f76d2f91`  
		Last Modified: Mon, 10 Mar 2025 19:23:40 GMT  
		Size: 27.1 MB (27053598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:41c291b78d01291b4e074ca310116351c914b1d41ed7e58010f2deab692910f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23952459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab099b990dcad98c19791832a0cef07c115c7838ac69f0d5b2fb182a1ffb3f9`

```dockerfile
```

-	Layers:
	-	`sha256:e86609d1e355ab10bd6d820fd2a116d172b4a98bb7db38f63431c84e6fa4c698`  
		Last Modified: Mon, 10 Mar 2025 19:23:39 GMT  
		Size: 23.9 MB (23935149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2e89718c8f5120e53472caff714fc37ef0340583427ef3d03926d65b0fc6d4`  
		Last Modified: Mon, 10 Mar 2025 19:23:38 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json
