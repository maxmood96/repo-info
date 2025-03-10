## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:8850899764de97dd0495d8bcea74a0d564560fe3ed652334aa0eeffbb61bc73e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:40ec4948f690202ffd4023159f354c56a70a29c8f3c2735f80b0414e53d86f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307000982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9303e688d675c01c68bac199b8903c0cdee5cf4679e570071319d69c5024bd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeea575c80af2e65fe04975f11edd4e921b04d3147a50068c5a5969bee6bafb3`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 680.3 KB (680324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4025c1e6627435e8c8b5d54ace9042ffc9abb779f9949a39e0c91708aac130`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 3.6 MB (3561468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199dff8e77acdbc33a1bde2acbdc1481733c8d72a039fe2915eb196af9159582`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b349db87fd4d4f170f5c76740209f134b55e13f869500cb7f89b880c0b205114`  
		Last Modified: Mon, 10 Mar 2025 18:13:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260dd0d00b496f4a4ee25f954e0fe78b05b9fa66549124673f930393e7aad709`  
		Last Modified: Mon, 10 Mar 2025 18:13:41 GMT  
		Size: 132.1 MB (132130563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe62c3fa6ae8df69810304838608966ed5075f03e07c7afa99eb32abebba528`  
		Last Modified: Mon, 10 Mar 2025 18:13:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48083a3093eb3741c5bebac5693dc02f455e4836d4735aa5691b4b7061665784`  
		Last Modified: Mon, 10 Mar 2025 19:11:55 GMT  
		Size: 112.6 MB (112551408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e150bfd5bb1e9ec2d0529236729c26b01437c7c53fb5f23c58b73b33148a436`  
		Last Modified: Mon, 10 Mar 2025 19:11:54 GMT  
		Size: 354.1 KB (354070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eed3d6e64faaf7b73c937a90a2ab822ab1ba7b3307f5d384fa434b120c8a0f`  
		Last Modified: Mon, 10 Mar 2025 19:11:54 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbbfc65a8942111f26e9dce5bb03c2e58c5a1f4ad990502b67e100a48835d`  
		Last Modified: Mon, 10 Mar 2025 19:11:54 GMT  
		Size: 28.0 MB (27963960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:914a5506bddff794c5ab87dc588a21e74cf4e23229ef1c07e12ad1aa65cdf31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23852862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49e93dd442d40b2cbd3ea10ee16daebbda5450e2095f496e49ccb5813ee8dea`

```dockerfile
```

-	Layers:
	-	`sha256:6246beee4fce5281d8aab40b7279ac53539db9b11a043ec6def5a5a31e618680`  
		Last Modified: Mon, 10 Mar 2025 19:11:54 GMT  
		Size: 23.8 MB (23835434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44b5076a9a9234771f1b2147db19acfab633544f337afed22231cbdb73be736`  
		Last Modified: Mon, 10 Mar 2025 19:11:54 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d256bde738393b24d40882d632f0a03854f7fee8e93427ca0ea102bce17fddd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294116584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2babb7c65162df7b88b6ea0439b4a2c099cb29a2d896bfdbf7b8580b7e4d0b6a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8d831e1a4059e2f42ef51fb31bbc35c38063fdc8eccaa465d49821f79dd0a5aa`  
		Last Modified: Mon, 10 Mar 2025 18:20:36 GMT  
		Size: 125.6 MB (125620540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a9d5a529cd232eba1f6392b838c02adaeaa7a2e4965c850a645b0fd30779e0`  
		Last Modified: Mon, 10 Mar 2025 18:20:33 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95cd021138d293a95e1efb05e7151fdb92ba15e342e95c3f967053ea9d344d`  
		Last Modified: Mon, 10 Mar 2025 19:20:44 GMT  
		Size: 107.9 MB (107946403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064f4d52c2edc9c08866ae50fcbbb32034c3f128b5b08290f6708bf281df33eb`  
		Last Modified: Mon, 10 Mar 2025 19:20:41 GMT  
		Size: 354.1 KB (354071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543e0e820e45d15b9790572f0cbb4f75877868440e4356c77e3b8f764f11a26`  
		Last Modified: Mon, 10 Mar 2025 19:20:41 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3025a4c0e9527e73815bb3e033f887f1ea6b8cd397368161af1ab7b535b964e`  
		Last Modified: Mon, 10 Mar 2025 19:20:42 GMT  
		Size: 27.1 MB (27056165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d7ecf4e927b0e99ab7585c3c6c30bf04f8086226aae68c84d46ce9dcc6cb7fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23875568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce70114c54d1e8881f61cb778aaaf2b91ecafd3f5733868f7efad67641ff67`

```dockerfile
```

-	Layers:
	-	`sha256:8b692f5f51c2a0afb20bd20417a2dcfd91a3cd2e28a0c7d854dd7893f5327569`  
		Last Modified: Mon, 10 Mar 2025 19:20:42 GMT  
		Size: 23.9 MB (23857990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19f3ca432e47eea1a1fcfa81cda5fb8d8dac98e4058b480c6bc3e559983aa85`  
		Last Modified: Mon, 10 Mar 2025 19:20:41 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json
