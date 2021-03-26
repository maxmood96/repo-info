## `ros:eloquent-ros1-bridge`

```console
$ docker pull ros@sha256:bd5e5d0afdad0931b3873e0a7e69ce3b336e0b9a9ac8715c8b321215898f7ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:cd85f2415878448b655862f477a9dc977fe63170b20a7df65c8042a5fc988c59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.2 MB (504240909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c451953464d1a8c18e0276625123974aa1671f780218bb9fe39a59c7769f914`
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
# Fri, 26 Mar 2021 13:15:25 GMT
ENV ROS_DISTRO=eloquent
# Fri, 26 Mar 2021 13:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:16:25 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 13:16:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 13:16:26 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:16:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:17:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 13:17:05 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Mar 2021 13:17:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:17:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 13:17:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 13:17:22 GMT
ENV ROS1_DISTRO=melodic
# Fri, 26 Mar 2021 13:17:22 GMT
ENV ROS2_DISTRO=eloquent
# Fri, 26 Mar 2021 13:18:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:19:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:20:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:20:06 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
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
	-	`sha256:100df2279e0dc61904734549ebfd32d6cd11b66ba5e64cc8afb62c303a2caf4c`  
		Last Modified: Fri, 26 Mar 2021 13:43:29 GMT  
		Size: 183.0 MB (183002927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8a7726296fcf934254f1086c0728df460e664e93fa6fcc96b124ddd5d7dfb0`  
		Last Modified: Fri, 26 Mar 2021 13:42:58 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721df4822775d77fcd842f373e76ace94c99dab7fcba95793dd4edf5dcc7a2a4`  
		Last Modified: Fri, 26 Mar 2021 13:43:51 GMT  
		Size: 63.5 MB (63527325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b2d0c4e2be3ad1c781f6ee529decfc33a76a71ea2c399958df431a3147871`  
		Last Modified: Fri, 26 Mar 2021 13:43:45 GMT  
		Size: 202.8 KB (202801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f58cdb26f6f98e32d79c0f5e44724bf2230f99019e4217f116953835d58c6c`  
		Last Modified: Fri, 26 Mar 2021 13:43:40 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200278c4817187e82b2614f5aa70b9f21435d463523f9790ccf98ed5b9f28278`  
		Last Modified: Fri, 26 Mar 2021 13:43:42 GMT  
		Size: 4.6 MB (4587680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe08c9a2091cfd05b77d494ff216e50ba1ee5e29392855d3c448a1f15cefda9`  
		Last Modified: Fri, 26 Mar 2021 13:44:10 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e3179f14de9ef85f235cd98e447032e8d551ef2452102f75ec1635b7108b38`  
		Last Modified: Fri, 26 Mar 2021 13:44:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4131e47e322a9824276b078b912412230bbbe035e3da3f6f3cec5b0fcc73911`  
		Last Modified: Fri, 26 Mar 2021 13:44:35 GMT  
		Size: 117.8 MB (117768169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83add1f84103b410e85015f441727156b8d26fceb0a20bd8b1eea799076f4d7f`  
		Last Modified: Fri, 26 Mar 2021 13:44:31 GMT  
		Size: 102.0 MB (101986470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b396409dcbd538491882ad197e6ebc883d73135f0ffbdb88a89299a3861bf8b4`  
		Last Modified: Fri, 26 Mar 2021 13:44:08 GMT  
		Size: 737.3 KB (737334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7fb4d67dbfea746d698511045dba78dc1477fd41cd2344fbd30761feef3ac`  
		Last Modified: Fri, 26 Mar 2021 13:44:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge` - linux; arm variant v7

```console
$ docker pull ros@sha256:0fb8771ca0c8d9d2e6ab68626a40957d1e02755b8dab8bf0862b07f295d4bc76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429058016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437d802ad042b1c841d77aabb93fe385b089ac319e600b2ae3d62ef9ab3a9ade`
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
# Fri, 26 Mar 2021 14:38:51 GMT
ENV ROS_DISTRO=eloquent
# Fri, 26 Mar 2021 14:41:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:41:23 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 14:41:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 14:41:27 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 14:42:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:43:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 14:43:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Mar 2021 14:43:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:43:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 14:43:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 14:43:56 GMT
ENV ROS1_DISTRO=melodic
# Fri, 26 Mar 2021 14:43:58 GMT
ENV ROS2_DISTRO=eloquent
# Fri, 26 Mar 2021 14:46:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:48:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:48:44 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
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
	-	`sha256:d789262ea8fb4eff0b48299578d090246d2db587c700a54231db330d4eeed6a0`  
		Last Modified: Fri, 26 Mar 2021 15:05:10 GMT  
		Size: 156.6 MB (156611792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0896b9912de18d03e8c0b57242c8862daee3e3499e9e78ced4deb2fbe2ca23ac`  
		Last Modified: Fri, 26 Mar 2021 15:04:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edab81ac439a103f8230bcb284758caad05fe4e69c782d292c254b689d8a90c`  
		Last Modified: Fri, 26 Mar 2021 15:05:41 GMT  
		Size: 47.9 MB (47921016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b5313194c624f0bf8d1450ad4ff01bf5b2007dc453052fea57d00048fbf613`  
		Last Modified: Fri, 26 Mar 2021 15:05:24 GMT  
		Size: 202.8 KB (202804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4713ec5e053ccb37e8613f9f3f0e9db660adc05ae1ad3058c66b2f8273463a3`  
		Last Modified: Fri, 26 Mar 2021 15:05:24 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dd7a72478c74586480dba5f73dc94cae0669ac6b2dafe7a37084f2b1894aa8`  
		Last Modified: Fri, 26 Mar 2021 15:05:31 GMT  
		Size: 3.5 MB (3496589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449a7bf5e1545d6ffb293566d033bad8312c0667bd1cdbd43dea14dfac4cf9ab`  
		Last Modified: Fri, 26 Mar 2021 15:05:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907594ddc7b00e7fba677ff22eaa925f60c9bfc6d962bb67783155231552dd18`  
		Last Modified: Fri, 26 Mar 2021 15:05:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5e720c92e4d72e9a48237429fb860bcc06ff7b6a86dc4081512f6a7734599a`  
		Last Modified: Fri, 26 Mar 2021 15:07:10 GMT  
		Size: 110.6 MB (110647350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc93ec57b841fb210a4739b1943069efe7f2cec495bfd944ec46b2e808bdd06`  
		Last Modified: Fri, 26 Mar 2021 15:06:41 GMT  
		Size: 82.2 MB (82221155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83cc93b928745c60919f76a1359f03853404bcb386e829991f60b7edeae09b9`  
		Last Modified: Fri, 26 Mar 2021 15:05:52 GMT  
		Size: 733.7 KB (733728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe05bc95b11a7c28fd49e5feef6fae3dd794c864625a02ad3ae6574d68addf2`  
		Last Modified: Fri, 26 Mar 2021 15:05:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6320d8a4405a18994d59bd502e0aae1a3c310de6acd9a5eaa27f83e5ae645646
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.1 MB (464137795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2c1cc29e064f1e53407959e5cc64b624fdc707f1d7a1bea45707b78707db51`
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
# Fri, 26 Mar 2021 15:02:08 GMT
ENV ROS_DISTRO=eloquent
# Fri, 26 Mar 2021 15:04:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:04:36 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 26 Mar 2021 15:04:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Mar 2021 15:04:37 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:05:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:05:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Mar 2021 15:05:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Mar 2021 15:06:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-base=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:06:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 26 Mar 2021 15:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 26 Mar 2021 15:06:26 GMT
ENV ROS1_DISTRO=melodic
# Fri, 26 Mar 2021 15:06:27 GMT
ENV ROS2_DISTRO=eloquent
# Fri, 26 Mar 2021 15:08:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-comm=1.14.10-1*     ros-melodic-roscpp-tutorials=0.9.3-1*     ros-melodic-rospy-tutorials=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:09:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros1-bridge=0.8.3-1*     ros-eloquent-demo-nodes-cpp=0.8.4-1*     ros-eloquent-demo-nodes-py=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:09:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     python-rosdep     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:09:45 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
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
	-	`sha256:2bde33bf9f0b84c28763cab88173a2ee0d071b1e376ca1a034e31b2bf6943818`  
		Last Modified: Fri, 26 Mar 2021 15:34:36 GMT  
		Size: 168.4 MB (168420492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825dafc62ee2dbddb5f8920b5c4ccd7357c4da637dc99d2393c63a53b529a242`  
		Last Modified: Fri, 26 Mar 2021 15:33:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd62dbd9f23e28692e234dd8d11bdaf58377d44c424082537bad1e98b56f2a92`  
		Last Modified: Fri, 26 Mar 2021 15:35:00 GMT  
		Size: 56.2 MB (56228806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b062f79bc613cb9cce9e1862075e214e7d81505385107048b424a767fff575`  
		Last Modified: Fri, 26 Mar 2021 15:34:48 GMT  
		Size: 202.8 KB (202812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6c3f7e1cf234d99dbdf81b1b44ac45747710cb51f9f8af58aede2ad076570d`  
		Last Modified: Fri, 26 Mar 2021 15:34:48 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ce603c051a4f549050bbad65dce56902cdd8aa9d590979fe493e7e29784c89`  
		Last Modified: Fri, 26 Mar 2021 15:34:49 GMT  
		Size: 3.9 MB (3934939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01c6f0651800448d8b17dc6795156e2865fddba9502e7e888324b012b301cec`  
		Last Modified: Fri, 26 Mar 2021 15:35:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211f32ff0fb2c82677662dbe83db3d1923be9ce1dbe09e7bcaaa9e986b1904ac`  
		Last Modified: Fri, 26 Mar 2021 15:35:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562a2c1e0b666d8c0abd3bba23a6489328ca7b89166127316b2ec3ee2c3085ea`  
		Last Modified: Fri, 26 Mar 2021 15:35:55 GMT  
		Size: 116.7 MB (116722139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efd6bcd91a4d57001e8a3596051d0b1140813bdf3f4a422b47c99b76fee4c2e`  
		Last Modified: Fri, 26 Mar 2021 15:35:47 GMT  
		Size: 88.9 MB (88860149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e08b9e030339de7ae671ad92459393d61ce8f288fc0549143c3effb65e1f696`  
		Last Modified: Fri, 26 Mar 2021 15:35:21 GMT  
		Size: 735.5 KB (735463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186dfc991cb757eec53389e11f79f4be0d850fb969c8e09497c6bb69a6300447`  
		Last Modified: Fri, 26 Mar 2021 15:35:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
