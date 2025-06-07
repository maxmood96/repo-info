## `ros:kinetic-robot-xenial`

```console
$ docker pull ros@sha256:a1d8308431e2f4ef024cb603220c9f2e3eb2a949a43ebcb64857165314830dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kinetic-robot-xenial` - linux; amd64

```console
$ docker pull ros@sha256:52393b4547e95f14793bdcdf65e593f70f46db6c0ef49dba59e6ef5edbfd82e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 MB (381403965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371122fce11112481df29e91461867c2a1b2da79b6f0280e53afcedf78152956`
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
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:bd8e71a6997214bea423419898421f1e9e1b360c601202db9427d3703d1da534`  
		Last Modified: Sat, 07 Jun 2025 00:09:34 GMT  
		Size: 21.5 MB (21515232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-robot-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:ecf49b5e9e923af52b7789bdba7015fc5e80d93b90e19dc4256987e950af2969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31827160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a93e7191c31a013c5f0e94554dc4e1551ebc3ba898df358e14015311f8f154`

```dockerfile
```

-	Layers:
	-	`sha256:d56a1ef14345698ced14c9ff6d60bdef979259ad08fcab29e6d5777814a159f5`  
		Last Modified: Sat, 07 Jun 2025 01:22:14 GMT  
		Size: 31.8 MB (31817202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc99658f3a722f18185ce01c45f3f9dc532bef713390db881e9ef2225a0c9b0`  
		Last Modified: Sat, 07 Jun 2025 01:22:16 GMT  
		Size: 10.0 KB (9958 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kinetic-robot-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:e4ed0ab966496d0c4539d5cc9ced0e029e2e08ab7956a0a7ba4c892d2574b59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.6 MB (331649240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d249815717e6df527b2d259afd51d1e6ac981fffdffcf8daa0118d9a09d8148`
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
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:202533c9d66c483fedc02e4ea22d03c4467019b01d1a9e686f95f1a8df515306`  
		Last Modified: Sat, 07 Jun 2025 00:22:13 GMT  
		Size: 20.3 MB (20266854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-robot-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:30f20b8235d5f28daf610b072b43a2fb974a3f26bc3608101b6ac60a274d8f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31602216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf1adf3b9a839ae0af42d353b1d756b466d7cb169542723689c890d4869537e`

```dockerfile
```

-	Layers:
	-	`sha256:3da93eea9ff4d385cae916c76fc8acf756c2e7bbb120b875a4cc33dd61e8a2d3`  
		Last Modified: Sat, 07 Jun 2025 01:22:48 GMT  
		Size: 31.6 MB (31592150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa462306029efa492bea048f06344eef58a3ecc504eb15fcc391278121953ea5`  
		Last Modified: Sat, 07 Jun 2025 01:22:49 GMT  
		Size: 10.1 KB (10066 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kinetic-robot-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:358c0809c5c0bc9e4e03c81251a000d4cfa3eaa50efe31d9e36e429226ef3204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345866650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb82d465bb6e0060c9f333f10dc2ffad86e2bcf6d222f991d417bff99b02e33`
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
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-robot=1.3.2-0*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:5c5edd9195df07b63521ed8eab56b849e705fa0ef8b13c61cd2389bf14815592`  
		Last Modified: Sat, 07 Jun 2025 00:08:43 GMT  
		Size: 20.5 MB (20523339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kinetic-robot-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:307f9ac77d299f2aeac809b19d4bf0454c7078b5cc988838c2f99f8866a64012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31675940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7dfff6ac73d32ac0f39c30306820918e584adfce8932327ab1b52df98d0c8d`

```dockerfile
```

-	Layers:
	-	`sha256:c8973675086ea04a5c478117dab5903f8047bd3e1d40d4be77dd1cb184e1356b`  
		Last Modified: Sat, 07 Jun 2025 01:23:17 GMT  
		Size: 31.7 MB (31665854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15e66d2ff749a66e493dc40738d80594fb9547854ab8e3bfdf80fc7d549a9b1c`  
		Last Modified: Sat, 07 Jun 2025 01:23:18 GMT  
		Size: 10.1 KB (10086 bytes)  
		MIME: application/vnd.in-toto+json
