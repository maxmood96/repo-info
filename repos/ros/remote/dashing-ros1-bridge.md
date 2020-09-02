## `ros:dashing-ros1-bridge`

```console
$ docker pull ros@sha256:1f3cf73916ccf28f2e12b0082a8bb851536a3002c41b10dd9b976ec3c0438710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:ae86dfef6e87fb1ece5ee271282fa61c32f5efbe99afefc280fdce90044d3009
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.5 MB (418522528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c1e4004ad9706dde9126086a2890285fcedbc7f149c339051582a9072c5d76`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:13:50 GMT
ADD file:5c125b7f411566e9daa738d8cb851098f36197810f06488c2609074296f294b2 in / 
# Wed, 19 Aug 2020 21:13:52 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:13:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:13:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:13:55 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:45:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:00:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:00:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 20 Aug 2020 00:21:29 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 20 Aug 2020 00:21:29 GMT
ENV LANG=C.UTF-8
# Thu, 20 Aug 2020 00:21:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 20 Aug 2020 00:21:29 GMT
ENV ROS_DISTRO=dashing
# Thu, 20 Aug 2020 00:23:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:23:18 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 20 Aug 2020 00:23:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 20 Aug 2020 00:23:19 GMT
CMD ["bash"]
# Thu, 20 Aug 2020 00:24:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:24:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 20 Aug 2020 00:24:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 20 Aug 2020 00:24:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:24:35 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 20 Aug 2020 00:24:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 20 Aug 2020 00:24:36 GMT
ENV ROS1_DISTRO=melodic
# Thu, 20 Aug 2020 00:24:36 GMT
ENV ROS2_DISTRO=dashing
# Tue, 01 Sep 2020 23:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.9-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 23:53:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 23:53:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 23:53:42 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:f08d8e2a3ba11bea23cf5c17e8e1c620057412ed05c32d1114640e18d6dd0a43`  
		Last Modified: Sat, 08 Aug 2020 12:21:16 GMT  
		Size: 26.7 MB (26700095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9cb2483bd9c5329a44d9c2fe72535625bbd4308bca95785dd58e72c06365`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e5ff4c0b1526abf77c236655f21c8f67a23313291c8b970fe6b469549d8153`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860925334f940c3145808527480b4f0cba7f01279087fdb27679e4354fba967`  
		Last Modified: Wed, 19 Aug 2020 21:16:44 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaa5f3004b43b04fcf57d7f29efd6191edc973046054cb1590c6c134fd4064d`  
		Last Modified: Wed, 19 Aug 2020 23:06:36 GMT  
		Size: 838.2 KB (838225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61a1a213ee0869dc0e68c035adc439944633af46f5812e47d6932677834acd6`  
		Last Modified: Thu, 20 Aug 2020 00:39:32 GMT  
		Size: 4.9 MB (4868690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2e3eccb0c48240ffede5da52708cb96dacd1972e92214fc59d902972e09ad`  
		Last Modified: Thu, 20 Aug 2020 00:39:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3736aed0c4e18d6ecc8cff6f5128a16e53acb2e3ecbcd7af51e31fd9503eb90a`  
		Last Modified: Thu, 20 Aug 2020 00:45:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d1a6d1f1ccd65b71c7351797567bfdabeffdf9e5e0377762ab2413985c67b3`  
		Last Modified: Thu, 20 Aug 2020 00:45:51 GMT  
		Size: 179.4 MB (179385080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0e60d56de9b0b1c0b76769e9ff21754939e0e75bfbe93ae6b862021af3548e`  
		Last Modified: Thu, 20 Aug 2020 00:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bc86677e1936f0291d166890955344abf6bee8cc54a6bd9c0646cb72ff6f1b`  
		Last Modified: Thu, 20 Aug 2020 00:46:07 GMT  
		Size: 64.1 MB (64124530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e45efa543e862ac42c53be3e8965ca6d99d13b0824e904adc2792cd9e51576`  
		Last Modified: Thu, 20 Aug 2020 00:45:55 GMT  
		Size: 187.6 KB (187581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedb75ea5fbecd53e659fd0db53a5a3d3ebc05a59dd02cb80ea1cae346476027`  
		Last Modified: Thu, 20 Aug 2020 00:45:55 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b427593adbb5cae22c1ae534cbd23bcf4570833f3abf57a66d5b9c65654718a`  
		Last Modified: Thu, 20 Aug 2020 00:45:57 GMT  
		Size: 4.3 MB (4312684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5223485c1d0052cf1c11642262baf9867bb175787bbfcec95e94d54a5e2097`  
		Last Modified: Thu, 20 Aug 2020 00:46:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16eb0965e68466e9bb229b85a232a19167129d8afd820378e8330e576914f79f`  
		Last Modified: Thu, 20 Aug 2020 00:46:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d374a93a132ca9224b8e5a947c6e0e46abc326808c5433e5f8a131a29413f8ee`  
		Last Modified: Tue, 01 Sep 2020 23:58:57 GMT  
		Size: 117.6 MB (117639357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab4052b3383a0736b128f50241650dab5bbecb901c91219a2373cf20d97b5fc`  
		Last Modified: Tue, 01 Sep 2020 23:58:41 GMT  
		Size: 19.8 MB (19787046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b98d2f793a1c45bbd2d9e44bb8ffaba11b3d705bbf6c4365ee526dd256400`  
		Last Modified: Tue, 01 Sep 2020 23:58:35 GMT  
		Size: 638.4 KB (638433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825653f7ae48a630c0a4759851304a5f2710febb1514ee2a788fa1e01920233`  
		Last Modified: Tue, 01 Sep 2020 23:58:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:afc9376292f0c3fb9885ae327b10345d9a4862f22034e4b687ab6521b23ecd54
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354681117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d5f91c754fe5c64832bd95fa6cb05f02ea348728a4c777b2981e1871940d15`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:45:03 GMT
ADD file:8369fef9339cb0f1b2b9660d860a6cbf4a5cd6c5e173fbb8cdf8b9485e56aaf4 in / 
# Wed, 19 Aug 2020 21:45:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:45:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:45:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:45:12 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:38:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:39:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:39:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 Aug 2020 23:00:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 19 Aug 2020 23:00:59 GMT
ENV LANG=C.UTF-8
# Wed, 19 Aug 2020 23:01:06 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 Aug 2020 23:01:11 GMT
ENV ROS_DISTRO=dashing
# Wed, 19 Aug 2020 23:03:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:03:35 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 19 Aug 2020 23:03:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 Aug 2020 23:03:37 GMT
CMD ["bash"]
# Wed, 19 Aug 2020 23:04:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:04:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 19 Aug 2020 23:04:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 19 Aug 2020 23:05:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:05:20 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 Aug 2020 23:05:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 Aug 2020 23:05:26 GMT
ENV ROS1_DISTRO=melodic
# Wed, 19 Aug 2020 23:05:27 GMT
ENV ROS2_DISTRO=dashing
# Wed, 02 Sep 2020 07:02:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.9-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Sep 2020 07:03:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Sep 2020 07:03:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Sep 2020 07:03:46 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:854ab59e811f2c269687884c4899a5de08a5f65b6489dffdb58754086f21e5fc`  
		Last Modified: Mon, 10 Aug 2020 14:29:24 GMT  
		Size: 22.3 MB (22278969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996b7ca18b137080bed3caae4f18c24a2ae9b41a0bd9279d21fe013600e6dbf6`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 35.5 KB (35458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a08dcf8afcac65e6356d202299b593954a299f9ebdb2db237496025225c8f2`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a2e7cb38ebbe96765deedfead50764f5a482a67ca440de7e9e660db464be7`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad916a6ba38726dfe52c5b41799106c13725f1aec4593b47134468adb6b5ce54`  
		Last Modified: Wed, 19 Aug 2020 23:18:39 GMT  
		Size: 838.8 KB (838820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc9bbe153be848ad83436e01a715c00bae1ab365f5fe8f3f50a45a9d53fc569`  
		Last Modified: Wed, 19 Aug 2020 23:18:38 GMT  
		Size: 4.1 MB (4084239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937cc416c13b9bac262c515211db686a9283da659b0a99c9ece75f76bccd487b`  
		Last Modified: Wed, 19 Aug 2020 23:18:37 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346e23a71a2d5226e57ed41548faabc9c8391bbc7e4b42620f49cf8181c7a5cf`  
		Last Modified: Wed, 19 Aug 2020 23:26:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f36cd17e6c24d2e737d14c80164c37d5b62b2601f49b381496722f40fb33076`  
		Last Modified: Wed, 19 Aug 2020 23:27:08 GMT  
		Size: 153.5 MB (153515938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9527c0d045870e6e9055cac954edbbff5e771dab07d594c7076d0ecb512b27`  
		Last Modified: Wed, 19 Aug 2020 23:26:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a2a8ab3cac2b0a656c712603ff11990911a5a37217d5912762be022459b835`  
		Last Modified: Wed, 19 Aug 2020 23:27:28 GMT  
		Size: 48.5 MB (48528086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae743be8fdd52bc68676b8ec7e41fae9f7f20240c1d4d5cb664ee657392b9f73`  
		Last Modified: Wed, 19 Aug 2020 23:27:16 GMT  
		Size: 187.6 KB (187648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933a32ec1f4febe609bbbc9d1d9ab00ec9d7da7a58972cd3a602d85bf1e6413b`  
		Last Modified: Wed, 19 Aug 2020 23:27:15 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1320f3e7655894c0539c66b5654641a1943a6729946fcec955bbff324b528d9d`  
		Last Modified: Wed, 19 Aug 2020 23:27:17 GMT  
		Size: 3.2 MB (3248752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14af7011c5dd16f7e93c147995c19d0d81c0468aa891134c0a9103660da8d4`  
		Last Modified: Wed, 02 Sep 2020 07:07:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c9dbc8a77c2cec2d7c475ab845e511e4772d64592e6b52434235d970ef13a9`  
		Last Modified: Wed, 02 Sep 2020 07:07:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfee6ba8af37e9cc4590c63ef18a71bd87b4760886b8bc07da57288e5852db2`  
		Last Modified: Wed, 02 Sep 2020 07:08:36 GMT  
		Size: 110.5 MB (110521779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d934bb1efa63120861197efa30027230e3849fd3269b5fd9de0bae5d9f924816`  
		Last Modified: Wed, 02 Sep 2020 07:08:05 GMT  
		Size: 10.8 MB (10801167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187402942d02f66f086e61d1b19cd2f8756381521658d7c8277580e08cd6aed9`  
		Last Modified: Wed, 02 Sep 2020 07:07:57 GMT  
		Size: 634.7 KB (634742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4d2a58184caa6e55bcb147d39d9c311c0d6f3e134a4d4494c2eae134982225`  
		Last Modified: Wed, 02 Sep 2020 07:07:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aa2a339382c4213072255a94d771fe9097d2c12c1e8272b8edeaf17096c4bf91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (387009390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04895db9ae8c4880477877a1e2ce8e7b5d8d2bdca09e916956c81f987330b0a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:29:47 GMT
ADD file:b8316fc82a2cf230ce4af7dcf02ec1d7e56b156cf610af8ed23b64509c77c799 in / 
# Wed, 19 Aug 2020 21:29:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:29:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:29:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:29:55 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 23:14:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:14:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:15:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 Aug 2020 23:35:47 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 19 Aug 2020 23:35:48 GMT
ENV LANG=C.UTF-8
# Wed, 19 Aug 2020 23:35:49 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 Aug 2020 23:35:50 GMT
ENV ROS_DISTRO=dashing
# Wed, 19 Aug 2020 23:37:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:37:58 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 19 Aug 2020 23:38:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 Aug 2020 23:38:00 GMT
CMD ["bash"]
# Wed, 19 Aug 2020 23:39:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:39:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 19 Aug 2020 23:39:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 19 Aug 2020 23:40:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 23:40:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 Aug 2020 23:40:48 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 19 Aug 2020 23:40:49 GMT
ENV ROS1_DISTRO=melodic
# Wed, 19 Aug 2020 23:40:50 GMT
ENV ROS2_DISTRO=dashing
# Tue, 01 Sep 2020 22:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.9-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 22:53:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros1-bridge=0.7.6-1*     ros-dashing-demo-nodes-cpp=0.7.9-1*     ros-dashing-demo-nodes-py=0.7.9-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 22:54:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 22:54:30 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:237528ba509b2abcdba1ff1344bab27ad56235cdb3c1c131d3587f6fba4d92c9`  
		Last Modified: Sat, 08 Aug 2020 00:25:26 GMT  
		Size: 23.7 MB (23721798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393b96f31d8b2bf3ce9eb4ac49e6c7411defa4057c1791f02f54c14f2de298ec`  
		Last Modified: Wed, 19 Aug 2020 21:32:13 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d82b0e39008d2fa246a0dca4cfa5feb15db58591582a839bd69d5000aa2e96d`  
		Last Modified: Wed, 19 Aug 2020 21:32:13 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ca375b8d34c9bc764ae24791184cba22510f0c002815b4f9766dd0463f5f5e`  
		Last Modified: Wed, 19 Aug 2020 21:32:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71f6dffa388a5afeaeeec2de7d9fa800e94f1e7f1ad2274f59f7157286f86ec`  
		Last Modified: Thu, 20 Aug 2020 00:06:26 GMT  
		Size: 838.7 KB (838677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ed841649442752ce9cf01dc1412c51934d12d590691361fb31a442d8793944`  
		Last Modified: Thu, 20 Aug 2020 00:06:21 GMT  
		Size: 4.5 MB (4451831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0e3e7bfbdedb57d66e251fe599446189354d4603eb3d458f1fedb2de4c72a8`  
		Last Modified: Thu, 20 Aug 2020 00:06:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e79a72e11b6e2117dbd4dae2a4673f7d8d31a14a1cffa234bc1e6637f0659fd`  
		Last Modified: Thu, 20 Aug 2020 00:16:23 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28841f536a353faaa820c6564df2b33e24c29347a9d62487a056e888edbdc3ac`  
		Last Modified: Thu, 20 Aug 2020 00:17:12 GMT  
		Size: 165.1 MB (165076559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74784c24f72dee0be556cbb37b89c05ea077933a9a1a49c22fa4b610412f4bf`  
		Last Modified: Thu, 20 Aug 2020 00:16:23 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bd5e01cd95c97549278c1e5b3869eeab949f41aa237dfdde8b74f076557e55`  
		Last Modified: Thu, 20 Aug 2020 00:17:34 GMT  
		Size: 56.8 MB (56837310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b420753a6a76c91bfa50e2840570baf864542c60730406dde01622aaeb9ae986`  
		Last Modified: Thu, 20 Aug 2020 00:17:22 GMT  
		Size: 187.6 KB (187648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e032b1979cdde7985f06c7c76e74d8367956b47c5c225bbc06b4593bd0d750`  
		Last Modified: Thu, 20 Aug 2020 00:17:22 GMT  
		Size: 2.1 KB (2067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31a5266993a413241f868a142b60bc74e7d4603e5bef8cedf01dc98e142ac47`  
		Last Modified: Thu, 20 Aug 2020 00:17:22 GMT  
		Size: 3.7 MB (3664658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4097f75cf46de7ede04627453e7461dbc9086d3437f6c53de312ff24fb643c1`  
		Last Modified: Tue, 01 Sep 2020 23:14:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa47e9cabf4ba5369fed31153d5136c2cb6e1cedd7eb324b1de93cc68c3ee4b2`  
		Last Modified: Tue, 01 Sep 2020 23:14:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a669974be4907d90aa4d0795541923088504dca5e7234bd0cc461996a50372fe`  
		Last Modified: Tue, 01 Sep 2020 23:15:21 GMT  
		Size: 116.6 MB (116611981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f88cce6f92968a2fa5a40fa1cd986df5a42bd384f2774f9827e0ff14b2a6d5`  
		Last Modified: Tue, 01 Sep 2020 23:14:53 GMT  
		Size: 14.9 MB (14942394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a82e3da75169ab07fd55ce12644d4f7af0fc6e162dde0e23431ea5a871663`  
		Last Modified: Tue, 01 Sep 2020 23:14:44 GMT  
		Size: 635.8 KB (635754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cd6da70e0eeda7f722da7869b2c5cb81d8c967f8e7cc1a56d3db1bd562483b`  
		Last Modified: Tue, 01 Sep 2020 23:14:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
