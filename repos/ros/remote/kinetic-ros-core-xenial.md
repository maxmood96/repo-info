## `ros:kinetic-ros-core-xenial`

```console
$ docker pull ros@sha256:3e8cbb7d3fbaac9c32440e46a423155d4ab927a20dcd3346d1bc0cb249b45fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core-xenial` - linux; amd64

```console
$ docker pull ros@sha256:fd6ed9ee18e53c0849b3d14a59de8b33cb389eaf1a951157926cdd9adf9773cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239053350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5810b19bfb42a0b16a331cdd071b78c441558ffa18ffd5b3cb3a55fdb38bfadf`
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
# Sat, 09 Dec 2023 02:28:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:28:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:28:41 GMT
RUN echo "deb http://snapshots.ros.org/kinetic/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:28:41 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:28:41 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:28:41 GMT
ENV ROS_DISTRO=kinetic
# Sat, 09 Dec 2023 02:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:31:41 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:31:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:31:41 GMT
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
	-	`sha256:51198ea216b4afa7b1145d361703d59a75ae9355dfae3d6a96280497583387f4`  
		Last Modified: Sat, 09 Dec 2023 04:28:43 GMT  
		Size: 5.4 MB (5364529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c7af8a2828b66ef1b1e3181b45d4470469f67657711f3ab91d1db26247064f`  
		Last Modified: Sat, 09 Dec 2023 04:28:42 GMT  
		Size: 17.0 KB (16980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5e704ca9382fcd31dbaf46473967f6b90212513d2a2f94c65fc16c88a5c89a`  
		Last Modified: Sat, 09 Dec 2023 04:28:42 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a6224a46620d02f972d2034204e764f00b37dd40b02cea4c5dddfcddd5f75a`  
		Last Modified: Sat, 09 Dec 2023 04:29:21 GMT  
		Size: 187.2 MB (187172315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f04f0f76145710d92517a5e46f5676a9ffd0db557eea02df467c41f2ba51a2a`  
		Last Modified: Sat, 09 Dec 2023 04:28:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:ea6bf56d6c55c21e064276bd6f6976fe0aa33bd7d8bf353570a791ec0291d981
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212984337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b775ba65eb5c314dcd0887bab5dc1edc10cf675468f67663bb5719586dc6c710`
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
# Sat, 09 Dec 2023 02:38:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:38:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:38:28 GMT
RUN echo "deb http://snapshots.ros.org/kinetic/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:38:28 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:38:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:38:28 GMT
ENV ROS_DISTRO=kinetic
# Sat, 09 Dec 2023 02:41:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:41:42 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:41:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:41:42 GMT
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
	-	`sha256:2b481def126bbe5e51e00147206a54d74b82d1c5d9cbebbb91f2198a288da443`  
		Last Modified: Sat, 09 Dec 2023 03:34:00 GMT  
		Size: 4.6 MB (4615558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c334ced8e9a34cc86d4c93b9170f8718eb5dc1de806e47db96c051959dd664c`  
		Last Modified: Sat, 09 Dec 2023 03:33:59 GMT  
		Size: 17.0 KB (16978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff3d9b435929fd0710dd407d00571dcbd3df58260ce5f4ac5977f82f1a8f37b`  
		Last Modified: Sat, 09 Dec 2023 03:34:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514602800f7755a543e5b81771887782002c8013fca5d7bf8058355e7d1c70f4`  
		Last Modified: Sat, 09 Dec 2023 03:34:40 GMT  
		Size: 168.0 MB (168037582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d541bb9e8daa03162635e4d21bfc26959327ebd90a4ed07d34f9a84aeed598`  
		Last Modified: Sat, 09 Dec 2023 03:34:00 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:50825ddd9f7bb8f3da67c5ff2d060319c84a28f89ee943ce7986fba3891f2dc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222100963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b71d7e613fd9c0849adcc76ad15e0e843935240c6a2c841a3790ccd45921277`
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
# Sat, 09 Dec 2023 02:06:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:06:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 02:06:30 GMT
RUN echo "deb http://snapshots.ros.org/kinetic/final/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-snapshots.list
# Sat, 09 Dec 2023 02:06:30 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:06:31 GMT
ENV ROS_DISTRO=kinetic
# Sat, 09 Dec 2023 02:09:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:09:37 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Sat, 09 Dec 2023 02:09:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:09:37 GMT
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
	-	`sha256:4334610fbf3db0b30d017e58e9054473e71894ae2c80b30288e4024492008aa5`  
		Last Modified: Sat, 09 Dec 2023 03:49:09 GMT  
		Size: 4.8 MB (4821109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ac2879c260f3b60817040ef127a513f007ef86ae2910ceecedbc89984ee815`  
		Last Modified: Sat, 09 Dec 2023 03:49:08 GMT  
		Size: 17.0 KB (16978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8904c06ed725c823fba424cc4f89cdeb2fb7d56028de2fa98dc6ffe5049a9b5`  
		Last Modified: Sat, 09 Dec 2023 03:49:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a8b83e107a8ced7aa304bb19f46e7b439d6383523ee093bf807ba09e04fd71`  
		Last Modified: Sat, 09 Dec 2023 03:49:43 GMT  
		Size: 176.0 MB (176021694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeed4f7171d1035c5088b0bd27406ddf7fa3efb658f3df57bc126094e5cb166a`  
		Last Modified: Sat, 09 Dec 2023 03:49:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
