## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:88b1c931214b198949a26df1b977c2b3ed7c4f1b4494e9cdb2b65e52aa3cef5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:9d0a234e8968e8c2fb6a372998640e8649f05a75aaa4587b9fd23e39c696d575
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.8 MB (954826606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa074b9ea856bbed471f1ba13bf6dbf77e569233c4fb365eb5c83e77db703366`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:56:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:56:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:56:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:57:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:06:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4bc00ea17676350d16ec75b469e205e9415ebee3ab68473e595a6ad96c1cb0`  
		Last Modified: Wed, 05 Jun 2024 06:26:34 GMT  
		Size: 98.2 MB (98153054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb06de83a3792c1712e62dc67e451ebac0861c13efe8e5c7868db4005e73797`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 324.7 KB (324740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cafd9f34a66cf722480d56c08a90d31c78896016d7a81945712ba94e121d26`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9200aa16c06bb4b2ff18680d36f42006535265b5ac135148f7d7b907d93e29ac`  
		Last Modified: Wed, 05 Jun 2024 06:26:25 GMT  
		Size: 22.8 MB (22824392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152771a7549d5b98f375618ab9ffa808eb174baef69ee606887c9e0cdd336ae8`  
		Last Modified: Wed, 05 Jun 2024 06:28:12 GMT  
		Size: 691.5 MB (691527950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7aca638db11345349c18296c5585f4172c050026bc9b7d06dc7ec7087374e6f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.4 MB (915363636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f111da1596b1936d3d6fd8a6862abe1c44c8c6248f2767f4aa6237156c4359e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:17:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:17:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:17:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:18:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb4ccb2bbb7400a6f6044af60a4d3dcf2663a0871f005456042c23a61df3519`  
		Last Modified: Wed, 05 Jun 2024 05:51:08 GMT  
		Size: 95.7 MB (95713365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055b2579f4a3a4150c53593f639d9b51bd4acae4c72a1f06c1f66bc4b35f1fcd`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 324.7 KB (324739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9743a79bf3af1d25fa2d5b114ba3d6a81f02966c6ead80289131d3de9e8452`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583dfc7042595ae5838b88a40d5feb0217901dde3b5ddac77e3b23c3c737573`  
		Last Modified: Wed, 05 Jun 2024 05:51:01 GMT  
		Size: 22.2 MB (22236354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e980cefc24b629cab20b19ac33c713392ca4ff4e769fd68864936c072e2c1c6`  
		Last Modified: Wed, 05 Jun 2024 05:52:40 GMT  
		Size: 659.4 MB (659425966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
