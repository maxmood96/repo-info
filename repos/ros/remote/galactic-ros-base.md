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
