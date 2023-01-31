## `ros:melodic`

```console
$ docker pull ros@sha256:a423722cd718ebba9f6e931542d141b9336c609aca62136237147229567a2e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:fb723744019f7fd23ecdf827d98f438840ed49bc04be33b84b9394c90c2c20cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437545037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3373bdb88182d13d88b174fec2db62c13515f5c07f9e9f99accde09d5e431d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:16:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:16:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:16:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Jan 2023 19:16:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Jan 2023 19:16:36 GMT
ENV LANG=C.UTF-8
# Tue, 31 Jan 2023 19:16:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Jan 2023 19:16:36 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Jan 2023 19:20:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:20:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 31 Jan 2023 19:20:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Jan 2023 19:20:44 GMT
CMD ["bash"]
# Tue, 31 Jan 2023 19:21:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:21:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Jan 2023 19:23:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1703b06e751e0680eec7a303ffd99a0b6d283044ef8ce1df7aa4f2659738335e`  
		Last Modified: Tue, 31 Jan 2023 20:06:30 GMT  
		Size: 819.0 KB (818957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff2dc1af9e78c8c03b3784e97b0c62313c5c52add693cb706e068fcce901459`  
		Last Modified: Tue, 31 Jan 2023 20:06:29 GMT  
		Size: 4.9 MB (4878622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ce8ecd18ce9a61cc5b737d625584f81283c15635bf0c0f055c4c0b3a67563`  
		Last Modified: Tue, 31 Jan 2023 20:06:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae71cc8d37cc871d60eee81184bc6d8a1e1c866501778e161631792888554553`  
		Last Modified: Tue, 31 Jan 2023 20:06:28 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bb8fdfb699e9ced52d11673eb22698de7487b7fc88a857f4508b0a950e9c01`  
		Last Modified: Tue, 31 Jan 2023 20:07:02 GMT  
		Size: 259.6 MB (259570609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1291bf00d97c79825103e22492524225aeab5e47bbd31ab04844639b765db48`  
		Last Modified: Tue, 31 Jan 2023 20:06:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d4df0a9d6cae5901fa83c22b170c6613ec8554355268edd38fa9474b59df15`  
		Last Modified: Tue, 31 Jan 2023 20:07:21 GMT  
		Size: 70.3 MB (70266400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe392d68e0b6456c752bccd1fb9cf78e14ab1a3e5e740974f70f35496e719dda`  
		Last Modified: Tue, 31 Jan 2023 20:07:11 GMT  
		Size: 296.5 KB (296510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023408b2b9e07a73bca7c237d1219b5bcc04e13cc52633064f49e90fe444019e`  
		Last Modified: Tue, 31 Jan 2023 20:07:23 GMT  
		Size: 75.0 MB (75000498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:c2bb574e034735f687dad3f78b30822b56f93ecc67099939469a79b8732190ad
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (386028403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62a82935fb270cc1459cc69df1e3ffba90f30fd177f408c00150af724fa04b5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:56:13 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:56:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:56:18 GMT
ADD file:1cc75b54b9c4d0824203532d4bb0eea2aaeafed003e37057b21aa3713b6bb0ea in / 
# Thu, 26 Jan 2023 09:56:18 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:20:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:20:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:20:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Jan 2023 18:20:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Jan 2023 18:20:23 GMT
ENV LANG=C.UTF-8
# Tue, 31 Jan 2023 18:20:23 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Jan 2023 18:20:23 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Jan 2023 18:23:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:23:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 31 Jan 2023 18:23:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Jan 2023 18:23:41 GMT
CMD ["bash"]
# Tue, 31 Jan 2023 18:24:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:24:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Jan 2023 18:25:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec3bd771f252293c5a70a0e50b16a27aa4cc182d5d5c4944c803b38ad12da038`  
		Last Modified: Tue, 31 Jan 2023 18:14:25 GMT  
		Size: 22.3 MB (22306068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898bc29158f865556f2328416deec408f89e4d5a959fac7ce4e350e350cf9948`  
		Last Modified: Tue, 31 Jan 2023 18:48:36 GMT  
		Size: 819.9 KB (819866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3252175da0105a82655f398b29438a19ec2e04f09ab235f83c29a401118f52df`  
		Last Modified: Tue, 31 Jan 2023 18:48:35 GMT  
		Size: 4.1 MB (4090515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31a38036063f67ca8d81ea7a7c48a0913f990ecc729a0f15ee4f76c8a1357c5`  
		Last Modified: Tue, 31 Jan 2023 18:48:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e5eb71797c26c4e2ace97586f0a68a43ce039f27828c6cf21272575ed2e6d7`  
		Last Modified: Tue, 31 Jan 2023 18:48:34 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c857a22c653cbfa30c01daeec86e851722e951de12cf98b755879a24931968d2`  
		Last Modified: Tue, 31 Jan 2023 18:49:15 GMT  
		Size: 239.0 MB (239028794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1278f26ed1cb273ce9811a04653bd478c9ef002fe208fbd3e55bc3c453d0f08b`  
		Last Modified: Tue, 31 Jan 2023 18:48:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66aeaf0eee0ac2d0004bc039c468a9230185faf6a37bf6d59d066a08d4500d90`  
		Last Modified: Tue, 31 Jan 2023 18:49:34 GMT  
		Size: 54.7 MB (54734814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ae25993c4669492bc1aa92d06f588563bc78055f50aaadd125d0f334dd5299`  
		Last Modified: Tue, 31 Jan 2023 18:49:26 GMT  
		Size: 296.5 KB (296495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7420fb008761a5a6d4974897a05891dd41de92eb360067fd91f6756bb177634`  
		Last Modified: Tue, 31 Jan 2023 18:49:38 GMT  
		Size: 64.8 MB (64750001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cbc4321812febb57cf26ee000188f548fa7f7896777a8de6532b5c954547e210
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.2 MB (412186398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f22525eac142b3219ca19244a21332c32edb778f702c2452226dd59965f9ad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:08:36 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:09:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:09:01 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Jan 2023 19:09:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Jan 2023 19:09:02 GMT
ENV LANG=C.UTF-8
# Tue, 31 Jan 2023 19:09:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Jan 2023 19:09:02 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Jan 2023 19:12:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:12:28 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 31 Jan 2023 19:12:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Jan 2023 19:12:29 GMT
CMD ["bash"]
# Tue, 31 Jan 2023 19:13:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:13:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Jan 2023 19:14:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c58359f0ed0774e1ace1315b1a5c48c0d40a2519a5d69c92eb49fab69b4ff6b8`  
		Last Modified: Tue, 31 Jan 2023 18:07:50 GMT  
		Size: 23.7 MB (23735530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07ee3e3960c32779378327e6f45b0cd530d673aaafbc3bb02ebf81f340f231e`  
		Last Modified: Tue, 31 Jan 2023 19:57:20 GMT  
		Size: 819.9 KB (819907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457ad94c7976c1f0f92300e8bf04d61b97cdbd29d3abceaeb552e6521cbed456`  
		Last Modified: Tue, 31 Jan 2023 19:57:19 GMT  
		Size: 4.5 MB (4462834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67efd42af4fc7886de98ff96d096d4ed7b9405745d9c8906d5653f976ae45d47`  
		Last Modified: Tue, 31 Jan 2023 19:57:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122ab8439c1d060a597f2d5eeff25fd2eae59f3e64978304b242eb00a01cbda2`  
		Last Modified: Tue, 31 Jan 2023 19:57:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b402da9bc8f48c19c5a9c90957224b0897438f973cb1974d5c3cb2e0cf2a9152`  
		Last Modified: Tue, 31 Jan 2023 19:57:51 GMT  
		Size: 252.5 MB (252537988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6d1f86048a05a76b199644c17bad44b57ff7c17d5c2797c33a2f0f81cbd9a`  
		Last Modified: Tue, 31 Jan 2023 19:57:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48ff7870888fd7c2689a34ee0c08e62fa57bee0e5d98b52bebc5cf1dcda394a`  
		Last Modified: Tue, 31 Jan 2023 19:58:06 GMT  
		Size: 63.1 MB (63096000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc824988bb5fd5c68aca3c7d45ecd9cd00ed0e24d258fa00bc730849bed3ba4`  
		Last Modified: Tue, 31 Jan 2023 19:58:00 GMT  
		Size: 296.5 KB (296508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba479b0958ccd24153a47d4c5c9b9f25672e1388ad2b3449a3fbe8b3db1d8cc`  
		Last Modified: Tue, 31 Jan 2023 19:58:10 GMT  
		Size: 67.2 MB (67235785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
