## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:4963d81fa53f3fde4c142e189e724ea6fce303fdc0507fc155234146d8df5db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:953694421478b83fbba6976e01a5b90cad68357b90f6529b7d2ef1b3446a00c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463447648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761281453a86dd6f2a1f49082e6d95a477f3f57b89d6a5be4bfd28b811b19c6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:19:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:19:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f066880bf184688bbe3b3bce165ab3ad72850aae130b41b408020b47003491`  
		Last Modified: Tue, 25 Oct 2022 07:57:07 GMT  
		Size: 86.6 MB (86586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c12225f8506452bbdfb135687a0e9642f4fd2bec37dacde2ff8e68f0031c8`  
		Last Modified: Tue, 25 Oct 2022 07:56:53 GMT  
		Size: 326.7 KB (326687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cb66701beaeeb105d227e3c100dab245e25d8e913dcb72fb68145181a9140f`  
		Last Modified: Tue, 25 Oct 2022 07:57:05 GMT  
		Size: 76.0 MB (75978159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dafb622bd0ec9c3b26dbddbfbea7811f23b16c2763a7cfedff27ce00dc3291fb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403303632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907dceb9ca2faa0d1ce52ae69c6569c16777514bca500657a2c0643760f5fcbc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:07 GMT
ADD file:21afa32c0395cc5046d09741d6821d21cfd9b77bce46ebcfc8fd9aca57c73648 in / 
# Tue, 25 Oct 2022 05:46:08 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:25:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:25:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:25:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:27:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:07 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:27:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:27:07 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:27:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ba81f4c3c21f92780061ee116827d64ac4edbcd02b056845c2aaa3097b730ed`  
		Last Modified: Tue, 25 Oct 2022 05:49:24 GMT  
		Size: 49.2 MB (49233280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d908f4a3bf1681c533c1f96d98947d2633d0dcaba9dfd301e3012eccad131bc6`  
		Last Modified: Tue, 25 Oct 2022 22:03:50 GMT  
		Size: 10.9 MB (10902593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83583a72ce25a255e794a38648eb0801f9216da38498d62ffb9804978957d95`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1a43410632b0d298d4c6dd3c98b00cf2db2e6c8f50916bd61fcb89cda1d392`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae854a5636ab767fe777452319631201aee587f29bea10e23ec81f5b368c445e`  
		Last Modified: Tue, 25 Oct 2022 22:04:20 GMT  
		Size: 184.4 MB (184376816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab694da339128addba43dd72984d8b40529266d26831ea594d60a8e3cd25b3`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b981c9cfec0e372d9f2e94116b59186d02a91e10dd99e9a8a10431e4e413f65`  
		Last Modified: Tue, 25 Oct 2022 22:04:37 GMT  
		Size: 84.4 MB (84372303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f047284ff16936b6148e2a2a68062d6263f473b9a42b4c1c0f1aa1fb42ed60c8`  
		Last Modified: Tue, 25 Oct 2022 22:04:28 GMT  
		Size: 326.7 KB (326683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de179756dba0e248264ebf803f000dce4ddada0cbe200f61a3fbeaf9c6a7e9e`  
		Last Modified: Tue, 25 Oct 2022 22:04:36 GMT  
		Size: 74.1 MB (74089547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
