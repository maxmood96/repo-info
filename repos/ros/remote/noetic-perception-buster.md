## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:e31da63b582dfad4ff372343b592993069d2ce4fa99c4a7b723399f8de3aa03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:88479259632814a8ddb61920a92867d0def1dd2e11eed92df6c05c8d2fa80525
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.3 MB (951332474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d05d361671e5f86b254c9b2d26943f3a1ecc3b8a35b5bccf598c2bd6945a81`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 11:15:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 11:15:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 May 2023 11:15:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 May 2023 11:15:16 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 11:15:16 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 May 2023 11:15:16 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 May 2023 11:16:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 11:16:55 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 May 2023 11:16:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 May 2023 11:16:55 GMT
CMD ["bash"]
# Tue, 23 May 2023 11:17:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 11:17:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 23 May 2023 11:18:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 11:22:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afe32a9e2aa6879179dd922d5110e7b70656894335d0a5d170f862b6b738bcc`  
		Last Modified: Tue, 23 May 2023 11:23:45 GMT  
		Size: 10.9 MB (10897032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3c517d1af8a91bc39846331070b017a72fa5cb36d5854b5389b5a30036b942`  
		Last Modified: Tue, 23 May 2023 11:23:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9213c642439a1e4a1896146dbbd56aac4577e20e81ebd8577f5dfa3f4dd5b633`  
		Last Modified: Tue, 23 May 2023 11:23:43 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97123da21a1729378dd90e7c547d899f8f278f8d8829b36baf5c46599553d42`  
		Last Modified: Tue, 23 May 2023 11:24:13 GMT  
		Size: 239.3 MB (239263027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eae86dc626aaa5855cc667d28fdf589cbc2c5b5c8490c57bd367160b2362ee6`  
		Last Modified: Tue, 23 May 2023 11:23:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a150ccb7e110005de8d7a69a9039a58733bb01fa11dc76078297fd8c6721d96`  
		Last Modified: Tue, 23 May 2023 11:24:31 GMT  
		Size: 86.6 MB (86624909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259069c799d6a2a44eb46f8de53e0593c75ff98a78d7b60b73ba324ea3763b6f`  
		Last Modified: Tue, 23 May 2023 11:24:20 GMT  
		Size: 293.6 KB (293589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc60d88871e2db978be27a714aada59aa620f329bb8e94d0bb094d4e01d92f78`  
		Last Modified: Tue, 23 May 2023 11:24:29 GMT  
		Size: 76.0 MB (75978152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723ee5d72e12e0072b8482b3c8d295c1d8d9b588ad66b938f8caccfc6618bb1d`  
		Last Modified: Tue, 23 May 2023 11:25:53 GMT  
		Size: 487.8 MB (487824638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:39428f939a086c7656f8cc93776e579c6b252a9972e77771aeaf96bda37a3bc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.2 MB (868182924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e1df8dd582ee1a7a61976a11ebe53aaba3e092a27e68d41d8f85b6186d1b9d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:41 GMT
ADD file:bb3cb9e6abc423742d7c1b6bc006a7cef70038c5621c71a90a2ae7c1ea29ec63 in / 
# Mon, 12 Jun 2023 23:40:42 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 13:42:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:43:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 13 Jun 2023 13:43:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 13 Jun 2023 13:43:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 13:43:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 13 Jun 2023 13:43:02 GMT
ENV ROS_DISTRO=noetic
# Tue, 13 Jun 2023 13:44:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:44:28 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 13 Jun 2023 13:44:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 13 Jun 2023 13:44:29 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 13:45:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:45:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 13 Jun 2023 13:45:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:50:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e8371d57f7426517aead21bff5af0cf321625cac166c86214c439fb67db84243`  
		Last Modified: Mon, 12 Jun 2023 23:45:01 GMT  
		Size: 49.2 MB (49238409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03375f4355e227cafbfa908999c3ddc516dfece8850f794cbfee3d98a3b0e4d`  
		Last Modified: Tue, 13 Jun 2023 13:51:27 GMT  
		Size: 10.9 MB (10902698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87455fe1f6c14ca646af35900faf90365ac3f7e81bed4b81b88e3abb574a4402`  
		Last Modified: Tue, 13 Jun 2023 13:51:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc3c46e762a7441e9f9691783ed4686cefafc163ebd2a456bdf433c89287d8`  
		Last Modified: Tue, 13 Jun 2023 13:51:26 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55db42145f6caf7e455205c09a9a1d3663adc3f0db751eeb654008b42dca4736`  
		Last Modified: Tue, 13 Jun 2023 13:51:48 GMT  
		Size: 184.5 MB (184469619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095f9b9f16405a7957c5409754d18a64bbe1f89878c0017a77fdde5fb330d868`  
		Last Modified: Tue, 13 Jun 2023 13:51:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeab7876fa087145597e605094b6a924f8619de8caf0255491fc4fa0f2948fd`  
		Last Modified: Tue, 13 Jun 2023 13:52:02 GMT  
		Size: 84.4 MB (84396970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aec8582d4f1b67ba097e7f015d6d6ad0dce469e56472570a9c1f44adfb35a4`  
		Last Modified: Tue, 13 Jun 2023 13:51:54 GMT  
		Size: 295.2 KB (295178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa121382b620e16c5f9ecbd7272677d1b17895ebb4f1143c54a743fbcd589ed`  
		Last Modified: Tue, 13 Jun 2023 13:52:01 GMT  
		Size: 74.1 MB (74136032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da614d951cd5c82b6858a4442fcb9a82ef3b68a63dbf191e6c6d95f4787d810`  
		Last Modified: Tue, 13 Jun 2023 13:53:03 GMT  
		Size: 464.7 MB (464741604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
