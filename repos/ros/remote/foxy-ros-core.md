## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:03528d3871764da0c6cee24e7baaeee8562c4ba3e90debfae5746ecd42ac82ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:87d8f4e045ca908ea1e9fc36cd58992b068c2243cd417af51df28015cae361c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155649379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f133e19ba781eb57466f334011e632c7258cb020aa4bd3f02210dc2724fc2f68`
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
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
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
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:14b37ec2f8cb57f1f948ddcb5dde6683ad4fed9db0365ff2ba990b3008ede6e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138445026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaad4dee75eed93cc82b94029a2a7353ef3d2e022f002a56599f1750b75818a`
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
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 21:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:35:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:35:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:35:02 GMT
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
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1125e614642ae08f414585e39268e20619496243391fc14223c48efb76567fe`  
		Last Modified: Tue, 25 Oct 2022 22:06:20 GMT  
		Size: 104.5 MB (104549412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257e5f004cfece29d48f51619b6b61a55c530aa1ecbc38e1be4208caa2ae368`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
