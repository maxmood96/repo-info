## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:eb0f0b232afea34865b29798f09433bff410dd5b28b0a3dfccb4005be34d96f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:ba314e83e1140e38b730ded90897ff4abf9920a365aa66f67bf4442263ae7407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212362926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c8e3327cb9948f69b0783b7a885aed24c0a9895e05b7e7b560ef3a8d1e4d64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:8a5ac73d28a505b16a86f3e7185d0c1434c7dbf19ba486945d55d589316b5333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188011580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67480a9eb0025f587eae298a084f3ebb439aa33830002554ff9936d59bdc8b7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f2439b922cac680e8c6cefcb54a18fa0c06efa19f290e0c7106c287944c9b1b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205346052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f02c719ef94496b7e6b92b6f5e381407904a4ca59c2e0b0fd8efc218cea02ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
