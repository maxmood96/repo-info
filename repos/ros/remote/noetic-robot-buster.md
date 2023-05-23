## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:dea046940a33c8f840da6a8b99b8660b2f51262f08c730d4fb2a593bd7f5d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:e5604709b3f5862b2097a59f1f4a1754fc7d66c76dba74f400dcd419a39b2dee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484664813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4939ec85a47f7963a6fbcd92ea15d32e2496a014830f0d96fb9c9c7b8713cf3d`
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
# Tue, 23 May 2023 11:18:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:6bfbde6cb3940c9f25d3d8b254c953b15987d125e895c848c75d3001d090e6b8`  
		Last Modified: Tue, 23 May 2023 11:24:40 GMT  
		Size: 21.2 MB (21156977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:50bb12073608fc106b929a22e72e30d3ffa649fab34d075bb37895a9b25dd406
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424196844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e7980c8f20e0b28634d551d75871da9017c1421a0d3a4fe5bb53f69112944`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:21 GMT
ADD file:a5100e7ed3c2665c1b4dfbb32eb2b47b85783f2a6800e0ae9004db0ce021dfa5 in / 
# Tue, 23 May 2023 00:43:22 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:09:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:09:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 May 2023 07:09:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 May 2023 07:09:55 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 07:09:55 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 May 2023 07:09:55 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 May 2023 07:11:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:11:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 May 2023 07:11:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 May 2023 07:11:26 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:11:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:12:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 23 May 2023 07:13:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:13:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5ea482247e9a0d1ae4ed218fb0828063b9cce53822e64fd4621f587ab85a7e6d`  
		Last Modified: Tue, 23 May 2023 00:46:24 GMT  
		Size: 49.2 MB (49238292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62aacc6d8d227c977953e480d4a68a0de585d973ccb199b674eb74cfae11ac6`  
		Last Modified: Tue, 23 May 2023 07:18:45 GMT  
		Size: 10.9 MB (10902726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44af36709d88eec5e6f50342c165ae44b26b6b1697b4445ad71fcde5bb66f72d`  
		Last Modified: Tue, 23 May 2023 07:18:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf23de21b4a8076854c4b81c2da993b3eb5504eb2993919efc62d70f024cc8f`  
		Last Modified: Tue, 23 May 2023 07:18:44 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e704756b8ca302bb92f857a7f79fa9bbe4245d11fd39fa2b48ad558d5ce859c`  
		Last Modified: Tue, 23 May 2023 07:19:05 GMT  
		Size: 184.5 MB (184450768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5cdc9acd26d4497666808bec531405faf0715bad80e7d3c9b4e865a8d80609`  
		Last Modified: Tue, 23 May 2023 07:18:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e339807dcdea4df15d2c46a5d429937129828e8742a63c58e7e9cd6b79a5f209`  
		Last Modified: Tue, 23 May 2023 07:19:19 GMT  
		Size: 84.4 MB (84397050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8edf64563834cf13dd87b16e82ca48379a6c011de4f3d8240641dca72fb457`  
		Last Modified: Tue, 23 May 2023 07:19:12 GMT  
		Size: 293.6 KB (293598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8cbf35aa60a417abbe378d7ee172e069be9971caa123cc79f0999f8b248137`  
		Last Modified: Tue, 23 May 2023 07:19:19 GMT  
		Size: 74.1 MB (74090723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70618ae76a4d3e2c4d8d6217d970d9d4c457e88342c0b3601cc0fe71cfe514ef`  
		Last Modified: Tue, 23 May 2023 07:19:28 GMT  
		Size: 20.8 MB (20821276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
