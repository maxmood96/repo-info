## `ros:kinetic-ros-base`

```console
$ docker pull ros@sha256:b851ec0bbb8c8ce3e12a2c08235e63a64b1d59aa98d19298f29e0b9041176977
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kinetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:81129e9483002653ea37a195911b48dc04a0d57c372478f17cd89bd47fa0c0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359888733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1619cf7aa662824915c0e5d646c362009ee38caad81bab4a1daf03bcb947c51a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 19:36:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/kinetic/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=kinetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Fri, 13 Dec 2024 13:12:07 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Fri, 13 Dec 2024 13:09:14 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Fri, 13 Dec 2024 13:10:06 GMT  
		Size: 528.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Fri, 13 Dec 2024 13:08:51 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8573b6923cb6a22b67d526bc12405fb6fbcbcb2e87c5ec4b154b6a46a52b0e`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 5.2 MB (5233825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfa084cb42f8b7c0c5fc72960c7637d1f92a1b0fc524eef71103a912586d110`  
		Last Modified: Fri, 06 Jun 2025 22:49:25 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8216b921d7ce0dcc05a81a498d6de866de3c930c16a595613c1fb649779ddbd`  
		Last Modified: Fri, 06 Jun 2025 22:49:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1587ff828e09727000bce6476c7288b0cd7bf11909ca08e5ecc295ca826e6de7`  
		Last Modified: Fri, 06 Jun 2025 23:07:36 GMT  
		Size: 187.2 MB (187154626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929b1bee8c4433c20dd2131efc184396b3ce55546124d3d2561feace2646af54`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173439ff273fecb2c1bdb4fa903c5b55f27746719229311b73062c8ff71a6e40`  
		Last Modified: Sat, 07 Jun 2025 00:07:49 GMT  
		Size: 57.2 MB (57249051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b8a523b115cfaf42058575e2e51f393c6f70dce0fa0d584a0d83ba57189a5e`  
		Last Modified: Fri, 06 Jun 2025 23:29:01 GMT  
		Size: 333.7 KB (333678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b7189315bed63fdc78712186278827f912dd6dd982fd6b4fbddf5893c87674`  
		Last Modified: Sat, 07 Jun 2025 00:07:49 GMT  
		Size: 63.4 MB (63400694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:ebec154b5af08c35f92a5dc718a8561b783ef0b069e568c266a135cf1faf2f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29801621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8996bd09717108260c42522297a03e27d2a626621ffb85c594e4e117e8984a19`

```dockerfile
```

-	Layers:
	-	`sha256:017d6b200070df4a595bc992b8b04b3ddfb1df7f424eaa3688303eca2a77a303`  
		Last Modified: Sat, 07 Jun 2025 01:21:50 GMT  
		Size: 29.8 MB (29786698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3409edf495a418e0993fbfb87a74560ac6a532ccc68dd21646bacfa51770ca7`  
		Last Modified: Sat, 07 Jun 2025 01:21:51 GMT  
		Size: 14.9 KB (14923 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kinetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:231a954068cf50cfdc8a03ac6f363bc88ca7828a25d163266fd2866c7cf77c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311382386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3356030e9d9cf8e96164c6f1311b234c82e93327f9023231ef36e2ecd813abf7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 19:36:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/kinetic/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=kinetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Tue, 17 Dec 2024 15:12:14 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67de3a011d085fbb829ef04d78536904c6ead23dbc82dd5facff2488d6398672`  
		Last Modified: Sat, 14 Dec 2024 10:56:05 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1202719f1ed95c66ca12784e9dd1983de008b6871eb2cb324c3a3f1a98836af`  
		Last Modified: Sat, 14 Dec 2024 08:45:37 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1764d93e99e79b6b91814768fa379cc5ce0dce26c71ecfe2f5fc6b3f38212b`  
		Last Modified: Sat, 14 Dec 2024 13:56:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804f9d49b32e303626788f9b5b8013d33088cee5fe4c2be72c4bb1a0533ae06`  
		Last Modified: Fri, 06 Jun 2025 23:00:12 GMT  
		Size: 4.5 MB (4484967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252fe34aaa0848dbcc21b4ef0212654fbe433d929c5964f3587f2a24835e6fd6`  
		Last Modified: Fri, 06 Jun 2025 23:00:11 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86d46b11a9d0c34ceabe354c26a103e09a978ef35e1ba17702032b954cfe73`  
		Last Modified: Fri, 06 Jun 2025 23:00:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77743ef7a8832f45a6f3836d366dda203fec014ee4a31ccfcbd6078ddf1d07b`  
		Last Modified: Sat, 07 Jun 2025 11:46:30 GMT  
		Size: 168.0 MB (168016694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e63262682947848a4f9e8464fd8fd261c8fe4de26bde6ce013477302fe8c40`  
		Last Modified: Fri, 06 Jun 2025 23:00:12 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3973509aa68b831a826551ab81e39c61ab48c9f356effcfa91a79db8f6462f8b`  
		Last Modified: Sat, 07 Jun 2025 11:46:45 GMT  
		Size: 42.9 MB (42892908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942e7ce90b3afe563251d5168f67f0ff123e57a758db3f7e5a3bdae0577860fa`  
		Last Modified: Fri, 06 Jun 2025 23:22:34 GMT  
		Size: 333.7 KB (333749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085e478ebabab7465a3e15a9d7c7572f0d3ad446db887e1ba2bdf14e366136b8`  
		Last Modified: Sat, 07 Jun 2025 11:46:56 GMT  
		Size: 55.3 MB (55322516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:bb1785841ddec90a5908c1edeb1b056ee3545c03de96ffd195b77014e56d58ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29575886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd2498a60252569e974eed3b9141c847a411deedeb544c7fb850786f49bd19`

```dockerfile
```

-	Layers:
	-	`sha256:e2cb45ba2619255965130c259fe00c28b0af9d99950bb4eb829b1e845c03b61b`  
		Last Modified: Sat, 07 Jun 2025 01:22:16 GMT  
		Size: 29.6 MB (29560773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:544cb89fa8b25b191f0d217f804512cd542f3411b633cba48f24b41134a177c3`  
		Last Modified: Sat, 07 Jun 2025 01:22:17 GMT  
		Size: 15.1 KB (15113 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kinetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fb8350d354a2c5cf62e447e909e70fda722de4066934878b1807d081837aee9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325343311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cec9e29a2048c442d8151fb5c1164024e8b1b8a23bee9a6570b2c5b9b1f658`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 17 Nov 2020 19:36:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/kinetic/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=kinetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-base=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Fri, 13 Dec 2024 17:43:40 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66927c6d1d3d2e9321c4893f7f2105b7cd23dfb082853d97ec08f188e271e612`  
		Last Modified: Fri, 13 Dec 2024 20:27:34 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000560be91651dcbf476ebacb8bf1f1339694a3327f8e6da2519e0b29b33eb5d`  
		Last Modified: Fri, 13 Dec 2024 18:38:28 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6225a0253717abdc2ee23ea211c1c439c93b84231ec0a4f1c74762a205ba7234`  
		Last Modified: Fri, 13 Dec 2024 13:19:32 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a712877b94dc94bc028192c1b3f25ce8351629d028a2d4e4e7808d08896564`  
		Last Modified: Fri, 06 Jun 2025 22:54:20 GMT  
		Size: 4.7 MB (4690335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95085c5b5fe521cd17a6df8b9aa20a6480c271642a41a96189c1cead5a5e4af4`  
		Last Modified: Fri, 06 Jun 2025 22:50:51 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60636c5e16fddd9f1d86e9e886a5b5578e34fc00d0e5cf5437a7f412a2e845f6`  
		Last Modified: Fri, 06 Jun 2025 22:50:51 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aa7678aa8b0212fef7cdac5ab297b6000cb80b6029b579c75073b486439ac`  
		Last Modified: Fri, 06 Jun 2025 22:50:41 GMT  
		Size: 176.0 MB (176001674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c026138e6ea9500bc5611be62a58e4858b04c4e999fdb1f2a20029e673a41d`  
		Last Modified: Fri, 06 Jun 2025 22:50:52 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370d79e5099dd0a1823461cd6e00abe5a4c365a1ffe3e5c4b871a2ebceed7bef`  
		Last Modified: Sat, 07 Jun 2025 11:46:58 GMT  
		Size: 46.0 MB (45950920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd33ebbb3f99dae61d8c4a27d607a3d8375f564e06e8d65dba40093dcead0afc`  
		Last Modified: Sat, 07 Jun 2025 00:12:04 GMT  
		Size: 333.7 KB (333672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2892e34e33d2258066381f910f616415517e82951770d82a783ee68f73396040`  
		Last Modified: Sat, 07 Jun 2025 11:47:07 GMT  
		Size: 57.1 MB (57108193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:cd6791064f68844055850daf1e23a48318d768ee3cd14c79006fdadd21b95655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29650478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd72d87318c32118549e159dea6e92d68ee0502d9e01b393e881b43f1bdef082`

```dockerfile
```

-	Layers:
	-	`sha256:d1866bdbafaca8da451bda0a15fc25566b48afa6584dd80b3393937b40933ebb`  
		Last Modified: Sat, 07 Jun 2025 01:22:43 GMT  
		Size: 29.6 MB (29635337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b1ff4359beddc0a1e576694e20f43007d4fafcb88486a75551e08e1b86adc0`  
		Last Modified: Sat, 07 Jun 2025 01:22:44 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json
