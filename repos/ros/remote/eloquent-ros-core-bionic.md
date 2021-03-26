## `ros:eloquent-ros-core-bionic`

```console
$ docker pull ros@sha256:3f17da0f098d4a08d6bb1e0abefd928ac3dbb5d8e692db6c01e1eb6600438734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:dd84d45d16fa5103f31691ae3d6ca36eeec06cefa44a233f450917c2903e5ab3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215428458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91145331c29cad9e66a93332ebb57e0808e0eb1146754af2312af284560d806`
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

### `ros:eloquent-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:e136fceeb7503f3b4fa8370cc8e568d0ac98648dbe58496a58e97141a6d56bb5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183832710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc65b6c9672c590a0161ea000f8e7a6c6faeed1684acb204c3d6ad8920ee47d`
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

### `ros:eloquent-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d6595d656d96dbe88e58f924717d65fab729c31bac595f80336ecbac284d1063
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197450814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e3be564764aab41d418f68431ba20cb52d3f72d0ecb74855a6ab78f4097a46`
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
