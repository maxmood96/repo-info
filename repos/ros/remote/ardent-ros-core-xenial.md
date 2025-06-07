## `ros:ardent-ros-core-xenial`

```console
$ docker pull ros@sha256:6bc3937dae7903c52764eace68529bb29d5dfb362701867158e985459f0fb602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:ardent-ros-core-xenial` - linux; amd64

```console
$ docker pull ros@sha256:6bc8d65c3e830d58c72b1ba7c7382e414256d7fe62f793dde778fa7b110451b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255212759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590f2cb6c9171a6322f033a25386f91aa26a1dde32fd3a369c570b0a9325081e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/ardent/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN pip3 install -U     argcomplete # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=ardent
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-core=0.4.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
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
	-	`sha256:7f59f20327a3c2413a15c81911a19c6e774f759e51f4a85a7c8479c39d808ee5`  
		Last Modified: Fri, 06 Jun 2025 23:07:45 GMT  
		Size: 129.1 MB (129109617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915665829fdac6e9940941926b7c0b9362f15eccd4c7674706590a3e9447ed55`  
		Last Modified: Fri, 06 Jun 2025 22:50:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0863b244a1a644d59a8f712f37dd50c3a2fe37bf0250dc83c023c631bc2f9f60`  
		Last Modified: Fri, 06 Jun 2025 22:50:15 GMT  
		Size: 17.3 KB (17334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60a7ca7f4fb30a9c5893b95f609b310ace6b6724688864bd69637181aa0e07b`  
		Last Modified: Fri, 06 Jun 2025 22:50:17 GMT  
		Size: 26.7 MB (26686761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52030ddcd0b88c9553f6b1ec0abbaa8079db7745238bd548938ba0f348d25e46`  
		Last Modified: Fri, 06 Jun 2025 22:50:16 GMT  
		Size: 2.0 MB (1981200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889492a95465d0b352992bb61da8818e75811499944b249804c85648fb256778`  
		Last Modified: Fri, 06 Jun 2025 22:50:16 GMT  
		Size: 2.5 KB (2539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236a36680ba1a5cbc6ffdb152d83e8a6983155a53c70dc30aceb2ff1553a1017`  
		Last Modified: Fri, 06 Jun 2025 22:50:17 GMT  
		Size: 163.3 KB (163332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46f6a498141b05f3af5f31e9775c1b72f553ca3cb19b362e8f79b2c46873a51`  
		Last Modified: Fri, 06 Jun 2025 22:50:19 GMT  
		Size: 50.8 MB (50752442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3796a3883e730442716e1577c464868ec5978b41b4429d52a5e08144d95a86ec`  
		Last Modified: Fri, 06 Jun 2025 22:50:16 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:ardent-ros-core-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:c7dbbb5bee1ac57a703b2be0507e8ee389471f7ac4591e989ff1b09c16077d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20883472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384e33c055c0cbe88c59bf70f93cc7b5f94fd20f7f4254e641c8641201087817`

```dockerfile
```

-	Layers:
	-	`sha256:f73f62ab78969eccc0075023c1d3c5371e05541de8aa2a38627709df01e97832`  
		Last Modified: Sat, 07 Jun 2025 01:17:34 GMT  
		Size: 20.9 MB (20856205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14bddf3ce8239f7b393f37d106720cf6da62cf1a3e7c93a9bd84fb7780456b16`  
		Last Modified: Sat, 07 Jun 2025 01:17:35 GMT  
		Size: 27.3 KB (27267 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:ardent-ros-core-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e4132aff96c55c81f5a9dbb99d9c109f120b3e9138a29c74b1fbcad518948697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194983373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f61a1c21cebb0cf3cd8102b92118fcd4cf4c65c465ee2b4ca2e3bab0f4d1d9a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:17 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Tue, 25 Oct 2022 05:55:18 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 25 Oct 2022 05:55:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:55:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 25 Oct 2022 05:55:19 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN echo "deb http://snapshots.ros.org/ardent/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:34 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
RUN pip3 install -U     argcomplete # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENV ROS_DISTRO=ardent
# Fri, 01 Dec 2023 06:00:34 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-core=0.4.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:34 GMT
CMD ["bash"]
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
	-	`sha256:642051bdf7c2fe86c8c44eb60a138cc9028990ffdbe783acbbec666dfcc570aa`  
		Last Modified: Fri, 06 Jun 2025 23:04:25 GMT  
		Size: 77.1 MB (77065494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a82607868b5101f8741789c8b84c0dc2ce6cfbdd3c5194627e2d16f95cb5c9`  
		Last Modified: Fri, 06 Jun 2025 23:04:21 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbe483ceedb2282180bda9dc1bb6e367030a4aa1d239326432fe1b29a12a02`  
		Last Modified: Fri, 06 Jun 2025 23:04:21 GMT  
		Size: 17.3 KB (17335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741cff9a25c93ecdb0981c5eb7124e6a1a43b177237d7e98255c0b541a8bc85a`  
		Last Modified: Fri, 06 Jun 2025 23:04:23 GMT  
		Size: 25.4 MB (25362838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76970b8c328bb4c9efde14a1b5972c3a84080a906812c9d840202875be6de665`  
		Last Modified: Fri, 06 Jun 2025 23:04:22 GMT  
		Size: 2.0 MB (1989575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38430a3d4ab5bd0403e7c584ea69cb2517390df271de7426829bd635cfc35461`  
		Last Modified: Fri, 06 Jun 2025 23:04:22 GMT  
		Size: 2.6 KB (2561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8ddcf224ebaf82a962fb0140f00099f3d7c9e062a18c648d0510801fedd236`  
		Last Modified: Fri, 06 Jun 2025 23:04:23 GMT  
		Size: 163.4 KB (163378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e866277645906e5996f83e646757e226467a1649cc01a478fadca5fa85b27b57`  
		Last Modified: Fri, 06 Jun 2025 23:04:26 GMT  
		Size: 49.1 MB (49141001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10542168abc3289e7113754b442061867474e9713b4f8771bc437f90593b7917`  
		Last Modified: Fri, 06 Jun 2025 23:04:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:ardent-ros-core-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:472d7338e12d9bf6f2a8ca99ffc347d856cab613d2ef37e154e56222097663ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20781607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595d02d83d270c998c5f567deea5866451811e108d48ef536b708cea240394f4`

```dockerfile
```

-	Layers:
	-	`sha256:b219b9d5cd2712d3b50842d664ddefa5cc9f03db878a6d41699b26086a6c0477`  
		Last Modified: Sat, 07 Jun 2025 01:17:49 GMT  
		Size: 20.8 MB (20754170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743d7eb9ab0d563ebb2353a9625d81efd29b0fdb4a8f8fd5a78c1d722e572241`  
		Last Modified: Sat, 07 Jun 2025 01:17:50 GMT  
		Size: 27.4 KB (27437 bytes)  
		MIME: application/vnd.in-toto+json
