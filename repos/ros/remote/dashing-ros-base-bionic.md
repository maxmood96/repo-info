## `ros:dashing-ros-base-bionic`

```console
$ docker pull ros@sha256:17301f55de8e658621b2b26736502bcc59cd20ad953aadc45fd64328defd8c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:cd82f4e7b5e766cc4441cb09e893c84fde196dfc02859708fe91b6be266d807b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280503032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8218dc7f4a69e7adb8d86d368fe14483842b14c4bc145d1097fa3c7cc538d9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 11:10:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:38:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:38:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 13:07:52 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Mar 2021 13:07:52 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 13:07:52 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 13:07:53 GMT
ENV ROS_DISTRO=dashing
# Fri, 26 Mar 2021 13:10:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:10:36 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 13:10:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 13:10:36 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:11:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:11:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 13:11:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Mar 2021 13:11:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa0eff1a96d1d945845cab86a8e978cc925e0c70eb0c4c23df2d989f3d08c6`  
		Last Modified: Fri, 26 Mar 2021 11:40:20 GMT  
		Size: 840.2 KB (840161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c35c871baa65cb3164cc6ebb22d25b6b58e98c1eb7a2e9f8aaa302c71730643`  
		Last Modified: Fri, 26 Mar 2021 13:34:06 GMT  
		Size: 4.9 MB (4871708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eceba2cf9f62d789d7d061842ed0f7e0a057fe97bb23b64fb5407a0fbeb4cd8`  
		Last Modified: Fri, 26 Mar 2021 13:34:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce24ab7544ded3587ecf9b2367d0305803b2195eb45ff5f0af17b48484fa2e7d`  
		Last Modified: Fri, 26 Mar 2021 13:40:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832c5e165f474ce06d6a26b50913c4787c2edf1e313b653baa5f8f043ddd0546`  
		Last Modified: Fri, 26 Mar 2021 13:41:27 GMT  
		Size: 179.4 MB (179406019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79f5162777a89b494fff747030f3ee263b09bc97109290a5980adea6f9c6b28`  
		Last Modified: Fri, 26 Mar 2021 13:40:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9eff232ff0c21e24c43985f499d53a613ecc0e060db5996acbe00df9c0abe6`  
		Last Modified: Fri, 26 Mar 2021 13:41:55 GMT  
		Size: 64.2 MB (64151585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e42269d465832d7ec14e108686c828af96c44ffe42b65cf4c889ecc0aa17035`  
		Last Modified: Fri, 26 Mar 2021 13:41:40 GMT  
		Size: 204.0 KB (203994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c1368317e443f451bbbd326ca265569c66c06cdcd0aeb02f88c014ec97f630`  
		Last Modified: Fri, 26 Mar 2021 13:41:40 GMT  
		Size: 2.0 KB (2027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbebcbec01acb4d9bdc02be0f7415df63c6fb12c83382abb653c284a731f8a4`  
		Last Modified: Fri, 26 Mar 2021 13:41:42 GMT  
		Size: 4.3 MB (4313875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:7c1ab4ec616fb54dfc0009dd9971129f52e51f5183b70c3cd4b04f882fc0f552
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232779361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741322600b3824282ed388d539efa277f2b52e4a2d8bc4f6d0eb9bcdceabbc7d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 09:13:19 GMT
ADD file:474c32464fde8c7d9e10b46057ab5cc2e1fc203fd8677ea3640c631f85117888 in / 
# Fri, 26 Mar 2021 09:13:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 26 Mar 2021 09:13:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 26 Mar 2021 09:13:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 26 Mar 2021 09:13:36 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:03:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:03:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:03:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 14:29:54 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Mar 2021 14:29:55 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 14:29:57 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 14:29:59 GMT
ENV ROS_DISTRO=dashing
# Fri, 26 Mar 2021 14:33:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:33:04 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 14:33:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 14:33:11 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 14:34:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:34:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 14:34:58 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Mar 2021 14:35:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:998199bcf9ef936a7f908e13358322e3ceff3224a4b18ade78181654c80572f9`  
		Last Modified: Fri, 26 Mar 2021 09:16:25 GMT  
		Size: 22.3 MB (22291239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b21c25a7bc95d706d25e4db24b7330a082cd700618204b85569a04519e8498`  
		Last Modified: Fri, 26 Mar 2021 09:16:21 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355a6e767920e1c47edc24001be388f7332ecb232abb204adfe5163baa1db64b`  
		Last Modified: Fri, 26 Mar 2021 09:16:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f739a69aad0312ff68f8b450af0b4a076cee88dfea995283a79928b9d574ef28`  
		Last Modified: Fri, 26 Mar 2021 14:49:49 GMT  
		Size: 841.2 KB (841170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1eb8b50942c458929fd4f04670c58019e677dae4b21d8057f63147a50b80bc`  
		Last Modified: Fri, 26 Mar 2021 14:49:45 GMT  
		Size: 4.1 MB (4085629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcb68acffef6ac858782dd1dc8ad3c0c6ff543858974beddf91d9fc01ae520b`  
		Last Modified: Fri, 26 Mar 2021 14:49:44 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847294f9fd3268c62141efa9743aa315a1ccb8a3564f4bcafa1bac50f1f3ee83`  
		Last Modified: Fri, 26 Mar 2021 15:01:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986dce8ed75e8fe52ab858c1901279fc8603fcfc4ae85ec838376808040ac332`  
		Last Modified: Fri, 26 Mar 2021 15:02:18 GMT  
		Size: 153.6 MB (153553306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439cc730f786a9c8cc8d42f93c25ae4781f31289271b181de953e76dabf445a8`  
		Last Modified: Fri, 26 Mar 2021 15:01:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1533ba4f0e877b04fd9ceac1509cd72a24c00fe85e88de0a40fdeade998bf4f`  
		Last Modified: Fri, 26 Mar 2021 15:02:43 GMT  
		Size: 48.5 MB (48548628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a824ce06f26d2ef8dcc18853213243c895694531dc42361f2849309f2d43d6`  
		Last Modified: Fri, 26 Mar 2021 15:02:26 GMT  
		Size: 204.0 KB (204007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7bc37a7b51e07cd56efb700933b6c08a840e04f4ca0fb32ad9b4a9e611dd4a`  
		Last Modified: Fri, 26 Mar 2021 15:02:27 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb48f591c9b52db78b487e1f171747e3991a8d80c03c5daebba5ac4a581a2a40`  
		Last Modified: Fri, 26 Mar 2021 15:02:32 GMT  
		Size: 3.3 MB (3250454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:db8157d0fff3ecafb642b368478692c1725bbf579d24f9a407256cc51311b4bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254843982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d07478d5961c109b269709dea43d413e585382caff2dbf68349d92ae066326a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:32:02 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:32:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:32:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 14:54:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Mar 2021 14:54:57 GMT
ENV LANG=C.UTF-8
# Fri, 26 Mar 2021 14:54:58 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Mar 2021 14:54:59 GMT
ENV ROS_DISTRO=dashing
# Fri, 26 Mar 2021 14:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-core=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:57:13 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 14:57:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 14:57:15 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 14:58:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:58:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 14:58:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Mar 2021 14:58:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-dashing-ros-base=0.7.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7088a5fdb71356345c9275386f82ff5adfe26259ac6a250dbb4044a6fdc0019a`  
		Last Modified: Fri, 26 Mar 2021 15:23:30 GMT  
		Size: 841.0 KB (841011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba42aa30b8246822d07c12b6e55f270f35d86257ef50ec34e1b9f02b34c4fbe`  
		Last Modified: Fri, 26 Mar 2021 15:23:27 GMT  
		Size: 4.5 MB (4453640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16613bcbb5a5d178bd2e6f3ee319ecef39d93cedb20e518169ad503abed5a60e`  
		Last Modified: Fri, 26 Mar 2021 15:23:25 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e4165e4b9f027817ea8febc97a2f5024d703055cb1b6888b74ca7b7198a89a`  
		Last Modified: Fri, 26 Mar 2021 15:31:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531bbd277528958f315b3607463d39fcb4c8090d666ea09f0e31902e64abe811`  
		Last Modified: Fri, 26 Mar 2021 15:32:34 GMT  
		Size: 165.1 MB (165087702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768c06ccf48c41fc06107953c51420f27b622545fbf23fd412aad8efd203450`  
		Last Modified: Fri, 26 Mar 2021 15:31:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8a9891682851ddd4c4e83453946971e93aa3732c22d3c6f7c04ddb27cee77a`  
		Last Modified: Fri, 26 Mar 2021 15:32:54 GMT  
		Size: 56.9 MB (56854240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e5c9132009b6d1f9095d471b0eb9704e2bb1ceaf326695c158b0da3c0a398`  
		Last Modified: Fri, 26 Mar 2021 15:32:42 GMT  
		Size: 204.0 KB (204008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c376b691b48c91f57ef2121339ef0cf4ea104ccff4666524cf8617be056a8d`  
		Last Modified: Fri, 26 Mar 2021 15:32:42 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f3088a88aca4ca8e11df08cbba49a9ce0a90621e3a24abd3ba4a90130751b9`  
		Last Modified: Fri, 26 Mar 2021 15:32:45 GMT  
		Size: 3.7 MB (3665657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
