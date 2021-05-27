## `ros:eloquent-ros-core-bionic`

```console
$ docker pull ros@sha256:4516dc4a2e50e0eb9be283a9cf575fc032bf95ae7c4e6d5404c97f4d40b6dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:eloquent-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:4ff43133e50a332ae85aaf22d91b9269d46125a9fa8c612bbd753477e279b29a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215471967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4a85f68e4ed58d4c82f27be3dc77cb0f6da7711b0a25b9c42f6d92640ed158`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:35:57 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:49:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 21:49:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 19 May 2021 22:02:52 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 19 May 2021 22:02:53 GMT
ENV LANG=C.UTF-8
# Wed, 19 May 2021 22:02:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 19 May 2021 22:05:31 GMT
ENV ROS_DISTRO=eloquent
# Wed, 19 May 2021 22:06:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 22:06:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Wed, 19 May 2021 22:06:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 19 May 2021 22:06:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1270d8e5a641a61675efd742287bbc693c243ab17fd4886a7550878d186f2565`  
		Last Modified: Wed, 19 May 2021 22:11:29 GMT  
		Size: 841.4 KB (841350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8ca49cb51a84fa2a9f93d1c7107f0d2aef6eba8e6373200924e7ed48f92b25`  
		Last Modified: Wed, 19 May 2021 22:11:28 GMT  
		Size: 4.9 MB (4872908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16393a6ac7473d1c49944336fa197f4dd193e6738e769c9485c31fcb6912e55a`  
		Last Modified: Wed, 19 May 2021 22:11:27 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af7786db6953ff9b0956663127b915dfd9785175f7c4ce5bac8ed4d3a42f8df`  
		Last Modified: Wed, 19 May 2021 22:14:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340abd911eddcda855fe16e37d73e81079bd9e327f3123908a0ae3c1d081709d`  
		Last Modified: Wed, 19 May 2021 22:15:45 GMT  
		Size: 183.1 MB (183058522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a92ef446eff175c18b6d7daafb53a4eee3cc667dc5a91733f885dd3947aa46`  
		Last Modified: Wed, 19 May 2021 22:15:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:39a59134330e10a1560d3ed6b134fdd0e87dc5fea03529178ad5c9e373068557
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183872217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4932df5c5343701e1a10a573cfc9ed91b3d3b8d1799ca39c9d1156c5c06d2ba7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 May 2021 17:00:25 GMT
ADD file:c990710d70105be91eebcea7dfdf28e2212d37ea9279eb2dfd0071e9ed2fd4f1 in / 
# Wed, 26 May 2021 17:00:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 26 May 2021 17:00:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 26 May 2021 17:00:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 26 May 2021 17:00:27 GMT
CMD ["/bin/bash"]
# Wed, 26 May 2021 23:58:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 23:59:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 26 May 2021 23:59:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 27 May 2021 00:12:42 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 27 May 2021 00:12:42 GMT
ENV LANG=C.UTF-8
# Thu, 27 May 2021 00:12:43 GMT
ENV LC_ALL=C.UTF-8
# Thu, 27 May 2021 00:16:22 GMT
ENV ROS_DISTRO=eloquent
# Thu, 27 May 2021 00:17:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:17:51 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 27 May 2021 00:17:52 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 27 May 2021 00:17:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c61ae1d5a3957b8a0838e053004a2ddf56e395d58ee3b63baa7b1c865a6383b9`  
		Last Modified: Wed, 19 May 2021 20:23:59 GMT  
		Size: 22.3 MB (22292007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efaa8fe9a238b7a58ef37a164ef3a580b7e27445d98012b50395eedd92bad76e`  
		Last Modified: Wed, 26 May 2021 17:03:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07c60aae22667580605aaf11e146d4ccd94df1bb94c42d91954727cd3515f9a`  
		Last Modified: Wed, 26 May 2021 17:03:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d935c6c5648a195e1f983ccaccfaf15bc4a8a7d76fbc25ca9d74a088cf1eca58`  
		Last Modified: Thu, 27 May 2021 00:25:19 GMT  
		Size: 841.2 KB (841165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ced11f60bd4cd445ffd162c5741258552033e478ee07a70c27a6bcbe9617084`  
		Last Modified: Thu, 27 May 2021 00:25:18 GMT  
		Size: 4.1 MB (4085572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7613d5403bc02868ee97e0011a528b36689e78ed74e3ded0b8b6d8800f9be5f2`  
		Last Modified: Thu, 27 May 2021 00:25:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6cc8227b417cd5bd483e886dcc4d7fbf238b6eb835b2e04e841f950dfb46a7`  
		Last Modified: Thu, 27 May 2021 00:32:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b70082ef822c7732096962ec6400a15d137f63bcc68adf4b0f60358de8c018`  
		Last Modified: Thu, 27 May 2021 00:35:01 GMT  
		Size: 156.7 MB (156650595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01851ed76b96980ba08583b94dd86a08ba653d527f9778bbc8ec5bf0a810ba7`  
		Last Modified: Thu, 27 May 2021 00:34:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:eloquent-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1b749aedf65fa91254f00bca24335f4fecd5a183c5960618940bd3c6d16f78f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 MB (197403583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a473cd81786cd38a7883b20490fd53099d22964795178bd3e0375c7b28f35ec7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:47:15 GMT
ADD file:5f7cb4b44f843eaef6ae7ddb75dfc228a33d20cd974074ca23c1bb2cad7f77ad in / 
# Fri, 23 Apr 2021 22:47:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:47:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:47:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:47:24 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:23:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:23:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 24 Apr 2021 00:46:16 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 24 Apr 2021 00:46:17 GMT
ENV LANG=C.UTF-8
# Sat, 24 Apr 2021 00:46:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 24 Apr 2021 00:53:59 GMT
ENV ROS_DISTRO=eloquent
# Sat, 24 Apr 2021 00:56:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-eloquent-ros-core=0.8.5-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:56:50 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 24 Apr 2021 00:56:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 24 Apr 2021 00:56:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:673aeee5c81c892477834e2b5e55575f16bfd52d9b841a1d8c524fb3805ee960`  
		Last Modified: Fri, 16 Apr 2021 16:25:11 GMT  
		Size: 23.7 MB (23703698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018b2790219d2003c0d437e634927887ee5cc3d8f985d7459adc5b2ff62d003f`  
		Last Modified: Fri, 23 Apr 2021 22:49:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509c77ce92ade89fbf09fe03b167023be51bf5a0c14c00487fa7a9ee33b55fc3`  
		Last Modified: Fri, 23 Apr 2021 22:49:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4d7949f503cfae35d1e4072cc9f714f7f8080ddc5b9c1a01a837bd00682493`  
		Last Modified: Sat, 24 Apr 2021 01:23:29 GMT  
		Size: 841.2 KB (841190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ffbacc392e75d546f657a3c5ccfb65077a82acaaf78fd4ee3e380b95ef811f`  
		Last Modified: Sat, 24 Apr 2021 01:23:26 GMT  
		Size: 4.5 MB (4453794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476ab02969bb3ddd3e04ec5657467e4e747f59f5e3e02c4af893ad380c8c6cfb`  
		Last Modified: Sat, 24 Apr 2021 01:23:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ca8bca9319a705f62ad9a055c3c031669e45715063fe23a399dc70e087705`  
		Last Modified: Sat, 24 Apr 2021 01:34:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeeb1f6ada61ac221f57749e9f46fdfe5c1a1a0d49da126542cc2434a7792ba4`  
		Last Modified: Sat, 24 Apr 2021 01:38:42 GMT  
		Size: 168.4 MB (168402022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b6099d852cf1da33eb73a465970abde3c79d1e51a4fa4eec2cc7e8a058d4b6`  
		Last Modified: Sat, 24 Apr 2021 01:37:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
