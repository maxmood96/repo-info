## `ros:kinetic-perception`

```console
$ docker pull ros@sha256:123b2e076ad488760600d3299d2ae1f2a87f9b0990fe40b68034cf434316b9d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kinetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:5dd10cb3fdff1882137b979feca65c8e54082e5c6e8c78634d50ae0dc7e64372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.3 MB (676329948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c61ae162dc8e5abd75dc8613881c66058d93694289404fdc3935443ccd9970`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:39ed2d3912a910cf9c264bffc3590b58bebb2684242b37e3ce63a2cd2b2e928a`  
		Last Modified: Sat, 07 Jun 2025 00:10:39 GMT  
		Size: 316.4 MB (316441215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:88ba44ff2511c37cf6c1ce7774233bc0fd99c11db1185c580a9d7037cfe38432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45687370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d510114586f8b0aedd0dc079d89d6acf909237f287637f4da86794dd4332e8`

```dockerfile
```

-	Layers:
	-	`sha256:1d997fefcf7188b96249a6059fb75127e7abae91432b74dcdeb9d10a1e151bb7`  
		Last Modified: Sat, 07 Jun 2025 01:22:02 GMT  
		Size: 45.7 MB (45677364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819c0892676708f62b33cc7969182227aee9e996971ab64aec605771cd66ad1a`  
		Last Modified: Sat, 07 Jun 2025 01:22:03 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kinetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:e33731fa2b18fe02abcc2e9ae4acc49bc1d0133bab80216a13000d3e9824e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.4 MB (569366085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1d96c72c6b183082edfe6ad025ee91e808ace030e52bbf36a9ac64805ff9e2`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a0b740576158196fdf9c5aaeea77c575fccac2b513e8451d50e1d33a45c979fc`  
		Last Modified: Sat, 07 Jun 2025 11:47:14 GMT  
		Size: 258.0 MB (257983699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:35fcc1262f7198c372c06290cc0238f766c7989ab9c55863695517e6c42d4997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45440809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d67f7835d5d2b066a454b3f0097f0e6ff44e5981465954f6a81251f6f06ad4`

```dockerfile
```

-	Layers:
	-	`sha256:fd6577503bd1f89e4fc9ab4c374ac70aef5286a0ed6aeee8a2de96fcb61fd004`  
		Last Modified: Sat, 07 Jun 2025 01:22:52 GMT  
		Size: 45.4 MB (45430695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fea4db284efdfaef32ab828c747de3954e0ce4e4be935dae03cf55fb0d609de0`  
		Last Modified: Sat, 07 Jun 2025 01:22:53 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kinetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:904de36c3faeec26b9d0faba41619010fbf25c9cdc00f404ce61353707277e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.4 MB (592374027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318fc4222ea8537db6fa0995b1b6de77f7f24ee1ad84b5149d9521c36077f386`
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
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-perception=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a9aad4e25c121cc8dd435963d8509184f1606ec1c2b22cca9de19340943c5857`  
		Last Modified: Sat, 07 Jun 2025 11:47:35 GMT  
		Size: 267.0 MB (267030716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:d491a24d8364e303150970d274d7dd3ca3c34d2e758be7cadb2da84aee766824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45332833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd813f374510efff3174f3c2119f5b0db930c825f572e416d4b6d496cb6ceca0`

```dockerfile
```

-	Layers:
	-	`sha256:48228e3a839e2f175b782da6c6be0fc963042405ac03bcef59075be1580f4b07`  
		Last Modified: Sat, 07 Jun 2025 01:23:47 GMT  
		Size: 45.3 MB (45322699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58358444c2c23bc4b0042a8fcb5ce5ecef8f24b317d6494debc81dcad9043094`  
		Last Modified: Sat, 07 Jun 2025 01:23:48 GMT  
		Size: 10.1 KB (10134 bytes)  
		MIME: application/vnd.in-toto+json
