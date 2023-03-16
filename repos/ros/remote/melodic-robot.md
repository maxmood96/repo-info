## `ros:melodic-robot`

```console
$ docker pull ros@sha256:d16b38b062ff41bb9a5f9ecca69a5c84e72d3cb0322e4aab4a422cc9ed1f1d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:23d8dbab51038f248d2d19a1777a731af2b53008955e098cf5b0b9a7c9ec10b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.7 MB (448652161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f043259d2a2626442c70c295a13dfe775b25fd522ffdbb6eddf514edbfcc4b60`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:56:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:58:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:58:26 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Mar 2023 03:58:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 03:58:28 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 03:58:28 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 03:58:28 GMT
ENV ROS_DISTRO=melodic
# Thu, 16 Mar 2023 04:00:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:00:33 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 16 Mar 2023 04:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 04:00:34 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 04:01:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:01:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 04:02:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73b43b50fc9056c1213c61cfa3193cd15f8faa751905b21e0e9019473426a74`  
		Last Modified: Thu, 16 Mar 2023 03:11:48 GMT  
		Size: 819.0 KB (818997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6111169e4c0857f4eaf38437fa0beb5e0f66979105b8fdfd3c85c5c5e1544992`  
		Last Modified: Thu, 16 Mar 2023 04:41:15 GMT  
		Size: 4.9 MB (4878581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280739d0ef2f7bb759ccb3b3bb8a5f15a3d1ee562afe99609a493c65039b87a6`  
		Last Modified: Thu, 16 Mar 2023 04:41:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d189808242488a25bc31490cfec5360bcb99b6a965f8782e6af80cf69e81ad79`  
		Last Modified: Thu, 16 Mar 2023 04:41:14 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc74d1ea892a60a383eaee3d39a2f94fcd19fa347ee48e940f7152e5a8d6bccb`  
		Last Modified: Thu, 16 Mar 2023 04:41:48 GMT  
		Size: 259.6 MB (259588669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43567d3a1b9a70a0e7ec7a689892a144345cf9bcb6eb4151afba22b1eab2d47e`  
		Last Modified: Thu, 16 Mar 2023 04:41:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc128d1e3275f672a35efb8cc6d100ff910f036dc6bbfdb5d0beea7ba5a48370`  
		Last Modified: Thu, 16 Mar 2023 04:42:06 GMT  
		Size: 70.3 MB (70268059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc3dceb46441b9a8de4be3a53517c7cf44efe430d819993027ffd084b6dc13b`  
		Last Modified: Thu, 16 Mar 2023 04:41:57 GMT  
		Size: 297.9 KB (297878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1901e3f6c09a6bb1a3a48da8fb1162deb79e4a57ae416e9ca5b86ec2e21cab3d`  
		Last Modified: Thu, 16 Mar 2023 04:42:08 GMT  
		Size: 75.0 MB (75000651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2931bcf3ec12937e9d6e316229b002c7515d449faaafafa0db8522e959dbde94`  
		Last Modified: Thu, 16 Mar 2023 04:42:22 GMT  
		Size: 11.1 MB (11086733 bytes)  
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
