## `ros:eloquent-ros-core`

```console
$ docker pull ros@sha256:9a489b9efd83aa2184ded15ece6294379fcbe25358745b0a7f56b03ec68e07b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f449b9ba717163a6f582ec87bcfa197415f0c956041dc4a85d31ca1f1f4bb240
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215424356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5788930d3d48c366a4f4a319bf58852bffa221c169aadda42356654c7b038334`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:37:59 GMT
ADD file:ef36fee25b0bd1d99979ecb8d54b206cec33d4e8fd2232189f0d8e5ab9754798 in / 
# Thu, 21 Jan 2021 03:38:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:05 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:26:51 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:02:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:02:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 11:24:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 11:24:07 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 11:24:07 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 11:29:46 GMT
ENV ROS_DISTRO=eloquent
# Thu, 21 Jan 2021 11:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 11:30:55 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 11:30:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 11:30:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d519e2592276828ca171d85e0532899cd4f98c70f5c697b45fa2e126e9f9fe49`  
		Last Modified: Thu, 21 Jan 2021 03:40:27 GMT  
		Size: 26.7 MB (26709716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d2dfcfa9cd230ed3c47defec2670d45081598c721dd85cafc34ea459f970e`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3afe92c540b778c64ca316d1e679d55d2d2e812e450f516a808ee591f0c3f77`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea992ddb93cee91b21cf19902eb7c0780191f8454157802d68fe834ad6c72d5`  
		Last Modified: Thu, 21 Jan 2021 08:49:44 GMT  
		Size: 840.0 KB (840038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe549b7120b83770f6772179d9e937e479567ac1297ed6808a3c029da14a498`  
		Last Modified: Thu, 21 Jan 2021 11:44:40 GMT  
		Size: 4.9 MB (4870380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3148dcdae1e4da81fc90c6c4dc4ca6a3612c7176d9a53c61cf366eb77428c96`  
		Last Modified: Thu, 21 Jan 2021 11:44:39 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b05bde605617d448eae8a91768817550ef24992dd60f0fb9ae887e07d2860b`  
		Last Modified: Thu, 21 Jan 2021 11:51:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90292505d7326fcf14326b5832275a274f935f100f6635ef221fb3084163d54`  
		Last Modified: Thu, 21 Jan 2021 11:53:01 GMT  
		Size: 183.0 MB (183001366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a79c3a57a82264d768f385d23e2a6db7ec45a227262ba0f1a33ad1e82902ef4`  
		Last Modified: Thu, 21 Jan 2021 11:52:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:346190a94c07de2b9415db178ad6dc6e51aacb0a993a27171fd31ec26c32fe42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183836607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b83746e6c165550a665e348644197528f161409d2528d0ed2e463d1421eeba`
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

### `ros:eloquent-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b5da766bedd15f1aa393d7f911b05c33e038e7b79efbe49ac84c484f7644a37f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197431059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695e4445f819eb6c07bbc46b6ccd24aaaf849ef5d15d9d35853853937c632455`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:35:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:35:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:35:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 06:54:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 21 Jan 2021 06:54:42 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 06:54:43 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 07:01:08 GMT
ENV ROS_DISTRO=eloquent
# Thu, 21 Jan 2021 07:03:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 07:03:25 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 21 Jan 2021 07:03:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 07:03:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75de3cb7cc851400a98b3f91be110991f7d3e5ef9e3362b2a1feaabe73b663eb`  
		Last Modified: Thu, 21 Jan 2021 07:25:58 GMT  
		Size: 840.9 KB (840945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d872ef396f747e28f1e5d655b4da63120065e5b8c19b451d0fd13ff642a0b99`  
		Last Modified: Thu, 21 Jan 2021 07:25:55 GMT  
		Size: 4.5 MB (4453230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4f3dc2dc6bc64630a22a47f207e4ff99ae9332e157017224e77646d47bfe94`  
		Last Modified: Thu, 21 Jan 2021 07:25:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d90ee048de88433b386164e5f1c1d3cc6a3f6a5bffd8ae7b49cccece73ca7`  
		Last Modified: Thu, 21 Jan 2021 07:33:30 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df77184d7d8e42363aa9c8dbfc8239f84ffcd09d1830e2605a419e1d90d9863`  
		Last Modified: Thu, 21 Jan 2021 07:35:23 GMT  
		Size: 168.4 MB (168401359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0765bd8d495afad02fb63a44551da2de2dfc6abf2aac15a9113e48b48b3fe94`  
		Last Modified: Thu, 21 Jan 2021 07:34:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
