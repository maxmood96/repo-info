## `ros:melodic-robot`

```console
$ docker pull ros@sha256:08a0e085c9ddc19f9be82852be33088a860e2c85aab5b019f23198a243f47e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:23456582011b89ff5a83e718b36bbcc9bb96f689f430f702de455580c981dfa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.8 MB (448835699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b9d9052510148a9741a3d24dba79d85bfabca8b35f04cdfde4e4cdd9aa00c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 May 2023 09:41:51 GMT
ARG RELEASE
# Fri, 12 May 2023 09:41:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:41:52 GMT
ADD file:47682dd3869ca8e57ceb15f69a6ac7c9048d4d42c7a99a976e597cf072423c12 in / 
# Fri, 12 May 2023 09:41:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:04:56 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:05:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:05:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 16 May 2023 01:05:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 16 May 2023 01:05:05 GMT
ENV LANG=C.UTF-8
# Tue, 16 May 2023 01:05:05 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 May 2023 01:05:05 GMT
ENV ROS_DISTRO=melodic
# Tue, 16 May 2023 01:08:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:08:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 16 May 2023 01:08:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 May 2023 01:08:45 GMT
CMD ["bash"]
# Tue, 16 May 2023 01:09:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:09:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 May 2023 01:10:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 01:11:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c67806d7e72dd941e600bad2eabe920a17ba1852b325b63900c819ffeae646fb`  
		Last Modified: Tue, 16 May 2023 01:01:48 GMT  
		Size: 26.7 MB (26715509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8112c7660661f5d395aac99b0d2403ccaaf47cfce01b40167688a866847d540`  
		Last Modified: Tue, 16 May 2023 01:17:48 GMT  
		Size: 819.1 KB (819098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64664c88569b54e7b2cace7a7eff36f63ca10a75b05e5c1ddceb69bbff1d387b`  
		Last Modified: Tue, 16 May 2023 01:17:47 GMT  
		Size: 4.9 MB (4878519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20548c67c76407d9f268011684621401f1bb204c67b556072a06759d86b2cd82`  
		Last Modified: Tue, 16 May 2023 01:17:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b96bc2cae0fba817ecce5d15aafad4eee15610dfe2178708ed47f732f7f71bd`  
		Last Modified: Tue, 16 May 2023 01:17:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60000963f8bb247e6b22511e73ce54d4b3fefb24047ab49992acd24f8272aab5`  
		Last Modified: Tue, 16 May 2023 01:18:20 GMT  
		Size: 259.6 MB (259592143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af96a47a2aa7f522fcdf38f50ca1ff4abda4c7efd140a1d960f59b90f47d7788`  
		Last Modified: Tue, 16 May 2023 01:17:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b12ba5acbea014d663262f916b8adc37a9271199290d917abd458538df9cb70`  
		Last Modified: Tue, 16 May 2023 01:18:38 GMT  
		Size: 70.5 MB (70459679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41bbf0250a9904f7b67e9257aa660ab936db8911b99cd58d9350b109b920e31`  
		Last Modified: Tue, 16 May 2023 01:18:29 GMT  
		Size: 282.3 KB (282294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70f25d5aeddde8c1ec7ab0e2e9b51e8c30c5e7d69ad7cb00cb679682e3a47b3`  
		Last Modified: Tue, 16 May 2023 01:18:40 GMT  
		Size: 75.0 MB (75000304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63750a48b8c413627810e36f792a3f745a8f70ef9615e698c1486f634756d35`  
		Last Modified: Tue, 16 May 2023 01:18:52 GMT  
		Size: 11.1 MB (11086307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:289b5773ca6f48c9b33f6e78d3927d5f8ce82e30caa4f1796bedace63ec7062c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396169033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fe266a72b185cf1431c8a4d377037aaa4b7bbcbe8656658935c11696fd107d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:11:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:11:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:11:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Mar 2023 03:11:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 03:11:55 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 03:11:55 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 03:11:55 GMT
ENV ROS_DISTRO=melodic
# Thu, 16 Mar 2023 03:16:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:16:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 16 Mar 2023 03:16:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 03:16:15 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 03:16:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:17:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 03:18:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:19:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fb42489e9f507aa183ef669baec25f94b8c4c22159a4ccc23a1977cedd0d1fa`  
		Last Modified: Thu, 16 Mar 2023 03:39:03 GMT  
		Size: 22.3 MB (22305374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fca3839c8bd4903e2ee5f523935fb729f15724615fd9f77ce0d6cc2adbfa6`  
		Last Modified: Thu, 16 Mar 2023 03:39:00 GMT  
		Size: 820.1 KB (820097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3f218bb6743682d83611cfd2ae16145e67489129eccf76d1236a70b3a5bcac`  
		Last Modified: Thu, 16 Mar 2023 03:38:59 GMT  
		Size: 4.1 MB (4090687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1bf44a1167e1c920f67efd944ec51807eb500e2fea8c0103e3a0d46a52fc32`  
		Last Modified: Thu, 16 Mar 2023 03:38:58 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00ed9b280b6ac98a36e5f3f6a1cdeba5961c20493eddf18a97a0b9db954fa6e`  
		Last Modified: Thu, 16 Mar 2023 03:38:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cea9e95a56ecce8cbb02ffdcdcb3059f16577e473b546648bf64fd56a319a1b`  
		Last Modified: Thu, 16 Mar 2023 03:39:32 GMT  
		Size: 239.0 MB (239044585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9735bdd7bdcf6fcc5f9450057e43d66daabf09facf6269f79ba9fabe328adba`  
		Last Modified: Thu, 16 Mar 2023 03:38:58 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dac314ffbb6434ef884f3647e224f3b30f1018f02b797077c272e6e18bf8339`  
		Last Modified: Thu, 16 Mar 2023 03:39:49 GMT  
		Size: 54.7 MB (54734178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b54e23bfe2054492ace7dfe9733463a7ec3acdb0fde54945898eb6183e0dc9`  
		Last Modified: Thu, 16 Mar 2023 03:39:42 GMT  
		Size: 297.9 KB (297866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbec2cdeae69a7086e37719ef96fc503992f0d4b2d60728205ec438444deda1b`  
		Last Modified: Thu, 16 Mar 2023 03:39:53 GMT  
		Size: 64.8 MB (64750962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7634457b9c881ce425d9d01bdff94fd83b012daa031b020cabb98af51b26e5ef`  
		Last Modified: Thu, 16 Mar 2023 03:40:09 GMT  
		Size: 10.1 MB (10123434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c0a0a8a25dc822ea48b40c45d74b267ddf4dbe22b8accc9fd66bb146c34eb974
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422923396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916440a18deb3d20ae03381c36c2693e05070e1e703b8b2f66e74168127dce44`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:56:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:56:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:56:47 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Mar 2023 02:56:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 02:56:48 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 02:56:48 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 02:56:48 GMT
ENV ROS_DISTRO=melodic
# Thu, 16 Mar 2023 03:00:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:00:50 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 16 Mar 2023 03:00:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 03:00:50 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 03:01:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:01:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 03:03:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:03:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c21a0233221a76e66b6c10d2445f591bd28eb0773e6cb539474d6dca9ea0b594`  
		Last Modified: Sun, 12 Mar 2023 07:27:31 GMT  
		Size: 23.7 MB (23734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d56daf02ac303e7c230365644aca63ed850ebf40d29e81a5814308c13562239`  
		Last Modified: Thu, 16 Mar 2023 03:44:18 GMT  
		Size: 819.9 KB (819945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b83e85404464664e50669adc31927b351faa0e1bf21c647f66d7f27782fdb61`  
		Last Modified: Thu, 16 Mar 2023 03:44:16 GMT  
		Size: 4.5 MB (4462823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a184771f70aafd7d78ff51d90244556b28011bac2d29106066a25ba9e96dc089`  
		Last Modified: Thu, 16 Mar 2023 03:44:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9074f6bcd0b3bae9f4c581397d152b553279dd7184769c00f73e89f9ae5a2d1a`  
		Last Modified: Thu, 16 Mar 2023 03:44:15 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4bc60dd1e1c3f4aaade0438967ef0ad4f929678ad0595f68c97aa6802e3508`  
		Last Modified: Thu, 16 Mar 2023 03:44:48 GMT  
		Size: 252.5 MB (252534995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1f4fb4d9a35efa338820eac3e26a8095ab5dee1791a6486ba31cb576260bca`  
		Last Modified: Thu, 16 Mar 2023 03:44:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fde270ea5c1652055c01f32fcccb425820da092a3595a17a1b46328120b1aff`  
		Last Modified: Thu, 16 Mar 2023 03:45:04 GMT  
		Size: 63.1 MB (63094293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b8e237fc97a182dc544c752d16ac1ce2e83c4d08538a122d43f03c33340a7e`  
		Last Modified: Thu, 16 Mar 2023 03:44:57 GMT  
		Size: 297.9 KB (297879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab7b64ecca2bb014b31a49a16d2dcd2856db7487d4967731df87dcc2c2b990d`  
		Last Modified: Thu, 16 Mar 2023 03:45:07 GMT  
		Size: 67.2 MB (67235800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1391b68cbd182ee0c5bb36c626732e1b8182df4ec25d7ad2c636d92cd8428df`  
		Last Modified: Thu, 16 Mar 2023 03:45:21 GMT  
		Size: 10.7 MB (10741104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
