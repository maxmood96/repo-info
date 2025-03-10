## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:f93cb3d086c3dc548c11e9a36ea572d10f3f1e09d68d2dd8d9fcc8404258219b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:668dc7034dbe9ae357f2f1f9729593dfbd859e75cc354d6c81abd6794827e8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.6 MB (673553950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ff1f581c7b931a923c3f42eef26a9825b79495458c8ab03af4e5f4bc612e83`
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
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:26c8e3939065799f8fdb726d99a9e1a9e8a5a3cdc322ceb2968163a363383217`  
		Last Modified: Mon, 10 Mar 2025 20:12:19 GMT  
		Size: 366.5 MB (366499871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:ad9b947100b57601f575e9e26a96f8116a1d32f69c2b39657e364664e81af629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42119978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd33fd4ba5c58d26a344d6e549c428779524ae2ee6dedd6739864ed3dc3ce86`

```dockerfile
```

-	Layers:
	-	`sha256:63414dc9b5b596aa1eb8efc3151a6794dae27522cc583a7a0fcdb8bb6868da5a`  
		Last Modified: Mon, 10 Mar 2025 20:12:15 GMT  
		Size: 42.1 MB (42110268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822eacfa59adf67b13f776f45f495fbc97be91e59593f75777f8dc86c5dc4674`  
		Last Modified: Mon, 10 Mar 2025 20:12:14 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:513bd218619c119495b1fcce5492f386f0682201996e7393d8bcedca30375e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.2 MB (576246050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72bb8edd0d2a8f4bb5e921bb7bbf98f4af979e2267575bea4a9af83b9ab547c`
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
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4ccf49c0175b5f99e9175cfc7527624ecc5d3482279ebac616c6abe404e220c3`  
		Last Modified: Mon, 10 Mar 2025 20:31:45 GMT  
		Size: 282.0 MB (282030404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:51c768f23fb5b6395809d7e493ee9553237dbe743324c48e2aed982d728fd483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42198532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ed227686c0cee77d229a94071bacc0141b6a4f5b24f3bbe40dd6dd8058938b`

```dockerfile
```

-	Layers:
	-	`sha256:9a23e993c71cc1fcb5c73d3dfc0d96a2b5ddafe923be525c20a98e8070574eea`  
		Last Modified: Mon, 10 Mar 2025 20:31:41 GMT  
		Size: 42.2 MB (42188742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6db7221d71869234341cecf4fc8d3abc3e7db23da1388e27be6e8f38b6a701`  
		Last Modified: Mon, 10 Mar 2025 20:31:39 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
