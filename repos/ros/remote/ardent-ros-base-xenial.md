## `ros:ardent-ros-base-xenial`

```console
$ docker pull ros@sha256:ce76d7f1c764de0ae2f7dbbf2ddc0a78cac8b7561cf2266ef517af4dbbf898ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:ardent-ros-base-xenial` - linux; amd64

```console
$ docker pull ros@sha256:84e0ce3330f1e31621a47cc8ce26eef30abe005906ae0bc5c746b1cd8518c4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332444170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9dfb57a4fa5044d165f6d5be6aefc74b598e69cf2502341a95bcb225471e828`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 29 Dec 2018 04:54:49 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Sat, 29 Dec 2018 04:54:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 29 Dec 2018 04:54:49 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 29 Dec 2018 04:54:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["/bin/bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo "deb http://snapshots.ros.org/ardent/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LANG=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN pip3 install -U     argcomplete # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV ROS_DISTRO=ardent
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-core=0.4.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-base=0.4.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:997925534c696e5039f0cdbaee36a2b963654a6c246790dd610a7191d9585ea1`  
		Last Modified: Fri, 06 Jun 2025 23:09:44 GMT  
		Size: 77.2 MB (77231411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:ardent-ros-base-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:8f29bcc6c80ca2bab6168b546f88bf7e2fab3a5738809a59e0ee2334d2b3a2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32204727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07501a77c3f6d22a5fdf2776532e5a600934ff57d772c6cf365fcfa64ffaf8c0`

```dockerfile
```

-	Layers:
	-	`sha256:931b4619a49046b79ced5a319c275a10d2c0fda53e80defc7cef9eef8a74d20b`  
		Last Modified: Sat, 07 Jun 2025 01:17:26 GMT  
		Size: 32.2 MB (32194199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c275c565ec83b35164ff13b3d0a4e5678118fc5266ef8758aac01e238c7e9b`  
		Last Modified: Sat, 07 Jun 2025 01:17:27 GMT  
		Size: 10.5 KB (10528 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:ardent-ros-base-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:25ebceb94ac44dde500f003dc71432bcfcb935f685d9aee9b646f05fcf77aaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270086574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46431e18d392af694ab57cbf5e25583ed2ce27aa5163fb954aa2e7bb9980091`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 29 Dec 2018 04:54:49 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Sat, 29 Dec 2018 04:54:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 29 Dec 2018 04:54:49 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 29 Dec 2018 04:54:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["/bin/bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN echo "deb http://snapshots.ros.org/ardent/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LANG=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 29 Dec 2018 04:54:49 GMT
RUN rosdep init     && rosdep update --include-eol-distros # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
RUN pip3 install -U     argcomplete # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENV ROS_DISTRO=ardent
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-core=0.4.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 29 Dec 2018 04:54:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 29 Dec 2018 04:54:49 GMT
CMD ["bash"]
# Sat, 29 Dec 2018 04:54:49 GMT
RUN apt-get update && apt-get install -y     ros-ardent-ros-base=0.4.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:2a39eaf20e8f7895dd04511bcc9b71e0fc0fc4efaab9c0b09f3fed881add722f`  
		Last Modified: Fri, 06 Jun 2025 23:29:47 GMT  
		Size: 75.1 MB (75103201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:ardent-ros-base-xenial` - unknown; unknown

```console
$ docker pull ros@sha256:771976fa6aeb30e6d8d41504a5bd835fb99d5b4d8a71010baef98c96a06fcc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32099947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644cacca8286d52d81e013cfef58d80046b278d29b5037f970037dbed8478b2b`

```dockerfile
```

-	Layers:
	-	`sha256:a16cbfdc5641daab8b9b76939eb9378a114ba55be69eb82e7931c4cd8b515f64`  
		Last Modified: Sat, 07 Jun 2025 01:18:01 GMT  
		Size: 32.1 MB (32089282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4719551cbaacc87aef74a64a1283333a7476d8ae5a3f729f4d7236032abe99`  
		Last Modified: Sat, 07 Jun 2025 01:18:02 GMT  
		Size: 10.7 KB (10665 bytes)  
		MIME: application/vnd.in-toto+json
