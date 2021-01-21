## `ros:eloquent-ros1-bridge`

```console
$ docker pull ros@sha256:dc42880c7404b0244517b666a9b8c44c3da4212466977eab58fc08490f5e922e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:e10a0ed4d151d7505e14e78df6ac8d11e1010832b2433f043aed55f08d1aa20e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.2 MB (504174061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0816f2c4724da408af1ffa34d1285e3225707ed7379b5cf865391960fd07965f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:13 GMT
ADD file:6ef542de9959c3061f2d0758adb031e226b221a1a2cd748ff59e6fc13216a1c0 in / 
# Wed, 25 Nov 2020 22:25:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:17 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 22:59:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:49:04 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:49:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 02:10:03 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 26 Nov 2020 02:10:04 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 02:10:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 02:15:24 GMT
ENV ROS_DISTRO=eloquent
# Mon, 14 Dec 2020 22:34:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:34:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 14 Dec 2020 22:34:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 14 Dec 2020 22:34:24 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 22:35:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:35:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 14 Dec 2020 22:35:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 14 Dec 2020 22:35:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:35:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 14 Dec 2020 22:35:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 14 Dec 2020 22:35:47 GMT
ENV ROS1_DISTRO=melodic
# Mon, 14 Dec 2020 22:35:47 GMT
ENV ROS2_DISTRO=eloquent
# Mon, 14 Dec 2020 22:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:38:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:39:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:39:02 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:f22ccc0b8772d8e1bcb40f137b373686bc27427a70c0e41dd22b38016e09e7e0`  
		Last Modified: Fri, 20 Nov 2020 13:21:30 GMT  
		Size: 26.7 MB (26708056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8fb62ba5ffb221a2edb2208741346eb4d2d99a174138e4afbb69ce1fd9966`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c964ece6a3edf0db1cfc72ae0e6f0699fb776bbfcc92b708fbb945b0b9547`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a8092b82e49df7860a001e4452fcbb13b91f571599dc4688933a1138f6b372`  
		Last Modified: Wed, 25 Nov 2020 23:10:00 GMT  
		Size: 839.0 KB (838950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebbce50bab7cc5a89e4b0fd9944d1a04f6624166cf7167f0b95f5996d0ef71b`  
		Last Modified: Thu, 26 Nov 2020 02:28:51 GMT  
		Size: 4.9 MB (4870594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742c8b372e747b17b29d1b06efb74ea9a51cf7ea00f2ed266fc0243518807cf1`  
		Last Modified: Thu, 26 Nov 2020 02:28:49 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492a3104cee6577e8151a449350051d44b30e14814dd70a59f87803ea538acce`  
		Last Modified: Thu, 26 Nov 2020 02:34:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0442dc1f0a537542dc230f8bb8f16a8d92dc8e30b6945c1cb72f2ffb95392be7`  
		Last Modified: Mon, 14 Dec 2020 22:42:05 GMT  
		Size: 183.0 MB (183003740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d6fe82abf28637a7aa5f82f4657acfe68ad8d24ed517ce74d86eaadcba14ad`  
		Last Modified: Mon, 14 Dec 2020 22:41:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0c7edd0d60c1e25aac5a4fa34ee6ae246fdf39ba570e545103f17b5a19c0f9`  
		Last Modified: Mon, 14 Dec 2020 22:42:21 GMT  
		Size: 63.5 MB (63513551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61030099e77268964c5a594de4b8dae235ae1084015b319c024920d2d3c1b803`  
		Last Modified: Mon, 14 Dec 2020 22:42:11 GMT  
		Size: 197.6 KB (197568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3ea72ca74ad6817f1de2ee6c0454a1991c90b1804babab81893c70267a6827`  
		Last Modified: Mon, 14 Dec 2020 22:42:11 GMT  
		Size: 2.0 KB (2003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a7777bd5691e5ceaddc8c1b24897a7fba4e6a6c971ee13612ba2752226c57`  
		Last Modified: Mon, 14 Dec 2020 22:42:12 GMT  
		Size: 4.6 MB (4584789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abed8fa2768166b4a8bec9a5a75e7e7a2ff78d35ebf957ee3a23f10796821f98`  
		Last Modified: Mon, 14 Dec 2020 22:42:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cfabc69bfaf5b59a47cb7ac6a7723b5a98fc721ae58ad73fd62db8ea8d8ac4`  
		Last Modified: Mon, 14 Dec 2020 22:42:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dce573e09425f73df9305af787225f8e92589197aef3b8953609099248f7b6f`  
		Last Modified: Mon, 14 Dec 2020 22:42:53 GMT  
		Size: 117.7 MB (117745540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08208cb2215bdacf9d1f6463964b8ed60c6df9c5873f7dac687d7959531f440`  
		Last Modified: Mon, 14 Dec 2020 22:42:51 GMT  
		Size: 102.0 MB (101968237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b787fc334ebf2878a562ffe49240b9d0d86915435e57596bd8e29ed88ea4b`  
		Last Modified: Mon, 14 Dec 2020 22:42:29 GMT  
		Size: 737.6 KB (737561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf05710b14f698aa6a4b727a4d4c3cf1e0c7b736cca8c25db10ea51dbe9adc9f`  
		Last Modified: Mon, 14 Dec 2020 22:42:28 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:3a3878e8dfc3bc5c192bf83d834e685c7ddaee497892d9b26f0cf248ef3ec317
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429051308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43146c7e1374742a0faf5e4ab09c8d231ac7496179d06798e493883cbd2753ab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:15:18 GMT
ADD file:270f582b851314ab60dfbbc136c8e36ec44a11ecba1448403947ce72b0f9c06a in / 
# Thu, 21 Jan 2021 03:15:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:15:22 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:15:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:15:27 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:30:45 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:31:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:31:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 04:52:26 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 04:52:27 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 04:52:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 04:59:00 GMT
ENV ROS_DISTRO=eloquent
# Thu, 21 Jan 2021 05:01:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:01:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 05:01:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 05:01:26 GMT
CMD ["bash"]
# Thu, 21 Jan 2021 05:02:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:02:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 21 Jan 2021 05:02:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 21 Jan 2021 05:02:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:03:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 05:03:12 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 05:03:12 GMT
ENV ROS1_DISTRO=melodic
# Thu, 21 Jan 2021 05:03:13 GMT
ENV ROS2_DISTRO=eloquent
# Thu, 21 Jan 2021 05:05:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:07:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:07:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:07:28 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:6d8bd15f2f6189f24e8f1b5dc573a293c963565ab012ca6a42e51a3023e72e7e`  
		Last Modified: Thu, 21 Jan 2021 03:18:06 GMT  
		Size: 22.3 MB (22291204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e961f21c7ea83c265a6de2897b8255e9e03cf1d39b74fb208b4ca936c6a53c5`  
		Last Modified: Thu, 21 Jan 2021 03:18:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b017766c8f695603aa5da2f534135bd1fbe253f667ef6faa77a77c66be9ba9f5`  
		Last Modified: Thu, 21 Jan 2021 03:18:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb7679849b59188f62bf017de9112158370c1d2eee07a8d614ba382cf612b62`  
		Last Modified: Thu, 21 Jan 2021 05:12:20 GMT  
		Size: 841.2 KB (841181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd1c8ec76e1cf5b551b2db58eb684cae7c4a3219c7175d85b4bf9ea4e5fe998`  
		Last Modified: Thu, 21 Jan 2021 05:12:19 GMT  
		Size: 4.1 MB (4085304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf27b43dde6748aae4a2d48a18d094192f874983a13d5046c161f02d3e11ab77`  
		Last Modified: Thu, 21 Jan 2021 05:12:16 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26cb5182d75745719bf677aa2f51d17ba9e1bf00013e8a22efd1af4049f56b8`  
		Last Modified: Thu, 21 Jan 2021 05:20:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bf5cdc7fd2ae521e561ce96210f47957bd69f3032060106f38a02688c1efe7`  
		Last Modified: Thu, 21 Jan 2021 05:22:36 GMT  
		Size: 156.6 MB (156616037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f241b728b2f9709369e16c00d041f060a94875ad95b5dd1c1c5438118431f`  
		Last Modified: Thu, 21 Jan 2021 05:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc40cfd9e4ea8827d37cb41a73878aea704e2990580a718aa8ac5458059120`  
		Last Modified: Thu, 21 Jan 2021 05:23:01 GMT  
		Size: 47.9 MB (47913242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229cea04c8d8ee1199714510ac014aeafc8e37c7455a30f3da03bc27c31ea9e2`  
		Last Modified: Thu, 21 Jan 2021 05:22:49 GMT  
		Size: 199.1 KB (199111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecce7881e10857f72ce0773c079be1066b2090ad5a1b53b9d81554c8b5abe21`  
		Last Modified: Thu, 21 Jan 2021 05:22:49 GMT  
		Size: 2.0 KB (2033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1cdcac95d88a0a637964de9099507b87799717fb314f076f54f0bae9c88a31`  
		Last Modified: Thu, 21 Jan 2021 05:22:51 GMT  
		Size: 3.5 MB (3496680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116eedc102ae405bf8d4360eab4f25526c0ddbf859145ec034e7d5bc9657b5e6`  
		Last Modified: Thu, 21 Jan 2021 05:23:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a994cec689232d55bd40cc55a496c9f0ce297422d4fe9c4d0f763148ae5fbd8a`  
		Last Modified: Thu, 21 Jan 2021 05:23:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c902c2d082a590502b1335f25e33b573f1c8501d1cdc519742d52378890d8`  
		Last Modified: Thu, 21 Jan 2021 05:23:53 GMT  
		Size: 110.7 MB (110657462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8594cf35472f1d309408bd36c2dddc7408406aa486a20ae7d0cc66747585da4f`  
		Last Modified: Thu, 21 Jan 2021 05:23:44 GMT  
		Size: 82.2 MB (82211958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3db1bee4213bd4fccd026222e28f3824ba78500cd0a26790905e1fdf7cf78e`  
		Last Modified: Thu, 21 Jan 2021 05:23:14 GMT  
		Size: 733.6 KB (733592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a028d4184bd02f13048e9ba5e25bdd5fe96655b8c9f92464824eec8077c60893`  
		Last Modified: Thu, 21 Jan 2021 05:23:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f8d3e80d51428935de742ec7cf61f191a6b44cb910880a7ff4b2290f0d460ee0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.1 MB (464098167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d14f5def366bdf7872f888f032f4a82c203235153bf426763754f1256abea3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:42:53 GMT
ADD file:e5b221023382c9e42b8558f8887f8317fe7e9759f59feb1799548aed9236e99b in / 
# Wed, 25 Nov 2020 22:42:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:42:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:58:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:58:27 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:58:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 00:20:15 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 26 Nov 2020 00:20:16 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 00:20:17 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 00:28:14 GMT
ENV ROS_DISTRO=eloquent
# Mon, 14 Dec 2020 22:05:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:05:41 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 14 Dec 2020 22:05:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 14 Dec 2020 22:05:42 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 22:06:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:06:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 14 Dec 2020 22:07:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 14 Dec 2020 22:07:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:07:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 14 Dec 2020 22:07:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 14 Dec 2020 22:07:37 GMT
ENV ROS1_DISTRO=melodic
# Mon, 14 Dec 2020 22:07:38 GMT
ENV ROS2_DISTRO=eloquent
# Mon, 14 Dec 2020 22:09:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:11:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:12:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Dec 2020 22:12:06 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:04da93b342eb651d6b94c74a934a3290697573a907fa0a06067b538095601745`  
		Last Modified: Thu, 19 Nov 2020 16:25:04 GMT  
		Size: 23.7 MB (23733196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b235194751dee33624fc154603f7e25ecdfbb02538fb7d55fa796df9afa95fee`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a67bb8db9a1111022bdc6406442e11c1a66653136c5c777114bf67b61038a`  
		Last Modified: Wed, 25 Nov 2020 22:44:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0829be0ab1546c2197017682a8fa87c2c9bf9d430bb72fa87778f5f0843c64c3`  
		Last Modified: Thu, 26 Nov 2020 01:07:09 GMT  
		Size: 839.6 KB (839595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcaa7dbaa51b95c71b56e7a0030e87a40fb2d5f4a046a05c9247a720a071ad7`  
		Last Modified: Thu, 26 Nov 2020 01:07:09 GMT  
		Size: 4.5 MB (4453176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8dc9620e81d964a23f1b0448c85d69a4123a5cdab77b15a1898429bd1f119f6`  
		Last Modified: Thu, 26 Nov 2020 01:07:05 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57317b10b7bc56973797de6fc7f96d26fcb5138891e793344fc0236282519161`  
		Last Modified: Thu, 26 Nov 2020 01:14:28 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4aaa03f14c0c4602fd40d4d9690deff2089b69339d4cba377e394c2308bbdb`  
		Last Modified: Mon, 14 Dec 2020 22:16:08 GMT  
		Size: 168.4 MB (168403434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5c7b95ab4fbd58b388933995857fff4f8fa181e000f8cc44b5b43eb5f92856`  
		Last Modified: Mon, 14 Dec 2020 22:15:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb50d763449bfd373487d39ad0b58ea3ad6b5fcb6ce0a6bd8dad084537ff5cc2`  
		Last Modified: Mon, 14 Dec 2020 22:16:28 GMT  
		Size: 56.2 MB (56226461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374ee103ecf676799b3dcabffe8de968132645b9b4ccbc14558ad5121c53fef7`  
		Last Modified: Mon, 14 Dec 2020 22:16:16 GMT  
		Size: 197.6 KB (197637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdc80dda6839010be54753a4fdd377a4d4d54cb89a6c9abb53a56f22ced9231`  
		Last Modified: Mon, 14 Dec 2020 22:16:16 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb91305b3c0f5c3dab29db733de51f974bd3a3eb1e8b0847732d68081280848`  
		Last Modified: Mon, 14 Dec 2020 22:16:17 GMT  
		Size: 3.9 MB (3935087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7fd37bb0b43e05371f8fa936152b3df19bd64d4b8cbfc340643edf4d079e76`  
		Last Modified: Mon, 14 Dec 2020 22:16:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a96a7beb6821a6fa43e511611a784c3364862c27fa3d012e15f6f3f5eefb385`  
		Last Modified: Mon, 14 Dec 2020 22:16:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d5db9d7877f5eb7305f0e7a5fbcf30861c2aa0307bcfe8f5fdccc0a659eaee`  
		Last Modified: Mon, 14 Dec 2020 22:17:13 GMT  
		Size: 116.7 MB (116699579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f84fd3f5c184eefa8d54429224fe5960c619e28eb2a4ffc8096e7b9336406`  
		Last Modified: Mon, 14 Dec 2020 22:17:16 GMT  
		Size: 88.9 MB (88868743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9746c29ce5650e5f0f67e0f923793da2ba3eb489af7f1579241d4b5dbeb370ea`  
		Last Modified: Mon, 14 Dec 2020 22:16:38 GMT  
		Size: 735.7 KB (735691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b167c7a7de04cd3e1d8275ed0f504355db968eeebdd8b2126b9784732efa896c`  
		Last Modified: Mon, 14 Dec 2020 22:16:38 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
