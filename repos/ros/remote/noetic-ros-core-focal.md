## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:73ba67c09c6ab756c57a1d8654d692f3055a8c7ec54b06f120e5b4f877e968ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:846f250f6dd222e44ee17b7f871875e20abd569082de6299b1d3fb89b4a60ee9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212304339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c78d80b5cf8bf8109d294a84172eb5bc1f718d08607ed579e63932bac8cfa9d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:67ea8f522d8e90ade44c0d45a623b182c7dbb9f48f4b567f1079e6d3136ca48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187982732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c3f4179402fe66a367adbf02ca6941b11a372f4111ef176ab7c3c7de1f500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89a530ed26b46eee46941dbadbb46db7466d5e5ce9d18d067dc815b0d3052467
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205343046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbd10085e3bd8e389031b83d712cb3a42365b13f88c647a9ee795d92151879d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
