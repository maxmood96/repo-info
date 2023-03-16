## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:2337605c48a6ea19b9d569b3d4bc85bbbbecac1127043bcdfef8a413f2509abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c4da6b64514e027f09106cab7acaa3746284d0d087fc2aa5f9d388834bdace2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263050019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83850d460372907bedba817705c89514b0e188eaeb3c00d70817a6418018f6a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:23:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:23:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:23:53 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 16 Mar 2023 04:23:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 04:23:54 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 04:23:54 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 04:23:54 GMT
ENV ROS_DISTRO=humble
# Thu, 16 Mar 2023 04:25:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:25:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 16 Mar 2023 04:25:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 04:25:34 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 04:26:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:26:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 04:26:42 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 16 Mar 2023 04:27:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ad1f8f26857dba14fd27f7d8af8cd5f9ce4c25d5e4264090e4e33665838f4a`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 1.2 MB (1169612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af12f0c8d10d787a739ce0beb1339ad34542095ac563892b59872c9b9229991`  
		Last Modified: Thu, 16 Mar 2023 04:47:16 GMT  
		Size: 3.8 MB (3828398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4f122dfff7592e93555f020a3ba95ce2e1d60b0b138d39e444d80b29e1fdce`  
		Last Modified: Thu, 16 Mar 2023 04:47:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c195d49a74ea3cc9e44dd424ab6c5a62643eb9cc1fd60c335335d24eaee3fd`  
		Last Modified: Thu, 16 Mar 2023 04:47:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62e2d9c70cd1fb5cfb879150c7d04b63ab2922e154e11b0fd47031a52c16a5a`  
		Last Modified: Thu, 16 Mar 2023 04:47:31 GMT  
		Size: 106.3 MB (106343939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273cc0c60a3141d6e964d07b9ac39f9126b3d3ca36a70493cc8496448375fd55`  
		Last Modified: Thu, 16 Mar 2023 04:47:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0800e2c533d39c10eda1c33c4cc5e7d8c164ae5d620b68a5674ec6ff18427d`  
		Last Modified: Thu, 16 Mar 2023 04:47:54 GMT  
		Size: 97.9 MB (97887694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130e7a70d397d234ae4137584d1d00a5ddf4d23b258ecf856deeefab1fe664f5`  
		Last Modified: Thu, 16 Mar 2023 04:47:41 GMT  
		Size: 314.1 KB (314072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a79070b854f777682eb1cc3a62e2cf75029fdd5105fe7ed8e85a993ea5226c`  
		Last Modified: Thu, 16 Mar 2023 04:47:41 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cfb85e0aafffb281729a9c1323877d16e594d6ccd10b8d798b53c0925247c4`  
		Last Modified: Thu, 16 Mar 2023 04:47:45 GMT  
		Size: 23.1 MB (23071520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:13ae2d3f3fa2154db958fc4c4532d4eee94ad5d1032bcb774ef1fc7d368c4715
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255710392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fb575afde737ff6d46340ec65ce6e4e2d3c7f1ebfcfd6a664737d25684d802`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:25:57 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:26:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:26:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 16 Mar 2023 03:26:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 03:26:18 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 03:26:18 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 03:26:18 GMT
ENV ROS_DISTRO=humble
# Thu, 16 Mar 2023 03:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:28:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 16 Mar 2023 03:28:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 03:28:11 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 03:29:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:29:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 03:29:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 16 Mar 2023 03:30:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ebc1fa788322832bbed71ceadb3e11cb1a26969d4d664f7655a5b7c81c2b78`  
		Last Modified: Thu, 16 Mar 2023 03:49:34 GMT  
		Size: 1.2 MB (1169852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c0de312547c3fc66abbc624c4b248800ec78c0aab6b4fe6c072f35858664f`  
		Last Modified: Thu, 16 Mar 2023 03:49:32 GMT  
		Size: 3.8 MB (3800241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d8e2247bed14b878a035c112eb817cbee79740c938c0893cd55b231b58017e`  
		Last Modified: Thu, 16 Mar 2023 03:49:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d086fdc5697b9365d08f5b9dd61a33e2547c5a22618ae5481f9d6041447223`  
		Last Modified: Thu, 16 Mar 2023 03:49:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6453cb94f5370ccc175e0beb4b452635a97dfef6eaef28404383ac68f1f1c853`  
		Last Modified: Thu, 16 Mar 2023 03:49:48 GMT  
		Size: 104.1 MB (104059541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a36e33dee97e6c3aeef467124304049cb4ac734784ca6a719d90245fdfc3941`  
		Last Modified: Thu, 16 Mar 2023 03:49:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8eae9dc476ad24b977f846a349417e676ed533c003e58f7ee95949832a7602`  
		Last Modified: Thu, 16 Mar 2023 03:50:08 GMT  
		Size: 95.5 MB (95477291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666fc157dbdee31a004f825aa48bbd562084d77e3c4f6af8224ebf3454372bd9`  
		Last Modified: Thu, 16 Mar 2023 03:49:58 GMT  
		Size: 314.1 KB (314059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d637ed46ef3f6193062806be0d5578e4896c4814956f0b3430a6df02a081a9f`  
		Last Modified: Thu, 16 Mar 2023 03:49:58 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eba6bb0da5c90df9800c7413610aa12a00f284a53b94640965b45315cc062f1`  
		Last Modified: Thu, 16 Mar 2023 03:50:01 GMT  
		Size: 22.5 MB (22497013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
