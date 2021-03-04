## `ros:eloquent-ros1-bridge`

```console
$ docker pull ros@sha256:acb75cf6cbba6b0d60c0748775c6ac1d3f07c9a5dabba5f99ec6c7a239972d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:7270c2fb24fec7d0ea48a6b0870ea37ae23f57dddef2aec5db2dc7a86e03cfb8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.2 MB (504228869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dd18c29a6f30521c10d2fad6d75a008638c9bace461c54c145af5c73e4069b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:01:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:17:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:17:24 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 05:37:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 04 Mar 2021 05:37:51 GMT
ENV LANG=C.UTF-8
# Thu, 04 Mar 2021 05:37:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 04 Mar 2021 05:43:45 GMT
ENV ROS_DISTRO=eloquent
# Thu, 04 Mar 2021 05:44:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:44:52 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 04 Mar 2021 05:44:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 04 Mar 2021 05:44:52 GMT
CMD ["bash"]
# Thu, 04 Mar 2021 05:45:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:45:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 04 Mar 2021 05:45:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 04 Mar 2021 05:45:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:45:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 05:45:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 04 Mar 2021 05:45:49 GMT
ENV ROS1_DISTRO=melodic
# Thu, 04 Mar 2021 05:45:50 GMT
ENV ROS2_DISTRO=eloquent
# Thu, 04 Mar 2021 05:46:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:48:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:48:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 05:48:07 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814c16bc426c5ae8d2f3d14c21f670e806e3ca48742168acaf3f4408adfc57b8`  
		Last Modified: Thu, 04 Mar 2021 04:18:20 GMT  
		Size: 841.3 KB (841302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ad1089bf02490bff9b59ba5aecc63b83336aba042dc1c4122405b22cefd648`  
		Last Modified: Thu, 04 Mar 2021 05:56:41 GMT  
		Size: 4.9 MB (4872141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c2010ec06ecf4c80f4ef1e520e02215f97a68c893afa50fe6f474209ad00c`  
		Last Modified: Thu, 04 Mar 2021 05:56:40 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d6be2ec2203465b3f61723529a688ca90159c55b205cc83753480fd7c2b91`  
		Last Modified: Thu, 04 Mar 2021 06:02:33 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91262e563eec5e6c9d87364c851aff7ec9fc243d0ac15c04296ccb92648e4e28`  
		Last Modified: Thu, 04 Mar 2021 06:04:55 GMT  
		Size: 183.0 MB (183001973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c68462e0d92ebac7e5937a97ee473471856923f11096d4b1aa45ebbc6bfa7a`  
		Last Modified: Thu, 04 Mar 2021 06:04:16 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab883d192d6872a9f9becbf78c0ae0322b6a410629e836b285845841ac532e5a`  
		Last Modified: Thu, 04 Mar 2021 06:05:11 GMT  
		Size: 63.5 MB (63515699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e86430d98ff0ec2fcacf018f2479bde14f9082a6df42f2ca7aa551365f38940`  
		Last Modified: Thu, 04 Mar 2021 06:05:00 GMT  
		Size: 201.6 KB (201623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55413c0932b184afa415a325d3f5509d084617da7ba9634e99a87bc8e8935411`  
		Last Modified: Thu, 04 Mar 2021 06:05:00 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db4ec67906ce1eb1314ce7e2c72b3d9f4072f0843b18238d2242c4f2d0fda06`  
		Last Modified: Thu, 04 Mar 2021 06:05:01 GMT  
		Size: 4.6 MB (4585727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302561852d55d35e6453da10c51e57108adf942dd45fc9ee2e302196d6740a28`  
		Last Modified: Thu, 04 Mar 2021 06:05:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef7156f9b601dbbb88d79b9baea4c941a6197a27ad55e59c6fd09d5a24bd11`  
		Last Modified: Thu, 04 Mar 2021 06:05:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7da3c32ed077590dfb60caa3e6fd69544493547720b9fb58bee104a89726e1`  
		Last Modified: Thu, 04 Mar 2021 06:05:48 GMT  
		Size: 117.8 MB (117761155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba74bbf9268c0ddc70d98ef24ff3da1cf39e2e4442f1ad019d3abe8065924f2`  
		Last Modified: Thu, 04 Mar 2021 06:05:44 GMT  
		Size: 102.0 MB (101995005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aeefb43e34a55d4991d0b0c8bb39ba5a177fbfcc4ff8deee4206757c08c7cf6`  
		Last Modified: Thu, 04 Mar 2021 06:05:17 GMT  
		Size: 738.7 KB (738651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70118bef60450dd4a71dbd72fe49f851665996f370ab570cc4f15ee0b318250`  
		Last Modified: Thu, 04 Mar 2021 06:05:17 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:ad4bd189e0d51634a10174bfc9d49320e245f8d55d66d89abe7ceaee2cb8d8b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429051776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea613831d7cbec368fcccca58af3d2deb337ecbdc35078466691cb774a771d2f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Mar 2021 03:11:28 GMT
ADD file:40381fcd77266e4b2259c02af63359b9cff79b4908e5f800f2b3cb9c555e092c in / 
# Thu, 04 Mar 2021 03:11:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 03:11:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 03:11:34 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 03:11:35 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:03:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:03:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:03:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 04:24:58 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 04 Mar 2021 04:24:59 GMT
ENV LANG=C.UTF-8
# Thu, 04 Mar 2021 04:25:00 GMT
ENV LC_ALL=C.UTF-8
# Thu, 04 Mar 2021 04:32:24 GMT
ENV ROS_DISTRO=eloquent
# Thu, 04 Mar 2021 04:34:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:34:47 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 04 Mar 2021 04:34:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 04 Mar 2021 04:34:49 GMT
CMD ["bash"]
# Thu, 04 Mar 2021 04:35:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:35:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 04 Mar 2021 04:35:54 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 04 Mar 2021 04:36:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:36:20 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 04:36:21 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 04 Mar 2021 04:36:22 GMT
ENV ROS1_DISTRO=melodic
# Thu, 04 Mar 2021 04:36:23 GMT
ENV ROS2_DISTRO=eloquent
# Thu, 04 Mar 2021 04:38:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:39:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:40:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 04:40:01 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:9ac910c0311f3581d0d4d512d5b9cb75f3cb4ac0ac05c27d5afe506d19ede5a4`  
		Last Modified: Mon, 01 Mar 2021 16:09:58 GMT  
		Size: 22.3 MB (22290308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b89a6b5bccf38a10ff30cb0b414a7e2dec5567d954850dfb98d67977e13fc38`  
		Last Modified: Thu, 04 Mar 2021 03:13:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36058ccabae5f30074009cee645af7e052db260738cc0bc08ec9386b0f8cf37e`  
		Last Modified: Thu, 04 Mar 2021 03:13:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055861ede19fe8606dca16da2271075d5d46ad1234acc782d134f1c941be2c72`  
		Last Modified: Thu, 04 Mar 2021 04:40:54 GMT  
		Size: 841.1 KB (841118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6fbf11975e6d976397a06700430b7ac889c14444fc7ad18a7be40983d9d468`  
		Last Modified: Thu, 04 Mar 2021 04:40:53 GMT  
		Size: 4.1 MB (4085567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e165c7fe50b6918ba96d9a80c7d25887947ae8b8aa8fd70fe773e79a745dff1b`  
		Last Modified: Thu, 04 Mar 2021 04:40:52 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cced3fb2c3ab38fac875c419ff81df8ddcc53b538cb2f9094df0e2f8de49339a`  
		Last Modified: Thu, 04 Mar 2021 04:48:28 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610ebe712acc613ed4684f809c031e5f92683905e6428dc3ab5868576d14485`  
		Last Modified: Thu, 04 Mar 2021 04:51:12 GMT  
		Size: 156.6 MB (156616799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81655ee6f1bdd57ccd4505d3859ab7e34e47f585c4ea4de7dbca1866600a40ee`  
		Last Modified: Thu, 04 Mar 2021 04:50:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9972e48fe8245a8298189943a2fdee353bb8bf0ca7d4c6a8e13336953ed4036a`  
		Last Modified: Thu, 04 Mar 2021 04:51:37 GMT  
		Size: 47.9 MB (47914711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db555332ef59faf7be7da641813c3345005466ebd8e9ae75aea20547e48b881`  
		Last Modified: Thu, 04 Mar 2021 04:51:25 GMT  
		Size: 201.7 KB (201677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf16d393b823c78b15cfc51130e23ad305e2b4a4166f575c2eaf0193458536b0`  
		Last Modified: Thu, 04 Mar 2021 04:51:25 GMT  
		Size: 2.0 KB (2044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1034e7a69686363691522efd2fdf8e5c26fa416cd5250b53a23df2c558d2cc17`  
		Last Modified: Thu, 04 Mar 2021 04:51:26 GMT  
		Size: 3.5 MB (3496339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4aa3e27a444e8994e2f98f9f5f930ea5269c8b55a6f07b245a6b0d3bafdc80`  
		Last Modified: Thu, 04 Mar 2021 04:51:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714e2b171da8283b873de670e6d68832ec090c7251790038d75963c806e68e3e`  
		Last Modified: Thu, 04 Mar 2021 04:51:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d1623c1c7a0c5a8b42177a095d2005fdde0664e1f10f60f0fa4fe3760a0537`  
		Last Modified: Thu, 04 Mar 2021 04:52:26 GMT  
		Size: 110.6 MB (110646203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10615ece687a6f0485607a7c4cf4125c6cdf9cfca1d14e5b2a21acf2a614508e`  
		Last Modified: Thu, 04 Mar 2021 04:52:15 GMT  
		Size: 82.2 MB (82220168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6d07192fb7badc288ea3733cfb52e239a17b0ff8ec274d3dfa1def39424084`  
		Last Modified: Thu, 04 Mar 2021 04:51:46 GMT  
		Size: 733.3 KB (733340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f8b1df22a58c0ce5d679945608babc52f1ead21ceaa4026df0004fbef12f62`  
		Last Modified: Thu, 04 Mar 2021 04:51:46 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:df308ce738e864d7e18d0308e596fd261cf383af41b6ae466f904b7de8681b03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.1 MB (464136722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb06cc18938705ad7a2d6c3d3515ba563e89de5a96426907f4d8719caa7c3d35`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 04 Mar 2021 02:52:16 GMT
ADD file:bd92fdc04a5552a5b6596d4efffc3b5ca8dcce88e1f1c8d731c4039ce95b09cf in / 
# Thu, 04 Mar 2021 02:52:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:52:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:52:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:52:24 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 03:12:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:13:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:13:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 03:32:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 04 Mar 2021 03:32:27 GMT
ENV LANG=C.UTF-8
# Thu, 04 Mar 2021 03:32:28 GMT
ENV LC_ALL=C.UTF-8
# Thu, 04 Mar 2021 03:39:09 GMT
ENV ROS_DISTRO=eloquent
# Thu, 04 Mar 2021 03:41:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:41:26 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 04 Mar 2021 03:41:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 04 Mar 2021 03:41:29 GMT
CMD ["bash"]
# Thu, 04 Mar 2021 03:42:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:42:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 04 Mar 2021 03:42:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 04 Mar 2021 03:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:43:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 04 Mar 2021 03:43:21 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 04 Mar 2021 03:43:23 GMT
ENV ROS1_DISTRO=melodic
# Thu, 04 Mar 2021 03:43:26 GMT
ENV ROS2_DISTRO=eloquent
# Thu, 04 Mar 2021 03:45:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:46:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:46:53 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:9243cbd63062004cb0062d0c8235fb578c194179c6526f26999de6c03daded31`  
		Last Modified: Tue, 23 Feb 2021 00:25:02 GMT  
		Size: 23.7 MB (23732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ce98c92d8885e63c0bde376962ac7d15ebb891a7019f801e1de07be167209`  
		Last Modified: Thu, 04 Mar 2021 02:54:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e35ad787dffb8fc50bf32fc5febb71a414956f1a93b71360349b44b113fef`  
		Last Modified: Thu, 04 Mar 2021 02:54:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb395c83b2a400ee825ab384f2c51674c732ff599742e127b5639756b0cc7a8b`  
		Last Modified: Thu, 04 Mar 2021 04:00:41 GMT  
		Size: 840.9 KB (840907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3418e9c274d60c6f142b25861afead56aafa5ece244d451cab264c52961bc618`  
		Last Modified: Thu, 04 Mar 2021 04:00:40 GMT  
		Size: 4.5 MB (4453487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee6263fb6dc4f04d5d149d5aa0d9932daea95f32e0478a12a5e66a986a1931`  
		Last Modified: Thu, 04 Mar 2021 04:00:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba1f39d246b743a36739f550b8be9d8c7d9eabc3ef41854beda836da5a2a313`  
		Last Modified: Thu, 04 Mar 2021 04:07:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ce0ebfeb4d2e555323f5c06e4cb35d0d4c4ed1bc771dd6693499f5c1759d37`  
		Last Modified: Thu, 04 Mar 2021 04:10:29 GMT  
		Size: 168.4 MB (168425669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82aa1bde67253b6384c49fc47b08dfbf5a701284a6f173e3b5c0db2e0226e87b`  
		Last Modified: Thu, 04 Mar 2021 04:09:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff496571ec081faf7c4d5caeb40984e7c77ad7b14f21c20cac20cc94b3b1ced`  
		Last Modified: Thu, 04 Mar 2021 04:10:51 GMT  
		Size: 56.2 MB (56227443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b9da9925b4002ad595d3a955ee82f9dc2798259f31f2dc8f84676f1e10355`  
		Last Modified: Thu, 04 Mar 2021 04:10:36 GMT  
		Size: 201.7 KB (201679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60ca71c09c1715d7d1bb735e03591cea0530693ac6e7484eecfc1afc171614`  
		Last Modified: Thu, 04 Mar 2021 04:10:36 GMT  
		Size: 2.0 KB (2036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265b99736ec68040007fc9e8cb5649c8d4320061e66e6d0e9cd6dabfaa0088b7`  
		Last Modified: Thu, 04 Mar 2021 04:10:38 GMT  
		Size: 3.9 MB (3934828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb68efd37d1758e016c90c1d1d8e0a3bd0451947a056a07b4f54964d137b8131`  
		Last Modified: Thu, 04 Mar 2021 04:11:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed146f55117251cc68d6dcfa9d168823b81e353fe4326a120deb0fe19337223`  
		Last Modified: Thu, 04 Mar 2021 04:11:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93eb2d7730873fbcba24459d88303c8060d362a86f90ace05c2f680e3a7125c`  
		Last Modified: Thu, 04 Mar 2021 04:11:37 GMT  
		Size: 116.7 MB (116719690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209ab03c34b5830b7d719549bb78b1f9e7dd3c3d5e40afc08202749ce1937edf`  
		Last Modified: Thu, 04 Mar 2021 04:11:28 GMT  
		Size: 88.9 MB (88860002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c4b34b1fcba374f23ea469c86046245f8ab9388347b121f6ba5753e36ea302`  
		Last Modified: Thu, 04 Mar 2021 04:11:03 GMT  
		Size: 735.4 KB (735422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70fda27be8e563bbbc381bfe842525e3c61160dbbf1df4020e13048e3ff1fd7`  
		Last Modified: Thu, 04 Mar 2021 04:11:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
