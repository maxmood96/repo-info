## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:a4390f135fffd127d22551438f3300550c11346e85c0df6480d169dc907cee6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:f21304aefed4d986028828f8dd4396439d7a26eb5bba02dbc54548bfc62b8be6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484654631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b4f231c4834ed6ffdebb57826b674b6e4a08226cff414a4d6831bd0809036d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:15:55 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:15:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 04 Feb 2023 13:15:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 04 Feb 2023 13:15:57 GMT
ENV LANG=C.UTF-8
# Sat, 04 Feb 2023 13:15:58 GMT
ENV LC_ALL=C.UTF-8
# Sat, 04 Feb 2023 13:15:58 GMT
ENV ROS_DISTRO=noetic
# Sat, 04 Feb 2023 13:17:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:17:21 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 04 Feb 2023 13:17:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 04 Feb 2023 13:17:22 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:17:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:17:54 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 04 Feb 2023 13:18:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:18:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44bf9327e4b7a8bf848c3699b20510e32f95481ba13b8d9a946754f18342fa5`  
		Last Modified: Sat, 04 Feb 2023 13:24:05 GMT  
		Size: 10.9 MB (10897097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b8a10b01929717aa618dcd6f710b0e66ce6ab72f8843e73f630735c2a73aed`  
		Last Modified: Sat, 04 Feb 2023 13:24:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dede64640aa97c0401af7c42dfc94a82841ba4c553f1e18510827c72b00afa14`  
		Last Modified: Sat, 04 Feb 2023 13:24:04 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604ceb6b1629e4d9e26c32dc0a33f68646f3e612f944ca073bdae4a5e7669778`  
		Last Modified: Sat, 04 Feb 2023 13:24:37 GMT  
		Size: 239.2 MB (239213880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659253c15397780551648f4e45c5915f6c3755e130e90fab1863f70c0124c436`  
		Last Modified: Sat, 04 Feb 2023 13:24:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bab81f9da21051763a7465deae8adac30260328bb9c35d25d676bd16176d27`  
		Last Modified: Sat, 04 Feb 2023 13:24:55 GMT  
		Size: 86.6 MB (86621101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c106973deec2e91cee88be69bb3557ec1139dd8cf6e0acc3af22d0f75bd0f43`  
		Last Modified: Sat, 04 Feb 2023 13:24:43 GMT  
		Size: 337.3 KB (337308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893cc2ca9a9446635b02ba2e46a324d7c9106103c2fc2a52e182f357d8b38f87`  
		Last Modified: Sat, 04 Feb 2023 13:24:53 GMT  
		Size: 76.0 MB (75978133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0751c66be7b627971424a7dd94e358719d59df5854d5e2c1a524c24495d9e8`  
		Last Modified: Sat, 04 Feb 2023 13:25:04 GMT  
		Size: 21.2 MB (21155588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ed477a6be40e207acabea7d63edf972e40423376f47ad8ab2f7c2155af2ef8b3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424216536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ba788c7fd4f8a2b2e64980a0826988a1226da2e9341ebfe57e36fc94c03c37`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:43 GMT
ADD file:6b2b58305052bb953886c976022efeb324ef33bc6e55f9e15915e98490bd8fcb in / 
# Wed, 11 Jan 2023 02:57:43 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:52:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:52:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 11 Jan 2023 13:52:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 11 Jan 2023 13:52:26 GMT
ENV LANG=C.UTF-8
# Wed, 11 Jan 2023 13:52:26 GMT
ENV LC_ALL=C.UTF-8
# Wed, 11 Jan 2023 13:52:26 GMT
ENV ROS_DISTRO=noetic
# Wed, 11 Jan 2023 13:53:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:53:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 11 Jan 2023 13:53:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 11 Jan 2023 13:53:46 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:54:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:54:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 11 Jan 2023 13:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:55:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:15639959ffec1b29b8f88b1e1db3ca0574ca52ee28fd8f3ac6d2cbb1c85fb209`  
		Last Modified: Wed, 11 Jan 2023 03:01:37 GMT  
		Size: 49.2 MB (49233802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426afb0be41a462ca64e39ae6a74ed19ce54db5cd4d8fc00b5094120e8fa8f2`  
		Last Modified: Wed, 11 Jan 2023 14:00:58 GMT  
		Size: 10.9 MB (10902625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71036bab13158db91bd98501b67328211754dad8cac28846bf4aa4ecbde4d658`  
		Last Modified: Wed, 11 Jan 2023 14:00:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e7410b12ea7be4c80024e40f3adcd15efb8dd2b0b24abe4227c4f21cfa894b`  
		Last Modified: Wed, 11 Jan 2023 14:00:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f2c8b362ea16751add95c3717f39e7f30cf2649c3affcc6ae88a08aeab9a5b`  
		Last Modified: Wed, 11 Jan 2023 14:01:21 GMT  
		Size: 184.4 MB (184440458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f46ce4b267a4a43fa1378cdd5ec96948d2840335e4ca90ab3100c67516d4c6`  
		Last Modified: Wed, 11 Jan 2023 14:00:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc73cadcad0750f2ced4b8a64f684d077dbc86dfcb490e0705f01e359820dc26`  
		Last Modified: Wed, 11 Jan 2023 14:01:36 GMT  
		Size: 84.4 MB (84392048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2f8d1d96d181162c436accd0a6a33bc249984e8e5ad2fc5476f0e4dd056bcc`  
		Last Modified: Wed, 11 Jan 2023 14:01:28 GMT  
		Size: 335.5 KB (335525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7756844afb4448a1b4c4ef76967534312274fc784844e8f40aa841618908afb6`  
		Last Modified: Wed, 11 Jan 2023 14:01:35 GMT  
		Size: 74.1 MB (74090649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dc647d253f2ca3df07893ab76884b46421df6548be3b133e786b1ca0a309aa`  
		Last Modified: Wed, 11 Jan 2023 14:01:45 GMT  
		Size: 20.8 MB (20819018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
