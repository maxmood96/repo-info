## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:01d1f416ae746c681ee32c6df1abcb50ea7ee510c4ba8c0dd0e6eafaf6a4cd2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e894f44bf088cc62986b1aae33d8a8ec96810c746194983ce48d373f28c2eb60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437515827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e77b7e42944fc41a062c94ba1e54f9bc75737c6f1ee3293947939145ea10318`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:23:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0804aad7d24aedc9674dd262573672ffb24e77bd0b94b38774dd4c1344a65`  
		Last Modified: Fri, 02 Sep 2022 05:05:12 GMT  
		Size: 70.3 MB (70259712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4c705dfb136d0edfefa4b6ea486990b27430cb1acb7e7aa9c680225f5845c`  
		Last Modified: Fri, 02 Sep 2022 05:05:02 GMT  
		Size: 284.7 KB (284711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d8179e60fd0676ccb9cded217236342e7d2d9185a56f2f003efb6d1e597bf`  
		Last Modified: Fri, 02 Sep 2022 05:05:14 GMT  
		Size: 75.0 MB (74995198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:df938dbfce72ec195200566eb00a046505a08bd0468c8d38f6853705b651be2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385999606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df02f2bbc53d38e90f00067ea8a4879191d1479c4dc6c613203aed1c27cc4e85`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 19:33:23 GMT
ADD file:45c82fca220161f3905a06e276f12ec0cb3be5c099cca70bb6d495da10088f7d in / 
# Tue, 06 Sep 2022 19:33:24 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 20:02:20 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:02:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:02:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 06 Sep 2022 20:02:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 06 Sep 2022 20:02:33 GMT
ENV LANG=C.UTF-8
# Tue, 06 Sep 2022 20:02:33 GMT
ENV LC_ALL=C.UTF-8
# Tue, 06 Sep 2022 20:02:33 GMT
ENV ROS_DISTRO=melodic
# Tue, 06 Sep 2022 20:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:04:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 06 Sep 2022 20:04:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 06 Sep 2022 20:04:42 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 20:05:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:05:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 06 Sep 2022 20:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:074d633b5bde02245e333b110dde5850e06ea4ebefe4283af6e4dfd8d462b170`  
		Last Modified: Tue, 06 Sep 2022 19:35:07 GMT  
		Size: 22.3 MB (22305954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4089b68bf46009d284fa16ca1d621c7049f3db1038f87fdc58aa3e52059`  
		Last Modified: Tue, 06 Sep 2022 20:09:19 GMT  
		Size: 832.1 KB (832054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb5783e1925df093ff571a9432fe1c845b3ece17f25ceaf82d5608e22b05bd1`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 4.1 MB (4088159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f716a6e78a03f97c202a01a3e1e98cf10bed5364c7c32c839c867d13681a6`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ca0dfda7d5b871d65a21978a3eb27b0e0df4356a07344a412a47884c99fa97`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f2026bdd33971a08db14214c57a9844a8b07c0419dd4f91cdb452cc945d2da`  
		Last Modified: Tue, 06 Sep 2022 20:10:01 GMT  
		Size: 239.0 MB (239016534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409e6ba5da3e6f8d9bfe01490e9a5fdbc6c46106af86015aa53de972cf17fb92`  
		Last Modified: Tue, 06 Sep 2022 20:09:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18156240d002de6754c981e2a6b01263d8e5b2ed7533d540aed2523a440b8969`  
		Last Modified: Tue, 06 Sep 2022 20:10:24 GMT  
		Size: 54.7 MB (54720950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe655b5f5872d42a2aa6dc285aee77585f2b351d69bf0fa7e469e55e08d5b4d`  
		Last Modified: Tue, 06 Sep 2022 20:10:14 GMT  
		Size: 285.5 KB (285538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056747a254333c4839465266c56c71c9917689606230324d5718be769198ebce`  
		Last Modified: Tue, 06 Sep 2022 20:10:29 GMT  
		Size: 64.7 MB (64748572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aa69b5ba8c09387ac30a0a61a0915bcd1f531fe8cdb6ddf06653e24ea840e3ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411708652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58250c8a80c58321b727945b00fdd1165730914bd9abdd446325c8c22ed25710`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:49:02 GMT
ADD file:26cb5ace98a4462b36211bf28f1e73781dd6d8984350d9bd53243dbe50ae180c in / 
# Tue, 06 Sep 2022 18:49:02 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:39:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:39:34 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 06 Sep 2022 19:39:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 06 Sep 2022 19:39:37 GMT
ENV LANG=C.UTF-8
# Tue, 06 Sep 2022 19:39:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 06 Sep 2022 19:39:39 GMT
ENV ROS_DISTRO=melodic
# Tue, 06 Sep 2022 19:41:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:41:03 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 06 Sep 2022 19:41:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 06 Sep 2022 19:41:06 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:41:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:41:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 06 Sep 2022 19:42:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d30cf2a6a25aea48a115837d149468c8de7df7fb51f210b9fa1173c065f7b34c`  
		Last Modified: Tue, 06 Sep 2022 18:50:34 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c4f657f16f312fa6dcdfe1497bf20b105de50db3390adc504f994c2e9f5b26`  
		Last Modified: Tue, 06 Sep 2022 19:47:40 GMT  
		Size: 831.3 KB (831309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0409a4a76860508a3bb6248ebf7f6c0e2710dcd922c36a4959dd70bc0bd27e`  
		Last Modified: Tue, 06 Sep 2022 19:47:38 GMT  
		Size: 4.3 MB (4265677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8c9b1355942f3d60e38808189d3e6d165d5be537fefc37fa08042bc39b874b`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890877cc8e4438ec9389664d9d410292ebcaed1e9f7bb0790d11083308930c25`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d08560eb8db9469de77a96e0f07ccc2d8735796b72d3360b34d33ea2ea3e9e`  
		Last Modified: Tue, 06 Sep 2022 19:48:12 GMT  
		Size: 252.5 MB (252503601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7dfbfc923a78aa6af356834ddc818505716f9ed414c5c15cd9563f4df2d3a4`  
		Last Modified: Tue, 06 Sep 2022 19:47:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e737e5219269563197c5a1752c0204a040cbf1b5392ed477a228b2aad8429087`  
		Last Modified: Tue, 06 Sep 2022 19:48:33 GMT  
		Size: 63.1 MB (63088672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcec473689040d5e1f94c9b1369ff622507a6679936505c84d0d2928fc5dcc0`  
		Last Modified: Tue, 06 Sep 2022 19:48:24 GMT  
		Size: 285.4 KB (285399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c063648ef6b170ec80363adfdf39d3c9585b60a8ec03510bc5872de9a351f87`  
		Last Modified: Tue, 06 Sep 2022 19:48:35 GMT  
		Size: 67.0 MB (66998115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
