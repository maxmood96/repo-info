## `ros:melodic-robot`

```console
$ docker pull ros@sha256:268be86daad36e728dea7638323df25ebc728d42526acd2fbb3385cb46a4afda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:abf9624b8719c6fd836a5c0803b77b5434fee248a7097dff4753e23ab8a686c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448488064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522a284b486243807f15fe56d2723bfd034c2b99de4104f787840cc842ff2f1a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:58:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:58:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:58:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 00:58:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 00:58:46 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 00:58:46 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 00:58:46 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 01:02:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:02:27 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 07 Jun 2022 01:02:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 01:02:27 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 01:03:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:03:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 01:04:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 01:05:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5177ec8aa0752191cb3a72f43a3a9259dcaef6c03b51ff91fd9c0fb0f2e45c2`  
		Last Modified: Tue, 07 Jun 2022 01:45:00 GMT  
		Size: 839.2 KB (839230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cd145b316c1fb7c938c3e1e06f5ce778bf9b0051a70db477ca7a8c7c01a026`  
		Last Modified: Tue, 07 Jun 2022 01:44:58 GMT  
		Size: 4.9 MB (4875695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598864753f0cbdc3bc5352575f8c0d1b6c501c07d44c5127932ca01c31c875d9`  
		Last Modified: Tue, 07 Jun 2022 01:44:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3485714346b9f0f8a36485f223b93e4f06586b8eae6ae6ec8a66b7e7e75fdc`  
		Last Modified: Tue, 07 Jun 2022 01:44:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab3a5eb67d539589601e0fc081dd6b4c37895928b80ca7a3091b0ce46c24005`  
		Last Modified: Tue, 07 Jun 2022 01:45:33 GMT  
		Size: 259.5 MB (259452207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9573725ebd5e712abd6f511e5ab7e0c71c4de8f3b5772bbe4b825f95eb98de`  
		Last Modified: Tue, 07 Jun 2022 01:44:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a68755b20fa638646cbc2cd697f406c0272ad07806d806fad4f3c1fb27824e2`  
		Last Modified: Tue, 07 Jun 2022 01:45:52 GMT  
		Size: 70.2 MB (70246372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aa4ee8bafcc8a148ea13c35a18a93a2916a788e882df1240801a488f2c5ed7`  
		Last Modified: Tue, 07 Jun 2022 01:45:42 GMT  
		Size: 280.9 KB (280922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9246d39f4c75714c673a4472b1a858abc20c63bbae81f24a3e477dfcef7f50e`  
		Last Modified: Tue, 07 Jun 2022 01:45:55 GMT  
		Size: 75.0 MB (74994714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5ffb1f2421f0599334f917713f403ebaea241a7e155f4e6afa5fc492ec43cd`  
		Last Modified: Tue, 07 Jun 2022 01:46:10 GMT  
		Size: 11.1 MB (11085450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:1d14bd9194543ed4a9d9f0dd81dbc60b9e4ceb6ddf151a2e4a2a09cda63e5b6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396027305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063acd2980c8c66d21cb505f4234c799e9f46aa28de7caa2849f8448d946245a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:58:25 GMT
ADD file:9604e3641a386ec134596dd717862c2386c1b90009c0646b1773930f98949d9c in / 
# Fri, 29 Apr 2022 22:58:26 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:28:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:28:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 30 Apr 2022 00:28:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 30 Apr 2022 00:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 30 Apr 2022 00:28:42 GMT
ENV ROS_DISTRO=melodic
# Sat, 30 Apr 2022 00:31:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:31:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 30 Apr 2022 00:31:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 30 Apr 2022 00:31:55 GMT
CMD ["bash"]
# Sat, 30 Apr 2022 00:32:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:33:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 30 Apr 2022 00:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Apr 2022 00:35:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:03ca5b55b2bdc3c68d23c18a88c099e2015c6bdcef6e3c43ca0bfb6aea0b032a`  
		Last Modified: Fri, 29 Apr 2022 23:02:31 GMT  
		Size: 22.3 MB (22300451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ab3231e4fbaccf7df6d1d44ef88608a6c1b716de9810c8e2ad6b7dcc9f5fc`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 840.2 KB (840158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f529e0e8ed7433413f39308a48052c609e82179d4d22b76f62189c616e5fe14`  
		Last Modified: Sat, 30 Apr 2022 00:51:07 GMT  
		Size: 4.1 MB (4086200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59f023c86c2016dd149f7a89f71dc59cb35eeaf64c75eadba638336b28f6abd`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdf654803a8e788e4166c4bf287b5137ec541b313ce50e4d9401f0bd63fc8d`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17f883dcf2090ca188521c82e8ecd78e6182c5c0af353b2dee9a1b0e0c44e`  
		Last Modified: Sat, 30 Apr 2022 00:53:38 GMT  
		Size: 238.9 MB (238937435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc27e0b0ee020522ab3317cb8094bd430e3fb49425c99d1cfafe5284f0562f68`  
		Last Modified: Sat, 30 Apr 2022 00:51:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c89127f2ab55d40e6d39537412903ef429801ea54d6baf3a6439a6bb01692f0`  
		Last Modified: Sat, 30 Apr 2022 00:54:21 GMT  
		Size: 54.7 MB (54710630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108adfc0916db7aeda7a39615caa2cee9b6fbe75cd66aa27a2ac82eaf1e6e9b9`  
		Last Modified: Sat, 30 Apr 2022 00:53:50 GMT  
		Size: 280.0 KB (279967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab1dc1feb0f323edf28a08fb0fcfc3796eb524ac698714b37837180467e312`  
		Last Modified: Sat, 30 Apr 2022 00:54:36 GMT  
		Size: 64.7 MB (64746523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b852a9e6f9b9db1a873f5d26b96fa8e2ec994256c7153e1ef272a96d26c60c`  
		Last Modified: Sat, 30 Apr 2022 00:54:59 GMT  
		Size: 10.1 MB (10123526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ad01fadf44cb9d22fd3187097376609d1432ffab314aa17f56ebeb98cd0fa349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422326280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee6f4bc89ca67e154f17d32c726aa8d469c74cbe7e5e383452ed4271e6f62bc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 05:47:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:47:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:47:47 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 05:47:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 05:47:50 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 05:47:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 05:47:52 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 05:49:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:49:28 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 07 Jun 2022 05:49:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jun 2022 05:49:30 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 05:50:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:50:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jun 2022 05:50:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 05:51:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b57592ad601b709b6d4af02430444d1ce166e53a2c06e41b70d06e27b5ec2d`  
		Last Modified: Tue, 07 Jun 2022 06:15:41 GMT  
		Size: 839.7 KB (839692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352bdaee988c61b20b656df8008d4be213733165c725560536714f21e8cf2ad2`  
		Last Modified: Tue, 07 Jun 2022 06:15:39 GMT  
		Size: 4.3 MB (4268418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e95ee74d62367ac78bdf552d35893b1bfa0b8538f69894f4ca7d5c558975e79`  
		Last Modified: Tue, 07 Jun 2022 06:15:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0702606dc329e1f145eeaad6f2f9524dc0917eb5ba25853c54f2e8025773e2`  
		Last Modified: Tue, 07 Jun 2022 06:15:38 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025651dc59757e03c16f059d8f61cb6a4f6ba0e81af77f6ad318d2bd7e0722fb`  
		Last Modified: Tue, 07 Jun 2022 06:16:14 GMT  
		Size: 252.4 MB (252387652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba45e675ef36970c7566157a82c9773fec38abb8e1dc9c1ab5228c5c333d1b6`  
		Last Modified: Tue, 07 Jun 2022 06:15:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f068196edb1d7b534e8104afff942478c06340976dcb3d4e4a774cbebf82daff`  
		Last Modified: Tue, 07 Jun 2022 06:16:34 GMT  
		Size: 63.1 MB (63076750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29281438a7a6ff1ad4878920abcef2cbb4ec2aebca524554f5785711059fc857`  
		Last Modified: Tue, 07 Jun 2022 06:16:25 GMT  
		Size: 280.9 KB (280861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52abeeddaef7b2bf20aa09a0de360fd0cee28343a09578cd2975aa04d87cd5bd`  
		Last Modified: Tue, 07 Jun 2022 06:16:36 GMT  
		Size: 67.0 MB (67001231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7836a98ca3a9f6ac7a5369792b042912457e839d10eb1679fb6ce3779dfc56f2`  
		Last Modified: Tue, 07 Jun 2022 06:16:53 GMT  
		Size: 10.7 MB (10735206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
