## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:9ca6a30b5a5955c1eaf3dd5f6861159e64a0e541c5a41931dd6dcaece396f7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:6c5832e2d84090112679bdf9555940df7945a6fc5ac833b74bd4b3a0919ce99b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463243986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72680f96123b9225bb0b5efb2484df6119d69ca2bbe8520ab36d53cf7a9b02e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 21:16:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 21:16:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 28 Sep 2021 21:17:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 28 Sep 2021 21:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 21:17:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 28 Sep 2021 21:17:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 28 Sep 2021 21:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 21:18:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 28 Sep 2021 21:18:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 28 Sep 2021 21:18:24 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 21:19:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 21:19:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 28 Sep 2021 21:19:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057f5227de8f6db89935faceb04e14221b934ffc6724618581f7e8392970c3ed`  
		Last Modified: Tue, 28 Sep 2021 21:24:45 GMT  
		Size: 10.9 MB (10891832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd2be7e40d77e274ec22ddb4f87a6316ce568f810184a8e59e18ba01fc96932`  
		Last Modified: Tue, 28 Sep 2021 21:24:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6d934e0e2132b27cda2cacacb9088097b537f9a40cdf536e2abc5d225c6387`  
		Last Modified: Tue, 28 Sep 2021 21:24:44 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898c3d5d521ed7072839820050082135fe093df92e6924f017afc47ddbb42355`  
		Last Modified: Tue, 28 Sep 2021 21:25:19 GMT  
		Size: 239.1 MB (239056614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57e0d0e6e00100bc444c8c1ff5b4028e0de1a63fe406669810c494e10803f6a`  
		Last Modified: Tue, 28 Sep 2021 21:24:43 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7a76943e01f7c49865103cc39e2286c3b843b81a9c9c07e122dfeeb1c99f93`  
		Last Modified: Tue, 28 Sep 2021 21:25:41 GMT  
		Size: 86.6 MB (86566434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb2d48531002cdd91f487084f1be81a6be323f175934a6d8ee366927fc89efa`  
		Last Modified: Tue, 28 Sep 2021 21:25:27 GMT  
		Size: 315.2 KB (315239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce5ac6d6887766f72c3011574775084de91b975f55a84cd4347d3bc3e028e6`  
		Last Modified: Tue, 28 Sep 2021 21:25:38 GMT  
		Size: 76.0 MB (75975243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cdf99750830dd20baaff40832d809188c310cc50e756a5ebda57f957fb0d4bb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.1 MB (403112247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91640fff9a9235c79504f2d762e335c216d45f35a30c06904aeeaebba5b0bd6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:56 GMT
ADD file:51975e5f400da759b2cd8f7eba13ad61dd4edbbee0d0fac09b697bfa039d1515 in / 
# Tue, 28 Sep 2021 01:40:57 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 12:17:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:17:58 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 28 Sep 2021 12:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 28 Sep 2021 12:18:09 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 12:18:09 GMT
ENV LC_ALL=C.UTF-8
# Tue, 28 Sep 2021 12:18:09 GMT
ENV ROS_DISTRO=noetic
# Tue, 28 Sep 2021 12:19:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:19:16 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 28 Sep 2021 12:19:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 28 Sep 2021 12:19:16 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 12:19:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 12:20:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 28 Sep 2021 12:20:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70fe10514d0290bd1e8986c0fd63a67204813d37fc5863cf9bf8bf61b2031537`  
		Last Modified: Tue, 28 Sep 2021 01:48:53 GMT  
		Size: 49.2 MB (49222381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b719e84e5c17a05db4cb91b65b25f4cecd9fda5ca86f7c93b9e8918c83ad07`  
		Last Modified: Tue, 28 Sep 2021 12:26:12 GMT  
		Size: 10.9 MB (10883372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b180205050ab5009747a1fa863a1467a5e672c5116542801e3f3890b57cc64`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0309f751216573b01fdef820a8e7c97a9ef1170563c0136c2e3faa29e4e99ed`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290538ca4b138960141fb0cf9d84a1ada042c2286a8714c2afa426ef9ea5baf9`  
		Last Modified: Tue, 28 Sep 2021 12:26:44 GMT  
		Size: 184.2 MB (184242688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8fe4a6c015780d0a432c652d6ac68724f7b7305a66625f3dde29654973d374`  
		Last Modified: Tue, 28 Sep 2021 12:26:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570cd6760219c636efbd15651c975651d6776ef161e5daf5e95ca0d02cf74440`  
		Last Modified: Tue, 28 Sep 2021 12:27:04 GMT  
		Size: 84.4 MB (84358024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225d1354fc88caaadf4d1c8428bc28ea51f87d230c8889449d028a90955656a4`  
		Last Modified: Tue, 28 Sep 2021 12:26:52 GMT  
		Size: 315.2 KB (315237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b400ed504130934571dad558eea43e0360a76dce52a046e08a6ad9ca01b97e`  
		Last Modified: Tue, 28 Sep 2021 12:27:02 GMT  
		Size: 74.1 MB (74088130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
