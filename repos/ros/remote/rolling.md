## `ros:rolling`

```console
$ docker pull ros@sha256:4c9583d3a5d19f075f0a52f72133ebc6a026da83da53169f4a956965b639ba14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:1569a90380536a8a55416203fc87501a40cc5686123ae1be1c7b9f66791d5983
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299750562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc58e01c5bb3f94e5a3c6565881b0e2f7d83691e89defb0484cfd8afd346a68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 22:51:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:51:34 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Mon, 17 Jun 2024 22:51:34 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 17 Jun 2024 22:51:34 GMT
ENV LC_ALL=C.UTF-8
# Mon, 17 Jun 2024 22:59:04 GMT
ENV ROS_DISTRO=rolling
# Mon, 17 Jun 2024 22:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:59:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Mon, 17 Jun 2024 22:59:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 17 Jun 2024 22:59:49 GMT
CMD ["bash"]
# Mon, 17 Jun 2024 23:00:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:00:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 17 Jun 2024 23:00:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 17 Jun 2024 23:00:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d74b73e18f4cfe583d2011834d4f58029ed8c6f75ec1ac223c14319e7fc98a`  
		Last Modified: Mon, 17 Jun 2024 23:02:51 GMT  
		Size: 682.0 KB (681986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0721768f53735ff5e23a4ed7d65da4b64feea90d1f7023f1880f1ed9788578`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 3.8 MB (3755150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6f743ff208ecaf33d7e919ef8874415a12085f64e2627692ca96f8de537e6b`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f5e306aee3e879b7e6c6f517d4884732af61361b421de13bccb3165b286e0`  
		Last Modified: Mon, 17 Jun 2024 23:02:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bf4a81719799814110e9f58b3944ea90c1033a2274eab4e6624992c9f09a`  
		Last Modified: Mon, 17 Jun 2024 23:04:52 GMT  
		Size: 122.4 MB (122447596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cc489dc7cb1f7d20b13283e4b7586c6fe6955dcd75de71f41fb9d4e839d2ef`  
		Last Modified: Mon, 17 Jun 2024 23:04:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126a1d525e956c943a665be6a1bdf2bd1c748cb8a6959056e416b5b858b4f2dc`  
		Last Modified: Mon, 17 Jun 2024 23:05:16 GMT  
		Size: 114.3 MB (114314070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dae707d6964653e32e5684b13a14702cfd58eb44815e4409bee401b4e94f77`  
		Last Modified: Mon, 17 Jun 2024 23:05:01 GMT  
		Size: 313.8 KB (313847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b5327b73417c56e1fd5f8a00a275431abffe89465447f184ec4399a924c693`  
		Last Modified: Mon, 17 Jun 2024 23:05:00 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe718ce59110b6c800a1a2ca943b53eaf075e1e58706b121dff1445fd9d00ef`  
		Last Modified: Mon, 17 Jun 2024 23:05:04 GMT  
		Size: 27.7 MB (27666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b3629b8ac343fec82ab34bdc012524b9511e1e196b7462730fc5b004b76cca46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289897896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1849614724cd139a7faf4d210dc57321d0d2b243b7225b34b617987364d58c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:46:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:46:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:46:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4662d32b5079aa867b80b3da7b6aeff46fe9e17b6fe2259eb511f34086c06b`  
		Last Modified: Wed, 05 Jun 2024 05:57:42 GMT  
		Size: 111.2 MB (111160874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed15ebbe5e1e631506250b6c996ae37c7ba07d31ab8d1319367c8c5e46d97a`  
		Last Modified: Wed, 05 Jun 2024 05:57:30 GMT  
		Size: 311.9 KB (311946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ea445888bf5410c54c8096c7c8479ddbf15fcc0cf7cb3f86625b4c08264bd`  
		Last Modified: Wed, 05 Jun 2024 05:57:29 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c1854b7a8c4003cdbef2894a590e165775f3bbceaf4e101c38f11718d434e`  
		Last Modified: Wed, 05 Jun 2024 05:57:34 GMT  
		Size: 26.8 MB (26812168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
