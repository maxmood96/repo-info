## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:58d005ec9465e0fe95b72a59234905c0f4e4ecfd4216910e317af67abcb60252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:03e17e6317e4e65d58883d37ba8b05a6bb805786480e4c0862d35af530ba8a74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300500143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf67f584ec11e38d39fcb8aa4cc831f033362886f1e04c65c08fe1a638e0c672`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:32 GMT
ADD file:5c5cde050dbdbd5c7c0d9c723f436d37ab4a8b1a498647a719771eccce99d9cb in / 
# Sat, 28 May 2022 01:20:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 15:31:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 15:31:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 May 2022 15:31:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 May 2022 15:31:04 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 15:31:04 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 May 2022 15:31:04 GMT
ENV ROS_DISTRO=noetic
# Sat, 28 May 2022 15:32:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 15:32:08 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 May 2022 15:32:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 May 2022 15:32:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:982cba7e471c6d3ce96014cf58b2e4e115a525e60da2e1e08716818f2c057a6b`  
		Last Modified: Sat, 28 May 2022 01:25:39 GMT  
		Size: 50.4 MB (50440422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5daa03f5fdf981e5e003e8bcdd00a064f8dec5b68d41a8637fa6e6614fb6daa`  
		Last Modified: Sat, 28 May 2022 15:37:19 GMT  
		Size: 10.9 MB (10892084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f843ce8d3b561918a03456323ce94ad1312c2635f4f04d88a0cccf0359be63`  
		Last Modified: Sat, 28 May 2022 15:37:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e16ee1496f8cf91f13a0be11f546bcc8a1019871d1ae4a593080f404b5cecdc`  
		Last Modified: Sat, 28 May 2022 15:37:18 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e5bca9474dcc4d1c2cb55eb48a9d537e3a19b1977360f0103e67ed68327b2e`  
		Last Modified: Sat, 28 May 2022 15:37:51 GMT  
		Size: 239.2 MB (239165226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e7664792e8911a123880c178f4d96e7735082492c404ecedd78d4ebfee2ede`  
		Last Modified: Sat, 28 May 2022 15:37:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fa6f900f8bc4964429c7cec97fc45e7755e94ab2b16b7e4dc1ade8d90af5ebd0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244293952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09146ff9c87a825048dba6a2047746045307900a5641c45537539fc17dc3280a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:49 GMT
ADD file:af879be34a7eccc177a3000eb8c45d5207bfbec108caf9be9d11c1a6620c376c in / 
# Sat, 28 May 2022 00:40:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 09:31:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:31:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 May 2022 09:31:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 May 2022 09:31:49 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 09:31:50 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 May 2022 09:31:51 GMT
ENV ROS_DISTRO=noetic
# Sat, 28 May 2022 09:33:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:33:11 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 May 2022 09:33:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 May 2022 09:33:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fadbed17b01e84815ca3018d3dc42670c3add65c67e7cc74d6bc477ae8425934`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 49.2 MB (49229054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3038e2c6f4de92209486b85dbcdfb0c3794568ec22f4fd2438f984045c9ab600`  
		Last Modified: Sat, 28 May 2022 09:40:41 GMT  
		Size: 10.7 MB (10688315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3e60f35c740bab355e4948391f92c4a13422a4e4c8b87db723eadc9c13293d`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986db8ad07690449985043b0f62b086ffb7575f69651d238a6c7914d8964a16a`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5687faf58ed162f39e6695b07560ab17b035ad665611906636878c34709ce634`  
		Last Modified: Sat, 28 May 2022 09:41:11 GMT  
		Size: 184.4 MB (184374214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a862c7e717410bf0c285d49d4b7c55f6aa21daeaf531c763e01ba890bd544d`  
		Last Modified: Sat, 28 May 2022 09:40:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
