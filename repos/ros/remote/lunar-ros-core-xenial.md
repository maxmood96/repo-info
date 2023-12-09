## `ros:lunar-ros-core-xenial`

```console
$ docker pull ros@sha256:55777aff9eaf2e6d8e2533e49a6a7f466e19276eb6b8100d489c38a4077c0449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:lunar-ros-core-xenial` - linux; amd64

```console
$ docker pull ros@sha256:8b5e82738b936e58bd93fbbe8a1aaa674f038cb3e3d1ec73fdac2007df298c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302873830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc37b082307948caf045416f3172f44e4d07d5d2e69cd715be30f32741f6ef48`
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
# Sat, 09 Dec 2023 02:39:52 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:39:53 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:39:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:40:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:40:25 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:40:25 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:40:48 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 02:40:48 GMT
ENV ROS_DISTRO=lunar
# Sat, 09 Dec 2023 02:41:45 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:41:48 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:41:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:41:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba1da48150be3464b0312a4a4317a2a6ca7c2fef2a7f3e8ddff3578fcfad3da`  
		Last Modified: Sat, 09 Dec 2023 04:31:14 GMT  
		Size: 6.9 MB (6940871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a309d39e728b7140a20ff64cb5ebb67b7bbbae039706d87ca989bd89e395b57`  
		Last Modified: Sat, 09 Dec 2023 04:31:12 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255a59fbdcede020dc55b73edb0cb3ce5219feb0640b7ba039ae80a236d6debc`  
		Last Modified: Sat, 09 Dec 2023 04:31:10 GMT  
		Size: 17.0 KB (16979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c74770ec06cb9f7020f3aac56f71cb01e9850e5fd1d82b02caec32752eafd5`  
		Last Modified: Sat, 09 Dec 2023 04:31:22 GMT  
		Size: 54.3 MB (54259186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5b3568df762c68c61b7a7c8e52975f9def6687fd7c8db5e4ce95ac9270fdb7`  
		Last Modified: Sat, 09 Dec 2023 04:31:11 GMT  
		Size: 1.6 MB (1611438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb090c382fe71f673961d1f7e14162b9723d61ec262795c97ee3ca2b7464af41`  
		Last Modified: Sat, 09 Dec 2023 04:31:47 GMT  
		Size: 193.5 MB (193545824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef8d941936706e76f42503c124245262cb1b272db9d9f91217c3b772d34b6d8`  
		Last Modified: Sat, 09 Dec 2023 04:31:10 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:lunar-ros-core-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:db8823eb76533dd67c7eb883858222793d060e37f81a1182cb795399e5f7fc13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262384453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f3d0861215d0f5e0cfb976eea9f9f5e239058983842f65d7c3331f80feb8e8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:07:58 GMT
ADD file:294a94a081de785c730003a440a0530a85add2bcb60c0f5bc4ce7ee17867ac4e in / 
# Tue, 25 Oct 2022 03:08:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 25 Oct 2022 03:08:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 03:08:02 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 25 Oct 2022 03:08:02 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 02:50:12 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:50:13 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:50:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:50:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:50:40 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:50:40 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:51:01 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 02:51:02 GMT
ENV ROS_DISTRO=lunar
# Sat, 09 Dec 2023 02:52:00 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:52:04 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:52:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:52:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b95ba076a26b98e98eac4b43596b59c20d1e61a36bcaf2afae3aeebadc8844cf`  
		Last Modified: Sun, 08 Aug 2021 01:00:22 GMT  
		Size: 40.3 MB (40312250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67de3a011d085fbb829ef04d78536904c6ead23dbc82dd5facff2488d6398672`  
		Last Modified: Tue, 25 Oct 2022 03:10:54 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1202719f1ed95c66ca12784e9dd1983de008b6871eb2cb324c3a3f1a98836af`  
		Last Modified: Tue, 25 Oct 2022 03:10:54 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1764d93e99e79b6b91814768fa379cc5ce0dce26c71ecfe2f5fc6b3f38212b`  
		Last Modified: Tue, 25 Oct 2022 03:10:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b80b81a7040e4c0b02b0abd72e1a97adbcd5bce111d7a502b04c3fbf186c5`  
		Last Modified: Sat, 09 Dec 2023 03:36:21 GMT  
		Size: 5.7 MB (5703072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a0756f6cf5b450181fd7d35a86f4a4d94bef3c6cc9931f167a50444415786f`  
		Last Modified: Sat, 09 Dec 2023 03:36:20 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd4e25781c8b5697552ea6f485f033566488485ec3698a21c7a3e4e0a12bf42`  
		Last Modified: Sat, 09 Dec 2023 03:36:18 GMT  
		Size: 17.0 KB (16979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bdb9f94d12140f4a8fd814dc094d00d7e899e702073a4b6cfd0c7c45359618`  
		Last Modified: Sat, 09 Dec 2023 03:36:30 GMT  
		Size: 49.8 MB (49814931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f353a8df1a914a2b8632491afcdd248e4162d0da470b9f7312c512934a8d24`  
		Last Modified: Sat, 09 Dec 2023 03:36:18 GMT  
		Size: 1.6 MB (1611470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9924350c9f8e995a0df3833fa4a91c592210ee06553122a9019833581732e`  
		Last Modified: Sat, 09 Dec 2023 03:36:55 GMT  
		Size: 164.9 MB (164923777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff9288e4dc53084dd34a30a91c07bcc72bf91d6aa5f296597445fc3467daedc`  
		Last Modified: Sat, 09 Dec 2023 03:36:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:lunar-ros-core-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d8c8fd5ad9a14423cf9c8f7fa93e6ee2de90d8cc9ed2587da8758f8be1b1c5c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274583260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6067a2db69eac9c309a91fb4a424afbdcd8c8028a28c77c7ca00d54ccffa0672`
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
# Sat, 09 Dec 2023 02:17:34 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:17:35 GMT
RUN echo "deb http://snapshots.ros.org/lunar/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:17:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:17:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:17:59 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:17:59 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:18:18 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 02:18:18 GMT
ENV ROS_DISTRO=lunar
# Sat, 09 Dec 2023 02:19:07 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:19:12 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:19:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:19:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66927c6d1d3d2e9321c4893f7f2105b7cd23dfb082853d97ec08f188e271e612`  
		Last Modified: Tue, 25 Oct 2022 05:57:02 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000560be91651dcbf476ebacb8bf1f1339694a3327f8e6da2519e0b29b33eb5d`  
		Last Modified: Tue, 25 Oct 2022 05:57:02 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6225a0253717abdc2ee23ea211c1c439c93b84231ec0a4f1c74762a205ba7234`  
		Last Modified: Tue, 25 Oct 2022 05:57:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9358939b1458b8b88ebc24636cfaeed34b2650b95831d478c76a61620f77bd6a`  
		Last Modified: Sat, 09 Dec 2023 03:51:18 GMT  
		Size: 6.0 MB (5959635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63bc909feb825fd5f3d5aa6d07252239d99d6e880a1fb78d7ccb3e49af49c16`  
		Last Modified: Sat, 09 Dec 2023 03:51:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff0b91c4df7587880944eb5992575206f7203a1a7078df9dbf926293b873ca4`  
		Last Modified: Sat, 09 Dec 2023 03:51:15 GMT  
		Size: 17.0 KB (16982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0327480e967f65c7d48af173d87548a8e17252628715c83b32861e247cdc80c0`  
		Last Modified: Sat, 09 Dec 2023 03:51:25 GMT  
		Size: 51.6 MB (51565210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4f06fd0a818693e15998856eab1c52e499de4d9aa9e0f539552900b24cc688`  
		Last Modified: Sat, 09 Dec 2023 03:51:15 GMT  
		Size: 1.6 MB (1611446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a597d484fddd204774965461408927c43958578a354a3e1a5e1140c9ce456270`  
		Last Modified: Sat, 09 Dec 2023 03:51:47 GMT  
		Size: 174.2 MB (174188799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3a1dee3a06cbbabef948d1b7df41e7db7394bc5caa7676dfaee141930f7e59`  
		Last Modified: Sat, 09 Dec 2023 03:51:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
