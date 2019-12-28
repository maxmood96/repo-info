<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:crystal`](#roscrystal)
-	[`ros:crystal-ros-base`](#roscrystal-ros-base)
-	[`ros:crystal-ros-base-bionic`](#roscrystal-ros-base-bionic)
-	[`ros:crystal-ros-core`](#roscrystal-ros-core)
-	[`ros:crystal-ros-core-bionic`](#roscrystal-ros-core-bionic)
-	[`ros:dashing`](#rosdashing)
-	[`ros:dashing-ros-base`](#rosdashing-ros-base)
-	[`ros:dashing-ros-base-bionic`](#rosdashing-ros-base-bionic)
-	[`ros:dashing-ros-core`](#rosdashing-ros-core)
-	[`ros:dashing-ros-core-bionic`](#rosdashing-ros-core-bionic)
-	[`ros:eloquent`](#roseloquent)
-	[`ros:eloquent-ros-base`](#roseloquent-ros-base)
-	[`ros:eloquent-ros-base-bionic`](#roseloquent-ros-base-bionic)
-	[`ros:eloquent-ros-core`](#roseloquent-ros-core)
-	[`ros:eloquent-ros-core-bionic`](#roseloquent-ros-core-bionic)
-	[`ros:kinetic`](#roskinetic)
-	[`ros:kinetic-perception`](#roskinetic-perception)
-	[`ros:kinetic-perception-xenial`](#roskinetic-perception-xenial)
-	[`ros:kinetic-robot`](#roskinetic-robot)
-	[`ros:kinetic-robot-xenial`](#roskinetic-robot-xenial)
-	[`ros:kinetic-ros-base`](#roskinetic-ros-base)
-	[`ros:kinetic-ros-base-xenial`](#roskinetic-ros-base-xenial)
-	[`ros:kinetic-ros-core`](#roskinetic-ros-core)
-	[`ros:kinetic-ros-core-xenial`](#roskinetic-ros-core-xenial)
-	[`ros:latest`](#roslatest)
-	[`ros:melodic`](#rosmelodic)
-	[`ros:melodic-perception`](#rosmelodic-perception)
-	[`ros:melodic-perception-bionic`](#rosmelodic-perception-bionic)
-	[`ros:melodic-perception-stretch`](#rosmelodic-perception-stretch)
-	[`ros:melodic-robot`](#rosmelodic-robot)
-	[`ros:melodic-robot-bionic`](#rosmelodic-robot-bionic)
-	[`ros:melodic-robot-stretch`](#rosmelodic-robot-stretch)
-	[`ros:melodic-ros-base`](#rosmelodic-ros-base)
-	[`ros:melodic-ros-base-bionic`](#rosmelodic-ros-base-bionic)
-	[`ros:melodic-ros-base-stretch`](#rosmelodic-ros-base-stretch)
-	[`ros:melodic-ros-core`](#rosmelodic-ros-core)
-	[`ros:melodic-ros-core-bionic`](#rosmelodic-ros-core-bionic)
-	[`ros:melodic-ros-core-stretch`](#rosmelodic-ros-core-stretch)

## `ros:crystal`

```console
$ docker pull ros@sha256:36fbae6caec095781850aaf95befa125b8754f946fac8ba323fae545877ab1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:crystal` - linux; amd64

```console
$ docker pull ros@sha256:b1af4202c181285f5f442d7980181e1b2320e854fb2fbbf2d2138422507a6f08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262303096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0698a656f4c860433f64c626099751783552db9ce5cbf2f74e4e1651ac0ed2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 08:35:41 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 08:36:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:36:30 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 08:36:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:36:35 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:36:35 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 08:37:12 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:37:13 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:37:31 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86030d638550e81441f6da252a39797dab06865ce8ae14d463520e39e559649`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 2.8 KB (2817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece8d38b909fe9607211392b727e7abee82002662332dc24c59bd968262065ab`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b73e844c0bae862a60484f39bb21b8c75356859ce082b30a682d1ef26e2b0`  
		Last Modified: Thu, 19 Dec 2019 08:47:02 GMT  
		Size: 28.4 MB (28396283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c13ac15ca13fc9b9d483336787f1035fe6b8836045b7a74cf5cc24bed939a7`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 1.0 MB (1002074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6ac3372c0d80649a253ece5234d2d9bfae4edb579505f69cc9f07a078ccd61`  
		Last Modified: Thu, 19 Dec 2019 08:46:52 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafe2728baa9ac7688525ff6c0fe0f0dded176856dbbdcabb28f67f1bf7a32af`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 105.6 KB (105620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1cd2a45d530f0795cf310a6e2438d26760a22940b1ed713409c4f0009d5664`  
		Last Modified: Thu, 19 Dec 2019 08:47:12 GMT  
		Size: 50.1 MB (50059390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dc116ee4bc9e060c26794661883b9d1869733d94d4a2fe53ba8c6824bd4b4`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3cbd2e4d389cc29c79fa67d983806bef9d24ddd107cbae165b8c78adc70088`  
		Last Modified: Thu, 19 Dec 2019 08:47:32 GMT  
		Size: 3.2 MB (3179649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:crystal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7c1fe5e019d78278512963791c1e48efaabd56e2bc983cc465da3b89306c18f0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238427791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a672ae1c1cd0d0b2231feff1755f61bb7c4156406381c29f7f8c0ba5b52cb8e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 09:32:27 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 09:33:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:34:05 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 09:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:34:15 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:34:16 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 09:35:26 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:35:30 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:35:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:35:31 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:35:51 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaad5616b153dafb9a1cece2bd1880697bfd9f89a4531619040669a22459adc`  
		Last Modified: Thu, 19 Dec 2019 09:49:46 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf9be4f838e5862dc76bf33c2d24a0a9b2d176dd2d4c5491b59d98f01506d14`  
		Last Modified: Thu, 19 Dec 2019 09:49:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20055ce1eeea4c2d78a23b5f2b4909d8a7e6ff15440cb5147600c1fecf62a2ae`  
		Last Modified: Thu, 19 Dec 2019 09:49:54 GMT  
		Size: 27.1 MB (27081012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f6068b42c17866001a64eb7b6d46cf01eb5722f3609342507f5efa8f8e5c83`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.0 MB (1002139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77a0280efc0979acb8b1955435e585d751968599d740568d671bbe02a6d860`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0788190750103e17a53267e42e2cfe2bb81c9e9fee4931bd11a9f4c9d2c8b734`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 105.8 KB (105751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a50324387b00b8e5b96f1f213f45d6266df3fadf4a04d22307e8ffa36ded85`  
		Last Modified: Thu, 19 Dec 2019 09:50:00 GMT  
		Size: 39.5 MB (39535906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb418d6d36d90e7c0bbab69f5f4dd6f504fa6f6dddbdb5786e86986716064c7`  
		Last Modified: Thu, 19 Dec 2019 09:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2874da3448b0f240119fc5971a320263e7e966e12750f7bbc662886816a49e0`  
		Last Modified: Thu, 19 Dec 2019 09:50:35 GMT  
		Size: 2.9 MB (2942356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:crystal-ros-base`

```console
$ docker pull ros@sha256:36fbae6caec095781850aaf95befa125b8754f946fac8ba323fae545877ab1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:crystal-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:b1af4202c181285f5f442d7980181e1b2320e854fb2fbbf2d2138422507a6f08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262303096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0698a656f4c860433f64c626099751783552db9ce5cbf2f74e4e1651ac0ed2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 08:35:41 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 08:36:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:36:30 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 08:36:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:36:35 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:36:35 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 08:37:12 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:37:13 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:37:31 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86030d638550e81441f6da252a39797dab06865ce8ae14d463520e39e559649`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 2.8 KB (2817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece8d38b909fe9607211392b727e7abee82002662332dc24c59bd968262065ab`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b73e844c0bae862a60484f39bb21b8c75356859ce082b30a682d1ef26e2b0`  
		Last Modified: Thu, 19 Dec 2019 08:47:02 GMT  
		Size: 28.4 MB (28396283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c13ac15ca13fc9b9d483336787f1035fe6b8836045b7a74cf5cc24bed939a7`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 1.0 MB (1002074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6ac3372c0d80649a253ece5234d2d9bfae4edb579505f69cc9f07a078ccd61`  
		Last Modified: Thu, 19 Dec 2019 08:46:52 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafe2728baa9ac7688525ff6c0fe0f0dded176856dbbdcabb28f67f1bf7a32af`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 105.6 KB (105620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1cd2a45d530f0795cf310a6e2438d26760a22940b1ed713409c4f0009d5664`  
		Last Modified: Thu, 19 Dec 2019 08:47:12 GMT  
		Size: 50.1 MB (50059390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dc116ee4bc9e060c26794661883b9d1869733d94d4a2fe53ba8c6824bd4b4`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3cbd2e4d389cc29c79fa67d983806bef9d24ddd107cbae165b8c78adc70088`  
		Last Modified: Thu, 19 Dec 2019 08:47:32 GMT  
		Size: 3.2 MB (3179649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:crystal-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7c1fe5e019d78278512963791c1e48efaabd56e2bc983cc465da3b89306c18f0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238427791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a672ae1c1cd0d0b2231feff1755f61bb7c4156406381c29f7f8c0ba5b52cb8e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 09:32:27 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 09:33:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:34:05 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 09:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:34:15 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:34:16 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 09:35:26 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:35:30 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:35:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:35:31 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:35:51 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaad5616b153dafb9a1cece2bd1880697bfd9f89a4531619040669a22459adc`  
		Last Modified: Thu, 19 Dec 2019 09:49:46 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf9be4f838e5862dc76bf33c2d24a0a9b2d176dd2d4c5491b59d98f01506d14`  
		Last Modified: Thu, 19 Dec 2019 09:49:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20055ce1eeea4c2d78a23b5f2b4909d8a7e6ff15440cb5147600c1fecf62a2ae`  
		Last Modified: Thu, 19 Dec 2019 09:49:54 GMT  
		Size: 27.1 MB (27081012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f6068b42c17866001a64eb7b6d46cf01eb5722f3609342507f5efa8f8e5c83`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.0 MB (1002139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77a0280efc0979acb8b1955435e585d751968599d740568d671bbe02a6d860`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0788190750103e17a53267e42e2cfe2bb81c9e9fee4931bd11a9f4c9d2c8b734`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 105.8 KB (105751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a50324387b00b8e5b96f1f213f45d6266df3fadf4a04d22307e8ffa36ded85`  
		Last Modified: Thu, 19 Dec 2019 09:50:00 GMT  
		Size: 39.5 MB (39535906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb418d6d36d90e7c0bbab69f5f4dd6f504fa6f6dddbdb5786e86986716064c7`  
		Last Modified: Thu, 19 Dec 2019 09:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2874da3448b0f240119fc5971a320263e7e966e12750f7bbc662886816a49e0`  
		Last Modified: Thu, 19 Dec 2019 09:50:35 GMT  
		Size: 2.9 MB (2942356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:crystal-ros-base-bionic`

```console
$ docker pull ros@sha256:36fbae6caec095781850aaf95befa125b8754f946fac8ba323fae545877ab1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:crystal-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:b1af4202c181285f5f442d7980181e1b2320e854fb2fbbf2d2138422507a6f08
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262303096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0698a656f4c860433f64c626099751783552db9ce5cbf2f74e4e1651ac0ed2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 08:35:41 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 08:36:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:36:30 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 08:36:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:36:35 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:36:35 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 08:37:12 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:37:13 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:37:31 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86030d638550e81441f6da252a39797dab06865ce8ae14d463520e39e559649`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 2.8 KB (2817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece8d38b909fe9607211392b727e7abee82002662332dc24c59bd968262065ab`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b73e844c0bae862a60484f39bb21b8c75356859ce082b30a682d1ef26e2b0`  
		Last Modified: Thu, 19 Dec 2019 08:47:02 GMT  
		Size: 28.4 MB (28396283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c13ac15ca13fc9b9d483336787f1035fe6b8836045b7a74cf5cc24bed939a7`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 1.0 MB (1002074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6ac3372c0d80649a253ece5234d2d9bfae4edb579505f69cc9f07a078ccd61`  
		Last Modified: Thu, 19 Dec 2019 08:46:52 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafe2728baa9ac7688525ff6c0fe0f0dded176856dbbdcabb28f67f1bf7a32af`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 105.6 KB (105620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1cd2a45d530f0795cf310a6e2438d26760a22940b1ed713409c4f0009d5664`  
		Last Modified: Thu, 19 Dec 2019 08:47:12 GMT  
		Size: 50.1 MB (50059390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dc116ee4bc9e060c26794661883b9d1869733d94d4a2fe53ba8c6824bd4b4`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3cbd2e4d389cc29c79fa67d983806bef9d24ddd107cbae165b8c78adc70088`  
		Last Modified: Thu, 19 Dec 2019 08:47:32 GMT  
		Size: 3.2 MB (3179649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:crystal-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7c1fe5e019d78278512963791c1e48efaabd56e2bc983cc465da3b89306c18f0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238427791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a672ae1c1cd0d0b2231feff1755f61bb7c4156406381c29f7f8c0ba5b52cb8e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 09:32:27 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 09:33:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:34:05 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 09:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:34:15 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:34:16 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 09:35:26 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:35:30 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:35:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:35:31 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:35:51 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-base=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaad5616b153dafb9a1cece2bd1880697bfd9f89a4531619040669a22459adc`  
		Last Modified: Thu, 19 Dec 2019 09:49:46 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf9be4f838e5862dc76bf33c2d24a0a9b2d176dd2d4c5491b59d98f01506d14`  
		Last Modified: Thu, 19 Dec 2019 09:49:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20055ce1eeea4c2d78a23b5f2b4909d8a7e6ff15440cb5147600c1fecf62a2ae`  
		Last Modified: Thu, 19 Dec 2019 09:49:54 GMT  
		Size: 27.1 MB (27081012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f6068b42c17866001a64eb7b6d46cf01eb5722f3609342507f5efa8f8e5c83`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.0 MB (1002139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77a0280efc0979acb8b1955435e585d751968599d740568d671bbe02a6d860`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0788190750103e17a53267e42e2cfe2bb81c9e9fee4931bd11a9f4c9d2c8b734`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 105.8 KB (105751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a50324387b00b8e5b96f1f213f45d6266df3fadf4a04d22307e8ffa36ded85`  
		Last Modified: Thu, 19 Dec 2019 09:50:00 GMT  
		Size: 39.5 MB (39535906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb418d6d36d90e7c0bbab69f5f4dd6f504fa6f6dddbdb5786e86986716064c7`  
		Last Modified: Thu, 19 Dec 2019 09:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2874da3448b0f240119fc5971a320263e7e966e12750f7bbc662886816a49e0`  
		Last Modified: Thu, 19 Dec 2019 09:50:35 GMT  
		Size: 2.9 MB (2942356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:crystal-ros-core`

```console
$ docker pull ros@sha256:657b0f5372752f0caf1b7990257bfb00f9e3016004950898d1be51bafa8f988e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:crystal-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:7f35c16542988c0ef1ac8aeb535e00342d8987532f53fc1462e350835dfd3a90
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259123447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e8cdce41b460e131c938105da9232e4ee08cc8aa49e80d42537a5f5b151590`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 08:35:41 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 08:36:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:36:30 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 08:36:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:36:35 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:36:35 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 08:37:12 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:37:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86030d638550e81441f6da252a39797dab06865ce8ae14d463520e39e559649`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 2.8 KB (2817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece8d38b909fe9607211392b727e7abee82002662332dc24c59bd968262065ab`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b73e844c0bae862a60484f39bb21b8c75356859ce082b30a682d1ef26e2b0`  
		Last Modified: Thu, 19 Dec 2019 08:47:02 GMT  
		Size: 28.4 MB (28396283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c13ac15ca13fc9b9d483336787f1035fe6b8836045b7a74cf5cc24bed939a7`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 1.0 MB (1002074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6ac3372c0d80649a253ece5234d2d9bfae4edb579505f69cc9f07a078ccd61`  
		Last Modified: Thu, 19 Dec 2019 08:46:52 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafe2728baa9ac7688525ff6c0fe0f0dded176856dbbdcabb28f67f1bf7a32af`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 105.6 KB (105620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1cd2a45d530f0795cf310a6e2438d26760a22940b1ed713409c4f0009d5664`  
		Last Modified: Thu, 19 Dec 2019 08:47:12 GMT  
		Size: 50.1 MB (50059390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dc116ee4bc9e060c26794661883b9d1869733d94d4a2fe53ba8c6824bd4b4`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:crystal-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:afef2b896e27833f74529f2fc0b22e87a693965c256cb4f7e7fbc648d7218f94
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235485435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfab838c40e7efdbe85d7784ee019e8915a9bb0629c148ec6c4614993f711da`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 09:32:27 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 09:33:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:34:05 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 09:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:34:15 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:34:16 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 09:35:26 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:35:30 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:35:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:35:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaad5616b153dafb9a1cece2bd1880697bfd9f89a4531619040669a22459adc`  
		Last Modified: Thu, 19 Dec 2019 09:49:46 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf9be4f838e5862dc76bf33c2d24a0a9b2d176dd2d4c5491b59d98f01506d14`  
		Last Modified: Thu, 19 Dec 2019 09:49:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20055ce1eeea4c2d78a23b5f2b4909d8a7e6ff15440cb5147600c1fecf62a2ae`  
		Last Modified: Thu, 19 Dec 2019 09:49:54 GMT  
		Size: 27.1 MB (27081012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f6068b42c17866001a64eb7b6d46cf01eb5722f3609342507f5efa8f8e5c83`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.0 MB (1002139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77a0280efc0979acb8b1955435e585d751968599d740568d671bbe02a6d860`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0788190750103e17a53267e42e2cfe2bb81c9e9fee4931bd11a9f4c9d2c8b734`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 105.8 KB (105751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a50324387b00b8e5b96f1f213f45d6266df3fadf4a04d22307e8ffa36ded85`  
		Last Modified: Thu, 19 Dec 2019 09:50:00 GMT  
		Size: 39.5 MB (39535906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb418d6d36d90e7c0bbab69f5f4dd6f504fa6f6dddbdb5786e86986716064c7`  
		Last Modified: Thu, 19 Dec 2019 09:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:crystal-ros-core-bionic`

```console
$ docker pull ros@sha256:657b0f5372752f0caf1b7990257bfb00f9e3016004950898d1be51bafa8f988e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:crystal-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:7f35c16542988c0ef1ac8aeb535e00342d8987532f53fc1462e350835dfd3a90
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259123447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e8cdce41b460e131c938105da9232e4ee08cc8aa49e80d42537a5f5b151590`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 08:35:41 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 08:36:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:36:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:36:30 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 08:36:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:36:35 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:36:35 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 08:37:12 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:12 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:37:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:37:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86030d638550e81441f6da252a39797dab06865ce8ae14d463520e39e559649`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 2.8 KB (2817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece8d38b909fe9607211392b727e7abee82002662332dc24c59bd968262065ab`  
		Last Modified: Thu, 19 Dec 2019 08:46:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310b73e844c0bae862a60484f39bb21b8c75356859ce082b30a682d1ef26e2b0`  
		Last Modified: Thu, 19 Dec 2019 08:47:02 GMT  
		Size: 28.4 MB (28396283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c13ac15ca13fc9b9d483336787f1035fe6b8836045b7a74cf5cc24bed939a7`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 1.0 MB (1002074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6ac3372c0d80649a253ece5234d2d9bfae4edb579505f69cc9f07a078ccd61`  
		Last Modified: Thu, 19 Dec 2019 08:46:52 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafe2728baa9ac7688525ff6c0fe0f0dded176856dbbdcabb28f67f1bf7a32af`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 105.6 KB (105620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1cd2a45d530f0795cf310a6e2438d26760a22940b1ed713409c4f0009d5664`  
		Last Modified: Thu, 19 Dec 2019 08:47:12 GMT  
		Size: 50.1 MB (50059390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dc116ee4bc9e060c26794661883b9d1869733d94d4a2fe53ba8c6824bd4b4`  
		Last Modified: Thu, 19 Dec 2019 08:46:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:crystal-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:afef2b896e27833f74529f2fc0b22e87a693965c256cb4f7e7fbc648d7218f94
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235485435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfab838c40e7efdbe85d7784ee019e8915a9bb0629c148ec6c4614993f711da`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Thu, 19 Dec 2019 09:32:27 GMT
RUN echo "deb http://snapshots.ros.org/crystal/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Thu, 19 Dec 2019 09:33:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:33:26 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:34:05 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Thu, 19 Dec 2019 09:34:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:34:15 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:34:16 GMT
ENV ROS_DISTRO=crystal
# Thu, 19 Dec 2019 09:35:26 GMT
RUN apt-get update && apt-get install -y     ros-crystal-ros-core=0.6.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:35:30 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:35:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:35:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaad5616b153dafb9a1cece2bd1880697bfd9f89a4531619040669a22459adc`  
		Last Modified: Thu, 19 Dec 2019 09:49:46 GMT  
		Size: 2.8 KB (2818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf9be4f838e5862dc76bf33c2d24a0a9b2d176dd2d4c5491b59d98f01506d14`  
		Last Modified: Thu, 19 Dec 2019 09:49:47 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20055ce1eeea4c2d78a23b5f2b4909d8a7e6ff15440cb5147600c1fecf62a2ae`  
		Last Modified: Thu, 19 Dec 2019 09:49:54 GMT  
		Size: 27.1 MB (27081012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f6068b42c17866001a64eb7b6d46cf01eb5722f3609342507f5efa8f8e5c83`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.0 MB (1002139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac77a0280efc0979acb8b1955435e585d751968599d740568d671bbe02a6d860`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0788190750103e17a53267e42e2cfe2bb81c9e9fee4931bd11a9f4c9d2c8b734`  
		Last Modified: Thu, 19 Dec 2019 09:49:45 GMT  
		Size: 105.8 KB (105751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a50324387b00b8e5b96f1f213f45d6266df3fadf4a04d22307e8ffa36ded85`  
		Last Modified: Thu, 19 Dec 2019 09:50:00 GMT  
		Size: 39.5 MB (39535906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb418d6d36d90e7c0bbab69f5f4dd6f504fa6f6dddbdb5786e86986716064c7`  
		Last Modified: Thu, 19 Dec 2019 09:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:dashing`

```console
$ docker pull ros@sha256:0572dd7b711da0ca207d914741eb55e3722d0779ad80fa58e70d704c8add3093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing` - linux; amd64

```console
$ docker pull ros@sha256:fe5a09241a2948911ea8b057386eb26f2e8d92a0f63b9b2d9023c9b68c419665
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280940254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958b9968a148ab097ba84453efeff88a97af7884f0f2d314654dcaf6126edff0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:38:15 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 08:38:53 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:38:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:38:54 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:39:11 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167ea1381276c7dc7b04edd787bcf75df5dbb8ff710b2c43ecccd1f8f6612069`  
		Last Modified: Thu, 19 Dec 2019 08:47:58 GMT  
		Size: 68.1 MB (68081869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890c70469f4c63a0a02b99782e6899dedb31822c49c5acff0b0e3f7e80206b70`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42ebbc26e5b1b6307858be5b3120f4aaa45fd058eb3ae2b5db634935fc5e290`  
		Last Modified: Thu, 19 Dec 2019 08:48:12 GMT  
		Size: 4.3 MB (4340016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing` - linux; arm variant v7

```console
$ docker pull ros@sha256:7a36518f9c3cbcf3ca30f2107d22f6879978fd6015c11a20b3e9aa5120b90078
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235170107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b4c04adb7029da84a9964d4b951a62f8c71981c2662e23f559f4793b921d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:19:40 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 07:21:14 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:21:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:21:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:21:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:21:56 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3616636fd9e22c226258c2d07af2460a21fd2510bd65ed92041c49a19e5ac34a`  
		Last Modified: Thu, 19 Dec 2019 07:32:37 GMT  
		Size: 49.3 MB (49261159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9722a50c0942731d1e428e25d664a464c1c4d7ad1b62bab3a646826b7f376c`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ad35ba3457422b4935bb6210534847d2877109a18b163af69257d57068650`  
		Last Modified: Thu, 19 Dec 2019 07:33:04 GMT  
		Size: 3.3 MB (3277913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:91945d503892408172e3ed8e0ca9f76a97c613692ce75f0bec36ce45c64cb371
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254657910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf6210c9322c9246c7c7178851d9fefe7ba3b007b11b6a8d5bfeca06c355baf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:37:34 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 09:38:57 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:39:02 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:39:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:39:04 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:39:32 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189f3f63dd5200825062e434a3ab79fc1dd5131d5e610f447d83ca295b6327d8`  
		Last Modified: Thu, 19 Dec 2019 09:51:05 GMT  
		Size: 55.6 MB (55559160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b6d0678809644c627168e16f34064ed60f3681e2965a73c4e56a3b15e60471`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c531b03e7d74d9fe667c8f76f8f2e30eaa800a55406487c13eb5efadfce7f0`  
		Last Modified: Thu, 19 Dec 2019 09:51:14 GMT  
		Size: 3.7 MB (3692349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:dashing-ros-base`

```console
$ docker pull ros@sha256:0572dd7b711da0ca207d914741eb55e3722d0779ad80fa58e70d704c8add3093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:fe5a09241a2948911ea8b057386eb26f2e8d92a0f63b9b2d9023c9b68c419665
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280940254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958b9968a148ab097ba84453efeff88a97af7884f0f2d314654dcaf6126edff0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:38:15 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 08:38:53 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:38:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:38:54 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:39:11 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167ea1381276c7dc7b04edd787bcf75df5dbb8ff710b2c43ecccd1f8f6612069`  
		Last Modified: Thu, 19 Dec 2019 08:47:58 GMT  
		Size: 68.1 MB (68081869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890c70469f4c63a0a02b99782e6899dedb31822c49c5acff0b0e3f7e80206b70`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42ebbc26e5b1b6307858be5b3120f4aaa45fd058eb3ae2b5db634935fc5e290`  
		Last Modified: Thu, 19 Dec 2019 08:48:12 GMT  
		Size: 4.3 MB (4340016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:7a36518f9c3cbcf3ca30f2107d22f6879978fd6015c11a20b3e9aa5120b90078
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235170107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b4c04adb7029da84a9964d4b951a62f8c71981c2662e23f559f4793b921d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:19:40 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 07:21:14 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:21:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:21:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:21:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:21:56 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3616636fd9e22c226258c2d07af2460a21fd2510bd65ed92041c49a19e5ac34a`  
		Last Modified: Thu, 19 Dec 2019 07:32:37 GMT  
		Size: 49.3 MB (49261159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9722a50c0942731d1e428e25d664a464c1c4d7ad1b62bab3a646826b7f376c`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ad35ba3457422b4935bb6210534847d2877109a18b163af69257d57068650`  
		Last Modified: Thu, 19 Dec 2019 07:33:04 GMT  
		Size: 3.3 MB (3277913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:91945d503892408172e3ed8e0ca9f76a97c613692ce75f0bec36ce45c64cb371
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254657910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf6210c9322c9246c7c7178851d9fefe7ba3b007b11b6a8d5bfeca06c355baf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:37:34 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 09:38:57 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:39:02 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:39:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:39:04 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:39:32 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189f3f63dd5200825062e434a3ab79fc1dd5131d5e610f447d83ca295b6327d8`  
		Last Modified: Thu, 19 Dec 2019 09:51:05 GMT  
		Size: 55.6 MB (55559160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b6d0678809644c627168e16f34064ed60f3681e2965a73c4e56a3b15e60471`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c531b03e7d74d9fe667c8f76f8f2e30eaa800a55406487c13eb5efadfce7f0`  
		Last Modified: Thu, 19 Dec 2019 09:51:14 GMT  
		Size: 3.7 MB (3692349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:dashing-ros-base-bionic`

```console
$ docker pull ros@sha256:0572dd7b711da0ca207d914741eb55e3722d0779ad80fa58e70d704c8add3093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:fe5a09241a2948911ea8b057386eb26f2e8d92a0f63b9b2d9023c9b68c419665
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280940254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958b9968a148ab097ba84453efeff88a97af7884f0f2d314654dcaf6126edff0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:38:15 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 08:38:53 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:38:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:38:54 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:39:11 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167ea1381276c7dc7b04edd787bcf75df5dbb8ff710b2c43ecccd1f8f6612069`  
		Last Modified: Thu, 19 Dec 2019 08:47:58 GMT  
		Size: 68.1 MB (68081869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890c70469f4c63a0a02b99782e6899dedb31822c49c5acff0b0e3f7e80206b70`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42ebbc26e5b1b6307858be5b3120f4aaa45fd058eb3ae2b5db634935fc5e290`  
		Last Modified: Thu, 19 Dec 2019 08:48:12 GMT  
		Size: 4.3 MB (4340016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:7a36518f9c3cbcf3ca30f2107d22f6879978fd6015c11a20b3e9aa5120b90078
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235170107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b4c04adb7029da84a9964d4b951a62f8c71981c2662e23f559f4793b921d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:19:40 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 07:21:14 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:21:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:21:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:21:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:21:56 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3616636fd9e22c226258c2d07af2460a21fd2510bd65ed92041c49a19e5ac34a`  
		Last Modified: Thu, 19 Dec 2019 07:32:37 GMT  
		Size: 49.3 MB (49261159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9722a50c0942731d1e428e25d664a464c1c4d7ad1b62bab3a646826b7f376c`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ad35ba3457422b4935bb6210534847d2877109a18b163af69257d57068650`  
		Last Modified: Thu, 19 Dec 2019 07:33:04 GMT  
		Size: 3.3 MB (3277913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:91945d503892408172e3ed8e0ca9f76a97c613692ce75f0bec36ce45c64cb371
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254657910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf6210c9322c9246c7c7178851d9fefe7ba3b007b11b6a8d5bfeca06c355baf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:37:34 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 09:38:57 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:39:02 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:39:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:39:04 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:39:32 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-base=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189f3f63dd5200825062e434a3ab79fc1dd5131d5e610f447d83ca295b6327d8`  
		Last Modified: Thu, 19 Dec 2019 09:51:05 GMT  
		Size: 55.6 MB (55559160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b6d0678809644c627168e16f34064ed60f3681e2965a73c4e56a3b15e60471`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c531b03e7d74d9fe667c8f76f8f2e30eaa800a55406487c13eb5efadfce7f0`  
		Last Modified: Thu, 19 Dec 2019 09:51:14 GMT  
		Size: 3.7 MB (3692349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:dashing-ros-core`

```console
$ docker pull ros@sha256:5882cb19c5494981f64250ec4cf0b61ef261a83d7407f16e352002f6f1522cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:85deb08a47d1c843e53d18840f162b20ec9141000b0902d0d980487fe2753798
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276600238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ddcfdd7528a7758e8b2b5e50ea533989b464b09ca25727c163159b7995bd8f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:38:15 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 08:38:53 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:38:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:38:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167ea1381276c7dc7b04edd787bcf75df5dbb8ff710b2c43ecccd1f8f6612069`  
		Last Modified: Thu, 19 Dec 2019 08:47:58 GMT  
		Size: 68.1 MB (68081869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890c70469f4c63a0a02b99782e6899dedb31822c49c5acff0b0e3f7e80206b70`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:66b0dcd3f0208294a057a97186d022b1e7695791ac22b84a8a7525292a686b49
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231892194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abc3ace1a8e0d4fc372656c1050e31c9206e8e7909ae046b3bfdda0718c62a9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:19:40 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 07:21:14 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:21:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:21:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:21:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3616636fd9e22c226258c2d07af2460a21fd2510bd65ed92041c49a19e5ac34a`  
		Last Modified: Thu, 19 Dec 2019 07:32:37 GMT  
		Size: 49.3 MB (49261159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9722a50c0942731d1e428e25d664a464c1c4d7ad1b62bab3a646826b7f376c`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fc7335f8f5e2144567350cab090f38fbe571265f3ab33957ca647ff29a5b7673
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250965561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe785a983a2d8473e81f13dfdac78247055ac4a2cf92bcb6be4fc56c7ff3acb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:37:34 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 09:38:57 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:39:02 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:39:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:39:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189f3f63dd5200825062e434a3ab79fc1dd5131d5e610f447d83ca295b6327d8`  
		Last Modified: Thu, 19 Dec 2019 09:51:05 GMT  
		Size: 55.6 MB (55559160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b6d0678809644c627168e16f34064ed60f3681e2965a73c4e56a3b15e60471`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:dashing-ros-core-bionic`

```console
$ docker pull ros@sha256:5882cb19c5494981f64250ec4cf0b61ef261a83d7407f16e352002f6f1522cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:dashing-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:85deb08a47d1c843e53d18840f162b20ec9141000b0902d0d980487fe2753798
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276600238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ddcfdd7528a7758e8b2b5e50ea533989b464b09ca25727c163159b7995bd8f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:38:15 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 08:38:53 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:54 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:38:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:38:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167ea1381276c7dc7b04edd787bcf75df5dbb8ff710b2c43ecccd1f8f6612069`  
		Last Modified: Thu, 19 Dec 2019 08:47:58 GMT  
		Size: 68.1 MB (68081869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890c70469f4c63a0a02b99782e6899dedb31822c49c5acff0b0e3f7e80206b70`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:66b0dcd3f0208294a057a97186d022b1e7695791ac22b84a8a7525292a686b49
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231892194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abc3ace1a8e0d4fc372656c1050e31c9206e8e7909ae046b3bfdda0718c62a9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:19:40 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 07:21:14 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:21:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:21:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:21:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3616636fd9e22c226258c2d07af2460a21fd2510bd65ed92041c49a19e5ac34a`  
		Last Modified: Thu, 19 Dec 2019 07:32:37 GMT  
		Size: 49.3 MB (49261159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9722a50c0942731d1e428e25d664a464c1c4d7ad1b62bab3a646826b7f376c`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:dashing-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fc7335f8f5e2144567350cab090f38fbe571265f3ab33957ca647ff29a5b7673
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250965561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe785a983a2d8473e81f13dfdac78247055ac4a2cf92bcb6be4fc56c7ff3acb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:37:34 GMT
ENV ROS_DISTRO=dashing
# Thu, 19 Dec 2019 09:38:57 GMT
RUN apt-get update && apt-get install -y     ros-dashing-ros-core=0.7.3-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:39:02 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:39:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:39:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189f3f63dd5200825062e434a3ab79fc1dd5131d5e610f447d83ca295b6327d8`  
		Last Modified: Thu, 19 Dec 2019 09:51:05 GMT  
		Size: 55.6 MB (55559160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b6d0678809644c627168e16f34064ed60f3681e2965a73c4e56a3b15e60471`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:eloquent`

```console
$ docker pull ros@sha256:4076f27d1138c5d75040757fa431cd8e923796df571d9d5544060b0dfe8d55b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent` - linux; amd64

```console
$ docker pull ros@sha256:bcb5d85c19485663b42c2031d79e6eb5ae8e8132d83922dcb10682b26ede88da
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283189197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fb12488000f98dc50ce7c550ab411d3bf9557bdfecca4e9b9c3ff194231e7b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:39:15 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 08:39:54 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:39:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:39:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:39:55 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:40:09 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2771b910aaad0e851dedbe69f2541e1e824ed2aa8f38727952ede7ea89d7f`  
		Last Modified: Thu, 19 Dec 2019 08:48:40 GMT  
		Size: 70.1 MB (70069689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6b8110d43d20db1dd17be79b05a909412d13eadd0e237abf6e919675b7e794`  
		Last Modified: Thu, 19 Dec 2019 08:48:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e331685dbdd14b2be46cc74667378ffe7f1a30cf710591b213fb83d4916e464`  
		Last Modified: Thu, 19 Dec 2019 08:48:51 GMT  
		Size: 4.6 MB (4601139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent` - linux; arm variant v7

```console
$ docker pull ros@sha256:4173a695b9610d23dd073e259afccaf3cf48ad5e657c519a5ab9824b19510c38
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236995043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63768acd9c2f6213a77f570d3cb846aba0b77eb50b7fff1c30c709d3a1dbba3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:22:03 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 07:23:43 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:23:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:23:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:23:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:24:22 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85320bb83837978f50bbd3baf84dea4b922e0b0218feb192ee0c7421258cc7`  
		Last Modified: Thu, 19 Dec 2019 07:33:33 GMT  
		Size: 50.8 MB (50848227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4350cb886547c239fa13e66d7ad666bcb99708c8af8d8b1971c4c41f8d28798a`  
		Last Modified: Thu, 19 Dec 2019 07:33:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcf385c37266da67c2efbf8727369a97dff9c1b4a5fe5000da790f158619882`  
		Last Modified: Thu, 19 Dec 2019 07:33:46 GMT  
		Size: 3.5 MB (3515780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e4ad7ce945bfbc722b57867202bb478d9a5a16e6e415364733d35aa1392e2c32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256759854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b71386b931ec4d533aae304dbe2a7561272b020bbc4927e5deecde2754f4f0f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:39:38 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 09:41:03 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:41:07 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:41:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:41:09 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:41:39 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a31c3e5f5c6d7bdff677a1c2ca244f9ed373f0d4abe4742c97676c2dbde2523`  
		Last Modified: Thu, 19 Dec 2019 09:51:43 GMT  
		Size: 57.4 MB (57400446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9c35595f41a6221be1b6d19e20a50234f79967a968819173bcee35c6de7d1c`  
		Last Modified: Thu, 19 Dec 2019 09:51:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f6ac8fdba9e6e6ef8fb0365c860ecd3b7a2cba6434bafb6f00651a3dbc90eb`  
		Last Modified: Thu, 19 Dec 2019 09:51:56 GMT  
		Size: 4.0 MB (3953006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:eloquent-ros-base`

```console
$ docker pull ros@sha256:4076f27d1138c5d75040757fa431cd8e923796df571d9d5544060b0dfe8d55b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:bcb5d85c19485663b42c2031d79e6eb5ae8e8132d83922dcb10682b26ede88da
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283189197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fb12488000f98dc50ce7c550ab411d3bf9557bdfecca4e9b9c3ff194231e7b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:39:15 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 08:39:54 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:39:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:39:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:39:55 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:40:09 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2771b910aaad0e851dedbe69f2541e1e824ed2aa8f38727952ede7ea89d7f`  
		Last Modified: Thu, 19 Dec 2019 08:48:40 GMT  
		Size: 70.1 MB (70069689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6b8110d43d20db1dd17be79b05a909412d13eadd0e237abf6e919675b7e794`  
		Last Modified: Thu, 19 Dec 2019 08:48:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e331685dbdd14b2be46cc74667378ffe7f1a30cf710591b213fb83d4916e464`  
		Last Modified: Thu, 19 Dec 2019 08:48:51 GMT  
		Size: 4.6 MB (4601139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:4173a695b9610d23dd073e259afccaf3cf48ad5e657c519a5ab9824b19510c38
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236995043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63768acd9c2f6213a77f570d3cb846aba0b77eb50b7fff1c30c709d3a1dbba3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:22:03 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 07:23:43 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:23:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:23:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:23:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:24:22 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85320bb83837978f50bbd3baf84dea4b922e0b0218feb192ee0c7421258cc7`  
		Last Modified: Thu, 19 Dec 2019 07:33:33 GMT  
		Size: 50.8 MB (50848227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4350cb886547c239fa13e66d7ad666bcb99708c8af8d8b1971c4c41f8d28798a`  
		Last Modified: Thu, 19 Dec 2019 07:33:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcf385c37266da67c2efbf8727369a97dff9c1b4a5fe5000da790f158619882`  
		Last Modified: Thu, 19 Dec 2019 07:33:46 GMT  
		Size: 3.5 MB (3515780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e4ad7ce945bfbc722b57867202bb478d9a5a16e6e415364733d35aa1392e2c32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256759854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b71386b931ec4d533aae304dbe2a7561272b020bbc4927e5deecde2754f4f0f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:39:38 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 09:41:03 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:41:07 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:41:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:41:09 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:41:39 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a31c3e5f5c6d7bdff677a1c2ca244f9ed373f0d4abe4742c97676c2dbde2523`  
		Last Modified: Thu, 19 Dec 2019 09:51:43 GMT  
		Size: 57.4 MB (57400446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9c35595f41a6221be1b6d19e20a50234f79967a968819173bcee35c6de7d1c`  
		Last Modified: Thu, 19 Dec 2019 09:51:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f6ac8fdba9e6e6ef8fb0365c860ecd3b7a2cba6434bafb6f00651a3dbc90eb`  
		Last Modified: Thu, 19 Dec 2019 09:51:56 GMT  
		Size: 4.0 MB (3953006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:eloquent-ros-base-bionic`

```console
$ docker pull ros@sha256:4076f27d1138c5d75040757fa431cd8e923796df571d9d5544060b0dfe8d55b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:bcb5d85c19485663b42c2031d79e6eb5ae8e8132d83922dcb10682b26ede88da
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283189197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fb12488000f98dc50ce7c550ab411d3bf9557bdfecca4e9b9c3ff194231e7b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:39:15 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 08:39:54 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:39:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:39:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:39:55 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:40:09 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2771b910aaad0e851dedbe69f2541e1e824ed2aa8f38727952ede7ea89d7f`  
		Last Modified: Thu, 19 Dec 2019 08:48:40 GMT  
		Size: 70.1 MB (70069689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6b8110d43d20db1dd17be79b05a909412d13eadd0e237abf6e919675b7e794`  
		Last Modified: Thu, 19 Dec 2019 08:48:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e331685dbdd14b2be46cc74667378ffe7f1a30cf710591b213fb83d4916e464`  
		Last Modified: Thu, 19 Dec 2019 08:48:51 GMT  
		Size: 4.6 MB (4601139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:4173a695b9610d23dd073e259afccaf3cf48ad5e657c519a5ab9824b19510c38
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236995043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63768acd9c2f6213a77f570d3cb846aba0b77eb50b7fff1c30c709d3a1dbba3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:22:03 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 07:23:43 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:23:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:23:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:23:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:24:22 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85320bb83837978f50bbd3baf84dea4b922e0b0218feb192ee0c7421258cc7`  
		Last Modified: Thu, 19 Dec 2019 07:33:33 GMT  
		Size: 50.8 MB (50848227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4350cb886547c239fa13e66d7ad666bcb99708c8af8d8b1971c4c41f8d28798a`  
		Last Modified: Thu, 19 Dec 2019 07:33:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcf385c37266da67c2efbf8727369a97dff9c1b4a5fe5000da790f158619882`  
		Last Modified: Thu, 19 Dec 2019 07:33:46 GMT  
		Size: 3.5 MB (3515780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e4ad7ce945bfbc722b57867202bb478d9a5a16e6e415364733d35aa1392e2c32
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256759854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b71386b931ec4d533aae304dbe2a7561272b020bbc4927e5deecde2754f4f0f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:39:38 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 09:41:03 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:41:07 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:41:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:41:09 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:41:39 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-base=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a31c3e5f5c6d7bdff677a1c2ca244f9ed373f0d4abe4742c97676c2dbde2523`  
		Last Modified: Thu, 19 Dec 2019 09:51:43 GMT  
		Size: 57.4 MB (57400446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9c35595f41a6221be1b6d19e20a50234f79967a968819173bcee35c6de7d1c`  
		Last Modified: Thu, 19 Dec 2019 09:51:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f6ac8fdba9e6e6ef8fb0365c860ecd3b7a2cba6434bafb6f00651a3dbc90eb`  
		Last Modified: Thu, 19 Dec 2019 09:51:56 GMT  
		Size: 4.0 MB (3953006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:eloquent-ros-core`

```console
$ docker pull ros@sha256:1f87fb45c3fb2206a2d0d263bff1d8a1ed98eff95082c8ee31d098a48bc42c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:67728aad1dbf9862a6a22053bffcef42ff9f8867094ec752b871aea638a02a24
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278588058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37edfccaf6b945622788fa59772f36ebecb0add5e67218c8da1635a2bf5c940`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:39:15 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 08:39:54 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:39:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:39:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:39:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2771b910aaad0e851dedbe69f2541e1e824ed2aa8f38727952ede7ea89d7f`  
		Last Modified: Thu, 19 Dec 2019 08:48:40 GMT  
		Size: 70.1 MB (70069689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6b8110d43d20db1dd17be79b05a909412d13eadd0e237abf6e919675b7e794`  
		Last Modified: Thu, 19 Dec 2019 08:48:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:3d4c31c77f2e83cc5a95318ffc9ed90067a20144cedb07e63c75da4edfd507d7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233479263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea615de602da4668c67fb0edd21d6812d5ff8ccc9315f37d80ad0d636b20312d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:22:03 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 07:23:43 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:23:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:23:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:23:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85320bb83837978f50bbd3baf84dea4b922e0b0218feb192ee0c7421258cc7`  
		Last Modified: Thu, 19 Dec 2019 07:33:33 GMT  
		Size: 50.8 MB (50848227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4350cb886547c239fa13e66d7ad666bcb99708c8af8d8b1971c4c41f8d28798a`  
		Last Modified: Thu, 19 Dec 2019 07:33:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:267c5f54b703e3f2fa98f5555ea89a385017be0639a39c51805fcc13ab0dd4a5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252806848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e787a2aab2a27535f377ff8b689b1fba26ae61da489d7c24f661af218b8beee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:39:38 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 09:41:03 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:41:07 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:41:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:41:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a31c3e5f5c6d7bdff677a1c2ca244f9ed373f0d4abe4742c97676c2dbde2523`  
		Last Modified: Thu, 19 Dec 2019 09:51:43 GMT  
		Size: 57.4 MB (57400446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9c35595f41a6221be1b6d19e20a50234f79967a968819173bcee35c6de7d1c`  
		Last Modified: Thu, 19 Dec 2019 09:51:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:eloquent-ros-core-bionic`

```console
$ docker pull ros@sha256:1f87fb45c3fb2206a2d0d263bff1d8a1ed98eff95082c8ee31d098a48bc42c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:67728aad1dbf9862a6a22053bffcef42ff9f8867094ec752b871aea638a02a24
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278588058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37edfccaf6b945622788fa59772f36ebecb0add5e67218c8da1635a2bf5c940`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:35:38 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:37:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:37:37 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 08:38:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:38:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:38:10 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:38:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 08:38:14 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 08:39:15 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 08:39:54 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:39:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 08:39:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:39:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e7fd1ee1a4284c30a83fa85e49be684ccb286a2acc2bef733184905ced2a0`  
		Last Modified: Thu, 19 Dec 2019 08:47:21 GMT  
		Size: 152.0 MB (151991699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1788b23e27b1dcb9bce2b1984a84b7d31947919c2163f9ade029e5332d53050a`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947606753c8584163c9d0773abc0362654dab6bbbc4b9bfba5a0cb4f2eefe5ff`  
		Last Modified: Thu, 19 Dec 2019 08:47:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc32392bda4b3149fab82011b47af99f0383238ba4b8512e9511a59fa420342`  
		Last Modified: Thu, 19 Dec 2019 08:47:45 GMT  
		Size: 28.4 MB (28396860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb28870019c0bdbda2621f8fb8eebc3e070b190e0081d00161bf4629228b6d66`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 457.2 KB (457226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd6f6f595fb36a05b0ee5a77cefa398fbe69ea89329d7b39e44d014b77ac06a`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3df7937065b6462f187e61fee4bd439fee17b170d67ac8133723ae0ad0bf8d`  
		Last Modified: Thu, 19 Dec 2019 08:47:37 GMT  
		Size: 105.6 KB (105619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc2771b910aaad0e851dedbe69f2541e1e824ed2aa8f38727952ede7ea89d7f`  
		Last Modified: Thu, 19 Dec 2019 08:48:40 GMT  
		Size: 70.1 MB (70069689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6b8110d43d20db1dd17be79b05a909412d13eadd0e237abf6e919675b7e794`  
		Last Modified: Thu, 19 Dec 2019 08:48:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:3d4c31c77f2e83cc5a95318ffc9ed90067a20144cedb07e63c75da4edfd507d7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233479263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea615de602da4668c67fb0edd21d6812d5ff8ccc9315f37d80ad0d636b20312d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:18:09 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 07:18:11 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 07:19:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:19:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:19:27 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:19:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 07:19:39 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 07:22:03 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 07:23:43 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:23:49 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 07:23:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:23:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455981857e9a410797e32fc0c529702018fc148c4f9d0c75e0761a06beca97f`  
		Last Modified: Thu, 19 Dec 2019 07:32:56 GMT  
		Size: 133.5 MB (133544797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c09f8172ff45416a62b29f2e242b4e1dfafebf97a0eb00a45e0987a8e903b57`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be10b58db720b2f091ed57e99a6b8792908ac7fb9a9dae6ea8349fffae5c68`  
		Last Modified: Thu, 19 Dec 2019 07:32:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df52c99895d650c13b1545ee01b48e2f64de5bbd927573c077cdf46a4db7e606`  
		Last Modified: Thu, 19 Dec 2019 07:32:26 GMT  
		Size: 25.4 MB (25369629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9644484caa92344ef25dc98de15e235a0e0f175c341d825f355e75a7f34ae`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 457.3 KB (457262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8449787a4d7a17919e9d9da626fbeb4ceb08944e85da16c1f2fc3e929852a`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f750c7df1c22431e41df26ec33d7c0ed7ce956e2676d7829c5fc8fb1aa5a33`  
		Last Modified: Thu, 19 Dec 2019 07:32:14 GMT  
		Size: 105.8 KB (105758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d85320bb83837978f50bbd3baf84dea4b922e0b0218feb192ee0c7421258cc7`  
		Last Modified: Thu, 19 Dec 2019 07:33:33 GMT  
		Size: 50.8 MB (50848227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4350cb886547c239fa13e66d7ad666bcb99708c8af8d8b1971c4c41f8d28798a`  
		Last Modified: Thu, 19 Dec 2019 07:33:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:267c5f54b703e3f2fa98f5555ea89a385017be0639a39c51805fcc13ab0dd4a5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252806848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e787a2aab2a27535f377ff8b689b1fba26ae61da489d7c24f661af218b8beee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:32:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:36:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:36:02 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 19 Dec 2019 09:37:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:37:02 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:37:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:37:23 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:37:29 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 19 Dec 2019 09:37:34 GMT
RUN pip3 install -U     argcomplete
# Thu, 19 Dec 2019 09:39:38 GMT
ENV ROS_DISTRO=eloquent
# Thu, 19 Dec 2019 09:41:03 GMT
RUN apt-get update && apt-get install -y     ros-eloquent-ros-core=0.8.4-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:41:07 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 19 Dec 2019 09:41:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:41:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ed8f55acfff2db1ab7fc05eaea5b50a6c3f2ff63e886257fcc39e267ca13e`  
		Last Modified: Thu, 19 Dec 2019 09:50:21 GMT  
		Size: 143.2 MB (143162770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70117b5d6348d6eb41e9752e5bca210f36e6c69d0a7eec87105e51fba6696e`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f1d24107e434232c8d8bfa81445e8130e3e7205bcb5c6b16fb0e07e2fa216f`  
		Last Modified: Thu, 19 Dec 2019 09:50:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c5a73503e8f3989553eea5fc6cf7c1a8b585289912466247d2225e61491144`  
		Last Modified: Thu, 19 Dec 2019 09:50:52 GMT  
		Size: 27.1 MB (27084179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fbd814641bb8462a721a29b7ed9ca4e9652633b42b310e5527bf2306a8be5f`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 457.3 KB (457269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c23284ec32c560e586cdc2f45375ab8f898ecf1111e856dfcd540b06c5f29ea`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d310b2c92d7854ea0c4a842a6bbce7672cc6b6512c4c51095c89b27d05f900`  
		Last Modified: Thu, 19 Dec 2019 09:50:43 GMT  
		Size: 105.8 KB (105750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a31c3e5f5c6d7bdff677a1c2ca244f9ed373f0d4abe4742c97676c2dbde2523`  
		Last Modified: Thu, 19 Dec 2019 09:51:43 GMT  
		Size: 57.4 MB (57400446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9c35595f41a6221be1b6d19e20a50234f79967a968819173bcee35c6de7d1c`  
		Last Modified: Thu, 19 Dec 2019 09:51:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic`

```console
$ docker pull ros@sha256:f0ba349754fbfb28ea273a202032a691f650348bb1cd96335b21d843046a74d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic` - linux; amd64

```console
$ docker pull ros@sha256:5bf8d73481a3be996cba1f449cdb9ee611c86ffb6098f46d9d1518ee8bb28fb8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385362973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2b2abbe31bd6239f97d00b57cb7491635d0ccb4a6b4b67824278ad80fef2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:16:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab15a38df195254a32dddf96ea9f512cf642931e5b6473721f49382f664eb5d8`  
		Last Modified: Thu, 19 Dec 2019 08:41:38 GMT  
		Size: 85.5 MB (85517553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:883106104357072e4011916e99987243b724d24ef59237c780d365dc3b9d7c9b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336647680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46c93cd10743885e0475a762078bed4e9d0b46679b0faf540c74c4a3de7dfc5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c614530517115569e9ae3f0044d6a421ebbd13ac383f336764f90dd7b4a53f3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350416724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e990888d3b78dd7adb0ad00f1e21db0d501a066cbb1d53c31ccd133119d6c17f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:12:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c43c9a069a6b32b2f9d9a0f2a7d2440dc58dd7dead223863bd4df11bcc96d`  
		Last Modified: Thu, 19 Dec 2019 09:43:29 GMT  
		Size: 77.8 MB (77818771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-perception`

```console
$ docker pull ros@sha256:6fecb1bfc3a6c322b4750ce4561e8f08ebb68ff6a2176a9fb99e5b15652c2c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:95883a5ecc776443c92e9a967e912ae5117d27fd171d14f0bc8b087dd873951e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.8 MB (725796754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39560f64d26d10e7f497fb84d581e4a9deaf8b3c0309bbdbfa125128800c2781`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:16:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:04 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab15a38df195254a32dddf96ea9f512cf642931e5b6473721f49382f664eb5d8`  
		Last Modified: Thu, 19 Dec 2019 08:41:38 GMT  
		Size: 85.5 MB (85517553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb543e1b061dcd491604c61f6d362f584edd2503b4c30c6e8119c2d0ee56c6d`  
		Last Modified: Thu, 19 Dec 2019 08:43:22 GMT  
		Size: 340.4 MB (340433781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:aac866977751e6059fc4082a1f0317ba50912335cc28dc82fa7ff8d4be03df4b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617144381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8d4e10cc6bba20a5b88895cf1eabf9a6820ccb359e97002838386368d67d56`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:58:40 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdbee25f536f2b6ca69e44872a3ff85213ae4c6817590438d4fbaace6b630c2`  
		Last Modified: Thu, 19 Dec 2019 07:28:23 GMT  
		Size: 280.5 MB (280496701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ada212b675755acd9e4176e7041acfe6e02b2d743ce8ebd15909ce30bd6be38b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.4 MB (641376706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e088c57dc613506178895fbc48f713fb96d24e422ef88567be51875be88bf27f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:12:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:17:54 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c43c9a069a6b32b2f9d9a0f2a7d2440dc58dd7dead223863bd4df11bcc96d`  
		Last Modified: Thu, 19 Dec 2019 09:43:29 GMT  
		Size: 77.8 MB (77818771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60445cdc0770b8cca74a1a32e21579e1542d44f6885a09a1e3b6e494177aa3b6`  
		Last Modified: Thu, 19 Dec 2019 09:45:47 GMT  
		Size: 291.0 MB (290959982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-perception-xenial`

```console
$ docker pull ros@sha256:6fecb1bfc3a6c322b4750ce4561e8f08ebb68ff6a2176a9fb99e5b15652c2c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-perception-xenial` - linux; amd64

```console
$ docker pull ros@sha256:95883a5ecc776443c92e9a967e912ae5117d27fd171d14f0bc8b087dd873951e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.8 MB (725796754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39560f64d26d10e7f497fb84d581e4a9deaf8b3c0309bbdbfa125128800c2781`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:16:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:04 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab15a38df195254a32dddf96ea9f512cf642931e5b6473721f49382f664eb5d8`  
		Last Modified: Thu, 19 Dec 2019 08:41:38 GMT  
		Size: 85.5 MB (85517553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb543e1b061dcd491604c61f6d362f584edd2503b4c30c6e8119c2d0ee56c6d`  
		Last Modified: Thu, 19 Dec 2019 08:43:22 GMT  
		Size: 340.4 MB (340433781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-perception-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:aac866977751e6059fc4082a1f0317ba50912335cc28dc82fa7ff8d4be03df4b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.1 MB (617144381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8d4e10cc6bba20a5b88895cf1eabf9a6820ccb359e97002838386368d67d56`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:58:40 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdbee25f536f2b6ca69e44872a3ff85213ae4c6817590438d4fbaace6b630c2`  
		Last Modified: Thu, 19 Dec 2019 07:28:23 GMT  
		Size: 280.5 MB (280496701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-perception-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ada212b675755acd9e4176e7041acfe6e02b2d743ce8ebd15909ce30bd6be38b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.4 MB (641376706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e088c57dc613506178895fbc48f713fb96d24e422ef88567be51875be88bf27f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:12:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:17:54 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c43c9a069a6b32b2f9d9a0f2a7d2440dc58dd7dead223863bd4df11bcc96d`  
		Last Modified: Thu, 19 Dec 2019 09:43:29 GMT  
		Size: 77.8 MB (77818771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60445cdc0770b8cca74a1a32e21579e1542d44f6885a09a1e3b6e494177aa3b6`  
		Last Modified: Thu, 19 Dec 2019 09:45:47 GMT  
		Size: 291.0 MB (290959982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-robot`

```console
$ docker pull ros@sha256:6ad627bb928e56716becae0578904a8751e94bbb0efc8163865bb82da2e1b3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:2926d19b34259537d64139b275af4e86d21d4819400c1632ec56e783316f42d4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.0 MB (489003753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e226e20021f502c9fbf6d1d411275edad4e8a7953b10e0d7abba1782ec50ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:16:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:18:34 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab15a38df195254a32dddf96ea9f512cf642931e5b6473721f49382f664eb5d8`  
		Last Modified: Thu, 19 Dec 2019 08:41:38 GMT  
		Size: 85.5 MB (85517553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b631b88ae33fd217906a014d6b63e43fdaa9b7483adfb60dd230cc41d2d410d1`  
		Last Modified: Thu, 19 Dec 2019 08:42:06 GMT  
		Size: 103.6 MB (103640780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:44e1c8272f83541e1f076e81a0bdb1b8f45511dfa244e51beed58a63e9fe08b4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.7 MB (426694611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1728e38a27da711c05cc852e98fda6d3eab861d10e5020038277670771361c0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:51:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a249b2dbb96cdf8717b8539b9dc7b5ab774ef36aa1398f27a7ad1e62df8f303`  
		Last Modified: Thu, 19 Dec 2019 07:26:55 GMT  
		Size: 90.0 MB (90046931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b50d810ca9c840a337f1df1d831c76c94c9c8674080ce88fd265b3697b8c639c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444347838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6d945d776011b6ab0c29d1add625444c67e856746d63d2c4196d07fcf200f2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:12:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:14:00 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c43c9a069a6b32b2f9d9a0f2a7d2440dc58dd7dead223863bd4df11bcc96d`  
		Last Modified: Thu, 19 Dec 2019 09:43:29 GMT  
		Size: 77.8 MB (77818771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e97856f1c4c523d01251c98961cf6abd799d3ba1603b9ecde888d7cf194cfae`  
		Last Modified: Thu, 19 Dec 2019 09:44:06 GMT  
		Size: 93.9 MB (93931114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-robot-xenial`

```console
$ docker pull ros@sha256:6ad627bb928e56716becae0578904a8751e94bbb0efc8163865bb82da2e1b3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot-xenial` - linux; amd64

```console
$ docker pull ros@sha256:2926d19b34259537d64139b275af4e86d21d4819400c1632ec56e783316f42d4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.0 MB (489003753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e226e20021f502c9fbf6d1d411275edad4e8a7953b10e0d7abba1782ec50ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:16:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:18:34 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab15a38df195254a32dddf96ea9f512cf642931e5b6473721f49382f664eb5d8`  
		Last Modified: Thu, 19 Dec 2019 08:41:38 GMT  
		Size: 85.5 MB (85517553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b631b88ae33fd217906a014d6b63e43fdaa9b7483adfb60dd230cc41d2d410d1`  
		Last Modified: Thu, 19 Dec 2019 08:42:06 GMT  
		Size: 103.6 MB (103640780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:44e1c8272f83541e1f076e81a0bdb1b8f45511dfa244e51beed58a63e9fe08b4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.7 MB (426694611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1728e38a27da711c05cc852e98fda6d3eab861d10e5020038277670771361c0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:51:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a249b2dbb96cdf8717b8539b9dc7b5ab774ef36aa1398f27a7ad1e62df8f303`  
		Last Modified: Thu, 19 Dec 2019 07:26:55 GMT  
		Size: 90.0 MB (90046931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b50d810ca9c840a337f1df1d831c76c94c9c8674080ce88fd265b3697b8c639c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444347838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6d945d776011b6ab0c29d1add625444c67e856746d63d2c4196d07fcf200f2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:12:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:14:00 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c43c9a069a6b32b2f9d9a0f2a7d2440dc58dd7dead223863bd4df11bcc96d`  
		Last Modified: Thu, 19 Dec 2019 09:43:29 GMT  
		Size: 77.8 MB (77818771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e97856f1c4c523d01251c98961cf6abd799d3ba1603b9ecde888d7cf194cfae`  
		Last Modified: Thu, 19 Dec 2019 09:44:06 GMT  
		Size: 93.9 MB (93931114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-ros-base`

```console
$ docker pull ros@sha256:f0ba349754fbfb28ea273a202032a691f650348bb1cd96335b21d843046a74d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:5bf8d73481a3be996cba1f449cdb9ee611c86ffb6098f46d9d1518ee8bb28fb8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385362973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2b2abbe31bd6239f97d00b57cb7491635d0ccb4a6b4b67824278ad80fef2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:16:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab15a38df195254a32dddf96ea9f512cf642931e5b6473721f49382f664eb5d8`  
		Last Modified: Thu, 19 Dec 2019 08:41:38 GMT  
		Size: 85.5 MB (85517553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:883106104357072e4011916e99987243b724d24ef59237c780d365dc3b9d7c9b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336647680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46c93cd10743885e0475a762078bed4e9d0b46679b0faf540c74c4a3de7dfc5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c614530517115569e9ae3f0044d6a421ebbd13ac383f336764f90dd7b4a53f3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350416724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e990888d3b78dd7adb0ad00f1e21db0d501a066cbb1d53c31ccd133119d6c17f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:12:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c43c9a069a6b32b2f9d9a0f2a7d2440dc58dd7dead223863bd4df11bcc96d`  
		Last Modified: Thu, 19 Dec 2019 09:43:29 GMT  
		Size: 77.8 MB (77818771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-ros-base-xenial`

```console
$ docker pull ros@sha256:f0ba349754fbfb28ea273a202032a691f650348bb1cd96335b21d843046a74d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-base-xenial` - linux; amd64

```console
$ docker pull ros@sha256:5bf8d73481a3be996cba1f449cdb9ee611c86ffb6098f46d9d1518ee8bb28fb8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385362973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2b2abbe31bd6239f97d00b57cb7491635d0ccb4a6b4b67824278ad80fef2c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:16:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab15a38df195254a32dddf96ea9f512cf642931e5b6473721f49382f664eb5d8`  
		Last Modified: Thu, 19 Dec 2019 08:41:38 GMT  
		Size: 85.5 MB (85517553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-base-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:883106104357072e4011916e99987243b724d24ef59237c780d365dc3b9d7c9b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336647680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46c93cd10743885e0475a762078bed4e9d0b46679b0faf540c74c4a3de7dfc5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 06:48:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f93dcb7dc9e66913c87f9984e99144e1f72b2d1c4e5ecaeb35a1b7c944cb1ee`  
		Last Modified: Thu, 19 Dec 2019 07:26:14 GMT  
		Size: 76.3 MB (76327967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-base-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c614530517115569e9ae3f0044d6a421ebbd13ac383f336764f90dd7b4a53f3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350416724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e990888d3b78dd7adb0ad00f1e21db0d501a066cbb1d53c31ccd133119d6c17f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:12:30 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19c43c9a069a6b32b2f9d9a0f2a7d2440dc58dd7dead223863bd4df11bcc96d`  
		Last Modified: Thu, 19 Dec 2019 09:43:29 GMT  
		Size: 77.8 MB (77818771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-ros-core`

```console
$ docker pull ros@sha256:b0b55770569b20906142d3afd8d4836742d26ffac5a60a8c788007f852fac435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:9841c829dd55ce7e95428c2ea2cc730c08f180fd64709b4b49b0fff7b95f164b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299845420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657425cfebe289a34210765c4239aa697ecdc3bad74c09b104f954d0286ed3b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:4eec0c04f790848cf033a94bb984e6cb932116c7a515263e2b4a7229809b3e04
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260319713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ba708c70ceac585604982b90b2d5fa3f01978acf807763ef5f1a7537f1f0f1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:42d9633ec599c43d9ce8d7bb8e54b0fe1e8d486b5d2a96c1a660d636963197f6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272597953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fddd802b449fc510d1bd35062e6dcf9c2ec1a1b5a8ba32fc3cbd709f28831d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-ros-core-xenial`

```console
$ docker pull ros@sha256:b0b55770569b20906142d3afd8d4836742d26ffac5a60a8c788007f852fac435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core-xenial` - linux; amd64

```console
$ docker pull ros@sha256:9841c829dd55ce7e95428c2ea2cc730c08f180fd64709b4b49b0fff7b95f164b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299845420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657425cfebe289a34210765c4239aa697ecdc3bad74c09b104f954d0286ed3b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:12:20 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:12:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:12:22 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:13:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:13:18 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:13:18 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 08:15:12 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:15:13 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:15:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:15:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457aec0e6396b59c9e392c1756f39b2b16eb4ec642ee9a245fa6be156e84fdcd`  
		Last Modified: Thu, 19 Dec 2019 08:40:28 GMT  
		Size: 6.9 MB (6938120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d003c6fb07330daa4bab99fc349a9e9c1ee91e901bdf12f937f4c57ce8abe53`  
		Last Modified: Thu, 19 Dec 2019 08:40:26 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26c6e39341421afd15b05b54468ad0588a45bb8baf5b09aa423d645cd9d2bd`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc96488ffb5e99fa546e5907bc1dace89168ad9711f3908be178fe24c491eaf9`  
		Last Modified: Thu, 19 Dec 2019 08:40:41 GMT  
		Size: 54.8 MB (54776706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc49700f647fe9094f423ff327d7eda8f4eaf317dde051ee8908c3138022a183`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529abb518cdf8d1e75141dca5c706d8a5e89944cac45b886fe844805d35ba5a`  
		Last Modified: Thu, 19 Dec 2019 08:41:10 GMT  
		Size: 193.5 MB (193541433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b27f5c340563860d4de224aea7cbaa86d27ef8124169500eded483af45ba0`  
		Last Modified: Thu, 19 Dec 2019 08:40:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:4eec0c04f790848cf033a94bb984e6cb932116c7a515263e2b4a7229809b3e04
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260319713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ba708c70ceac585604982b90b2d5fa3f01978acf807763ef5f1a7537f1f0f1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:13:48 GMT
ADD file:1eb3c4071d32b0a8303ba31b94ccbe4e41eeb6f7bd63e421422b6ec57189510f in / 
# Thu, 19 Dec 2019 06:13:58 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:14:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:14:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:14:16 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:41:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:41:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:41:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 06:42:52 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:42:55 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 06:42:56 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 06:43:17 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 06:43:20 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 06:46:06 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:46:09 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 06:46:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 06:46:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c9254c1ab1fb38e9ae02953d2c8a3049d31856bab7053e388f23cef210597bbe`  
		Last Modified: Mon, 16 Dec 2019 15:43:26 GMT  
		Size: 38.8 MB (38831502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8a4af221588d688f657274b15fea720573656acf9ece94a8510b1488318419`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaefd48a3cde2542d0443d4731a3b7074e41344bb62c8327297c61293398164`  
		Last Modified: Thu, 19 Dec 2019 06:16:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d3331f5ad1f67a66c9fa286fc830645fa2e844e3e2cc1d60522c436fd72205`  
		Last Modified: Thu, 19 Dec 2019 06:16:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2b81ce07a861e3a76db0d541986a49a354ef54454ff21d24bf645e67fde13a`  
		Last Modified: Thu, 19 Dec 2019 07:24:52 GMT  
		Size: 5.7 MB (5702275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07255d05e2ac7c0f25c2d22f1e93030a378e873c66223e96f2a65d09258f6d76`  
		Last Modified: Thu, 19 Dec 2019 07:24:48 GMT  
		Size: 13.1 KB (13104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0768a4e7c85d399dca304c025c827c978b1bcbb05e169d5e80ea777b76c8bdb1`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800347818d646ad2df8d6e1a34ac1dbf389baac9807e9431b22bfe71278380c8`  
		Last Modified: Thu, 19 Dec 2019 07:25:08 GMT  
		Size: 50.3 MB (50348758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b767d331b13e63935e560445c037945b0c0aa0c74a025bd89c2755f8ed3142`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 450.8 KB (450788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aeee38c540e19a6a1d2fe06d366d70fbdf94076ff4975fb8e805951ab205a0`  
		Last Modified: Thu, 19 Dec 2019 07:25:44 GMT  
		Size: 165.0 MB (164971334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b050311edafb3addc3b75044375077583f5c4d2be8da079ccb578ca6ca150`  
		Last Modified: Thu, 19 Dec 2019 07:24:45 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:42d9633ec599c43d9ce8d7bb8e54b0fe1e8d486b5d2a96c1a660d636963197f6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272597953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fddd802b449fc510d1bd35062e6dcf9c2ec1a1b5a8ba32fc3cbd709f28831d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:54:56 GMT
ADD file:ef40ad352b3111bab843b916e802c7cb18aeccc96a65fe9a7a5330572431e7c7 in / 
# Thu, 19 Dec 2019 03:54:59 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 03:55:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:55:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:55:11 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:07:10 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:07:13 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:07:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:08:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:08:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:08:45 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:08:46 GMT
ENV ROS_DISTRO=kinetic
# Thu, 19 Dec 2019 09:10:38 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:10:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:10:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:10:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8d9a83fac1745f67aed1e924445fc9a89cd885fe70d0e1e335cbe4791f490b5`  
		Last Modified: Thu, 19 Dec 2019 03:57:28 GMT  
		Size: 39.9 MB (39875399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9cc76ef947c73adaf3c9e2dd2f8da166e815b37d431b9baae7aebe84096fe`  
		Last Modified: Thu, 19 Dec 2019 03:57:19 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d286195ea15592986e2820cc7366deda87cc2802b6cfe82a6f5388aceb4a4`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120fa5dd162f3d2fa3a1452a4d909074c6ffcba06016d39e5781581ec1ec5f88`  
		Last Modified: Thu, 19 Dec 2019 03:57:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df16651e3000bf2b6ae3cc1a8de5b7bde1ca91f2aad31aeb231f24ccf0621c10`  
		Last Modified: Thu, 19 Dec 2019 09:42:09 GMT  
		Size: 6.0 MB (5959610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76792d633ca9466c8e705ff4072fc431f386601da8441f84320f135fa15f177`  
		Last Modified: Thu, 19 Dec 2019 09:42:07 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a02948fb7dd58f67c357b01591ed9a5340d4569b8af575f92538c569993d59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98ef3031817ddbe31b799a64b5e4bd9292394da1ca7e29cd7a6c004d15d8a1`  
		Last Modified: Thu, 19 Dec 2019 09:42:23 GMT  
		Size: 52.1 MB (52072413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6c9ea297fd5aadfda1a295cae5f39632d3547eab77874341a70adc4d25bd59`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 450.9 KB (450886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ce4c6453b3968056ea13fd280e8ce590d9140c330ccd73152d4a89fa919fd`  
		Last Modified: Thu, 19 Dec 2019 09:42:58 GMT  
		Size: 174.2 MB (174224631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d922cb7a8f5abf9067bfd287531cd8808086a55c8aa5d11e24fb2f2f52335930`  
		Last Modified: Thu, 19 Dec 2019 09:42:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:53622f114bb197d282d214d6174e19c243d5ee8d5c605cb5ee9aba301567ca1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:56b12ce9ab14a158b56336d7fbbf1de011d87cda514b0f32fd77827df42f8a8c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419392123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23b8327e0c6d9af7ce96796e4a0554d1710236fe9c1fc5e75247e424c0f254`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm variant v7

```console
$ docker pull ros@sha256:ccfe308c17a0e677ecc384052b23e469680d809e45f2aa635d45ffabf6da2a6c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372218761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d463c5c602806461c174727773f1f51c9e8cc6bf7e8ef9df0efcbf0eed86e211`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cc6647386c614121fb5a83d73135ec42dfd021d68232451d1cbf1b601de3cd9d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395850107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b1f1f4aeb2e8fc3b3d375fc521f707f54d81076199339adfba7ea9857aaf48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic`

```console
$ docker pull ros@sha256:53622f114bb197d282d214d6174e19c243d5ee8d5c605cb5ee9aba301567ca1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:56b12ce9ab14a158b56336d7fbbf1de011d87cda514b0f32fd77827df42f8a8c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419392123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23b8327e0c6d9af7ce96796e4a0554d1710236fe9c1fc5e75247e424c0f254`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:ccfe308c17a0e677ecc384052b23e469680d809e45f2aa635d45ffabf6da2a6c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372218761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d463c5c602806461c174727773f1f51c9e8cc6bf7e8ef9df0efcbf0eed86e211`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cc6647386c614121fb5a83d73135ec42dfd021d68232451d1cbf1b601de3cd9d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395850107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b1f1f4aeb2e8fc3b3d375fc521f707f54d81076199339adfba7ea9857aaf48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception`

```console
$ docker pull ros@sha256:d7c1843d0b06e9084394b9751ee36a5ef179022d3ea442c8ec008e1331e12cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:0f705f84af33fca62348d41d1b72ca0146093336c17f16be4215e3df8d7fa949
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.7 MB (768686804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed7b4d6cf1eff66c3f545520735f73bb983f2851219a786e0c20d133c1858d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:34:25 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b360f8dfc5add824e034fbb0aab4dbf1c9b908b29ee0c17dfd7844e38ac1835`  
		Last Modified: Thu, 19 Dec 2019 08:46:30 GMT  
		Size: 349.3 MB (349294681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:b8c5d12f1ed1dbd4e182384625be07ff72403fd1f0a96601ca4663be363ce29c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.6 MB (671552540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf0f9e1180fac3d0ad516dbb0c7531fac82d2c641b3e5159c7945892ca9df84`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:16:10 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1097a042946fdc9a0d74dba87323a695aa51dd3eaa42fd507652d51116d54c`  
		Last Modified: Thu, 19 Dec 2019 07:32:06 GMT  
		Size: 299.3 MB (299333779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:992707b40498c1aad649d19083e4ab7272ba72935e2fdeed9779a7978b7b7ab8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.8 MB (727757670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28648406a40d50ef51dc4ef4f738806b336354e670a13b4807e7fc2f4f71fedf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:29:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c920b091f73fda48cb91862cd02300c3a439478c33082ee77bb9520323a0b9`  
		Last Modified: Thu, 19 Dec 2019 09:49:36 GMT  
		Size: 331.9 MB (331907563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:d7c1843d0b06e9084394b9751ee36a5ef179022d3ea442c8ec008e1331e12cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:0f705f84af33fca62348d41d1b72ca0146093336c17f16be4215e3df8d7fa949
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.7 MB (768686804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed7b4d6cf1eff66c3f545520735f73bb983f2851219a786e0c20d133c1858d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:34:25 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b360f8dfc5add824e034fbb0aab4dbf1c9b908b29ee0c17dfd7844e38ac1835`  
		Last Modified: Thu, 19 Dec 2019 08:46:30 GMT  
		Size: 349.3 MB (349294681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:b8c5d12f1ed1dbd4e182384625be07ff72403fd1f0a96601ca4663be363ce29c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.6 MB (671552540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf0f9e1180fac3d0ad516dbb0c7531fac82d2c641b3e5159c7945892ca9df84`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:16:10 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1097a042946fdc9a0d74dba87323a695aa51dd3eaa42fd507652d51116d54c`  
		Last Modified: Thu, 19 Dec 2019 07:32:06 GMT  
		Size: 299.3 MB (299333779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:992707b40498c1aad649d19083e4ab7272ba72935e2fdeed9779a7978b7b7ab8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.8 MB (727757670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28648406a40d50ef51dc4ef4f738806b336354e670a13b4807e7fc2f4f71fedf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:29:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c920b091f73fda48cb91862cd02300c3a439478c33082ee77bb9520323a0b9`  
		Last Modified: Thu, 19 Dec 2019 09:49:36 GMT  
		Size: 331.9 MB (331907563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-stretch`

```console
$ docker pull ros@sha256:f479c0b9b2cf1db20fcf913425f9aaf75b65c30866207a70673852e5757acb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-perception-stretch` - linux; amd64

```console
$ docker pull ros@sha256:4c4d41289c5c477347591ae5f7e982621e5472529c829ff8c1efa81ea41aec0b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.3 MB (876331066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603424d168bbf73c728d468785aad51e2e294b582bb394a973f47ed8379b8718`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:26:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:26:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 08:26:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 08:27:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:27:02 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:27:03 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 08:27:21 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 08:27:21 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 08:29:05 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:29:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 08:29:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 08:29:07 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:30:14 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:33:51 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cf93dae3672c4b23e304be8bfbd86a1a70e192920d9bb7d980774a433b7123`  
		Last Modified: Sat, 28 Dec 2019 08:34:45 GMT  
		Size: 10.5 MB (10476716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4d94fcfba96b58c2a901f6286ca7d1ce99dacfe09968fc037d5553f2025e8a`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7ebb2626a2bc1ed27e07d7ca29f5a02c7cfb09f84608d38f9c99b1b798ced`  
		Last Modified: Sat, 28 Dec 2019 08:34:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc08219e7fdb9a27aa4c99a6f1d467eab7640d963871a1400ebfdaae3af68c57`  
		Last Modified: Sat, 28 Dec 2019 08:35:00 GMT  
		Size: 64.8 MB (64771041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191195f75e3d8a24ce1e680579fd09913504e418871b9b7ec1e38aaa061fdd1`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 451.5 KB (451468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9fd3f2a56a2d531756ee769940fada1e88517a593b70c3e21e959874a7bc78`  
		Last Modified: Sat, 28 Dec 2019 08:35:41 GMT  
		Size: 270.4 MB (270404151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0106c5e798490c33945ce9ebe7647215eb890cf55e081b770471e498436353`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2db8c7023a66d21e38358720aab69dc412fb39a5366737c69bc7bbb76c53ba1`  
		Last Modified: Sat, 28 Dec 2019 08:36:17 GMT  
		Size: 108.5 MB (108473946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e00711f861b9c055a4a53b6b4cd5db34f3e2dd6f6919595b5630854da331048`  
		Last Modified: Sat, 28 Dec 2019 08:38:37 GMT  
		Size: 376.4 MB (376371186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a37ab6bf0820d77cc72df9028681ab1de373743fe259b5f63fa0428e5315040f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **794.1 MB (794089994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed189ff040a6be63c69243fa04762c1f8bfc155ee47616b03b5cc305ca617c98`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:34:23 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:34:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 18:34:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 18:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:35:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 18:35:41 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 18:36:03 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 18:36:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 18:38:50 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:39:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 18:39:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 18:39:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:40:15 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:47:10 GMT
RUN apt-get update && apt-get install -y     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facfbd1fae886a379926b7add3095adbf575d32e87e67282e12488332f12f747`  
		Last Modified: Sat, 28 Dec 2019 18:48:28 GMT  
		Size: 9.8 MB (9774604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a6b709bed6b18e5ba839847d0f3e3a5a4e53a163b69ea7858c561fdc7f1e3a`  
		Last Modified: Sat, 28 Dec 2019 18:48:25 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af9a8179e95515f1f6e62a300ca75906566906d949c7403c9f61b8511afc033`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23b6ea616f3e8e138683f48ca757b84bc23de865b250839eba047a141cc6721`  
		Last Modified: Sat, 28 Dec 2019 18:48:46 GMT  
		Size: 62.1 MB (62085764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101b4656b4d26f6236d97a86a31ae20834b113b525d2830521853323cfb6369`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 451.5 KB (451514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e52b33734a366437f8b9e807980e3273684eeef72d2fd1822dc4ea7ae5638`  
		Last Modified: Sat, 28 Dec 2019 18:49:32 GMT  
		Size: 224.6 MB (224573326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de7b9c0321a0098bd333b1ceb564c2a4389249dc4f9e3f45da7c389198a1ba`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033d8666e6f7cc5f88f89356fb0b79d8bcb42f576c433b924571484da93bdc43`  
		Last Modified: Sat, 28 Dec 2019 18:50:04 GMT  
		Size: 103.0 MB (102961244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd8023d447d2b366f450e3089908dbf1ee5a2f68483463b3eec7364566a1771`  
		Last Modified: Sat, 28 Dec 2019 18:52:10 GMT  
		Size: 351.1 MB (351075248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot`

```console
$ docker pull ros@sha256:34e8a268f932479ff82983d48a84ed32ef0fa181bbe97fbaff1896c69a413a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:14c3aab1743e7dbcc35c41e2ec41504f911b2a37a2fc9b9a9e4897429416def0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.2 MB (457217092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4ca50e6fb9f368b452da83c51a05844ca0bbed49ed6063880c4d72b8523d44`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:28:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9543e560cfd8b575c8ad881be11cfe4c03c9677d7cd39fd2e42be6f9fbad2ea0`  
		Last Modified: Thu, 19 Dec 2019 08:44:55 GMT  
		Size: 37.8 MB (37824969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:d66ff9a7c66797929a6aad4e564eec2d6f9417ca65592667e3f2eba17d4609e1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 MB (405650899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308fba543127eb40e0244d1ca461909e22d9b940b1de3c65749bcd3b623a407a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:11:30 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05379b30cbec8b17120c9c7a5d56e25ccf9d27fa548a66668df3c3da7e8d95c0`  
		Last Modified: Thu, 19 Dec 2019 07:30:28 GMT  
		Size: 33.4 MB (33432138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28e71d4a6e26626f23aa7c36fd39da30be80ffcfd96d1185e1d1920bc51ca217
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.4 MB (431449154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f9eb3f60da6113b36827731e999576f7ed1b6525d2800646d8ee16933cb1fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:25:07 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c583c24554587ad09f85b4c34b258384a9e73da8f6b7ac5f5e653c79325b3b`  
		Last Modified: Thu, 19 Dec 2019 09:47:50 GMT  
		Size: 35.6 MB (35599047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:34e8a268f932479ff82983d48a84ed32ef0fa181bbe97fbaff1896c69a413a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:14c3aab1743e7dbcc35c41e2ec41504f911b2a37a2fc9b9a9e4897429416def0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.2 MB (457217092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4ca50e6fb9f368b452da83c51a05844ca0bbed49ed6063880c4d72b8523d44`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:28:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9543e560cfd8b575c8ad881be11cfe4c03c9677d7cd39fd2e42be6f9fbad2ea0`  
		Last Modified: Thu, 19 Dec 2019 08:44:55 GMT  
		Size: 37.8 MB (37824969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:d66ff9a7c66797929a6aad4e564eec2d6f9417ca65592667e3f2eba17d4609e1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.7 MB (405650899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308fba543127eb40e0244d1ca461909e22d9b940b1de3c65749bcd3b623a407a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:11:30 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05379b30cbec8b17120c9c7a5d56e25ccf9d27fa548a66668df3c3da7e8d95c0`  
		Last Modified: Thu, 19 Dec 2019 07:30:28 GMT  
		Size: 33.4 MB (33432138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28e71d4a6e26626f23aa7c36fd39da30be80ffcfd96d1185e1d1920bc51ca217
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.4 MB (431449154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f9eb3f60da6113b36827731e999576f7ed1b6525d2800646d8ee16933cb1fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:25:07 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c583c24554587ad09f85b4c34b258384a9e73da8f6b7ac5f5e653c79325b3b`  
		Last Modified: Thu, 19 Dec 2019 09:47:50 GMT  
		Size: 35.6 MB (35599047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-stretch`

```console
$ docker pull ros@sha256:6c102c9db9a12ac05ca4ecbf00008dbb48fa6cfe74ce7e1f1b010d511c9074bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-robot-stretch` - linux; amd64

```console
$ docker pull ros@sha256:bfe8b818535c76586b58ecc7483bdff42271664cbbebf0565bebdd546df7f060
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.3 MB (555257867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8bd493dbb7aa0c510c6b607557211be54160da982b18746d8ddeddf67a0ba9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:26:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:26:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 08:26:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 08:27:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:27:02 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:27:03 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 08:27:21 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 08:27:21 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 08:29:05 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:29:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 08:29:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 08:29:07 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:30:14 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:31:13 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cf93dae3672c4b23e304be8bfbd86a1a70e192920d9bb7d980774a433b7123`  
		Last Modified: Sat, 28 Dec 2019 08:34:45 GMT  
		Size: 10.5 MB (10476716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4d94fcfba96b58c2a901f6286ca7d1ce99dacfe09968fc037d5553f2025e8a`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7ebb2626a2bc1ed27e07d7ca29f5a02c7cfb09f84608d38f9c99b1b798ced`  
		Last Modified: Sat, 28 Dec 2019 08:34:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc08219e7fdb9a27aa4c99a6f1d467eab7640d963871a1400ebfdaae3af68c57`  
		Last Modified: Sat, 28 Dec 2019 08:35:00 GMT  
		Size: 64.8 MB (64771041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191195f75e3d8a24ce1e680579fd09913504e418871b9b7ec1e38aaa061fdd1`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 451.5 KB (451468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9fd3f2a56a2d531756ee769940fada1e88517a593b70c3e21e959874a7bc78`  
		Last Modified: Sat, 28 Dec 2019 08:35:41 GMT  
		Size: 270.4 MB (270404151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0106c5e798490c33945ce9ebe7647215eb890cf55e081b770471e498436353`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2db8c7023a66d21e38358720aab69dc412fb39a5366737c69bc7bbb76c53ba1`  
		Last Modified: Sat, 28 Dec 2019 08:36:17 GMT  
		Size: 108.5 MB (108473946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e16b33263adec4f1c03667573f6c3b75bb569d408fcae9b0bae116cad8f387a`  
		Last Modified: Sat, 28 Dec 2019 08:36:44 GMT  
		Size: 55.3 MB (55297987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:44b25396f459f6ad6d285ad9d4baf6e8f8eadc3038876b7bdbdf977873a29a5f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.6 MB (495596210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892f7831c3059d2c225b6ded4253b3541828d9b2cc3c195d6bfd261ae98578ee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:34:23 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:34:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 18:34:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 18:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:35:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 18:35:41 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 18:36:03 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 18:36:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 18:38:50 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:39:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 18:39:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 18:39:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:40:15 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:41:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facfbd1fae886a379926b7add3095adbf575d32e87e67282e12488332f12f747`  
		Last Modified: Sat, 28 Dec 2019 18:48:28 GMT  
		Size: 9.8 MB (9774604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a6b709bed6b18e5ba839847d0f3e3a5a4e53a163b69ea7858c561fdc7f1e3a`  
		Last Modified: Sat, 28 Dec 2019 18:48:25 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af9a8179e95515f1f6e62a300ca75906566906d949c7403c9f61b8511afc033`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23b6ea616f3e8e138683f48ca757b84bc23de865b250839eba047a141cc6721`  
		Last Modified: Sat, 28 Dec 2019 18:48:46 GMT  
		Size: 62.1 MB (62085764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101b4656b4d26f6236d97a86a31ae20834b113b525d2830521853323cfb6369`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 451.5 KB (451514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e52b33734a366437f8b9e807980e3273684eeef72d2fd1822dc4ea7ae5638`  
		Last Modified: Sat, 28 Dec 2019 18:49:32 GMT  
		Size: 224.6 MB (224573326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de7b9c0321a0098bd333b1ceb564c2a4389249dc4f9e3f45da7c389198a1ba`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033d8666e6f7cc5f88f89356fb0b79d8bcb42f576c433b924571484da93bdc43`  
		Last Modified: Sat, 28 Dec 2019 18:50:04 GMT  
		Size: 103.0 MB (102961244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19be1af64328e4305c7048a43c021ab70b6023255e1fef0eb01a7cd97128eec9`  
		Last Modified: Sat, 28 Dec 2019 18:50:24 GMT  
		Size: 52.6 MB (52581464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:53622f114bb197d282d214d6174e19c243d5ee8d5c605cb5ee9aba301567ca1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:56b12ce9ab14a158b56336d7fbbf1de011d87cda514b0f32fd77827df42f8a8c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419392123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23b8327e0c6d9af7ce96796e4a0554d1710236fe9c1fc5e75247e424c0f254`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:ccfe308c17a0e677ecc384052b23e469680d809e45f2aa635d45ffabf6da2a6c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372218761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d463c5c602806461c174727773f1f51c9e8cc6bf7e8ef9df0efcbf0eed86e211`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cc6647386c614121fb5a83d73135ec42dfd021d68232451d1cbf1b601de3cd9d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395850107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b1f1f4aeb2e8fc3b3d375fc521f707f54d81076199339adfba7ea9857aaf48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:53622f114bb197d282d214d6174e19c243d5ee8d5c605cb5ee9aba301567ca1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:56b12ce9ab14a158b56336d7fbbf1de011d87cda514b0f32fd77827df42f8a8c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419392123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23b8327e0c6d9af7ce96796e4a0554d1710236fe9c1fc5e75247e424c0f254`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 08:27:43 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f4332440558d0adb9cfebba043639b1cf26d2a5b0741c27295cd15f4bbcd27`  
		Last Modified: Thu, 19 Dec 2019 08:44:40 GMT  
		Size: 68.3 MB (68334967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:ccfe308c17a0e677ecc384052b23e469680d809e45f2aa635d45ffabf6da2a6c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372218761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d463c5c602806461c174727773f1f51c9e8cc6bf7e8ef9df0efcbf0eed86e211`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 07:09:54 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d810dbfbec2f7a9860a8d74cf4595e10a606f9c6c5b36b1b5fff09e4498bce2`  
		Last Modified: Thu, 19 Dec 2019 07:30:05 GMT  
		Size: 60.3 MB (60258526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cc6647386c614121fb5a83d73135ec42dfd021d68232451d1cbf1b601de3cd9d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395850107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b1f1f4aeb2e8fc3b3d375fc521f707f54d81076199339adfba7ea9857aaf48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
# Thu, 19 Dec 2019 09:23:59 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd098fc5b3755d3c0b1a3a95eff7e7379b198075d3da50b35407d6988d8cf004`  
		Last Modified: Thu, 19 Dec 2019 09:47:30 GMT  
		Size: 62.8 MB (62841501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-stretch`

```console
$ docker pull ros@sha256:5ea106fc953880e151e8b2c8afc1fb2eb9f1e8c92e419161a4f1627f67e17464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-stretch` - linux; amd64

```console
$ docker pull ros@sha256:b03e9701a180b9ce5d6df50bc0a23b7a3dfd2fa592c7f1444343790880ec7fd8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (499959880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cc38ae8baaac327b75ffd4fd8d36c8f4f57546d4169209651465da229f1657`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:26:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:26:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 08:26:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 08:27:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:27:02 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:27:03 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 08:27:21 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 08:27:21 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 08:29:05 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:29:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 08:29:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 08:29:07 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:30:14 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cf93dae3672c4b23e304be8bfbd86a1a70e192920d9bb7d980774a433b7123`  
		Last Modified: Sat, 28 Dec 2019 08:34:45 GMT  
		Size: 10.5 MB (10476716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4d94fcfba96b58c2a901f6286ca7d1ce99dacfe09968fc037d5553f2025e8a`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7ebb2626a2bc1ed27e07d7ca29f5a02c7cfb09f84608d38f9c99b1b798ced`  
		Last Modified: Sat, 28 Dec 2019 08:34:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc08219e7fdb9a27aa4c99a6f1d467eab7640d963871a1400ebfdaae3af68c57`  
		Last Modified: Sat, 28 Dec 2019 08:35:00 GMT  
		Size: 64.8 MB (64771041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191195f75e3d8a24ce1e680579fd09913504e418871b9b7ec1e38aaa061fdd1`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 451.5 KB (451468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9fd3f2a56a2d531756ee769940fada1e88517a593b70c3e21e959874a7bc78`  
		Last Modified: Sat, 28 Dec 2019 08:35:41 GMT  
		Size: 270.4 MB (270404151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0106c5e798490c33945ce9ebe7647215eb890cf55e081b770471e498436353`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2db8c7023a66d21e38358720aab69dc412fb39a5366737c69bc7bbb76c53ba1`  
		Last Modified: Sat, 28 Dec 2019 08:36:17 GMT  
		Size: 108.5 MB (108473946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bda4c8f3ddfb11e74a3e7a6e33f13b388b7b667c4832e20f0e3e0b11f486dbba
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.0 MB (443014746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95461410a52add4d5ba4d8315b9518d7ed40ff65a2044a57092a0b99fcbd92c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:34:23 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:34:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 18:34:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 18:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:35:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 18:35:41 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 18:36:03 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 18:36:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 18:38:50 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:39:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 18:39:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 18:39:02 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:40:15 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facfbd1fae886a379926b7add3095adbf575d32e87e67282e12488332f12f747`  
		Last Modified: Sat, 28 Dec 2019 18:48:28 GMT  
		Size: 9.8 MB (9774604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a6b709bed6b18e5ba839847d0f3e3a5a4e53a163b69ea7858c561fdc7f1e3a`  
		Last Modified: Sat, 28 Dec 2019 18:48:25 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af9a8179e95515f1f6e62a300ca75906566906d949c7403c9f61b8511afc033`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23b6ea616f3e8e138683f48ca757b84bc23de865b250839eba047a141cc6721`  
		Last Modified: Sat, 28 Dec 2019 18:48:46 GMT  
		Size: 62.1 MB (62085764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101b4656b4d26f6236d97a86a31ae20834b113b525d2830521853323cfb6369`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 451.5 KB (451514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e52b33734a366437f8b9e807980e3273684eeef72d2fd1822dc4ea7ae5638`  
		Last Modified: Sat, 28 Dec 2019 18:49:32 GMT  
		Size: 224.6 MB (224573326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de7b9c0321a0098bd333b1ceb564c2a4389249dc4f9e3f45da7c389198a1ba`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033d8666e6f7cc5f88f89356fb0b79d8bcb42f576c433b924571484da93bdc43`  
		Last Modified: Sat, 28 Dec 2019 18:50:04 GMT  
		Size: 103.0 MB (102961244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:b5d4d93ac96fb5c6fdeccd356249126962289756b90317d84f673586b5ca3f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e873c3fc43f41e5ad2d12d94f7bed5b7003663c082267173164c435f0fccd7ac
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351057156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30b7b2faeb653ede7f6ad75b823b2a3bcf33aaee8ca468c506816815cbb6ea2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:71fadcaf02a6a1c64ffb2556a1845dd5a7f50db82fd36b28d6070bfa70a46c05
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (311960235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9787b288f41d6777936dba39f82b0689986fb51c6420d41c213cbd84fda7013b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9068251c6380c479ee68ff541bb2ca47b1289bf9abc492be8772a781157e81c2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333008606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862fc4352003f0d8220db2c412401b528522361f69db17a3d5bdbc00b2bbe8e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:b5d4d93ac96fb5c6fdeccd356249126962289756b90317d84f673586b5ca3f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:e873c3fc43f41e5ad2d12d94f7bed5b7003663c082267173164c435f0fccd7ac
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351057156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30b7b2faeb653ede7f6ad75b823b2a3bcf33aaee8ca468c506816815cbb6ea2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:04:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 08:22:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 08:23:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 08:23:29 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 08:23:37 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 08:23:38 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 08:26:22 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 08:26:23 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 08:26:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 08:26:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a7a80998c2488750fb62cc72ab6b34ff4df5153da1f459e097dc693564ab46`  
		Last Modified: Thu, 19 Dec 2019 07:18:37 GMT  
		Size: 837.4 KB (837369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c5773ef4faea2ab4bb067f34730723b5e4e4e5124526e52f046d4fda6ff93`  
		Last Modified: Thu, 19 Dec 2019 08:43:29 GMT  
		Size: 6.8 MB (6776450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5aab8a595911e0f910e5bbc45fbaba1872d9b2ff7ddf0b8596fe487e6b35ed`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a691a8db646c53d5a2c1bc8133de575f671497f29ba26550912c360fe7c92e84`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224950fdddc8e9a7e0642acd70f24e007e024605e33623bd88fa78c701d7e738`  
		Last Modified: Thu, 19 Dec 2019 08:43:40 GMT  
		Size: 55.1 MB (55078634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b544deac8ac028cca15755fe7f73466c66453367d47613d71723e888966206`  
		Last Modified: Thu, 19 Dec 2019 08:43:27 GMT  
		Size: 450.8 KB (450831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfeeeabb29071b671ff85ced5fe96a930389986cdb960d654b253f4cc981292`  
		Last Modified: Thu, 19 Dec 2019 08:44:19 GMT  
		Size: 261.2 MB (261186116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32130377944b2d86d62bf74958bd8765a6db237ce408848f094f9012bfd55da7`  
		Last Modified: Thu, 19 Dec 2019 08:43:26 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:71fadcaf02a6a1c64ffb2556a1845dd5a7f50db82fd36b28d6070bfa70a46c05
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (311960235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9787b288f41d6777936dba39f82b0689986fb51c6420d41c213cbd84fda7013b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 06:09:19 GMT
ADD file:0b507e6fc0387385b81eb4b0b08a7f002c26cedd83accdfb47ec3b19da44f05c in / 
# Thu, 19 Dec 2019 06:09:23 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 06:09:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 06:09:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 06:09:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:17:08 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:17 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 06:59:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 06:59:23 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 07:00:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 07:00:31 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 07:00:51 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 07:00:53 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 07:08:29 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:08:33 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 07:08:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 07:08:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b0b312c654a9005a92655349cacee5a649d1bfe150d2c297568f5e7ee164c3bb`  
		Last Modified: Mon, 02 Dec 2019 15:30:10 GMT  
		Size: 22.3 MB (22275326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a2b7886d4309cb3ee39451b8d94c4b2e723555d9b5704c5e41d851c393e9`  
		Last Modified: Thu, 19 Dec 2019 06:14:43 GMT  
		Size: 35.5 KB (35459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07ab3b900d1c89ef87b70fcf305d67a8534335dacf8d799ca8bc2648ee082a`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1f49a588539a397d55c87543a08282192f41e544029df74a83714075010fca`  
		Last Modified: Thu, 19 Dec 2019 06:14:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef97618b6d676c44cb31fe287f3d84e47d454365a734cf411f4e43971bdb535e`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 838.0 KB (838032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74cc414b82f13364c01a11f261e8dfed1c196857c6ff34fb70f0ae05cdadfe5`  
		Last Modified: Thu, 19 Dec 2019 07:28:34 GMT  
		Size: 5.6 MB (5627378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df074ca58e1db5e1711022ecb5cdd76a220b6bcdad705ae5f2b4097dcea2525c`  
		Last Modified: Thu, 19 Dec 2019 07:28:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b10ee1dff6220bba3f0494edd98e32dae244100726ac1d65948bcab451571`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8b3b5e870295ae6e91943a63475637fb09bd851a8b97e5d6538c2e8d5d02bb`  
		Last Modified: Thu, 19 Dec 2019 07:28:54 GMT  
		Size: 50.1 MB (50110869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005c3125f47e1a15eeb61825c4016a74ef84c311e2ebe39ecfdaa069d25c3d9b`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 450.8 KB (450781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba09cdd58271001701d29f1fb4b54a02439e03b240e48983b5c3a314c47bf3b2`  
		Last Modified: Thu, 19 Dec 2019 07:29:37 GMT  
		Size: 232.6 MB (232619513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43581541e27c972fc18c3282a8cd3c06be9ee0e2ac22cac04e534064b4b5822f`  
		Last Modified: Thu, 19 Dec 2019 07:28:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9068251c6380c479ee68ff541bb2ca47b1289bf9abc492be8772a781157e81c2
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333008606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862fc4352003f0d8220db2c412401b528522361f69db17a3d5bdbc00b2bbe8e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 19 Dec 2019 03:49:55 GMT
ADD file:1f180a3d70349350f43f477e4053af7a5fbc4d62d4e76ada091884500bfb6ee1 in / 
# Thu, 19 Dec 2019 03:50:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 03:50:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 03:50:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 03:50:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 08:35:50 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:29 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:18:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 19 Dec 2019 09:18:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 19 Dec 2019 09:19:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:19:35 GMT
ENV LANG=C.UTF-8
# Thu, 19 Dec 2019 09:19:36 GMT
ENV LC_ALL=C.UTF-8
# Thu, 19 Dec 2019 09:19:53 GMT
RUN rosdep init     && rosdep update
# Thu, 19 Dec 2019 09:19:54 GMT
ENV ROS_DISTRO=melodic
# Thu, 19 Dec 2019 09:22:38 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:22:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 19 Dec 2019 09:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 19 Dec 2019 09:22:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:083ab90813fd405397dbca2b021972603ae62211e401e42b4e928dff050de9c2`  
		Last Modified: Mon, 02 Dec 2019 15:30:26 GMT  
		Size: 23.7 MB (23718714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87467c9ed1fdecf80ce31dc51b980ebd7b2391419ff6113f32e4d170c9f4c4b6`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a1b2b6a922bf6c8024e2f9276928ed5e5538fd58bf3f0ba6a4a193d515ee7`  
		Last Modified: Thu, 19 Dec 2019 03:55:41 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69de117a966f92306b4142bdfbccb0b74cbef319ce8b1c6652cf92ce28b0ddf1`  
		Last Modified: Thu, 19 Dec 2019 03:55:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17024d1f595c1964e3292740469d5bc052a8d1acd8225621a2e0bc3791d729be`  
		Last Modified: Thu, 19 Dec 2019 08:44:33 GMT  
		Size: 837.7 KB (837722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7031f0dfe1a04190bd784e5140bfe7a474f680cb88e49c049b6a2d371157dc0d`  
		Last Modified: Thu, 19 Dec 2019 09:45:57 GMT  
		Size: 6.1 MB (6093647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9585186791b7513d0e7887faa2eda00c150730fa9d288e256287ba4f707523`  
		Last Modified: Thu, 19 Dec 2019 09:45:55 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f78613907751037733fccddc9dc67a836dd5b544bbf0b2c8923d21c01acac`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc647a64f2557054880db6223f6f3db4ff16b7bb70d6134c12db30f9e832725`  
		Last Modified: Thu, 19 Dec 2019 09:46:13 GMT  
		Size: 52.9 MB (52924497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a00593d29483a6884bc23393ee1795cfa7a81f65260cfe008652fccbd45e1c`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 450.9 KB (450888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccdbbaf4322fbc1f325853bb8914640a8811d91977624dee8288ac558140ca`  
		Last Modified: Thu, 19 Dec 2019 09:47:04 GMT  
		Size: 248.9 MB (248945060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db7cb2524131c6a2ce80bdff4abf63cb47681674f1f9ac63006daddf3cb5f8`  
		Last Modified: Thu, 19 Dec 2019 09:45:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-stretch`

```console
$ docker pull ros@sha256:7f6d57bf3e025d7f7311adeee42aa8042c51c5f2decb742908aad12d1444c56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-stretch` - linux; amd64

```console
$ docker pull ros@sha256:43aaaa6cfb47d8de9eb5b33e656a4e9747a57a7c09c3933cac178d0052794aea
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 MB (391485934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac88139a4ae488377be19ec7123f1ce8e6e1e001bef55d16813f80f4aa1e54`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:26:02 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:26:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 08:26:07 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 08:27:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:27:02 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:27:03 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 08:27:21 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 08:27:21 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 08:29:05 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:29:06 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 08:29:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 08:29:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cf93dae3672c4b23e304be8bfbd86a1a70e192920d9bb7d980774a433b7123`  
		Last Modified: Sat, 28 Dec 2019 08:34:45 GMT  
		Size: 10.5 MB (10476716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4d94fcfba96b58c2a901f6286ca7d1ce99dacfe09968fc037d5553f2025e8a`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa7ebb2626a2bc1ed27e07d7ca29f5a02c7cfb09f84608d38f9c99b1b798ced`  
		Last Modified: Sat, 28 Dec 2019 08:34:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc08219e7fdb9a27aa4c99a6f1d467eab7640d963871a1400ebfdaae3af68c57`  
		Last Modified: Sat, 28 Dec 2019 08:35:00 GMT  
		Size: 64.8 MB (64771041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191195f75e3d8a24ce1e680579fd09913504e418871b9b7ec1e38aaa061fdd1`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 451.5 KB (451468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9fd3f2a56a2d531756ee769940fada1e88517a593b70c3e21e959874a7bc78`  
		Last Modified: Sat, 28 Dec 2019 08:35:41 GMT  
		Size: 270.4 MB (270404151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0106c5e798490c33945ce9ebe7647215eb890cf55e081b770471e498436353`  
		Last Modified: Sat, 28 Dec 2019 08:34:42 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-stretch` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f5ec08ded445c9338b439668c8e668290ed0528a5cc3278334fe8e7b6a44f748
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340053502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed90e0838aeb67fd3fa8237f21c25198eacd48a0305185d1e41973423fc8b5e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:15 GMT
ADD file:e439b3c387852978811a6a5a058745ebb9392da7e8936beb4f37ff076e656213 in / 
# Sat, 28 Dec 2019 04:43:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:34:23 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:34:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 28 Dec 2019 18:34:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu stretch main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 28 Dec 2019 18:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:35:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 18:35:41 GMT
ENV LC_ALL=C.UTF-8
# Sat, 28 Dec 2019 18:36:03 GMT
RUN rosdep init     && rosdep update
# Sat, 28 Dec 2019 18:36:04 GMT
ENV ROS_DISTRO=melodic
# Sat, 28 Dec 2019 18:38:50 GMT
RUN apt-get update && apt-get install -y     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:39:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 28 Dec 2019 18:39:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 28 Dec 2019 18:39:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d07bcf5901dfa793fa6b2c4c617e86bcef315b0b092cbfd1a929eefedaf8e3f2`  
		Last Modified: Sat, 28 Dec 2019 04:48:57 GMT  
		Size: 43.2 MB (43166476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facfbd1fae886a379926b7add3095adbf575d32e87e67282e12488332f12f747`  
		Last Modified: Sat, 28 Dec 2019 18:48:28 GMT  
		Size: 9.8 MB (9774604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a6b709bed6b18e5ba839847d0f3e3a5a4e53a163b69ea7858c561fdc7f1e3a`  
		Last Modified: Sat, 28 Dec 2019 18:48:25 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af9a8179e95515f1f6e62a300ca75906566906d949c7403c9f61b8511afc033`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23b6ea616f3e8e138683f48ca757b84bc23de865b250839eba047a141cc6721`  
		Last Modified: Sat, 28 Dec 2019 18:48:46 GMT  
		Size: 62.1 MB (62085764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101b4656b4d26f6236d97a86a31ae20834b113b525d2830521853323cfb6369`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 451.5 KB (451514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5e52b33734a366437f8b9e807980e3273684eeef72d2fd1822dc4ea7ae5638`  
		Last Modified: Sat, 28 Dec 2019 18:49:32 GMT  
		Size: 224.6 MB (224573326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de7b9c0321a0098bd333b1ceb564c2a4389249dc4f9e3f45da7c389198a1ba`  
		Last Modified: Sat, 28 Dec 2019 18:48:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
