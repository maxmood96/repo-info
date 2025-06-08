## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:c9d2f75092d231e91bb82bec267fe20955a4929890027feb453a4b08f489487d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:98f9e5f7859236b18f9d5956c211b1e65ecf2be0eecb7d5e1d7e1ea78af9d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238975790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffcc5430a28e01427c334f5dc1dc19cf3c71cb22a017b4741bfab6d53fe3e22`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945134a43cf5436bcd4c4fabbe5f8689d89a7e3813c2be30f673ddd81f849543`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 1.2 MB (1194815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddc9e11a6f24d45a0fd6c2fd537bb5c96fcfe7ad0f2a5534cc8f35938605463`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 5.4 MB (5363955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49802bd0654544e040c6c148afac52b1bc2758819ccf7844589f6ea1f8d42935`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4547639f65f5b71b189c02bc2917e674ef90e9b6aac3744e8961e9ae71488bc0`  
		Last Modified: Fri, 06 Jun 2025 22:49:32 GMT  
		Size: 109.2 MB (109184147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd6130c854a7c7deccae5be3df2133266053727e77edb5553b49a3f07c39cf8`  
		Last Modified: Sat, 07 Jun 2025 01:24:00 GMT  
		Size: 73.3 MB (73268699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92773102787c1ed83158d901c443a22e72710fd2821edf229d354302d9bb6589`  
		Last Modified: Fri, 06 Jun 2025 23:25:24 GMT  
		Size: 308.6 KB (308613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd060b418219001fd791439bf81ed5acda05148f2f046a379087a3659e4e07`  
		Last Modified: Fri, 06 Jun 2025 23:25:27 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b4106c64a336d4312d21c00493611465eda6a53262564b5789d93a322c8dcd`  
		Last Modified: Sat, 07 Jun 2025 01:23:56 GMT  
		Size: 22.1 MB (22138284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:b6d203e67d5964510ea58905e769ea3610c57338b8759e49541de4b399f62172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21772917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e255e579a924496a78e3a0b9c24bb53224f9c53a53f5012d77e3eb8f1a8039`

```dockerfile
```

-	Layers:
	-	`sha256:41c025e72d1e802ebc408a6d258c99ea6c3318a4927da14afb47025422cb5e65`  
		Last Modified: Sat, 07 Jun 2025 01:19:43 GMT  
		Size: 21.8 MB (21755730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20f696845da6b6223f1206047b3b3d059e483bf237a4341fcfbd2c7e7a0575c`  
		Last Modified: Sat, 07 Jun 2025 01:19:44 GMT  
		Size: 17.2 KB (17187 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eaedd5322112f1fb29519d09baf756a224d84e287455e6a8b5dbff053a356dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226604103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9792d43dba722882763614064989ed09b6ca0125ab49161f2051ad6cd7705a5a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c8192db141ffbb5140fe411c5eced3897890db3b1fcea32de47823cb1e9f5`  
		Last Modified: Fri, 06 Jun 2025 23:24:52 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d05758778f2814758f8af46ee68fc371f4c70c37e44d6667bd998a6a401889`  
		Last Modified: Sat, 07 Jun 2025 23:59:04 GMT  
		Size: 104.7 MB (104674775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d724ca4312a3680a73d9b733e052cdc81fc0456386fb1c596c2520fc09de111`  
		Last Modified: Fri, 06 Jun 2025 23:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75b490757b30dade46f2da5ace5d4729ad05bfce3c989747b9cc271a60d8696`  
		Last Modified: Sat, 07 Jun 2025 11:54:37 GMT  
		Size: 67.6 MB (67616740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f0fee2ade4717f94fb8fbca0c15d03895ca738793e29f7de8aa9122e3793e`  
		Last Modified: Sat, 07 Jun 2025 01:12:38 GMT  
		Size: 308.6 KB (308611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d1b759c544dc86e0206d68eb46690ce0bff76dbb7c93936c619d810f074c9`  
		Last Modified: Sat, 07 Jun 2025 01:12:41 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ab5088ca56b495d0591758e096786563c29f23898224f755dd1dab7398fac`  
		Last Modified: Sat, 07 Jun 2025 11:54:44 GMT  
		Size: 21.5 MB (21480630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:b474cae5bff3cb1f75e809fbf49e95a76e43a09f544121b0448388aa4ac65f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21793637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3746a18bfc50b6d25389611b5050dd370b3817c466b99140219a01d8c3fa8c5e`

```dockerfile
```

-	Layers:
	-	`sha256:464f23f22d6008437b37547ff8cfdeb68eef5764f21caaf5ad74ab98a9b664b2`  
		Last Modified: Sat, 07 Jun 2025 01:20:04 GMT  
		Size: 21.8 MB (21776313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a4879757c50c2079366e7fd0020cceb1f8ca7b673c7e8178057aaf539069bb`  
		Last Modified: Sat, 07 Jun 2025 01:20:05 GMT  
		Size: 17.3 KB (17324 bytes)  
		MIME: application/vnd.in-toto+json
