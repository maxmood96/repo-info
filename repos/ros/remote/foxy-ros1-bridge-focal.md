## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:3df748a354582095c6d1a9263027bacd179cdf828157534d6442635095d8c356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:d0dca420c0e34068187d847e901f1b7ad8a453144bcc1ff331c67ee99ed60b0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354556761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1455d101c5c71ff7bf511dfd66d07a8691f54dc2aea6233dad8243b3b8f76aea`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 02:08:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:04:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:55:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:55:18 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:55:18 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:55:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:55:18 GMT
ENV ROS_DISTRO=foxy
# Sat, 09 Dec 2023 03:57:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:57:23 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:57:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:57:23 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:58:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:58:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:58:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:59:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:59:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:59:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:59:35 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 03:59:35 GMT
ENV ROS2_DISTRO=foxy
# Sat, 09 Dec 2023 04:01:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:01:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:01:34 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1327734170da8c4ae4171fb4248189d0691d6b4a3f01b09239c3e34688651`  
		Last Modified: Sat, 02 Dec 2023 02:20:57 GMT  
		Size: 1.2 MB (1198788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77125e61032dbbcd43c015fe756de97b5661bdbbf4f5219588148f651ae900c1`  
		Last Modified: Sat, 02 Dec 2023 05:59:34 GMT  
		Size: 5.6 MB (5553989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cfdb297cb2e56f5144d6a03d94e416f7101347779b1dac8d072ddb965d0b5`  
		Last Modified: Sat, 09 Dec 2023 04:49:40 GMT  
		Size: 3.6 KB (3622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8d76fdc12cd19e368e2e5b21e5d481559248fe3c64da35af018355d18977f`  
		Last Modified: Sat, 09 Dec 2023 04:49:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf35df53ba113fe177d0183f4f445e060ccef226ed32cd3aa6f3f4f4de6774d`  
		Last Modified: Sat, 09 Dec 2023 04:50:06 GMT  
		Size: 125.5 MB (125548513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756e62193488345e83b7f3bc2f2f5886a4e5f412e64e38fa594af820c9163a82`  
		Last Modified: Sat, 09 Dec 2023 04:49:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cebe9015ddead423a6b6692f059bcec1ee4a7135ac384b80dfddfd44c52f05`  
		Last Modified: Sat, 09 Dec 2023 04:50:25 GMT  
		Size: 73.5 MB (73519978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd79866e649ea889791009144a2b64171483730cbc5851b85dadfe2dccc0d3`  
		Last Modified: Sat, 09 Dec 2023 04:50:14 GMT  
		Size: 271.1 KB (271061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29aa10f749f0e3485f98a7d6b1d1cc10f3c1165d1bf4afee0905d2aff8744e2e`  
		Last Modified: Sat, 09 Dec 2023 04:50:14 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74769e56d216fe1fa3364194dbaf8bdff6904a92bf9947f4e9255eb7f2368db`  
		Last Modified: Sat, 09 Dec 2023 04:50:18 GMT  
		Size: 21.7 MB (21683234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057ff5f003438bbf1a70b54ad3107bf12e5b462d8a68fc840e4d9dcd45138f2d`  
		Last Modified: Sat, 09 Dec 2023 04:50:36 GMT  
		Size: 5.4 KB (5404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbbc004a620e1e7fdfba67fe5bb2771bfa5d70dc58cf73166680dd158a889ee`  
		Last Modified: Sat, 09 Dec 2023 04:50:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71f7f8c767245b2da788a8cf7dceea44db9385146db02309651a27bd5cd3a2`  
		Last Modified: Sat, 09 Dec 2023 04:50:56 GMT  
		Size: 76.5 MB (76492172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57cdbb28b729ddfa83268c455ba85c6e54031fa38d939dff072bfd24873d32`  
		Last Modified: Sat, 09 Dec 2023 04:50:41 GMT  
		Size: 21.7 MB (21692589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c741ae3129549281c8610a35bfe3e10b39f0874fae2d38987b04a2063d2e6a4a`  
		Last Modified: Sat, 09 Dec 2023 04:50:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d1a6c46f9a144df8fff76353189b6acf19dd65ef1b487758a56b7960266d7347
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322212818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc6569dc3c3df330b1505026894f9f64ef725899f310877ea859d9511057c35`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:21:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:18:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:18:16 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:18:17 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:18:17 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:18:17 GMT
ENV ROS_DISTRO=foxy
# Sat, 09 Dec 2023 03:20:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:20:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:20:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:20:29 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:21:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:21:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:21:30 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:22:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:22:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:22:32 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 03:22:32 GMT
ENV ROS2_DISTRO=foxy
# Sat, 09 Dec 2023 03:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:24:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:24:03 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:5d2acf9ee7cfde47b6ce997317767b8fa9bf8d93b8297016db9e093d06aa913d`  
		Last Modified: Wed, 29 Nov 2023 17:47:09 GMT  
		Size: 27.2 MB (27203865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2aa78ed8ad18394d7ae521e83b2810fec9fbb7d95aa074d794bb43e6e2bbfb`  
		Last Modified: Sat, 02 Dec 2023 06:56:12 GMT  
		Size: 1.2 MB (1198781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f106a95fef578814e019c4ac69f1cf32b15d5f85da2729a7ab2487c5d3505d`  
		Last Modified: Sat, 02 Dec 2023 06:56:11 GMT  
		Size: 5.5 MB (5532202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2293949a62535f558d267574d694fe0b0e9498fce13b94a8a2e83b00a4d86669`  
		Last Modified: Sat, 09 Dec 2023 04:05:04 GMT  
		Size: 3.6 KB (3625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a9aa07ed44d01bc5e93b12e2d7956a74afaa4429287652b3977b63f637eb95`  
		Last Modified: Sat, 09 Dec 2023 04:05:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c6bf64f4814b4883be6b658102c6e1626f806dd4da742884c5abaee2a0ef41`  
		Last Modified: Sat, 09 Dec 2023 04:05:26 GMT  
		Size: 108.9 MB (108868171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690afa1d3835689299293b326bad874dae11c7272f40b31361519f157bafc83d`  
		Last Modified: Sat, 09 Dec 2023 04:05:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7872575e51da68e3230da2c297adc491d124bf859b36958f1bbb8426f35ba1be`  
		Last Modified: Sat, 09 Dec 2023 04:05:43 GMT  
		Size: 67.9 MB (67873751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc82c8b47ed2a55171cb49066a548ce009f33651de5c18b9dc2086aabacfadc`  
		Last Modified: Sat, 09 Dec 2023 04:05:35 GMT  
		Size: 271.1 KB (271064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda9fbaf443befc328955ce52a4dd2c785013d6799696a4312ceb7d63ac4649`  
		Last Modified: Sat, 09 Dec 2023 04:05:34 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e0e60e385c86f6ec04d573e8b226dc2ba301f5c10fdf44e7abb07e631cfaec`  
		Last Modified: Sat, 09 Dec 2023 04:05:38 GMT  
		Size: 20.4 MB (20408514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4172bb37850053590c8bbf0338196240ede633d066a382295a21572b1fc8b`  
		Last Modified: Sat, 09 Dec 2023 04:05:55 GMT  
		Size: 5.4 KB (5403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c292a706f58ad87895b431b677d07c737296e8c792c8c10511ee7a5de6c971c0`  
		Last Modified: Sat, 09 Dec 2023 04:05:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a2e04f638e8e4d5c997363cd45c5a87919e4bc2b68a9b96359ce78a414bfdd`  
		Last Modified: Sat, 09 Dec 2023 04:06:14 GMT  
		Size: 76.5 MB (76512109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3ed3d56043a07cf4529a0f627c33bb37cb2dee51fbae9033aacaf67a91297a`  
		Last Modified: Sat, 09 Dec 2023 04:05:59 GMT  
		Size: 14.3 MB (14331997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd141cd9a723fb1f5d673bb205f80a3201cb973960b759d0f8fd8c7faafd91a0`  
		Last Modified: Sat, 09 Dec 2023 04:05:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
