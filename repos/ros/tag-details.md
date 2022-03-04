<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:foxy`](#rosfoxy)
-	[`ros:foxy-ros-base`](#rosfoxy-ros-base)
-	[`ros:foxy-ros-base-focal`](#rosfoxy-ros-base-focal)
-	[`ros:foxy-ros-core`](#rosfoxy-ros-core)
-	[`ros:foxy-ros-core-focal`](#rosfoxy-ros-core-focal)
-	[`ros:foxy-ros1-bridge`](#rosfoxy-ros1-bridge)
-	[`ros:foxy-ros1-bridge-focal`](#rosfoxy-ros1-bridge-focal)
-	[`ros:galactic`](#rosgalactic)
-	[`ros:galactic-ros-base`](#rosgalactic-ros-base)
-	[`ros:galactic-ros-base-focal`](#rosgalactic-ros-base-focal)
-	[`ros:galactic-ros-core`](#rosgalactic-ros-core)
-	[`ros:galactic-ros-core-focal`](#rosgalactic-ros-core-focal)
-	[`ros:galactic-ros1-bridge`](#rosgalactic-ros1-bridge)
-	[`ros:galactic-ros1-bridge-focal`](#rosgalactic-ros1-bridge-focal)
-	[`ros:latest`](#roslatest)
-	[`ros:melodic`](#rosmelodic)
-	[`ros:melodic-perception`](#rosmelodic-perception)
-	[`ros:melodic-perception-bionic`](#rosmelodic-perception-bionic)
-	[`ros:melodic-robot`](#rosmelodic-robot)
-	[`ros:melodic-robot-bionic`](#rosmelodic-robot-bionic)
-	[`ros:melodic-ros-base`](#rosmelodic-ros-base)
-	[`ros:melodic-ros-base-bionic`](#rosmelodic-ros-base-bionic)
-	[`ros:melodic-ros-core`](#rosmelodic-ros-core)
-	[`ros:melodic-ros-core-bionic`](#rosmelodic-ros-core-bionic)
-	[`ros:noetic`](#rosnoetic)
-	[`ros:noetic-perception`](#rosnoetic-perception)
-	[`ros:noetic-perception-buster`](#rosnoetic-perception-buster)
-	[`ros:noetic-perception-focal`](#rosnoetic-perception-focal)
-	[`ros:noetic-robot`](#rosnoetic-robot)
-	[`ros:noetic-robot-buster`](#rosnoetic-robot-buster)
-	[`ros:noetic-robot-focal`](#rosnoetic-robot-focal)
-	[`ros:noetic-ros-base`](#rosnoetic-ros-base)
-	[`ros:noetic-ros-base-buster`](#rosnoetic-ros-base-buster)
-	[`ros:noetic-ros-base-focal`](#rosnoetic-ros-base-focal)
-	[`ros:noetic-ros-core`](#rosnoetic-ros-core)
-	[`ros:noetic-ros-core-buster`](#rosnoetic-ros-core-buster)
-	[`ros:noetic-ros-core-focal`](#rosnoetic-ros-core-focal)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-jammy`](#rosrolling-ros-base-jammy)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-jammy`](#rosrolling-ros-core-jammy)

## `ros:foxy`

```console
$ docker pull ros@sha256:930f40a5376c44cbab5530a2041fec5b5450923f5ef363a04b02807c824d2af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:babb22519610f12b1529494de563695c81150c28ff264c9f9cd4556f0bb7f4fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248188953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3806924aedd5638614fa27299cd797f8f5e40afc4227cd8eaa0adfb37d22e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:09:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:09:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbad41d04cdd4ef0ac30989e309c7b3c6e2195487617f6de0de31531e94f0e0`  
		Last Modified: Thu, 03 Mar 2022 23:26:26 GMT  
		Size: 70.9 MB (70858279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2334a170618fa03d191f1cd8e76fc82332385dc22bf836010ede2a8d3f3a8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 251.4 KB (251411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19351c10f0dc4c8c58bf2b0c669363804f1d9b92749d5edb3877509307285bc8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5cea3cbaf19126de5c75f225a7b897c0dc23588d0f04f627c7f54b8b6ccd16`  
		Last Modified: Thu, 03 Mar 2022 23:26:19 GMT  
		Size: 21.7 MB (21668565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cffe42f34f12f2cac99f2f639a0534db4e5096ee95ecf7f6b03a4f6e1f3e79dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223565751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1e3d028aba56486550927ccb43d05f309b5b914b733bdafe1510a90e652cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:28:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:28:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa316f1e52a8742158d7e022dfed33680c4467154b94a6516bd8eff84dabce86`  
		Last Modified: Thu, 03 Mar 2022 21:44:45 GMT  
		Size: 65.0 MB (64978916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259c8d5169fc4cfec7b5c89bec35869a21563e7fd7a75dafe4bf7d62a2a0276b`  
		Last Modified: Thu, 03 Mar 2022 21:44:35 GMT  
		Size: 251.4 KB (251357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77fb0b75c8c330b2dfb7c0039de9cc5b918cd16d1fb5dfe5ffcfa2d946d6cd`  
		Last Modified: Thu, 03 Mar 2022 21:44:36 GMT  
		Size: 2.2 KB (2157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d067c6b6ac7d13b7c8d6074e843f1bc10d0b956e77e1088ce78fdd2a237b380`  
		Last Modified: Thu, 03 Mar 2022 21:44:38 GMT  
		Size: 20.4 MB (20373551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:930f40a5376c44cbab5530a2041fec5b5450923f5ef363a04b02807c824d2af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:babb22519610f12b1529494de563695c81150c28ff264c9f9cd4556f0bb7f4fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248188953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3806924aedd5638614fa27299cd797f8f5e40afc4227cd8eaa0adfb37d22e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:09:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:09:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbad41d04cdd4ef0ac30989e309c7b3c6e2195487617f6de0de31531e94f0e0`  
		Last Modified: Thu, 03 Mar 2022 23:26:26 GMT  
		Size: 70.9 MB (70858279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2334a170618fa03d191f1cd8e76fc82332385dc22bf836010ede2a8d3f3a8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 251.4 KB (251411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19351c10f0dc4c8c58bf2b0c669363804f1d9b92749d5edb3877509307285bc8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5cea3cbaf19126de5c75f225a7b897c0dc23588d0f04f627c7f54b8b6ccd16`  
		Last Modified: Thu, 03 Mar 2022 23:26:19 GMT  
		Size: 21.7 MB (21668565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cffe42f34f12f2cac99f2f639a0534db4e5096ee95ecf7f6b03a4f6e1f3e79dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223565751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1e3d028aba56486550927ccb43d05f309b5b914b733bdafe1510a90e652cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:28:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:28:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa316f1e52a8742158d7e022dfed33680c4467154b94a6516bd8eff84dabce86`  
		Last Modified: Thu, 03 Mar 2022 21:44:45 GMT  
		Size: 65.0 MB (64978916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259c8d5169fc4cfec7b5c89bec35869a21563e7fd7a75dafe4bf7d62a2a0276b`  
		Last Modified: Thu, 03 Mar 2022 21:44:35 GMT  
		Size: 251.4 KB (251357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77fb0b75c8c330b2dfb7c0039de9cc5b918cd16d1fb5dfe5ffcfa2d946d6cd`  
		Last Modified: Thu, 03 Mar 2022 21:44:36 GMT  
		Size: 2.2 KB (2157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d067c6b6ac7d13b7c8d6074e843f1bc10d0b956e77e1088ce78fdd2a237b380`  
		Last Modified: Thu, 03 Mar 2022 21:44:38 GMT  
		Size: 20.4 MB (20373551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:930f40a5376c44cbab5530a2041fec5b5450923f5ef363a04b02807c824d2af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:babb22519610f12b1529494de563695c81150c28ff264c9f9cd4556f0bb7f4fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248188953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3806924aedd5638614fa27299cd797f8f5e40afc4227cd8eaa0adfb37d22e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:09:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:09:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbad41d04cdd4ef0ac30989e309c7b3c6e2195487617f6de0de31531e94f0e0`  
		Last Modified: Thu, 03 Mar 2022 23:26:26 GMT  
		Size: 70.9 MB (70858279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2334a170618fa03d191f1cd8e76fc82332385dc22bf836010ede2a8d3f3a8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 251.4 KB (251411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19351c10f0dc4c8c58bf2b0c669363804f1d9b92749d5edb3877509307285bc8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5cea3cbaf19126de5c75f225a7b897c0dc23588d0f04f627c7f54b8b6ccd16`  
		Last Modified: Thu, 03 Mar 2022 23:26:19 GMT  
		Size: 21.7 MB (21668565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cffe42f34f12f2cac99f2f639a0534db4e5096ee95ecf7f6b03a4f6e1f3e79dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223565751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1e3d028aba56486550927ccb43d05f309b5b914b733bdafe1510a90e652cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:28:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:28:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa316f1e52a8742158d7e022dfed33680c4467154b94a6516bd8eff84dabce86`  
		Last Modified: Thu, 03 Mar 2022 21:44:45 GMT  
		Size: 65.0 MB (64978916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259c8d5169fc4cfec7b5c89bec35869a21563e7fd7a75dafe4bf7d62a2a0276b`  
		Last Modified: Thu, 03 Mar 2022 21:44:35 GMT  
		Size: 251.4 KB (251357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77fb0b75c8c330b2dfb7c0039de9cc5b918cd16d1fb5dfe5ffcfa2d946d6cd`  
		Last Modified: Thu, 03 Mar 2022 21:44:36 GMT  
		Size: 2.2 KB (2157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d067c6b6ac7d13b7c8d6074e843f1bc10d0b956e77e1088ce78fdd2a237b380`  
		Last Modified: Thu, 03 Mar 2022 21:44:38 GMT  
		Size: 20.4 MB (20373551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:0548f9d944829e10ef9f2c248c7058b15e3802a4cc45093c78f00abaa0dad128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:17ee7b6a09e61ac31209bd962e35d49602fc8ecbb7211f7ab5e51980bda21240
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155408514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b65a6fce20400cf3f548ecf2dd6cd898e1b2bd4b64a31b229d2899224c7c26`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8ddbbbc88706185eb341a59dc460c0cc57732b46184aafe5c81e23f37fc49592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137959770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d0909c8afa62cd4df54ec32fbd3e75dd332eda799ec3632fa3e9940c208b45`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:0548f9d944829e10ef9f2c248c7058b15e3802a4cc45093c78f00abaa0dad128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:17ee7b6a09e61ac31209bd962e35d49602fc8ecbb7211f7ab5e51980bda21240
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155408514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b65a6fce20400cf3f548ecf2dd6cd898e1b2bd4b64a31b229d2899224c7c26`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8ddbbbc88706185eb341a59dc460c0cc57732b46184aafe5c81e23f37fc49592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137959770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d0909c8afa62cd4df54ec32fbd3e75dd332eda799ec3632fa3e9940c208b45`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:ef6398326083a99a10cfc1fd673822b90c94709f289a8a55d62870ae7703a9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:6a82ef6c322c9dcc744e97cb4d9963082d628b814f2c661b32acbbec17df4513
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346058199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9837fbe5b59081660925be593be0641db31c4d810097d704e6749878165e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:09:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:09:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 23:10:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:10:23 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 23:10:23 GMT
ENV ROS2_DISTRO=foxy
# Thu, 03 Mar 2022 23:10:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:57 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbad41d04cdd4ef0ac30989e309c7b3c6e2195487617f6de0de31531e94f0e0`  
		Last Modified: Thu, 03 Mar 2022 23:26:26 GMT  
		Size: 70.9 MB (70858279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2334a170618fa03d191f1cd8e76fc82332385dc22bf836010ede2a8d3f3a8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 251.4 KB (251411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19351c10f0dc4c8c58bf2b0c669363804f1d9b92749d5edb3877509307285bc8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5cea3cbaf19126de5c75f225a7b897c0dc23588d0f04f627c7f54b8b6ccd16`  
		Last Modified: Thu, 03 Mar 2022 23:26:19 GMT  
		Size: 21.7 MB (21668565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da4735eb0f83b7e7035ec5c2b795a45802eaa037f0396d7ce85bed3d974b46`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eac423a1ad520cfeaee1eb128a6c76cf8c96a5da4e2d639a1dae97441e8e5e4`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b15f5a81eed01b7221df719b0ae09c496f479919878cf653779190b846afce`  
		Last Modified: Thu, 03 Mar 2022 23:27:02 GMT  
		Size: 76.3 MB (76324495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d28e7e3b67e20f4905961c74a0a7bf08e737ccb31981aa0743a0ed3096473bd`  
		Last Modified: Thu, 03 Mar 2022 23:26:48 GMT  
		Size: 21.5 MB (21544127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec25e5b6d44635614eec05ea663ac517157327ef1e48387d7d8a7f67c18fc99b`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75a13f909d02eb9b215c141c79353f7a4477b2f8e2656e61060cfa7ce2a178d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313685609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb658bf3078b2e64b9bbe724ec4d13a6a339e94d93efc8794e4f3ede1ee9455e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:28:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:28:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:29:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:29:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:29:32 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 21:29:33 GMT
ENV ROS2_DISTRO=foxy
# Thu, 03 Mar 2022 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:30:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:30:33 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa316f1e52a8742158d7e022dfed33680c4467154b94a6516bd8eff84dabce86`  
		Last Modified: Thu, 03 Mar 2022 21:44:45 GMT  
		Size: 65.0 MB (64978916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259c8d5169fc4cfec7b5c89bec35869a21563e7fd7a75dafe4bf7d62a2a0276b`  
		Last Modified: Thu, 03 Mar 2022 21:44:35 GMT  
		Size: 251.4 KB (251357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77fb0b75c8c330b2dfb7c0039de9cc5b918cd16d1fb5dfe5ffcfa2d946d6cd`  
		Last Modified: Thu, 03 Mar 2022 21:44:36 GMT  
		Size: 2.2 KB (2157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d067c6b6ac7d13b7c8d6074e843f1bc10d0b956e77e1088ce78fdd2a237b380`  
		Last Modified: Thu, 03 Mar 2022 21:44:38 GMT  
		Size: 20.4 MB (20373551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c049479168ee5d90c70a2c94ba07d775e84624893e0891e3512c8746d3962f`  
		Last Modified: Thu, 03 Mar 2022 21:45:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276caa0dbe0e51c985df9653b22670ddd523c804857e5be2b479b21cb1edfb97`  
		Last Modified: Thu, 03 Mar 2022 21:45:18 GMT  
		Size: 76.2 MB (76154541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de33646892d7a0d39f2850d920d648c8c345dd4bca7c96cceef7ce88a9a56e8`  
		Last Modified: Thu, 03 Mar 2022 21:45:06 GMT  
		Size: 14.0 MB (13964844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ace697c4b9d045e3b333b61bbf06cc7a5985b40576f92dfe88e2b91b225738`  
		Last Modified: Thu, 03 Mar 2022 21:45:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:ef6398326083a99a10cfc1fd673822b90c94709f289a8a55d62870ae7703a9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:6a82ef6c322c9dcc744e97cb4d9963082d628b814f2c661b32acbbec17df4513
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346058199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9837fbe5b59081660925be593be0641db31c4d810097d704e6749878165e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:09:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:09:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 23:10:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:10:23 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 23:10:23 GMT
ENV ROS2_DISTRO=foxy
# Thu, 03 Mar 2022 23:10:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:10:57 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbad41d04cdd4ef0ac30989e309c7b3c6e2195487617f6de0de31531e94f0e0`  
		Last Modified: Thu, 03 Mar 2022 23:26:26 GMT  
		Size: 70.9 MB (70858279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2334a170618fa03d191f1cd8e76fc82332385dc22bf836010ede2a8d3f3a8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 251.4 KB (251411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19351c10f0dc4c8c58bf2b0c669363804f1d9b92749d5edb3877509307285bc8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5cea3cbaf19126de5c75f225a7b897c0dc23588d0f04f627c7f54b8b6ccd16`  
		Last Modified: Thu, 03 Mar 2022 23:26:19 GMT  
		Size: 21.7 MB (21668565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81da4735eb0f83b7e7035ec5c2b795a45802eaa037f0396d7ce85bed3d974b46`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eac423a1ad520cfeaee1eb128a6c76cf8c96a5da4e2d639a1dae97441e8e5e4`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b15f5a81eed01b7221df719b0ae09c496f479919878cf653779190b846afce`  
		Last Modified: Thu, 03 Mar 2022 23:27:02 GMT  
		Size: 76.3 MB (76324495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d28e7e3b67e20f4905961c74a0a7bf08e737ccb31981aa0743a0ed3096473bd`  
		Last Modified: Thu, 03 Mar 2022 23:26:48 GMT  
		Size: 21.5 MB (21544127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec25e5b6d44635614eec05ea663ac517157327ef1e48387d7d8a7f67c18fc99b`  
		Last Modified: Thu, 03 Mar 2022 23:26:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75a13f909d02eb9b215c141c79353f7a4477b2f8e2656e61060cfa7ce2a178d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313685609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb658bf3078b2e64b9bbe724ec4d13a6a339e94d93efc8794e4f3ede1ee9455e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:28:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:28:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:29:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:29:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:29:32 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 21:29:33 GMT
ENV ROS2_DISTRO=foxy
# Thu, 03 Mar 2022 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:30:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:30:33 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa316f1e52a8742158d7e022dfed33680c4467154b94a6516bd8eff84dabce86`  
		Last Modified: Thu, 03 Mar 2022 21:44:45 GMT  
		Size: 65.0 MB (64978916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259c8d5169fc4cfec7b5c89bec35869a21563e7fd7a75dafe4bf7d62a2a0276b`  
		Last Modified: Thu, 03 Mar 2022 21:44:35 GMT  
		Size: 251.4 KB (251357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77fb0b75c8c330b2dfb7c0039de9cc5b918cd16d1fb5dfe5ffcfa2d946d6cd`  
		Last Modified: Thu, 03 Mar 2022 21:44:36 GMT  
		Size: 2.2 KB (2157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d067c6b6ac7d13b7c8d6074e843f1bc10d0b956e77e1088ce78fdd2a237b380`  
		Last Modified: Thu, 03 Mar 2022 21:44:38 GMT  
		Size: 20.4 MB (20373551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c049479168ee5d90c70a2c94ba07d775e84624893e0891e3512c8746d3962f`  
		Last Modified: Thu, 03 Mar 2022 21:45:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276caa0dbe0e51c985df9653b22670ddd523c804857e5be2b479b21cb1edfb97`  
		Last Modified: Thu, 03 Mar 2022 21:45:18 GMT  
		Size: 76.2 MB (76154541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de33646892d7a0d39f2850d920d648c8c345dd4bca7c96cceef7ce88a9a56e8`  
		Last Modified: Thu, 03 Mar 2022 21:45:06 GMT  
		Size: 14.0 MB (13964844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ace697c4b9d045e3b333b61bbf06cc7a5985b40576f92dfe88e2b91b225738`  
		Last Modified: Thu, 03 Mar 2022 21:45:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic`

```console
$ docker pull ros@sha256:f4b9acb71de84ce81fff13dcd72c6328a2775fd1d001ba8d26683e4614344513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:eb083ea54e22b762f7b975fa333fddc4e2525fb3b7734d2cf56ed5e9ca0e9f9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232148547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a617c2bfaf537453dc2ee42b24750ee8b27625c2698e37582b0366117d53d4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:11:02 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:11:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:11:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:11:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:12:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b248cd64c64d8e30c5cb2f7ea8dbecb02fab8491c449e0048783e3c1205d124d`  
		Last Modified: Thu, 03 Mar 2022 23:27:34 GMT  
		Size: 103.7 MB (103667338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e15bc9621edeab205d7571ce463791887cabdc21b9e8e1ac5935a76ebb995`  
		Last Modified: Thu, 03 Mar 2022 23:27:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732c3e362fa680af3dd9651f9aec63ef06df9c94b1a1dd431f145c87d748f54`  
		Last Modified: Thu, 03 Mar 2022 23:27:56 GMT  
		Size: 70.8 MB (70810157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701903a724365f87cb60a32b5451bd9fd1cb50c2e4dee6654808a8feb0f2e8f`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 259.1 KB (259109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752acc754cec460fa8bcbdba673e5550046741728000255b0703d7452f6536fe`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 2.2 KB (2197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3863acee3e82cec893523789175d85445eb3c8b9cb65be831fda3921510ed3`  
		Last Modified: Thu, 03 Mar 2022 23:27:49 GMT  
		Size: 22.1 MB (22112701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e3536f4ba82a271420615511b0998090c878b327508224863f23b9f3bdf4d479
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220354717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7ce76856307133568701aa1ef066573428c9f3cbd069ff0c201e7971f190d8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:30:49 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 21:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:31:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:31:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:31:43 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:32:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:32:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74ba87af23be8f4aafd5c8302b2c467c2e6e67b9794d06802e60b060e39bfd`  
		Last Modified: Thu, 03 Mar 2022 21:45:48 GMT  
		Size: 100.0 MB (100046542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c4b0afbfb88a5779d6abf06adb29ca9d54b62d91ea159930e32462307ceea4`  
		Last Modified: Thu, 03 Mar 2022 21:45:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345c2a2a8a38fcc2d0b77b5163370614cc12f1b4ea4d4ad4788daf63b495e62d`  
		Last Modified: Thu, 03 Mar 2022 21:46:09 GMT  
		Size: 64.9 MB (64933636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aceb2a5ab9c6f59cd0a5078300dc2090bc5bca6d071cd804997dce357ee33d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 259.1 KB (259066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fcb9bad2c4037cdb5644f47bcf33538409d201e1138610e734d9f92899033d`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c97bb6461d23f7baa16c6659051576ee711edb2c04d350122e94eec49fa15af`  
		Last Modified: Thu, 03 Mar 2022 21:46:03 GMT  
		Size: 21.4 MB (21435107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:f4b9acb71de84ce81fff13dcd72c6328a2775fd1d001ba8d26683e4614344513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:eb083ea54e22b762f7b975fa333fddc4e2525fb3b7734d2cf56ed5e9ca0e9f9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232148547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a617c2bfaf537453dc2ee42b24750ee8b27625c2698e37582b0366117d53d4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:11:02 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:11:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:11:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:11:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:12:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b248cd64c64d8e30c5cb2f7ea8dbecb02fab8491c449e0048783e3c1205d124d`  
		Last Modified: Thu, 03 Mar 2022 23:27:34 GMT  
		Size: 103.7 MB (103667338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e15bc9621edeab205d7571ce463791887cabdc21b9e8e1ac5935a76ebb995`  
		Last Modified: Thu, 03 Mar 2022 23:27:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732c3e362fa680af3dd9651f9aec63ef06df9c94b1a1dd431f145c87d748f54`  
		Last Modified: Thu, 03 Mar 2022 23:27:56 GMT  
		Size: 70.8 MB (70810157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701903a724365f87cb60a32b5451bd9fd1cb50c2e4dee6654808a8feb0f2e8f`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 259.1 KB (259109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752acc754cec460fa8bcbdba673e5550046741728000255b0703d7452f6536fe`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 2.2 KB (2197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3863acee3e82cec893523789175d85445eb3c8b9cb65be831fda3921510ed3`  
		Last Modified: Thu, 03 Mar 2022 23:27:49 GMT  
		Size: 22.1 MB (22112701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e3536f4ba82a271420615511b0998090c878b327508224863f23b9f3bdf4d479
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220354717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7ce76856307133568701aa1ef066573428c9f3cbd069ff0c201e7971f190d8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:30:49 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 21:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:31:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:31:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:31:43 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:32:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:32:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74ba87af23be8f4aafd5c8302b2c467c2e6e67b9794d06802e60b060e39bfd`  
		Last Modified: Thu, 03 Mar 2022 21:45:48 GMT  
		Size: 100.0 MB (100046542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c4b0afbfb88a5779d6abf06adb29ca9d54b62d91ea159930e32462307ceea4`  
		Last Modified: Thu, 03 Mar 2022 21:45:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345c2a2a8a38fcc2d0b77b5163370614cc12f1b4ea4d4ad4788daf63b495e62d`  
		Last Modified: Thu, 03 Mar 2022 21:46:09 GMT  
		Size: 64.9 MB (64933636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aceb2a5ab9c6f59cd0a5078300dc2090bc5bca6d071cd804997dce357ee33d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 259.1 KB (259066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fcb9bad2c4037cdb5644f47bcf33538409d201e1138610e734d9f92899033d`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c97bb6461d23f7baa16c6659051576ee711edb2c04d350122e94eec49fa15af`  
		Last Modified: Thu, 03 Mar 2022 21:46:03 GMT  
		Size: 21.4 MB (21435107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:f4b9acb71de84ce81fff13dcd72c6328a2775fd1d001ba8d26683e4614344513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:eb083ea54e22b762f7b975fa333fddc4e2525fb3b7734d2cf56ed5e9ca0e9f9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232148547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a617c2bfaf537453dc2ee42b24750ee8b27625c2698e37582b0366117d53d4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:11:02 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:11:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:11:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:11:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:12:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b248cd64c64d8e30c5cb2f7ea8dbecb02fab8491c449e0048783e3c1205d124d`  
		Last Modified: Thu, 03 Mar 2022 23:27:34 GMT  
		Size: 103.7 MB (103667338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e15bc9621edeab205d7571ce463791887cabdc21b9e8e1ac5935a76ebb995`  
		Last Modified: Thu, 03 Mar 2022 23:27:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732c3e362fa680af3dd9651f9aec63ef06df9c94b1a1dd431f145c87d748f54`  
		Last Modified: Thu, 03 Mar 2022 23:27:56 GMT  
		Size: 70.8 MB (70810157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701903a724365f87cb60a32b5451bd9fd1cb50c2e4dee6654808a8feb0f2e8f`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 259.1 KB (259109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752acc754cec460fa8bcbdba673e5550046741728000255b0703d7452f6536fe`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 2.2 KB (2197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3863acee3e82cec893523789175d85445eb3c8b9cb65be831fda3921510ed3`  
		Last Modified: Thu, 03 Mar 2022 23:27:49 GMT  
		Size: 22.1 MB (22112701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e3536f4ba82a271420615511b0998090c878b327508224863f23b9f3bdf4d479
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220354717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7ce76856307133568701aa1ef066573428c9f3cbd069ff0c201e7971f190d8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:30:49 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 21:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:31:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:31:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:31:43 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:32:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:32:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74ba87af23be8f4aafd5c8302b2c467c2e6e67b9794d06802e60b060e39bfd`  
		Last Modified: Thu, 03 Mar 2022 21:45:48 GMT  
		Size: 100.0 MB (100046542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c4b0afbfb88a5779d6abf06adb29ca9d54b62d91ea159930e32462307ceea4`  
		Last Modified: Thu, 03 Mar 2022 21:45:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345c2a2a8a38fcc2d0b77b5163370614cc12f1b4ea4d4ad4788daf63b495e62d`  
		Last Modified: Thu, 03 Mar 2022 21:46:09 GMT  
		Size: 64.9 MB (64933636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aceb2a5ab9c6f59cd0a5078300dc2090bc5bca6d071cd804997dce357ee33d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 259.1 KB (259066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fcb9bad2c4037cdb5644f47bcf33538409d201e1138610e734d9f92899033d`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c97bb6461d23f7baa16c6659051576ee711edb2c04d350122e94eec49fa15af`  
		Last Modified: Thu, 03 Mar 2022 21:46:03 GMT  
		Size: 21.4 MB (21435107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:66a18b035d68e46eba50d4dec1102b62252adc7b00d47ce838622cb52967184b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:67d91e396edf8e878ac9f8a9d47964e89be1bb7375726b85d0f4bed45ac259ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138964383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c143344161d2c38b77eca29ce65e79dded382cb6f18d0726fdbb9468ae4d2011`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:11:02 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:11:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:11:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:11:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b248cd64c64d8e30c5cb2f7ea8dbecb02fab8491c449e0048783e3c1205d124d`  
		Last Modified: Thu, 03 Mar 2022 23:27:34 GMT  
		Size: 103.7 MB (103667338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e15bc9621edeab205d7571ce463791887cabdc21b9e8e1ac5935a76ebb995`  
		Last Modified: Thu, 03 Mar 2022 23:27:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b194504a6a51a87bf2dea767db5161a1ff7187817eabf92702469d5ca7da86a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133724769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f876b0d35877d9d3e035f4891757721a64371d0fa2724b217f4b16cf2459a53`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:30:49 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 21:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:31:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:31:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:31:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74ba87af23be8f4aafd5c8302b2c467c2e6e67b9794d06802e60b060e39bfd`  
		Last Modified: Thu, 03 Mar 2022 21:45:48 GMT  
		Size: 100.0 MB (100046542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c4b0afbfb88a5779d6abf06adb29ca9d54b62d91ea159930e32462307ceea4`  
		Last Modified: Thu, 03 Mar 2022 21:45:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:66a18b035d68e46eba50d4dec1102b62252adc7b00d47ce838622cb52967184b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:67d91e396edf8e878ac9f8a9d47964e89be1bb7375726b85d0f4bed45ac259ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138964383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c143344161d2c38b77eca29ce65e79dded382cb6f18d0726fdbb9468ae4d2011`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:11:02 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:11:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:11:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:11:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b248cd64c64d8e30c5cb2f7ea8dbecb02fab8491c449e0048783e3c1205d124d`  
		Last Modified: Thu, 03 Mar 2022 23:27:34 GMT  
		Size: 103.7 MB (103667338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e15bc9621edeab205d7571ce463791887cabdc21b9e8e1ac5935a76ebb995`  
		Last Modified: Thu, 03 Mar 2022 23:27:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b194504a6a51a87bf2dea767db5161a1ff7187817eabf92702469d5ca7da86a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133724769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f876b0d35877d9d3e035f4891757721a64371d0fa2724b217f4b16cf2459a53`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:30:49 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 21:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:31:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:31:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:31:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74ba87af23be8f4aafd5c8302b2c467c2e6e67b9794d06802e60b060e39bfd`  
		Last Modified: Thu, 03 Mar 2022 21:45:48 GMT  
		Size: 100.0 MB (100046542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c4b0afbfb88a5779d6abf06adb29ca9d54b62d91ea159930e32462307ceea4`  
		Last Modified: Thu, 03 Mar 2022 21:45:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:e8423998a53717145f0fdd7f6490fcc32803ae304e9968ad6b333a66a504fc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:27a670666d8ccff4e83882b79f9867abd92d98910475a9f2f62cfad1ebf45b5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327118570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aafcbea07b171b4f69586b3745f9b45c50da133bcf370ad143a186e6f27ac6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:11:02 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:11:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:11:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:11:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:12:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 23:13:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:13:12 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 23:13:12 GMT
ENV ROS2_DISTRO=galactic
# Thu, 03 Mar 2022 23:13:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:13:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:13:45 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b248cd64c64d8e30c5cb2f7ea8dbecb02fab8491c449e0048783e3c1205d124d`  
		Last Modified: Thu, 03 Mar 2022 23:27:34 GMT  
		Size: 103.7 MB (103667338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e15bc9621edeab205d7571ce463791887cabdc21b9e8e1ac5935a76ebb995`  
		Last Modified: Thu, 03 Mar 2022 23:27:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732c3e362fa680af3dd9651f9aec63ef06df9c94b1a1dd431f145c87d748f54`  
		Last Modified: Thu, 03 Mar 2022 23:27:56 GMT  
		Size: 70.8 MB (70810157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701903a724365f87cb60a32b5451bd9fd1cb50c2e4dee6654808a8feb0f2e8f`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 259.1 KB (259109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752acc754cec460fa8bcbdba673e5550046741728000255b0703d7452f6536fe`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 2.2 KB (2197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3863acee3e82cec893523789175d85445eb3c8b9cb65be831fda3921510ed3`  
		Last Modified: Thu, 03 Mar 2022 23:27:49 GMT  
		Size: 22.1 MB (22112701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e7b46e5b5f113985bacb845856e85d14963d36d088ceaa252db41356811896`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8138ddd0a976f036fb80071ba323cba6da065e2558abc4db3df504995762de6`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cca671b57fb188baee96041b23f929cba69e33bf3a2ea94411119dec659f6e2`  
		Last Modified: Thu, 03 Mar 2022 23:28:29 GMT  
		Size: 78.6 MB (78598774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaab2677aec32303bba20adc1ec9701c5032f47334ac1e5ea197dddf17f1aa31`  
		Last Modified: Thu, 03 Mar 2022 23:28:14 GMT  
		Size: 16.4 MB (16370626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c08b09b5b4a5ca6937134a3af1433aae5df635fc9254b400c7c2c8fb7ac715`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:410823f474c93353c212c190f415e4a0e1301610fc7a1272cb74cb4047035703
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314348568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a5389ec8da4846fd1dae53e6425e1dd4244a2a37365e008f1c8d99a9f9e86a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:30:49 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 21:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:31:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:31:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:31:43 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:32:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:32:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:52 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:33:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:33:23 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 21:33:25 GMT
ENV ROS2_DISTRO=galactic
# Thu, 03 Mar 2022 21:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:16 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74ba87af23be8f4aafd5c8302b2c467c2e6e67b9794d06802e60b060e39bfd`  
		Last Modified: Thu, 03 Mar 2022 21:45:48 GMT  
		Size: 100.0 MB (100046542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c4b0afbfb88a5779d6abf06adb29ca9d54b62d91ea159930e32462307ceea4`  
		Last Modified: Thu, 03 Mar 2022 21:45:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345c2a2a8a38fcc2d0b77b5163370614cc12f1b4ea4d4ad4788daf63b495e62d`  
		Last Modified: Thu, 03 Mar 2022 21:46:09 GMT  
		Size: 64.9 MB (64933636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aceb2a5ab9c6f59cd0a5078300dc2090bc5bca6d071cd804997dce357ee33d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 259.1 KB (259066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fcb9bad2c4037cdb5644f47bcf33538409d201e1138610e734d9f92899033d`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c97bb6461d23f7baa16c6659051576ee711edb2c04d350122e94eec49fa15af`  
		Last Modified: Thu, 03 Mar 2022 21:46:03 GMT  
		Size: 21.4 MB (21435107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fab5e336e5e39a97b55eb611e6a9a384dfd59d4b0a3b6233a8cd8b28d8cc0d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6830c0744c85b7f4dedaf77d774a3e56a947aff0a8038943ef82f3ee3151d7`  
		Last Modified: Thu, 03 Mar 2022 21:46:39 GMT  
		Size: 78.3 MB (78323318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d6996295c1690911f8f20370aab626e914d0617128bcfd8ea7f61318620e3`  
		Last Modified: Thu, 03 Mar 2022 21:46:27 GMT  
		Size: 15.7 MB (15670064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e92b1df749ade68a89f261301805003060e300745185b6f9a12e2cf32f3d52`  
		Last Modified: Thu, 03 Mar 2022 21:46:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:e8423998a53717145f0fdd7f6490fcc32803ae304e9968ad6b333a66a504fc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:27a670666d8ccff4e83882b79f9867abd92d98910475a9f2f62cfad1ebf45b5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327118570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aafcbea07b171b4f69586b3745f9b45c50da133bcf370ad143a186e6f27ac6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:11:02 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 23:11:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:11:43 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:11:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:11:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:12:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:12:15 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:12:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:12:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 23:13:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:13:12 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 23:13:12 GMT
ENV ROS2_DISTRO=galactic
# Thu, 03 Mar 2022 23:13:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:13:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:13:45 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b248cd64c64d8e30c5cb2f7ea8dbecb02fab8491c449e0048783e3c1205d124d`  
		Last Modified: Thu, 03 Mar 2022 23:27:34 GMT  
		Size: 103.7 MB (103667338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4e15bc9621edeab205d7571ce463791887cabdc21b9e8e1ac5935a76ebb995`  
		Last Modified: Thu, 03 Mar 2022 23:27:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732c3e362fa680af3dd9651f9aec63ef06df9c94b1a1dd431f145c87d748f54`  
		Last Modified: Thu, 03 Mar 2022 23:27:56 GMT  
		Size: 70.8 MB (70810157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701903a724365f87cb60a32b5451bd9fd1cb50c2e4dee6654808a8feb0f2e8f`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 259.1 KB (259109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752acc754cec460fa8bcbdba673e5550046741728000255b0703d7452f6536fe`  
		Last Modified: Thu, 03 Mar 2022 23:27:45 GMT  
		Size: 2.2 KB (2197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3863acee3e82cec893523789175d85445eb3c8b9cb65be831fda3921510ed3`  
		Last Modified: Thu, 03 Mar 2022 23:27:49 GMT  
		Size: 22.1 MB (22112701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e7b46e5b5f113985bacb845856e85d14963d36d088ceaa252db41356811896`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8138ddd0a976f036fb80071ba323cba6da065e2558abc4db3df504995762de6`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cca671b57fb188baee96041b23f929cba69e33bf3a2ea94411119dec659f6e2`  
		Last Modified: Thu, 03 Mar 2022 23:28:29 GMT  
		Size: 78.6 MB (78598774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaab2677aec32303bba20adc1ec9701c5032f47334ac1e5ea197dddf17f1aa31`  
		Last Modified: Thu, 03 Mar 2022 23:28:14 GMT  
		Size: 16.4 MB (16370626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c08b09b5b4a5ca6937134a3af1433aae5df635fc9254b400c7c2c8fb7ac715`  
		Last Modified: Thu, 03 Mar 2022 23:28:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:410823f474c93353c212c190f415e4a0e1301610fc7a1272cb74cb4047035703
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314348568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a5389ec8da4846fd1dae53e6425e1dd4244a2a37365e008f1c8d99a9f9e86a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:30:49 GMT
ENV ROS_DISTRO=galactic
# Thu, 03 Mar 2022 21:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:31:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:31:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:31:43 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:32:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:32:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:32:52 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:33:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:33:23 GMT
ENV ROS1_DISTRO=noetic
# Thu, 03 Mar 2022 21:33:25 GMT
ENV ROS2_DISTRO=galactic
# Thu, 03 Mar 2022 21:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:16 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f74ba87af23be8f4aafd5c8302b2c467c2e6e67b9794d06802e60b060e39bfd`  
		Last Modified: Thu, 03 Mar 2022 21:45:48 GMT  
		Size: 100.0 MB (100046542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c4b0afbfb88a5779d6abf06adb29ca9d54b62d91ea159930e32462307ceea4`  
		Last Modified: Thu, 03 Mar 2022 21:45:30 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345c2a2a8a38fcc2d0b77b5163370614cc12f1b4ea4d4ad4788daf63b495e62d`  
		Last Modified: Thu, 03 Mar 2022 21:46:09 GMT  
		Size: 64.9 MB (64933636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aceb2a5ab9c6f59cd0a5078300dc2090bc5bca6d071cd804997dce357ee33d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 259.1 KB (259066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70fcb9bad2c4037cdb5644f47bcf33538409d201e1138610e734d9f92899033d`  
		Last Modified: Thu, 03 Mar 2022 21:46:00 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c97bb6461d23f7baa16c6659051576ee711edb2c04d350122e94eec49fa15af`  
		Last Modified: Thu, 03 Mar 2022 21:46:03 GMT  
		Size: 21.4 MB (21435107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fab5e336e5e39a97b55eb611e6a9a384dfd59d4b0a3b6233a8cd8b28d8cc0d3`  
		Last Modified: Thu, 03 Mar 2022 21:46:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6830c0744c85b7f4dedaf77d774a3e56a947aff0a8038943ef82f3ee3151d7`  
		Last Modified: Thu, 03 Mar 2022 21:46:39 GMT  
		Size: 78.3 MB (78323318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d6996295c1690911f8f20370aab626e914d0617128bcfd8ea7f61318620e3`  
		Last Modified: Thu, 03 Mar 2022 21:46:27 GMT  
		Size: 15.7 MB (15670064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e92b1df749ade68a89f261301805003060e300745185b6f9a12e2cf32f3d52`  
		Last Modified: Thu, 03 Mar 2022 21:46:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:930f40a5376c44cbab5530a2041fec5b5450923f5ef363a04b02807c824d2af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:babb22519610f12b1529494de563695c81150c28ff264c9f9cd4556f0bb7f4fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248188953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3806924aedd5638614fa27299cd797f8f5e40afc4227cd8eaa0adfb37d22e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:08:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:08:05 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 23:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:06 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:09:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:09:06 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:09:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:09:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:09:53 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:10:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45822bee284f286c1b9017d8c0340898db77e55d45413118e56c846dfe2337`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd6796769d2993930b0cda49dd5ee84077832c58fdeeca4faf0b49e2e5d4aa`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb466a19e5d71cadc5ac106348f67794f1a6edf85f5469548dc348c3c5fdde`  
		Last Modified: Thu, 03 Mar 2022 23:26:04 GMT  
		Size: 120.1 MB (120111469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d2bf34444dcb4cc481a44d5aeda5be8969cb83307a807e99ad07f27043d5a5`  
		Last Modified: Thu, 03 Mar 2022 23:25:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbad41d04cdd4ef0ac30989e309c7b3c6e2195487617f6de0de31531e94f0e0`  
		Last Modified: Thu, 03 Mar 2022 23:26:26 GMT  
		Size: 70.9 MB (70858279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb2334a170618fa03d191f1cd8e76fc82332385dc22bf836010ede2a8d3f3a8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 251.4 KB (251411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19351c10f0dc4c8c58bf2b0c669363804f1d9b92749d5edb3877509307285bc8`  
		Last Modified: Thu, 03 Mar 2022 23:26:15 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5cea3cbaf19126de5c75f225a7b897c0dc23588d0f04f627c7f54b8b6ccd16`  
		Last Modified: Thu, 03 Mar 2022 23:26:19 GMT  
		Size: 21.7 MB (21668565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cffe42f34f12f2cac99f2f639a0534db4e5096ee95ecf7f6b03a4f6e1f3e79dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223565751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c1e3d028aba56486550927ccb43d05f309b5b914b733bdafe1510a90e652cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:27:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:27:02 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:27:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:27:04 GMT
ENV ROS_DISTRO=foxy
# Thu, 03 Mar 2022 21:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:27:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:27:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:27:57 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:28:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:28:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:29:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a17f465ff68c2d550aacbdc48bedd15f82396a4e7686299c85063d4b8b20938`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4e94e576ea3dc0401e941f94bc00fcb465eba4c5dd5155d8fbcd852119ed0`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e9b235b54d9f3d3f87e423bd03406ef9b8ae2902cb273df86b1fd1ecab1cf1`  
		Last Modified: Thu, 03 Mar 2022 21:44:21 GMT  
		Size: 104.3 MB (104281543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c404730aa3dbad019440ed84d064c62054e142241ea05aa3bbc22eeb1f618b`  
		Last Modified: Thu, 03 Mar 2022 21:44:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa316f1e52a8742158d7e022dfed33680c4467154b94a6516bd8eff84dabce86`  
		Last Modified: Thu, 03 Mar 2022 21:44:45 GMT  
		Size: 65.0 MB (64978916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259c8d5169fc4cfec7b5c89bec35869a21563e7fd7a75dafe4bf7d62a2a0276b`  
		Last Modified: Thu, 03 Mar 2022 21:44:35 GMT  
		Size: 251.4 KB (251357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77fb0b75c8c330b2dfb7c0039de9cc5b918cd16d1fb5dfe5ffcfa2d946d6cd`  
		Last Modified: Thu, 03 Mar 2022 21:44:36 GMT  
		Size: 2.2 KB (2157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d067c6b6ac7d13b7c8d6074e843f1bc10d0b956e77e1088ce78fdd2a237b380`  
		Last Modified: Thu, 03 Mar 2022 21:44:38 GMT  
		Size: 20.4 MB (20373551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic`

```console
$ docker pull ros@sha256:f72486be3c09d539e3dd61144de6ac5b2e83a8942f53d2f382ad43d33f8125c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:db32264c05d9a644cb3d824c53f58925f6bc2a9a20cf906400136712fffc7e64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437400143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07b45da64ef12de4aa8a95490faff003d1b0e2fd1bb34b725a2a7736d4f0719`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:527edd5cb53dda632d40f47b024ef6c14c249e67293604c1034b8f621dafa4ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385890767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21394d3b4c786ff653a964f7dab4509dc78cbb489a7c17258bc1dac8ac6d1a1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aed820f4237dbd767f9d71944780cc89346127cdfe2c63ca5d2211f555866220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411547352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c8ad27d9dbc3d3329751a3c83aa314989729f01071e231f59ac9c938a12e4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:17:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:18:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908fc1da6687829639272ef87642b5189b703086a36418bd251644d6cf90a838`  
		Last Modified: Thu, 03 Mar 2022 21:39:54 GMT  
		Size: 63.1 MB (63067275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80f61cfdf9250e18c6dde75bca8870207161d0f38c1ef62f5505293cf93b3b`  
		Last Modified: Thu, 03 Mar 2022 21:39:46 GMT  
		Size: 277.3 KB (277339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e820e23ff014d59bcfd20cb2799ec78174c68fb17f14b25296ab734d5d103`  
		Last Modified: Thu, 03 Mar 2022 21:39:56 GMT  
		Size: 67.0 MB (67002031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception`

```console
$ docker pull ros@sha256:325961f6bcfc69fc475eb7bf88fd6a5abab589f04359f65e04b57a2d711a460d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:e4706211e9fb242a325422ca078700b9b4acd3c9fcba786379e524df63fdbe77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.7 MB (742726447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f653c3f29d5782e426aba9f3174eca54428737a5c0da8219d001ed64b6dd707`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:53:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ca478d4105a8544fb086f107bc416fb0bfb1e1cc29001d54364b46a16bc30f`  
		Last Modified: Thu, 03 Mar 2022 23:22:25 GMT  
		Size: 305.3 MB (305326304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:d43d5c41b41717048affa0892c8db8cbd25ce32d65b36e27943ce3d59c19bb67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.9 MB (645924814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b68e7d0472c6483050fbe4040087d00f0240dadb059b281234291a3620d1a11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd351a11d70b7c3033838cb428bd245dea197cdebf6b8ebbda529b168b2e480f`  
		Last Modified: Wed, 02 Feb 2022 03:37:56 GMT  
		Size: 260.0 MB (260034047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ce08498d3cb0f1969d59966cc27df17edf536f29eddcf5195863f31ddbb4fd81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702930095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2039c59e0e453f7e3ca33b865b74345df3211928fa60860b192b42c703c728`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:17:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:18:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:20:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908fc1da6687829639272ef87642b5189b703086a36418bd251644d6cf90a838`  
		Last Modified: Thu, 03 Mar 2022 21:39:54 GMT  
		Size: 63.1 MB (63067275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80f61cfdf9250e18c6dde75bca8870207161d0f38c1ef62f5505293cf93b3b`  
		Last Modified: Thu, 03 Mar 2022 21:39:46 GMT  
		Size: 277.3 KB (277339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e820e23ff014d59bcfd20cb2799ec78174c68fb17f14b25296ab734d5d103`  
		Last Modified: Thu, 03 Mar 2022 21:39:56 GMT  
		Size: 67.0 MB (67002031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc8a5a5820075f89c0df2b87c043e2fdb390f7d1f3e467101ef371bfae50c43`  
		Last Modified: Thu, 03 Mar 2022 21:41:08 GMT  
		Size: 291.4 MB (291382743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:325961f6bcfc69fc475eb7bf88fd6a5abab589f04359f65e04b57a2d711a460d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:e4706211e9fb242a325422ca078700b9b4acd3c9fcba786379e524df63fdbe77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.7 MB (742726447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f653c3f29d5782e426aba9f3174eca54428737a5c0da8219d001ed64b6dd707`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:53:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ca478d4105a8544fb086f107bc416fb0bfb1e1cc29001d54364b46a16bc30f`  
		Last Modified: Thu, 03 Mar 2022 23:22:25 GMT  
		Size: 305.3 MB (305326304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:d43d5c41b41717048affa0892c8db8cbd25ce32d65b36e27943ce3d59c19bb67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.9 MB (645924814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b68e7d0472c6483050fbe4040087d00f0240dadb059b281234291a3620d1a11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd351a11d70b7c3033838cb428bd245dea197cdebf6b8ebbda529b168b2e480f`  
		Last Modified: Wed, 02 Feb 2022 03:37:56 GMT  
		Size: 260.0 MB (260034047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ce08498d3cb0f1969d59966cc27df17edf536f29eddcf5195863f31ddbb4fd81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702930095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2039c59e0e453f7e3ca33b865b74345df3211928fa60860b192b42c703c728`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:17:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:18:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:20:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908fc1da6687829639272ef87642b5189b703086a36418bd251644d6cf90a838`  
		Last Modified: Thu, 03 Mar 2022 21:39:54 GMT  
		Size: 63.1 MB (63067275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80f61cfdf9250e18c6dde75bca8870207161d0f38c1ef62f5505293cf93b3b`  
		Last Modified: Thu, 03 Mar 2022 21:39:46 GMT  
		Size: 277.3 KB (277339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e820e23ff014d59bcfd20cb2799ec78174c68fb17f14b25296ab734d5d103`  
		Last Modified: Thu, 03 Mar 2022 21:39:56 GMT  
		Size: 67.0 MB (67002031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc8a5a5820075f89c0df2b87c043e2fdb390f7d1f3e467101ef371bfae50c43`  
		Last Modified: Thu, 03 Mar 2022 21:41:08 GMT  
		Size: 291.4 MB (291382743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot`

```console
$ docker pull ros@sha256:dcd4db432562a1b5333dc9288542c2ba35fc6ae7e67ea2affe53eb35896e12a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:d2ae6094a89afad254aa5ea418551f845cd01230cb1278a65027707c0a569962
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448482378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ae7023f2ec792e3ee143428c1f2ea0f62d2bdeb057093003e8f58e20b73be`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:47:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf2234c2d9148450317f62d9d62fbf420f271a1d80346b40848fe1c82b463ac`  
		Last Modified: Thu, 03 Mar 2022 23:21:23 GMT  
		Size: 11.1 MB (11082235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:80356ffe0b31b1ce87d70e3ef62ade22cc00dc6d400060e0e8de30d9775d83d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396013110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c1fa5010e397d2fb24ce8d8818df5556f09ea81dceec5fdf91c02b7248881`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:08:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d4d1894d4d4734259ce4328e795671cde30e59717a29ccce3e64de9197c6bc`  
		Last Modified: Wed, 02 Feb 2022 03:35:00 GMT  
		Size: 10.1 MB (10122343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ac5bb37c87d69ac097dbe2f19310de8cb89bf8260c9c395fcfaa01e288975f81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422280318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667daf428f2d4f8cf5143f41531e203424dc27a0726fbce6eb3173bd36e4697b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:17:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:18:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:19:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908fc1da6687829639272ef87642b5189b703086a36418bd251644d6cf90a838`  
		Last Modified: Thu, 03 Mar 2022 21:39:54 GMT  
		Size: 63.1 MB (63067275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80f61cfdf9250e18c6dde75bca8870207161d0f38c1ef62f5505293cf93b3b`  
		Last Modified: Thu, 03 Mar 2022 21:39:46 GMT  
		Size: 277.3 KB (277339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e820e23ff014d59bcfd20cb2799ec78174c68fb17f14b25296ab734d5d103`  
		Last Modified: Thu, 03 Mar 2022 21:39:56 GMT  
		Size: 67.0 MB (67002031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290e23f3297761c3a8f5d737f183e68c2053dd1bc8a89cf47b0196d8815df9c1`  
		Last Modified: Thu, 03 Mar 2022 21:40:13 GMT  
		Size: 10.7 MB (10732966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:dcd4db432562a1b5333dc9288542c2ba35fc6ae7e67ea2affe53eb35896e12a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:d2ae6094a89afad254aa5ea418551f845cd01230cb1278a65027707c0a569962
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448482378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875ae7023f2ec792e3ee143428c1f2ea0f62d2bdeb057093003e8f58e20b73be`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:47:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf2234c2d9148450317f62d9d62fbf420f271a1d80346b40848fe1c82b463ac`  
		Last Modified: Thu, 03 Mar 2022 23:21:23 GMT  
		Size: 11.1 MB (11082235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:80356ffe0b31b1ce87d70e3ef62ade22cc00dc6d400060e0e8de30d9775d83d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396013110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c1fa5010e397d2fb24ce8d8818df5556f09ea81dceec5fdf91c02b7248881`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:08:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d4d1894d4d4734259ce4328e795671cde30e59717a29ccce3e64de9197c6bc`  
		Last Modified: Wed, 02 Feb 2022 03:35:00 GMT  
		Size: 10.1 MB (10122343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ac5bb37c87d69ac097dbe2f19310de8cb89bf8260c9c395fcfaa01e288975f81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422280318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667daf428f2d4f8cf5143f41531e203424dc27a0726fbce6eb3173bd36e4697b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:17:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:18:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:19:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908fc1da6687829639272ef87642b5189b703086a36418bd251644d6cf90a838`  
		Last Modified: Thu, 03 Mar 2022 21:39:54 GMT  
		Size: 63.1 MB (63067275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80f61cfdf9250e18c6dde75bca8870207161d0f38c1ef62f5505293cf93b3b`  
		Last Modified: Thu, 03 Mar 2022 21:39:46 GMT  
		Size: 277.3 KB (277339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e820e23ff014d59bcfd20cb2799ec78174c68fb17f14b25296ab734d5d103`  
		Last Modified: Thu, 03 Mar 2022 21:39:56 GMT  
		Size: 67.0 MB (67002031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290e23f3297761c3a8f5d737f183e68c2053dd1bc8a89cf47b0196d8815df9c1`  
		Last Modified: Thu, 03 Mar 2022 21:40:13 GMT  
		Size: 10.7 MB (10732966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:f72486be3c09d539e3dd61144de6ac5b2e83a8942f53d2f382ad43d33f8125c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:db32264c05d9a644cb3d824c53f58925f6bc2a9a20cf906400136712fffc7e64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437400143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07b45da64ef12de4aa8a95490faff003d1b0e2fd1bb34b725a2a7736d4f0719`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:527edd5cb53dda632d40f47b024ef6c14c249e67293604c1034b8f621dafa4ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385890767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21394d3b4c786ff653a964f7dab4509dc78cbb489a7c17258bc1dac8ac6d1a1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aed820f4237dbd767f9d71944780cc89346127cdfe2c63ca5d2211f555866220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411547352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c8ad27d9dbc3d3329751a3c83aa314989729f01071e231f59ac9c938a12e4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:17:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:18:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908fc1da6687829639272ef87642b5189b703086a36418bd251644d6cf90a838`  
		Last Modified: Thu, 03 Mar 2022 21:39:54 GMT  
		Size: 63.1 MB (63067275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80f61cfdf9250e18c6dde75bca8870207161d0f38c1ef62f5505293cf93b3b`  
		Last Modified: Thu, 03 Mar 2022 21:39:46 GMT  
		Size: 277.3 KB (277339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e820e23ff014d59bcfd20cb2799ec78174c68fb17f14b25296ab734d5d103`  
		Last Modified: Thu, 03 Mar 2022 21:39:56 GMT  
		Size: 67.0 MB (67002031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:f72486be3c09d539e3dd61144de6ac5b2e83a8942f53d2f382ad43d33f8125c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:db32264c05d9a644cb3d824c53f58925f6bc2a9a20cf906400136712fffc7e64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437400143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07b45da64ef12de4aa8a95490faff003d1b0e2fd1bb34b725a2a7736d4f0719`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:45:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:45:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982d60b18cea4bea769d9f920f3dec216d47f7abc629c2e3247d1c8bcb9664fc`  
		Last Modified: Thu, 03 Mar 2022 23:21:02 GMT  
		Size: 70.2 MB (70235171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4815cafc69491f37c4c880c78fa1db27e0958876cf27ecf99773e197520f3`  
		Last Modified: Thu, 03 Mar 2022 23:20:51 GMT  
		Size: 277.4 KB (277396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520e34a3cdb3a45de4b4329914faade54515b3c32762ef0cd1139b67ebd19d5`  
		Last Modified: Thu, 03 Mar 2022 23:21:07 GMT  
		Size: 75.0 MB (74994244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:527edd5cb53dda632d40f47b024ef6c14c249e67293604c1034b8f621dafa4ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385890767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21394d3b4c786ff653a964f7dab4509dc78cbb489a7c17258bc1dac8ac6d1a1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:06:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:06:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1251fbe6e11e670fa2c22ca7555185a87af09b7a00a1ab304466e2f6df89d8`  
		Last Modified: Wed, 02 Feb 2022 03:34:21 GMT  
		Size: 54.7 MB (54704691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e091dbbcdc27d08f83c858d8ab9782a9333716a03aa27d4d1eff19be1c461a0`  
		Last Modified: Wed, 02 Feb 2022 03:33:51 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a28d93bdcdace9abbf308c29b5a74316a08464be2c22d0734623443d57ae2f`  
		Last Modified: Wed, 02 Feb 2022 03:34:36 GMT  
		Size: 64.7 MB (64746010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aed820f4237dbd767f9d71944780cc89346127cdfe2c63ca5d2211f555866220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.5 MB (411547352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c8ad27d9dbc3d3329751a3c83aa314989729f01071e231f59ac9c938a12e4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:17:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:18:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:18:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908fc1da6687829639272ef87642b5189b703086a36418bd251644d6cf90a838`  
		Last Modified: Thu, 03 Mar 2022 21:39:54 GMT  
		Size: 63.1 MB (63067275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e80f61cfdf9250e18c6dde75bca8870207161d0f38c1ef62f5505293cf93b3b`  
		Last Modified: Thu, 03 Mar 2022 21:39:46 GMT  
		Size: 277.3 KB (277339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76e820e23ff014d59bcfd20cb2799ec78174c68fb17f14b25296ab734d5d103`  
		Last Modified: Thu, 03 Mar 2022 21:39:56 GMT  
		Size: 67.0 MB (67002031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:4b28f6dc6597cb2def231cf5105c79a6b5fc78e817c6a4273cb18cf6630eb542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:44757c657bd24960ff356d1af9f68364aedf8961c3a3e53129f4ecb3e3974123
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291893332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32efa7f1a4917b7e0a333420e7bf2b442122e02a6ad3ea1b213cc361180ce59`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:81574e74b25c691033866489463a92fe540be285a2dc77ddef68f6b50d6c1fa7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266163609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03b18dfca19d1eeac5ca2370489745ae376ca1702e84146914f5fa69f5759b5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e62bc224429f6614a7bdf1f3f59dcc3901c1d1b2f37fb9bd4a85e18e9fb4b84
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281200707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dcb81deff7c65484ea567ca392f57bf15a109fcca1505f4833fe9248b4e089`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:4b28f6dc6597cb2def231cf5105c79a6b5fc78e817c6a4273cb18cf6630eb542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:44757c657bd24960ff356d1af9f68364aedf8961c3a3e53129f4ecb3e3974123
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291893332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32efa7f1a4917b7e0a333420e7bf2b442122e02a6ad3ea1b213cc361180ce59`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:25 GMT
ADD file:dee0aa8497bd26ca41dffa17adff99be2523f66f9b2c557ba9ad2388ed052dca in / 
# Thu, 03 Mar 2022 20:19:25 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:30:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:40:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:41:04 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:41:05 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 22:44:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:44:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:44:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:44:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf06a7c3161117888114e7e91dbd21915efae33c2dbfb086380f7b21946d6e59`  
		Last Modified: Thu, 03 Mar 2022 20:20:28 GMT  
		Size: 26.7 MB (26708326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb61ec94593913764bceda6f5225dfb36c85ab821bba51cfc351aee5c0d15bf9`  
		Last Modified: Thu, 03 Mar 2022 21:53:03 GMT  
		Size: 838.9 KB (838912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842eb625b70f7cd66ae8b93c358fac16bc433d0810c8ad1b72e31f0fb51166d7`  
		Last Modified: Thu, 03 Mar 2022 23:19:58 GMT  
		Size: 4.9 MB (4872136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52318dcbcc7ab7aed846173e137fac8dcca9fd5a9e31f387253baac28a116b29`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7493a4839f98183bd1f660117bc0db64ff324c2821edf758cbac92100fb196`  
		Last Modified: Thu, 03 Mar 2022 23:19:56 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d7cd6f01398c2360ed50375d1d7dd55bcfa633c0d22f561ac31fff3a382158`  
		Last Modified: Thu, 03 Mar 2022 23:20:41 GMT  
		Size: 259.5 MB (259471543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1c8834da4a4cd3b6cd4a81f3da74c08dd5eff8e5057788bac9d716d9c5b70`  
		Last Modified: Thu, 03 Mar 2022 23:19:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:81574e74b25c691033866489463a92fe540be285a2dc77ddef68f6b50d6c1fa7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266163609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03b18dfca19d1eeac5ca2370489745ae376ca1702e84146914f5fa69f5759b5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:00:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:00:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:01:00 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:01:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:01:19 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:01:20 GMT
ENV ROS_DISTRO=melodic
# Wed, 02 Feb 2022 03:05:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:05:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:05:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:05:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a13c5f3e0b3838377e14a11d204289624c042d330876e3c31326720c4d7633`  
		Last Modified: Wed, 02 Feb 2022 03:31:11 GMT  
		Size: 840.0 KB (839965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6068e70d21b899600a53c2d674310c256ac800a719d3fcfdd734cf60e92d3eb`  
		Last Modified: Wed, 02 Feb 2022 03:31:10 GMT  
		Size: 4.1 MB (4085945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34531b8ea861d18f8d51dc03b87850d8d18b299f2d6b1ebe0b8ebf8a15b3ed3`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579acbc591d9acea07aa3dbff7ade00b16cb57796ad701bc27624222b7af656f`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac0551ba705e2667e48f840f79e3b176a553e1f36cf08900716bd4c33e4b67`  
		Last Modified: Wed, 02 Feb 2022 03:33:38 GMT  
		Size: 238.9 MB (238928288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065e30721392aaa57a123c9a6042528a6f2a9d540d03191232f5b206ac1890cf`  
		Last Modified: Wed, 02 Feb 2022 03:31:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e62bc224429f6614a7bdf1f3f59dcc3901c1d1b2f37fb9bd4a85e18e9fb4b84
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281200707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dcb81deff7c65484ea567ca392f57bf15a109fcca1505f4833fe9248b4e089`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:15:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:15:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:15:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:15:56 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:15:57 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:15:58 GMT
ENV ROS_DISTRO=melodic
# Thu, 03 Mar 2022 21:17:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:17:24 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:17:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:17:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4dfa614ed82a619e5b6979c089765d43055a6030db1c3a59cec567b3243eb9`  
		Last Modified: Thu, 03 Mar 2022 21:39:01 GMT  
		Size: 839.6 KB (839634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4785012e1c31b52667716aaf1acad79f62862b118fc616e415cd8f59c57301da`  
		Last Modified: Thu, 03 Mar 2022 21:38:59 GMT  
		Size: 4.3 MB (4263949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc2db9d965436f9f4e5765760ac4a6279674d5fce01d781718de32ac40ed0fc`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed235bb58840a758fddf27104e6525eee36219068b5f6698ce91fe148c119b`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7cb893fa9093c1fb16c697cbf9e24d8e6c64690ca8ad90b4a971dc71eedf9e`  
		Last Modified: Thu, 03 Mar 2022 21:39:34 GMT  
		Size: 252.4 MB (252365097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5fb4153575874a251dc579a38764467e6bd9e778d96a1a9232c317ca4b67c`  
		Last Modified: Thu, 03 Mar 2022 21:38:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:6d2f08cc87eaa471d8f007507f79fccc5be63b1cdd3090723e2c2a3a4dedc9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:6b90ed09399e4bf5a0ecdeaf699e7ca1454c5f195f5360c94bc864a19a8453e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339341488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05afa4c30b5c4c64a0037aa61e2fc0aacc7db210306cf63c84063a5c48df3529`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdb29fca48f80a5c577bd9b967f52c92498f920fef9c8cea16e92fe29294d8`  
		Last Modified: Thu, 03 Mar 2022 23:23:32 GMT  
		Size: 47.3 MB (47259959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ea2ede910be8f02c9b1715aaae3578bc6e9de8f924e0010c5c50bee03085f`  
		Last Modified: Thu, 03 Mar 2022 23:23:24 GMT  
		Size: 309.3 KB (309305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3ddd0a93300f77b84e4f3b49a2ff6bb47cbbe03e467e1802b516ac6da7cdf4`  
		Last Modified: Thu, 03 Mar 2022 23:23:37 GMT  
		Size: 79.6 MB (79602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:277f1fd41a140afc9ed2d616455ee61a35fcedb4eadeec5c8a539fa5d29408e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284832769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3cacf471dede1928c65963cc6cdd7ce02abf949e0685ba74731dfb64d46e8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:19:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fdd92407a8900894de7f6dbf7a326be593b5663a7f4518e16df2931a01d55f`  
		Last Modified: Wed, 02 Feb 2022 03:40:47 GMT  
		Size: 36.7 MB (36693351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e59c776bb1019a065b28cef04e5b1b18c33eec8c605f6e45ba2a18f50dd190`  
		Last Modified: Wed, 02 Feb 2022 03:40:28 GMT  
		Size: 307.1 KB (307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9163f530a84dc1c9c920138491b4c40e78a8f8a866050f052016ea1a3ce47f4b`  
		Last Modified: Wed, 02 Feb 2022 03:41:07 GMT  
		Size: 60.5 MB (60482212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d119adcb89a5828cd52594fef5e68b9562154df95338c992dc0661b5960baf3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318358664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05d81fdcfee79bf461355a632af39bbeaa36114b567c644a5de08036267217`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:22:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:23:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea941390b34bc172dd454813e17c4c94eb7be3f768300a4e17dbb81ae98d26`  
		Last Modified: Thu, 03 Mar 2022 21:42:06 GMT  
		Size: 41.3 MB (41306182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadb9a6241a00137ca5b9f7f28c3331089cc2c768b75ee0d25737ce38ce7a21`  
		Last Modified: Thu, 03 Mar 2022 21:42:00 GMT  
		Size: 309.2 KB (309238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d950cf49074d5c0c0ab8bd4dc48b1407692aa1d1d8eae8d12ec75326e488a0`  
		Last Modified: Thu, 03 Mar 2022 21:42:11 GMT  
		Size: 71.8 MB (71753730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:bd87a0440d97e738f8166fbfaf6b42ba7e06a44cc6d8ccc897c3b66288726924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:282dd9085542968f2236e813cfdd39c0289a250805b71295c916b568e1aac04e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **831.3 MB (831289980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9983b8470d111e88fe2adb5a30eabf79803355b685be14648190ee8c0ca0e2b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdb29fca48f80a5c577bd9b967f52c92498f920fef9c8cea16e92fe29294d8`  
		Last Modified: Thu, 03 Mar 2022 23:23:32 GMT  
		Size: 47.3 MB (47259959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ea2ede910be8f02c9b1715aaae3578bc6e9de8f924e0010c5c50bee03085f`  
		Last Modified: Thu, 03 Mar 2022 23:23:24 GMT  
		Size: 309.3 KB (309305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3ddd0a93300f77b84e4f3b49a2ff6bb47cbbe03e467e1802b516ac6da7cdf4`  
		Last Modified: Thu, 03 Mar 2022 23:23:37 GMT  
		Size: 79.6 MB (79602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d20b699901600cccce48488414a9dd0422d2895492730687aa8adef23a7b687`  
		Last Modified: Thu, 03 Mar 2022 23:25:24 GMT  
		Size: 491.9 MB (491948492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:4523fda981e7422844b7f1e51b0ee3fc802299b1362c0be612c583337b98544e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.1 MB (721114502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d7e660599567d0d130ff0f3b07814a32df28654472fe0974aa59d64a3159cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:19:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:29:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fdd92407a8900894de7f6dbf7a326be593b5663a7f4518e16df2931a01d55f`  
		Last Modified: Wed, 02 Feb 2022 03:40:47 GMT  
		Size: 36.7 MB (36693351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e59c776bb1019a065b28cef04e5b1b18c33eec8c605f6e45ba2a18f50dd190`  
		Last Modified: Wed, 02 Feb 2022 03:40:28 GMT  
		Size: 307.1 KB (307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9163f530a84dc1c9c920138491b4c40e78a8f8a866050f052016ea1a3ce47f4b`  
		Last Modified: Wed, 02 Feb 2022 03:41:07 GMT  
		Size: 60.5 MB (60482212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b4c7a328f0c55d991752acd1e86f087cee7829349dc21b75beb8b1ee74989f`  
		Last Modified: Wed, 02 Feb 2022 03:46:12 GMT  
		Size: 436.3 MB (436281733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f91e6d5ad30903ca659a9e6465dadff5a434900146a4b17c8fdb7613f1457f2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.8 MB (780835119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4ba87571080cec8f30b7a3856f03b4a37cefcb6266c40c2f9d25ba80fab48d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:22:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:23:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea941390b34bc172dd454813e17c4c94eb7be3f768300a4e17dbb81ae98d26`  
		Last Modified: Thu, 03 Mar 2022 21:42:06 GMT  
		Size: 41.3 MB (41306182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadb9a6241a00137ca5b9f7f28c3331089cc2c768b75ee0d25737ce38ce7a21`  
		Last Modified: Thu, 03 Mar 2022 21:42:00 GMT  
		Size: 309.2 KB (309238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d950cf49074d5c0c0ab8bd4dc48b1407692aa1d1d8eae8d12ec75326e488a0`  
		Last Modified: Thu, 03 Mar 2022 21:42:11 GMT  
		Size: 71.8 MB (71753730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df905bd7e0288b9a41622859f12eee9a1eac351afa894a89a9c8037e37854c5b`  
		Last Modified: Thu, 03 Mar 2022 21:43:45 GMT  
		Size: 462.5 MB (462476455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:4d84e6517c110bd902a5b907aa74e47cc2393271c86fc66794b15cfd87e198b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:540b61c3d6c1a503aa1932987820a050e217eb5790d0ed9b8c76830e8b243133
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.3 MB (951259140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb695e29ce5ed8caaebe3e6225350cbae49f321f1293c695edfc9d62f4d98bb8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:37:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:37:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Mar 2022 10:37:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Mar 2022 10:38:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:38:59 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Mar 2022 10:38:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Mar 2022 10:38:59 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:39:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:39:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Mar 2022 10:39:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:42:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c133b370766b6f5552e000ccf033e32442276773c2cd08a21a0ac9f18259d3`  
		Last Modified: Wed, 02 Mar 2022 10:43:37 GMT  
		Size: 10.9 MB (10892098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ae26f65841562882d5b66361657c9e58e057d74f3ecdca875adcf248f594eb`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c03d38883523f98928ace45a667c9a6f9c1e357c09c22bc32e9f75e3ee391`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3c4ec48c4a1bce55afcd9bbda77e99d790164b04caa20748eb0bd7b2dd5ae`  
		Last Modified: Wed, 02 Mar 2022 10:44:10 GMT  
		Size: 239.1 MB (239095099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970c2b44800a0ec91c9c10e46c3e219d142dbbce8abf085f6c89e01de485a28a`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f52ffdc8600971c23fcc3470929f8e69fcf2f8140208f05977079961d4c9237`  
		Last Modified: Wed, 02 Mar 2022 10:44:29 GMT  
		Size: 86.6 MB (86566685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44425534870ef9a16bf44a1fe3fa688b25244bebc0c9fe2c9db6e3107d70aa`  
		Last Modified: Wed, 02 Mar 2022 10:44:17 GMT  
		Size: 303.9 KB (303871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c3bc0c0b6b4ceaa48e62a3d09745513fcedb49c063d68038f3b84cd2ef6909`  
		Last Modified: Wed, 02 Mar 2022 10:44:27 GMT  
		Size: 76.0 MB (75976673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936eb4d6ce9175f6ea5ceac81d0faf33295da1adfb9748fdd642e0628eeba00`  
		Last Modified: Wed, 02 Mar 2022 10:45:57 GMT  
		Size: 488.0 MB (487985253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0da82160c5492e045954646ac43bb2e9ea2859360e4aae1f23c983be1cdcead3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.4 MB (867433770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358c42be9b77f6ad411faeaf4ce6119e2c6cd664c0a0757eba0f3a8a2d8af9fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:41 GMT
ADD file:ec3d90624857dbfae217c1372a38966f453fcd51282379652f07d2ccf6fcc67e in / 
# Tue, 01 Mar 2022 02:11:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:06:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:06:27 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 01 Mar 2022 22:07:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 01 Mar 2022 22:07:13 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 22:07:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 01 Mar 2022 22:07:15 GMT
ENV ROS_DISTRO=noetic
# Tue, 01 Mar 2022 22:08:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:08:31 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 01 Mar 2022 22:08:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 01 Mar 2022 22:08:34 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:09:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:09:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 01 Mar 2022 22:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:13:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:72f0eb753e825356fa0fef854ac259cc8eefdb0f689516f29b13da8b1595c342`  
		Last Modified: Tue, 01 Mar 2022 02:18:46 GMT  
		Size: 49.2 MB (49223022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81dad0cc65e28099216f8e66fc4a9ff1d7beb908c009b51ce776f53e30ed16e`  
		Last Modified: Tue, 01 Mar 2022 22:15:59 GMT  
		Size: 10.7 MB (10688196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbbf1f406c973f913df3bf3c1a30b098a376a89b1bdb355fa67a4d85c53437`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cb5a189c80ce8736e0a2023d103c32a058bb7dc0ffd1788e9621c793e613af`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f4e8ce419e89e72b01e8ac6833ae7d79adf8b984203a468dacae04d36dbc01`  
		Last Modified: Tue, 01 Mar 2022 22:16:29 GMT  
		Size: 184.3 MB (184303647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47f84d9b6f883f86b5ab85b7341f781dd8a4f20c3576334ec2b1b2511b39120`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823c701829b09ea926c81cf7d31b4ce9fa4d4990e4d494dcc244816cfbb6f59b`  
		Last Modified: Tue, 01 Mar 2022 22:16:48 GMT  
		Size: 84.4 MB (84351038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d8e0cf44deb036ea2133c6e3b736cea94b5676c0043de056918a76f8693cbf`  
		Last Modified: Tue, 01 Mar 2022 22:16:37 GMT  
		Size: 303.8 KB (303820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b401603f0a64181e3faea2a2fedbe6b9d6528a442bc2163aef25c8efaba1757`  
		Last Modified: Tue, 01 Mar 2022 22:16:48 GMT  
		Size: 73.9 MB (73864242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8811ffba184043e283bca735162fdfc3c813fed87a372e54aeb244f9fe558be`  
		Last Modified: Tue, 01 Mar 2022 22:18:15 GMT  
		Size: 464.7 MB (464697433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:bd87a0440d97e738f8166fbfaf6b42ba7e06a44cc6d8ccc897c3b66288726924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:282dd9085542968f2236e813cfdd39c0289a250805b71295c916b568e1aac04e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **831.3 MB (831289980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9983b8470d111e88fe2adb5a30eabf79803355b685be14648190ee8c0ca0e2b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:07:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdb29fca48f80a5c577bd9b967f52c92498f920fef9c8cea16e92fe29294d8`  
		Last Modified: Thu, 03 Mar 2022 23:23:32 GMT  
		Size: 47.3 MB (47259959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ea2ede910be8f02c9b1715aaae3578bc6e9de8f924e0010c5c50bee03085f`  
		Last Modified: Thu, 03 Mar 2022 23:23:24 GMT  
		Size: 309.3 KB (309305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3ddd0a93300f77b84e4f3b49a2ff6bb47cbbe03e467e1802b516ac6da7cdf4`  
		Last Modified: Thu, 03 Mar 2022 23:23:37 GMT  
		Size: 79.6 MB (79602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d20b699901600cccce48488414a9dd0422d2895492730687aa8adef23a7b687`  
		Last Modified: Thu, 03 Mar 2022 23:25:24 GMT  
		Size: 491.9 MB (491948492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:4523fda981e7422844b7f1e51b0ee3fc802299b1362c0be612c583337b98544e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.1 MB (721114502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d7e660599567d0d130ff0f3b07814a32df28654472fe0974aa59d64a3159cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:19:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:29:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fdd92407a8900894de7f6dbf7a326be593b5663a7f4518e16df2931a01d55f`  
		Last Modified: Wed, 02 Feb 2022 03:40:47 GMT  
		Size: 36.7 MB (36693351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e59c776bb1019a065b28cef04e5b1b18c33eec8c605f6e45ba2a18f50dd190`  
		Last Modified: Wed, 02 Feb 2022 03:40:28 GMT  
		Size: 307.1 KB (307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9163f530a84dc1c9c920138491b4c40e78a8f8a866050f052016ea1a3ce47f4b`  
		Last Modified: Wed, 02 Feb 2022 03:41:07 GMT  
		Size: 60.5 MB (60482212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b4c7a328f0c55d991752acd1e86f087cee7829349dc21b75beb8b1ee74989f`  
		Last Modified: Wed, 02 Feb 2022 03:46:12 GMT  
		Size: 436.3 MB (436281733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f91e6d5ad30903ca659a9e6465dadff5a434900146a4b17c8fdb7613f1457f2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.8 MB (780835119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4ba87571080cec8f30b7a3856f03b4a37cefcb6266c40c2f9d25ba80fab48d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:22:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:23:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:26:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea941390b34bc172dd454813e17c4c94eb7be3f768300a4e17dbb81ae98d26`  
		Last Modified: Thu, 03 Mar 2022 21:42:06 GMT  
		Size: 41.3 MB (41306182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadb9a6241a00137ca5b9f7f28c3331089cc2c768b75ee0d25737ce38ce7a21`  
		Last Modified: Thu, 03 Mar 2022 21:42:00 GMT  
		Size: 309.2 KB (309238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d950cf49074d5c0c0ab8bd4dc48b1407692aa1d1d8eae8d12ec75326e488a0`  
		Last Modified: Thu, 03 Mar 2022 21:42:11 GMT  
		Size: 71.8 MB (71753730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df905bd7e0288b9a41622859f12eee9a1eac351afa894a89a9c8037e37854c5b`  
		Last Modified: Thu, 03 Mar 2022 21:43:45 GMT  
		Size: 462.5 MB (462476455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:7414860b6a81a390f69360f642a5a28026241a0c76798c56a606d773875949f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:80679cce228945c03e1427e608de5521febbc56bda6c5a4a28c830e72737eb47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355200160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aecc1e5ec0bd211d96d9433a230892d21bc09be11b389512e8c9d0fc7407f4fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:59:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdb29fca48f80a5c577bd9b967f52c92498f920fef9c8cea16e92fe29294d8`  
		Last Modified: Thu, 03 Mar 2022 23:23:32 GMT  
		Size: 47.3 MB (47259959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ea2ede910be8f02c9b1715aaae3578bc6e9de8f924e0010c5c50bee03085f`  
		Last Modified: Thu, 03 Mar 2022 23:23:24 GMT  
		Size: 309.3 KB (309305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3ddd0a93300f77b84e4f3b49a2ff6bb47cbbe03e467e1802b516ac6da7cdf4`  
		Last Modified: Thu, 03 Mar 2022 23:23:37 GMT  
		Size: 79.6 MB (79602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefd4600aede5debdfad6d4a14579797ca9edaf8350f1bf34461b20100f7199b`  
		Last Modified: Thu, 03 Mar 2022 23:23:53 GMT  
		Size: 15.9 MB (15858672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:0d43b3f0e23fb14a2704ff979c25d9c2710be3c671ae414e53fedc5730013d07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 MB (298896792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4823ddcf39f7cc998877cc8fe5c9ee13dbd9578b704eb1a957bc1c7874fef95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:19:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:20:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fdd92407a8900894de7f6dbf7a326be593b5663a7f4518e16df2931a01d55f`  
		Last Modified: Wed, 02 Feb 2022 03:40:47 GMT  
		Size: 36.7 MB (36693351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e59c776bb1019a065b28cef04e5b1b18c33eec8c605f6e45ba2a18f50dd190`  
		Last Modified: Wed, 02 Feb 2022 03:40:28 GMT  
		Size: 307.1 KB (307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9163f530a84dc1c9c920138491b4c40e78a8f8a866050f052016ea1a3ce47f4b`  
		Last Modified: Wed, 02 Feb 2022 03:41:07 GMT  
		Size: 60.5 MB (60482212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92593c1fe25cb5f82c66cf08822259456cd24be835a0d854f5b5f2a74a1d03f4`  
		Last Modified: Wed, 02 Feb 2022 03:41:33 GMT  
		Size: 14.1 MB (14064023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:81c5f246d2e463772f86aba5957324a5b4f82e22b24386efd229d15aa147dda4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.8 MB (333805834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97946ba8c9ec9dd286a4fda7f3dc64872038f161c4d7d31947f9af60688a5d25`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:22:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:23:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:23:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea941390b34bc172dd454813e17c4c94eb7be3f768300a4e17dbb81ae98d26`  
		Last Modified: Thu, 03 Mar 2022 21:42:06 GMT  
		Size: 41.3 MB (41306182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadb9a6241a00137ca5b9f7f28c3331089cc2c768b75ee0d25737ce38ce7a21`  
		Last Modified: Thu, 03 Mar 2022 21:42:00 GMT  
		Size: 309.2 KB (309238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d950cf49074d5c0c0ab8bd4dc48b1407692aa1d1d8eae8d12ec75326e488a0`  
		Last Modified: Thu, 03 Mar 2022 21:42:11 GMT  
		Size: 71.8 MB (71753730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a9bba347021b913a73d390cdff8d9b1ce7d67e0304f69bca5bd2af1add45ba`  
		Last Modified: Thu, 03 Mar 2022 21:42:27 GMT  
		Size: 15.4 MB (15447170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:4655c2268c00e6855ac921a1d8cfb8e1dccb2b894a75886524def8b6643ad99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:0826acf3094fb06cb67862cc778126d3da3339aed28a17b85264b8c6d4a5d016
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484719661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a2f0ff2c89449c2ef8f9c1983c5141c503f303650b90ca53fac013a962c247`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:37:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:37:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Mar 2022 10:37:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Mar 2022 10:38:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:38:59 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Mar 2022 10:38:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Mar 2022 10:38:59 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:39:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:39:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Mar 2022 10:39:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:40:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c133b370766b6f5552e000ccf033e32442276773c2cd08a21a0ac9f18259d3`  
		Last Modified: Wed, 02 Mar 2022 10:43:37 GMT  
		Size: 10.9 MB (10892098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ae26f65841562882d5b66361657c9e58e057d74f3ecdca875adcf248f594eb`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c03d38883523f98928ace45a667c9a6f9c1e357c09c22bc32e9f75e3ee391`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3c4ec48c4a1bce55afcd9bbda77e99d790164b04caa20748eb0bd7b2dd5ae`  
		Last Modified: Wed, 02 Mar 2022 10:44:10 GMT  
		Size: 239.1 MB (239095099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970c2b44800a0ec91c9c10e46c3e219d142dbbce8abf085f6c89e01de485a28a`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f52ffdc8600971c23fcc3470929f8e69fcf2f8140208f05977079961d4c9237`  
		Last Modified: Wed, 02 Mar 2022 10:44:29 GMT  
		Size: 86.6 MB (86566685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44425534870ef9a16bf44a1fe3fa688b25244bebc0c9fe2c9db6e3107d70aa`  
		Last Modified: Wed, 02 Mar 2022 10:44:17 GMT  
		Size: 303.9 KB (303871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c3bc0c0b6b4ceaa48e62a3d09745513fcedb49c063d68038f3b84cd2ef6909`  
		Last Modified: Wed, 02 Mar 2022 10:44:27 GMT  
		Size: 76.0 MB (75976673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34040ac500755ccc5d3ece91bb7a076154faabf7adda6b8dcef8ccfdd4b17fea`  
		Last Modified: Wed, 02 Mar 2022 10:44:38 GMT  
		Size: 21.4 MB (21445774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a8fee6794a222965f2de45c8e2edc4d1f0227888d451598241938b1c82eaaa48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.8 MB (423840982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bb2e80fdbadc9b1a28d1bbc7471ce08ab4d17f583b143410d75861c4a0a752`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:41 GMT
ADD file:ec3d90624857dbfae217c1372a38966f453fcd51282379652f07d2ccf6fcc67e in / 
# Tue, 01 Mar 2022 02:11:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:06:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:06:27 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 01 Mar 2022 22:07:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 01 Mar 2022 22:07:13 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 22:07:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 01 Mar 2022 22:07:15 GMT
ENV ROS_DISTRO=noetic
# Tue, 01 Mar 2022 22:08:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:08:31 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 01 Mar 2022 22:08:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 01 Mar 2022 22:08:34 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:09:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:09:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 01 Mar 2022 22:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:10:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:72f0eb753e825356fa0fef854ac259cc8eefdb0f689516f29b13da8b1595c342`  
		Last Modified: Tue, 01 Mar 2022 02:18:46 GMT  
		Size: 49.2 MB (49223022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81dad0cc65e28099216f8e66fc4a9ff1d7beb908c009b51ce776f53e30ed16e`  
		Last Modified: Tue, 01 Mar 2022 22:15:59 GMT  
		Size: 10.7 MB (10688196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbbf1f406c973f913df3bf3c1a30b098a376a89b1bdb355fa67a4d85c53437`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cb5a189c80ce8736e0a2023d103c32a058bb7dc0ffd1788e9621c793e613af`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f4e8ce419e89e72b01e8ac6833ae7d79adf8b984203a468dacae04d36dbc01`  
		Last Modified: Tue, 01 Mar 2022 22:16:29 GMT  
		Size: 184.3 MB (184303647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47f84d9b6f883f86b5ab85b7341f781dd8a4f20c3576334ec2b1b2511b39120`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823c701829b09ea926c81cf7d31b4ce9fa4d4990e4d494dcc244816cfbb6f59b`  
		Last Modified: Tue, 01 Mar 2022 22:16:48 GMT  
		Size: 84.4 MB (84351038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d8e0cf44deb036ea2133c6e3b736cea94b5676c0043de056918a76f8693cbf`  
		Last Modified: Tue, 01 Mar 2022 22:16:37 GMT  
		Size: 303.8 KB (303820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b401603f0a64181e3faea2a2fedbe6b9d6528a442bc2163aef25c8efaba1757`  
		Last Modified: Tue, 01 Mar 2022 22:16:48 GMT  
		Size: 73.9 MB (73864242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86145621139710bd0d3767406b61a6649dff3fcf4db514486574200746d74acd`  
		Last Modified: Tue, 01 Mar 2022 22:16:59 GMT  
		Size: 21.1 MB (21104645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:7414860b6a81a390f69360f642a5a28026241a0c76798c56a606d773875949f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:80679cce228945c03e1427e608de5521febbc56bda6c5a4a28c830e72737eb47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355200160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aecc1e5ec0bd211d96d9433a230892d21bc09be11b389512e8c9d0fc7407f4fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:59:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdb29fca48f80a5c577bd9b967f52c92498f920fef9c8cea16e92fe29294d8`  
		Last Modified: Thu, 03 Mar 2022 23:23:32 GMT  
		Size: 47.3 MB (47259959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ea2ede910be8f02c9b1715aaae3578bc6e9de8f924e0010c5c50bee03085f`  
		Last Modified: Thu, 03 Mar 2022 23:23:24 GMT  
		Size: 309.3 KB (309305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3ddd0a93300f77b84e4f3b49a2ff6bb47cbbe03e467e1802b516ac6da7cdf4`  
		Last Modified: Thu, 03 Mar 2022 23:23:37 GMT  
		Size: 79.6 MB (79602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefd4600aede5debdfad6d4a14579797ca9edaf8350f1bf34461b20100f7199b`  
		Last Modified: Thu, 03 Mar 2022 23:23:53 GMT  
		Size: 15.9 MB (15858672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:0d43b3f0e23fb14a2704ff979c25d9c2710be3c671ae414e53fedc5730013d07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 MB (298896792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4823ddcf39f7cc998877cc8fe5c9ee13dbd9578b704eb1a957bc1c7874fef95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:19:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:20:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fdd92407a8900894de7f6dbf7a326be593b5663a7f4518e16df2931a01d55f`  
		Last Modified: Wed, 02 Feb 2022 03:40:47 GMT  
		Size: 36.7 MB (36693351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e59c776bb1019a065b28cef04e5b1b18c33eec8c605f6e45ba2a18f50dd190`  
		Last Modified: Wed, 02 Feb 2022 03:40:28 GMT  
		Size: 307.1 KB (307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9163f530a84dc1c9c920138491b4c40e78a8f8a866050f052016ea1a3ce47f4b`  
		Last Modified: Wed, 02 Feb 2022 03:41:07 GMT  
		Size: 60.5 MB (60482212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92593c1fe25cb5f82c66cf08822259456cd24be835a0d854f5b5f2a74a1d03f4`  
		Last Modified: Wed, 02 Feb 2022 03:41:33 GMT  
		Size: 14.1 MB (14064023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:81c5f246d2e463772f86aba5957324a5b4f82e22b24386efd229d15aa147dda4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.8 MB (333805834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97946ba8c9ec9dd286a4fda7f3dc64872038f161c4d7d31947f9af60688a5d25`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:22:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:23:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:23:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea941390b34bc172dd454813e17c4c94eb7be3f768300a4e17dbb81ae98d26`  
		Last Modified: Thu, 03 Mar 2022 21:42:06 GMT  
		Size: 41.3 MB (41306182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadb9a6241a00137ca5b9f7f28c3331089cc2c768b75ee0d25737ce38ce7a21`  
		Last Modified: Thu, 03 Mar 2022 21:42:00 GMT  
		Size: 309.2 KB (309238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d950cf49074d5c0c0ab8bd4dc48b1407692aa1d1d8eae8d12ec75326e488a0`  
		Last Modified: Thu, 03 Mar 2022 21:42:11 GMT  
		Size: 71.8 MB (71753730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a9bba347021b913a73d390cdff8d9b1ce7d67e0304f69bca5bd2af1add45ba`  
		Last Modified: Thu, 03 Mar 2022 21:42:27 GMT  
		Size: 15.4 MB (15447170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:6d2f08cc87eaa471d8f007507f79fccc5be63b1cdd3090723e2c2a3a4dedc9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:6b90ed09399e4bf5a0ecdeaf699e7ca1454c5f195f5360c94bc864a19a8453e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339341488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05afa4c30b5c4c64a0037aa61e2fc0aacc7db210306cf63c84063a5c48df3529`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdb29fca48f80a5c577bd9b967f52c92498f920fef9c8cea16e92fe29294d8`  
		Last Modified: Thu, 03 Mar 2022 23:23:32 GMT  
		Size: 47.3 MB (47259959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ea2ede910be8f02c9b1715aaae3578bc6e9de8f924e0010c5c50bee03085f`  
		Last Modified: Thu, 03 Mar 2022 23:23:24 GMT  
		Size: 309.3 KB (309305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3ddd0a93300f77b84e4f3b49a2ff6bb47cbbe03e467e1802b516ac6da7cdf4`  
		Last Modified: Thu, 03 Mar 2022 23:23:37 GMT  
		Size: 79.6 MB (79602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:277f1fd41a140afc9ed2d616455ee61a35fcedb4eadeec5c8a539fa5d29408e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284832769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3cacf471dede1928c65963cc6cdd7ce02abf949e0685ba74731dfb64d46e8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:19:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fdd92407a8900894de7f6dbf7a326be593b5663a7f4518e16df2931a01d55f`  
		Last Modified: Wed, 02 Feb 2022 03:40:47 GMT  
		Size: 36.7 MB (36693351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e59c776bb1019a065b28cef04e5b1b18c33eec8c605f6e45ba2a18f50dd190`  
		Last Modified: Wed, 02 Feb 2022 03:40:28 GMT  
		Size: 307.1 KB (307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9163f530a84dc1c9c920138491b4c40e78a8f8a866050f052016ea1a3ce47f4b`  
		Last Modified: Wed, 02 Feb 2022 03:41:07 GMT  
		Size: 60.5 MB (60482212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d119adcb89a5828cd52594fef5e68b9562154df95338c992dc0661b5960baf3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318358664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05d81fdcfee79bf461355a632af39bbeaa36114b567c644a5de08036267217`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:22:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:23:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea941390b34bc172dd454813e17c4c94eb7be3f768300a4e17dbb81ae98d26`  
		Last Modified: Thu, 03 Mar 2022 21:42:06 GMT  
		Size: 41.3 MB (41306182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadb9a6241a00137ca5b9f7f28c3331089cc2c768b75ee0d25737ce38ce7a21`  
		Last Modified: Thu, 03 Mar 2022 21:42:00 GMT  
		Size: 309.2 KB (309238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d950cf49074d5c0c0ab8bd4dc48b1407692aa1d1d8eae8d12ec75326e488a0`  
		Last Modified: Thu, 03 Mar 2022 21:42:11 GMT  
		Size: 71.8 MB (71753730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:d8d0895f1c50ba21d84bce7e701147c22ca577f176ccb7ae0ae5c0364b90106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:f74ba82e15175cee129d5bc5d1566d954c2ccefd2a2f3f3c3dadb8ae506590a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463273887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453b48768682d6f37b5d6c1086b7e92ad5582750be12d2ed159fe2c8fd0a9c34`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:37:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:37:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Mar 2022 10:37:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Mar 2022 10:38:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:38:59 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Mar 2022 10:38:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Mar 2022 10:38:59 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:39:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:39:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Mar 2022 10:39:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c133b370766b6f5552e000ccf033e32442276773c2cd08a21a0ac9f18259d3`  
		Last Modified: Wed, 02 Mar 2022 10:43:37 GMT  
		Size: 10.9 MB (10892098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ae26f65841562882d5b66361657c9e58e057d74f3ecdca875adcf248f594eb`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c03d38883523f98928ace45a667c9a6f9c1e357c09c22bc32e9f75e3ee391`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3c4ec48c4a1bce55afcd9bbda77e99d790164b04caa20748eb0bd7b2dd5ae`  
		Last Modified: Wed, 02 Mar 2022 10:44:10 GMT  
		Size: 239.1 MB (239095099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970c2b44800a0ec91c9c10e46c3e219d142dbbce8abf085f6c89e01de485a28a`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f52ffdc8600971c23fcc3470929f8e69fcf2f8140208f05977079961d4c9237`  
		Last Modified: Wed, 02 Mar 2022 10:44:29 GMT  
		Size: 86.6 MB (86566685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44425534870ef9a16bf44a1fe3fa688b25244bebc0c9fe2c9db6e3107d70aa`  
		Last Modified: Wed, 02 Mar 2022 10:44:17 GMT  
		Size: 303.9 KB (303871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c3bc0c0b6b4ceaa48e62a3d09745513fcedb49c063d68038f3b84cd2ef6909`  
		Last Modified: Wed, 02 Mar 2022 10:44:27 GMT  
		Size: 76.0 MB (75976673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a6f9e01d94995d5ebdc90a7aa8a404c598ab2cea80c225426a61af23251a41ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402736337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f468d0d131a18dfa9ea4ea06d230eac24e5bec1f8c34a89ed2f78a58427b6d59`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:41 GMT
ADD file:ec3d90624857dbfae217c1372a38966f453fcd51282379652f07d2ccf6fcc67e in / 
# Tue, 01 Mar 2022 02:11:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:06:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:06:27 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 01 Mar 2022 22:07:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 01 Mar 2022 22:07:13 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 22:07:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 01 Mar 2022 22:07:15 GMT
ENV ROS_DISTRO=noetic
# Tue, 01 Mar 2022 22:08:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:08:31 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 01 Mar 2022 22:08:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 01 Mar 2022 22:08:34 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:09:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:09:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 01 Mar 2022 22:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:72f0eb753e825356fa0fef854ac259cc8eefdb0f689516f29b13da8b1595c342`  
		Last Modified: Tue, 01 Mar 2022 02:18:46 GMT  
		Size: 49.2 MB (49223022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81dad0cc65e28099216f8e66fc4a9ff1d7beb908c009b51ce776f53e30ed16e`  
		Last Modified: Tue, 01 Mar 2022 22:15:59 GMT  
		Size: 10.7 MB (10688196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbbf1f406c973f913df3bf3c1a30b098a376a89b1bdb355fa67a4d85c53437`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cb5a189c80ce8736e0a2023d103c32a058bb7dc0ffd1788e9621c793e613af`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f4e8ce419e89e72b01e8ac6833ae7d79adf8b984203a468dacae04d36dbc01`  
		Last Modified: Tue, 01 Mar 2022 22:16:29 GMT  
		Size: 184.3 MB (184303647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47f84d9b6f883f86b5ab85b7341f781dd8a4f20c3576334ec2b1b2511b39120`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823c701829b09ea926c81cf7d31b4ce9fa4d4990e4d494dcc244816cfbb6f59b`  
		Last Modified: Tue, 01 Mar 2022 22:16:48 GMT  
		Size: 84.4 MB (84351038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d8e0cf44deb036ea2133c6e3b736cea94b5676c0043de056918a76f8693cbf`  
		Last Modified: Tue, 01 Mar 2022 22:16:37 GMT  
		Size: 303.8 KB (303820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b401603f0a64181e3faea2a2fedbe6b9d6528a442bc2163aef25c8efaba1757`  
		Last Modified: Tue, 01 Mar 2022 22:16:48 GMT  
		Size: 73.9 MB (73864242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:6d2f08cc87eaa471d8f007507f79fccc5be63b1cdd3090723e2c2a3a4dedc9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:6b90ed09399e4bf5a0ecdeaf699e7ca1454c5f195f5360c94bc864a19a8453e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339341488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05afa4c30b5c4c64a0037aa61e2fc0aacc7db210306cf63c84063a5c48df3529`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:57:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 22:58:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdb29fca48f80a5c577bd9b967f52c92498f920fef9c8cea16e92fe29294d8`  
		Last Modified: Thu, 03 Mar 2022 23:23:32 GMT  
		Size: 47.3 MB (47259959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1ea2ede910be8f02c9b1715aaae3578bc6e9de8f924e0010c5c50bee03085f`  
		Last Modified: Thu, 03 Mar 2022 23:23:24 GMT  
		Size: 309.3 KB (309305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3ddd0a93300f77b84e4f3b49a2ff6bb47cbbe03e467e1802b516ac6da7cdf4`  
		Last Modified: Thu, 03 Mar 2022 23:23:37 GMT  
		Size: 79.6 MB (79602604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:277f1fd41a140afc9ed2d616455ee61a35fcedb4eadeec5c8a539fa5d29408e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284832769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3cacf471dede1928c65963cc6cdd7ce02abf949e0685ba74731dfb64d46e8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:18:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:18:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 02 Feb 2022 03:19:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fdd92407a8900894de7f6dbf7a326be593b5663a7f4518e16df2931a01d55f`  
		Last Modified: Wed, 02 Feb 2022 03:40:47 GMT  
		Size: 36.7 MB (36693351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e59c776bb1019a065b28cef04e5b1b18c33eec8c605f6e45ba2a18f50dd190`  
		Last Modified: Wed, 02 Feb 2022 03:40:28 GMT  
		Size: 307.1 KB (307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9163f530a84dc1c9c920138491b4c40e78a8f8a866050f052016ea1a3ce47f4b`  
		Last Modified: Wed, 02 Feb 2022 03:41:07 GMT  
		Size: 60.5 MB (60482212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d119adcb89a5828cd52594fef5e68b9562154df95338c992dc0661b5960baf3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318358664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05d81fdcfee79bf461355a632af39bbeaa36114b567c644a5de08036267217`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:22:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:23:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ea941390b34bc172dd454813e17c4c94eb7be3f768300a4e17dbb81ae98d26`  
		Last Modified: Thu, 03 Mar 2022 21:42:06 GMT  
		Size: 41.3 MB (41306182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadb9a6241a00137ca5b9f7f28c3331089cc2c768b75ee0d25737ce38ce7a21`  
		Last Modified: Thu, 03 Mar 2022 21:42:00 GMT  
		Size: 309.2 KB (309238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d950cf49074d5c0c0ab8bd4dc48b1407692aa1d1d8eae8d12ec75326e488a0`  
		Last Modified: Thu, 03 Mar 2022 21:42:11 GMT  
		Size: 71.8 MB (71753730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:54ba371fc315ce334490d1dca1ae8603ce6905b8ea46a0750cd60ffa702815bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d5288bf07359d1a92f6ae3333f2fec4eddc429dd253619d5db7394448df1fe42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212169620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08514670a8a0e2d7393eb92d8355d2323bc3aa9a8a38570af6d3fc4ed2e19386`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:a78462b673b8587f7341890f90c3240e321f18022c101c46d2d665ea478f350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187350115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5ca30f9ece0cdcbbfde22d3bf7182e7a86a841d28a9ca8953997d47e4ae1cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1f51dc332d38278d7ff86c87f16d64fd180365182b56f98010c9ffc13fb93680
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204989514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389444e501305edacd8c96409ec5d352876c401d8d531d3a316628b65935d120`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:11741487d2f4b010aae9db137f123cde7cd8e4ffadfde53289d3b7826778b7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:2a4b90935f4fc43465af808ac2fafe40d23ae53c5d942ae8c903ac2b6722a06a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300426658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784f655f06d9d4392b5f6143f4296c48f1b01585b8829d59e49d32b3b710845b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 10:37:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:37:18 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Mar 2022 10:37:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Mar 2022 10:37:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Mar 2022 10:38:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 10:38:59 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Mar 2022 10:38:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Mar 2022 10:38:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c133b370766b6f5552e000ccf033e32442276773c2cd08a21a0ac9f18259d3`  
		Last Modified: Wed, 02 Mar 2022 10:43:37 GMT  
		Size: 10.9 MB (10892098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ae26f65841562882d5b66361657c9e58e057d74f3ecdca875adcf248f594eb`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32c03d38883523f98928ace45a667c9a6f9c1e357c09c22bc32e9f75e3ee391`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3c4ec48c4a1bce55afcd9bbda77e99d790164b04caa20748eb0bd7b2dd5ae`  
		Last Modified: Wed, 02 Mar 2022 10:44:10 GMT  
		Size: 239.1 MB (239095099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970c2b44800a0ec91c9c10e46c3e219d142dbbce8abf085f6c89e01de485a28a`  
		Last Modified: Wed, 02 Mar 2022 10:43:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4b7a420cb8b439ed3d7af772a45dd3b41428ef502c6dfef48cc2361d181492c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244217237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17b1f72b94dcbc75ac63e9176bf80918c97e7cce85abdbbbeda9f79e34a246a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:41 GMT
ADD file:ec3d90624857dbfae217c1372a38966f453fcd51282379652f07d2ccf6fcc67e in / 
# Tue, 01 Mar 2022 02:11:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:06:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:06:27 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 01 Mar 2022 22:07:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 01 Mar 2022 22:07:13 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 22:07:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 01 Mar 2022 22:07:15 GMT
ENV ROS_DISTRO=noetic
# Tue, 01 Mar 2022 22:08:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:08:31 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 01 Mar 2022 22:08:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 01 Mar 2022 22:08:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:72f0eb753e825356fa0fef854ac259cc8eefdb0f689516f29b13da8b1595c342`  
		Last Modified: Tue, 01 Mar 2022 02:18:46 GMT  
		Size: 49.2 MB (49223022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81dad0cc65e28099216f8e66fc4a9ff1d7beb908c009b51ce776f53e30ed16e`  
		Last Modified: Tue, 01 Mar 2022 22:15:59 GMT  
		Size: 10.7 MB (10688196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffbbf1f406c973f913df3bf3c1a30b098a376a89b1bdb355fa67a4d85c53437`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cb5a189c80ce8736e0a2023d103c32a058bb7dc0ffd1788e9621c793e613af`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f4e8ce419e89e72b01e8ac6833ae7d79adf8b984203a468dacae04d36dbc01`  
		Last Modified: Tue, 01 Mar 2022 22:16:29 GMT  
		Size: 184.3 MB (184303647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47f84d9b6f883f86b5ab85b7341f781dd8a4f20c3576334ec2b1b2511b39120`  
		Last Modified: Tue, 01 Mar 2022 22:15:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:54ba371fc315ce334490d1dca1ae8603ce6905b8ea46a0750cd60ffa702815bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:d5288bf07359d1a92f6ae3333f2fec4eddc429dd253619d5db7394448df1fe42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212169620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08514670a8a0e2d7393eb92d8355d2323bc3aa9a8a38570af6d3fc4ed2e19386`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:42:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:54:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 22:55:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 22:55:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 22:55:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 22:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 22:57:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 22:57:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 22:57:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806bc8c3926ddb263b6e70eea4ef851e3f5bd20b4b6b9c1735d783a6bf212115`  
		Last Modified: Thu, 03 Mar 2022 21:55:36 GMT  
		Size: 1.2 MB (1182245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e57c84e6c44fa22daf7b317eb8bea7b772833f073035f421fa3cc74d5625e`  
		Last Modified: Thu, 03 Mar 2022 23:22:36 GMT  
		Size: 5.5 MB (5546634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa2eb54a60c95c61cac397efee2b5089a064ea4104b9c9f94d336c5d9f1009c`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555a91022cf7c6850417f6ff058a465ac1bd1cae9c7d0704f47478e73cfa33f4`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efac7f5755be9906320c0f5e560ea6363658d90e82bc42daaeba16dcc711261`  
		Last Modified: Thu, 03 Mar 2022 23:23:14 GMT  
		Size: 176.9 MB (176872576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ad681eea6d61da84250457ef45a6d442d9141b20917de50aef3186eae3a835`  
		Last Modified: Thu, 03 Mar 2022 23:22:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:a78462b673b8587f7341890f90c3240e321f18022c101c46d2d665ea478f350f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187350115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5ca30f9ece0cdcbbfde22d3bf7182e7a86a841d28a9ca8953997d47e4ae1cf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:13:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:13:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 02 Feb 2022 03:13:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 02 Feb 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 02 Feb 2022 03:13:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 02 Feb 2022 03:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:16:34 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Wed, 02 Feb 2022 03:16:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 02 Feb 2022 03:16:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a00403b45dfef687f4d96b9d93b7f1faa1e085fb7f5399ad1c4d3972e22a33`  
		Last Modified: Wed, 02 Feb 2022 03:38:13 GMT  
		Size: 1.2 MB (1183495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a346b5c6873a995df2c12469d7464f1596cd61c00168c869711d291cca1ec3`  
		Last Modified: Wed, 02 Feb 2022 03:38:12 GMT  
		Size: 4.7 MB (4676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e808252a53ad64e27c8579a98ad066591cde96558c55174e369563ff274d9`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dcf23ebea83b29129e099a6c06b92b159629f1a1ccb3e8f6d1c397ab636e60`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad2830e8dc1eab49942f83118bc7e7a2944da39923442cba83579a95d65800`  
		Last Modified: Wed, 02 Feb 2022 03:40:15 GMT  
		Size: 157.4 MB (157424599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d228b695dfcd78c5d1f360dd4e57b204b5933003cf3f1c8b449f5d8c3d8e40df`  
		Last Modified: Wed, 02 Feb 2022 03:38:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1f51dc332d38278d7ff86c87f16d64fd180365182b56f98010c9ffc13fb93680
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204989514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389444e501305edacd8c96409ec5d352876c401d8d531d3a316628b65935d120`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:20:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:21:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 03 Mar 2022 21:21:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:21:22 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:21:23 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:21:24 GMT
ENV ROS_DISTRO=noetic
# Thu, 03 Mar 2022 21:22:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:22:25 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 03 Mar 2022 21:22:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:22:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd8981cd7d2c5bf9f1c828fbedc2a414b627398ea4b1ca1e3f66f57961431b`  
		Last Modified: Thu, 03 Mar 2022 21:41:22 GMT  
		Size: 1.2 MB (1184037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b34d9665c53450354ca2f7756e3b4c83e8ed6f29c26b1b08c4e58134ccce9`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 5.3 MB (5322186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54752882ed071296a46e72950c5e1b88248ba0e41ce80c263963f712ba2b45a3`  
		Last Modified: Thu, 03 Mar 2022 21:41:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0170018ba4cd75abace305ee5159a76d7abd735e28da2bf530450ddadcb5928`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f5e9ca0b6a3e0d08fc9136d85b1314861557ec85d8f7a584f851355769c7e3`  
		Last Modified: Thu, 03 Mar 2022 21:41:49 GMT  
		Size: 171.3 MB (171311291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f39b2afd66a521f7c47bae6770d4670b853ae088b73c09d51cb5179abf9cab2`  
		Last Modified: Thu, 03 Mar 2022 21:41:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:f8484b4f1ae03c8f5e0bd1e4b5c8cba6c905c5854770e5c79d4c615722680ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:38d0eda59074a76c2fedabc17e427a77f20a382ad5134a0598d41f3aa6f32af8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281486234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9b430563473d41dfe87af5f554ec8a99c1fe055ea18e2d8f40a036f90c5e95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:48 GMT
ADD file:9819681ee3999b437c13bff560a32c11eff16275eebf27adae84e96bcd687c87 in / 
# Thu, 03 Mar 2022 20:19:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:13:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:14:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 23:16:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:16:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:16:49 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:18:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:18:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:18:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:19:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9e826c39a5168edf554e8eafc809c69b421ddb67d281f317701f2e68286572e`  
		Last Modified: Thu, 03 Mar 2022 20:21:20 GMT  
		Size: 30.5 MB (30494980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4dc87efafd76095187b9b08077be01b83bde15c579cfe05bbab1b3f63d7a15`  
		Last Modified: Thu, 03 Mar 2022 23:28:43 GMT  
		Size: 1.2 MB (1192034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3b3f063c560dae631f46501c2c2ed1bf5c561f9798967a66da02c749e05ec`  
		Last Modified: Thu, 03 Mar 2022 23:28:41 GMT  
		Size: 3.8 MB (3827015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c343a4279e03a0022358b546056ce7f7e9b4b77cef16db7afc0015666a941f27`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af60ffccd86a7ef972999007193d41e24dddc29c85ab84f305447dbb54d65d6`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f7fbe0ba4f2f696faf33efcff82102506241eb673f48aa1952c167e345326`  
		Last Modified: Thu, 03 Mar 2022 23:29:07 GMT  
		Size: 121.5 MB (121532323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4ac8443dc7c2edded48c4c8264b4a51695b9faa55a0238605be85b5241623d`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead5a34546f8900cda4e9de96e9cd4a7a650d5be1f5949942016571a4244032`  
		Last Modified: Thu, 03 Mar 2022 23:29:33 GMT  
		Size: 101.4 MB (101445856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca5b6585cca9cbb05be933a805b52aae270c65c73d7ef24f9ee011077f40b11`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 265.2 KB (265159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e91f5eb941c683c8d2b964e8d20709acdb6ea51277119e994ee237e60a961`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5835613a889cfce3aa74a609f078371294f96cc09e3d67b30d8ba77d03333f`  
		Last Modified: Thu, 03 Mar 2022 23:29:22 GMT  
		Size: 22.7 MB (22724265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89f4fcdebd12236d4a9d6b9bd92aee24307c8bb21390fc29512f6e533416537b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274639882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ecb26d0b4a8988881ba584fed194d12808f67b77c86b80937ec3a3514c942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:34:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:35:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:35:09 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:35:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:35:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 21:36:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:36:11 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:36:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:36:13 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:36:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:37:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:37:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913010b6995b5164a1549824b8740252b134f42bdbfd66c186edd8996fe831cc`  
		Last Modified: Thu, 03 Mar 2022 21:46:54 GMT  
		Size: 1.2 MB (1194373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89fb22e35ba47ea1110fdb11cb4cb95a691245ed9e2a91a3a7b58fa5b8dc01c`  
		Last Modified: Thu, 03 Mar 2022 21:46:52 GMT  
		Size: 3.6 MB (3594847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d16bcb793950fd11553a33ebaeecb9e7bfb47ece6a96be98044a4f1ce9e0834`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfb4c8069516cf1840c780cf0b359af1585479edbc36ca828f5fea5be4e8c2d`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adbc630fc1669a96b7ac2781a007e4aac2b3c4bc418bee6825d38ad9d5fe64c`  
		Last Modified: Thu, 03 Mar 2022 21:47:10 GMT  
		Size: 120.3 MB (120269595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871d52e65e8c1899c5818fd43e766b4c3660974b4ab50336f98156616d4f3142`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fa110d993e661579fc2549e60076ef96c7596fd264edeccb0e9bb4bee943a5`  
		Last Modified: Thu, 03 Mar 2022 21:47:36 GMT  
		Size: 98.8 MB (98753517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4259e629fc55157753363b5dc198f34af61fc52b31cc34e309d23c49701431e6`  
		Last Modified: Thu, 03 Mar 2022 21:47:22 GMT  
		Size: 265.1 KB (265110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e145d15a9076a5707c76250e341ffa4ad41ec8e5d686c0f851caab37e3a8aa4a`  
		Last Modified: Thu, 03 Mar 2022 21:47:21 GMT  
		Size: 2.2 KB (2155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c843328f781595a670b1eb748b22e0a2b1190545a3c7f305724f1ec54ef9daf`  
		Last Modified: Thu, 03 Mar 2022 21:47:25 GMT  
		Size: 22.1 MB (22133207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:f8484b4f1ae03c8f5e0bd1e4b5c8cba6c905c5854770e5c79d4c615722680ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:38d0eda59074a76c2fedabc17e427a77f20a382ad5134a0598d41f3aa6f32af8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281486234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9b430563473d41dfe87af5f554ec8a99c1fe055ea18e2d8f40a036f90c5e95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:48 GMT
ADD file:9819681ee3999b437c13bff560a32c11eff16275eebf27adae84e96bcd687c87 in / 
# Thu, 03 Mar 2022 20:19:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:13:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:14:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 23:16:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:16:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:16:49 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:18:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:18:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:18:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:19:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9e826c39a5168edf554e8eafc809c69b421ddb67d281f317701f2e68286572e`  
		Last Modified: Thu, 03 Mar 2022 20:21:20 GMT  
		Size: 30.5 MB (30494980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4dc87efafd76095187b9b08077be01b83bde15c579cfe05bbab1b3f63d7a15`  
		Last Modified: Thu, 03 Mar 2022 23:28:43 GMT  
		Size: 1.2 MB (1192034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3b3f063c560dae631f46501c2c2ed1bf5c561f9798967a66da02c749e05ec`  
		Last Modified: Thu, 03 Mar 2022 23:28:41 GMT  
		Size: 3.8 MB (3827015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c343a4279e03a0022358b546056ce7f7e9b4b77cef16db7afc0015666a941f27`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af60ffccd86a7ef972999007193d41e24dddc29c85ab84f305447dbb54d65d6`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f7fbe0ba4f2f696faf33efcff82102506241eb673f48aa1952c167e345326`  
		Last Modified: Thu, 03 Mar 2022 23:29:07 GMT  
		Size: 121.5 MB (121532323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4ac8443dc7c2edded48c4c8264b4a51695b9faa55a0238605be85b5241623d`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead5a34546f8900cda4e9de96e9cd4a7a650d5be1f5949942016571a4244032`  
		Last Modified: Thu, 03 Mar 2022 23:29:33 GMT  
		Size: 101.4 MB (101445856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca5b6585cca9cbb05be933a805b52aae270c65c73d7ef24f9ee011077f40b11`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 265.2 KB (265159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e91f5eb941c683c8d2b964e8d20709acdb6ea51277119e994ee237e60a961`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5835613a889cfce3aa74a609f078371294f96cc09e3d67b30d8ba77d03333f`  
		Last Modified: Thu, 03 Mar 2022 23:29:22 GMT  
		Size: 22.7 MB (22724265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89f4fcdebd12236d4a9d6b9bd92aee24307c8bb21390fc29512f6e533416537b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274639882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ecb26d0b4a8988881ba584fed194d12808f67b77c86b80937ec3a3514c942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:34:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:35:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:35:09 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:35:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:35:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 21:36:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:36:11 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:36:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:36:13 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:36:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:37:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:37:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913010b6995b5164a1549824b8740252b134f42bdbfd66c186edd8996fe831cc`  
		Last Modified: Thu, 03 Mar 2022 21:46:54 GMT  
		Size: 1.2 MB (1194373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89fb22e35ba47ea1110fdb11cb4cb95a691245ed9e2a91a3a7b58fa5b8dc01c`  
		Last Modified: Thu, 03 Mar 2022 21:46:52 GMT  
		Size: 3.6 MB (3594847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d16bcb793950fd11553a33ebaeecb9e7bfb47ece6a96be98044a4f1ce9e0834`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfb4c8069516cf1840c780cf0b359af1585479edbc36ca828f5fea5be4e8c2d`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adbc630fc1669a96b7ac2781a007e4aac2b3c4bc418bee6825d38ad9d5fe64c`  
		Last Modified: Thu, 03 Mar 2022 21:47:10 GMT  
		Size: 120.3 MB (120269595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871d52e65e8c1899c5818fd43e766b4c3660974b4ab50336f98156616d4f3142`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fa110d993e661579fc2549e60076ef96c7596fd264edeccb0e9bb4bee943a5`  
		Last Modified: Thu, 03 Mar 2022 21:47:36 GMT  
		Size: 98.8 MB (98753517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4259e629fc55157753363b5dc198f34af61fc52b31cc34e309d23c49701431e6`  
		Last Modified: Thu, 03 Mar 2022 21:47:22 GMT  
		Size: 265.1 KB (265110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e145d15a9076a5707c76250e341ffa4ad41ec8e5d686c0f851caab37e3a8aa4a`  
		Last Modified: Thu, 03 Mar 2022 21:47:21 GMT  
		Size: 2.2 KB (2155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c843328f781595a670b1eb748b22e0a2b1190545a3c7f305724f1ec54ef9daf`  
		Last Modified: Thu, 03 Mar 2022 21:47:25 GMT  
		Size: 22.1 MB (22133207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:f8484b4f1ae03c8f5e0bd1e4b5c8cba6c905c5854770e5c79d4c615722680ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:38d0eda59074a76c2fedabc17e427a77f20a382ad5134a0598d41f3aa6f32af8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281486234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9b430563473d41dfe87af5f554ec8a99c1fe055ea18e2d8f40a036f90c5e95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:48 GMT
ADD file:9819681ee3999b437c13bff560a32c11eff16275eebf27adae84e96bcd687c87 in / 
# Thu, 03 Mar 2022 20:19:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:13:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:14:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 23:16:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:16:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:16:49 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:18:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:18:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 23:18:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 23:19:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9e826c39a5168edf554e8eafc809c69b421ddb67d281f317701f2e68286572e`  
		Last Modified: Thu, 03 Mar 2022 20:21:20 GMT  
		Size: 30.5 MB (30494980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4dc87efafd76095187b9b08077be01b83bde15c579cfe05bbab1b3f63d7a15`  
		Last Modified: Thu, 03 Mar 2022 23:28:43 GMT  
		Size: 1.2 MB (1192034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3b3f063c560dae631f46501c2c2ed1bf5c561f9798967a66da02c749e05ec`  
		Last Modified: Thu, 03 Mar 2022 23:28:41 GMT  
		Size: 3.8 MB (3827015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c343a4279e03a0022358b546056ce7f7e9b4b77cef16db7afc0015666a941f27`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af60ffccd86a7ef972999007193d41e24dddc29c85ab84f305447dbb54d65d6`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f7fbe0ba4f2f696faf33efcff82102506241eb673f48aa1952c167e345326`  
		Last Modified: Thu, 03 Mar 2022 23:29:07 GMT  
		Size: 121.5 MB (121532323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4ac8443dc7c2edded48c4c8264b4a51695b9faa55a0238605be85b5241623d`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ead5a34546f8900cda4e9de96e9cd4a7a650d5be1f5949942016571a4244032`  
		Last Modified: Thu, 03 Mar 2022 23:29:33 GMT  
		Size: 101.4 MB (101445856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca5b6585cca9cbb05be933a805b52aae270c65c73d7ef24f9ee011077f40b11`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 265.2 KB (265159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e91f5eb941c683c8d2b964e8d20709acdb6ea51277119e994ee237e60a961`  
		Last Modified: Thu, 03 Mar 2022 23:29:17 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5835613a889cfce3aa74a609f078371294f96cc09e3d67b30d8ba77d03333f`  
		Last Modified: Thu, 03 Mar 2022 23:29:22 GMT  
		Size: 22.7 MB (22724265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89f4fcdebd12236d4a9d6b9bd92aee24307c8bb21390fc29512f6e533416537b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274639882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12ecb26d0b4a8988881ba584fed194d12808f67b77c86b80937ec3a3514c942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:34:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:35:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:35:09 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:35:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:35:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 21:36:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:36:11 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:36:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:36:13 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:36:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:37:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 03 Mar 2022 21:37:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 03 Mar 2022 21:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913010b6995b5164a1549824b8740252b134f42bdbfd66c186edd8996fe831cc`  
		Last Modified: Thu, 03 Mar 2022 21:46:54 GMT  
		Size: 1.2 MB (1194373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89fb22e35ba47ea1110fdb11cb4cb95a691245ed9e2a91a3a7b58fa5b8dc01c`  
		Last Modified: Thu, 03 Mar 2022 21:46:52 GMT  
		Size: 3.6 MB (3594847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d16bcb793950fd11553a33ebaeecb9e7bfb47ece6a96be98044a4f1ce9e0834`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfb4c8069516cf1840c780cf0b359af1585479edbc36ca828f5fea5be4e8c2d`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adbc630fc1669a96b7ac2781a007e4aac2b3c4bc418bee6825d38ad9d5fe64c`  
		Last Modified: Thu, 03 Mar 2022 21:47:10 GMT  
		Size: 120.3 MB (120269595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871d52e65e8c1899c5818fd43e766b4c3660974b4ab50336f98156616d4f3142`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fa110d993e661579fc2549e60076ef96c7596fd264edeccb0e9bb4bee943a5`  
		Last Modified: Thu, 03 Mar 2022 21:47:36 GMT  
		Size: 98.8 MB (98753517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4259e629fc55157753363b5dc198f34af61fc52b31cc34e309d23c49701431e6`  
		Last Modified: Thu, 03 Mar 2022 21:47:22 GMT  
		Size: 265.1 KB (265110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e145d15a9076a5707c76250e341ffa4ad41ec8e5d686c0f851caab37e3a8aa4a`  
		Last Modified: Thu, 03 Mar 2022 21:47:21 GMT  
		Size: 2.2 KB (2155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c843328f781595a670b1eb748b22e0a2b1190545a3c7f305724f1ec54ef9daf`  
		Last Modified: Thu, 03 Mar 2022 21:47:25 GMT  
		Size: 22.1 MB (22133207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:63e9e99c3b05bfecd088d098c62b89e35bde93e2e3a132ce9881595ab1513427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:18a5e1a66a17f012c48465ec3d6af2defd495e33b8cf5516a3b508f29e6dea70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157048767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54cc4f069f109a484a13840fb28d8ce7bb8410e41da083e163285dbb68832af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:48 GMT
ADD file:9819681ee3999b437c13bff560a32c11eff16275eebf27adae84e96bcd687c87 in / 
# Thu, 03 Mar 2022 20:19:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:13:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:14:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 23:16:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:16:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:16:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b9e826c39a5168edf554e8eafc809c69b421ddb67d281f317701f2e68286572e`  
		Last Modified: Thu, 03 Mar 2022 20:21:20 GMT  
		Size: 30.5 MB (30494980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4dc87efafd76095187b9b08077be01b83bde15c579cfe05bbab1b3f63d7a15`  
		Last Modified: Thu, 03 Mar 2022 23:28:43 GMT  
		Size: 1.2 MB (1192034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3b3f063c560dae631f46501c2c2ed1bf5c561f9798967a66da02c749e05ec`  
		Last Modified: Thu, 03 Mar 2022 23:28:41 GMT  
		Size: 3.8 MB (3827015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c343a4279e03a0022358b546056ce7f7e9b4b77cef16db7afc0015666a941f27`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af60ffccd86a7ef972999007193d41e24dddc29c85ab84f305447dbb54d65d6`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f7fbe0ba4f2f696faf33efcff82102506241eb673f48aa1952c167e345326`  
		Last Modified: Thu, 03 Mar 2022 23:29:07 GMT  
		Size: 121.5 MB (121532323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4ac8443dc7c2edded48c4c8264b4a51695b9faa55a0238605be85b5241623d`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bc7955d291b0751463181a4b33562cd75f6c951543abb23ce21866e5603b0068
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153485893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efc2a70e5ba2f0e64350096fd50366ef42dce1aaa266f72cbd5caab6d2e5767`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:34:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:35:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:35:09 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:35:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:35:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 21:36:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:36:11 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:36:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:36:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913010b6995b5164a1549824b8740252b134f42bdbfd66c186edd8996fe831cc`  
		Last Modified: Thu, 03 Mar 2022 21:46:54 GMT  
		Size: 1.2 MB (1194373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89fb22e35ba47ea1110fdb11cb4cb95a691245ed9e2a91a3a7b58fa5b8dc01c`  
		Last Modified: Thu, 03 Mar 2022 21:46:52 GMT  
		Size: 3.6 MB (3594847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d16bcb793950fd11553a33ebaeecb9e7bfb47ece6a96be98044a4f1ce9e0834`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfb4c8069516cf1840c780cf0b359af1585479edbc36ca828f5fea5be4e8c2d`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adbc630fc1669a96b7ac2781a007e4aac2b3c4bc418bee6825d38ad9d5fe64c`  
		Last Modified: Thu, 03 Mar 2022 21:47:10 GMT  
		Size: 120.3 MB (120269595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871d52e65e8c1899c5818fd43e766b4c3660974b4ab50336f98156616d4f3142`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:63e9e99c3b05bfecd088d098c62b89e35bde93e2e3a132ce9881595ab1513427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:18a5e1a66a17f012c48465ec3d6af2defd495e33b8cf5516a3b508f29e6dea70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157048767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54cc4f069f109a484a13840fb28d8ce7bb8410e41da083e163285dbb68832af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:48 GMT
ADD file:9819681ee3999b437c13bff560a32c11eff16275eebf27adae84e96bcd687c87 in / 
# Thu, 03 Mar 2022 20:19:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:13:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:14:18 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 23:14:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 23:14:38 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 23:16:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:16:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 23:16:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 23:16:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b9e826c39a5168edf554e8eafc809c69b421ddb67d281f317701f2e68286572e`  
		Last Modified: Thu, 03 Mar 2022 20:21:20 GMT  
		Size: 30.5 MB (30494980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4dc87efafd76095187b9b08077be01b83bde15c579cfe05bbab1b3f63d7a15`  
		Last Modified: Thu, 03 Mar 2022 23:28:43 GMT  
		Size: 1.2 MB (1192034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3b3f063c560dae631f46501c2c2ed1bf5c561f9798967a66da02c749e05ec`  
		Last Modified: Thu, 03 Mar 2022 23:28:41 GMT  
		Size: 3.8 MB (3827015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c343a4279e03a0022358b546056ce7f7e9b4b77cef16db7afc0015666a941f27`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af60ffccd86a7ef972999007193d41e24dddc29c85ab84f305447dbb54d65d6`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f7fbe0ba4f2f696faf33efcff82102506241eb673f48aa1952c167e345326`  
		Last Modified: Thu, 03 Mar 2022 23:29:07 GMT  
		Size: 121.5 MB (121532323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4ac8443dc7c2edded48c4c8264b4a51695b9faa55a0238605be85b5241623d`  
		Last Modified: Thu, 03 Mar 2022 23:28:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bc7955d291b0751463181a4b33562cd75f6c951543abb23ce21866e5603b0068
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153485893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efc2a70e5ba2f0e64350096fd50366ef42dce1aaa266f72cbd5caab6d2e5767`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:34:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:34:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 03 Mar 2022 21:35:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 03 Mar 2022 21:35:09 GMT
ENV LANG=C.UTF-8
# Thu, 03 Mar 2022 21:35:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 03 Mar 2022 21:35:11 GMT
ENV ROS_DISTRO=rolling
# Thu, 03 Mar 2022 21:36:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:36:11 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 03 Mar 2022 21:36:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 03 Mar 2022 21:36:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913010b6995b5164a1549824b8740252b134f42bdbfd66c186edd8996fe831cc`  
		Last Modified: Thu, 03 Mar 2022 21:46:54 GMT  
		Size: 1.2 MB (1194373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89fb22e35ba47ea1110fdb11cb4cb95a691245ed9e2a91a3a7b58fa5b8dc01c`  
		Last Modified: Thu, 03 Mar 2022 21:46:52 GMT  
		Size: 3.6 MB (3594847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d16bcb793950fd11553a33ebaeecb9e7bfb47ece6a96be98044a4f1ce9e0834`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfb4c8069516cf1840c780cf0b359af1585479edbc36ca828f5fea5be4e8c2d`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adbc630fc1669a96b7ac2781a007e4aac2b3c4bc418bee6825d38ad9d5fe64c`  
		Last Modified: Thu, 03 Mar 2022 21:47:10 GMT  
		Size: 120.3 MB (120269595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871d52e65e8c1899c5818fd43e766b4c3660974b4ab50336f98156616d4f3142`  
		Last Modified: Thu, 03 Mar 2022 21:46:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
