## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:1b88921e614ddb5e72223547f89868583789ca5912472f6019cdf7e998248651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:518d9f49f3956bf92607be0c47a8dbf00d0c567dbb919c607b611e3bcf8c8912
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212002719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b1740831ef859270de7fd9091d58dda92142f7d3f71df422fb26d0376da185`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:45f08fb5b042970e1b561d9b3940fdabc46b34958678536c54a07e17c3a253cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187137436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a223e481044d9ab0a67a6bad021ae42bd8957c52c4a9357dd2632e569d1594c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9b5b88250a972b3fc9a192cdd5c9678df78af943a929029f915130fef85cbe43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205008829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca665cbdb77afab287059cb642a874abc6ffefb94725ad83c3ddf747724e552a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:03:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:03:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:03:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 26 Jul 2021 23:03:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 26 Jul 2021 23:03:31 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 23:03:32 GMT
ENV LC_ALL=C.UTF-8
# Mon, 26 Jul 2021 23:03:32 GMT
ENV ROS_DISTRO=noetic
# Mon, 26 Jul 2021 23:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:04:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Mon, 26 Jul 2021 23:04:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 26 Jul 2021 23:04:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47ae118bf19cf825ac83647c1d65d099e24417c73620e6553806e36aa26d8c5`  
		Last Modified: Mon, 26 Jul 2021 23:20:22 GMT  
		Size: 1.2 MB (1183453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74becffb9ea2d3b903303692f91a3abc607df25339bd7464db56343eefb622e`  
		Last Modified: Mon, 26 Jul 2021 23:20:20 GMT  
		Size: 5.5 MB (5512652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578d28ea46fe795b56172879ee97757cb6ea98226a43662f62f5bd8e1490c4fb`  
		Last Modified: Mon, 26 Jul 2021 23:20:19 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b73a67b1165693bd1ae07bace3301ab4fb82cfe1b5e61e2b536d3e2f75e47`  
		Last Modified: Mon, 26 Jul 2021 23:20:19 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2161207e597e1e7621916bed37a91d2ed819071ecf81902fa5f9a199d8581048`  
		Last Modified: Mon, 26 Jul 2021 23:20:58 GMT  
		Size: 171.1 MB (171140053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eab310c95b66fdb5ac105888d128d19608c8cd336dad6a23a85eee7e7b3a3e8`  
		Last Modified: Mon, 26 Jul 2021 23:20:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
