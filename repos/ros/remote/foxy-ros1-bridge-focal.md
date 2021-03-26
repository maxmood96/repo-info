## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:845cee91c6814caadcb5ef546768ac014a079bab2c39feb5b49f6b36fe86166b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:9a6806a714436da157e76f5e37a209017695c944238c29bbc2177eca59a527ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340969919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b871f27726d575dad1051bf1261aff301e131826038d96501e0f5ba0d6a8c80`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:08 GMT
ADD file:a8d2f02fbaddf8cec8e4da320cd03c06435f395e9d454f69954efe422eb6e1ba in / 
# Thu, 25 Mar 2021 22:33:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 11:25:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:52:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:52:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 13:20:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Mar 2021 13:20:17 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 13:20:18 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 13:20:18 GMT
ENV ROS_DISTRO=foxy
# Fri, 26 Mar 2021 13:22:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:22:28 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 13:22:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 13:22:29 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:23:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:23:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 13:23:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Mar 2021 13:23:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:24:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 13:24:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 13:24:11 GMT
ENV ROS1_DISTRO=noetic
# Fri, 26 Mar 2021 13:24:11 GMT
ENV ROS2_DISTRO=foxy
# Fri, 26 Mar 2021 13:25:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:26:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:26:14 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:04a5f4cda3eea2313a61a2f72208342a57ea36a9326dff54f4f26ed47d145c7c`  
		Last Modified: Thu, 25 Mar 2021 22:34:46 GMT  
		Size: 28.6 MB (28569428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff496a88c8ed9b745dab2f00bfbd9013c6d1db198442a6a8683998a29a85458a`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce83f459fe7e0bf459d0c222ef3b2ca4d9911f6b0f9aae02c2120561b54ca18`  
		Last Modified: Thu, 25 Mar 2021 22:34:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4c238a927e44fc68e49f93b318a224102c5d7eed49fc3af359975559e12857`  
		Last Modified: Fri, 26 Mar 2021 11:46:19 GMT  
		Size: 1.2 MB (1182444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31284e097e1d0ebfe603632f456f1b3448f6f14c43b12ead735c6914fe702e0`  
		Last Modified: Fri, 26 Mar 2021 13:37:24 GMT  
		Size: 5.5 MB (5547694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d7646f67a7f499fee4f81d175005244721e2da4e7c26ca4043e71e31ecf316`  
		Last Modified: Fri, 26 Mar 2021 13:37:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bdc4b51bc40412fcaa260772905420e5f00507790e2e926d26be5e759fa190`  
		Last Modified: Fri, 26 Mar 2021 13:44:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f7f266847e24ead25f7ca2d87c21dd29a8f6143e5d9dfe25ea0b3388460aed`  
		Last Modified: Fri, 26 Mar 2021 13:45:13 GMT  
		Size: 119.9 MB (119904410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77037c0775c3d5d1819042c8624f8501491576b92d21d53fc5f1c883c63ac6c`  
		Last Modified: Fri, 26 Mar 2021 13:44:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87af5b1fd805242bb892d4d93dc3666a32627848de922718994a63a3909334e0`  
		Last Modified: Fri, 26 Mar 2021 13:45:37 GMT  
		Size: 66.6 MB (66602574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3db4ce63f166f2ae3862e249ba01f077653eab97603714027507709b2bf576`  
		Last Modified: Fri, 26 Mar 2021 13:45:24 GMT  
		Size: 215.6 KB (215615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb9842785bcc499396dd7b0a751086a2c6297c1d1b80cff88ae501d1ca96f8c`  
		Last Modified: Fri, 26 Mar 2021 13:45:24 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bccc089d5aec25757440842298d79739ede43c08521ddc08b3679f86a15a46`  
		Last Modified: Fri, 26 Mar 2021 13:45:29 GMT  
		Size: 10.3 MB (10282745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5465a129a0878be6e44550bae14c1e7e2a374bbc6412dd64b5e53f51b8536a5e`  
		Last Modified: Fri, 26 Mar 2021 13:45:54 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6bb4edee1b53219dbfa6abc45e0d39fff587fedd7a517d94cc2aaa42d11788`  
		Last Modified: Fri, 26 Mar 2021 13:45:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b062a880381ed051f43d28148408687cc040bedd2be66d09e7505c155517eeb`  
		Last Modified: Fri, 26 Mar 2021 13:46:15 GMT  
		Size: 76.1 MB (76114444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e1f7363dd472905461523e4d51e271bf5516b9279ceaab9fadc8b8b832f53d`  
		Last Modified: Fri, 26 Mar 2021 13:46:03 GMT  
		Size: 32.5 MB (32545041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97360b794752a0e1b0b234a3dcefcd53a02daa4c5a1c79f42901f88641f521f`  
		Last Modified: Fri, 26 Mar 2021 13:45:54 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:712330ddab9ae4214905f18dca4854ab41346c2d769a84b13997c4164c8ff7a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309616252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c26d74171fc6e62d2bac6a66cb44ff7de8ce7ae6878e4f065a81eb76cad513`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 23:22:32 GMT
ADD file:ee49f9e75d7f5923826cf089f2ac0100a27ef7051f10c31b310b573f9c26d91f in / 
# Thu, 25 Mar 2021 23:22:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:22:59 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:23:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:23:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:43:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:44:11 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:44:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 15:09:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Mar 2021 15:09:57 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 15:09:58 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 15:09:59 GMT
ENV ROS_DISTRO=foxy
# Fri, 26 Mar 2021 15:12:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:12:10 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 15:12:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 15:12:13 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:13:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:13:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 15:13:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Mar 2021 15:13:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:14:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 15:14:20 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 15:14:21 GMT
ENV ROS1_DISTRO=noetic
# Fri, 26 Mar 2021 15:14:22 GMT
ENV ROS2_DISTRO=foxy
# Fri, 26 Mar 2021 15:15:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.9-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:15:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:15:56 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:c5b23ab54a1c0bb81bfc8f1ef83601638d672cc89e3bd3d49290ecfe0834ea2f`  
		Last Modified: Thu, 25 Mar 2021 23:28:04 GMT  
		Size: 27.2 MB (27176798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de628c73ef9a73e299e0e05bce39612341c12b0907fb5a1f8e9a569631ad20c`  
		Last Modified: Thu, 25 Mar 2021 23:27:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61ee5c846071ed2213196ef64402731d6ed75cca1bb954645d89b53db8d2266`  
		Last Modified: Thu, 25 Mar 2021 23:27:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da2f3772e7d14f6c8dd92787d62ebcc31d2930ead31dc0a5b82c4462c3444ae`  
		Last Modified: Fri, 26 Mar 2021 15:27:30 GMT  
		Size: 1.2 MB (1183079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3209da98cad32d45c3b49245366b4b28933f6fc899ead421d14c9c30784bc235`  
		Last Modified: Fri, 26 Mar 2021 15:27:28 GMT  
		Size: 5.5 MB (5513254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf7f90a086ceae99b2f71d9ecb6b27ca9bf4412f7198bce0252b1f2d1903ad0`  
		Last Modified: Fri, 26 Mar 2021 15:27:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8238ce340fac0e12b439ee9e06f2f3dd9943e7b2eed79c2b74f442b23842c8d9`  
		Last Modified: Fri, 26 Mar 2021 15:36:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78a426e426e221718cc3228b118b077a444dc32e6ed643405b2ccf34f3d306a`  
		Last Modified: Fri, 26 Mar 2021 15:36:34 GMT  
		Size: 104.1 MB (104088975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dd9262c9ff647c08e920ac6102bb6e26339d60272dc99748e82a685003d4db`  
		Last Modified: Fri, 26 Mar 2021 15:36:05 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8add9b6435d6c19400171e19d7e13539a1fb672561a51d4c748526ad3862fa`  
		Last Modified: Fri, 26 Mar 2021 15:37:01 GMT  
		Size: 61.0 MB (60971344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dded4ffe8de749999b28aacb816d8b830594fbea44695193b9d81c7406adb2d9`  
		Last Modified: Fri, 26 Mar 2021 15:36:48 GMT  
		Size: 215.6 KB (215618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03b8e0dd3e10e02882b949915801fb9480aed81b5c812d181ba774f3dc5d8f`  
		Last Modified: Fri, 26 Mar 2021 15:36:46 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22b18e4010aa03b841154c27dc41926a4edafbfb0bec2399794e2b760cfc213`  
		Last Modified: Fri, 26 Mar 2021 15:36:52 GMT  
		Size: 9.3 MB (9298797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db375c4011cb3bb399979b4f97e852cd7fcc51f9d423cb67b776a8a50ddc1b5e`  
		Last Modified: Fri, 26 Mar 2021 15:37:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9279b29809f45542818228170269cbc164523ddac9e396537bf8ff033fc17985`  
		Last Modified: Fri, 26 Mar 2021 15:37:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf2e872289a6e32bf394f5a2058ee10dd0fbd7bd15af658bdcd126e80cc3e7c`  
		Last Modified: Fri, 26 Mar 2021 15:37:44 GMT  
		Size: 76.2 MB (76157822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19b35f3e5669c876372a9bfaec0b82e2382ea58f226c46233ba88e72e0eb60e`  
		Last Modified: Fri, 26 Mar 2021 15:37:23 GMT  
		Size: 25.0 MB (25005009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfef13cb182864ff0a4b9ac242076a9fada6a3aa68b34c62e7ec64b787ce957`  
		Last Modified: Fri, 26 Mar 2021 15:37:17 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
