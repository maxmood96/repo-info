## `ros:jade-perception`

```console
$ docker pull ros@sha256:dffa08d5134dbfc2d422ae7f11bc980c2e66068d259f055271b2f3190d2afc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm variant v7

### `ros:jade-perception` - linux; amd64

```console
$ docker pull ros@sha256:902b5358f0d39fee6b17bca74d101a8ca7004a1c3e03461c5a0dd63a31875d5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535311876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae08b9b38adaadc267ea6b3d9b8ad21b189d6f40b829c7dbcaf7b95ece9c523`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:40 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 25 Mar 2021 22:33:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:44 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:13:00 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:23:50 GMT
RUN echo "deb http://snapshots.ros.org/jade/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:23:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:24:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:24:25 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:24:25 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:24:47 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 02:24:47 GMT
ENV ROS_DISTRO=jade
# Sat, 09 Dec 2023 02:25:37 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-core=1.2.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:25:39 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:25:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:25:39 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 02:25:52 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-base=1.2.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:27:59 GMT
RUN apt-get update && apt-get install -y     ros-jade-perception=1.2.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0551a797c01db074ab0233ceb567e66b8ebdcb9de9a2e7baa36d57dfbca463a3`  
		Last Modified: Thu, 25 Mar 2021 22:35:39 GMT  
		Size: 72.7 KB (72664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512123a864da5e2a62949e65b67106292c5c704eff90cac2b949fc8d7ac1e58e`  
		Last Modified: Thu, 25 Mar 2021 22:35:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d01337e947ad8ba5e7f80fe0d19f7e8e84090acc36f4b1c5cf200012cd97bb`  
		Last Modified: Sat, 09 Dec 2023 04:24:49 GMT  
		Size: 14.4 MB (14431564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c96153f4e588786cd925471a77fc3556a775f66f5670ebf2d0e0fb0e29d5d0`  
		Last Modified: Sat, 09 Dec 2023 04:26:44 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbb9cb708d8ceb426b09fe00dc9bb7c16daefa236b44400fbefb3d3bdbef35e`  
		Last Modified: Sat, 09 Dec 2023 04:26:42 GMT  
		Size: 15.3 KB (15320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe08daaf27c2f3a370a2349f40b68adbfd23136223f9451c3e2f33d6006cedb2`  
		Last Modified: Sat, 09 Dec 2023 04:26:49 GMT  
		Size: 30.9 MB (30916570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd1679552169184505d19ce771ce96fd496c5b33d3c8fbc1ee2e439259ea27a`  
		Last Modified: Sat, 09 Dec 2023 04:26:42 GMT  
		Size: 1.6 MB (1611440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0751997d97cf8c1b521c5a34413e1d7637fe87361010221313ebcbf797e28ce8`  
		Last Modified: Sat, 09 Dec 2023 04:27:12 GMT  
		Size: 150.1 MB (150103492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e25e86d5ba9fa465b66f0984335414abb68428fe6d01f0687a411788de38135`  
		Last Modified: Sat, 09 Dec 2023 04:26:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a97430dcbef96a4842e71af48a3751e0e81deab991f658fba4ab3ce51c10ee6`  
		Last Modified: Sat, 09 Dec 2023 04:27:22 GMT  
		Size: 4.0 MB (4019240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398362f1ab721cfc99dd0a801ceb7c430aa52ff204079753bfc5907880e0c0aa`  
		Last Modified: Sat, 09 Dec 2023 04:28:33 GMT  
		Size: 263.4 MB (263449390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jade-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:dd988c73e0325db104c75b4f2887afdd28ea8913dacea880bf40767bdf6665be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483068998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ca05e03c48de16d62f064ae021268f520067a93df0f3cff1190173a452ad26`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:07:46 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 25 Oct 2022 03:07:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 25 Oct 2022 03:07:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 25 Oct 2022 03:07:49 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 25 Oct 2022 03:07:49 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:23:01 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:33:30 GMT
RUN echo "deb http://snapshots.ros.org/jade/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:33:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:33:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:33:58 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:33:58 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:34:19 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 02:34:19 GMT
ENV ROS_DISTRO=jade
# Sat, 09 Dec 2023 02:35:08 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-core=1.2.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:35:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:35:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:35:14 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 02:35:32 GMT
RUN apt-get update && apt-get install -y     ros-jade-ros-base=1.2.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:37:31 GMT
RUN apt-get update && apt-get install -y     ros-jade-perception=1.2.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a31831ce9fd9e38ad9d926286efdb85e400dc823da723d72cc676869c295fb0`  
		Last Modified: Tue, 25 Oct 2022 03:10:28 GMT  
		Size: 76.8 KB (76775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66373b79ee1bedb2a2bf237fb2a717660559ee8e3fec0aae52d9797c2b32b27c`  
		Last Modified: Tue, 25 Oct 2022 03:10:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d774ce67fd876f763d56c53eda188d1d3d2f597db1c31de370c9bb8078081`  
		Last Modified: Sat, 09 Dec 2023 03:30:01 GMT  
		Size: 12.8 MB (12784112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54c115f62ca21dee95b1512826f919cf441ef820ad4def1fd12e9399cfd2368`  
		Last Modified: Sat, 09 Dec 2023 03:31:58 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0a76166bf02cedd290a248eb2b6936b5050f1867e626fd4a1e875a3c1c181d`  
		Last Modified: Sat, 09 Dec 2023 03:31:56 GMT  
		Size: 15.3 KB (15323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0435615c916dd3345d46937ee435a0444206a393cfe5128f7267986aefec3bd`  
		Last Modified: Sat, 09 Dec 2023 03:32:03 GMT  
		Size: 28.4 MB (28380029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ff40d2bf1609ff61e7db9047f51372b505754fe595fe7867653d62cde72ab5`  
		Last Modified: Sat, 09 Dec 2023 03:31:57 GMT  
		Size: 1.6 MB (1611489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad007fe4c686a92a7afdee4c7d40555a8777f4978c95555372f2f323425a80d6`  
		Last Modified: Sat, 09 Dec 2023 03:32:28 GMT  
		Size: 137.7 MB (137714912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60141996d55b47658bdb73f10c2906a9616a7c7b53b356d1b2258ed2de7d317d`  
		Last Modified: Sat, 09 Dec 2023 03:31:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c090b43ae257023878b4f3578b78f70878cfd158cfd3516f8b78b9aa923232c4`  
		Last Modified: Sat, 09 Dec 2023 03:32:40 GMT  
		Size: 3.7 MB (3666801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2881c454f602f72f250a4c91e1d1019526c4088bf4298368a900d61d1dff486`  
		Last Modified: Sat, 09 Dec 2023 03:33:51 GMT  
		Size: 234.2 MB (234194950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
