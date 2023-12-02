## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:fc8b890012d2a92eb570f95e8df44917b940c8a6db361842e156ce94413204c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:aa2cf66a0f6d613a56907d64c1325f9219b8b151d9d675bcfd85b6944e999572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343162706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a5187b601f631f06e901329e1c6c9ee32ed4e1e4e235f6cd34d5af345f2cdc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 02:08:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:04:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:09:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:09:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:12:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1327734170da8c4ae4171fb4248189d0691d6b4a3f01b09239c3e34688651`  
		Last Modified: Sat, 02 Dec 2023 02:20:57 GMT  
		Size: 1.2 MB (1198788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77125e61032dbbcd43c015fe756de97b5661bdbbf4f5219588148f651ae900c1`  
		Last Modified: Sat, 02 Dec 2023 05:59:34 GMT  
		Size: 5.6 MB (5553989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80787bbb4e152705c432d0f6be72de515673d0bd1e13c308b0b2b79dab42b28c`  
		Last Modified: Sat, 02 Dec 2023 06:00:19 GMT  
		Size: 50.9 MB (50940359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f0aa48fdc5b62a25880ad49af8531594ffd5a9eec93f28c14935098f88138`  
		Last Modified: Sat, 02 Dec 2023 06:00:12 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0836b9b651f92dfca6a4c94574298a84d6bacf8a6bca656aed2e8303d90f6687`  
		Last Modified: Sat, 02 Dec 2023 06:00:23 GMT  
		Size: 79.6 MB (79616330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:0fd9dea9c5d965b8f1aac9de754061a9af491ee68a5f83f8ce06b3739794de24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5c45a515d47a675244ea3d82b56837ee4fbb452d87b30d3d6614dd9161af57`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:27:44 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:27:51 GMT
ADD file:043af50602b163e71a05aa02ec03cbbb2659582ffeea29004c4477939cf448e0 in / 
# Tue, 28 Nov 2023 05:27:52 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 07:01:10 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:01:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 07:03:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 07:05:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e2f879bfa159449422063ff666ac028f07b2d0d0240c9d1beecd2171ce0eac6b`  
		Last Modified: Wed, 29 Nov 2023 17:47:28 GMT  
		Size: 24.6 MB (24600167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d98a07bfa7aac27f091bf0d7219b9f7fde1d8aaaef4867256e199e71b299f1`  
		Last Modified: Sat, 02 Dec 2023 07:13:58 GMT  
		Size: 1.2 MB (1198794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3b1f005911cb4959d07abd5ac0987c950ecd363f9b62c9ee6a67f9c4207207`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 4.7 MB (4679365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b79dd0ed94f80d2de78257d78c33d475395e1d9e55732cd72ada3887a0717`  
		Last Modified: Sat, 02 Dec 2023 07:14:39 GMT  
		Size: 40.5 MB (40503315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5a3f5071b46f597aab2326583c0f774fd82fecc054a20570259f785de32873`  
		Last Modified: Sat, 02 Dec 2023 07:14:34 GMT  
		Size: 310.9 KB (310893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56d1947f08554ee75c5bda5801bfebf9ec01d3683acd6a10c163711051742e`  
		Last Modified: Sat, 02 Dec 2023 07:14:43 GMT  
		Size: 60.5 MB (60499537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:86754d86372cc5705c9dcdcb2078f2206e84f1533c8db73c737a8557e22d5cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322842615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90418c9f216065116e56913f7c337bb94efc9ea7a6ec2cf94548ea3efe4a99be`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:21:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d2acf9ee7cfde47b6ce997317767b8fa9bf8d93b8297016db9e093d06aa913d`  
		Last Modified: Wed, 29 Nov 2023 17:47:09 GMT  
		Size: 27.2 MB (27203865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2aa78ed8ad18394d7ae521e83b2810fec9fbb7d95aa074d794bb43e6e2bbfb`  
		Last Modified: Sat, 02 Dec 2023 06:56:12 GMT  
		Size: 1.2 MB (1198781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f106a95fef578814e019c4ac69f1cf32b15d5f85da2729a7ab2487c5d3505d`  
		Last Modified: Sat, 02 Dec 2023 06:56:11 GMT  
		Size: 5.5 MB (5532202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270ce1b1ab74f6a22bb249c1e772e63b0d3ede8da05dce0dd2b7c9965f3c20`  
		Last Modified: Sat, 02 Dec 2023 06:56:58 GMT  
		Size: 45.2 MB (45205899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739604b9ea2a1ceaa377c06051f683917437130648ea4f1d94825fd4c213a9c1`  
		Last Modified: Sat, 02 Dec 2023 06:56:52 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4198184c381704c040a49d0b342520596e024d46e12a627f21e6849afbf2b8b`  
		Last Modified: Sat, 02 Dec 2023 06:57:01 GMT  
		Size: 72.0 MB (71972220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
