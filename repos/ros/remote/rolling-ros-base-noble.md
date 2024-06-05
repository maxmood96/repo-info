## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:5f04661331f7f5b8436131e062823706575533b394b56891bd9666ca5d878c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:6c30cecf18841ec4493fc206d8c63906980801503e2a88911db49035b3a70f64
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299756307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd504a35a414a0fff6a3a3cfdb872ff6eb158c969708d6d01da21b59681c2a9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:21:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:21:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:21:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2662c619c85291f1c5373990ce67dd656732b1713e6a2e530dc4c7e919aa4d`  
		Last Modified: Wed, 05 Jun 2024 06:33:14 GMT  
		Size: 114.3 MB (114315856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46788892d21f6a27a3146a33bf193d36045bf80d7ccf46b31b7f81aa48ac2dd`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 311.9 KB (311937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599c02e1aaa8a27726480aeda8f420f4d510c18c033236710719593a3a8683d2`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af64f7b4bca9f0f94faee8b3e77e6898cede65a278230955cd65948cd5998b`  
		Last Modified: Wed, 05 Jun 2024 06:33:03 GMT  
		Size: 27.7 MB (27665965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

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
