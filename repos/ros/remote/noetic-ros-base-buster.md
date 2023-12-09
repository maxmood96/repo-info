## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:10525b5f5d44879f60c7b134a5c8c6048d800dd305433584f3bbc888367e0977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:4cd69ee0bc2bd756b6e968ecbaa1c8b3857c4964fdba51b10d9914c42440b6db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.5 MB (465454878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded28dc4870d86f9f7c7c13c6881865f20e98ad93c05e119495bcb5cad7a36f5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:27:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:27:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:27:10 GMT
RUN echo "deb http://snapshots.ros.org/noetic/final/debian buster main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 03:27:10 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:27:10 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:27:10 GMT
ENV ROS_DISTRO=noetic
# Sat, 09 Dec 2023 03:28:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:28:38 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 09 Dec 2023 03:28:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:28:38 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:29:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:29:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:29:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f209ac47bbad9349d294a1d1cbb6d9fcaff7160febbc4e64d287a05a15c5ae`  
		Last Modified: Sat, 09 Dec 2023 04:42:03 GMT  
		Size: 10.9 MB (10897281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc77feccf7f841b1658a5bef58a4cfd3986627fc513be817d7142eb99bb9b19`  
		Last Modified: Sat, 09 Dec 2023 04:42:02 GMT  
		Size: 3.6 KB (3623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471b8af9a66822c68acf4ff84e105b00bd47f187a4e65ac3616cbd040d560420`  
		Last Modified: Sat, 09 Dec 2023 04:42:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43875765bc15c16ab3a8d1581500ae72527c0f9bdbdbea24da0142b26cab5e63`  
		Last Modified: Sat, 09 Dec 2023 04:42:45 GMT  
		Size: 241.2 MB (241189702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53514930aa403bdf01922f5760100a224157886e4a1b3107f94291486d8912fd`  
		Last Modified: Sat, 09 Dec 2023 04:42:02 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceac8f8f906f05289ee6d5f7b23c0754f8b26d43c2fc17dbef34e379e4240df4`  
		Last Modified: Sat, 09 Dec 2023 04:43:05 GMT  
		Size: 86.6 MB (86626253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f3b2c08e2a9e1a85d6ab2f2e2f51f55b0114a79cd5ba4e0bd80a30fa628cef`  
		Last Modified: Sat, 09 Dec 2023 04:42:52 GMT  
		Size: 305.7 KB (305685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2daf9534b355cae9d23985a406b8f32012f660e96c2156aac4a5bf7268415848`  
		Last Modified: Sat, 09 Dec 2023 04:43:03 GMT  
		Size: 75.9 MB (75932440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e97726ab8dd3215e2e594ceb60beff90daeb05d6adcfd9732e6c4031e218c7d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 MB (405367419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dca62ad8a1aa90288624c6e4ace6699521057c2d02fd4d2060363f9d3433497`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 02:51:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:51:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:51:33 GMT
RUN echo "deb http://snapshots.ros.org/noetic/final/debian buster main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:51:33 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:51:33 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:51:33 GMT
ENV ROS_DISTRO=noetic
# Sat, 09 Dec 2023 02:53:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:53:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 09 Dec 2023 02:53:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:53:06 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 02:53:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:53:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 02:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e22731ba8317c3e4292079fcbb5665214e49bdedaed1d5ea8c26325acbd187`  
		Last Modified: Sat, 09 Dec 2023 03:58:22 GMT  
		Size: 10.9 MB (10902922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042f8166c7a898db9ebe3bdc1b1fd4b345c04f90c84acc1e215f054071ace6b3`  
		Last Modified: Sat, 09 Dec 2023 03:58:20 GMT  
		Size: 3.6 KB (3622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001d3d4be7cfa77e427d2ad833094ebc781e98bfeddcf1aed3ed9b25a3969574`  
		Last Modified: Sat, 09 Dec 2023 03:58:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741e8388dcee7d51f54711669e55120799938a387ab6a513e25e0c2297fffa9`  
		Last Modified: Sat, 09 Dec 2023 03:58:59 GMT  
		Size: 186.3 MB (186347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eba60571364761e21d390bfb43c00ab5bbf10ffec29442a543b2f13ec426a9`  
		Last Modified: Sat, 09 Dec 2023 03:58:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba8053d2e3150145c614df3f5743ce75a811f7a3c11b0310ebf37e1e1b52839`  
		Last Modified: Sat, 09 Dec 2023 03:59:15 GMT  
		Size: 84.4 MB (84397611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd316eff7db208a6a94aa74a4599b1b374dc28c8e45a1006ac78248bc7c5a6d`  
		Last Modified: Sat, 09 Dec 2023 03:59:06 GMT  
		Size: 305.7 KB (305686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2acf608305bb06a933fe1cca691a16357adb5e13db2ee669ede9611e80198eb`  
		Last Modified: Sat, 09 Dec 2023 03:59:14 GMT  
		Size: 74.1 MB (74118183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
