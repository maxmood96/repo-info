## `ros:foxy`

```console
$ docker pull ros@sha256:0c0e69ff71d21bff3a263c54143a60ea28ecebe24e3c01fdcfc642f883088914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:c6c4dcdcdba4646d8a6bebd6448625ed80cb18d8f1cae85e21a55a7e3d7ffec2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236641898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df65e6ff4c8f4ed1107f086582df71878afcbeb8d71e39214959ca5517adda77`
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
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:04:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:04:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588ff9fb226bda0f04608743623449eccc27c7cc333932238b83bb7ec32398ea`  
		Last Modified: Tue, 27 Jul 2021 01:17:40 GMT  
		Size: 70.8 MB (70843719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a912ea800775dd8e48e78dac7555405832fcd4ad530eeae4cc976ba08ed32dbf`  
		Last Modified: Tue, 27 Jul 2021 01:17:30 GMT  
		Size: 238.5 KB (238478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b8c908ab26db0ef9598ff88bf38a1008a48fa6cc4f426e318321c589e254b4`  
		Last Modified: Tue, 27 Jul 2021 01:17:29 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ba81eeaf2f769cfb5f06e3b9de2651d04e9927d713613e7e5e7f86afbdba4`  
		Last Modified: Tue, 27 Jul 2021 01:17:32 GMT  
		Size: 10.3 MB (10282984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cdcae8270776ec90508842a8c4507bb33cdc7d4214929a81086e14995baaca01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212758009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fb2a38e2f521cb18fcad29f129d0d60d00ccfff4b77004a8f8f5c0e8dc4d75`
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
# Mon, 26 Jul 2021 23:08:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 26 Jul 2021 23:08:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 26 Jul 2021 23:08:17 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 23:08:17 GMT
ENV LC_ALL=C.UTF-8
# Mon, 26 Jul 2021 23:08:17 GMT
ENV ROS_DISTRO=foxy
# Mon, 26 Jul 2021 23:08:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:09:00 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 26 Jul 2021 23:09:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 26 Jul 2021 23:09:00 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:09:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:09:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 26 Jul 2021 23:09:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 26 Jul 2021 23:09:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8145ea28ffd9b0942ba98116cde1e498e4572f6c665186683366584a32a0a9c0`  
		Last Modified: Mon, 26 Jul 2021 23:23:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb0e59f8a1856416b541915263ab8419535ec407203cdedec71cee7983a4f28`  
		Last Modified: Mon, 26 Jul 2021 23:23:37 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99638d27524b744be6c72b148745cecbd30fce62732e56202509249a739f015`  
		Last Modified: Mon, 26 Jul 2021 23:24:01 GMT  
		Size: 104.2 MB (104166106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0795de1605d5236fe906b0103be795fd0d5906337ac8e1219ab8680fc286d6cc`  
		Last Modified: Mon, 26 Jul 2021 23:23:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9212adaf308df7200d272b55747b777ee4c3f69fd8c33ed43a8cff46b456bcc`  
		Last Modified: Mon, 26 Jul 2021 23:24:25 GMT  
		Size: 65.2 MB (65183893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31858964d3495f929c4fbd43404976dce2b87c812a4a25b1a0c2c83dd29fddd`  
		Last Modified: Mon, 26 Jul 2021 23:24:14 GMT  
		Size: 238.5 KB (238481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c120cd143733715303fadf97c47bb4fc1cb0590feeb076c32ccfe7258ac90b`  
		Last Modified: Mon, 26 Jul 2021 23:24:14 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28758a874a9f9821a0fabd399ffae95818ddd755930e5b479087a3bd9b77b272`  
		Last Modified: Mon, 26 Jul 2021 23:24:16 GMT  
		Size: 9.3 MB (9298707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
