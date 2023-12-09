## `ros:indigo-robot-trusty`

```console
$ docker pull ros@sha256:ff31d297038f8b37e7a5d6998665f0d7cebae77b820790a076c74befdca9b955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm variant v7

### `ros:indigo-robot-trusty` - linux; amd64

```console
$ docker pull ros@sha256:2e4fce86c5b19df40a1cab833a9ce6e9760f19f55ad6b124c49a3466edad808e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333529237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb32c23b9a9140b884dbd32d639a2999f9528b2a64b2804d52bef241cce3a97b`
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
# Sat, 09 Dec 2023 02:13:01 GMT
RUN echo "deb http://snapshots.ros.org/indigo/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:13:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:13:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:13:45 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:13:45 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:14:09 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 02:14:09 GMT
ENV ROS_DISTRO=indigo
# Sat, 09 Dec 2023 02:16:36 GMT
RUN apt-get update && apt-get install -y     ros-indigo-ros-core=1.1.6-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:16:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:16:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:16:38 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 02:17:50 GMT
RUN apt-get update && apt-get install -y     ros-indigo-ros-base=1.1.6-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:18:43 GMT
RUN apt-get update && apt-get install -y     ros-indigo-robot=1.1.6-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1e64097ecdc27174710d13fa38bb31305493acbde6bf43d0c3a2829e7aacac4a`  
		Last Modified: Sat, 09 Dec 2023 04:24:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2c1e615ad78b75bf5f7ff680cd727ddf19e627d5fb2c7d233e0abc282111b6`  
		Last Modified: Sat, 09 Dec 2023 04:24:44 GMT  
		Size: 15.3 KB (15325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1d571639cb96d5efeb22a0101ea94ddb1a8e0e996e37ff3f517a825a314c5d`  
		Last Modified: Sat, 09 Dec 2023 04:24:51 GMT  
		Size: 30.9 MB (30916798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f92aba38d11aae4066169659f0b37865b0a14fe5508080c69071187700880f4`  
		Last Modified: Sat, 09 Dec 2023 04:24:45 GMT  
		Size: 1.6 MB (1611443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107a822dfdeb5553899a0de270743c42a851c992f6967cbc682274d814d5ba16`  
		Last Modified: Sat, 09 Dec 2023 04:25:13 GMT  
		Size: 150.0 MB (149967614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbc1688717a18b4bb6914e07af354ce3c84aca85e9c41c35cf490fb81db2421`  
		Last Modified: Sat, 09 Dec 2023 04:24:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70ef0771ff1f908ae937e201f779f819e5b64425bc94f3b001677458ea30339`  
		Last Modified: Sat, 09 Dec 2023 04:25:30 GMT  
		Size: 46.8 MB (46786192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1490404e551bde07e2958842e486566d8651224cb388c64c04e6d4b5a78ecef5`  
		Last Modified: Sat, 09 Dec 2023 04:25:45 GMT  
		Size: 19.0 MB (19035439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:indigo-robot-trusty` - linux; arm variant v7

```console
$ docker pull ros@sha256:890534eea0c632cdd4fe68ddde59e99e1c846cb259d21671f495cb8be168a4c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303167883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da212c810dd8c7310a87ec5b34474688f532076bd6594c77c04d5efce3c2256a`
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
# Sat, 09 Dec 2023 02:23:02 GMT
RUN echo "deb http://snapshots.ros.org/indigo/final/ubuntu trusty main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:23:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:23:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:23:46 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:23:46 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:24:11 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 02:24:11 GMT
ENV ROS_DISTRO=indigo
# Sat, 09 Dec 2023 02:26:44 GMT
RUN apt-get update && apt-get install -y     ros-indigo-ros-core=1.1.6-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:26:46 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:26:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:26:46 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 02:27:33 GMT
RUN apt-get update && apt-get install -y     ros-indigo-ros-base=1.1.6-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:28:27 GMT
RUN apt-get update && apt-get install -y     ros-indigo-robot=1.1.6-0*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:0478947c0c1a4d7a23d9410e34b7bfa85e250e5bdb13e2fe7a7c23fb40959f9a`  
		Last Modified: Sat, 09 Dec 2023 03:29:59 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fd31b5325c39d7ced7627cbbaa4e65fed2886161e1f2ccf1b78e7191d8402d`  
		Last Modified: Sat, 09 Dec 2023 03:29:57 GMT  
		Size: 15.3 KB (15319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c634c81fc4924e33cfdac87b03a11441a177230579e1229824253bedc77f5fd9`  
		Last Modified: Sat, 09 Dec 2023 03:30:04 GMT  
		Size: 28.4 MB (28379872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f81dbd1a456c35d28a0ccbfe88e2949ab5edd892d2de6c95e5a250a0294a03`  
		Last Modified: Sat, 09 Dec 2023 03:29:58 GMT  
		Size: 1.6 MB (1611485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c16526727904ad230390337eeb65dcb5a68f03408ee5a10f781132b889725b`  
		Last Modified: Sat, 09 Dec 2023 03:30:29 GMT  
		Size: 137.6 MB (137591936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13a51bf14241277dffdf75e5789a4298d0b710d8287a402d18dda765f3957c4`  
		Last Modified: Sat, 09 Dec 2023 03:29:57 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4b98b1fe44920174ec592b5c955b5f5c1f31296db81d69609bdc36e0d1c5a5`  
		Last Modified: Sat, 09 Dec 2023 03:30:45 GMT  
		Size: 40.4 MB (40392694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca0ee35ba6f6ad5d0c20125def2aa943181c84a75eb726d9d0b4482795fb91e`  
		Last Modified: Sat, 09 Dec 2023 03:31:01 GMT  
		Size: 17.7 MB (17691083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
